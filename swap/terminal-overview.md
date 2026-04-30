# Swap Terminal Overview

The Swap product is onchain.cc's cross-chain spot trading terminal — built for traders who want fast execution, best-price routing, and full self-custody, without paying the inflated fees charged by most DeFi frontends. Trade across **17+ chains** from a single interface. (For pre-graduated pump.fun tokens, see [Degen](../degen/overview.md). For perpetual futures, see [Perps](../perps/overview.md).)

***

## What It Is

onchain.cc is a DEX terminal that spans 17+ chains. You connect your self-custody wallet, search for any token, and trade directly on-chain. There is no custodian, no order book, and no intermediary holding your funds. Every trade settles on-chain in seconds.

***

## Key Features

### Fast Execution

Trades are routed and submitted to the relevant chain with minimal latency. You see a price, you confirm, it settles.

### Best-Price Routing via Carbium

Every swap goes through Carbium — onchain.cc's internal DEX aggregator. Carbium splits and routes your order across DEX liquidity sources to get you the best available price. You don't configure anything; it works automatically on every trade.

### Rank-Based Platform Fee (0.15% → 0.10%)

onchain.cc charges 0.15% per trade at the **Recruit** rank — the lowest base platform fee in DeFi. Each Colosseum rank reduces your swap fee by 0.01 percentage points, all the way down to **0.10% at Immortal**. See [Rank System](../colosseum/ranks.md) for the full schedule.

### Self-Custody

You authenticate via Privy and trade with your own wallet. onchain.cc never holds your tokens. Every transaction is yours to verify on-chain.

***

## Navigating the UI

### Search Bar

Located at the top of the terminal. Search by token name or paste a contract address (CA) directly. Results show token name, ticker, price, and liquidity at a glance.

### Swap Panel

The primary trading interface. From the swap panel you can:

* Select the input token (what you're spending) and the output token (what you're buying)
* Enter an amount in SOL or approximate USD value
* Set slippage tolerance
* Review the quoted output and route before confirming

### Token Info Panel

Displayed when you select a token. Shows:

* Current price
* 24-hour volume
* Liquidity depth
* Market cap
* Price chart

Use the token info panel to assess a token before committing to a trade.

***

\[SCREENSHOT: full trading terminal UI]

***

## What You Need to Trade

* A connected self-custody wallet (via Privy)
* A small balance of the chain's native token (e.g. SOL on Solana, ETH on Ethereum) for gas fees
* The token you want to sell, or the chain's native token if you're buying

> **Info:** Gas fees are paid in the chain's native token (SOL on Solana, ETH on Ethereum, etc.) and are separate from the 0.15% platform fee. Keep a small balance of the native token on whichever chain you're trading on to cover transaction costs.
