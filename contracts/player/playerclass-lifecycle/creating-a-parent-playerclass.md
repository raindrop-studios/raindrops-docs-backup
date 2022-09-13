# Creating a Parent PlayerClass

First, let's start with a standard JSON file for a `PlayerClass`. As you can see, you don't _need_ to set every field, most are optional. In fact, a lot of the fields we are setting in this example here _are_ optional, but this is a working example so you can play with it as needed.

```json
{
  "data": {
    "settings": {
      "defaultCategory": {
        "category": "Abstract Warrior",
        "inherited": { "notInherited": true }
      },
      "childrenMustBeEditions": {
        "boolean": false,
        "inherited": { "notInherited": true }
      },
      "builderMustBeHolder": {
        "boolean": true,
        "inherited": { "notInherited": true }
      },
      "updatePermissiveness": [
        {
          "permissivenessType": { "tokenHolder": true },
          "inherited": { "notInherited": true }
        }
      ],
      "instanceUpdatePermissiveness": null,
      "buildPermissiveness": null,
      "equipItemPermissiveness": null,
      "addItemPermissiveness": null,
      "useItemPermissiveness": null,
      "unequipItemPermissiveness": null,
      "removeItemPermissiveness": null,
      "stakingWarmUpDuration": 10,
      "stakingCooldownDuration": 10,
      "stakingPermissiveness": null,
      "unstakingPermissiveness": null,
      "childUpdatePropagationPermissiveness": [
        {
          "childUpdatePropagationPermissivenessType": {
            "bodyParts": true
          },
          "inherited": { "notInherited": true }
        },
        {
          "childUpdatePropagationPermissivenessType": {
            "defaultCategory": true
          },
          "overridable": true,
          "inherited": { "notInherited": true }
        }
      ]
    },
    "config": {
      "startingStatsUri": null,
      "basicStats": [
        {
          "index": 0,
          "name": "str",
          "inherited": { "notInherited": true },
          "statType": {
            "integer": {
              "min": 1,
              "max": 10,
              "starting": 3,
              "stakingAmountScaler": 1,
              "stakingDurationScaler": 2
            }
          }
        },
        {
          "index": 1,
          "name": "name",
          "inherited": { "notInherited": true },
          "statType": {
            "string": {
              "starting": "billy"
            }
          }
        }
      ],
      "bodyParts": [
        {
          "index": 0,
          "bodyPart": "Arm",
          "totalItemSpots": 1,
          "inherited": { "notInherited": true }
        }
      ],
      "equipValidation": null,
      "addToPackValidation": null
    }
  },
  "metadataUpdateAuthority": null,
  "storeMint": true,
  "storeMetadataFields": true,
  "mint": "GwB8ZtjDXYNR4iheuSS2uLa7EYC9J7b8yaRY9YmXXqUh",
  "index": 2,
  "updatePermissivenessToUse": { "tokenHolder": true },
  "namespaceRequirement": 1,
  "totalSpaceBytes": 400,
  "parent": null
}

```

There's a lot going on here. To skip understanding it and just see how it can be made to "go," let's just run this command:

```bash
player-cli create_player_class -cp parentClass.json 
                                -k ~/key.json 
                                --log-level debug 
                                -e mainnet-beta
```



With this, a PDA has been made on top of your NFT. Check it out with the `show_player_class` command:

```bash
player-cli show_player_class -cp parentClass.json 
                                -k ~/key.json 
                                --log-level debug 
                                -e mainnet-beta
```

This produces:

```bash
Player Class 6FDjBCMtHVruRgPTi1aWf8GGkn473Ws9B6cCjRDP7XwZ
Namespaces: [ undefined ]
Parent: None
Mint: GwB8ZtjDXYNR4iheuSS2uLa7EYC9J7b8yaRY9YmXXqUh
Metadata: 8dTzVjzmAHnWo3d4c2gCJGB2AivMz9ZM9wYfAyCid1uz
Edition: 6TwKWbTgi5owFKiP1HuA9wBGtehaqMNvPxduEE4VkL5a
Existing Children: 0
Player Class Data:
--> Player Class Settings:
----> Default Category (notInherited): Abstract Warrior
----> Children must be editions (notInherited): false
----> Builder must be holder (notInherited): true
----> Update Permissiveness:
------> (notInherited) tokenHolder
----> Instance Update Permissiveness:
----> Build Permissiveness:
----> Equip Item Permissiveness:
----> Add Item Permissiveness:
----> Use Item Permissiveness:
----> Unequip Item Permissiveness:
----> Remove Item Permissiveness:
----> Staking warm up duration: 10
----> Staking cooldown duration: 10
----> Staking Permissiveness:
----> Unstaking Permissiveness:
----> Child Update Propagation Permissiveness:
------> (notInherited) bodyParts - is overridable? false
------> (notInherited) defaultCategory - is overridable? true
--> Player Class Config:
----> Starting Stats Uri: Not Set
----> Basic Stat Templates:
------> Index: 0
------> Name: str
------> Stat Type: Integer (1 min <= 3 start <= 10 max)
------> Staking Amount Scaler: 1
------> Staking Duration Scaler: 2
------> Inherited: notInherited
-------
------> Index: 1
------> Name: name
------> Stat Type: String (Start: billy)
------> Inherited: notInherited
-------
----> Body Parts:
------> Index: 0
------> Inherited: notInherited
------> Body Part: Arm
------> Total item spots: 1
------
-------
------> Equipment Validation Callback: Not Set
------> Add to Pack Callback: Not Set
```

