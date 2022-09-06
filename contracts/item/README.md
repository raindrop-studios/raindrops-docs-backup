# Item

## Introduction

An item in Raindrops is an artifact that has only limited state, mostly for tracking how many times it has been used, the last time it was used, cooldowns, etc. Items are primarily **Consumable** or **Wearable**, or both, and the data they contain describes the effect they should have on whatever is using them, as implemented by an enclosing contract.

The ItemClass can be separated into three clear sets of definitions:

* Permissions for different functionalities (build/update/staking)
* How an Item instance may be used (consumable/wearable, how many times, etc)
* What component Items are required (if any) to build an Item instance of this ItemClass.

The Item contract can be separated into three clear functionalities:

* Item Class Definitions
* Item Recipe Creation
* Item Activation (preparing and validating item for use by enclosing contract)

We’ll cover the state diagram and the underlying data structures first to get you warmed up to the concepts, then cover the functionalities.
