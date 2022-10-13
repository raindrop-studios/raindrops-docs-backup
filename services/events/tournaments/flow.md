# Flow

1. Create a Tournament
   * Tournament Name
   * Tournament Size
   * Entry Fee (optional)
   * Token Gate (optional)
2. Users can now enter the tournament if they meet all the requirements (token gating and paying the entry fee if specified)
3. Optionally, add tournament rewards, this will escrow the funds on-chain. Adding rewards can be done throughout the entire tournament lifecycle.
4. Update the tournament state to started, no more participants can join at this time
5. Create a round of tournament matches, initial release assumes each match is a 1v1 scenario.
6. The tournament creator can now assign the participants to each match however they like and make each match as started.
7. For each match, the creator will declare the winner and set the match to ended
8. Continue creating new rounds within the tournament and pairing up participants until you determine a winner.
9. When a winner is determined, move the tournament state to Ended.
10. When the tournament is ended, it's time to distribute the rewards! This is configurable, the winner can receive all or it can be split up based on tournament performance.
11. After all the rewards are distributed, mark the tournament as finalized, once a tournament is in finalized the results are set and no further changes can be made. The state of the tournament is now frozen on chain forever.
