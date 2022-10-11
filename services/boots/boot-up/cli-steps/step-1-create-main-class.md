---
description: >-
  This step creates the player class on chain and stores the information needed
  in the configuration file.
---

# Step 1 - Create Main Class

To run, issue the following command:

```
boot-up step_one_create_main_nft_class \
                   --env mainnet-beta \
                   --rpc-url https://api.mainnet-beta.solana.com \
                   --log-level debug \
                   --keypair ./nftCollectionUpdateAuthority.json \
                   --config-path ./bootsConfigurationFile.json
```

The command line parameters are as follows:

| option                       | description                                                                                                                |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| <p>-e,<br>--env</p>          | Which environment to use (devnet, testnet, mainnet-beta, localnet)                                                         |
| <p>-r,<br>--rpc-url</p>      | <p>The RPC to use to connect to Solana. This should be a paid RPC,<br>as this application causes heavy use to the RPC.</p> |
| <p>-l,<br>--loglevel</p>     | The log level to use (all, trace, DEBUG, info, warn, error, fatal, off)                                                    |
| <p>-k,<br>--keypair</p>      | The keypair which is the update authority for the NFT collection                                                           |
| <p>-cp,<br>--config-path</p> | The path to the configuration file                                                                                         |
| <p>-h,<br>--help</p>         | Get help with this command                                                                                                 |

The output of the help option is the following:

```
Usage: boot_up step_one_create_main_nft_class [options]

Options:
  -e, --env <string>           Solana cluster env name (default: "devnet")
  -r, --rpc-url <string>       Solana cluster rpc-url
  -l, --log-level <string>     log level
  -k, --keypair <path>         Solana wallet location
  -cp, --config-path <string>  JSON file with namespace settings
  -h, --help                   display help for command
```

After this command is run, the `existingClassDef` entry of the configuration file will be updated with the class definition information.

Once this command finishes successfully, you can move on to the next step
