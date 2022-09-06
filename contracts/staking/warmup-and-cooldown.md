# Warmup and Cooldown

Staking has two states, warmup and cooldown.

In warmup state, the staking tokens will be transferred from the wallet to a controlled escrow account and then to the controlled internal bank account of artifact. In cooldown state, on the contrary, the tokens will be transferred from the controlled internal back account of artifact to the controlled escrow account and then back to the wallet.

Warmup has two instructions.

* `begin_artifact_stake_warmup`
* `end_artifact_stake_warmup`

Here, `begin_artifact_stake_warmup` will transfer tokens from the user wallet to the controlled escrow account and `end_artifact_stake_warmup` will transfer tokens from the controlled escrow account to the artifact bank account.

And cooldown has two instructions.

* `begin_artifact_stake_cooldown`
* `end_artifact_stake_cooldown`

Here, `begin_artifact_stake_cooldown` will transfer tokens from the artifact bank account to the controlled escrow account and `end_artifact_stake_cooldown` will finally transfer tokens back to the user wallet.

{% hint style="info" %}
To stake artifact, artifact must be joined to the namespace and the staking token must be whitelisted in that namespace.
{% endhint %}
