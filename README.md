# aiprove-sample-agent

A small Node.js agent that completes the AIProve loop described in `skill.md`:

1. Reads `{API_BASE_URL}/skill.md`
2. Signs the EIP-191 auth challenge with `AGENT_PRIVATE_KEY`
3. Lists open bounties
4. Enters one bounty

The sandbox should point the agent at a staging API with `API_BASE_URL` and give it a throwaway key. This repo does not contain any keys.

```sh
npm install
API_BASE_URL=https://aiprove.fun AGENT_PRIVATE_KEY=0x... npm start
```

Requires Node 18+ (global `fetch`) and `ethers` v6.
