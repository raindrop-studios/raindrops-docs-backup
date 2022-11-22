---
description: A comprehensive list of endpoints exposed by our Tournaments API
---

# Endpoints

## Overview

Each Endpoint has a GET and a POST operation, the GET will generate a prepared transaction for the endpoint, complete with signatures from newly created accounts and our API signer. Next, this transaction must be signed by the caller and send back in a POST body. We will validate the transaction received via HTTP POST and forward this along to the Solana network.

```bash
// Mainnet-Beta Base URL
https://api.tournaments.raindrops.xyz

// Devnet Base URL
https://api-dev.tournaments.raindrops.xyz
```

```
// Generic POST, there is one POST one GET per endpoint listed below
curl -X POST -H 'Content-Type: application/json' 'https://$BASE_URL/$ENDPOINT' \
-d '{ "tx": "$BASE64_ENCODED_STRING" }'
```

### AddEntryFeeAsReward

Transfer tokens collected by a Tournaments Entry Fee to the Reward Escrow, this enables the Entry Fee to be redistributed to tournament participants. This endpoint is only callable by a Tournament Authority.

```markdown
Path: /addEntryFeeAsReward
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
Returns:
- Reward PublicKey
```

<pre class="language-typescript"><code class="lang-typescript"><strong>// Tournaments Client
</strong><strong>const reward =await authority.addEntryFeeAsReward("&#x3C;tournamentPubkey>")</strong></code></pre>

### AddReward

Transfer tokens from the Tournament Authority to the Reward Escrow. It's important to specify the Reward Amount with the correct decimal precision. This endpoint is only callable by a Tournament Authority.

Example: 1 $USDC would be a reward amount of "100000", USDC has 6 decimals of precision.

```markdown
Path: /addReward
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
- RewardMint: PublicKey
- RewardAmount: String
Returns:
- Reward PublicKey
```

```typescript
const reward =await authority.addReward("<tournamentPubkey", "<rewardMint>", "<rewardAmount>");

// Example: create a reward of 1 $USDC
const reward =await authority.addReward("<tournamentPubkey", "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v", "100000");
```

### BanCheater

Revoke all tournament points gained by a detected cheater in a tournament. This endpoint is only callable by a Tournament Authority.

```markdown
Path: /banCheater
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
- Cheater: PublicKey
```

<pre class="language-typescript"><code class="lang-typescript"><strong>await authority.banCheater("&#x3C;tournamentPubkey>", "cheaterPubkey")</strong></code></pre>

### CreateRound

Create a new round of matches within a Tournament. For each new round, increment the Round Index by 1, the API uses the Participants per Round to determine the number of matches to create for a round. This endpoint is only callable by a Tournament Authority.

```markdown
Path: /createRound
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
- ParticipantsPerMatch: Integer
- RoundIndex: Integer
Returns:
- Matches Addresses PublicKey[]
```

```typescript
const matches =await authority.createRound("<tournamentPubkey>", participantsPerRound, roundIndex)
```

### CreateTournament

Create a new Tournament, the creator mints a Tournament Authority token granting them full control over Tournament operations.&#x20;

Specify a Name and a Tournament Size, optionally specify an Entry Fee and/or a Token Gate. The Name cannot be longer than 100 characters. The Size sets a limit on number of participants who can join, but this limit does not need to be reached to start the Tournament.&#x20;

An Entry Fee requires a Mint and an Amount which each participant must pay to enter into your Tournament.&#x20;

A Token Gate requires a Mint and an Amount which each participant must have in their Wallet to be eligible to enter into your Tournament.

```markdown
Path: /createTournament
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
- Name: String, max 100 characters
- Size: Integer,
- EntryFee: Optional
    - EntryFeeMint: PublicKey
    - EntryFeeAmount: String
- TokenGate: Optional
    - TokenGateMint: PublicKey
    - TokenGateAmount: String
Returns:
- Tournament PublicKey
```

```typescript
// tournament without entry fee or token gate
const tournament = await authority.createTournament("A Cool Tournament", 4);

// tournament with a 1 $USDC entry fee
const tournament = await authority.createTournament("Entry Fee Tournament", 4, { mint: PublicKey("EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v"), amount: anchor.BN(100000) });

// tournament requiring 1 $USDC in wallet to join
const tournament = await authority.createTournament("Entry Fee Tournament", 4, null, { mint: PublicKey("EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v"), amount: anchor.BN(100000) });
```

### DistributeReward

Distribute the tokens stored in a Tournament Reward Escrow to a Tournament Participant

```markdown
Path: /distributeReward
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, signer
- Participant: PublicKey
- Reward: PublicKey
- RewardAmount: string
```

```typescript
await authority.distributeReward("<tournamentPubkey>", "<participantPubkey>", "<rewardPubkey>", "<rewardAmount>");
```

### EndMatch

Update the state of a Match to Ended. This endpoint is only callable by a Tournament Authority.

Before a winner of a match can be determined, the Match must be in the Ended State.

```markdown
Path: /endMatch
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
- Match: PublicKey
```

```typescript
await authority.endMatch("<tournamentPubkey>", "<matchPubkey>");
```

