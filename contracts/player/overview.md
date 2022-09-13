# State

Here's a pseudo-code rendering of the PlayerClass state with all the structs merged together so that you can see it "all in one".

```rust
pub struct PlayerClass {
    pub namespaces: Option<Vec<NamespaceAndIndex>>,
    pub parent: Option<Pubkey>,
    pub mint: Option<Pubkey>,
    pub metadata: Option<Pubkey>,
    pub edition: Option<Pubkey>,
    pub data: PlayerClassData,
    pub existing_children: u64,
    pub bump: u8,
}

pub struct PlayerClassData {
    pub settings: PlayerClassSettings,
    pub config: PlayerClassConfig,
}

pub struct PlayerClassSettings {
    pub default_category: Option<PlayerCategory>,
    pub children_must_be_editions: Option<Boolean>,
    pub builder_must_be_holder: Option<Boolean>,
    pub update_permissiveness: Option<Vec<Permissiveness>>,
    pub instance_update_permissiveness: Option<Vec<Permissiveness>>,
    pub build_permissiveness: Option<Vec<Permissiveness>>,
    pub equip_item_permissiveness: Option<Vec<Permissiveness>>,
    pub add_item_permissiveness: Option<Vec<Permissiveness>>,
    pub use_item_permissiveness: Option<Vec<Permissiveness>>,
    // if not set, assumed to use equip permissiveness
    pub unequip_item_permissiveness: Option<Vec<Permissiveness>>,
    // if not set, assumed to use remove item permissiveness
    pub remove_item_permissiveness: Option<Vec<Permissiveness>>,
    pub staking_warm_up_duration: Option<u64>,
    pub staking_cooldown_duration: Option<u64>,
    pub staking_permissiveness: Option<Vec<Permissiveness>>,
    // if not set, assumed to use staking permissiveness
    pub unstaking_permissiveness: Option<Vec<Permissiveness>>,
    pub child_update_propagation_permissiveness: Option<Vec<ChildUpdatePropagationPermissiveness>>,
}

pub struct PlayerClassConfig {
    pub starting_stats_uri: Option<StatsUri>,
    pub basic_stats: Option<Vec<BasicStatTemplate>>,
    pub body_parts: Option<Vec<BodyPart>>,
    pub equip_validation: Option<Callback>,
    pub add_to_pack_validation: Option<Callback>,
}

```



`PlayerClass` is cut into two major areas: The settings and the config. The settings mostly covers who may do what to either the class or its children. There is even a permissiveness (`child_update_propagation_permissiveness`) that covers which permissions and data propagate to children!&#x20;

The config focuses on what most devs classically recognize as the "definition" of a `Player`.  You can define `BodyParts`, `BasicStats`, which in their blueprint form are called `BasicStatTemplates`, and the starting URI for each `Player` in this class. `Players` will inherit this information as their starting state.

{% hint style="info" %}
You can describe a starting URI as some third party link, similar to the URI in Token Metadata. Maybe it's JSON, maybe it's an image, it can be anything you like. All instantiated `Player` from this `PlayerClass` will start with it, and it should contain richer data about the `Player` that cannot be contained within `BodyParts` or `BasicStats`. It works via 'write-on-change' so when you make an update to `Player`, you can change it to a new URI that represents a small shift away from the common starting URI all `Players` of the same class share.
{% endhint %}

{% hint style="info" %}
Any change to a `PlayerClass` can be permissionlessly propagated to all `Players` via a hit to the update\_player endpoint on the `Player` contract for each `Player`. So feel free to add a new body part to the Warrior class if you need it!&#x20;
{% endhint %}

Here is the Player state:

```rust
pub struct Player {
    pub namespaces: Option<Vec<NamespaceAndIndex>>,
    // extra byte that is always 1 to simulate same structure as player class.
    pub padding: u8,
    pub parent: Pubkey,
    pub class_index: u64,
    pub mint: Option<Pubkey>,
    pub metadata: Option<Pubkey>,
    pub edition: Option<Pubkey>,
    pub bump: u8,
    pub tokens_staked: u64,
    pub active_item_counter: u64,
    pub items_in_backpack: u64,
    pub data: PlayerData,
    pub equipped_items: Vec<EquippedItem>,
}

pub struct EquippedItem {
    item: Pubkey,
    amount: u64,
    index: u16,
}

pub struct PlayerData {
    pub stats_uri: Option<StatsUri>,
    pub category: Option<PlayerCategory>,
    pub basic_stats: Option<Vec<BasicStat>>,
}

```

The `Player` state is much smaller than the `PlayerClass` and is sort of the yin to the class's yang - it contains only the stateful pieces of information that vary from `Player` to `Player`. For instance, there is an array of equipped items, and for each `BasicStatTemplate`, a corresponding `BasicStat` that represents the current state of that Stat.&#x20;

{% hint style="info" %}
You'll also notice that, as with Items, it's possible for the `PlayerClass` and `Player` to be either entirely separate NFTs or indeed, the SAME NFT! Due to the index system used with the PDA seeds, you could have the same NFT have a class defined at index 0, and its instance defined at index 1. This would be the Singleton pattern for those of you familiar with OO programming styles.
{% endhint %}
