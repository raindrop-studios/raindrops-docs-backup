# BodyParts

Every `Player` may have `BodyParts` if it so chooses. In the `PlayerClass`, they are defined as:

```rust
pub struct BodyPart {
    pub index: u16,
    pub body_part: String,
    pub total_item_spots: Option<u64>,
    pub inherited: InheritanceState,
}
```

On the actual `Player` there is no corresponding state, as the only stateful part of a `BodyPart` is what is equipped on it, and this is contained in the `equipped_items` array. You'll notice that each `BodyPart` has its own index - this, like `BasicStats`, is a required unique field, to help disambiguate parts.

{% hint style="info" %}
It's possible for a `BodyPart` to equip more than one item (see `total_item_spots`).
{% endhint %}
