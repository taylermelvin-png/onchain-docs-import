# Degen Overview

Degen is the dedicated onchain.cc product for trading **pre-graduated pump.fun tokens** — Solana memecoins that are still on their bonding curve and not yet listed on a regular DEX. It's a separate surface from [Swap](../swap/terminal-overview.md) (which is for established, post-graduation tokens) and from [Discover](../discover/degen-feed.md) (which is the feed that surfaces what's moving).

\[SCREENSHOT: Degen tab on the onchain.cc terminal showing a pre-graduated token's bonding-curve panel]

> **Info:** **Currently Solana-only.** Degen exists because pump.fun is a Solana product. The pre-graduate market only exists there.

***

## What "Pre-Graduated" Means

On pump.fun, every token launches on a **bonding curve** rather than on a traditional liquidity pool:

* As people buy, the price moves up the curve.
* As people sell, it moves down.
* The token does **not** trade on Raydium, Orca, or any other DEX during this phase.
* Once the token's market cap reaches roughly **$69k** (the graduation threshold), pump.fun automatically migrates the liquidity to Raydium and the token "graduates" — at which point it becomes a normal post-grad token tradable through any DEX (and on onchain.cc through [Swap](../swap/terminal-overview.md)).

A **pre-graduated** token is one that is still on the bonding curve. To buy or sell it, you must trade against the curve directly — which is what Degen is for.

***

## Why Degen Is Its Own Product

Pre-graduated tokens behave differently from post-graduated ones. Standard DEX routing (the Carbium aggregator that powers [Swap](../swap/terminal-overview.md)) doesn't apply, because there's no liquidity pool to route through yet. The price is set entirely by the bonding curve, slippage works differently, and execution paths are different. Degen handles that flow specifically:

| | Swap | Degen | Discover |
|---|---|---|---|
| What it's for | Trading post-graduation tokens across 17+ chains | Trading pre-graduation pump.fun tokens (Solana-only) | Finding tokens to trade (signals, feeds, first-callers) |
| Pricing model | DEX liquidity pools (AMMs) routed by Carbium | Pump.fun bonding curve | N/A — informational |
| Chain coverage | 17+ chains | Solana only | Solana only |

***

## Where Degen Fits in Your Flow

A typical Solana memecoin lifecycle on onchain.cc:

1. **Discover** it — the [Degen Feed (Trenches)](../discover/degen-feed.md) surfaces newly launched and trending tokens. [Derek Bot](../discover/derek-bot.md) flags first-caller activity.
2. **Trade it pre-graduation** — if you want to buy before it hits Raydium, use **Degen** (this section).
3. **Trade it post-graduation** — once the token graduates, it trades like any other Solana token via [Swap](../swap/terminal-overview.md).

***

## Fees on Degen

Degen uses the same Colosseum rank-based fee schedule as Swap:

* **Recruit:** 0.15%
* **Warrior:** 0.14%
* **Gladiator:** 0.13%
* **Champion:** 0.12%
* **Warlord:** 0.11%
* **Immortal:** 0.10%

There is no separate Degen-specific fee. Your rank applies platform-wide. See [Rank System](../colosseum/ranks.md) for how the schedule works.

> **Warning:** Pre-graduated tokens are highly speculative. Most pump.fun tokens never graduate — many lose most of their value within hours of launch. Trade only with capital you are willing to lose entirely.

***

## Read Next

* [Pump.fun Bonding Curves](bonding-curves.md) — how pricing actually works on pre-graduates
* [How to Buy a Pre-Graduated Token](how-to-buy.md) — the step-by-step trade flow
