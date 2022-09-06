# Namespace

### Introduction

All Artifacts like an Item or a Match can be joined and then cached to a Namespace. This extends to other Namespaces. Namespaces within namespaces allow you to create hierarchies/groupings of artifacts for fine-grained organization and indexability of your Artifacts. This greatly speeds up query speeds and accessibility within a large collection of Artifacts.

When an Artifact is first created, the creator can define the number of Namespaces an Artifact may join, which can be changed at any time through the UpdateNamespace instruction.

### Account Spec

```rust
/// seed ['namespace', namespace program, mint]
#[account]
pub struct Namespace {
    pub namespaces: Option<Vec<NamespaceAndIndex>>,
    pub mint: Pubkey,
    pub metadata: Pubkey,
    pub master_edition: Pubkey,
    pub uuid: String,
    pub pretty_name: String,
    pub artifacts_added: u64,
    pub max_pages: u64,
    pub full_pages: Vec<u64>,
    pub artifacts_cached: u64,
    pub permissiveness_settings: PermissivenessSettings,
    pub bump: u8,
    pub whitelisted_staking_mints: Vec<Pubkey>,
    pub gatekeeper: Option<Pubkey>,
}
```

### Instructions Overview

* initializeNamespace: Create a Namespace with the desired configuration
* updateNamespace: Update the Namespace configuration
* cacheArtifact: Add a Raindrops Artifact to the Namespace's cache, remember the Artifact can be another Namespace.
* uncacheArtifact: Remove an Artifact from the Namespace cache, this is necessary to remove an Artifact from a Namespace completely.
* createNamespaceGatekeeper: Initialize a Gatekeeper which can store Artifact Filters, only one Gatekeeper is associated to a Namespace at a time.
* addToNamespaceGatekeeper: Add an Artifact Filter to the Gatekeeper
* removeFromNamespaceGatekeeper: Remove an Artifact Filter from a Gatekeeper
* joinNamespace: Add an Artifact to a Namespace, this must be done first before caching
* leaveNamespace: Remove an Artifact completely from a Namespace, must already be removed from the cache.



## Artifacts

Full list of Artifacts that are joinable and cachable to any Namespace.

* `Item`
* `Match`
* `Namespace`
* `Player` _NOT IMPLEMENTED_
