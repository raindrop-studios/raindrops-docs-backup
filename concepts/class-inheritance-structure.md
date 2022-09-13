# Class Inheritance Structure

It is a pain to have to redefine the _same_ stats for different player or item NFTs across many unique NFT mints, as well as **costly**. The Raindrops Protocol avoids this by taking the stance that object inheritance is useful, and an object class should be it’s own NFT. Just as an NFT is simply two structs from the Token Metadata program that live on top of a token (specifically the `Metadata` and `Master Edition` structs), Raindrops adds additional structs on top of that NFT depending if that NFT represents a Class or an Instance of some Class.

One object class NFT can inherit from another class NFT, and all existing object instances should inherit from an existing object class NFT.

Both the [Player](https://github.com/long-banana/raindrops-docs/blob/main/concepts/broken-reference/README.md) and [Item](https://github.com/long-banana/raindrops-docs/blob/main/concepts/broken-reference/README.md) contract behave this way, with `PlayerClass` structs and `ItemClass` storing configurational information about what makes up this kind of `Player` or `Item` (like `BodyParts`, `BasicStats` like strength, or what `BasicItemEffects` an item should have), and the actual `Player` and `Item` instance structs are slimmed down data that only contain stateful information specific to that given NFT, like whether the strength is 5, or if the item was used 5 minutes ago.

For an example of this, here is an `ItemUsage`(Configurational data from an `ItemClass`) and an `ItemUsageState`(Stateful information from an `Item` that is a child of this class):

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

`ItemUsage` defines how a given `Item` may be **used**, and an `Item` can be used in _many_ ways. However, the `ItemClass` doesn’t actually get used - it is a blueprint for creating `Item` instances. When made, `Items` don’t all contain this massive struct in their PDAs, they instead contain a trimmed down `ItemUsageState` for the `ItemUsage` defined within their parent `ItemClass` class. This keeps the `Items` and `Players` relatively small as PDAs.
