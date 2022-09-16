# Backpackin'

All `Players` come with the ability to add `Items` to their backpacks. They can even add other `Players` to their backpack too, provided those `Players` are also declared to be `Items`, something completely possible in the Raindrops framework. Something to think about here would be multiple fighters being stored in a Battlecruiser. Here's how to add an `Item` to a `Player`. First, you'll need a JSON file that meets the following basic format:

```json
{
  "playerMint": "edo3DzeqXsFzoaEhGHVn1GRCcFf4CWTaUSU4DDDVpJY",
  "playerClassMint": "GwB8ZtjDXYNR4iheuSS2uLa7EYC9J7b8yaRY9YmXXqUh",
  "addItemPermissivenessToUse": { "tokenHolder": true },
  "index": 3,
  "metadataUpdateAuthority": null,
}

```

and `metadataUpdateAuthority` need only be present if you plan to use `updateAuthority` as `updatePermissivenessToUse` instead of something else. The `playerMint` key is the mint of the `Player` you wish to add the item to, and the `playerClassMint` is the mint of the class that spawned that `Player`. The index is the offset on the `playerMint`. You can read more about index offsets [here](../../../concepts/indexing.md).&#x20;

Then you can issue call from the player-cli using this json file and a few additional arguments, which we'll break down:

```bash
player-cli add_item -cp myconfig.json     
        -k ~/new-metaplex/mykey.json --log-level debug 
        -e mainnet-beta 
        -m 7LmihZJPobESB6nrWwk8xPneNFdeVACwg7PSjdAMrkPV 
        -i 1  
        -a 1 
        -cm 7t5G3x4Zq5p2ZbAX8owcSi1tiLwLwYTDMJc1FmAYYpb7
```

In this command, -m is saying the `Item` mint I wish to add is 7lmih, it's index offset is 1, the amount of that `Item` is 1(this could be an SFT `Item` like a Potion that has many, hence the explicitness), and then finally the -cm stands for "Class Mint", which in this case is 7t5G3x, and points at the `ItemClass` mint for this particular `Item`. Between the config file passed and the arguments provided, the `player-cli` is able to construct the command for the Player contract to have it move the `Item` from your wallet to your `Player's` backpack!

{% hint style="info" %}
A similar command called remove\_item exists that operates in reverse and takes the same commands.
{% endhint %}

If you wish to operate this command from your website, you can use the Raindrops SDK, which will look more like this:

```typescript
  await (
      await anchorProgram.addItem(
        {
          index: playerIndex,
          addItemPermissivenessToUse:
            config.addItemPermissivenessToUse ||
            config.updatePermissivenessToUse,
          playerMint,
          amount: new BN(amount),
          itemIndex,
        },
        {
          itemMint,
          metadataUpdateAuthority: config.metadataUpdateAuthority
            ? new PublicKey(config.metadataUpdateAuthority)
            : keypair.publicKey,
        },
        {
          itemProgram,
          playerClassMint: new PublicKey(config.playerClassMint),
          itemClassMint: classMint ? new PublicKey(classMint) : null,
        }
      )
    ).rpc();
  });
```

When added, the `Item` token account is stored as a PDA relative to the `Player` PDA with seeds `[ PREFIX.as_bytes(), item.key().as_ref(), player.key().as_ref() ]` It is explicitly not an associated token account, as to make it one would require an additional nested CPI which is a waste of CPU.

The benefit of this design is that your `Player` can carry many items while appearing as a single NFT in your wallet. Only `Items` carried by your `Player` can be equipped.&#x20;
