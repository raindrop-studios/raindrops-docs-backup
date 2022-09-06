# Live Example

Let’s use this live example JSON to illustrate how to create, enter, and complete a match:

```json
{
  "winOracle": null,
  "matchState": { "initialized": true },
  "winOracleCooldown": 10,
  "space": 300,
  "minimumAllowedEntryTime": null,
  "tokenEntryValidation": [
    {
      "filter": {
        "parent": {
          "key": "2aEHhUyRXvV18i7wb17nNJsD2qafHpiJcKS3wcBgUoui"
        }
      },
      "isBlacklist": false,
      "validation": {
        "key": "nameAxQRRBnd4kLfsVoZBBXfrByZdZTkh8mULLxLyqV",
        "code": 1
      }
    }
  ],
  "authority": null,
  "leaveAllowed": true,
  "joinAllowedDuringStart": true,
  "oracleState": {
    "seed": "Gz5x6myaWWSKKzAhh2LHA5YmXExLiyTfj89S9zXyT17g",
    "authority": "44kiGWWsSgdqPMvmqYgTS78Mx2BKCWzduATkfY4biU97",
    "finalized": false,
    "tokenTransferRoot": null,
    "tokenTransfers": [
    
    ]
  },
  "tokensToJoin": [
    {
      "mint": "AoDxuMeVojMb9pBjcrKnCrz6e2u6HxdcJBPgUDDfd4W7",
      "amount": 1,
      "sourceType": 1,
      "index": 1,
      "validationProgram": "nameAxQRRBnd4kLfsVoZBBXfrByZdZTkh8mULLxLyqV"
    },
    {
      "mint": "9UtumWmQhYFxS5EnqxccFm1t7JixT5kivLiYASA4AiaG",
      "amount": 1,
      "sourceType": 2,
      "index": null
    }
  ]
}
```

This JSON actually is setup to do a few different things, at different points among the lifetime of the match. We’ll go over each as we do it. First, let’s create the oracle!

```bash
match-cli create_or_update_oracle \
          -k <keypair> \
          --env devnet \
          -cp example-configs/createMatch.json
```

This uses the “oracleState” hash to seed and create an oracle. Whatever is in this hash file will be placed in the oracle every time the above command is run. Alternatively, if oracleState is null and winOracle is set, the expectation is that the oracle is not owned by the Matches program and you’re choosing not to use this endpoint to update it, but it still fits the standard.

Now let’s create the match:

```bash
match-cli create_match \
          -k <keypair> \
          --env devnet \
          -cp example-configs/createMatch.json
```

Checking the token entry validation in our JSON, or via the show match call, run here, we can see that only one type of token can be added:

```bash
match-cli show_match \
          -k <keypair> \
          --env devnet \
          -cp example-configs/createMatch.json
```

```
Match  2NJ6s5ZaXRR2ED4dAgT6Xz6o8JXcX2BvStC4DX7cjEwz
Namespaces: Not Set
State: initialized
Win Oracle: PublicKey {
  _bn: <BN: fe47ad6b4d80429f9ec5f00138cca26d1812424952113f3d9e0094e112422bea>
}
Oracle Cooldown: 10
Last Oracle Check: Never Checked
Oracle Finalized: false
Oracle Token Transfer Root: Unset
Oracle Token Transfers:
Leaving Match Allowed?: Yes
Joining Match Allowed?: No
Minimum Allowed Entry Time: Unset
Current token transfer index: 0
Token Types Added: 0
Token Types Removed: 0
Token Entry Validations:
--> Filter:
----> Parent: 2aEHhUyRXvV18i7wb17nNJsD2qafHpiJcKS3wcBgUoui
--> Blacklist?: false
--> Validation: Call nameAxQRRBnd4kLfsVoZBBXfrByZdZTkh8mULLxLyqV with 1
Token Entry Validation Root: Unset
```

We happen to know that the first entry in the tokensToJoin list is the token whose parent matches, see:

