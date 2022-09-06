# State

The layout of Match is fairly simple - one defines a match that acts as a state machine, and gives it an oracle that can be controlled by a third party that can define outcomes. The match can define TokenValidations by which people are allowed to enter, and the oracle can define TokenDeltas by which tokens are redistributed to the entrants in the match.

```rust
#[account]
pub struct Match {
    namespaces: Option<Vec<NamespaceAndIndex>>,
    // Win oracle must always present some rewards struct
    // for redistributing items
    win_oracle: Pubkey,
    win_oracle_cooldown: u64,
    last_oracle_check: u64,
    authority: Pubkey,
    state: MatchState,
    leave_allowed: bool,
    minimum_allowed_entry_time: Option<u64>,
    bump: u8,
    /// Increased by 1 every time the next token transfer
    /// in the win oracle is completed.
    current_token_transfer_index: u64,
    token_types_added: u64,
    token_types_removed: u64,
    token_entry_validation: Option<Vec<TokenValidation>>,
    token_entry_validation_root: Option<Root>,
    join_allowed_during_start: bool,
}

#[derive(AnchorSerialize, AnchorDeserialize, Clone, PartialEq)]
pub enum MatchState {
    Draft,
    Initialized,
    Started,
    Finalized,
    PaidOut,
    Deactivated,
}

// To transfer a player token, make it a Normal type
// and use it as the mint
// To transfer item from player a to b, use player to player
// and from and to are the player pubkeys, with item mint being mint
// To transfer item from player a to entrant b, use PlayerToEntrant
// from is the player pubkey, to is the wallet to which item is going.
#[derive(AnchorSerialize, AnchorDeserialize, Clone)]
pub struct TokenDelta {
    // Is either player pda, or original wallet that moved token in
    from: Pubkey,
    /// if no to, token is burned
    // can be player pda, or new wallet to send to.
    to: Option<Pubkey>,
    token_transfer_type: TokenTransferType,
    mint: Pubkey,
    amount: u64,
}
// Oracles must match this serde
#[account]
pub struct WinOracle {
    finalized: bool,
    token_transfer_root: Option<Root>,
    token_transfers: Option<Vec<TokenDelta>>,
}

#[derive(AnchorSerialize, AnchorDeserialize, Clone, PartialEq)]
pub enum TokenType {
    /// No missions explicitly.
    Player,
    Item,
    Any,
}

#[derive(AnchorSerialize, AnchorDeserialize, Clone, PartialEq)]
pub enum TokenTransferType {
    /// No missions explicitly.
    PlayerToPlayer,
    PlayerToEntrant,
    Normal,
}

#[derive(AnchorSerialize, AnchorDeserialize, Clone)]
pub enum Filter {
    None,
    All,
    Namespace { namespace: Pubkey },
    Parent { key: Pubkey },
    Mint { mint: Pubkey },
}

#[derive(AnchorSerialize, AnchorDeserialize, Clone)]
pub struct TokenValidation {
    filter: Filter,
    is_blacklist: bool,
    validation: Option<Callback>,
}
```
