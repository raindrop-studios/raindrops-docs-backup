# Propagation Permission

Permissions can be propagated from a parent class to a child class in either the fashion that overwrites the child array or is additive.

To specify which permissions get propagated, use the `child_update_propagation_permissiveness` array on the `Player` or `Item` classes.

The available options are:

```rust
pub struct ChildUpdatePropagationPermissiveness {
    overridable: bool,
    inherited: InheritanceState,
    child_update_propagation_permissiveness_type: ChildUpdatePropagationPermissivenessType,
}

pub enum ChildUpdatePropagationPermissivenessType {
    Usages,
    Components,
    UpdatePermissiveness,
    BuildPermissiveness,
    ChildUpdatePropagationPermissiveness,
    ChildrenMustBeEditionsPermissiveness,
    BuilderMustBeHolderPermissiveness,
    StakingPermissiveness,
    Namespaces,
    FreeBuildPermissiveness,
}
```

If you change this setting on an `ItemClass`, a permission-less `update_item_class` call can be made to the `Item` contract to enforce this down the `ItemClass`'s inheritance tree.
