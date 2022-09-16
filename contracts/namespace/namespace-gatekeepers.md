# Namespace Gatekeepers

Namespace Gatekeepers are responsible for filtering which artifacts are allowed to be joined to a given Namespace. Each Namespace can only have one Gatekeeper but the Gatekeeper can have multiple filters attached, an artifact must pass all filters to be eligible to join a Namespace. To reiterate, Gatekeepers only filter on initial Joining actions to Namespaces, they do not filter on caching artifacts.

## Filters

There are 2 different filter types and each type can be applied independently to each different type of artifact.

### Filter Types

```rust
pub enum Filter {
    Namespace {
        namespaces: Vec<Pubkey>,
    },
    Key {
        key: Pubkey,
        mint: Pubkey,
        metadata: Pubkey,
        edition: Option<Pubkey>,
    },
}
```

* Namespace: Filters on an array of Namespaces
* Key: _PARTIALLY\_IMPLEMENTED,_ Filters on arbitrary accounts, currently only `mint` is implemented.

### Permissiveness

Permissiveness defines how the Filter Types are applied to a given Artifact when joining a Namespace

### Permissiveness Types

```rust
pub enum Permissiveness {
    All,
    Whitelist,
    Blacklist,
    Namespace,
}
```

* All: Automatically passes the filter, nothing is checked
* Whitelist: Artifact must match the filter
* Blacklist: Artifact must not match the filter
* Namespace: Artifact token holder must sign the transaction for it to be joined to the Namespace.

### Permissiveness Settings

```rust
pub struct PermissivenessSettings {
    namespace_permissiveness: Permissiveness,
    item_permissiveness: Permissiveness,
    player_permissiveness: Permissiveness,
    match_permissiveness: Permissiveness,
    mission_permissiveness: Permissiveness,
    cache_permissiveness: Permissiveness,
}
```

During the initialization of a Namespace, PermissivenessSettings are defined for each artifact that can be joined to a Namespace. This allows granular permissives to be applied. For example, an Item can have a Permissiveness set to Whitelist while a Match can be set to Blacklist, both of these artifacts will run through the same set of filters but evaluated in opposite ways.
