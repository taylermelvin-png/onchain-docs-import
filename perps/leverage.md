# Leverage & Margin

Leverage is the defining feature — and the defining risk — of perps trading. This page explains how it works mechanically, how margin and liquidation are calculated, and how to keep yourself out of trouble.

\[SCREENSHOT: Leverage slider with liquidation price updating in real time]

***

## What Leverage Does

Leverage multiplies your market exposure relative to the collateral you post.

**Example:** At 10x, $100 of margin controls a $1,000 position.

* The asset rises 10% → your $1,000 position gains $100 — a 100% return on margin.
* The asset falls 10% → your position loses $100 — your entire margin is gone.

Upside and downside are amplified equally.

### Leverage Limits

The maximum leverage is set per asset. Majors like BTC and ETH support up to 40x; mid-cap assets typically 10–20x; smaller-cap assets less. The slider in the order panel shows the maximum for the asset you've selected.

***

## Margin

Margin is the USDC collateral that backs your leveraged position.

### Initial Margin

The collateral required to open a position:

`Initial margin = position size × mark price ÷ leverage`

Higher leverage reduces the initial margin needed but increases liquidation risk.

### Maintenance Margin

The minimum margin required to keep the position open. It's set to **half of the initial margin at the asset's maximum leverage**, so it varies by asset class — roughly:

| Asset's max leverage | Maintenance margin |
| -------------------- | ------------------ |
| 40x (majors)         | \~1.25%            |
| 20x                  | \~2.5%             |
| 10x                  | \~5%               |
| 3x                   | \~16.7%            |

If your account equity falls below the maintenance margin requirement, [liquidation](leverage.md#liquidation) is triggered.

### Margin Modes: Cross vs. Isolated

| Mode                | Collateral pool                                             | Effect of liquidation                                           | Best for                                  |
| ------------------- | ----------------------------------------------------------- | --------------------------------------------------------------- | ----------------------------------------- |
| **Cross** (default) | Shared across all your cross positions, plus unrealised PnL | A liquidation can affect the entire cross account               | Capital efficiency; coordinated positions |
| **Isolated**        | Locked to one position only                                 | A liquidation cannot touch your other positions or free balance | Ringfenced risk on a specific trade       |

You select the mode when opening the position. Cross uses your full free balance plus unrealised PnL on winners as headroom. Isolated walls off a fixed amount.

### Adding or Removing Margin

* **Cross positions** — initial margin is locked while the position is open and cannot be selectively withdrawn.
* **Isolated positions** — you can add or remove margin from the Positions panel after opening, which moves the liquidation price further from (or closer to) the current price.

***

## Liquidation

Every leveraged position has a liquidation price. If the **mark price** reaches it, the position is closed automatically and the margin assigned to it is lost.

### Why It Exists

Leverage means you can lose more than your collateral. Liquidation is the mechanism that ensures you cannot — the protocol closes the position before losses exceed the margin posted.

### Mark Price, Not Last Trade

Liquidations trigger on the **mark price**, which combines external CEX prices with the on-platform book state. This protects against being liquidated by a single thin print or a brief wick. In high volatility, the mark price can still differ noticeably from the last trade.

### How the Liquidation Process Works

1. **Book-based attempt** — when account equity falls below maintenance margin, the protocol sends a market order for the position to the order book.
2. **Partial liquidation for large positions** — for positions larger than $100k notional, the protocol initially sends only 20% as a market order, with a 30-second cooldown before another partial fires. This avoids smashing the book on a single print.
3. **Backstop liquidation** — if account equity falls below ⅔ of maintenance margin and the book hasn't absorbed the position, the liquidator vault takes over the remaining position.

### What Happens to Leftover Collateral

* **Book-based liquidation** — any remaining collateral after the position closes stays with you.
* **Backstop liquidation** — the maintenance margin is retained by the liquidator vault to keep the backstop economically viable on average.

There is **no clearance fee** charged on liquidation itself.

### Liquidation Price (Long, simplified)

Liquidation price moves closer to entry as leverage increases:

| Entry | Leverage | Approx. liquidation price |
| ----- | -------- | ------------------------- |
| $100  | 2x       | \~$51                     |
| $100  | 5x       | \~$80                     |
| $100  | 10x      | \~$91                     |
| $100  | 20x      | \~$95                     |
| $100  | 40x      | \~$98                     |

Exact liquidation price depends on the asset's maintenance margin rate and current funding accrued. The live value is always shown on the position in the Positions panel.

***

## Reducing Liquidation Risk

**1. Use lower leverage.** The single most effective control. 2–5x leaves real room to breathe.

**2. Add margin to an isolated position.** Lowers effective leverage and pushes the liquidation price further from market.

**3. Set a stop-loss above your liquidation price.** Triggers off the mark price, exits on your terms, and preserves capital you can redeploy. See [How to Close a Position](how-to-close.md).

**4. Watch funding.** Funding is paid hourly (see [Fees → Funding](fees.md#funding)). Sustained adverse funding eats into your margin and brings the liquidation price closer over time.

***

> **Info:** The liquidation price on your position is live and reacts to mark price, accrued funding, and any margin you add or remove. Check it before walking away from a position, especially in volatile markets.
