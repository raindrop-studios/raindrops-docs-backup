# Guide

This first script highlights tournaments setup taken by the Tournament Authority, the Authority has full control over configuration, point and reward distribution.

```typescript
import { Http } from "@raindrop-studios/events-client";

// tournament authority controls the tournament
const authority = new Http.Tournaments.Client(
    `${os.homedir()}/.config/solana/id.json`,
    "mainnet-beta"
);

// create a tournament with a max size of 4 participants
// do not require any Token Gates or Entry Fee to be paid
// keep track of the tournament pubkey returned, all data can be retrieved from this
// DETAILS:
// An optional Entry Fee can be added that participants must pay to enter the tournament
// An optional Token Gate can be added which participants are required to own to be eligible to enter the tournament
// Both of these optional arguments can be required together
const tournament = await authority.createTournament("simple", 4, null, null);

// Add a token reward, this will move the token(s) into tournament escrow
// DETAILS:
// unlimited rewards are allowed
// collected entry fees can be moved into reward escrow
// rewards can be added throughout the tournament
await authority.addReward("tournamentPubkey", "rewardMint", "rewardAmount");
```

With the Tournament configured, participants can now enter the tournament

```typescript
import { Http } from "@raindrop-studios/events-client";

// A Participant initializes their client to enter the tournament
const participant = new Http.Tournaments.Client(
    `${os.homedir()}/.config/solana/id.json`,
    "mainnet-beta"
);

// participant now enters the tournament
await participant.enterTournament("tournamentPubkey");

```

Once all participants have entered, it's time to start the tournament. When the tournament moves into the started state, no more participants can join.

```typescript
// start the tournament
await authority.startTournament("tournamentPubkey");
```

Now that the tournament has started, it's time to create a tournament round. A round is simply a collection of matches in which participants face off against each other.

```typescript
// As this is the first round, the roundIndex is 0
// The roundIndex tracks which matches belong to a round
await authority.createRound("tournamentPubkey", roundIndex = 0);
```

After the round of matches have been created, it's time to select which participants face each other in each match, this is completely up to the Tournament Authority

```typescript
// get the list of matches for this round
const matches = await authority.getMatchesByRound("tournamentPubkey", roundIndex = 0, finalized = false);

// get the list of tournament participants eligible for this round (all of them in this example)
const participants = await authority.getParticipantsForRound("tournamentPubkey", roundIndex = 0);

// enter each participant into the match of your choosing
// NOTE: this code only enters 1 participant into 1 match, it's open ended
await authority.enterMatch("tournamentPubkey", "matchPubkey", "participantPubkey");
```

\~Matches are now played off chain\~

Once the matches finish, it's time to tell Tournaments who won!

```typescript
// get the list of matches for this round
const matches = await authority.getMatchesByRound("tournamentPubkey", roundIndex = 0, finalized = false);

// get the list of tournament participants eligible for this round (all of them in this example)
const participants = await authority.getParticipantsForRound("tournamentPubkey", roundIndex = 0);

// end the match
await authority.endMatch("tournamentPubkey", "matchPubkey");

// set the result of the match
await authority.setMatchResult("tournamentPubkey", "matchPubkey", "winnerPubkey")
```

At this point, a full round of a tournament has been played out off-chain and the results have been written on-chain. Repeat this flow until a tournament winner has been determined. For each round, increment the `roundIndex` by 1.

Lets say the final tournament standings have been determined, it's time to wrap this up!

```typescript
// end the tournament, no more matches can be played
await tournamentAuthority.endTournament("tournamentPubkey");

// get the final standings of the tournament
// the first participant in the returned array has the most points
// DETAILS:
// For each round the match winner is awarded 1 point
// Use points to keep track of participant progress
const finalStandings = await tournamentAuthority.getStandings("tournamentPubkey");

// In our simple tournament, it's winner take all
// distribute our rewards to the winner
// NOTE: rewards can be distributed to any number of participants
await tournamentAuthority.distributeRewardToWinner("tournamentPubkey", finalStandings[0][0]);

// Once rewards have been distributed, finalize the tournament to make it immutable
await tournamentAuthority.finalizeTournament("tournamentPubkey");
```
