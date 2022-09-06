# SFTs and Inexpensive Gaming

To keep gaming inexpensive, only stateful items should be NFTs.

Non-stateful items, like single-use potions, should be Semi-Fungible Tokens (supply > 0, decimals = 0, this requires only a metadata struct from the Metaplex Token Metadata Program with no edition struct).

In this way, all users share potions from the same mint, without needing to create new mints for each potion. There are certain limitations on SFTs being used, but the trade-offs in cost are extraordinary.
