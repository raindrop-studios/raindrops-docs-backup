---
description: Update the NFT with the new equipped items.
---

# Manipulate

First we need to prepare the payload to create the transaction for the user to sign.

```typescript
import { State } from "@raindrops-protocol/raindrops";

enum Action {
  Adding,
  Removing,
  Equipping,
  Unequipping,
}

type PlayerManipulatorPayload = {
  nftMint: string;
  nftHolder: string;
  actions: {
    itemClassMint: any;
    itemMint: any;
    parentItemClassMint: web3.PublicKey;
    bodyPartIndex: number | undefined;
    itemUsageIndex: any;
    action: Action;
  }[];
};

const getBodyPartIndex = (player: Player, bodyPartName: string) => {
  return player.parent.bodyParts.find(
    (bodyPart: Omit<BodyPartDetails, "items">) => {
      return bodyPart.bodyPart.toLowerCase() === bodyPartName.toLowerCase();
    }
  )?.index;
};

const getItemUsageIndex = (itemClassData: any, bodyPartName: string) => {
  return itemClassData?.itemClassData?.config?.usages?.find(
    (usage: State.Item.ItemUsage) =>
      usage.itemClassType.wearable &&
      usage.itemClassType.wearable.bodyPart.length &&
      usage.itemClassType.wearable.bodyPart
        .map((x) => x.toLowerCase())
        .includes(bodyPartName.toLowerCase())
  )?.index;
};

const payload: PlayerManipulatorPayload = {
    nftMint: player.mint.toBase58(),
    nftHolder: wallet.publicKey.toBase58(),
    actions: actions.map(({ item, action }) => ({
      itemClassMint: item.itemClassData.mint,
      itemMint: item.itemData.mint,
      parentItemClassMint: item.parentItemClassMint,
      bodyPartIndex: getBodyPartIndex(player, item.bodyPart),
      itemUsageIndex: getItemUsageIndex(item.itemClassData, item.bodyPart),
      action,
    })),
  };
```

Then we send the payload off to the Boots API

```typescript
const submitResponse = await fetch(
  getBootsApiUrl("player-manipulator/manipulate"),
  {
    method: "POST",
    mode: "cors",
    body: JSON.stringify(payload),
    headers: {
      "x-api-key": getBootsAPIKey(),
      "Content-Type": "application/json",
      "x-stage": getBootsStage(),
    },
  }
);
const response = await submitResponse.json();
const { licenseState, transactions } = response;
```

If the resultant `licenseState` is `"SUB_LICENSE_FILLED"` the user will not be able to proceed.

If the resultant `licenseState` is `"SUB_LICENSE_AVAILABLE"` the user will need to pay the license fee.

However, if the `licenseState` is `"NONE"` we can continue to sign the transactions and send a call to the API to update the metadata:

```typescript
import { State, Utils } from "@raindrops-protocol/raindrops";
import { WalletContextState } from "@solana/wallet-adapter-react";
import { Connection, PublicKey, Transaction } from "@solana/web3.js";

const { sendSignedTransaction, sleep } = Utils.Transactions;

type MetadataManipulatorPayload = {
  nftMint: string;
  nftHolder: string;
};

const submitRecievedTransactions = async ({
  payload,
  transactions,
  signTransaction,
  connection,
}: {
  payload?: MetadataManipulatorPayload;
  transactions: Transaction[];
  signTransaction: NonNullable<WalletContextState["signTransaction"]>;
  connection: Connection;
}) => {
  const signed = await signTransaction(transactions[0]);

  const { txid } = await sendSignedTransaction({
    signedTransaction: signed,
    connection,
  });

  if (!txid) {
    return { txid };
  }

  if (payload) {
    await sleep(10000);

    for (let i = 0; i < 3; i++) {
      const response = await fetch(
        getBootsApiUrl("metadata-manipulator/manipulate"),
        {
          method: "POST",
          mode: "cors",
          body: JSON.stringify(payload),
          headers: {
            "x-api-key": getBootsAPIKey(),
            "Content-Type": "application/json",
            "x-stage": getBootsStage(),
          },
        }
      );

      if (response.ok) {
        const result = await response.json();
        if (result.transactionId) {
          return { txid: result.transactionId };
        }
      }
      await sleep(15000);
    }
    throw new Error("Manipulate metadata request error");
  }

  return { txid };
};
```
