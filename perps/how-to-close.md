# How to Close a Position

Closing a position locks in your P\&L and releases the margin back to your balance. You can close fully, partially, or automate closes with take-profit and stop-loss orders.

\[SCREENSHOT: Open positions panel with close button]

***

## Steps

### 1. Go to Perps — Positions Panel

On the Perps tab, open the **Positions** panel. All currently open positions are listed with live PnL, entry price, mark price, and liquidation price.

### 2. Find the Position to Close

Locate the position. Each row shows the asset, direction (long/short), size, entry price, mark price, unrealised PnL, and the funding accrued so far.

### 3. Click Close

Click **Close** on the position. You will be prompted to choose:

* **Full close** — closes the entire position
* **Partial close** — enter a percentage (e.g. 50%) or a specific size to close part of the position, leaving the remainder open

Partial closes are useful for taking profit on part of a winning trade while keeping exposure on the rest.

### 4. Choose Market or Limit Close

| Close type | How it works                                                       | Fee impact                                                                             |
| ---------- | ------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| Market     | Executes immediately at the current best price against the book.   | Pays the taker fee from your tier (see [Fees](fees.md)).                               |
| Limit      | Rests at your target exit price; fills when the market reaches it. | Pays the maker fee from your tier — and may not fill if the market doesn't move there. |

A market close guarantees execution. A limit close lets you target a specific exit price but isn't guaranteed.

### 5. Confirm

Review the closing price, estimated fee, and net PnL, then click **Confirm**. The position is removed from the Positions panel once filled.

***

## Understanding Your PnL

Realised PnL is calculated at close:

**Long:** `(Exit price − Entry price) × Size − Fees − Net funding paid`

**Short:** `(Entry price − Exit price) × Size − Fees − Net funding paid`

Fees include the trading fee on the closing order. Net funding is the running total of hourly payments paid (or received) during the life of the trade — see [Fees → Funding](fees.md#funding).

> **Success:** Closing a position locks in PnL. Unrealised PnL becomes realised and is credited to your margin balance immediately after the close fills.

***

## Automating Closes: Take-Profit and Stop-Loss

You can attach TP/SL orders when you open a position, or add them later from the Positions panel. Both trigger off the **mark price** rather than the last trade, which prevents accidental triggers from a single rogue print.

### Market vs. Limit TP/SL

| Variant      | Behaviour                                              | Trade-off                                                                |
| ------------ | ------------------------------------------------------ | ------------------------------------------------------------------------ |
| Market TP/SL | Triggers a market order with a fixed 10% slippage cap. | Highest fill probability; slippage can be meaningful in fast markets.    |
| Limit TP/SL  | Triggers a limit order at a price you specify.         | Tightest price control; may rest unfilled if price gaps past your limit. |

A common pattern: set a **stop loss** below your liquidation price (long) or above it (short) so you exit on your own terms before the protocol closes you out.

### Attaching TP/SL

* **From the position** — defaults to closing the full size. Simple and beginner-friendly. Cancellation is straightforward.
* **From a parent order** (OCO style) — child TP/SL orders activate only if the parent fully fills, or partially fills and is then cancelled because of insufficient margin. If you cancel the parent manually, the children are cancelled too.

### TP/SL on the Chart

You can drag your TP/SL levels directly on the TradingView chart on the Perps surface. Dragging a level into territory that would trigger immediately is blocked — to prevent fat-finger closes.

***

> **Info:** A stop-loss placed above your liquidation price is the single biggest risk-management win on perps. It guarantees you exit on your terms, with capital remaining, rather than leaving it to the protocol.

See [How to Open a Position](how-to-open.md) for where to set TP/SL during order entry.
