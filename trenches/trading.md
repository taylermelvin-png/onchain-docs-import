# Trading on Trenches

Trenches is built for speed: pre-configured presets, one-tap buys from any card, and quick sells from your positions. This page covers the trade flow and every setting behind it.

***

## Snipe Presets

The **snipe config bar** is always visible at the top of Trenches. It holds three presets — each a complete trade configuration you can switch between in one click:

* **Amount** — how much to spend per snipe, in your chosen funding currency
* **Buy slippage / sell slippage** — your tolerance per side
* **Priority settings** — how aggressively your transaction competes for inclusion

Defaults ship sensibly (small size, ~10–20% slippage for launch conditions, fast-inclusion settings on) and everything is editable in the preset settings. Fund snipes with **SOL, USDC, or USD1** — if a token's curve quotes in a different currency, Trenches bridges the difference automatically inside the same transaction.

<!-- 📸 SCREENSHOT NEEDED: Snipe config bar with the three presets open -->

{% hint style="info" %}
Launch-moment trading needs higher slippage than normal swaps — fast launches routinely move double-digit percent between submission and inclusion. Below 10% your snipes on hot launches are likely to fail; the settings panel warns you accordingly.
{% endhint %}

***

## Ways to Trade

1. **Quick snipe from a card** — one tap on any Live or Explorer card buys with your active preset. Graduated tokens get the same one-tap **Buy**.
2. **The token page terminal** — full Buy/Sell panel with amount presets, currency selector, and your slippage / priority / tip settings one tap away. The chart supports overlays for your average entry and exit, and the token's dev trades.
3. **Quick grid** — hover (or tap) a position row for an instant grid of buy amounts and sell percentages.
4. **Sell from Positions** — the Positions tab shows every bag with live PnL; quick-sell buttons fire at your configured sell percentage (default 100%, configurable to 25/50/75% and more).

Transactions are submitted for the fastest possible inclusion, with MEV protection on by default.

***

## Guardrails

* **Price-impact block at 20%** — Trenches refuses trades whose quoted impact exceeds 20% of the pool, protecting you from fat-fingering a thin curve.
* **Gas pre-check** — before a buy, the terminal verifies your SOL covers the trade plus network fees, priority fee, and tips, with a safety buffer, so you don't strand a transaction mid-flight.
* **Trade reverts, not bad fills** — if price moves beyond your slippage between submission and inclusion, the trade reverts and you keep your funds (minus network gas).

***

## Fees

* **Platform fee:** the same schedule as [Swap](../swap/fees.md) — 0.50% per trade, with 25–50% returned as [cashback](../colosseum/cashback.md) by Colosseum rank.
* **Launchpad protocol fees:** each launchpad charges its own fee on its trades — included in the quoted price you see, not an onchain.cc charge.
* **Network costs:** Solana gas plus your configured priority fee and inclusion tip.

***

## Positions and PnL

The **Positions** tab aggregates every Trenches bag: total value, open positions, and unrealized PnL, with per-position cost basis where available. Pending buys show while a trade confirms. Any position can be shared as a PnL card — copy, download, or post it to X in one tap.

***

{% hint style="warning" %}
One-tap trading is a loaded weapon by design. Check your active preset — amount, slippage, funding currency — before a session. The card you tap is the trade you get.
{% endhint %}
