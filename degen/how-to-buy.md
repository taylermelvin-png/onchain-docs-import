# How to Buy a Pre-Graduated Token

Buying a pre-grad on Degen takes under a minute once your wallet is connected and funded with SOL. This page walks the flow step-by-step.

\[SCREENSHOT: Degen buy panel with a pre-graduated token, bonding-curve progress bar, and amount field]

***

## Before You Start

* You need a connected Solana wallet (Phantom, Solflare, Backpack) or an EVM wallet with the Solana sign-in flow handled by Privy.
* You need **SOL** on Solana — both for the trade and for gas. Keep at least 0.05 SOL in reserve for gas.
* You need to have identified a token. Most users come in via the [Degen Feed (Trenches)](../discover/degen-feed.md) or by pasting a contract address.

***

## Steps

### 1. Open the Degen Tab

Click the **Degen** tab at the top of the onchain.cc terminal. This loads the Degen surface, separate from Swap and Perps.

### 2. Select a Token

You have two options:

* **Browse from Trenches** — click any token card in the [Degen Feed](../discover/degen-feed.md) to open it directly in Degen.
* **Paste a contract address (CA)** — paste a pump.fun token's CA into the search bar. Degen will detect that the token is pre-graduated and load the bonding-curve interface.

If a token has already graduated, Degen will tell you and route you to [Swap](../swap/terminal-overview.md) for the post-grad trade flow.

### 3. Read the Token Panel

The Degen panel shows everything you need to evaluate the trade:

* **Bonding-curve progress** — a bar showing how far along the curve the token is (e.g. "73% of the way to graduation").
* **Current price** and **market cap**.
* **Liquidity behind the curve** — how much SOL is currently held by the bonding curve. Larger = more depth = less slippage on your size.
* **Holder count** and **buy/sell ratio** in the last hour.
* **Time since launch** and recent volume.

> **Warning:** Pump.fun tokens carry high rug-pull and abandonment risk. Even with healthy onchain signals, most pre-grads never graduate. Verify the contract address, check holder concentration, and only deploy capital you are willing to lose entirely.

### 4. Enter Your Buy Amount

Enter how much **SOL** you want to spend. Degen will quote:

* The estimated tokens you'll receive
* The implied price after this trade lands (price impact)
* The new bonding-curve position after the buy

The price impact is generally larger than on a normal DEX swap — see [Pump.fun Bonding Curves](bonding-curves.md) for why.

### 5. Set Slippage Tolerance

Degen lets you set a slippage tolerance for the trade.

* **Default:** 5%
* **Active launch / fast mover:** 10–15%
* **Calm token, deep liquidity:** can go lower, e.g. 2–3%

If price moves more than your tolerance between submission and inclusion, the trade reverts (you keep your SOL minus gas).

> **Info:** Setting slippage very high (e.g. 30%+) makes you a sandwich target. Only push it up if you accept getting worse fills as the cost of getting any fill at all.

### 6. Review the Order

Before confirming, check:

* **Spend amount** in SOL
* **Estimated output** in tokens
* **Price impact** percentage
* **Slippage tolerance**
* **Platform fee** — your rank-based fee (0.15% at Recruit, 0.10% at Immortal). See [Rank System](../colosseum/ranks.md).

### 7. Confirm and Sign

Click **Buy**. Your wallet (or the Privy embedded wallet) will prompt you to sign the transaction. Approve.

The transaction is submitted directly to the pump.fun bonding-curve contract on Solana. Once confirmed, the tokens land in your wallet and appear in [Portfolio View](../portfolio/portfolio-view.md).

\[SCREENSHOT: Confirmation screen showing the executed trade with transaction hash]

***

## Selling a Pre-Graduate

The flow is symmetric: open the token in Degen, switch to **Sell**, choose how much you want to offload (or use the 25% / 50% / 75% / 100% quick-sell buttons), set slippage, and confirm. Selling pushes the bonding curve back down by exactly as much as your buy pushed it up — see [Pump.fun Bonding Curves](bonding-curves.md) for why.

> **Info:** If a token is illiquid or holders are exiting in size, sell impact can be large. Consider selling in smaller tranches if you're trying to exit a meaningful position.

***

## After Graduation

If the token you hold **graduates** while you're holding it, your position transitions automatically:

* The token starts trading on Raydium and other Solana DEXes.
* Future buys and sells go through [Swap](../swap/terminal-overview.md) (Carbium routes the order across the post-grad liquidity).
* Your existing holdings are unaffected — the tokens in your wallet are the same; only the venue for trading them changes.

There is no action required from you at graduation. Just be aware that price behaviour around the graduation event can be volatile in either direction.
