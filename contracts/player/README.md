# Player

## Introduction

A `Player` in Raindrops is the primary primitive of the entire protocol. Just like `Item`, it follows a class-inheritance system and has permissions for different functionalities. Every `PlayerClass` represents a "blueprint" NFT that could be used to turn another NFT into a `Player`, and once done, that NFT gains certain privileges, such as:

* The right to store items and other players in their internal backpack, removing those NFTs/SFTs from your wallet, making for easy transport across your wallets. Never worry about transporting your player + 10 pieces of equipment from hot wallet to hot wallet again!
* The right to equip items on various body parts
* The right to have body parts!
* The right to have different attributes of different data types that can change over time from outside stimuli, all on chain
* The right to use items on oneself or on others per recipes encoded on chain

The underlying `PlayerClass` for any `Player` has permissions for different functionalities that control what a holder may do, such as:

* Equipping, adding, or using items
* Updating one's stats
* Building new Players
* Staking

We’ll cover `PlayerClass` first, and then look at `Player` to see how they connect, and then move on to some Live Fire exercises.
