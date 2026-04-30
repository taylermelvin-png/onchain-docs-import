# Reading Token Signals

> **Info:** This page covers signals shown on the [Degen Feed](degen-feed.md) and [Derek Bot](derek-bot.md), both of which are currently Solana-only. The mechanics described here apply to Solana tokens.

The Degen Feed and token detail pages surface two categories of signal: onchain and social. Understanding what each signal actually measures — and what its limits are — is the difference between informed conviction and noise-chasing.

***

## Onchain Signals

Onchain signals are derived directly from blockchain activity. They are objective and verifiable.

### New Listing

A token has just launched or added liquidity to a trading pair. "New" means it recently became tradeable on Solana — either through a launchpad like Pump.fun or by adding a pool to a DEX like Raydium.

New listings carry maximum risk and maximum upside potential. There is no price history and often no established community. Treat them as high-conviction or high-speculation plays only.

### Volume Spike

Trading volume has spiked significantly above the token's recent baseline. A volume spike does not tell you whether the move is organic or manufactured — it tells you that something is happening and traders are paying attention.

Cross-reference a volume spike with liquidity. High volume on a low-liquidity token means a small number of trades drove the movement. That can indicate a pump — or it can mean early organic accumulation. Context matters.

### Liquidity

Liquidity is the total value locked in a token's trading pair. It determines how much you can trade without moving the price against yourself (slippage).

| Liquidity Level  | What It Means                                                           |
| ---------------- | ----------------------------------------------------------------------- |
| **Under $10K**   | Extreme caution. Even small trades will cause significant price impact. |
| **$10K — $50K**  | High risk. Suitable only for very small position sizes.                 |
| **$50K — $500K** | Moderate risk. Workable for most retail-size trades.                    |
| **Over $500K**   | Lower slippage risk. More established trading pair.                     |

As a baseline: check that a token has at least $50K in liquidity before entering a position. Anything below that and the math works against you before the trade even settles.

### Holder Concentration

The percentage of total supply held by the top wallets. A high concentration — for example, one wallet holding 30%+ of supply — means a single actor can move the price significantly by selling. Low distribution is a risk factor regardless of volume or social activity.

onchain.cc surfaces the top holder percentage on every token detail page. Review it before sizing into a position.

***

## Social Signals

Social signals measure external activity and sentiment. They are indicative, not deterministic.

### KOL Mentions

Key Opinion Leaders (KOLs) are tracked influencers in the Solana and broader crypto space. When a KOL with an established track record mentions a token, it often precedes a price move — not because the KOL controls the market, but because their audience acts on their commentary.

KOL mention data on onchain.cc is sourced from tracked wallet activity and public posts. You can see which KOLs have flagged a token and when.

### Community Mentions

The volume of public conversation about a token on X/Twitter over a rolling window. A rising community mention count indicates organic interest is building. A sudden spike often correlates with a price move — sometimes leading it, sometimes lagging it.

Community mentions are a momentum indicator, not a valuation signal. High mention volume on a token with no liquidity is a yellow flag, not a green light.

### Derek Bot Flags

Derek Bot is onchain.cc's first-caller intelligence layer. It identifies wallets and influencers that called a token before the price moved, tracks their historical accuracy, and surfaces that data on the platform.

When a Derek Bot flag appears on a token, it means one or more tracked first-callers have a position or made a call on that token. See the [Derek Bot](derek-bot.md) page for a full breakdown of how to interpret first-caller data.

***

## How to Assess Risk Before Trading

Use this checklist before entering any position discovered through the Degen Feed:

1. **Check liquidity** — is it above $50K? If not, understand the slippage math before sizing in.
2. **Check top holder percentage** — is supply concentrated? High concentration is a structural risk.
3. **Cross-reference with Derek Bot** — has a tracked first-caller flagged this token? What is their historical hit rate?
4. **Verify the contract address** — paste the CA into a Solana explorer to confirm the contract is what it claims to be. Copycat tokens are common.
5. **Check the age** — a token listed 3 minutes ago is a different risk profile than one listed 3 days ago.

\[SCREENSHOT: token detail view with signals annotated]

***

> **Warning:** Social signals are indicators, not guarantees. A KOL mention or Derek Bot flag does not mean a token will go up. Many called tokens go to zero. Always do your own research before trading.
