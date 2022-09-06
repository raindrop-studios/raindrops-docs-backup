# ItemUsages

An Item can be used as either a `Consumable` or `Wearable`. In fact, an Item can have many `ItemUsages` describing the different ways in which it may be used. For example, it may be that a legendary sword could both be worn and used in a spell - these are two different `ItemUsage`s in the array.

Both `ItemUsage`s can have `BasicItemEffect`s, which look like this:

```rust
#[derive(AnchorSerialize, AnchorDeserialize, Clone)]
pub struct BasicItemEffect {
    amount: u64,
    stat: String,
    item_effect_type: BasicItemEffectType,
    active_duration: Option<u64>,
    staking_amount_numerator: Option<u64>,
    staking_amount_divisor: Option<u64>,
    staking_duration_numerator: Option<u64>,
    staking_duration_divisor: Option<u64>,
    // point where this effect no longer applies
    max_uses: Option<u64>,
}
```

The primary difference is in the `ItemClassType` enum of your `ItemUsage`, which allows for different data storage depending on whether this item is being worn or consumed:

```rust
#[derive(AnchorSerialize, AnchorDeserialize, Clone)]
pub enum ItemClassType {
    Wearable {
        body_part: Vec<String>,
        limit_per_part: Option<u64>,
    },
    Consumable {
        max_uses: Option<u64>,
        // If none, is assumed to be 1 (to save space)
        max_players_per_use: Option<u64>,
        item_usage_type: ItemUsageType,
        cooldown_duration: Option<u64>,
        warmup_duration: Option<u64>,
    },
}
```

The `Wearable` enum is focused on scoping and limiting on a per-body-part basis, which is similar to the component scoping used by the `Components` array. It is up to the enclosing contract to enforce this.

The `Consumable` enum revolves around setting usage limits, how many players can use it in a given use, warmups and cooldowns.

{% hint style="info" %}
You may have noticed that both an `BasicItemEffect`s, and the `ItemUsage` itself, both can have `max_uses`. This is so that you can have different effects wear down before the item as a whole does.
{% endhint %}

There are a few `ItemUsageTypes` you can use:

```rust
#[derive(AnchorSerialize, AnchorDeserialize, Clone, PartialEq)]
pub enum ItemUsageType {
    Exhaustion,
    Destruction,
    Infinite,
}
```

{% hint style="info" %}
Please note that `Exhaustion` is not an allowable `ItemUsageType` for SFTs, nor is `max_uses` > 1.
{% endhint %}

`Exhaustion` means an Item will not be destroyed once `max_uses` hits zero (and `max_uses` is required for `Exhaustion`), but it will be rendered unusable for this particular `ItemUsage`.

`Destruction` means when `max_uses` hit zero (and it must be set for `Destruction`) will cause a token to be burned. For SFTs, with their required `max_uses` == 1, this means one token is burned per use.

`Infinite` is self-explanatory - `max_uses` is ignored or unset, and the item can be used forever. Not applicable to SFTs.

When you define an `ItemUsage`, it gets a corresponding `ItemUsageState` in any `Item` instance to keep track of usage, and cooldowns:

```rust
#[derive(AnchorSerialize, AnchorDeserialize, Clone)]
pub struct ItemUsageState {
    index: u16,
    uses: u64,
    activated_at: Option<u64>,
}
```

Obviously SFTs cannot have such state as all tokens in the SFT mint share the same Item PDA, which is why there are restrictions on them.

## Callbacks and Validation

Just a side note, each `ItemUsage` can have its own validation and callback (both of type `Callback`). Validations are CPIs that are called when the item is being activated, whereas callbacks are intended to be CPI’d from the enclosing contract when it is enacting the `Item`’s changes on its target(s). Here’s what a Callback looks like:

```rust
#[derive(AnchorSerialize, AnchorDeserialize, Clone)]
pub struct Callback {
    pub key: Pubkey,
    pub code: u64,
}
```

An example validation that will work on prod is a dummy endpoint added to the stubbed out Namespace contract. Here’s an example `ItemUsage` from an `ItemClass` definition JSON used for `create_item_class` calls that will make this work:

```json
{
          "index": 0,
          "basicItemEffects": null,
          "callback": null,
           "validation": {
            "key": "nameAxQRRBnd4kLfsVoZBBXfrByZdZTkh8mULLxLyqV",
            "code": 35
          },
          "usagePermissiveness": [{ "updateAuthority": true }],
          "inherited": { "notInherited": true },
          "itemClassType": {
            "consumable": {
              "maxUses": null,
              "maxPlayersPerUse": null,
              "itemUsageType": { "infinite": true },
              "cooldownDuration": 500,
              "warmupDuration": null
            }
          }
        }
```

Feel free to experiment with this. The additional `code` is a `u64` that is passed in just after the 8 bytes describing the instruction so it can be used for additional filtering. The contract implementing this must have a method called `item_validation` in its `main` module and must be an Anchor contract.
