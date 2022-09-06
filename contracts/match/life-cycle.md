# Life Cycle

1. Draft - Nobody can join the match in this state, but it is updatable by its authority.
2. Initialized - Entrants can join provided they meet at least one TokenValidation. No TokenValidations means anybody can join. Oracles cannot effect a match in this state. Can initialize the match in this state if you wish.
3. Started - Entrants can join provided the match has join\_allowed\_during\_start is set to true. Entrants can leave if leave\_allowed is set to true. This state can only be reached by the match authority updating the match from the Initialized state.
4. Finalized - This state can only be reached by the finalized boolean on the oracle being flipped to true. Then update\_match\_from\_oracle can be called permissionlessly to get Match into this state. Once here, entrant’s tokens can be paid out to the original entrants, or new recipients, based on the TokenDeltas present in the oracle. Note: An oracle need not be created for a given match until you wish to Finalize the match.
5. PaidOut - This state is reached once all tokens have been removed from the oracle.
6. Deactivated - This state can be reached via a direct call to update\_match while in Draft or Initialized state, or from PaidOut state. The Match MUST be in this state before drain\_match is available to reclaim lamports.
