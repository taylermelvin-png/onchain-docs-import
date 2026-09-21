# FAQ

Answers to the most common questions about onchain.cc.

***

## General

### Is onchain.cc safe to use?

onchain.cc is built and backed by Bitso — Latin America's largest licensed crypto exchange — and is fully self-custodial: you always control your own wallets and private keys, and onchain.cc never holds your funds or can move your assets on your behalf. As with all of crypto, the risk that remains is the market itself — trade accordingly.

### How do I sign in? Do I need a wallet?

You can sign in three ways: **Google**, **email** (with a 6-digit code), or by connecting an existing **Solana or EVM wallet**. Signing in with Google or email creates embedded self-custody wallets for you — one Solana, one EVM — managed non-custodially through Privy. You can view them, and export their private keys, on the Wallets page at any time.

### Is onchain.cc available in my country?

The terminal is available in most countries, but certain products are restricted in certain jurisdictions — you'll see a notice on the affected product if that applies to you, and our [Terms of Use](https://onchain.cc/terms/#restricted) list the details. Prediction markets have their own jurisdiction rules; in some regions you can browse markets but not place orders.

***

## Trading

### What are the fees?

It depends on the product:

* **Swap and Trenches** — 0.50% per trade. Trenches trades also carry the launchpad's own protocol fee, included in the quoted price.
* **Spot** — buys are free; sells pay 0.25% maker / 0.35% taker.
* **Perps** — Hyperliquid's volume-tiered maker/taker fee plus a 0.05% Onchain service fee, shown combined in the order panel.
* **Predictions** — 0.50% per order, capped on low-priced shares.

And on all of it: **25–50% of every fee comes back to you as [cashback](../colosseum/cashback.md)**, set by your Colosseum rank and claimable in USDC. Network gas applies to on-chain trades (Swap/Trenches) and is sponsored on most EVM chains.

### How does cashback work?

Every fee you pay accrues cashback at your rank's rate (25% at Recruit up to 50% at Immortal), into weekly buckets you claim from the Cashback panel — minimum claim $1, paid on-chain in seconds. **Claim regularly: buckets expire 14 days after their week closes (30 days at Warlord and Immortal)**, and accrual pauses if you go 60 days without trading. Full detail: [Cashback](../colosseum/cashback.md).

### Do I need a chain's native token to trade?

For **Swap and Trenches**: on Solana, Ethereum, and BNB, yes — keep a small native-token balance for gas or transactions will fail (on Solana, a few thousandths of a SOL covers a trade). On the other supported EVM chains gas is sponsored. **Spot, Perps, and Predictions** trade from funded product balances, so orders there don't need gas from your wallet.

### What is a contract address (CA)?

The unique on-chain identifier for a token. Pasting a CA into the search bar is the fastest and safest way to pull up exactly the token you mean — names and tickers can be duplicated; contract addresses can't. Always verify the CA before trading.

### Why did my transaction fail?

The two most common causes on on-chain trades: insufficient native-token balance for gas, or slippage set below what the market moved. Failed transactions revert — you keep your funds (minus network gas). Top up gas or raise slippage slightly and retry. On launch-moment Trenches trades, slippage below ~10% frequently fails by design — fast curves move faster than your transaction lands.

### What happens to my funds if I close the app?

Nothing. Your funds live in your wallets and product balances on-chain, not on onchain.cc's servers. Sign back in and everything is where you left it.

***

## Colosseum

### How do I join Colosseum?

You already have. Enrollment is automatic when you create an account, and your first trade starts earning points. Head to the Colosseum tab to see your rank, quests, and leaderboard position.

### What's the difference between a Season and a Session?

A **Season** is the long campaign (weeks to months) with the headline prize pool. A **Session** is a shorter competition inside it — typically weekly — with its own leaderboard and prizes, scored from zero. Rank points reset when a new season opens — everyone starts the climb again from Recruit — while your lifetime points balance carries forever.

### How do I rank up faster?

Rank points come from trading volume, at each product's own rate — Trenches earns the most per dollar, and quests add points on top. Occasional Bonus Windows and faction boosts multiply earnings, but the base rates carry the climb. See [Rank System](../colosseum/ranks.md) for the full rate table and thresholds.

### When do session prizes arrive?

Payouts follow **about a week after the session ends** — a verification window runs first, then prizes are distributed.

### How do referrals work?

Every account has a referral link — find your code in the Colosseum section, and it's attached automatically when you share PnL cards to X. Traders who join through your link and trade earn you referral rewards, tracked through referral quests.

***

## Support

### How do I contact support?

**Discord** is the primary channel — join via the link at [onchain.cc](https://onchain.cc) and head to the help channels. In the terminal, **Get support** in the menu opens live chat. For announcements, follow [@Onchaincc](https://x.com/Onchaincc) on X. See [Support & Community](support.md).
