# Tournaments

Tournaments is an Events service for creating and managing tournament events. You can use an HTTP client to interact with our API. Soon after the initial release of the API you will also be able to use a Web UI to create and run a tournament.

## Features

* Unlimited matches and participants per tournament
* Rewards escrow (aka Prize pool)
  * Entry fees can be used for rewards
  * Unlimited number of rewards can be held
  * Customizable reward distribution
* Optionally enforce token gating for tournament entry
* Optionally require entry fees to join a tournament
* Ban tournament cheaters or revoke any of their rewards for cheating in a match
* Data availability, it's simple to query the existing state of the tournament without having to store anything client side
