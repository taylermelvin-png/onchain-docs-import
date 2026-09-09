# Leverage & Margin

Leverage is the defining feature — and the defining risk — of perps trading. This page explains how it works mechanically, how margin and liquidation behave, and how to keep yourself out of trouble.

***

## What Leverage Does

Leverage multiplies your market exposure relative to the collateral you post.

**Example:** At 10x, $100 of margin controls a $1,000 position.

* The asset rises 10% → your position gains $100 — a 100% return on margin.
* The asset falls 10% → your position loses $100 — your entire margin is gone.

Upside and downside are amplified equally.

### Leverage Limits

Maximum leverage is set **per market** by Hyperliquid — up to 40x on the deepest majors like BTC and ETH, lower on mid-caps, and as low as 3x on newer or thinner markets. The order panel shows the current maximum for the selected market and caps your setting to it.

***

## Margin

Margin is the USDC collateral that backs your leveraged position.

### Initial Margin

The collateral required to open a position:

`Initial margin = position size ÷ leverage`

Higher leverage reduces the initial margin needed but increases liquidation risk.

### Maintenance Margin

The minimum margin required to keep the position open — set by Hyperliquid per market, at half the margin required at that market's maximum leverage. For example, on a 20x-max market the minimum initial margin is 5%, so maintenance margin is 2.5%. If your equity falls below it, [liquidation](#liquidation) is triggered.

### Margin Modes: Isolated vs. Cross

| Mode | Collateral pool | Effect of liquidation | Best for |
| --- | --- | --- | --- |
| **Isolated** (default) | Locked to one position only | Cannot touch your other positions or free balance | Ringfenced risk on a specific trade |
| **Cross** | Shared across all your cross positions, plus unrealised PnL | A liquidation can affect the entire cross account | Capital efficiency; coordinated positions |

You select the mode before opening; changing it requires closing the position in that market first.

### Adding or Removing Margin

* **Isolated positions** — add or remove margin from the Positions panel after opening, which moves the liquidation price further from (or closer to) the current price. Adding is capped by your available balance.
* **Cross positions** — margin is managed at the account level rather than per position.

***

## Liquidation

Every leveraged position has a liquidation price, shown before you confirm the order and live on the position afterwards. If the **mark price** reaches it, the position is closed automatically and the margin backing it is lost.

### Mark Price, Not Last Trade

Liquidations trigger on the **mark price**, which Hyperliquid derives from external exchange prices and the order book. This protects against being liquidated by a single thin print or a brief wick — though in high volatility the mark can still differ noticeably from the last trade.

### How Liquidation Runs

Liquidation is handled by Hyperliquid's protocol: the position is sent to the order book to close, with large positions unwound in stages, and a backstop liquidator takes over if the book can't absorb it. There is no separate clearance fee — the cost of liquidation is the loss of the margin backing the position.

### Leverage vs. Liquidation Distance (long, simplified)

| Entry | Leverage | Approx. liquidation price |
| ----- | -------- | ------------------------- |
| $100  | 2x       | ~$51                      |
| $100  | 5x       | ~$81                      |
| $100  | 10x      | ~$91                      |
| $100  | 20x      | ~$96                      |
| $100  | 40x      | ~$98                      |

Exact liquidation price depends on the market's maintenance margin and accrued funding — the live value is always shown on your position.

***

## Reducing Liquidation Risk

1. **Use lower leverage.** The single most effective control. 2–5x leaves real room to breathe.
2. **Add margin to an isolated position.** Lowers effective leverage and pushes the liquidation price away from market.
3. **Set a stop-loss before your liquidation price.** Triggers off the mark price, exits on your terms, and preserves capital. See [How to Close a Position](how-to-close.md).
4. **Watch funding.** Funding settles hourly (see [Fees → Funding](fees.md#funding)). Sustained adverse funding eats into margin and brings the liquidation price closer over time.

***

{% hint style="info" %}
Your liquidation price is live — it reacts to mark price, accrued funding, and margin changes. Check it before walking away from a position, especially in volatile markets.
{% endhint %}
