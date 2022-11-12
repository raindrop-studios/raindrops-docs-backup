# API Reference

Tournaments users will interact with the Tournaments API via HTTP, this allows flexibility for a variety of user types with the service, we will proxy your requests to the blockchain for you after signing.

## Typescript HTTP Client

We support a typescript HTTP client which will always be compatible with our Tournaments API, we suggest starting here to try things out. The client is designed to be usable from web applications and scripting.

```typescript
import { Http } from "@raindrop-studios/events-client";
import { useWallet, useConnection } from '@solana/wallet-adapter-react';
import { AnchorProvider } from "@project-serum/anchor";

// grab the wallet and connection
const wallet = useWallet();
const { connection } = useConnection();

// create an Anchor Provider
const provider = new AnchorProvider(
    connection,
    wallet,
    {}
);

// Initialize the client Tournaments HTTP Client
const client = new Http.Tournaments.Client(provider, "mainnet-beta");
```

### Errors and State Reference

Tournaments is built on top of a generic Events Program, please refer to the Events Reference Errors & State Pages for detail. On those pages, a Tournament is an Event and a Match is a Contest.
