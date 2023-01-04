# Creating a Player from the Subclass

Ok, so now let's build a player. Here's the JSON I will use:

```json
{
  "newPlayerMint": "edo3DzeqXsFzoaEhGHVn1GRCcFf4CWTaUSU4DDDVpJY",
  "playerClassMint": "edo3DzeqXsFzoaEhGHVn1GRCcFf4CWTaUSU4DDDVpJY",
  "buildPermissivenessToUse": { "updateAuthority": true },
  "newPlayerTokenHolder": null,
  "classIndex": 4,
  "newPlayerIndex": 5,
  "parent": {
    "index": 2,
    "mint": "GwB8ZtjDXYNR4iheuSS2uLa7EYC9J7b8yaRY9YmXXqUh"
  },
  "totalSpaceBytes": 300,
  "storeMetadataFields": false,
  "storeMint": false,
  "metadataUpdateAuthority": null
}

```

When building players, the JSON provided always needs at least two levels up - the `Player's` class, and that class's class, if necessary (notice the `parent` block.) Also, you'll notice from the previous page that the `buildPermissiveness` array did not allow `tokenHolder` permissions, so instead I had to rely on the fact that I had `updateAuthority` on the NFT to build the `Player`.

Also notice that I did something new here too with the NFTs. While the parent `PlayerClass` NFT was located on mint GwB8Zt index 2, and the child was at edo3Dz index 4, I didn't use a whole new NFT for the `Player` itself. I reused the second NFT, edo3Dz, just at a different index - 5! This is a very powerful design pattern you can use to create Singletons, if you wish.

Also notice that you get your choice of `totalSpaceBytes`. Make sure to set it large enough to accommodate the maximum amount of equipment that can be attached to this `Player` (the math is roughly 34 bytes multiplied by the number of `BodyParts` multiplied by how many items per part can be applied). At some point in the future we will add dynamic account resizing to item equipping so that the account can grow and shrink as needed.

Here's the command to run to create the `Player`:

```bash
player-cli build_player -cp buildPlayer.json 
                        -k ~/key.json 
                        --log-level debug 
                        -e mainnet-beta
```

After running, you can run the `show_player` command to check out the state on chain:

```bash
player-cli show_player -cp buildPlayer.json 
                        -k ~/key.json 
                        --log-level debug 
                        -e mainnet-beta
```

Or from the client side:

```typescript
import {
  ItemProgram,
  PlayerProgram,
  State,
  Utils,
  getItemProgram,
} from "@raindrops-protocol/raindrops";
import { Instruction as InstructionUtils } from "@raindrop-studios/sol-kit";

const { getMetadata, getEdition, getPlayerPDA } = Utils.PDA;

const getPlayer = async (
  mint: web3.PublicKey,
  playerIndex: BN,
  wallet: Wallet,
  env: string,
  customRpcUrl: string
) => {
  const [playerKey] = await getPlayerPDA(mint, playerIndex);
  const playerProgram = await PlayerProgram.getProgramWithWallet(
    PlayerProgram,
    wallet,
    env,
    customRpcUrl
  );
  const playerData = await playerProgram.client.account.player.fetch(
    playerKey,
    "confirmed"
  );
  const player: Partial<Player> = await decodePlayer(
    playerData as unknown as PlayerData,
    playerProgram,
    playerKey,
    playerIndex,
    mint
  );
  return player;
};

const getPlayerClass = async (key: string, playerProgram: PlayerProgram) => {
  const playerClass = await playerProgram.client.account.playerClass.fetch(key);
  return playerClass;
};

async function decodePlayer(
  playerData: PlayerData,
  playerProgram: PlayerProgram,
  playerKey: PublicKey,
  playerIndex: BN,
  mint: PublicKey
) {
  const { parent, ...otherPlayerData } = playerData;
  if(!otherPlayerData.mint) {
    otherPlayerData.mint = mint;
    //@ts-ignore
    otherPlayerData.metadata = await getMetadata(mint);
    otherPlayerData.edition = await getEdition(mint);
  }
  const player: Partial<Player> = InstructionUtils.convertTypeToType(
    { ...otherPlayerData, index: playerIndex },
    [
      "activeItemCounter",
      "classIndex",
      "equippedItems.[].amount",
      "itemsInBackpack",
      "tokensPaidIn",
      "tokensStaked",
      "index",
    ],
    BN,
    (arg: BN) => arg.toNumber()
  );
  if (parent) {
    const parentData: any = await getPlayerClass(
      parent.toString(),
      playerProgram
    );
    player.parent = InstructionUtils.convertTypeToType(
      {
        basicStats: parentData.data.config.basicStats,
        bodyParts: parentData.data.config.bodyParts,
        mint: parentData.mint,
      },
      ["bodyParts.[].totalItemSpots"],
      BN,
      (arg: BN) => arg.toNumber()
    );
  }
  player.key = playerKey;
  return player as Player;
}
```



You'll get something like this:

```bash
Player GVcBFt8U58ebioKw2rqnjJcfn56ct48oHTpvan11dik2
Namespaces: [ undefined ]
Parent: DkcUn2LNFPVjL5EKLsuJNmZF5tKcd5p3t9fv7HVqMMoi Index: 4 Mint: Not cached on object
Mint: Not cached on object
Metadata: Not cached on object
Edition: Not cached on object
Tokens Staked: 0
Active Item Counter: 0
Items in Backpack: 0
Player Data:
--> Stats Uri: Not set
--> Category:  (overridden) Abstract Warrior
--> Basic Stats:
----> Index: 0
----> Name: alive
----> Bool Value: false
----
----> Index: 1
----> Name: state
----> Enum Value: Billy
----
--> Equipped Items:
--
--> Player's Body Parts:
----> Index: 0
----> Inherited: inherited
----> Body Part: Arm
----> Total item spots: 1
----
----> Index: 1
----> Inherited: notInherited
----> Body Part: Leg
----> Total item spots: 1
```

{% hint style="info" %}
Note that on mainnet-beta, you'll be charged 1 $RAIN to build a player, and you'll receive that $RAIN back if you drain the player later.
{% endhint %}
