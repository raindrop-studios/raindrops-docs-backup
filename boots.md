# NFTs <> Boots

Boots is a proprietary NFT upgrade service that exists on top of the Raindrops Protocol that allows NFT holders to trade and collect traits on their NFT in a controlled and fee-gated environment that produces reliable new revenue streams for NFT companies and the platform and is consistent with web3 principles.

## Current Ecosystem Limitations

### People like customizing...and they can't

The only way to customize an NFT presently is to trade it for another. The best NFT collections are the ones with enough trait variance that a given user can find a PFP that matches about 80% of their personality. Inevitably, the quest for a "forever PFP" is out of reach for most and more importantly, doesn't lead to much money exchanging hands.

### Royalties decrease over time

In the traditional secondary sales model, volume and therefore income to NFT companies decreases over time as collectors settle in for the long haul. There is little incentive to trade on existing traits, and speculators lose interest in collections that are no longer new.

### New sub-collections dilute brand strength

Releasing new sub-collections to revitalize revenue is a short-term salve. The long-term effect is that your brand is now diluted across many different collections, all which share the same-sized user base and compete for volume. You may have won a short-term cash prize but in the long term you now have more collections to maintain and a wider roadmap to service.

### Royalties are tough to enforce

Royalties on Solana are unenforceable because the Token Program has no idea what they are, and doesn't care what they say when a user initiates a token transfer. There are no plans by the Solana team to merge the Token Metadata program into the Token Program at any point in the future to rectify this. The only real solution to this is to either turn the Token Metadata program into a clone of the Token Program, which is infeasible, or enforce royalties punitively, which does not have 100% efficacy.

## The Boots Solution

### Traits are Tokens

All NFTs come with some traits that are customizable and some that are inherent traits, as defined by the Raindrops protocol. Think what shirt an NFT is wearing vs its skin color. The shirt is a token that the NFT is carrying in its backpack and is presently equipped. It's skin-color is a piece of data recorded in an on-chain account [similar to Metadata from Metaplex](contracts/player/). The token can be unequipped, removed, and like any old semi-fungible token, traded. On removal or addition, the NFT's image is updated to reflect the image change.

Now people can truly customize their NFT, and can get to 100% match without breaking the bank!

### Royalties Remain Constant

With Project Boots, new SFT tokens representing new traits can be dropped by the season or monthly using the Launchpad feature. This can take place through collaborating and splitting revenue/royalties with artists, other major clothing brands, or by releasing your own new traits. There will also be opportunities to use Cupcake technology to couple the clothing to IRL phygital goods.&#x20;

Fashion brands have used this technique from time immemorial to revitalize their income streams every season and every year. Why trade on last year's trait?&#x20;

### New trait collections grow brand strength

With each new trait collection, the power of expression for your NFT collection grows. Without sub-collections to dilute volume, it remains moving in the base collection, propping up royalties there. Customers will be forced to keep up with each monthly or season installment of traits or their NFT will fall out of cultural relevance. Old traits will trade on a secondary market similar to discount stores found in the real world today.

### Fees are the new Royalties

With the Project Boots system, while our marketplace does enforce royalties when the secondary market is used for trait token sales, this is not intended to be the primary source of revenue. All Boots enabled collections require the authority on the collection to sign off on any addition, removal, equipping, or un-equipping of any trait on the collection. What this means is that the NFT Collection Owners are the gatekeepers of change.

When a user wishes to apply a new trait in their NFT's backpack, they could attempt to sign a transaction that tells the Raindrops protocol to do this, but it would fail because they lack permissions on Boots NFTs. They instead must cosign a transaction with the NFT Collection Owner. The Boots system will provide such a cosigned transaction, but this transaction will come with a standard SOL fee as a side-instruction - which will be split 20% with the platform and 80% among the royalty recipients on the NFT Collections.

This new revenue source is guaranteed by the protocol, cannot be bypassed, and while smaller in magnitude than a secondary sale, is going to happen significantly more frequently. Web2 has already proven the magnitude and power of micro-transactions. This is the future of the NFT ecosystem and the future of your company.

Welcome to Boots.

