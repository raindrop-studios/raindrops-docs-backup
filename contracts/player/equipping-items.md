# Equipping Items

Once an `Item` has been [added to your backpack](backpackin/), if it has within it's list of acceptable `ItemUsages` the ability to be equipped, you can equip it using the methodology described here. First, let's create a JSON file like this:

```json
{
  "playerMint": "edo3DzeqXsFzoaEhGHVn1GRCcFf4CWTaUSU4DDDVpJY",
  "playerClassMint": "GwB8ZtjDXYNR4iheuSS2uLa7EYC9J7b8yaRY9YmXXqUh",
  "equipItemPermissivenessToUse": { "tokenHolder": true },
  "classIndex": 3,
  "index": 3,
  "metadataUpdateAuthority": null,
  "items": [
    {
      "itemClassMint": "7t5G3x4Zq5p2ZbAX8owcSi1tiLwLwYTDMJc1FmAYYpb7",
      "itemMint": "7t5G3x4Zq5p2ZbAX8owcSi1tiLwLwYTDMJc1FmAYYpb7",
      "itemIndex": 1,
      "amount": 1,
      "bodyPartIndex": 1,
      "itemUsageIndex": 0,
      "equipping": true
    }
  ]
}

```

Here you can see that it's possible to equip multiple items using the CLI in a row, or unequip some and equip others, using the `equipping` boolean in each object entry of the `items` array. You'll also see that we are electing to equip this item at the `BodyPart` with index 1 and we're using the `ItemUsage` at index 0 of the `ItemUsages` array on the `ItemClass` of the `Item`.

{% hint style="info" %}
&#x20;You can figure out what values are at these indices by running [`show_player_class`](playerclass-lifecycle/creating-a-parent-playerclass.md) on the `player-cli` and [`show_item_class`](../item/class-definition.md) for the `Item` using the `item-cli`. Both will display the `BodyParts` and `ItemUsages` respectively and their indexes so that you can plug them in here.
{% endhint %}

&#x20;Save this file and then run

```bash
player-cli toggle_equip_items -cp equipItems.json 
                              -k ~/key.json 
                              --log-level debug 
                              -e mainnet-beta
```

After this, if you run a `show_player` call, you'll see something like this:

```bash
--> Equipped Items:
----> Index: 1
----> Amount: 1
----> Pubkey: 3akMuc6LSg51cuZLmRas1tcmXSbz5pRa2axVnJXTErCq
----
```

Indicating that that item is now equipped on the `BodyPart` at index 1, through the Wearable `ItemUsage` at index 0 of the `ItemUsages` array of the `ItemClass` of this particular `Item`.
