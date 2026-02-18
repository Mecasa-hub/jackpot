---
description: The heart of JACPOT — a two-tier daily draw system with guaranteed small wins and a conditional jackpot
---

# Jackpot System

## Overview

The JACPOT draw system operates on **two tiers** that run simultaneously every day:

| Tier | Name | Frequency | Winners | Condition |
| --- | --- | --- | --- | --- |
| **Tier 1** | Daily Small Wins | Every day | Multiple wallets | Always happens — no conditions |
| **Tier 2** | Daily Jackpot | Every day | 1 winner | Conditional — based on internal protocol parameters |

This dual structure ensures that **someone always wins something every day**, while the big jackpot grows until conditions are met for a life-changing payout.

## How the Jackpot Pot Grows

The Jackpot Pot is a USDC-denominated smart contract funded by a **single source**:

| Source | Contribution |
| --- | --- |
| **Buy Tax (5%)** | 4% → Jackpot Pot, 1% → Team (deployer-adjustable) |
| **Sell Tax (5%)** | 4% → Jackpot Pot, 1% → Team (deployer-adjustable) |

> The pot is always denominated in **USDC** — no exposure to token price volatility. Raffle ticket sales do **not** fund the jackpot directly; they flow to the Treasury.

---

## Tier 1: Daily Small Wins

Every day, **25 ticket buyers** are randomly selected to receive small prizes. This happens regardless of any other conditions — if tickets were sold that day, small wins are distributed.

### Funding

Small wins are funded by **10% of that day's total raffle ticket sales**, allocated from the Treasury.

### Tiered Winner Structure

| Place | Winners | Share of Pool | Example ($1,000 pool) |
| --- | --- | --- | --- |
| **1st Place** | 1 wallet | 30% | **$300** |
| **2nd – 5th** | 4 wallets | 40% (10% each) | **$100 each** |
| **6th – 25th** | 20 wallets | 30% (1.5% each) | **$15 each** |
| **Total** | **25 winners** | **100%** | **$1,000** |

### Small Wins at Different Ticket Volumes

| Daily Ticket Sales | 10% Small Wins Pool | 1st Place | 2nd–5th | 6th–25th |
| --- | --- | --- | --- | --- |
| $1,000 | $100 | $30 | $10 each | $1.50 each |
| $5,000 | $500 | $150 | $50 each | $7.50 each |
| $10,000 | $1,000 | $300 | $100 each | $15 each |
| $50,000 | $5,000 | $1,500 | $500 each | $75 each |

### Selection Method

- Winners are selected **purely at random** using Chainlink VRF
- Every ticket buyer that day has an equal chance
- Luck Score does **not** affect small win odds — this is a level playing field

### Claim Requirement: Share on X

To claim a small win prize, the winner **must share a post on X (Twitter)**.

```
User wins small prize
        │
        ▼
DApp displays: "You won! Share on X to claim your reward"
        │
        ▼
User clicks → Auto-generated post:
"Just won on @JACPOT_Base! #JACPOT #Base"
        │
        ▼
DApp verifies post via X API
        │
        ▼
Prize released to wallet in USDC
```

This creates a **viral marketing engine** built directly into the protocol:

- 25 winners per day = 25 organic posts per day minimum
- Real people sharing real wins = social proof
- Zero marketing cost — the prize was already allocated
- Non-holders see wins in their feed → FOMO → new users join

---

## Tier 2: Daily Jackpot (Conditional)

The Jackpot is the **big prize** — a single winner takes home a significant USDC payout. However, the jackpot draw is **conditional**: internal smart contract parameters determine whether a winner is drawn on any given day.

### When a Winner IS Drawn

If the protocol's internal conditions are met, a jackpot winner is selected:

| Allocation | Percentage | Destination |
| --- | --- | --- |
| **Winner Prize** | 50% | Sent directly to winner's wallet in USDC |
| **Rollover** | 35% | Stays in the pot for the next draw |
| **LP & Buyback** | 10% | Used to buy back JACPOT and add to LP |
| **Treasury** | 5% | Sent to treasury for ecosystem operations |

> The pot **never fully drains** — 35% always rolls over, ensuring the next day's pot starts with a healthy base.

### When No Winner Is Drawn

If conditions are not met for a jackpot draw, the **No-Winner Protocol** activates:

