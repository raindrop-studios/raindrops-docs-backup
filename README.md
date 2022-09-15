# Introduction

The Solana ecosystem has a fragmented and very customized way of storing in-game assets on chain, with as many different formats as there are play-2-earn games. However, the methods of storing ordinary NFT data _are_ standardized in the [Metaplex Protocol](https://docs.metaplex.com). The aim of Raindrops Protocol is to do the same thing for game assets.

The Raindrops Protocol is a series of five a la carte contracts that govern on-chain or proof-on-chain data specifically for games, allowing any player or item to be interchangeable with any game client that can process them.

Following the [composability](https://en.wikipedia.org/wiki/Composability) doctrine, the Raindrops Protocol lives literally on top of the Metaplex Protocol, further decorating existing NFTs with new metadata about whether they are a [Player](https://github.com/long-banana/raindrops-docs/blob/main/broken-reference/README.md), an [Item](https://github.com/long-banana/raindrops-docs/blob/main/broken-reference/README.md), or both! All contracts within the Protocol are designed to be composed with other Solana contracts enforcing game-specific rules.

Each contract was built to work together to form a complete protocol that satisfies the needs of blockchain-based games, when using raindrops you retain the choice to include just the parts you need to build your game.

The protocol source is available on GitHub:

{% embed url="https://github.com/raindrops-protocol/raindrops" %}

{% hint style="warning" %}
The Raindrops Protocol is in an alpha state and presently only two contracts are eligible for use on Mainnet-Beta (Item and Matches Contract). While we will try to maintain the integrity of PDAs created as contract development iterates, there is no guarantee that this will be possible.
{% endhint %}

## Description

Learn about what's possible with the raindrops protocol

{% content-ref url="description.md" %}
[description.md](description.md)
{% endcontent-ref %}

## Quick Start

Jump in to the quick start docs and start making your first game's objects with raindrops:

{% content-ref url="quick-start.md" %}
[quick-start.md](quick-start.md)
{% endcontent-ref %}

## Concepts

There are several powerful concepts used across the raindrops protocol. They are outlined under this section

{% content-ref url="concepts/" %}
[concepts](concepts/)
{% endcontent-ref %}

## Contracts

Explore any contract to get a deep understanding of what it can do

{% content-ref url="contracts/item/" %}
[item](contracts/item/)
{% endcontent-ref %}

{% content-ref url="contracts/player/" %}
[player](contracts/player/)
{% endcontent-ref %}

{% content-ref url="contracts/match/" %}
[match](contracts/match/)
{% endcontent-ref %}

{% content-ref url="contracts/namespace/" %}
[namespace](contracts/namespace/)
{% endcontent-ref %}

{% content-ref url="contracts/staking/" %}
[staking](contracts/staking/)
{% endcontent-ref %}
