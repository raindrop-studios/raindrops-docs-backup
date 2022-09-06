# Namespace Actions

## Namespace Initialization

Creating a Namespace should be the first step when designing how to store state with Raindrops. During Namespace creation, it's possible to configure many variables, like which Staking mints are allowed to be staked, caching parameters and naming schemes. Creating Namespace Gatekeepers is also a configurable aspect to initialization, these Gatekeepers can have filters that determine which Artifacts are eligible to be joined to your new Namespace.

## Namespace Joining

After a Namespace is created, next create a Raindrops artifact, these can be Item's, Matches or Players. After an Artifact is created, try joining it to a Namespace. Joining artifacts to a namespace allow you to associate and index them in different ways depending on your use case. It's possible to query for all Artifacts that belong to a given Namespace very easily.

## Namespace Caching

Artifacts which are joined to a Namespace can subsequently be cached to the same Namespace. If an Artifact needs to be removed from a Namespace, it's first removed from the namespace's cache. Caching enables easy lookup of an Artifact's Namespaces.

```rust
// An Index containing cached Artifacts in the Namespace Account
pub struct NamespaceIndex {
    pub namespace: Pubkey,
    pub bump: u8,
    pub page: u64,
    pub caches: Vec<Pubkey>,
}

// A field in an Artifact Account, this denotes which Namespace it's cached and at what index
pub struct NamespaceAndIndex {
    namespace: Pubkey,
    index: Option<u64>,
    inherited: InheritanceState,
}
```

### Full Artifact Namespace Lifecycle

\
These directions use the CLI, the example configuration is simply to understand the JSON structure you need to provider, use your own payloads.



Setup

```bash
git clone git@github.com:raindrops-protocol/raindrops.git && cd raindrops/js
```



Artifact Created

```bash
ts-node cli/src/item.ts create_item_class -k ~/.config/solana/id.json -cp cli/example-configs/item/createItem.json -e devnet -r https://devnet.genesysgo.net
```

Namespace Initialized

```bash
ts-node cli/src/namespace.ts initialize_namespace -k ~/.config/solana/id.json -cp cli/example-configs/namespace/initializeNamespace.json -e devnet -r https://devnet.genesysgo.net
```

Namespace Gatekeeper created

```bash
ts-node cli/src/namespace.ts create_namespace_gatekeeper -k ~/.config/solana/id.json -cp cli/example-configs/namespace/createNamespaceGatekeeper.json -e devnet -r https://devnet.genesysgo.net
```

Artifact Joins a Namespace

```bash
ts-node cli/src/namespace.ts join_namespace -k ~/.config/solana/id.json -cp cli/example-configs/namespace/joinNamespace.json -e devnet -r https://devnet.genesysgo.net
```

Cache Artifact to the Namespace

```bash
ts-node cli/src/namespace.ts cache_artifact -k ~/.config/solana/id.json -cp cli/example-configs/namespace/cacheArtifact.json -e devnet -r https://devnet.genesysgo.net
```

Artifact Removed from Namespace Cache

```bash
ts-node cli/src/namespace.ts uncache_artifact -k ~/.config/solana/id.json -cp cli/example-configs/namespace/uncacheArtifact.json -e devnet -r https://devnet.genesysgo.net
```

Artifact Leaves a Namspace

```bash
ts-node cli/src/namespace.ts leave_namespace -k ~/.config/solana/id.json -cp cli/example-configs/namespace/leaveNamespace.json -e devnet -r https://devnet.genesysgo.net
```