| Allocation | Percentage | Destination |
| --- | --- | --- |
| **Staker Rewards** | 15% | Distributed to JACPOT stakers as USDC |
| **Rollover** | 85% | Stays in the pot — grows for tomorrow |

This means:

- **Stakers earn real USDC** on days when no jackpot winner is drawn
- The pot **grows larger** every day it rolls over
- A growing pot creates increasing excitement and attracts more participants
- Eventually, conditions are met and a massive jackpot is awarded

> The team **never** benefits from a no-winner scenario. This is enforced at the smart contract level.

### Winner Selection Process

1. **Condition Check** — Smart contract evaluates internal parameters
2. **If conditions met** → proceed to draw
3. **Snapshot** — All valid ticket holders are snapshotted
4. **Luck Weighting** — Each entry is weighted by the holder's current Luck Score
5. **VRF Request** — A Chainlink VRF request is submitted on-chain
6. **Random Selection** — The VRF response selects a weighted random winner
7. **Payout** — USDC is automatically sent to the winner's wallet
8. **Announcement** — Winner address and amount are published on-chain and in the UI

### Odds Calculation

Your odds of winning the jackpot (when a draw occurs):

```
Your Odds = (Your Tickets × Your Luck Multiplier) /
            Sum of (All Tickets × All Luck Multipliers)
```

**Example:**
- You hold 5 tickets with a Luck Multiplier of 3x (Gold tier)
- Your weighted entries: 5 × 3 = 15
- Total weighted entries in the draw: 1,000
- Your odds: 15 / 1,000 = **1.5%**

> **Staking gives you significantly better odds — without spending more on tickets.**

---

## Full Day Example

```
Day 47 — Jackpot Pot: $8,000

Trading Volume: $100,000
  └── 5% Tax = $5,000 (4% = $4,000 → Jackpot Pot, 1% = $1,000 → Team)
  Jackpot Pot now: $12,000

Ticket Sales: 200 tickets = $3,000 revenue
  └── 100% → TREASURY
         │
    Treasury allocates:
         │
         ├── 10% ($300)   → Small Wins Pool
         ├──  5% ($150)   → Staker Rewards (USDC)
         ├──  5% ($150)   → Development
         ├──  5% ($150)   → Treasury Reserves
         └── 75% ($2,250) → DeFi Yield Deployments

DAILY SMALL WINS (always happens):
    Prize pool: $300
    1st Place: $90
    2nd–5th: $30 each
    6th–25th: $4.50 each
    All 25 winners share on X to claim!

JACKPOT CHECK:
    Protocol evaluates internal conditions...

    Scenario A — No Winner:
      15% of pot ($1,950) → Stakers (USDC)
      85% of pot ($11,050) → Rolls over to tomorrow

    Scenario B — Winner Drawn:
      50% ($6,500) → Winner's wallet
      35% ($4,550) → Rollover for tomorrow
      10% ($1,300) → LP & Buyback
       5% ($650)   → Treasury

End of Day Summary:
    25 people won small prizes (shared on X)
    Stakers earned USDC rewards
    Jackpot either paid out or grew bigger
    Cycle repeats tomorrow
```

---

## Why Two Tiers?

| Feature | Effect |
| --- | --- |
| **Daily small wins** | People come back every day — "I might win today" |
| **Conditional jackpot** | Pot can't be drained during low participation |
| **Growing pot** | When jackpot doesn't trigger, pot gets bigger → more exciting |
| **Self-correcting** | Bigger pot → more participants → conditions eventually met → winner drawn |
| **Stakers always earn** | 5% from ticket sales + 15% on no-winner days |
| **Viral marketing** | 25 tweets per day from real winners at zero cost |

## Jackpot Transparency

- Pot balance is **publicly visible** on-chain at all times
- A real-time counter on the JACPOT website shows the current pot size
- All draw transactions are verifiable on-chain
- Historical draws, winners, and amounts are displayed on the "Winner Wall"
- Small win distributions are logged and publicly viewable

## Smart Contract Details

- Jackpot contract is **non-upgradeable** after deployment
- No admin function can withdraw from the pot
- Draw execution is permissionless (anyone can trigger it after the scheduled time)
- Emergency pause function requires multi-sig approval (for critical bugs only)
- Chainlink VRF ensures provably fair randomness for both tiers
