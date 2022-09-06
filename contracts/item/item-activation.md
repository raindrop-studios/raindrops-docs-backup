# Item Activation

Okay so you’ve defined your `ItemClass`, instantiated an `Item`, and now you want to use it. What does that mean? Well, with composability as a central tenet of this protocol, it means that the Item contract should only be responsible for validating that it is _possible_ to use an `Item`, and then provide _proof_ that you have decided to use the `Item`. It is then the responsibility of the enclosing contract to call the Item contract back to let it know that the `Item` has been used, and the activation period is over. Given the “price” of activation is paid up front, not calling back the Item contract simply means you cannot use this `Item` again until you do.

To activate an `Item`, you issue a `begin_item_activation` call with a JSON file like so:

```json
{
  "itemMint": "DQKJRRHjyiS1DgDuMWtdD2Cy2nbLqEP86sQ8nnBQMv2w",
  "index": 10,
  "itemClassMint": "Hz5x6myaWWSKKzAhh2LHA5YmXExLiyTfj89S9zXyT17M",
  "classIndex": 10,
  "itemMarkerSpace": 37,
  "usagePermissivenessToUse": { "updateAuthority": true },
  "amount": 1,
  "usageIndex": 0,
  "originator": null,
  "metadataUpdateAuthority": "44kiGWWsSgdqPMvmqYgTS78Mx2BKCWzduATkfY4biU97"
}
```

{% hint style="info" %}
itemMarkerSpace must have a value in the range of 20 to 66, inclusive
{% endhint %}

```bash
item-cli begin_item_activation \
         -k <keypair> \
         --env devnet \
         -cp example-configs/activateItem.json
```

This creates an `ItemActivationMarker` that acts as a kind of ticket that other programs can use as proof of use:

```rust
#[account]
pub struct ItemActivationMarker {
    bump: u8,
    valid_for_use: bool,
    amount: Option<u64>,
    // In the case we need to reset root, we want to use
    // timestamp from original activation
    unix_timestamp: u64,
    proof_counter: Option<ItemActivationMarkerProofCounter>,
}
```

{% hint style="warning" %}
Note that if you used a `validation` key in the `ItemUsage` being provided, it will be called during this `begin_item_activation` stage. This allows you to hook into item use with custom feedback. It is up to your enclosing program to call the `callback` after the enactment. What accounts (writable or otherwise) that you send in a callback is up to you - validation has a preset format that must be followed.
{% endhint %}

You can provide this PDA address to any enclosing program and they can validate that the `Item` is valid for use (i.e. past it’s warmup state if one is specified) and how many of that item is being used (mostly going to be 1 but if it’s an SFT it could potentially be many).

Once your enclosing contract has “enacted” the changes the `Item`’s `ItemClass` describes, it can make a CPI call to `end_item_activation`, or you can use the CLI:

```bash
item-cli end_item_activation \
         -k <keypair> \
         --env devnet \
         -cp example-configs/activateItem.json
```

{% hint style="info" %}
If your `Item` contains a warmup period, you may need to use this additional command after beginning item activation to push it into “valid\_for\_use” after the warmup duration:
{% endhint %}

```bash
item-cli update_valid_for_use_if_warmup_passed \
         -k ~/cope.json \
         --env devnet \
         -cp example-configs/activateItem.json
```
