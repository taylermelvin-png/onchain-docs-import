# How to Close a Position

Closing a position locks in your PnL and releases the margin back to your balance. You can close fully, partially, or automate closes with take-profit and stop-loss orders.

<!-- 📸 SCREENSHOT NEEDED: Positions panel with Close and TP/SL controls -->

***

## Steps

### 1. Open the Positions Panel

All open positions are listed with live PnL, entry price, mark price, and liquidation price.

### 2. Click Close

Choose:

* **Full close** — closes the entire position
* **Partial close** — enter a percentage or a specific size, leaving the remainder open

Partial closes are useful for taking profit on part of a winner while keeping exposure on the rest.

### 3. Choose Market or Limit Close

| Close type | How it works | Fee impact |
| --- | --- | --- |
| **Market** | Executes immediately at the best price, within your slippage tolerance. | Pays the taker rate. |
| **Limit** | Rests at your target exit price; fills when the market reaches it. | Pays the maker rate — but may not fill. |

### 4. Confirm

Review the closing price, estimated fee, and net PnL, then confirm. Closing a position also cancels any TP/SL triggers attached to it.

***

## Understanding Your PnL

Realised PnL is calculated at close:

**Long:** `(Exit price − Entry price) × Size − Fees − Net funding paid`

**Short:** `(Entry price − Exit price) × Size − Fees − Net funding paid`

Net funding is the running total of hourly payments paid (or received) during the life of the trade — see [Fees → Funding](fees.md#funding).

{% hint style="success" %}
Closing a position locks in PnL. Unrealised PnL becomes realised and is credited to your balance as soon as the close fills.
{% endhint %}

***

## Automating Closes: Take-Profit and Stop-Loss

Attach TP/SL when you open a position, or add them later from the Positions panel. Both trigger off the **mark price** rather than the last trade — this prevents accidental triggers from a single rogue print.

* **Attached at entry** — the TP/SL arms only once your entry order actually fills.
* **On an open position** — by default the full position closes at market when the trigger fires, within your global slippage tolerance. Triggers auto-cancel once the position closes.

### Market vs. Limit TP/SL

| Variant | Behaviour | Trade-off |
| --- | --- | --- |
| **Market TP/SL** | Triggers a market order, capped by your slippage setting. | Highest fill probability; slippage can matter in fast markets. |
| **Limit TP/SL** | Triggers a limit order at a price you specify. | Tightest price control; may rest unfilled if price gaps past your limit. |

A common pattern: set a **stop loss** on your side of the liquidation price so you exit on your own terms, with capital remaining, rather than leaving it to the protocol.

***

{% hint style="info" %}
A stop-loss placed before your liquidation price is the single biggest risk-management win on perps. See [Leverage & Margin](leverage.md) for how liquidation works.
{% endhint %}
