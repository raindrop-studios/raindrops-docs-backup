# Build

All Items start as bare-bones NFTs or SFTs that were previously made before starting the build process. You can either attempt to make them in the same transaction or bring them in from a prior. The Raindrops contracts _expect_ them to **pre-exist**.

As a reminder, an NFT is a mint with supply = 1, decimals = 0, and both a Metadata and Edition or MasterEdition struct from the Token Metadata program.

An SFT is a mint with supply > 0, decimals = 0, and **ONLY** a Metadata struct from the Token Metadata program. Ideal uses for SFTs are single-use items like Potions so that you do not need to create a new mint for each potion. SFT-based items **cannot** have stateful usage types, such as a cooldown period.

To build an `Item` from an `ItemClass`:

1. Create an Item Escrow in which to store components from a specific component scope (recipe) for a specific index.
2. Add or burn or prove absence of required components against the escrow
3. Start the build phase
4. If there is no build time, building can be ended immediately. Otherwise, it must be ended once the build time duration has passed.
5. Now the NFT or SFT provided has a new `Item` PDA with seeds `[’item’, mint_id, index]`, where index is some `u64` > 0 that corresponds to the index used to initialize the Item escrow.

{% hint style="info" %}
Presently the CLI has the low-level commands for #1-5 but does not have a higher level smart command that can produce all these commands in aggregated transactions. We will be adding a single CLI build command where recipes are read and transactions are built to minimize overhead across all steps.
{% endhint %}

Let’s walk through how to create an item using the low-level commands. First, you’ll need a JSON file describing what you are trying to do:

```json
{
  "newItemMint": "DQKJRRHjyiS1DgDuMWtdD2Cy2nbLqEP86sQ8nnBQMv2w",
  "itemClassMint": "Hz5x6myaWWSKKzAhh2LHA5YmXExLiyTfj89S9zXyT17M",
  "amountToMake": 1,
  "namespaceIndex": null,
  "buildPermissivenessToUse": { "parentTokenHolder": true },
  "classIndex": 10,
  "newItemIndex": 10,
  "craftEscrowIndex": 1,
  "componentScope": "set1",
  "parent": {
    "mint": "Hz5x6myaWWSKKzAhh2LHA5YmXExLiyTfj89S9zXyT17M",
    "index": 9
  },
  "originator": "44kiGWWsSgdqPMvmqYgTS78Mx2BKCWzduATkfY4biU97",
  "merkleInfo": null,
  "totalSpaceBytes": 200,
  "storeMetadataFields": false,
  "storeMint": false,
  "metadataUpdateAuthority": "44kiGWWsSgdqPMvmqYgTS78Mx2BKCWzduATkfY4biU97",
  "components": [
    {
      "mint": "5VDCnw9NADV4Bwr2x6wXcyNXU5EuWWksfceUtk7nxubm",
      "index": 1
    }
  ]
}
```

You’ll need to give the mints for both the new `Item`, and the existing `ItemClass`. You’ll need to indicate to the `ItemClass` which build permissiveness you want to use as this will determine what accounts the CLI will be passing up to authenticate you.

For every `Item` or `ItemClass`, it has a specific index offset against the mint to allow the creation of multiple classes and instances from the same mint, and you’ll need to indicate which you want to use for this creation.

The `craftEscrowIndex` is used to allow you to have multiple builds progressing for the same `ItemClass` against the same mint should you need it.

Components in the recipe list each come tagged with a `componentScope`. When you choose a specific scope here, you are required only to provide components that have that tag. Imagine each scope as a different recipe to make the same Item.

If your `ItemClass` has itself a parent `ItemClass`, the `parent` field will need to be set. If not, it can be null.

`originator` is an optional field that should be used if those adding components to the escrow will not be the same signer as the one who starts the escrow.

When creating `Item`s or `ItemClass`es, you get to specify how much space you want to spend. In Solana 1.8 this space is fixed, so think carefully about how much data you plan to store on chain for this `Item` before setting this. Depending on `ItemUsageState`s, `Item`s can be quite inexpensive.

The `components` list is a list of actual `Item` mints (and their `index` offsets) you plan to use when assembling the `component`s. This is as opposed to the `component` list on the `ItemClass` struct itself, which describes what `ItemClass`_es_ **must** be present. This list lets you choose _which_ instance of a given `ItemClass` you will use in this build.

Once this is setup, here are the commands, in sequence, that must be run for a single-component recipe:

```bash
item-cli create_item_escrow \
         -k <keypair> \
         --env devnet \
         -cp example-configs/createItem.json
         
# If components are required, run:
item-cli add_craft_item_to_escrow \
         -k <keypair> \
         -i 0 \
         -a 1 \
         --env devnet \
         -cp example-configs/createItem.json
         
item-cli start_item_escrow_build_phase \
         -k <keypair> \
         --env devnet \
         -cp example-configs/createItem.json
         
item-cli complete_item_escrow_build_phase \
         -k <keypair> \
         --env devnet \
         -cp example-configs/createItem.json
         
# Drain the craft item from escrow for lamports and get back item possibly
item-cli remove_craft_item_from_escrow \
         -k <keypair> \
         -i 0 \
         -a 1 \
         --env devnet \
         -cp example-configs/createItem.json
         
# Drain item escrow of lamports
item-cli drain_item_escrow \
         -k <keypair> \
         --env devnet \
         -cp example-configs/createItem.json
```

Some things to note here: the `-i` when adding and removing dictate what `index` in the `component` list you are trying to add (you should always start with 0 and move in order) and the `-a` indicates how many of that item you are adding (most of the time, 1.)

If your recipe has a build time, `complete_item_escrow_build_phase` will error out until that duration has passed. It is also important, but not required, to remember to run `remove_craft_item_from_escrow` _even if_ the `Item` was destroyed as part of the crafting, as you will at the very least reclaim lamports for the token account on the escrow side.

The new `Item` PDA is setup during the `complete_item_escrow_build_phase` step. At this point, the item is now usable.

Want to see what you built? Run this:

```bash
item-cli show_item \
         -k <keypair> \
         --env devnet \
         -m DQKJRRHjyiS1DgDuMWtdD2Cy2nbLqEP86sQ8nnBQMv2w \
         -i 10
```

You’ll need to supply the `mint` and `index` offset.

Or from the client side:

<pre class="language-typescript"><code class="lang-typescript">import { ItemProgram, Utils } from "@raindrops-protocol/raindrops";
<strong>
</strong><strong>const getItem = async(
</strong>	mint: web3.PublicKey,
	itemIndex: BN,
	wallet: Wallet,
	env: string,
	customRpcUrl: string
) => {
    const [itemKey] = await Utils.PDA.getItemPDA(
      mint,
      itemIndex
    );
<strong>    const itemProgram = ItemProgram.getProgramWithWallet(
</strong>        ItemProgram,
        anchorWallet as Wallet,
        env,
        customRpcUrl
      );
    return (await itemProgram.client.account.item.fetch(
        itemKey
      )) as unknown as FetchedItem;
};
</code></pre>

Want to cut out before you finish crafting? Simply deactivate and reclaim lamports:

```bash
item-cli deactivate_item_escrow \
         -k <keypair> \
         --env devnet \
         -cp example-configs/createItem.json

# Drain the craft item escrow for lamports and get back item possibly
item-cli remove_craft_item_from_escrow \
         -k <keypair> \
         -i 0 \
         -a 1 \
         --env devnet \
         -cp example-configs/createItem.json

# Drain item escrow of lamports
item-cli drain_item_escrow \
         -k <keypair> \
         --env devnet \
         -cp example-configs/createItem.json
```
