# Spot Fees

Spot fees have two parts, combined into the **single rate shown in the order panel** before you confirm any trade:

1. **Hyperliquid's trading fee** — the exchange's own maker/taker rate for your account. Hyperliquid tiers fees by trading volume, so active accounts pay less; maker orders always pay less than taker orders.
2. **Onchain service fee** — a small markup added by onchain.cc.

The order panel always shows the combined maker and taker rate you'll actually pay — check it there rather than relying on any table, since Hyperliquid's component varies with your account's volume tier and discounts.

***

## How to pay less

* **Make, don't take.** A resting limit order (or a post-only ALO order) that fills pays the maker rate — meaningfully cheaper than a market order's taker rate.
* **Trade more.** Hyperliquid's fee component falls as your rolling trading volume rises.

***

## What Spot fees are *not*

* **Not the 0.15% swap fee.** The rank-based 0.15% → 0.10% schedule applies to [Swap](../swap/fees.md) and [Trenches](../trenches/trading.md) — on-chain token trades. Spot runs on Hyperliquid's order book with its own fee structure.
* **No gas.** Spot orders trade against your Perps/Spot balance, so there's no per-order network fee.
* **No deposit fee.** Funding Perps/Spot is free apart from routing costs shown in the transfer dialog; withdrawals carry Hyperliquid's flat $1 fee.

***

{% hint style="info" %}
Fees are deducted from the trade at execution and itemized in your fills history.
{% endhint %}
