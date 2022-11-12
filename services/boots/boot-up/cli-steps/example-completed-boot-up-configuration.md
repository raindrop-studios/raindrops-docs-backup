---
description: >-
  This is an example of a Boots-Up configuration file after all four steps are
  completed.
---

# Example - Completed Boot-Up Configuration

All Ids are valid on the Mainnet environment. This is an example for a collection of 1 Trash Panda. This particular booted collection was booted on the 102th index of the Degen Trash Pandas, so it's actually a shadow collection of Players on top of the "real" ones that exist at index 0. It shows how multiple player collections can be made on a single NFT collection if one wished!

```
{
  "scope": {
    "type": 0,
    "values": ["2C1XGHmsE8zdv3bnFYevgshQZykzNJQkii89uybnbHuJ"]
  },
  "bodyPartLayers": ["GLASSES", "DUMPSTER", "BODY", "HEAD", "MOUTH"],
  "stringLayers": ["BACKGROUND", "FUR"],
  "newBasicStats": [
    {
      "index": 0,
      "name": "mutationLevel",
      "inherited": { "notInherited": true },
      "statType": {
        "enum": {
          "starting": 0,
          "values": [
            { "name": "NA", "value": 0 },
            { "name": "Lvl1", "value": 1 },
            { "name": "Lvl2", "value": 2 },
            { "name": "Lvl3", "value": 3 },
            { "name": "Lvl4", "value": 4 }
          ]
        }
      }
    }
  ],
  "itemsWillBeSFTs": true,
  "className": "panda",
  "namespaceName": "dtp",
  "allowTokenHolder": false,
  "itemClassLookup": {
    "DUMPSTER": {
      "BLACK": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "GDpbKFQhwZnHqPU8cTv7GrKenUp9NvRyNcmtLnrEv3TZ",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "RED": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "H4GvbhVb7aN5k8SrJ2YzWSHG59uXmn6XFVwGsRKoLQ7D",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "GREEN": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "AHVMV7jXnn1dFRnPAfcm9oo4iyyFUGK7L1UwHB3QyMrE",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "ZOMBIE": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "CK9Kif7dbiu79aGnXtntQGu2NguUG9j5Q6LtdXASLwxu",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "BLUE": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "8wy9Tnm7dqPVM4imG1J7av4P7ysKtCqMw8wHY2tZHD7T",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "PURPLE": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "4w3JDgL8RM5TNTAirh5Apx8zqYUCA3mSonzHf22wnuf1",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "BROWN": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "GPiscCEzbavCu4PECo3cpLjVoTUr2hcb5SY46qaJKdX4",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "ANTIQUE": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "7jwWxpuGaCCtPkG1Y7YMVuMActVDrvBXA6wt5b4iP8ua",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "FOX": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "JD5j1g9xNQ9KnEdBNDzaRRr7YweKuNGTXRNCt69gYMmV",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "ACID": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "9B4YVLvPSk5SKdSD91Bqf7sdqcojZeBnhz4T8GbXJz5z",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "GOLD": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "D87jLHoriye2FBJGbihdfAPbs72chSLhjVS2Dax7DGAh",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "EXALTED_STAT | RUGGED_COUNT: 2": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "ETaV49gLYxxLwwEcZJ5MFLxewWqFHHLmYyE1xazvFxa2",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "EXALTED_STAT | TELL_ME_A_JOKE: Mint Date": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "AkDc1gLVyWMdTiPeyWzs7VkzpBqKvMfFvvnoM2emUpoq",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "EXALTED_STAT | PSYCHOLOGICAL_TRAUMA_LEVEL: Medium": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "9s2rSDheSya5atniWLFyiigbat4nGpTYYFskecL14eiD",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "EXALTED_STAT | WEN: 2 hours": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "E3ySYEo43nKTrNk4AXqtDvvUA2MtoFhGNdFPY456U6qv",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "EXALTED_STAT | EXILED: Just kidding": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "A9kn7ypE6DPe9LchpBeRcyoiZuQiAvmuGthURYZ8hJy8",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "EXALTED_STAT | MONOLIFF?: Mono-LEAF!": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "7Y3SExK6B8As4TMajf7hTv9AX7SbyzN4m81PJhh4UBix",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "EXALTED_STAT | B_AND_J": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["DUMPSTER"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "9JSTjcGBuT5zwQLnhHC24iQeTkuMcgd2ax533nQQuKwE",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      }
    },
    "BODY": {
      "Fairy Wings": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "8wiQnzct345B8Q4pLRDfoJD1DzF12kaLZ4ZLp8zreKMy",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Turtle Neck": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "3e6pmwLeEiNvwnzzAAkdqmapXUuP4keFd2fKGuH1YsUB",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Tweed Suit": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "iekZB2m8NibdW3ppGjXjtcBXz7XrDZQYVZ39GMEf64s",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Knitted Vest": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "5oyxG3Mm6tVKeh13FEK6ceUcxLTUG5Ads5ye1cfCBAtJ",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Singlet": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "H7tKLMBEgKuWxPqsXYS82kUb8hHdvPm7bjyn6N8TMvHR",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Hoodie": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "9BVh4KjDBkyEsaRJ4N5iHttmFkQaXXJrqkeYgT6Mjqjd",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Xmas Sweater": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "B8j7gipkE479tLQXb6RaNQvvPocwDFqD9teAVFoxsoXs",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Football Jersey - Red/Blue": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "FDLKFLmhJXXnTS4gfQ2ne8ZzJ4ejwKgk1Fb2t6v6LNQV",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Football Jersey - Blue/White": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "5BJ5kFEqTDxVyVMxAYbspuacKhCh64NXZZwEZfNKn4p4",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Prom King": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "BhAgBc7bMB4SffzH764pmiZasMKsrhbJnFNmYr4i1sTJ",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Leather Jacket": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "C4HBLuJcLH5wxSgZSafJfKwmRikvc6CFbA1GUsBv7wJg",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Dress Shirt": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "EuswCn1vX9cjNeiNsDHrz2XZpDdG5GtrEgNJC47o7Epq",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Degen Service Polo": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "BRShWE19fp4paWdnjxLYt5WQsyRmMvo5E6TriG2eYG47",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Open Shirt": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "Hx9MxHZ2QQyr4dwNAwXeBHtmqYdqKQLhNBfoq8mpVVVM",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Rain Jacket": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "CrFsAPANs1E3WnwkWyaawCcT8Gab1vJY5qWtk3mtqymp",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Designer Jacket": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "8isZ49HFTaNqN5wimF4AqTiLitV6y5AjMGwnQFqp3gEx",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Engineer": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "4S5keWt1LEMGcsVFU3NVos4hhGgXQbKmNDrJzbavRWLb",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Bandana": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "AfGHUCLrkQKLcmqXKfTsq1mfkwkyByLKKCZTm1GD9Tqi",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Overalls": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "6ZhxB6MZ8mQtgeFGKmr6nsWbSrN2BhjvejLj6vr58QSb",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Fishing Vest": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "4N4uMutjDE2dahuqPQRF5TsnNu81Pr53k43LuWDNjb4P",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Admiral": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "J9RtnFJRjW2fotTkDMPVVDKfPiCj8iJ3QqUYs7p66tyf",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Down Jacket": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "ASuYtaG3DEsTBep1aBD5tEwPmx4mBzLpVa5fhfGFbdrW",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": "AwStb9saCGbUJWjKEYGcSruByNN9dBRLJqHFPNJSL2AP"
      },
      "Bumbag": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "Fv9RewyovAXaWfgdv1wuhdKmyGkYyBpr5gtLSLvXKGbE",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "T-Shirt": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "Bru4Gs1ryTNcSUSnHkkCtmqrKAgzedYgsVYa5Sf7Yed8",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Hockey Pads": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "Dyiah4B3WF3KUZgWSKBheEMMtxhHBg1DLYn57ogTEGTm",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Chav Jacket": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "C4CcTLdZ6rDSY11Pz11uNavKGpNCQpZf7ZJnMWth9vvY",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Slav Jacket": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "6FGXVsvFtwEttPcHTAqhzwybuNHGz9HCGc55X1ErBpiK",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Spacesuit": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "7tNfW8BceHZf2McdVVxG5Dq21qFiHUeDWziuFF738hfn",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Chain": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "2RiMwirGdZYZvTfFohMY7EWXtuNART9T5BmPiHvAh9yJ",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Crayon Farmer": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "B8MMYezcQfgC6DM733jUfwZHgipyrE2WTxHsKiNHaUuc",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Toga": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "4G4AKgQXqkRfVbJZfc56yqnkq8rgkWWyCtt4Kr4FsaVm",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Mummy": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "PSWD87gk7HJetLytuDrKuUxY8uY8Zg62W3SvU2PWmNH",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Vampire Cape": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "3uYAC1iTExk1NnykakNjRT4ekQYsLPHPnCiXSbwHCZQP",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Denim Vest": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["BODY"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "BGp4wuu2ZodEqytUduPJbKBYCJ2ymohBTeLZjvxMBnSx",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      }
    },
    "HEAD": {
      "Space Helmet": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "CFDLfqhREBc4Mdi1mYjSkDMX1NbRjCnCgFffWWW6U6jg",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Pandas Pickles": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "FbqKrWqxKenz7JUqAqa2DHhZTSNvoTwPE8TN9SAy4rKP",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Cardboard Box": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "Hvq4CZUfzprWTRg6wubVip3pHNHtiExxMPC2adWBEAsB",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Lampshade": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "8pHZyVQZNLWaj23uPTc3abMe9s2Jjetd1eSMWegURmVU",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Ice Cream": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "9sCfz4fRgi9si2qhWKqMzEJEDbQitsExJiYv5Cvmkg1K",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Road Cone": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "5VVQgMYawG6FPcqiTfPkF9Q3d4Zf5iMYxAw5qKfdAyQU",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Pot": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "3yRJFJ7Z5fJatumtsEELseroCUSUnoyBeTNWTLze61mw",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Crown": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "7GNF7s9nTwycom7wphLtTfg3nQveugkD6R1UKHZZgGe6",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Boot": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "9XT8qG1gD9uiTysK3HRAqP8ndrX9SLnzD8CHCBcq6i18",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Trash Lid": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "2Dqog3PzaaxeySnqNosZEbyViLo8F8RvZcDRf1EdMvsG",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Headband": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "HjbCx5bvv46GJ99Z8QZPYFjXeYLsdMJ7bex4T71FqqQg",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Paper Bag": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "HTmjWKPRHAkcUv8aJDGntKS4krKP6tkvGqLLEnNKUTDv",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Paint Can": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "5sNZ6sbiC1r6e92zWERsXH2PxrgowYhPveHL6MrcL8UV",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Sock": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "3QVMt8icy9SiF6MofdN9KpSUoSCRtArXZbYdEDPns2KA",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Belt": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "CYkqjSsNwRoqVBZ3xR4UczrRUEmPXgHwFUWDb9L83k8u",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Takeout": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "ATuSFdfHXq24zWmLk1GqZa5JJgT61UpdFRqtQeHAR4aU",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Pandos": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "CJ1ERaDhynRgNR1xfZUMJWt6TGLNUNGVYjfo6hiHUEox",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Beanie": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "B6B2psTZCLeeKN4MKfbYr6K1L2WNhHYiJkLDwAyCdtao",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Degen Service Hat": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "EAQXredzUwj1L5bgbSSqymJ737RsazRFZYruzQ5CzNAK",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Flat Cap": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "6kVwDnmuL4a9Z2DNyAea9RGyfc1yL9Msbj6FTTGnxJ4f",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Colander": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "B64FCbEaFrLM1hz9VxbqGz4HuRSUX29y4CXSkgXY8s3J",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Trucker Cap": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "2NsawY1ZPSwb64XNUaF8ihNEjUbobtBgxE6NLs3ev8u6",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "The Gambler": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "G1i3QoqjuVbp5ryb1oDPjNHpRpJr1UDD1cXYZScgNR9h",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Steampunk Hat": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "7Lh8VEDqWd39NyUCNEaafNxNHCX92ijXFtPXtg8jsqXH",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Beret": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "Am9jtSQY6HKeHU5N5QMSb2VX2BXx2McyJqxy9SgqMNAd",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Pirate Hat": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "2WZXwLG3fP5zpJKUnxkAucAHQmBW8BidSQE8SrhdG18Q",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Sombrero": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "Gc1mwoFx4dXUk4XjxbtDsw4re5YBapZ7UEeMj8KJnz1h",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Tomato Soup": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "79prCBLp1adDSocSgWNeL5jGkqSnBUAM181H4emX45sh",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Plunger": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "FcKWHHEH5FkYGTvGiW3PPXdLUTXXui7n2zkLX7HtnhoC",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Urn": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "eHWF1UL3ceaes1EqM5ZJRhsTwEtRi3nZohyzkjYRLfD",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Tamberine": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "23wNxQQxKzMqZARZ76xiH55qVatcKW3WxWurGEQTb3rd",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Unicorn Headband": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["HEAD"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "3HRQ2JvWumptMTMdkYCVcGKSdzQiBjZPwDbDaFp5vS1o",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      }
    },
    "GLASSES": {
      "Trash Vipers": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["GLASSES"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "CNeg7jNZ4AJ5DhJPpogqUwEj2twSCKdA8FkUYAv8uBLx",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Snow Goggles": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["GLASSES"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "8ib3AP49J8NpUwq9u4ekAiejMviFruWpeaiH5cvp3wR4",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Reading Glasses": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["GLASSES"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "6YAfTTnPEgfL1YhRecbbjxzPaBMCgRhD8Cvc4RAVpQ3X",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Star Glasses": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["GLASSES"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "89KDtk2dbrcc7ZYeFjxjo9fFRo9p4ws5Cz3Uv9fLAeLR",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Designer Glasses": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["GLASSES"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "7Qb9aEtE5seexsL3BMNA5onnrH4nECCNmSD8DPC66pY2",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": "HBX2vhxguzHDZFFMB9ZJC8VF5MMfLtSumXTQkmdZ19Cu"
      },
      "Swimming Goggles": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["GLASSES"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "GKHPVMu99nnvH4bX6K93MDiytoqE46E75o9G3KCZXuc9",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Monocle": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": {
                      "bodyPart": ["GLASSES"],
                      "limitPerPart": "01"
                    }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "G9DhoPQjhSYom7Lot8ut9naNdTso9TGQLsSsuBG7C9eH",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      }
    },
    "MOUTH": {
      "Cigarette - Smirk": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "6AM6ddKcUfi1tzZZGE6fiEcJ9q33zVipYiyZ1gyaX54y",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "War Medal - Smirk": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "FF2wMcXbA674QpmgiisfaGR5BVsogoXMr6evQHyiFFPP",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Match Stick - Smirk": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "DFd2XLHDjNTM6VjFkzeoYUwqB7fVvxePCxof5HssD1cJ",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Joint - Smirk": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "BGtZHsSVV4K515xSqjuQ3a7PkmZzWT17dr1Miv3aLje3",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Crayon Shiv - Smirk": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "J3AgerKzEpWWMH5fyEDjWsZCYmYavCtjB4kmFLtkSvum",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Bird Foot - Smirk": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "2vFnzRgoducYT5Tg4DqqFyxwnR8KBxCLWxNJTQxTr5SE",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Burnt Spoon - Smirk": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "7gV2oQJWGRpnDnJUeK72XLcBbrUiDD8RHa6npXo2nqFc",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Rat Tail - Smirk": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "BQzrtjNJ3uyxs62VTXsjj6Rd4YcEvFnbU5UNLCZP6iNa",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Dirty Fiat - Grin": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "6ptYYSvKoVE5ctd1KEteLqz2Syg1uvBoQLFrBoVLTSJ6",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Dynamite - Grin": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "3CvAV2iQh4S9oz7pfwqAos9atkWLaHfBMtdo9vKLCYtY",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Cigar - Grin": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "GrRP8Si6YCfCbXYpHjN4WzXKTPwZMBRD2ofXqwPa4qkz",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Acid - Grin": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "jpCZUTx25RHF7Xb9xQnUqBZGwsv4t4FoJysqFisUihf",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Lollipop - Grin": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "9Ka1j2ETnU3y7jhUHptHBgxbmEJ8bjxDtha6ZKLSutp2",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Smashed Bottle - Grin": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "AUhEvYS9sSBF3NsNsEgpzteiP8wJAtKT8ruPictoixDf",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": null
      },
      "Bone - Grin": {
        "existingClassDef": {
          "data": {
            "settings": {
              "freeBuild": null,
              "childrenMustBeEditions": null,
              "builderMustBeHolder": null,
              "updatePermissiveness": [
                {
                  "permissivenessType": { "parentTokenHolder": true },
                  "inherited": { "notInherited": true }
                }
              ],
              "buildPermissiveness": [],
              "stakingWarmUpDuration": null,
              "stakingCooldownDuration": null,
              "stakingPermissiveness": null,
              "unstakingPermissiveness": null,
              "childUpdatePropagationPermissiveness": []
            },
            "config": {
              "usageRoot": null,
              "usageStateRoot": null,
              "componentRoot": null,
              "usages": [
                {
                  "index": 0,
                  "basicItemEffects": null,
                  "usagePermissiveness": [{ "parentTokenHolder": true }],
                  "inherited": { "notInherited": true },
                  "validation": null,
                  "callback": null,
                  "itemClassType": {
                    "wearable": { "bodyPart": ["MOUTH"], "limitPerPart": "01" }
                  }
                }
              ],
              "components": []
            }
          },
          "parent": {
            "index": 101,
            "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV"
          },
          "metadataUpdateAuthority": null,
          "storeMint": true,
          "storeMetadataFields": true,
          "mint": "4oTtqxdDQvwCv3JD6Awo3vzTtP9RF6o7Lk9Ck4Dk8DYR",
          "index": 101,
          "updatePermissivenessToUse": { "parentTokenHolder": true },
          "namespaceRequirement": 1,
          "totalSpaceBytes": 300
        },
        "address": "7xFXfbyanjV15iE68bhkGbCpnR1D2XcKh772S4p4KDiH"
      }
    }
  },
  "collectionMint": "GoLMLLR6iSUrA6KsCrFh7f45Uq5EHFQ3p8RmzPoUH9mb",
  "masterMint": "GmSRDXiXgvNo7UEx3rNvPCqD6aSreJaXT51tfq6ATXTK",
  "index": 102,
  "itemIndex": 101,
  "existingClassDef": {
    "data": {
      "settings": {
        "defaultCategory": {
          "category": "panda",
          "inherited": { "notInherited": true }
        },
        "childrenMustBeEditions": {
          "boolean": false,
          "inherited": { "notInherited": true }
        },
        "builderMustBeHolder": {
          "boolean": false,
          "inherited": { "notInherited": true }
        },
        "updatePermissiveness": [
          {
            "permissivenessType": { "tokenHolder": true },
            "inherited": { "notInherited": true }
          }
        ],
        "instanceUpdatePermissiveness": [
          {
            "permissivenessType": { "parentTokenHolder": true },
            "inherited": { "notInherited": true }
          }
        ],
        "buildPermissiveness": [
          {
            "permissivenessType": { "tokenHolder": true },
            "inherited": { "notInherited": true }
          }
        ],
        "equipItemPermissiveness": [
          {
            "permissivenessType": { "parentTokenHolder": true },
            "inherited": { "notInherited": true }
          }
        ],
        "addItemPermissiveness": [
          {
            "permissivenessType": { "parentTokenHolder": true },
            "inherited": { "notInherited": true }
          }
        ],
        "useItemPermissiveness": [
          {
            "permissivenessType": { "parentTokenHolder": true },
            "inherited": { "notInherited": true }
          }
        ],
        "unequipItemPermissiveness": null,
        "removeItemPermissiveness": null,
        "stakingWarmUpDuration": null,
        "stakingCooldownDuration": null,
        "stakingPermissiveness": null,
        "unstakingPermissiveness": null,
        "childUpdatePropagationPermissiveness": []
      },
      "config": {
        "startingStatsUri": null,
        "basicStats": [
          {
            "index": 0,
            "name": "mutationLevel",
            "inherited": { "notInherited": true },
            "statType": {
              "enum": {
                "starting": 0,
                "values": [
                  { "name": "NA", "value": 0 },
                  { "name": "Lvl1", "value": 1 },
                  { "name": "Lvl2", "value": 2 },
                  { "name": "Lvl3", "value": 3 },
                  { "name": "Lvl4", "value": 4 }
                ]
              }
            }
          },
          {
            "index": 1,
            "name": "BACKGROUND",
            "inherited": { "notInherited": true },
            "statType": { "string": { "starting": "unset" } }
          },
          {
            "index": 2,
            "name": "FUR",
            "inherited": { "notInherited": true },
            "statType": { "string": { "starting": "unset" } }
          }
        ],
        "bodyParts": [
          {
            "index": 0,
            "bodyPart": "GLASSES",
            "totalItemSpots": 1,
            "inherited": { "notInherited": true }
          },
          {
            "index": 1,
            "bodyPart": "DUMPSTER",
            "totalItemSpots": 1,
            "inherited": { "notInherited": true }
          },
          {
            "index": 2,
            "bodyPart": "BODY",
            "totalItemSpots": 1,
            "inherited": { "notInherited": true }
          },
          {
            "index": 3,
            "bodyPart": "HEAD",
            "totalItemSpots": 1,
            "inherited": { "notInherited": true }
          },
          {
            "index": 4,
            "bodyPart": "MOUTH",
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
    "mint": "GmSRDXiXgvNo7UEx3rNvPCqD6aSreJaXT51tfq6ATXTK",
    "index": 102,
    "updatePermissivenessToUse": { "parentTokenHolder": true },
    "namespaceRequirement": 1,
    "totalSpaceBytes": 739
  },
  "existingItemClassDef": {
    "data": {
      "settings": {
        "freeBuild": { "boolean": true, "inherited": { "notInherited": true } },
        "childrenMustBeEditions": {
          "boolean": true,
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
        "instanceUpdatePermissiveness": [
          {
            "permissivenessType": { "parentTokenHolder": true },
            "inherited": { "notInherited": true }
          }
        ],
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
            "childUpdatePropagationPermissivenessType": {
              "buildPermissiveness": true
            },
            "inherited": { "notInherited": true }
          },
          {
            "childUpdatePropagationPermissivenessType": {
              "builderMustBeHolderPermissiveness": true
            },
            "inherited": { "notInherited": true }
          },
          {
            "childUpdatePropagationPermissivenessType": {
              "childrenMustBeEditionsPermissiveness": true
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
        "usages": [],
        "components": []
      }
    },
    "metadataUpdateAuthority": null,
    "storeMint": true,
    "storeMetadataFields": true,
    "mint": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV",
    "index": 101,
    "updatePermissivenessToUse": { "updateAuthority": true },
    "namespaceRequirement": 1,
    "totalSpaceBytes": 300
  },
  "skipUpdates": true,
  "runDuplicateChecks": true,
  "redoFailures": true,
  "itemsName": "DTP Traits Collection - Fake2",
  "existingCollectionForItems": "9X3KW48ShDXtGsFQsU5Q25F4GuXNVg18exhX9okdbBoV",
  "playerStates": {
    "2C1XGHmsE8zdv3bnFYevgshQZykzNJQkii89uybnbHuJ": {
      "state": 4,
      "itemsAdded": [
        "7Qb9aEtE5seexsL3BMNA5onnrH4nECCNmSD8DPC66pY2",
        "NA",
        "3e6pmwLeEiNvwnzzAAkdqmapXUuP4keFd2fKGuH1YsUB",
        "NA",
        "7gV2oQJWGRpnDnJUeK72XLcBbrUiDD8RHa6npXo2nqFc"
      ],
      "itemsMinted": [
        "7Qb9aEtE5seexsL3BMNA5onnrH4nECCNmSD8DPC66pY2",
        "NA",
        "3e6pmwLeEiNvwnzzAAkdqmapXUuP4keFd2fKGuH1YsUB",
        "NA",
        "7gV2oQJWGRpnDnJUeK72XLcBbrUiDD8RHa6npXo2nqFc"
      ],
      "itemsEquipped": [
        "7Qb9aEtE5seexsL3BMNA5onnrH4nECCNmSD8DPC66pY2",
        "NA",
        "3e6pmwLeEiNvwnzzAAkdqmapXUuP4keFd2fKGuH1YsUB",
        "NA",
        "7gV2oQJWGRpnDnJUeK72XLcBbrUiDD8RHa6npXo2nqFc"
      ]
    }
  },
  "itemImageFile": "/Users/jprince/Documents/pandaItems/"
}

```
