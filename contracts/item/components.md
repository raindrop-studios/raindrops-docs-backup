# Components

All components must be ItemClasses. Any Item that inherits from those classes directly can be used as this component. Adding support for a top-level ItemClass component that is more than one level up from an Item is on the cards in a future release but was deemed too complex for this iteration.

Each Component requires an amount of that type, and a condition. The allowable conditions are:

```rust
pub enum ComponentCondition {
    Consumed,
    Presence,
    // Specifically, mint.supply == 0.
    Absence,
    Cooldown,
    CooldownAndConsume,
}
```

When Cooldown or CooldownAndConsume are used, the use\_usage\_index field is looked at to figure out what ItemUsageState to check in the given item’s usage state array to use when looking to see if the Item is on cooldown or not. In this way you can require a user to first bring an item to cooldown through a use before allowing it to be used as a crafting component.

{% hint style="info" %}
When Consume or CooldownAndConsume are used, the item is destroyed if used as a component here.
{% endhint %}

Time\_to\_build should be the same across all components in a component\_scope, and will be used (in seconds) to determine how long to force the user to wait once they enter the build phase for creating an item. A component\_scope is an arbitrary grouping of components so that multiple component recipes can be stored in the same array without nesting.
