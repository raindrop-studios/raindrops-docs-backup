# Item Validations

When `Items` are added/removed to/from backpacks, the Player program checks for the presence of an `add_to_pack_validation` on the `PlayerClass` of the `Player`. If set, this callback is called, and if it fails, then the `add_item` or `remove_item` call fails. This can be quite useful for making sure users cannot add items that are too powerful to packs, or something like that.

The key layout for this callback's args is:

```rust
 let keys = vec![
            AccountMeta::new_readonly(item.key(), false),
            AccountMeta::new_readonly(item_class.key(), false),
            AccountMeta::new_readonly(player.key(), false),
            AccountMeta::new_readonly(player_class.key(), false),
            // The token account in your wallet (an ATA)
            AccountMeta::new_readonly(item_account.key(), false),
            // The account the item token is being transferred into
            AccountMeta::new_readonly(player_item_account.key(), false),
            AccountMeta::new_readonly(item_mint.key(), false),
        ];

    
```

If the call is `add_item`, it will try to call a method on your callback contract called `add_item_validation` and if it's `remove_item`, it will be `remove_item_validation`. The args passed will be:

```rust
pub struct AddOrRemoveItemValidationArgs {
    // For enum detection on the other end.
    pub instruction: [u8; 8],
    pub extra_identifier: u64,
    pub amount: u64,
    pub player_mint: Pubkey,
    pub item_permissiveness_to_use: Option<PermissivenessType>,
}
```

This Callback expects an Anchor program on the other end, so if it isn't one, God have mercy on your soul.
