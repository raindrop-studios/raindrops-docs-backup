# Namespaces

All Raindrops artifacts that can be cached or assigned to a namespace have an identical first few fields.

Examples:

```rust
#[account]
pub struct Item {
    namespaces: Option<Vec<NamespaceAndIndex>>,
    // extra byte that is always 1 to simulate same structure as item class.
    padding: u8,
    parent: Pubkey,
...
}

#[account]
pub struct ItemClass {
    namespaces: Option<Vec<NamespaceAndIndex>>,
    parent: Option<Pubkey>,
...
}


#[account]
pub struct Player {
    namespaces: Option<Vec<NamespaceAndIndex>>,
    // extra byte that is always 1 to simulate same structure as item class.
    padding: u8,
    parent: Pubkey,

	...
}

#[account]
pub struct PlayerClass {
    namespaces: Option<Vec<NamespaceAndIndex>>,
    parent: Option<Pubkey>,
...
}

#[account]
pub struct Namespace {
    pub namespaces: Option<Vec<NamespaceAndIndex>>,
...
}
```

Note that even `Namespace` has a namespaces section that can be used to join it to other namespaces, making it composable. Any artifact can join a namespace if it has this optional array up front with available slots (defined and set on creation).

Joining a namespace is done through the namespace contract.

{% hint style="info" %}
It is not required to have a namespace for your raindrops artifacts. However, if you use namespaces, your artifacts become eligible to use staking and you can charge entry fees in $RAIN to join those namespaces.
{% endhint %}