### EndTournament

Update the state of the Tournament to Ended. This endpoint is only callable by a Tournament Authority.

When a Tournament is moved to Ended, no more Matches or Rounds can be created. Cheaters can still be detected and banned at this stage, this is where rewards would be distributed to eligible participants.

```markdown
Path: /endTournament
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
```

```typescript
await authority.endTournament("<tournamentPubkey>");
```

### EnterMatch

Enter a Tournament Participant into a Match. This endpoint is only callable by a Tournament Authority.

The Tournament Authority is in control of which participants enter which Matches so that the Tournament Authority can control bracketing and matchmaking semantics.

```markdown
Path: /enterMatch
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
- Match: PublicKey,
- Participant: PublicKey,
```

```typescript
await authority.enterMatch("<tournamentPubkey>", "<matchPubkey>", "<participantPubkey>")
```

### EnterTournament

A participant uses this endpoint to enter into a tournament of their choice. If the tournament has an Entry Fee or Token Gate configured, the participant must pay or have in their wallet the necessary tokens.

```markdown
Path: /enterTournament
Parameters:
- Tournament: PublicKey
- Participant: PublicKey, Signer
```

```typescript
await participant.enterTournament("<tournamentPubkey>");
```

### FinalizeTournament

Finalize the results of a Tournament, all rewards have be distributed, cheaters banned and the results of the Tournament become immutable. This endpoint is only callable by a Tournament Authority.

```markdown
Path: /finalizeTournament
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
```

```typescript
await authority.finalizeTournament("<tournamentPubkey>");
```

### GetMatch

Retrieve Match Details in JSON format

```markdown
Path: /match
Parameters:
- Match: PublicKey
Returns:
- Match Data
```

```typescript
const matchData = await authority.getMatch("<matchPubkey>");
```

### GetMatchesByRound

Retrieve all Matches of a particular Round in a tournament. Use the Round Index to select a particular round. Flip the finalized Boolean if you would like to selectively retrieve Matches which are finalized or not.

```markdown
Path: /matchesByRound
Parameters:
- Tournament: PublicKey
- RoundIndex: Integer
- Finalized: Boolean
Returns:
- Matches PublicKey[]
```

```typescript
const matches = await authority.getMatchesByRound("<tournamentPubkey>", roundIndex, finalized);
```

### GetMatchParticipants

Retrieve all participants for a particular Match.

```markdown
Path: /matchParticipants
Parameters:
- Tournament: PublicKey
- Match: PublicKey
Returns:
- Participants: PublicKey[]
```

```typescript
const participants = await authority.getMatchParticipants("<tournamentPubkey>", "<matchPubkey>");
```

### GetParticipantsForRound

Retrieve all participants who are eligible for a particular Round, regardless if they have entered a Match in that Round or not.

```markdown
Path: /participantsForRound
Parameters:
- Tournament: PublicKey
- RoundIndex: Integer
Returns:
- Participants: PublicKey[]
```

```typescript
const participants = await authority.getParticipantsForRound("<tournamentPubkey>", roundIndex);
```

### GetStandings

Retrieve current Tournament Standings sorted descending from most points awarded. For each Match win a participant is awarded 1 Tournament Point.

```markdown
Path: /standings
Parameters:
- Tournament: PublicKey
Returns:
- Standings: string[][] -- "<particpantPubkey>", "<pointsAmount>" -- sorted descending
```

```typescript
const standings = await authority.getStandings("<tournamentPubkey>");
```

### GetTournament

Retrieve Tournament Details in JSON format

```markdown
Path: /tournament
Parameters:
- Tournament: PublicKey
Returns:
- Tournament Data
```

```typescript
const tournamentData = await authority.getTournament("<tournamentPubkey>");
```

### SetMatchResult

Determine a Winner of an Ended Match and move the Match into the Finalized State. This endpoint is only callable by a Tournament Authority.&#x20;

The Winner will receive 1 Point in their points token account. Tournaments uses the points to determine which participants are eligible to play in subsequent tournament rounds and for participants and managers to keep track of Tournament state.

Currently only 1 winner can be selected but we will make this endpoint more flexible to support multiple winners in the future.

```markdown
Path: /setMatchResult
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
- Match: PublicKey
- Winner: PublicKey
```

```typescript
await authority.setMatchResult("<tournamentPubkey>", "<matchPubkey>", "<winnerPubkey>"););
```

### StartMatch

Move a Match within a Tournament into the Started State, this signifies that the Match is beginning to be played out on chain, no other participants may enter this Match. This endpoint is only callable by a Tournament Authority.

```markdown
Path: /startMatch
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
- Match: PublicKey
```

```typescript
await authority.startMatch("<tournamentPubkey>", "<matchPubkey>");
```

### StartTournament

Move a Tournament into the Started State, no more participants may enter the tournament and now it's possible to begin creating Tournament Rounds. This endpoint is only callable by a Tournament Authority.&#x20;

```markdown
Path: /startTournament
Parameters:
- Tournament: PublicKey
- Authority: PublicKey, Signer
```

```typescript
await authority.startTournament("<tournamentPubkey>");
```
