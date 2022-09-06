# Example

Example config JSON: (stake.json)

```json
{
  "classIndex": 11,
  "parentClassIndex": null,
  "index": 20,
  "stakingIndex": 0,
  "artifactClassMint": "HVfbCH1wRsGVnrj95LFaytRiQ1mgb7gdGiKJsaHx3qJ5",
  "artifactClass": "DvtUpy2KGLAiA4SvLwxrmTaNUs6Zjk1i6a4vAY3ov6UC",
  "artifactMint": "HVfbCH1wRsGVnrj95LFaytRiQ1mgb7gdGiKJsaHx3qJ5",
  "artifact": "5grecm6WVz31Dy9aiUKBuVuTiuerdEqR8gHFAfMWHMuZ",
  "parentClassMint": null,
  "parentClass": null,
  "stakingAmount": 10000000000,
  "stakingPermissivenessToUse": { "updateAuthority": true },
  "stakingAccount": "BztKBroQAb42i93UUgqCoNmeTv6wiceHdp8tVhNXfVPW",
  "stakingMint": "3SRBwtc6r84HPLBqMNQCLNFFuGCwMc7Aof7Ngiqg9JsX",
  "metadataUpdateAuthority": "HGyYRWMfXurNiGce5cBdrSkgourS97Tp8poDRuaDVZUD",
  "namespace": "AmoCTRBCNWDVuseq3Va6E8d1Et29bxTw8YrP1hgXYV1D"
}
```

To begin stake warmup:

```bash
npx ts-node js/cli/src/staking.ts begin_artifact_stake_warmup \
    -k ~/.config/solana/id.json \
    -e devnet \
    -cp js/cli/example-configs/staking/stake.json
```

To end stake warmup:

```bash
npx ts-node js/cli/src/staking.ts end_artifact_stake_warmup \
    -k ~/.config/solana/id.json \
    -e devnet \
    -cp js/cli/example-configs/staking/stake.json
```

To begin stake cooldown:

```bash
npx ts-node js/cli/src/staking.ts begin_artifact_stake_cooldown \
    -k ~/.config/solana/id.json \
    -e devnet \
    -cp js/cli/example-configs/staking/stake.json
```

To end stake cooldown:

```bash
npx ts-node js/cli/src/staking.ts end_artifact_stake_cooldown \
    -k ~/.config/solana/id.json \
    -e devnet \
    -cp js/cli/example-configs/staking/stake.json
```
