# Class Definition

To define a class, you’ll need to start with a JSON file:

```json
{
  "data": {
    "settings": {
      "freeBuild": {
	"boolean": true,
        "inherited": { "notInherited": true }
      },
      "childrenMustBeEditions": null,
      "builderMustBeHolder": null,
      "updatePermissiveness": null,
      "buildPermissiveness": [
        {
          "permissivenessType": { "parentTokenHolder": true },
          "inherited": { "notInherited": true }
        }
      ],
      "stakingWarmUpDuration": null,
      "stakingCooldownDuration": null,
      "stakingPermissiveness": null,
      "unstakingPermissiveness": null,
      "childUpdatePropagationPermissiveness": [
        {
          "childUpdatePropagationPermissivenessType": { "usages": true },
          "inherited": { "notInherited": true }
        },
        {
          "childUpdatePropagationPermissivenessType": { "components": true },
          "inherited": { "notInherited": true }
        },
        {
          "childUpdatePropagationPermissivenessType": {
            "updatePermissiveness": true
          },
          "inherited": { "notInherited": true }
        },
        {
          "childUpdatePropagationPermissivenessType": {
            "buildPermissiveness": true
          },
          "inherited": { "notInherited": true }
        },
        {
          "childUpdatePropagationPermissivenessType": {
            "stakingPermissiveness": true
          },
          "inherited": { "notInherited": true }
        },
        {
          "childUpdatePropagationPermissivenessType": {
            "freeBuildPermissiveness": true
          },
          "inherited": { "notInherited": true }
        }
      ]
    },
    "config": {
      "usageRoot": null,
      "usageStateRoot": null,
      "componentRoot": null,
      "usages": [
        {
          "index": 0,
          "basicItemEffects": null,
          "usagePermissiveness": [{ "updateAuthority": true }],
          "inherited": { "notInherited": true },
          "itemClassType": {
            "consumable": {
              "maxUses": null,
              "maxPlayersPerUse": null,
              "itemUsageType": { "infinite": true },
              "cooldownDuration": 500,
              "warmupDuration": null
            }
          }
        }
      ],
      "components": [
        {
          "mint": "FvGU3HCV4BjtFs2YbvbMugySMbXDE7i2iKsaQqvNyWZx",
          "amount": 1,
          "classIndex": 0,
          "timeToBuild": null,
          "componentScope": "set1",
          "useUsageIndex": 0,
          "condition": { "presence": true },
          "inherited": { "notInherited": true }
        }
      ]
    }
  },
  "metadataUpdateAuthority": null,
  "storeMint": false,
  "storeMetadataFields": false,
  "mint": "Hz5x6myaWWSKKzAhh2LHA5YmXExLiyTfj89S9zXyT17M",
  "index": 9,
  "updatePermissivenessToUse": { "updateAuthority": true },
  "namespaceRequirement": 1,
  "totalSpaceBytes": 300
}
```

Now there’s a lot to unpack here, so let’s go step by step.

Your `settings` contains mostly permissions arrays that use the `PermissivenessType` described in [Concepts](../../concepts/) to tell the `ItemClass` who is allowed to do which things. Examples include who can stake, who can unstake, who can build, and who can update.

You’ll also notice two special options which are optional Booleans (a boolean + an inheritance marker), `free_build` and `children_must_be_editions`. For a traditional `ItemClass`, a lack of `Components` means that it cannot be built. Setting `free_build` to `true` indicates that rather than indicating the `ItemClass` cannot be used to build an NFT into an `Item`, it can be done for free (no components required). `children_must_be_editions` is fairly straightforward - all `Item`s created from this `ItemClass` must be a limited edition of the `ItemClass`’s underlying NFT. This requirement is not enforced for child `ItemClass`es.

{% hint style="warning" %}
Whenever you are using the JSON files to define Permissivenesses, you’ll notice `notInherited` is exclusively used. This is by design. Overridden and Inherited values are provided by the program when class propagation occurs.
{% endhint %}

The config part of the JSON file covers how an item may be used, and what components are required to build it. You’ll notice that usages are required to have indexes that match up with their position in the array - this is for later use in item activation. You’ll also see that you can configure the way your item is used to have different permissions depending on the type of use.

The top-level of the JSON file lets the CLI know what permissions to use to define or update the class, how much space should be used for the `ItemClass` struct, and whether or not you wish to store the metadata and mint fields on the `ItemClass` for reverse-lookups.

Once you have this file, you can create an `ItemClass` on top of an existing NFT (no SFTs allowed, sorry) like so:

```bash
item-cli create_item_class \
         -k <keypair> \
         --env devnet \
         -cp example-configs/itemClass.json
```

Updating it is just as easy:

```bash
item-cli update_item_class \
         -k <keypair> \
         --env devnet \
         -cp example-configs/itemClass.json
```

Remember, if you want to propagate updates from a parent `ItemClass` to your `ItemClass`, you must start at the highest parent that has changed, and issue updates in sequence from parent to child via the `update_item_class` command until all updates are propagated. If you wish to do this permissionlessly, use the `-iu` flag with `update_item_class`.

Want to see what you made? Run `show_item_class`!

```bash
item-cli show_item_class \
         -k <keypair> \
         --env devnet \
         -cp example-configs/itemClass.json
```
