# Terminology

### EntryFee

An EntryFee can be optionally set at Tournament creation, requires all participants entering the tournament to pay a fee upon entrance. There can only be one tournament entry fee at this time

### Match

Multiple Matches can be created within a Tournament, each Match can have an unlimited number of participants, winners of matches accrue Points.

### Participant

A Participant is an entity which has entered a Tournament and is eligible to play matches

### Points

Points are accrued by winners of Matches within a Tournament. These points are used to keep track of which participants are eligible to move onto the next Tournament Round. Throughout the Tournament it's possible to query the point totals of all participating. Tournament Authorities can use these point totals to determine distribution of Tournament Rewards. In addition, if it's determined that one or multiple participants have cheated, their points can be revoked.

### Reward

Rewards are used to incentivize participants to enter into Tournaments. There can be unlimited number of rewards and the Tournament Authority has complete control over the distribution of these Rewards after the Tournament has been moved to the Ended State. Optionally, the Tournament Entry Fee tokens can be used as a Tournament Reward.

### Round

A Round is a grouping of matches within a Tournament, each Round has a unique Round Index. The first round in a Tournament has a Round Index of 0, this means that any participant is eligible to play in the first round of matches (provided they have entered the Tournament of course!).&#x20;

The winners of each match within a Round are awarded 1 point, this corresponds to the Round Index. For example, the Second Round in this Tournament has a Round Index of 1, which means participants who have been awarded 1 Point from playing in the previous round are eligible for these new Matches.&#x20;

The farther along a participant makes it within a Tournament, the more points they accrue and the Tournament Authority can query these point totals to make a decision on Reward distribution.

### TokenGate

When a Tournament is created it's possible to add a Token Gate, a Token Gate requires that a prospective participant has a particular mint and amount of said mint in their wallet upon joining. One use case of this might be a whitelist token, only allowing participants with the token to be eligible to play in the tournament.

### Tournament

A Tournament is a series of Matches in which participants compete for escrowed Rewards, the Tournament results are recorded on chain and when complete, are immutable and forever public.

