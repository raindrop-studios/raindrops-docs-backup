# Basic

As mentioned in the Introduction, the raindrops protocol is a series of 5 contracts running on Solana. These contracts govern on-chain or proof-on-chain data specifically for games, currently. This allows any player or item data to be interchangeable with any game client that wishes to process them.

Let's go through the "Who, What, Why, and How" of the raindrops protocol.

## Who can use it?

Since raindrops is made up of 5 contracts, each of which is specialized to different functions/needs of a game, a game is able to choose any contract(s) that provide just what they need. Or they can decide to use all of them. This allows for games of all sizes and complexities, as well as games that already exist or ones being built from the beginning to benefit from using raindrops.

An existing or established game can decide if they want to move just one feature of their game at a time. Or they can integrate raindrops by using it for an entirely new feature they want to build.

A brand new game will have more freedom to use raindrops in it's entirety from the very beginning. This will greatly reduce the cost and time it takes to get a game into gamers hands, reduce a lot of ongoing headaches with maintaining the same code common to all games, and starting from day one, make their game a part of the raindrops ecosystem of connected games.

## What does it make possible?

What does this mean for gaming and what even is an ecosystem of connected games?

Just like bitcoin introduced a trust-less way for anyone in the world to create and access transaction information for a currency moving from one wallet to another. Raindrops does this for gaming, but it's not specific to a game's economic transactions.

The types of data raindrops makes available consists of [items](advanced/item.md), [players](advanced/player.md), [games](advanced/game.md), [matches](advanced/match.md) and [staking](advanced/staking.md). Having this data available on-chain enables games to do very cool things that have just never been possible, or were prohibitively expensive to do.

We should first break down why this actually matters for gaming (it's actually applicable beyond gaming, but let's start there) so we can better understand what it actually means.

## Why does it matter?

Why is this information so important and ground-breaking for gaming? Let's reference bitcoin again for a moment.

When bitcoin made transaction data available to anyone in the world, and it was trust-worthy, suddenly the world had a global ledger(database) for anyone to add to and read from. This not only cut out the middle men, it also made it possible to access all the data the middle men might have never even made available, in addition to the start and end state of the data(who owns which bitcoins). Before bitcoin, the only way to track and get data about a currency transaction was to communicate with each banking entity involved, and potentially everything in between. That's assuming everyone involved even provided access to the data and you were allowed to talk to them. That's an enormous undertaking from both a technology and time-cost perspective. Each hand-off from one entity to another can take an undetermined amount of time, as well as be rolled back in the event of a refund or some other event. With bitcoin, you now have one place to look for this information, you can trust it will be accurate, and after enough time has passed, it's very unlikely to ever be rolled back.

So, how does this apply to gaming? And why should you care?

Gaming has the exact same fundamental problem. Before raindrops, every game has been siloed and is separate from one another. Each game has its own database, hidden behind a group of servers, or isn’t even on a server but stored locally on your computer. In addition to that, each game speaks it's own language. That language may even be proprietary and unintelligible without spending a very large amount of time decoding it. This means the only way to share/access game information between two games is to be bilingual and write very specific software that connects to both. That's assuming both games even make their information available. Most don't. This becomes incredibly time consuming and brittle. Therefore, most games never even try to do it. Which is a huge shame and a big loss for gaming as a whole.

It's even more involved then that within the pre-raindrops state of gaming. If you are able to have two games communicate with each other, you're dependent on both games never changing their language. Sometimes that isn't possible if they need to build something new or fix something that's broken. The availability of both game's servers also come into play. If either of the game's servers go down or the language they use changes, you now can't communicate without updating the software connecting them together, or by implementing usually complicated logic that handles these error cases when they happen. This really sucks for game developers and the players that play their game.

Raindrops eliminates all of that and empowers game companies by not forcing them to implement all this common logic themselves, as well as making their game's data available for any other game to consume. This provides a far more immersive gaming experience. Raindrops also provides solutions to common functions many games need to build themselves to just make their games playable. That stops the same bugs from occuring across many different implementations inside each game, as well as the expenses and time each game has to incur to build and maintain their own version. Furthermore, in the blockchain world, without raindrops, each game needs their custom software to be audited for security and data purposes.

Does all this complexity seem error prone, wasteful, and make your head hurt yet? We hate to think about all the time lost and how much further along gaming could be if these problems didn't exist!

Raindrops eliminates these problems. Games can now have one source of truth, one language for communicating with one another, and save a whole lot of time and money in the process of building and maintaining a game. In addition to being more secure.

## How does it change gaming?

By using raindrops, a game's data is available **on-chain** to itself as well as any other game that wants to use it. This data can be read from a contract running on solana or by making an HTTP request.

Even more interestingly, it doesn't have to just be other games that use the data either. Say someone wants to build a dashboard to view the progress of other players/items in a game, or to show how a Legendary Sword has been used across multiple games and what game caused it to take the most damage. They can do all that using the data made available by games using raindrops.

Best of all, the data is verified to be accurate since it uses the same mechanisms used when sending tokens(currency, NFTs, etc...) from one wallet to another. Games can now trust that an item and it's data hasn't been tampered with and the game that updated it is who they claim to be.

In addition, raindrops is compatible with the $RAIN token. The $RAIN token reduces friction for the gamer to play different games.

We don't believe the future of gaming is to have a different token for every game you want to play. We don't know about you, but we don't want to have 10+ different gaming tokens in our wallets to play the games we love.

If a game already has their own token and they want to continue using it, raindrops does support any SPL mint for gameplay costs, rewards, or staking.

## Again, What does this make possible?

With that background, let's ask again, what does raindrops make possible?

For one, gone are the days where your hard work and accomplishments have to be stuck in a single game or lost completely if a game ceases to exist. If a player decides they want to sell their Legendary Sword that they have been leveling up through play in one game, they can, and whomever chooses to buy it will get that sword at it's current level rather then having to start from scratch back at level 1. This means your in-game work using an item will create real-world value.

It's also possible to use that leveled up sword in a completely different game with the same level stats. How crazy is that?! Before raindrops, this would be unheard of to have an item work across games and have the same stats without a significant amount of work and coordination between two games. With raindrops, all the data is just there, and it's in the same format for every game to use. Simple. No surprises.

This also means that a player's progress can be shared across games. That might seem like a more abstract concept, but you can imagine something along the lines of if you were to beat [Rainbow Road](https://www.mariowiki.com/Rainbow\_Road) while playing Mario Kart 1, it could unlock a special level in Mario Kart 2 that you can only unlock by beating Rainbow Road on Mario Kart 1. While this example highlights what is possible within just the Mario Kart universe, it also works within any other game. A game series like [Need For Speed](https://en.wikipedia.org/wiki/Need\_for\_Speed) could see that you've beaten Rainbow Road and unlock special cars or tracks that are only available to players with that acheivement. No specific coordination would be required between the makers of Mario Kart and Need For Speed besides using the raindrops protocol.

Those are just a few examples of what is possible within an ecosystem of games connected through raindrops. What we're most excited about is what we haven't even imagined is possible when games share both the language and the storage of their game data, and it’s verifiable.
