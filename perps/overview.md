# Perps Overview

Perpetual futures (perps) let you trade any supported asset long or short with leverage — no expiry date, no rolling contracts. You hold the position until you close it, or until a liquidation event forces it shut.

\[SCREENSHOT: Perps tab on the onchain.cc terminal]

***

## Where Perps Live

Perps are a separate surface from the spot terminal and Degen Feed. Access them via the **Perps** tab at the top of the onchain.cc interface. Spot and perps positions are tracked independently and use **separate balances** — to start trading perps you'll fund a USDC perps balance via the **Fund Perps** button. See [How to Open a Position](how-to-open.md) for the full flow.

***

## Spot vs. Perps

|              | Spot                   | Perps                                      |
| ------------ | ---------------------- | ------------------------------------------ |
| What you own | The token itself       | A leveraged contract on the price          |
| Expiry       | None                   | None (perpetual)                           |
| Leverage     | No                     | Yes — up to 40x on majors, varies by asset |
| Direction    | Long only (you own it) | Long or short                              |
| Costs        | 0.15% per trade        | Tiered maker/taker + hourly funding        |
| Settlement   | Instant on-chain       | Continuous, with funding payments          |

Spot trading means you own the underlying asset. If you buy SOL, you hold SOL. With perps, you never hold the asset — you hold a contract that tracks the price. You can go long (profit if price rises) or short (profit if price falls).

***

## Powered by Hyperliquid

The onchain.cc perps product is built on Hyperliquid's execution layer. You get the onchain.cc interface and experience — Hyperliquid handles the order matching, mark pricing, funding, and settlement under the hood. You do not need a separate Hyperliquid account.

***

## Key Concepts

Before opening a position, understand these four mechanics. Each has its own page with full detail.

| Concept                                | What it means                                                                                |
| -------------------------------------- | -------------------------------------------------------------------------------------------- |
| [Leverage & Margin](leverage.md)       | Leverage multiplies exposure; margin is the collateral that backs the trade.                 |
| [Funding](fees.md#funding)             | Hourly payments between longs and shorts that keep the perp price anchored to spot.          |
| [Liquidation](leverage.md#liquidation) | Automatic close when your margin falls below the maintenance threshold.                      |
| [Fees](fees.md)                        | Tiered maker/taker rates based on rolling 14-day volume, with no fee charged on liquidation. |

***

> **Info:** Perps involve leverage and carry significantly higher risk than spot trading. Only trade with capital you can afford to lose. New to perps? Start at 1–2x leverage while you learn the mechanics.
