# Launchpads & Graduation

New launchpad tokens don't start life on a normal DEX. They trade on a **bonding curve** — a pricing contract that is the market until the token "graduates" to a full liquidity pool. Understanding that lifecycle is essential to trading Trenches well.

***

## Bonding Curves

A bonding curve is a pricing formula coded into the token's launch contract:

* Every **buy** pushes the price up the curve; every **sell** pushes it back down.
* There is no order book and no separate liquidity pool — you transact with the contract itself.
* Pricing is deterministic: what you pay depends only on how far up the curve your buy pushes it.

Two practical implications:

1. **Earlier is cheaper.** The same spend buys more tokens low on the curve than high on it. The flip side: most tokens never make it far up the curve.
2. **Your size moves the price.** On a fresh token with little behind the curve, even a modest buy has visible price impact. Trenches shows the expected impact before you confirm — and blocks trades where it would exceed 20%.

***

## Graduation

When a token completes its bonding curve, its liquidity migrates automatically to a full DEX pool and the curve closes. Where it lands depends on the launchpad:

| Launchpad | Graduates to |
| --- | --- |
| **PumpFun** | PumpSwap |
| **LaunchLab** | Raydium |
| **Meteora** | Meteora pools |

Each launchpad sets its own graduation threshold, and the **bonding progress bar** on every token card and detail page shows how close a token is. At 100% the token reads **Graduated**.

<!-- 📸 SCREENSHOT NEEDED: Bonding-curve progress bar on a token page -->

**What graduation means for you:**

* **Nothing happens to your holdings.** The tokens in your wallet are the same; only the venue changes.
* **Trading continues seamlessly** — Trenches routes post-graduation trades to the token's new pool automatically (and checks the available venues to fill you at the best price). The buy button simply switches from **SNIPE** to **Buy**.
* **Price can move sharply around the event** in either direction as the market re-prices on the new pool.

***

## The Risk Ledger

* **Graduation is the rare case, not the expected one.** Most launchpad tokens die on the curve.
* **Exits are as brutal as entries are cheap.** Selling pushes the price back down the curve — if holders exit together, the cascade is explicit and there is no LP buffer to absorb it.
* **No graduation can mean no exit.** A token abandoned on its curve may have no meaningful liquidity left to sell into.

{% hint style="warning" %}
Treat every pre-graduation token as a high-mortality trade by default. The holder-analysis chips and audit strip (see [Finding Tokens](discovery.md)) exist to keep the odds honest — use them before you size in.
{% endhint %}
