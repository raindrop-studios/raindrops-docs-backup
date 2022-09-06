# Inheritance

A “inherited field” has the following structure:

```rust
pub enum InheritanceState {
    NotInherited,
    Inherited,
    Overridden,
}
```

Properties/fields that can be inherited in an `ItemClass` that come from it’s parent classes are marked appropriately if they came from it’s own definition(NotInherited), came from it’s parent definition(Inherited), or the parent class has permissions to make it illegal for any sub-definitions to be made on the given class(Overridden).

An example of `Overridden` would be the parent class saying that the child class cannot override the build permissiveness settings. The build permissiveness array, which can host a variety of different permissions types, must be a **1:1** match with the parent’s copy of it.
