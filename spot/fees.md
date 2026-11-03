# Spot Fees

Spot fees are simple: **no onchain.cc fee on buys, sells pay the onchain.cc fee — and cashback applies.** Hyperliquid's own spot fee applies on both sides, on top.

* **Buying:** no onchain.cc fee (Hyperliquid's own spot fee still applies).
* **Selling:** **0.25% maker / 0.35% taker** onchain.cc fee, on top of Hyperliquid's spot fee, shown combined in the order panel before you confirm. A resting limit order (or post-only ALO order) that fills pays the maker rate; market orders and limit orders that fill immediately pay taker.
* **Cashback:** 25–50% of the onchain.cc fee comes back by [Colosseum rank](../colosseum/cashback.md), claimable in USDC. Hyperliquid's fee is not included.

The order panel's combined rate is always the source of truth for your account.

***

## How to pay less

* **Make, don't take.** A resting limit order (or a post-only ALO order) that fills pays the cheaper maker rate.
* **Rank up.** A higher Colosseum rank returns more of the onchain.cc fee as [cashback](../colosseum/cashback.md).

***

## What Spot fees are *not*

* **Not the swap fee.** [Swap](../swap/fees.md) and [Trenches](../trenches/trading.md) have their own schedule — Spot runs on Hyperliquid's order book with its own fee structure.
* **No gas.** Spot orders trade against your Perps/Spot balance, so there's no per-order network fee.
* **No deposit fee.** Funding Perps/Spot is free apart from routing costs shown in the transfer dialog; withdrawals carry Hyperliquid's flat $1 fee.

***

{% hint style="info" %}
Fees are deducted from the trade at execution and itemized in your fills history; the cashback on them accrues live in the [Cashback panel](../colosseum/cashback.md).
{% endhint %}
