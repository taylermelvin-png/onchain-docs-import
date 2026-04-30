# How to Buy a Token

Buying a token on onchain.cc takes under a minute. Here's how it works from search to confirmed swap.

***

## Steps

**1. Search for a token by name or paste its contract address (CA)**

Use the search bar at the top of the terminal. Type the token name or ticker, or paste the contract address directly. Pasting the CA is the most reliable way to find the exact token you're looking for — names and tickers can have duplicates.

\[SCREENSHOT: search bar with a token name and CA example]

***

**2. Review the token info**

Before you trade, check the token's stats in the info panel:

* **Price** — current market price
* **24h Volume** — how actively it's trading
* **Liquidity** — total liquidity available in the pool
* **Market Cap** — fully diluted and circulating where available

Low liquidity is a red flag. Thin markets mean wider spreads and higher slippage. Always review liquidity before buying.

> **Warning:** Low-liquidity tokens carry significantly higher slippage risk. A large buy into a thin pool can move the price against you. Always check the liquidity figure before placing a trade.

***

**3. Enter the amount you want to spend**

In the swap panel, enter how much you want to spend. You can input in SOL or switch to an approximate USD value. The terminal will show you the estimated output amount based on current market conditions and Carbium's routing.

\[SCREENSHOT: swap panel with amount entered and estimated output shown]

***

**4. Set your slippage tolerance**

Slippage is the difference between the price you expect and the price you actually get. It happens because on-chain prices shift between the moment you submit a transaction and when it settles.

> **Info:** **What is slippage?**
>
> Slippage tolerance is the maximum price movement you're willing to accept. If the price moves more than your tolerance before your transaction confirms, the trade will fail rather than execute at a worse price than you expected.
>
> * **Recommended default:** 1–3% for most tokens
> * **High slippage (5%+):** May be needed for low-liquidity or volatile tokens, but increases your exposure to front-running and price impact
> * **Too low slippage:** Your transaction may fail if the price moves even slightly

Set slippage in the swap panel settings before confirming.

***

**5. Click Buy and confirm in your wallet**

Once you've reviewed the trade — output amount, price impact, and slippage — click **Buy**. Your connected wallet will prompt you to confirm the transaction. Review the details in your wallet and approve.

\[SCREENSHOT: wallet confirmation prompt]

***

## After the Trade

> **Success:** A confirmed transaction means your tokens are in your wallet. You can verify the swap on the chain's block explorer (Solana Explorer for Solana, Etherscan for Ethereum, etc.) using the transaction hash shown in the confirmation screen. Your new token balance will appear in Portfolio View.

***

## Quick Reference

| Step | Action                                      |
| ---- | ------------------------------------------- |
| 1    | Search by name or paste CA                  |
| 2    | Review price, volume, liquidity, market cap |
| 3    | Enter spend amount (SOL or USD)             |
| 4    | Set slippage (1–3% recommended)             |
| 5    | Click Buy and confirm in wallet             |
