# Permissions

There are four different permissions types supported by the five contracts. When speaking here we'll be using the `Item` contract for examples, but this works equally well for the other contracts.

* TokenHolder
* ParentTokenHolder
* UpdateAuthority
* Anybody

### TokenHolder

In order to do the action, the token on which the action is being taken must be held by the signer of the transaction.

### ParentTokenHolder

In order to do the action, the token on which the action is being taken must already have a predefined struct (like an `ItemClass` or an `Item`) and that struct must have its `parent` field set to a valid pubkey. That pubkey will point to the `ItemClass` of another NFT. The signer calling this action must be holding the NFT of that `parent` `ItemClass`.

### UpdateAuthority

In order to do the action, the update authority of the `Metadata` of the token (as defined by the Token Metadata program) must be the signer on the transaction.

### Anybody

Anybody can do this action. There are no requirements to be met.

### Use cases

These permissiveness types are used to gate every kind of activity there is to do on any object across many of the contracts. In the item contract, for instance, you can set who is allowed to build an instance of an `ItemClass`, who can update it, who can stake against it, etc.

Here is an example of an `ItemClassSettings` struct that has several fields/properties that use these permissions:

```rust
pub struct ItemClassSettings {
    free_build: Option<Boolean>,
    children_must_be_editions: Option<Boolean>,
    builder_must_be_holder: Option<Boolean>,
    update_permissiveness: Option<Vec<Permissiveness>>,
    build_permissiveness: Option<Vec<Permissiveness>>,
    staking_warm_up_duration: Option<u64>,
    staking_cooldown_duration: Option<u64>,
    staking_permissiveness: Option<Vec<Permissiveness>>,
    unstaking_permissiveness: Option<Vec<Permissiveness>>,
    child_update_propagation_permissiveness: Option<Vec<ChildUpdatePropagationPermissiveness>>,
}

pub struct Permissiveness {
    inherited: InheritanceState,
    permissiveness_type: PermissivenessType,
}
```

When performing an action against a Raindrops contract, you must specify what type of permissiveness you want to use to do that action and that permissiveness will be checked against the existing array of permissions for the object being manipulated with that contract's endpoint.

The CLI will also use the permissiveness chosen to determine what additional accounts that might be needed to send in the instruction call to prove validity.

Here’s an example configuration file for opening an item escrow, which is the first action one does to create an `Item` from an `ItemClass` using the Item contract:

```json
{
  "newItemMint": "DQKJRRHjyiS1DgDuMWtdD2Cy2nbLqEP86sQ8nnBQMv2w",
  "itemClassMint": "Hz5x6myaWWSKKzAhh2LHA5YmXExLiyTfj89S9zXyT17M",
  "amountToMake": 1,
  "namespaceIndex": null,
  "buildPermissivenessToUse": { "tokenHolder": true },
  "classIndex": 10,
  "newItemIndex": 10,
  "craftEscrowIndex": 1,
  "componentScope": "set1",
  "parent": {
    "mint": "Hz5x6myaWWSKKzAhh2LHA5YmXExLiyTfj89S9zXyT17M",
    "index": 9
  },
  "originator": "44kiGWWsSgdqPMvmqYgTS78Mx2BKCWzduATkfY4biU97",
  "merkleInfo": null,
  "totalSpaceBytes": 200,
  "storeMetadataFields": false,
  "storeMint": false,
  "metadataUpdateAuthority": "44kiGWWsSgdqPMvmqYgTS78Mx2BKCWzduATkfY4biU97",
  "components": [
    {
      "mint": "5VDCnw9NADV4Bwr2x6wXcyNXU5EuWWksfceUtk7nxubm",
      "index": 1
    }
  ]
}
```

Notice that `buildPermissivenessToUse` is set to tokenHolder. This means that the `ItemClass` allows anybody holding the `ItemClass` NFT to use the `ItemClass` recipe to turn a non-raindrops NFT into an `Item` instance of this `ItemClass`. For instance, if you have an NFT that looks like a potion that you just made on a minting website, that does not mean it is an actual Potion that is used during play by Game X. If you hold the NFT representing the `ItemClass` for Potion, then you have the right to go through the creation process to turn this freshly minted NFT potion look-alike into an actual Potion that your game client can process during gameplay. At the end of this creation cycle you’ll have an Item PDA seeded to your potion NFT that allows it to be used within the game.
