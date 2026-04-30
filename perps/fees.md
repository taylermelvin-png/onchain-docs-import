# Fees & Funding

There are two distinct cost types on perps: **trading fees** (charged per trade) and **funding** (paid hourly between longs and shorts while a position is open). Understanding both is essential before sizing a position.

***

## Trading Fees

Perps trading fees are tiered by your **rolling 14-day volume**, recalculated daily in UTC. Higher volume = lower fees.

### Base Tier (Tier 0)

| Side  | Rate   |
| ----- | ------ |
| Maker | 0.015% |
| Taker | 0.045% |

### Volume Tiers

| Tier | 14-day perps volume | Maker  | Taker  |
| ---- | ------------------- | ------ | ------ |
| 0    | < $5M               | 0.015% | 0.045% |
| 1    | > $5M               | 0.012% | 0.040% |
| 2    | > $25M              | 0.008% | 0.035% |
| 3    | > $100M             | 0.004% | 0.030% |
| 4    | > $500M             | 0.002% | 0.028% |
| 5    | > $2B               | 0%     | 0.026% |
| 6    | > $7B               | 0%     | 0.024% |

> **Info:** Spot volume on onchain.cc counts double toward your perps fee tier. Effective volume = (perps 14-day) + 2 × (spot 14-day).

### Maker vs. Taker

* **Maker** — your order added liquidity to the book. Limit orders that don't match immediately make liquidity available for others; when they fill, you pay the maker fee (or earn a rebate at the highest tiers).
* **Taker** — your order removed liquidity. A market order, or a limit order that matches immediately, takes existing liquidity. You pay the taker fee.

If you want to enter at the current price right now, you pay taker. If you're patient and rest a limit order, you pay maker when (and if) it fills.

### No Fee on Liquidation

The protocol charges no clearance fee on liquidations themselves. The cost of liquidation is the loss of margin, not an additional fee.

***

## Funding

Funding is **not** a fee paid to the exchange — it is a peer-to-peer payment exchanged between longs and shorts to keep the perp price anchored to the underlying spot price.

### Direction of Payment

| Perp price vs. spot | Funding sign | Direction        |
| ------------------- | ------------ | ---------------- |
| Perp above spot     | Positive     | Longs pay shorts |
| Perp below spot     | Negative     | Shorts pay longs |

This incentivises traders to take the side that closes the gap, which keeps the perp price near spot.

### Effect on Your PnL

| You are | Funding  | Outcome                 |
| ------- | -------- | ----------------------- |
| Long    | Positive | You pay — costs you     |
| Long    | Negative | You receive — earns you |
| Short   | Positive | You receive — earns you |
| Short   | Negative | You pay — costs you     |

### Settlement Cadence

Funding is paid **every hour**. Hyperliquid quotes funding as an 8-hour rate but settles ⅛ of it each hour, so you don't have to time the 8-hour boundary to manage it. If you close before the next hourly settlement, you don't pay or receive funding for that period.

### How the Rate Is Calculated

The hourly funding rate has two components:

* **Interest rate component** — a fixed 0.01% every 8 hours (≈ 0.00125% per hour, ≈ 11.6% APR), representing the cost difference between borrowing USD and spot crypto.
* **Premium component** — sampled every 5 seconds and averaged over the hour, based on the gap between the perp's impact prices and the spot oracle price.

The hourly rate is capped at **4%**. Funding payments are calculated against the **spot oracle price** (not mark), to convert position size into notional value.

\[SCREENSHOT: Funding rate display on the perps panel]

***

> **Info:** Funding can compound meaningfully over a multi-day hold. A persistent 0.01% per hour is \~7.4% per month. Always check the current rate before opening a long-duration position — and remember the sign can flip.

***

## How These Costs Stack Up

A simple example, ignoring slippage:

* You open a $10,000 BTC long with a market order at Tier 0 → **opening fee: $4.50** (0.045% taker).
* You hold for 24 hours at +0.01% hourly funding → **funding paid: \~$24** (long pays positive).
* You close with a limit order at Tier 0 → **closing fee: $1.50** (0.015% maker).

Total cost of the round trip: \~$30 plus or minus PnL.

The fee bill is far smaller than funding for any hold longer than a few hours — funding is the dominant ongoing cost on perps, not the trading fee.
