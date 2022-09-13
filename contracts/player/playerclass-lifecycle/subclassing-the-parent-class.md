# Subclassing the Parent Class

Let's Subclass the Parent with this JSON file:

```json
{
  "data": {
    "settings": {
      "defaultCategory": {
        "category": "Concrete Warrior",
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
          "permissivenessType": { "updateAuthority": true },
          "inherited": { "notInherited": true }
        }
      ],
      "instanceUpdatePermissiveness": null,
      "buildPermissiveness": [
        {
          "permissivenessType": { "updateAuthority": true },
          "inherited": { "notInherited": true }
        }
      ],
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
          "name": "alive",
          "inherited": { "notInherited": true },
          "statType": {
            "bool": {
              "starting": false,
              "stakingFlip": null
            }
          }
        },
        {
          "index": 1,
          "name": "state",
          "inherited": { "notInherited": true },
          "statType": {
            "enum": {
              "starting": 0,
              "values": [{ "name": "Billy", "value": 0 }]
            }
          }
        }
      ],
      "bodyParts": [
        {
          "index": 1,
          "bodyPart": "Leg",
          "totalItemSpots": 1,
          "inherited": { "notInherited": true }
        }
      ],
      "equipValidation": null,
      "addToPackValidation": null
    }
  },
  "metadataUpdateAuthority": null,
  "storeMint": false,
  "storeMetadataFields": false,
  "mint": "edo3DzeqXsFzoaEhGHVn1GRCcFf4CWTaUSU4DDDVpJY",
  "index": 4,
  "parent": {
    "index": 2,
    "mint": "GwB8ZtjDXYNR4iheuSS2uLa7EYC9J7b8yaRY9YmXXqUh"
  },
  "updatePermissivenessToUse": { "tokenHolder": true },
  "namespaceRequirement": 1,
  "totalSpaceBytes": 400
}

```

The key thing to really note here is the parent block in the JSON,

```json
{
 "parent": {
    "index": 2,
    "mint": "GwB8ZtjDXYNR4iheuSS2uLa7EYC9J7b8yaRY9YmXXqUh"
  }
}
```

If you note from the prior section, this mint and index is the mint and index used to create the parent class. By referencing it in the JSON file here for the child class, we are telling the contract to consider this class a child. This also means that when we choose an `updatePermissivenessToUse` for creation here, we're actually using a permissiveness _on the parent, not the child._ So that tokenHolder is actually referencing the parent token, not the child. This is a nice way to get around needing to own updateAuthority on a specific NFT if you don't have it but want to make a game with it.

To create the subclass, run the same command as before:

```bash
player-cli create_player_class -cp childClass.json 
                                -k ~/key.json 
                                --log-level debug 
                                -e mainnet-beta
```

The resulting `show_player_class` command will yield the following:

```bash
Player Class DkcUn2LNFPVjL5EKLsuJNmZF5tKcd5p3t9fv7HVqMMoi
Namespaces: [ undefined ]
Parent: 6FDjBCMtHVruRgPTi1aWf8GGkn473Ws9B6cCjRDP7XwZ
Mint: edo3DzeqXsFzoaEhGHVn1GRCcFf4CWTaUSU4DDDVpJY
Metadata: EdKhUU1NwT6vQAFC29GS8jF9sqGnPRVSjuPzDtGyuvE1
Edition: GTVngak2nEZ3SB8qVdvqhuBgRq2hmJmJ5KUPEitZAi7J
Existing Children: 0
Player Class Data:
--> Player Class Settings:
----> Default Category (overridden): Abstract Warrior
----> Children must be editions (notInherited): false
----> Builder must be holder (notInherited): true
----> Update Permissiveness:
------> (notInherited) updateAuthority
----> Instance Update Permissiveness:
----> Build Permissiveness:
------> (notInherited) updateAuthority
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
------> (notInherited) bodyParts - is overridable? true
--> Player Class Config:
----> Starting Stats Uri: Not Set
----> Basic Stat Templates:
------> Index: 0
------> Name: alive
------> Stat Type: Boolean (Start: false, Staking Flip At: Not Set)
------> Inherited: notInherited
-------
------> Index: 1
------> Name: state
------> Stat Type: Enum (Start: Billy)
------> Values: Billy => 0
------> Inherited: notInherited
-------
----> Body Parts:
------> Index: 0
------> Inherited: inherited
------> Body Part: Arm
------> Total item spots: 1
------
------> Index: 1
------> Inherited: notInherited
------> Body Part: Leg
------> Total item spots: 1
------
-------
------> Equipment Validation Callback: Not Set
------> Add to Pack Callback: Not Set
```

The clever among you will probably be wondering where the `BasicStatTemplates` from the parent class are. If it had had `BasicStatTemplates` in the `childUpdatePropagationPermissivenessArray`,  it would have! In this case, we didn't add it in the previous section, so this child will only have the two stats it defines for itself, but if you try this example with that minor tweak to the parent, you can see the inheritance work.

However, we did set the propagation up for `BodyParts`, and this resultant class does have both a Leg and an Arm.&#x20;
