# Spot Overview

Spot is onchain.cc's order-book spot trading terminal, powered by **Hyperliquid**. Trade a deep universe of USDC pairs — majors, memes, AI, DeFi, and more — with a real order book, professional charts, and market, limit, and TWAP orders.

<!-- 📸 SCREENSHOT NEEDED: Spot terminal — markets list, chart, order book, order entry -->

Spot lives under the **Perps/Spot** tab alongside perpetual futures. The two share one interface family and **one USDC balance** — fund it once and trade both.

***

## What makes Spot different from Swap

onchain.cc has two ways to buy a token, built for different jobs:

|  | Spot | [Swap](../swap/overview.md) |
| --- | --- | --- |
| Execution | Central limit order book (Hyperliquid) | DEX aggregation across on-chain liquidity |
| Order types | Market, limit (GTC/IOC/post-only), TWAP | Instant swap |
| Pairs | Curated USDC pairs | Any routable token on 12 chains |
| Balance | Shared Perps/Spot USDC balance | Your wallet |
| Best for | Actively trading liquid markets with price control | Converting between any two tokens, cross-chain |

If you want to work an order — rest a bid, scale out with a TWAP, pay maker fees — use Spot. If you want token A to become token B right now, use Swap.

***

## The markets list

The Spot markets screen shows the tradeable universe with live prices, 24h change, volume, and category filters (Trending, Memes, AI, L1, L2, DeFi, Gaming, and more), plus your Favorites and a Recently Listed highlight.

Listings are curated for quality: USDC-quoted pairs with real trading volume. Many symbols are Hyperliquid's bridged versions of majors (BTC, ETH, SOL and others) shown under their canonical names.

***

## Funding Spot

Spot trades from the shared **Perps/Spot USDC balance**:

1. Click **Transfer** on the Spot account panel (or in the header balance menu).
2. Fund from any supported chain — the terminal routes it automatically. **Instant** mode lands in seconds; **Standard** is cheaper and takes a few minutes.
3. Minimum deposit $10. Withdrawals (minimum $2, $1 Hyperliquid fee) arrive as USDC on Arbitrum.

Because the balance is shared, margin used by open perps positions reduces what's available to spend on Spot, and vice versa. The account panel shows total and available at all times.

See [Funding Your Account](../getting-started/funding.md) for the full flow.

***

## What you pay

Each order pays Hyperliquid's trading fee for your account plus a small Onchain service fee, combined into the single rate shown in the order panel before you confirm. Maker orders pay less than taker orders. See [Spot Fees](fees.md).

***

{% hint style="info" %}
Spot involves real order-book execution — partial fills, resting orders, and maker/taker mechanics. If you're new to order books, start with small sizes and market orders, and read [Order Types](order-types.md) before using limit or TWAP orders.
{% endhint %}