&#x20;It is not itself a `Player` but a blueprint for one. If you want to use it in games, you'll actually need to either instantiate a `Player` from this class, or, as we'll do in this example, subclass this `PlayerClass` one `PlayerClass` further, and then instantiate a `Player`. So now this NFT represents a blueprint for an Abstract Warrior. We plan to have a bunch of different Warrior classes, let's move on and subclass it to make a more specific warrior called Concrete Warrior in the next section.

If you're interested in what is going on in the JSON file above, please take a look at this "Breaking down the Magic" section below.

### Breaking down the Magic

#### Special Storage Magic

With `Players` and `PlayerClasses`, you can specify how big you'd like them to be but be aware that if they aren't big enough (`totalSpaceBytes`) you run into serialization errors when you equip too many items, for instance. So size appropriately for your game. You can also decide whether you want to store the mint and metadata and edition pubkeys on the PDAs, which take up a lot of space but help with indexing by your front-ends using `storeMint` and `storeMetadataFields`. If you yourself are not the `metadataUpdateAuthority`, make sure to set it. This is a Token Metadata concept from Metaplex - meaning you have the right to update the NFT.

#### Weird Permissions Magic

When creating a `PlayerClass`, the contract will always use `updateAuthority` even if you put, as we did above in `updatePermissivenessToUse`, `tokenHolder`. The only way it will not use `updateAuthority` when creating a class on top of an NFT is if the `PlayerClass` being created has a `parent` field set in the JSON, meaning it will be inheriting from some other `PlayerClass`. In that case, the `updatePermissivenessToUse` you chose (in this case, `tokenHolder`) is passed along to the `parent`, so you'd be trying to prove you have a right to create this `PlayerClass` because you are holding the token of the parent `PlayerClass` and that `PlayerClass` has in it's `update_permissiveness` array an entry for `tokenHolder`, allowing for such a permission to be used on it.

#### Inheritance Voodoo

If you want to have a `parent`, `parent` can fit the format, if not null, of:

```json
{
    "index": 3,
    "mint": "GwB8ZtjDXYNR4iheuSS2uLa7EYC9J7b8yaRY9YmXXqUh"
}
```

Also take a look at this garbage:

```json
{
  "childUpdatePropagationPermissiveness": [
        {
          "childUpdatePropagationPermissivenessType": {
            "bodyParts": true
          },
          "inherited": { "notInherited": true }
        },
        {
          "childUpdatePropagationPermissivenessType": {
            "defaultCategory": true
          },
          "overridable": true,
          "inherited": { "notInherited": true }
        }
      ] 
  }
```

What is all this? What this mess of JSON is saying that any child class inherits all `BodyParts` from the parent, and it's `defaultCategory`, but nothing else. This system of selective inheritance allows you to decide what parts of your classes filter down to children and what don't.

#### Overridable Refresher

&#x20;The `overridable` field, when present, determines whether or not the child's values will be completely overridden if present.&#x20;

So for arrays like `BodyParts`, if the parent has a Head and a Neck in its initial JSON file and the child has an Arm in its JSON file, and `overridable` is false, then the resultant child will have a Head, Neck, and Arm. If `overridable` is true, then the child, despite being created with an Arm in its JSON file, will end up with only a Head and a Neck during the creation call. For single-value types like `defaultCategory`, what `overridable` = true means is that even if you try to create a child class with an explicit value for `defaultCategory` in the initial JSON, it will be ignored, whereas if you try to set it in the initial JSON when `overridable` is false, it will be overwrite what was in the parent.

Basically, `overridable` true indicates that the `parent` crushes everything beneath it, and `overridable` false means that the `parent` will step aside for the `child` if the child has a better or additional idea of what a value should be.
