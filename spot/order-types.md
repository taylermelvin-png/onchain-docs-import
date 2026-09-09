# Order Types

Spot supports three order types: **Market**, **Limit**, and **TWAP**. Pick them from the tabs at the top of the order entry panel.

<!-- 📸 SCREENSHOT NEEDED: Spot order entry showing Market / Limit / TWAP tabs -->

***

## Market

Executes immediately against the order book at the best available price.

* **Slippage cap** — market orders carry a maximum slippage setting (default 0.5%, adjustable from 0.01% up to 20%). If the book moves beyond your cap before the order lands, the unfilled remainder is cancelled instead of filling at a worse price.
* Size can be entered in the base asset or in USD, or as a percentage of your balance.

Use market orders when speed matters more than price.

***

## Limit

Rests on the book at your chosen price. Three time-in-force options:

| TIF | Behaviour |
| --- | --- |
| **GTC** (Good til canceled) | Rests on the book until it fills or you cancel it. |
| **IOC** (Immediate or cancel) | Fills whatever it can immediately at your price or better; cancels the rest. |
| **ALO** (Add liquidity only / post-only) | Joins the book without ever matching immediately — cancelled if it would cross. Guarantees you pay the maker rate. |

Use limit orders when you want price control. A resting limit order that fills pays the **maker** fee — the cheapest way to trade on Spot.

***

## TWAP

A TWAP (Time-Weighted Average Price) order splits a large order into small slices executed steadily over a duration you choose, reducing the market impact of sizing in or out.

* **Duration:** 5 minutes to 24 hours. Presets for 15m / 30m / 1h / 4h; default 30 minutes.
* **Randomize timing** (on by default): varies the spacing of the slices so the pattern is harder to front-run.
* **Minimum TWAP size: $100.**

The TWAP runs in the background — you can watch progress and cancel the remainder at any time from the open orders panel.

***

## Order minimums and precision

* Minimum order value: **$10**.
* Prices are quoted to 5 significant figures; size precision varies by asset. The order panel enforces both for you.

***

## After you place an order

* **Open orders** — resting limit orders and running TWAPs appear in the orders panel, where you can cancel them individually or all at once.
* **Fills** — executions appear in your trade history and update your balances immediately.
* **Positions** — spot holdings appear in the Spot tab of [Portfolio](../portfolio/portfolio-view.md), alongside total and available balance.

***

{% hint style="info" %}
Spot has no stop-loss or take-profit orders — those are perps features. If you need conditional exits, see [Perps → How to Close a Position](../perps/how-to-close.md).
{% endhint %}
