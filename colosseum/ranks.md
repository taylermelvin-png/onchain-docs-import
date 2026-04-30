# Rank System

Your rank is your standing in the Colosseum. It reflects how much you have traded, earned, and competed over your lifetime on the platform — and it directly affects two things: how fast you earn points on every future trade, and the **swap fee rate** you pay on every trade.

***

## The Six Ranks

Ranks are determined by your **lifetime total points** — the cumulative points you have earned across all sessions and seasons. As your total points grow, your rank automatically increases.

| Tier | Rank Name | Subtiers | Swap Fee |
| ---- | --------- | -------- | -------- |
| 1    | Recruit   | 1–4      | 0.15%    |
| 2    | Warrior   | 1–4      | 0.14%    |
| 3    | Gladiator | 1–4      | 0.13%    |
| 4    | Champion  | 1–4      | 0.12%    |
| 5    | Warlord   | 1–4      | 0.11%    |
| 6    | Immortal  | 1–4      | 0.10%    |

Each rank applies a **multiplier** to your base point earnings, on top of reducing your swap fee. If you are Champion and another trader is Recruit, you earn more points for the same trade — every time — and pay a lower fee while doing it.

> **Info:** Your rank is based on lifetime points. Rank up once and the benefit is permanent — both the higher point multiplier and the lower fee apply to every trade you make from that point forward.

***

## Subtiers (1–4)

Each rank is divided into **four subtiers** — Recruit 1 through Recruit 4, then Warrior 1, and so on. Subtiers represent your progression *within* a rank:

* You move from subtier 1 → 2 → 3 → 4 as your points accumulate.
* When you complete subtier 4, your next points push you into the next rank's subtier 1.
* The **swap fee is set at the rank level**, so all four subtiers within a rank pay the same fee rate.
* Subtier progression unlocks visual badge upgrades and feeds your overall rank progression speed.

***

## Swap Fee Reduction

Every rank step reduces your swap fee by 0.01 percentage points, all the way down to the floor of **0.10%** at Immortal:

* **Recruit:** 0.15% (the platform-wide base rate)
* **Warrior:** 0.14%
* **Gladiator:** 0.13%
* **Champion:** 0.12%
* **Warlord:** 0.11%
* **Immortal:** 0.10% (lowest possible fee on onchain.cc)

The fee reduction applies automatically to every trade you make on **Swap** and **Degen** from the moment you cross into the new rank. There is nothing to claim, no token to hold, and no opt-in.

> **Info:** Perps fees follow a separate, volume-based schedule because perps run on Hyperliquid infrastructure with different economics. See [Perps → Fees & Funding](../perps/fees.md) for the perps fee schedule.

> **Success:** Reach Immortal and you pay 0.10% on every trade — a 33% reduction off the base rate, locked in for life.

***

## Points Formula

Every trade you complete generates points using the following formula:

```
Points = Base Rate × Rank Multiplier × Faction Multiplier × Bonus Window Multiplier × Quest Multiplier
```

* **Base Rate** — the baseline points per dollar of volume traded.
* **Rank Multiplier** — scales with your rank tier (higher rank = higher multiplier).
* **Faction Multiplier** — bonus applied when you are a member of an active faction.
* **Bonus Window Multiplier** — applied during time-limited multiplier events.
* **Quest Multiplier** — applied when you are actively completing a qualifying quest.

Stacking these multipliers — by holding a high rank, being in a faction, trading during a Bonus Window, and actively completing quests — is how top traders maximize their point earnings.

***

## How to Rank Up

1. **Trade more volume.** Points accumulate with every trade. No minimum trade size is required — volume compounds over time.
2. **Complete quests.** Daily, weekly, and one-time quests award bonus points that count toward your lifetime total.
3. **Stay active across sessions.** Lifetime points do not reset between sessions. Every session you participate in adds to your rank progress.

There are no shortcuts or rank resets in Season 1. Your rank reflects your real trading history.
