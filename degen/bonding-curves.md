# Pump.fun Bonding Curves

Pre-graduated pump.fun tokens don't trade on a DEX. They trade against a **bonding curve** — a deterministic pricing function controlled by a smart contract on Solana. Understanding how the curve works is essential before buying or selling on [Degen](overview.md), because it changes how you think about price, size, and slippage.

***

## What a Bonding Curve Is

A bonding curve is a pricing formula coded into the token's launch contract. It defines the price of the token as a function of how much has been bought from it. Every buy moves the price up the curve; every sell moves it back down. There is no order book and no separate liquidity pool — the curve **is** the market until the token graduates.

The result is fully deterministic pricing:

* The price you pay depends only on how far up the curve you push it with your buy.
* No one is on the other side of your trade as a counterparty — you're transacting with the contract.
* The price cannot be manipulated by withdrawing liquidity (there is no LP to drain).

***

## The Pump.fun Curve

Pump.fun uses a **virtual constant-product** bonding curve. In practical terms:

* Each token launches with a fixed virtual reserve of SOL and a fixed virtual reserve of the token.
* The price moves as buys and sells push tokens out of and back into the curve.
* The curve is calibrated so that as the market cap approaches roughly **$69k USD**, the curve becomes too expensive to push much further — at which point the token graduates.

### What "Graduation" Means

When a token's market cap crosses the graduation threshold:

1. Pump.fun automatically deposits the accumulated SOL liquidity (~$12k worth at graduation) plus the token reserve into a new Raydium liquidity pool.
2. The bonding curve is closed.
3. From that moment, the token trades on Raydium like any other Solana token.
4. The pool's LP tokens are typically burned, so the liquidity is permanent.

After graduation, you trade the token via [Swap](../swap/terminal-overview.md) (Carbium routes through Raydium and other DEXes), not through Degen.

***

## How Price Moves on the Curve

Two practical implications you need to internalise:

### 1. Bigger buys move the price more

Because the curve is convex, buying $100 of a token at the bottom of the curve costs much less per token than buying $100 of the same token after $50k has already been bought from it. This is true for every bonding curve — it is *the* defining property.

### 2. Slippage is a function of your size relative to the curve depth

On a typical DEX swap with deep liquidity, a $100 trade barely moves the price. On a fresh pump.fun token with $5k of liquidity behind the curve, a $100 trade can move it noticeably. Set your slippage tolerance accordingly — Degen displays the expected price impact before you confirm.

> **Warning:** Slippage on pre-graduates can spike sharply during launches and rugs. If price moves more than your tolerance allows, the trade reverts. Setting slippage too high to compensate exposes you to MEV-style sandwiching and worse fills. Default to **5–10%** for active pre-grads; only push higher if you accept the worse-fill risk.

***

## What This Means for Your Strategy

* **Earlier is cheaper.** The same $100 buys more tokens early on the curve than late on it. The flip side: most pre-grads die before graduating.
* **Exits matter as much as entries.** Selling pushes price back down the curve. If you and other holders all try to exit at once, the curve makes the cascade explicit and brutal — there's no LP buffer.
* **Graduation is a discrete event.** Tokens that graduate often have a price reaction at graduation as the market re-prices around the new Raydium liquidity. Some traders specifically target graduation events.
* **No graduation, no exit.** A token that never graduates remains trapped on the curve. If liquidity dries up, you may not be able to sell at any reasonable price.

> **Info:** Graduation is the rare success case, not the expected case. Most pump.fun tokens never reach the threshold. Treat every pre-grad as a high-mortality trade by default.
