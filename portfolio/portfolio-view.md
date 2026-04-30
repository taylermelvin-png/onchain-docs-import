# Portfolio View

The portfolio view gives you a real-time snapshot of everything in your connected wallet — token balances, open positions, current value, and P\&L — without leaving the terminal.

> **Info:** Your portfolio reflects your connected wallet in real time — onchain.cc never holds your funds.

\[SCREENSHOT: portfolio view with positions listed]

***

## What the Portfolio View Shows

The portfolio view updates continuously as on-chain state changes. It is not a snapshot — if a position moves, you see it move.

| Column              | What it shows                                                             |
| ------------------- | ------------------------------------------------------------------------- |
| **Token**           | Token name, ticker, and contract address                                  |
| **Balance**         | Number of tokens held in your wallet                                      |
| **Current Price**   | Live market price, sourced from DEX liquidity on the token's native chain |
| **Value (USD)**     | Current USD value of your holdings at the live price                      |
| **Avg. Entry**      | Average price you paid across all buys of that token                      |
| **Unrealized P\&L** | Profit or loss if you sold now, shown in USD and %                        |
| **Realized P\&L**   | Profit or loss already locked in from previous sells                      |

***

## Navigating the Portfolio

### Token List

The default view shows all tokens currently held in your wallet. Tokens with open positions are sorted by USD value, largest first.

* Use the **search bar** at the top of the panel to filter by token name or ticker.
* Toggle between **All Holdings** and **Open Positions** using the tabs at the top of the list.
* Tokens with zero balance that have realized P\&L history are visible under the **Closed Positions** tab.

### Individual Position View

Click any row in the token list to expand the individual position view. This shows:

* Entry history — each buy transaction with timestamp, price, and size
* Running P\&L broken down by entry lot
* A mini chart showing price action since your first entry

### Unrealized vs. Realized P\&L

* **Unrealized P\&L** — what your current holdings are worth relative to your average entry. This number changes in real time as price moves. It is not locked in until you sell.
* **Realized P\&L** — profit or loss from positions you have already closed. This is final and does not change.

Both figures appear in USD and as a percentage. Your total session P\&L (the figure that feeds into Colosseum rankings) is the sum of realized P\&L within the active session window.

***

## Acting From the Portfolio View

The portfolio view is not just for reading — it is the fastest path to executing a sell.

**To sell from the portfolio view:**

1. Click any token in your token list.
2. The individual position view opens, showing your holdings and current P\&L.
3. Click **Sell** — this opens the Trading Terminal pre-loaded with that token and your full position size pre-filled.
4. Adjust the amount if needed, review slippage, and confirm the transaction in your wallet.

> **Info:** Clicking a token from the portfolio view always opens the Trading Terminal ready to sell. You can adjust size, review fees, and cancel before signing — nothing executes until you approve the transaction in your wallet.

\[SCREENSHOT: portfolio view with positions listed]

***

## Portfolio and Colosseum

Your portfolio data feeds directly into Colosseum scoring. Realized P\&L within an active session counts toward your session score and leaderboard position. Unrealized P\&L does not count until you close the position.

See [Seasons & Sessions](../colosseum/seasons-sessions.md) for how session windows and scoring work.
