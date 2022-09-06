# Class Inheritance Structure

It is a pain to have to redefine the _same_ stats for different player or item NFTs across many unique NFT mints, as well as **costly**. The Raindrops Protocol avoids this by taking the stance that object inheritance is useful, and an object class should be it’s own NFT.

An object class can inherit from another, and all existing object instances should inherit from an existing object class NFT.

Both the [Player](https://github.com/long-banana/raindrops-docs/blob/main/concepts/broken-reference/README.md) and [Item](https://github.com/long-banana/raindrops-docs/blob/main/concepts/broken-reference/README.md) contract behave this way, with `PlayerClass` structs and `ItemClass` structs living on top of their own NFTs where configuration data is stored, and the actual Player and Item instance structs being slimmed down structs that only contain stateful information specific to that NFT.

For an example of this, here is an `ItemUsage`(Object class, configuration data) and an `ItemUsageState`(Object instance, stateful information):

```rust
pub struct ItemUsage {
    index: u16,
    basic_item_effects: Option<Vec<BasicItemEffect>>,
    usage_permissiveness: Vec<PermissivenessType>,
    inherited: InheritanceState,
    item_class_type: ItemClassType,
    callback: Option<Callback>,
    validation: Option<Callback>,
    do_not_pair_with_self: bool,
    dnp: Option<Vec<DNPItem>>,
}

pub struct ItemUsageState {
    index: u16,
    uses: u64,
    activated_at: Option<u64>,
}
```

An `ItemUsage` will have a _has\_many_ relationship with an `ItemClass` and is embedded within the `ItemClass`.

`ItemUsage` defines how a given item may be **used**, and an item can be used in _many_ ways. However, the `ItemClass` doesn’t actually get used - it is a blueprint for creating `Item` instances. When made, `Item`s don’t all contain this massive struct in their PDAs, they instead contain a **single** trimmed down `ItemUsageState` for each `ItemUsage` defined within their parent `ItemClass` class.
