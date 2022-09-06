# Match

## Introduction

The matches contract is a simple escrow contract that allows for an independent oracle to redistribute tokens added to the match. The idea is to support multiplayer gaming. This contract will be developed further in the future, to add new features such as:

* Match defines maximum loss allowed by oracle for joiners to cross-compare
* Match has support for player backpacks once player contract comes online, so that items can swap player backpacks without the player having to add those items directly to the match
* Match CLI support for Merkle roots
* Build out logic for minimum\_allowed\_entry\_time
