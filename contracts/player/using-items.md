# Using Items

If an `Item` is in your backpack, and it has an `ItemUsage` in it's `ItemClass` that describes it as a `Consumable`, then your `Player` may use the item. Before going through a live example, let's walk through the theory.

#### Architecture

When a `Player` uses an `Item` via `use_item`, it will do a CPI to `begin_item_activation` to the underlying item contract, wherein it will create a `ItemActivationMarker` PDA owned by the item contract.

However, this `use_item` call does not actually affect the `Player`. It just begins the usage. This may mean that the `Item` is now in a warmup period or it may simply just mean that the `Item` now has a PDA registering its "activated."&#x20;

Either way, with this PDA in hand, the next step is to add the `Item's` effect to the `Player` using the `add_item_effect` call, wherein the `ItemActivationMarker` PDA will be destroyed through a CPI of `end_item_activation` to the underlying item contract. It will be exchanged for a `PlayerItemActivationMarker` PDA meant to keep track of information the player contract needs about what the `Item` is doing to the player throughout the lifecycle of the `Item's` use.

```json
pub struct PlayerItemActivationMarker {
    pub bump: u8,
    pub player: Pubkey,
    pub item: Pubkey,
    pub usage_index: u16,
    pub basic_item_effects: Option<Vec<BasicItemEffect>>,
    pub removed_bie_bitmap: Option<Vec<u8>>,
    pub amount: u64,
    pub activated_at: u64,
    pub active_item_counter: u64,
}
```

After this, the final call in the lifecycle of using an `Item` is to `subtract_item_effect` which will remove the effect from the `Player's` stats. In cases where the `Item` has a duration, this subtraction may not be callable until some time in the future. In cases where the `Item` has no duration (like a Potion that adds 20 health immediately), this subtraction is a no-op that simply returns lamports to you and deletes the PDA.

#### Example Walkthrough

TODO
