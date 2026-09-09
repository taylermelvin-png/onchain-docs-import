# Key Concepts & Glossary

onchain.cc has its own vocabulary — some of it standard crypto terminology, some of it specific to the terminal. This page covers both.

***

## Products

| Term | Definition |
| --- | --- |
| **Spot** | The order-book spot trading product, powered by Hyperliquid. A deep universe of USDC pairs with market, limit, and TWAP orders. Shares one USDC balance with Perps. |
| **Perps** | Perpetual futures, powered by Hyperliquid. Go long or short with leverage; no expiry. Uses the shared Perps/Spot balance. |
| **Trenches** | The token-launch product. A live scanner and trading surface for new Solana tokens across the PumpFun, LaunchLab, and Meteora launchpads — from first block to graduation and beyond. |
| **Predictions** | Prediction markets powered by Polymarket. Buy Yes or No shares on real-world events; winning shares settle at $1. |
| **Swap** | Cross-chain token swaps across 12 supported chains, with automatic best-price routing. |
| **Portfolio** | Your consolidated view: wallet holdings, Spot, Perps, and Predictions balances, positions, and PnL. |
| **Dashboard** | Your customizable home screen — build it from 30+ widgets, save up to three layouts, share and import boards. |
| **Colosseum** | The competitive layer. Trading earns points; points build rank and standing on prize-pool leaderboards. |

***

## Trading terms

| Term | Definition |
| --- | --- |
| **CA** | Contract Address — the unique on-chain identifier for a token. Paste a CA into the search bar to pull up any token instantly. |
| **Self-custody** | You hold your own private keys. No exchange or third party can access, freeze, or move your funds. onchain.cc is fully self-custody. |
| **Privy** | The authentication and wallet infrastructure behind sign-in. Supports Google, email, and wallet login, and manages embedded wallets non-custodially. |
| **Embedded wallet** | The self-custody Solana and EVM wallets attached to your account when you sign in with Google or email. View them — and export their keys — on the Wallets page. |
| **Carbium** | The Solana routing engine behind Swap. It splits and routes orders across DEX liquidity to get the best available price. |
| **Slippage** | The difference between the price you expect and the price you get at execution. Your slippage tolerance is the maximum move you'll accept before the trade reverts. |
| **MEV protection** | Routing safeguards against sandwich attacks on Solana swaps. On by default. |
| **Gas fee** | The network's fee for processing a transaction, paid in the chain's native token. Sponsored on most supported EVM chains. |
| **Maker / Taker** | On order-book products: a maker order rests on the book and adds liquidity; a taker order fills immediately against it. Takers pay slightly higher fees. |
| **TWAP** | Time-Weighted Average Price — an order type that splits a large order into small slices over a chosen duration to reduce market impact. |
| **Funding rate** | On perps: the hourly payment exchanged between longs and shorts that keeps the perp price anchored to the underlying. |
| **Liquidation** | The automatic close of a leveraged position when its margin can no longer support it. |

***

## Trenches terms

| Term | Definition |
| --- | --- |
| **Launchpad** | The platform a token launched on. Trenches covers PumpFun, LaunchLab (Raydium), and Meteora. |
| **Bonding curve** | The pricing contract new launchpad tokens trade on before graduation. Buys push the price up the curve; sells push it down. |
| **Graduation** | The point where a token completes its bonding curve and its liquidity migrates to a full DEX (PumpFun tokens graduate to PumpSwap). After graduation it trades like any other token. |
| **Snipe** | A fast pre-configured buy on a launchpad token, using your saved amount, slippage, and priority settings. |
| **USD1** | A USD stablecoin supported as a Trenches funding currency alongside SOL and USDC. |
| **Tracker** | The wallet-tracking tab in Trenches — follow up to 50 wallets, get live buy/sell/launch alerts, and see their trades on your charts. |
| **Dev / Sniper / Bundler / Insider** | Holder-analysis flags on every token showing what share of supply is held by the token deployer, early snipers, bundled buyers, and insiders. |

***

## Colosseum terms

| Term | Definition |
| --- | --- |
| **Points** | Earned automatically from trading volume across all products, plus quests and other actions. Lifetime points set your rank. |
| **Rank** | Your standing: Recruit → Warrior → Gladiator → Champion → Warlord → Immortal, each with subtiers 1–4. Rank sets your swap fee and your points multiplier. |
| **Season** | A long-running campaign with a prize pool and its own boosts. |
| **Session** | A shorter competition window inside a season — typically weekly — with its own leaderboard and prizes. |
| **Quest** | A challenge that pays bonus points, boosts, or loot boxes — daily, weekly, or one-time. |
| **Loot Box** | A reward drop earned from quests and milestones. Four rarities: Common, Rare, Epic, Legendary. Contains points or USDC. |
| **Faction** | A team of up to 50 traders competing together. Top factions by weekly volume earn a points multiplier for every member. |
| **Vault** | A community campaign: the whole platform trades toward a shared volume target to unlock rewards. |
| **Bonus Window** | A time-limited event that boosts point earnings for eligible trades. |
| **Social Scoring** | Points progress for quality posts about onchain.cc on X. |

***

{% hint style="info" %}
New terms get added as the platform evolves. If you see something in the UI that is not covered here, check the product-specific docs or ask in [Discord](../resources/support.md).
{% endhint %}

***

Ready to trade? Start with the [Quick Start Guide](quick-start.md).
