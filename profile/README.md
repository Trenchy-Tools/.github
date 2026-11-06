<p align="center"><img src="./banner.png" alt="TrenchyTools API" width="100%"></p>

<p align="center"><a href="https://trenchy.tools/docs">Docs</a> · <a href="https://api.trenchy.tools/api/create-api-key">Get an API key</a> · <a href="https://api.trenchy.tools/AGENTS.md">AGENTS.md</a> · <a href="https://api.trenchy.tools/openapi.json">OpenAPI</a> · <a href="https://trenchy.tools/status">Status</a> · <a href="https://t.me/trenchytools"><img src="https://cdn.simpleicons.org/telegram/26A5E4" height="14" alt="Telegram"> Telegram</a> · <a href="https://x.com/trenchytools"><img src="https://cdn.simpleicons.org/x/1d9bf0" height="14" alt="X"> X</a></p>

### Live demos

<a href="https://pumpfun.trenchy.tools"><img src="https://img.shields.io/badge/pump.fun_launcher-f7931a?style=for-the-badge&logo=solana&logoColor=white" /></a> <a href="https://pons.trenchy.tools"><img src="https://img.shields.io/badge/pons_launcher-8957e5?style=for-the-badge&logo=ethereum&logoColor=white" /></a> <a href="https://mover.trenchy.tools"><img src="https://img.shields.io/badge/wallet_mover-1f6feb?style=for-the-badge&logo=bitcoin&logoColor=white" /></a> <a href="https://elysium.trenchy.tools"><img src="https://img.shields.io/badge/elysium_launcher-2ea043?style=for-the-badge&logo=hyperliquid&logoColor=white" /></a> 

Open any of them in the browser — wallets are created locally and stay in your browser.

**TrenchyTools** is a trading and launch API for pump.fun, PumpSwap and pons. One API key replaces the RPC node, the Jito client and the IPFS keys: the API builds unsigned transactions, your code signs them locally, the API sends them.

### Community

<p><a href="https://t.me/trenchytools"><img src="https://cdn.simpleicons.org/telegram/26A5E4" height="16" alt="Telegram"> <b>Telegram channel</b></a> — announcements, new starters, uptime<br>
<a href="https://t.me/dogtoshi_x"><img src="https://cdn.simpleicons.org/telegram/26A5E4" height="16" alt="Telegram"> <b>Dev / support</b></a> — questions, bugs, feature asks<br>
<a href="https://x.com/dogtoshi_x"><img src="https://cdn.simpleicons.org/x/1d9bf0" height="16" alt="X"> <b>X</b></a> — @dogtoshi_x</p>


### Starters

| Repo | What it is | Live demo |
|---|---|---|
| [**trenchytools-pumpfun-launcher**](https://github.com/Trenchy-Tools/trenchytools-pumpfun-launcher) | Wallets, Jito-bundled launches with up to 16 buyers, snipers, holder auto-buys, custom pairs, Mayhem mode, trading with timed sells, vanity mints. Solana. | [pumpfun.trenchy.tools](https://pumpfun.trenchy.tools) |
| [**trenchytools-pons-launcher**](https://github.com/Trenchy-Tools/trenchytools-pons-launcher) | Launch and trade on pons, curve and Uniswap v4. Robinhood Chain. | [pons.trenchy.tools](https://pons.trenchy.tools) |
| [**trenchytools-wallet-mover**](https://github.com/Trenchy-Tools/trenchytools-wallet-mover) | Create wallets, split, distribute and consolidate funds, direct or through an exchange, same chain or cross-chain. | [mover.trenchy.tools](https://mover.trenchy.tools) |
| [**trenchytools-elysium-launcher**](https://github.com/Trenchy-Tools/trenchytools-elysium-launcher) ⚗️ | Launch on Ascend, bundle, stagger and auto-sell straight against the chain, with pre-signed exits. Elysium (Hyperliquid L2), experimental / pre-mainnet. | [elysium.trenchy.tools](https://elysium.trenchy.tools) |
| [**trenchytools-api**](https://github.com/Trenchy-Tools/trenchytools-api) | The API itself — endpoints, auth, and the hosted AGENTS.md / OpenAPI. | [api.trenchy.tools](https://api.trenchy.tools) |
| [**trenchytools**](https://github.com/Trenchy-Tools/trenchytools) | Monorepo: API, docs site and the starters side by side. | [trenchy.tools](https://trenchy.tools) |

All starters share one wallet folder, so a wallet made in one is usable in the others. Try each one in the browser first (your wallets stay in your browser; download the backup before funding), or clone it, paste your key and `npm run dev`.

### 30-second start

```bash
curl "https://api.trenchy.tools/api/create-api-key"
```

```bash
curl -X POST "https://api.trenchy.tools/api/sol/trade-local?api-key=YOUR_KEY" \
  -H "content-type: application/json" \
  -d '{"publicKey":"YOUR_WALLET","action":"buy","mint":"COIN_MINT","amount":0.01,"denominatedInSol":"true","slippage":10}'
```

The answer is an unsigned transaction. Sign it with your wallet and send it with `POST /api/sol/send`.

### Build with AI

Paste into your coding agent:

> Read https://api.trenchy.tools/AGENTS.md and https://api.trenchy.tools/openapi.json, then build me a pump.fun bot that buys a coin when it launches and sells half at 2x. Save every wallet you create to a file before funding it.

### What the API covers

- **Solana**: pump.fun create, buy and sell, including custom pairs (coins priced in stocks, USDC or other coins) and Mayhem mode; PumpSwap after graduation; Jito bundles; vanity mints; creator fees; live websocket.
- **Robinhood Chain**: pons create, buy and sell on the curve and on Uniswap v4; live trades.
- **Elysium** *(experimental, pre-public-mainnet)*: Ascend launches on the Hyperliquid L2 (chain 99901, HYPE gas) — create, buy, sell, creator-fee claims, a per-wallet trading desk, and a live relay picker.
- **Wallets**: direct or exchange-routed transfers, same chain or cross-chain, with live venue health.
