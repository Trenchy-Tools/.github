# TrenchyTools

**One API key to launch and trade memecoins** — pump.fun and PumpSwap (Solana), pons (Robinhood Chain).
No RPC node, no Jito client, no IPFS keys: the API builds unsigned transactions, your code signs locally.

**[trenchy.tools](https://trenchy.tools)** · [docs](https://trenchy.tools/docs) · [API spec](https://trenchy.tools/openapi.json) · [AGENTS.md](https://api.trenchy.tools/AGENTS.md) · [X @trenchytools](https://x.com/trenchytools)

## Start here

```bash
curl "https://api.trenchy.tools/api/create-api-key?label=my-agent"   # get a key
curl -H "x-api-key: ***" "https://api.trenchy.tools/api/me"          # verify it
```

Then read **[AGENTS.md](https://api.trenchy.tools/AGENTS.md)** — endpoint-by-endpoint, written for coding agents.

## Repos

| Repo | What it is |
|---|---|
| **[api](https://github.com/Trenchy-Tools/api)** | the product: pitch, quickstart, links |
| [pumpfun-starter](https://github.com/Trenchy-Tools/pumpfun-starter) | Solana: wallets, Jito-bundled launches (16 buyers), snipers, timed sells |
| [pons-starter](https://github.com/Trenchy-Tools/pons-starter) | Robinhood Chain: launches and trading, curve → Uniswap v4 |
| [wallet-mover](https://github.com/Trenchy-Tools/wallet-mover) | create, fund, split and consolidate wallets across chains |

Demos: [pumpfun.trenchy.tools](https://pumpfun.trenchy.tools) · [pons.trenchy.tools](https://pons.trenchy.tools) · [mover.trenchy.tools](https://mover.trenchy.tools)

## For agents

`openclaw skills install trenchytools` — a skill that teaches the full launch/trade flow (key → metadata → `trade-local` → local signing → `send`), with the wallet-backup rule and error-code discipline.
