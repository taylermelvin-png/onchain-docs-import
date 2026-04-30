# Derek Bot

> **Info:** Derek Bot tracks Solana wallet activity and Solana-token calls. It is part of the same Solana-only Trenches surface as the [Degen Feed](degen-feed.md) — coverage on other chains is on the roadmap.

Derek Bot is onchain.cc's first-caller intelligence layer. It tracks which wallets and influencers called tokens before the price moved — and surfaces their historical track record directly on the platform.

The thesis is simple: not all alpha is equal. Some wallets are consistently early. Derek Bot exists to tell you which ones, when they moved, and how it played out.

***

## What Derek Bot Does

Most token discovery tools tell you what is moving right now. Derek Bot tells you who saw it coming.

Derek Bot continuously monitors public wallet activity and social posts across the Solana ecosystem. When a wallet takes an early position in a token, or when an influencer posts about a token before it gains traction, Derek Bot logs the call. Over time, it builds a track record for each first-caller: how often they are early, how often those calls hit, and how big the average move was after their call.

This data is surfaced on two places inside onchain.cc:

* **Token pages** — the first-caller panel shows who called the token, when, and their historical accuracy
* **Degen Feed** — tokens with active Derek Bot flags are surfaced with a first-caller badge on the card

***

## Why First-Caller Data Matters

In Solana DeFi, information asymmetry is one of the main edges available to retail traders. Some wallets are structurally earlier than others — they have better sources, faster execution, or better instincts about what gains traction.

The problem is that identifying those wallets historically required hours of manual on-chain investigation. Derek Bot automates that research and makes it available to everyone on onchain.cc.

When you see that a first-caller with a 70%+ historical hit rate flagged a token 4 hours ago, that is a materially different signal than an anonymous social post. It is not a guarantee. But it is real, verifiable information with a track record attached to it.

***

## How First-Caller Data Works

1. **Monitoring** — Derek Bot monitors public wallet transactions on Solana and public posts on X/Twitter in real time.
2. **Call identification** — when a tracked wallet buys into a token early, or a tracked influencer posts about a token before it moves, Derek Bot records the call with a timestamp and token snapshot.
3. **Track record calculation** — each first-caller builds a track record over time: number of calls, hit rate (% that resulted in a significant price move after the call), and average return window.
4. **Surfacing** — that data appears on the relevant token page and in the Degen Feed so you can factor it into your own decision.

Derek Bot does not weight social buzz or follower counts. It weights demonstrated on-chain behavior and verifiable post timestamps against subsequent price action.

***

## Reading the First-Caller Panel

\[SCREENSHOT: Derek Bot first-caller UI on a token page]

The first-caller panel on a token page shows:

| Field                   | What It Shows                                                           |
| ----------------------- | ----------------------------------------------------------------------- |
| **Caller**              | Wallet address or influencer handle                                     |
| **Called at**           | The timestamp when the call was made or position opened                 |
| **Token price at call** | Price when the first-caller entered or posted                           |
| **Current price**       | Live price — lets you see the move since the call                       |
| **Historical hit rate** | % of this caller's past calls that resulted in a significant price move |
| **Total calls tracked** | Sample size — higher numbers make the hit rate more meaningful          |

A caller with 5 calls and a 100% hit rate is less informative than one with 80 calls and a 72% hit rate. Sample size matters.

***

## Where to Find Derek Bot Data

Derek Bot data is visible in two places on onchain.cc:

* **Token detail pages** — open any token from the Degen Feed or Trading Terminal search to see the full first-caller panel
* **Degen Feed cards** — tokens with active Derek Bot flags display a first-caller indicator alongside the standard signal data

You do not need to navigate anywhere special. If Derek Bot has flagged a token, the data is surfaced in the same flow as the rest of your research.

***

> **Info:** Derek Bot tracks and surfaces publicly available information — wallet activity on Solana and public social posts. It does not guarantee price performance. First-caller data is historical. Past accuracy does not predict future results. Use it as one signal among many, not as a trading instruction.
