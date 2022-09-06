# State

### `ArtifactClass` and `Artifact`

```rust
#[account]
pub struct ArtifactClass {
    pub namespaces: Option<Vec<NamespaceAndIndex>>,
    pub parent: Option<Pubkey>,
    pub mint: Option<Pubkey>,
    pub metadata: Option<Pubkey>,
    /// If not present, only Destruction/Infinite consumption types are allowed,
    /// And no cooldowns because we can't easily track a cooldown
    /// on a mint with more than 1 coin.
    pub edition: Option<Pubkey>,
    pub bump: u8,
    pub existing_children: u64,
    pub data: ArtifactClassData,
}

#[account]
pub struct Artifact {
    pub namespaces: Option<Vec<NamespaceAndIndex>>,
    pub parent: Pubkey,
    pub mint: Option<Pubkey>,
    pub metadata: Option<Pubkey>,
    /// If not present, only Destruction/Infinite consumption types are allowed,
    /// And no cooldowns because we can't easily track a cooldown
    /// on a mint with more than 1 coin.
    pub edition: Option<Pubkey>,
    pub bump: u8,
    pub tokens_staked: u64,
}
```

`ArtifactClass` is an alias of `ItemClass` / `PlayerClass` and `Artifact` is an alias of `Item` / `Player`. In other words, `ArtifactClass` can be `ItemClass` or `PlayerClass` and `Artifact` can be `Item` or `Player`. Artifacts and ArtifactClasses are not actually stored on-chain. They are only used for deserialize them to the same structure as they have their own structure in their own contracts and make them easy to manage in the staking contract.&#x20;

### `StakingCounter`

```rust
#[account]
pub struct StakingCounter {
    pub bump: u8,
    pub event_start: i64,
    pub event_type: u8,
}
```

`StakingCounter` records the type and start time of every staking process. If `event_type` is 0, the staking process is in warmup state and if `event_type` is 1, the staking process is in cooldown state.
