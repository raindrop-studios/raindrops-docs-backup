# BasicStats

```rust
pub struct BasicStatTemplate {
    pub index: u16,
    pub name: String,
    pub stat_type: BasicStatType,
    pub inherited: InheritanceState,
}

pub struct BasicStat {
    pub index: u16,
    pub state: BasicStatState,
}
```

All `PlayerClasses` define an optional vec of `BasicStatTemplates` that will map 1:1 to `BasicStats` in `Players` when instantiated. The Template defines what kind of stat it is, as well as its name, and the actual `BasicStat` contains the current state for that stat. An example `BasicStat` is "health," which might have a min/max of 0/100, and could be 50 on one `Player` and 60 on another.

{% hint style="info" %}
You'll notice the use of index on both structs. This is to assist in matching across both `Player` and `PlayerClass` in a more stable way than `name`.&#x20;
{% endhint %}

The meat of a `BasicStatTemplate` is the `BasicStatType`, defined below:

```rust
pub enum BasicStatType {
    Enum {
        starting: u8,
        values: Vec<Threshold>,
    },
    Integer {
        min: Option<i64>,
        max: Option<i64>,
        starting: i64,
        staking_amount_scaler: Option<u64>,
        staking_duration_scaler: Option<u64>,
    },
    Bool {
        starting: bool,
        staking_flip: Option<u64>,
    },
    String {
        starting: String,
    },
}
```

It is an enum that defines all the information a `Player` would need to know to govern a stat of a given type as that stat moves in value over time. The actual state, called a `BasicStatState`, is defined thusly:

```rust
pub enum BasicStatState {
    Enum {
        current: u8,
    },
    Integer {
        base: i64,
        with_temporary_changes: i64,
        temporary_numerator: i64,
        temporary_denominator: i64,
        finalized: i64,
    },
    Bool {
        current: bool,
    },
    String {
        current: String,
    },
    Null,
} 
```

With most of the data types the state is only pointing at the current value. The tricky part comes for Integers, which need to keep track of a bunch of intermediate values to track how items, both equipped and used, change the stat over time. When the contract "does math," it uses both structs in memory to figure out where to position the `current` value next, however your `Player` PDA is much smaller than the `PlayerClass` it inherits from because it doesn't need to keep track of mins, maxes, or all possible values.

{% hint style="info" %}
If you need a more complex type of data field than those provided here, the stats URI provided to every `Player` by its `PlayerClass` may be the right fit for you. You can store any type of data you want there, but it's up to you to handle changes to it and logic with it.
{% endhint %}
