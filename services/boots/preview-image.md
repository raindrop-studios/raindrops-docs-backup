---
description: Prior to making changes, view the potential resultant NFT.
---

# Preview Image

Get the layers required for the new NFT image:

```typescript
function getPreviewLayers(
  newAttrsWithSfts: {
    trait_type?: string;
    value?: string;
    item?: EquippableItem;
    updated?: boolean;
    sft?: Sft;
  }[],
  collectionDetails: Collection
): any {
  // Prepare metadata to generate preview
  let newAttrs = cloneDeep(newAttrsWithSfts);
  if (newAttrs) {
    for (let i = 0; i < newAttrs.length; i++) {
      const newAttr = newAttrs[i];
      // Remove blank traits
      if (newAttr.value === undefined) {
        // use the noTraitString set on the attributeRule since it might be unique. But fallback to the general config if none is set
        const attributeCollectionRuleset: any =
          collectionDetails.imageGen?.attributeRules?.find(
            (rule: any) => rule.layer == newAttr.trait_type
          );
        const noTraitString =
          attributeCollectionRuleset?.noTraitString ||
          collectionDetails.imageGen.noTraitsString;
        newAttr.value = noTraitString;
      } else {
        newAttr.value = newAttr.sft?.name || newAttr.value;
      }
    }
    newAttrs = newAttrs?.filter((attr) => attr.value !== undefined);
    newAttrs = newAttrs?.filter(
      (attr) =>
        collectionDetails.stringLayers.includes(attr.trait_type as string) ||
        collectionDetails.bodyPartLayers.includes(attr.trait_type as string)
    );
  }
  if (collectionDetails.imageGen?.fileType == "png") {
    return [
      ...(newAttrs || []).map((m) => {
        return {
          traitType: m.trait_type as string,
          value: m.value as string,
          layerUri: m.sft?.json?.layerUri || (m.sft?.json?.image as string),
        };
      }),
    ];
  } else {
    return [
      ...(newAttrs || []).map((m) => [
        m.trait_type as string,
        m.value as string,
      ]),
      ...(collectionDetails.imageGen.autoLayers
        ? collectionDetails.imageGen.autoLayers.map((l: string) => [l, null])
        : []),
    ];
  }
}
```

Pass the result of this to one of the following.

### Collection using PNG renderer

```typescript
async function getImagePng(
  imageGenUrl: string,
  nftMint: string,
  layers: (string | null)[][]
): Promise<string> {
  const response = await fetch(imageGenUrl, {
    method: "POST",
    mode: "cors",
    headers: {
      "x-api-key": getBootsAPIKey(),
      "Content-Type": "application/json",
      "x-stage": getBootsStage(),
    },
    body: JSON.stringify({
      nftMint,
      layers,
    }),
  });
  const file = await response.blob();

  return await new Promise((resolve, reject) => {
    try {
      const reader = new FileReader();
      reader.onload = function () {
        resolve(this.result as string);
      };
      reader.onerror = reject;
      reader.readAsDataURL(file);
    } catch (e) {
      reject(e);
    }
  });
}
```

### Collection using PSD renderer

```typescript
async function getImage(
  imageGenUrl: string,
  bucket: string,
  key: string,
  layers: (string | null)[][]
): Promise<string> {
  const response = await fetch(imageGenUrl, {
    method: "POST",
    mode: "cors",
    headers: {
      "x-api-key": getBootsAPIKey(),
      "Content-Type": "application/json",
      "x-stage": getBootsStage(),
    },
    body: JSON.stringify({
      bucket,
      key,
      layers,
    }),
  });
  const file = await response.blob();

  return await new Promise((resolve, reject) => {
    try {
      const reader = new FileReader();
      reader.onload = function () {
        resolve(this.result as string);
      };
      reader.onerror = reject;
      reader.readAsDataURL(file);
    } catch (e) {
      reject(e);
    }
  });
}
```
