# SFTs and Inexpensive Gaming

To keep gaming inexpensive, only stateful `Items` should be NFTs.

Non-stateful `Items`, like single-use potions, should be Semi-Fungible Tokens (supply > 0, decimals = 0, this requires only a metadata struct from the Metaplex Token Metadata Program with no edition struct).

In this way, all users share potions from the same mint, without needing to create new mints for each potion. There are certain limitations on SFTs being used, but the trade-offs in cost are extraordinary.

What this means is that you only need a single NFT defining the `ItemClass` for a given SFT item, and then a second mint of semi-fungibles representing the supply that you sell or give to users. It is on top of this mint that you define the`Item`. As long as you meet the rules of SFT `Items`, you've now got a very efficient gameplay item.
