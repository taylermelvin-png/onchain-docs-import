# Fees & Funding

There are two distinct cost types on perps: **trading fees** (charged per order) and **funding** (exchanged hourly between longs and shorts while a position is open). Understanding both is essential before sizing a position.

***

## Trading Fees

Every order pays a combined rate made of two parts:

1. **Hyperliquid's trading fee** — the exchange's maker/taker rate for your account. Hyperliquid tiers these rates by rolling trading volume, so active accounts pay less, and maker orders always pay less than taker orders.
2. **Onchain service fee** — a small markup added by onchain.cc.

The order panel shows the **combined taker and maker rate you'll actually pay** on every order before you confirm — that display is the source of truth for your account.

### Maker vs. Taker

* **Maker** — your order added liquidity to the book. Limit orders that rest and later fill pay the maker rate.
* **Taker** — your order removed liquidity. Market orders, and limit orders that match immediately, pay the taker rate.

If you want to enter right now, you pay taker. If you're patient and rest a limit order, you pay maker when (and if) it fills.

### No Fee on Liquidation

There is no separate clearance fee on liquidations. The cost of liquidation is the loss of the margin backing the position, not an additional charge.

***

## Funding

Funding is **not** a fee paid to the exchange — it is a peer-to-peer payment exchanged between longs and shorts to keep the perp price anchored to the underlying spot price.

### Direction of Payment

| Perp price vs. spot | Funding sign | Direction        |
| ------------------- | ------------ | ---------------- |
| Perp above spot     | Positive     | Longs pay shorts |
| Perp below spot     | Negative     | Shorts pay longs |

This incentivises traders to take the side that closes the gap.

### Effect on Your PnL

| You are | Funding  | Outcome                 |
| ------- | -------- | ----------------------- |
| Long    | Positive | You pay                 |
| Long    | Negative | You receive             |
| Short   | Positive | You receive             |
| Short   | Negative | You pay                 |

### Settlement Cadence

Funding settles **every hour**, on the hour — the terminal shows the current rate and a countdown to the next settlement on every market. If you close before the next settlement, you don't pay or receive funding for that period.

The rate itself is set by Hyperliquid from the gap between the perp price and the spot oracle price; the annualized equivalent is shown in the rate tooltip.

***

## How These Costs Stack Up

For a multi-day hold, funding — not the trading fee — is usually the dominant cost. A persistent 0.01% per hour compounds to roughly 7% per month. Always check the current funding rate (and its sign) before opening a long-duration position, and remember it can flip.

Your full funding history is available in the Funding tab of the perps portfolio, and funding paid or received is included in each position's PnL.
