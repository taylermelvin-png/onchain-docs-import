# How to Open a Position

Opening a perps position takes under a minute once your wallet is connected and your perps balance is funded. Work through each step in order — the order summary in step 9 shows you the full picture before any funds move.

\[SCREENSHOT: Perps order entry panel with long selected, leverage set, size entered]

***

## Steps

### 1. Go to the Perps Tab

Open the onchain.cc terminal and click the **Perps** tab. This loads the perps trading surface, separate from the spot terminal and Degen Feed.

### 2. Fund Your Perps Balance

Perps run on a **separate balance** from your spot wallet. Click **Fund Perps** at the top of the perps panel and transfer USDC from your wallet into your perps balance. Until you do this, you can browse markets but cannot open a position.

> **Info:** Your perps balance is the collateral pool used for opening, maintaining, and settling perp positions. You can withdraw unused perps balance back to your wallet at any time using the same panel.

\[SCREENSHOT: Fund Perps modal with USDC amount field]

### 3. Select the Asset

Use the asset selector to choose what you want to trade. Each asset has its own maximum leverage and contract specification — majors like BTC and ETH support the highest leverage, smaller-cap assets less.

### 4. Choose Your Direction

Select **Long** or **Short**:

* **Long** — you profit if the asset price rises
* **Short** — you profit if the asset price falls

### 5. Choose a Margin Mode

| Mode     | Behaviour                                                                                                                          | When to use                                                                                       |
| -------- | ---------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Cross    | Shares collateral across all your cross positions. Unrealised PnL on winners offsets margin demand on losers.                      | The default. Best when you're managing multiple correlated positions and want capital efficiency. |
| Isolated | Locks a specific amount of collateral to this position only. A liquidation here cannot touch your other positions or free balance. | When you want a single position's risk fully ringfenced.                                          |

> **Info:** Cross is the default. Pick isolated when you want a hard wall between this trade and the rest of your account.

### 6. Set Your Leverage

Use the leverage slider or type a value manually. The maximum is asset-specific — typically up to 40x on majors and lower for smaller-cap assets. The terminal shows the asset's maximum on the slider.

> **Warning:** Higher leverage means your liquidation price is closer to your entry. A 10x position can be liquidated by roughly a 10% adverse move; a 40x position by \~2.5%. Most experienced traders use 2–5x.

### 7. Enter Your Position Size

Enter either:

* **Notional size** — the total value of the position (e.g. $1,000 of BTC)
* **Margin amount** — the collateral you want to put up (e.g. $100, which at 10x gives $1,000 notional)

Required initial margin is calculated as `position size × mark price ÷ leverage`. The terminal shows both values alongside the USDC margin requirement.

### 8. Choose Your Order Type

| Order type              | How it works                                                                         | When to use                                                        |
| ----------------------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------ |
| Market                  | Executes immediately against the order book at the current best price.               | You prioritise speed over price.                                   |
| Limit (GTC)             | Rests on the book at your price until filled or cancelled.                           | You want price control and are willing to wait.                    |
| Limit (IOC)             | Fills immediately against the book up to your limit; cancels any unfilled remainder. | You want price control without leaving an order on the book.       |
| Limit (ALO / Post Only) | Adds to the book and never executes immediately — guarantees you pay maker fees.     | You're providing liquidity and want maker rebates.                 |
| Stop Market             | A market order that triggers when the mark price hits your trigger level.            | Defensive entries (e.g. buy a breakout above resistance).          |
| Stop Limit              | A limit order that activates at your trigger price.                                  | Trigger-based entries with a fill cap.                             |
| Scale                   | A set of limit orders spaced across a price range.                                   | Averaging into a position without manual order placement.          |
| TWAP                    | Splits a large order into 30-second sub-orders, capped at 3% slippage each.          | Sizing into or out of a large position with minimal market impact. |

### 9. Review the Order Summary

Before confirming, check:

* **Entry price** — where the position opens
* **Liquidation price** — the price at which the position will be forcibly closed
* **Required margin** — USDC locked as collateral
* **Estimated fee** — based on your current volume tier (see [Fees](fees.md))

> **Info:** Your liquidation price is shown before you confirm. If the mark price reaches it, the position is closed automatically and the margin is lost. Adjust leverage or size if the gap to the current price is uncomfortable.

### 10. (Optional) Attach Take-Profit and Stop-Loss

You can attach TP/SL orders during entry. They trigger off the **mark price**, not last trade. See [How to Close a Position](how-to-close.md) for details on how they fire.

### 11. Confirm the Trade

Click **Confirm** to submit. Your position will appear in the Positions panel once it fills.

***

## After Opening

* Set or verify your **take-profit** and **stop-loss** — see [How to Close a Position](how-to-close.md).
* Monitor the **funding rate** — see [Fees](fees.md#funding) for how it affects your holding cost.
* Watch your **liquidation price** — especially in volatile markets or when funding is paying you to stay in.
