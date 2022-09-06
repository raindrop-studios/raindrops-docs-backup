# Indexing

Throughout the contracts, with every mint there is often an associated index which is an `u64`. The reason for this is that while you may have a single NFT, you may wish to use it across multiple games. These different games may not wish to share a `Player` stat sheet or an `Item` definition. This is why all NFTs can have multiple `Items` and `Players` defined on top of them using the index as part of the seed. This index allows a single NFT can be used in different ways by different games.

Another common use-case might be to define index 0 of an NFT as an `ItemClass`, and index 1 as the `Item` for a true 1/1 `Item` so that you don’t need to have two NFTs to define a single legendary sword. Same could be done with a `PlayerClass`/`Player`.

{% hint style="warning" %}
It should be noted that if one `Item` PDA describes a `Consumable` that destroys the NFT, and you use the NFT in this way, it will be destroyed, regardless of its other definitions.
{% endhint %}
