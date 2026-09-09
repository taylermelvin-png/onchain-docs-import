# Finding Tokens

Trenches gives you two discovery surfaces — the **Live** scanner for real-time launches and the **Explorer** for filtered browsing — plus the signal layer that tells you what's worth a second look.

***

## Live — the scanner

Three columns stream tokens in real time as they move through the launch lifecycle:

| Column | What's in it |
| --- | --- |
| **New** | Just launched — the freshest tokens on the curve |
| **Bonding** | Progressing along the bonding curve toward graduation |
| **Graduated** | Completed the curve and now trading on a full DEX |

* **Hover to freeze.** Moving your cursor into a column pauses it so the card you're reading doesn't scroll away — a pause icon shows while frozen. Searching freezes it too.
* **Filter per column** — age, bonding %, market cap, volume, and holder-quality ranges (dev, sniper, bundler, and insider share), plus "my tokens first".
* **Pin to watchlist** — right-click a card (long-press on mobile) to pin it.
* **Hover a token's logo** for a quick preview without leaving the feed.

***

## Explorer — the browser

Five views, each a different cut of the market:

| View | What it surfaces |
| --- | --- |
| **Pumping** | Strongest 1-hour price movers with real liquidity |
| **All** | Everything, sorted by 24h volume |
| **New** | Latest listings |
| **Gainers** | Biggest 24h gainers among established tokens |
| **Watchlist** | Your pinned tokens, as cards or a chart grid |

Filter by launchpad, then stack up to four filters on top: pre-graduated vs. graduated, minimum market cap / liquidity / volume / holders, bonding-curve range, age, and FDV.

<!-- 📸 SCREENSHOT NEEDED: Explorer view with token cards and filters -->

***

## What a token card tells you

Every card carries the numbers that matter for a fast read:

* **Price action** — market cap and volume with live green/red flashes
* **Bonding progress** — how far along the curve the token is
* **Flow** — buys vs. sells, holder count, liquidity, 1h change
* **Age** — time since launch
* **Socials** — X, Telegram, and website links when the token has them
* **Launchpad badge** — which platform it launched on

### Holder-analysis chips

Four chips flag who actually holds the supply — the fastest rug check available:

| Chip | What it measures |
| --- | --- |
| **Dev** | The deployer's share of supply — "sold" means the dev fully exited |
| **Sniper** | Supply held by launch snipers |
| **Bundler** | Supply bought in bundled transactions |
| **Insider** | Supply held by insider-linked wallets |

Each chip shifts from neutral to caution to danger as that group's share of supply grows. Hover a chip for detail — the dev's wallet, buy/sell counts, and totals.

<!-- 📸 SCREENSHOT NEEDED: Token card close-up with holder-analysis chips -->

### The audit strip

The token detail header adds a **Top 10 holders %** readout (red when ten wallets hold too much of the supply) and an **audit score** — checks for freeze authority, mutable metadata, verified listing, and holder concentration.

***

## Signals and alerts

The **signal strip** across the top of Trenches — and the **Alerts** feed (right rail on desktop, its own tab on mobile) — streams events as they fire:

* **Graduations** — a token completed its curve
* **Whale buys** — large single purchases
* **Dev exits** — a deployer selling out
* **Bond milestones** — tokens crossing 50% and 80% of the curve
* **Volume spikes** — sudden activity crossing meaningful thresholds
* **Your positions and watchlist** — meaningful moves in tokens you hold or pinned
* **Tracked wallets** — buys, sells, and launches from wallets you follow (see [Wallet Tracker](tracker.md))

Click any signal to jump straight to the token.

***

{% hint style="warning" %}
Signals surface what's happening — they don't make it a good trade. High activity is not a substitute for checking holders, liquidity, and the contract. Many hyped tokens go to zero.
{% endhint %}