```bash
item-cli show_item \
         -k <keypair> \
         --env devnet \
         -m AoDxuMeVojMb9pBjcrKnCrz6e2u6HxdcJBPgUDDfd4W7 \
         -i 1
```

```
Item 4v3REPCUsHd1fUX44XUbQ75apUMdJwFj3quoJELchCAH
Namespaces: [ undefined ]
Parent: 2aEHhUyRXvV18i7wb17nNJsD2qafHpiJcKS3wcBgUoui Index: 0
Mint: Not cached on object
Metadata: Not cached on object
Edition: Not cached on object
tokensStaked: 0
Item Data:
--> Usage State Root: Not Set
--> Usage States:
----> Index: 0
----> # Times Used: <BN: 0>
----> Activated At: Not Active
```

We can also see that when this token is added, it will do a CPI call to a specific validation we set. This is entirely optional - removing the callback from the JSON would remove this requirement. It just allows the match author to add additional custom logic beyond the standard filters.

To add this token to the match, we run:

```
match-cli join_match \
          -k <keypair> \
          --env devnet \
          -cp example-configs/createMatch.json \
          -i 0
```

This command uses the “tokensToJoin” array in the JSON file and either iterates through and adds each token to the match escrow OR if -i is provided, only adds that index (as we are doing here). If we then try to add index 1, we will see it fail due to our token entry validation.

After this, we can change the entry for matchState to started in the JSON, then issue the update using the update command.

```json
"matchState": { "initialized": true },

"matchState": { "started": true },
```

```
match-cli update_match \
          -k <keypair> \
          --env devnet \
          -cp example-configs/createMatch.json
```

At this point, now we must use the oracle to determine the outcome of the match. Let’s update the Oracle hash to the following:

```json
{
"oracleState": {
    "seed": "Gz5x6myaWWSKKzAhh2LHA5YmXExLiyTfj89S9zXyT17g",
    "authority": "44kiGWWsSgdqPMvmqYgTS78Mx2BKCWzduATkfY4biU97",
    "finalized": true,
    "tokenTransferRoot": null,
    "tokenTransfers": [
      {
        "from": "44kiGWWsSgdqPMvmqYgTS78Mx2BKCWzduATkfY4biU97",
        "to": "Dq3SXLF283A5Q7abqR4EpNkwUr6nLEVoQ7zFd5MNXFec",
        "tokenTransferType": { "normal": true },
        "mint": "AoDxuMeVojMb9pBjcrKnCrz6e2u6HxdcJBPgUDDfd4W7",
        "amount": 1
      }
    ]
  },
 }
```

Please note that this JSON/update call combo will only work if your oracle is an internally produced one. If it is external, the external party must do their own writing. To issue this oracle state to the on-chain oracle, run

```
match-cli create_or_update_oracle \
          -k <keypair> \
          --env devnet \
          -cp example-configs/createMatch.json
```

Now that the oracle has been updated, you’ll need to notify the match that the oracle has changed and it should “listen” to it. This will move the match from the Started state to the Finalized state.

```
match-cli update_match_from_oracle \
          -k <keypair> \
          --env devnet \
          -cp example-configs/createMatch.json
```

Note that this call is permissionless! Anybody can do this. Now if we run show\_match, we’ll see that the state has changed. Now it is up to permissionless cranks to follow the TokenTransfers provided and issue out the tokens to either original owners or new owners.

```
match-cli disburse_tokens_by_oracle \
          -k <keypair> \
          --env devnet \
          -cp example-configs/createMatch.json
```

In this case, this will issue a single command to the cluster to move the token to its new owner. Now the match will have entered its final state, PaidOut, because all tokens have left the match escrow. Let’s drain the match and oracle and reclaim lamports!

```
match-cli drain_match \
          -k <keypair> \
          --env devnet \
          -cp example-configs/createMatch.json
          
match-cli drain_oracle \
          -k <keypair> \
          --env devnet \
          -cp example-configs/createMatch.json
```
