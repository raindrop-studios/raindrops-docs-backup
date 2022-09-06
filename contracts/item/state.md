# State

This is a pseudo-diagram of the state defining an ItemClass, with all structs merged together:

```rust
#[account]
pub struct ItemClass {
    namespaces: Option<Vec<NamespaceAndIndex>>,
    parent: Option<Pubkey>,
    mint: Option<Pubkey>,
    metadata: Option<Pubkey>,
    edition: Option<Pubkey>,
    bump: u8,
    existing_children: u64,
    item_class_data: {
	    settings: {
				// If true and no components present, build is free
				// If false/none and no components present, nobody can build
				free_build: Option<Boolean>,
				// All new item NFTs must be limited editions of the item class NFT master edition
		    children_must_be_editions: Option<Boolean>,
				// Builder of the new item must be holding the NFT for that new item
			  builder_must_be_holder: Option<Boolean>,
		    update_permissiveness: Option<Vec<Permissiveness>>,
		    build_permissiveness: Option<Vec<Permissiveness>>,
		    staking_warm_up_duration: Option<u64>,
		    staking_cooldown_duration: Option<u64>,
		    staking_permissiveness: Option<Vec<Permissiveness>>,
		    unstaking_permissiveness: Option<Vec<Permissiveness>>,
		    child_update_propagation_permissiveness: Option<Vec<ChildUpdatePropagationPermissiveness>>,
			},
	    config: {
				usage_root: Option<Root>,
		    usage_state_root: Option<Root>,
		    component_root: Option<Root>,
		    usages: Option<Vec<ItemUsage>>,
		    components: Option<Vec<Component>>,
			},
		}
}

#[derive(AnchorSerialize, AnchorDeserialize, Clone)]
pub struct ItemUsage {
    index: u16,
    basic_item_effects: Option<Vec<BasicItemEffect>>,
    usage_permissiveness: Vec<PermissivenessType>,
    inherited: InheritanceState,
    item_class_type: ItemClassType,
    callback: Option<Callback>,
    validation: Option<Callback>,
    do_not_pair_with_self: bool,
    dnp: Option<Vec<DNPItem>>,
}

#[derive(AnchorSerialize, AnchorDeserialize, Clone)]
pub struct Component {
    mint: Pubkey,
    class_index: u64,
    amount: u64,
    time_to_build: Option<u64>,
    component_scope: String,
    use_usage_index: u16,
    condition: ComponentCondition,
    inherited: InheritanceState,
}
```

As you can see, an ItemClass is made up of its recipe (the Components required to create it), and the ways in which it may be used (the ItemUsage), as well as various permissiveness settings for different kinds of actions. Let’s cover them one at a time.
