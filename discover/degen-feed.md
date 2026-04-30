# Degen Feed

> **Info:** **Currently Solana-only.** The Degen Feed (also called **Trenches**) is the one part of onchain.cc that's Solana-only — the rest of the platform is cross-chain across 17+ networks. Cross-chain coverage for the discovery feed is on the roadmap.

The Degen Feed is onchain.cc's real-time token discovery interface. It surfaces new and trending Solana tokens using a combination of onchain signals (volume, liquidity, new listings) and social signals (KOL mentions, community activity). Instead of manually scanning DEX screeners, you get a live, ranked view of what's moving — right inside the platform where you can act on it immediately.

***

## What the Degen Feed Shows

The feed is a continuous stream of token cards. Each card surfaces the data points that matter most for evaluating a move quickly.

### Token Card Breakdown

| Data Point                | What It Means                                                                                            |
| ------------------------- | -------------------------------------------------------------------------------------------------------- |
| **Token name + ticker**   | The token's name and trading symbol                                                                      |
| **Price**                 | Current market price in USD                                                                              |
| **24h Volume**            | Total trading volume in the last 24 hours — a fast proxy for interest                                    |
| **Liquidity**             | Total value locked in the token's trading pair — low liquidity means higher slippage and risk            |
| **Social Activity Score** | A composite score based on KOL mentions, X/Twitter community volume, and Derek Bot first-caller activity |
| **Age**                   | Time since the token was first listed or liquidity was added                                             |

The cards are sorted by signal strength by default. Tokens with high volume relative to their liquidity, recent social spikes, or first-caller activity rank higher.

***

## Navigating the Feed

\[SCREENSHOT: Degen Feed with token cards annotated]

### Filter Options

Use the filter bar at the top of the feed to narrow the view:

* **New Listings** — tokens that launched or added liquidity recently
* **Trending** — tokens with above-average volume relative to their liquidity baseline
* **Gainers** — tokens with the strongest positive price movement in the last 24 hours
* **Your Watchlist** — tokens you have manually saved

Filters can be combined. For example, filtering by New Listings + Trending surfaces freshly launched tokens that are already seeing unusual activity.

***

## Acting on a Token

1. Scroll the feed and identify a token worth investigating.
2. Click anywhere on the token card to open the full token detail view.
3. Review the expanded signal data — price chart, liquidity depth, holder concentration, and social signals.
4. If you want to trade, click **Trade** to open the token directly in the Trading Terminal with the pair pre-loaded.

The Degen Feed does not require you to copy contract addresses or leave the platform to look up a token. Discovery and execution are in the same flow.

***

> **Info:** The Degen Feed surfaces signals — it does not make trading decisions for you. Before entering any position, always check liquidity depth, verify the contract address, and assess holder concentration. High social activity is not a substitute for onchain due diligence.
