---
description: Accounts and Data Structures
---

# State

```rust
// seeds = [authority_mint]
#[account]
pub struct Event {
    pub name: String,
    pub authority_mint: Pubkey,
    pub points_mint: Pubkey,
    pub event_participant_mint: Pubkey,
    pub state: EventState,
    pub contest_index: u64,
    pub reward_index: u64,
    pub max_participants: u64,
    pub event_entry_fee: Option<EntryFee>,
    pub event_token_gate: Option<TokenGate>,
}
```

```rust
// seeds = ['contest', event, index]
#[account]
pub struct Contest {
    pub name: String,
    pub event: Pubkey,
    pub authority_mint: Pubkey,
    pub points_mint: Pubkey,
    pub contest_participant_mint: Pubkey,
    pub state: ContestState,
    pub index: u64,
    pub max_participants: u64,
    pub join_by_authority: bool,
    pub contest_entry_fee: Option<EntryFee>,
    pub contest_token_gate: Option<TokenGate>,
}
```

```rust
// seeds = ['reward', event, index]
#[account]
pub struct Reward {
    pub event: Pubkey,
    pub reward_mint: Pubkey,
    pub reward_escrow: Pubkey,
    pub reward_index: u64,
}
```

```rust
pub enum EventState {
    Initializing, // Event has been created and participants may now enter
    Started, // No more participants can enter the Event
    Ended, // No more contests can be created
    Finalized, // All rewards and revokes have been determined, Event becomes immutable
}
```

```rust
pub enum ContestState {
    Initializing, // Contest has been created and participants may now enter
    Started, // No more participants can enter the Contest
    Ended, // Contest has completed, results are being finalized
    Finalized, // Contest points have been distributed, Contest is now immutable
}
```

```rust
pub struct TokenGate {
    pub mint: Pubkey,
    pub amount: u64,
}
```

```rust
pub struct EntryFee {
    pub mint: Pubkey,
    pub vault: Pubkey,
    pub amount: u64,
}
```
