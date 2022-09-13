# Cleaning Up

Now that you've made a `Player` and two `PlayerClasses`, you probably want to clean up and drain them. This is pretty easy, just run the drain commands:

```bash
player-cli drain_player -cp buildPlayer.json 
                        -k ~/key.json 
                        --log-level debug 
                        -e mainnet-beta
```

```bash
player-cli drain_player_class -cp childClass.json 
                        -k ~/key.json 
                        --log-level debug 
                        -e mainnet-beta
```

```bash
player-cli drain_player_class -cp parentClass.json 
                        -k ~/key.json 
                        --log-level debug 
                        -e mainnet-beta
```

Be careful to run these in order - the protocol won't lead a parent be drained until all children have first been drained. Similarly a `Player` cannot be deleted until all `Items` have been unequipped, removed from the backpack, and had their effects removed from `BasicStats`.
