---
description: The heart of JACPOT — a continuously growing, provably fair jackpot
---

# Jackpot System

## Overview

The Jackpot is the central prize pool of JACPOT. It grows continuously from trading tax revenue and raffle pass sales, and is distributed through provably fair draws powered by Chainlink VRF.

## How the Jackpot Grows

The Jackpot Pot is a USDC-denominated smart contract that receives funds from two sources:

| Source | Contribution |
| --- | --- |
| **Buy Tax** | 100% of the 5% buy tax (in USDC) |
| **Sell Tax** | 100% of the 5% sell tax (in USDC) |
| **Raffle Pass Sales** | 90% of all raffle pass purchase revenue |

> The pot is always denominated in USDC — no exposure to token price volatility.

## Jackpot Distribution

![Jackpot Prize Distribution](../assets/chart-jackpot-distribution.png)

When a draw occurs and a winner is selected:

| Allocation | Percentage | Destination |
| --- | --- | --- |
| **Winner Prize** | 50% | Sent directly to winner's wallet in USDC |
| **Rollover** | 35% | Stays in the pot for the next draw |
| **LP & Buyback** | 10% | Used to buy back JACPOT and add to LP |
| **Treasury** | 5% | Sent to treasury for ecosystem operations |

### If No Winner Is Selected

In the rare event that no valid winner is drawn (e.g., all eligible entries expired):

- **100% of the pot rolls over** to the next draw
- The pot continues to grow
- No funds are diverted to team or marketing
- This creates a growing "must-win" pot that generates excitement

> The team **never** benefits from a no-winner scenario. This is enforced at the smart contract level.

## Draw Schedule

| Draw Type | Frequency | Eligibility |
| --- | --- | --- |
| **Weekly Draw** | Every Friday at 20:00 UTC | All valid Raffle Pass holders |
| **Mini Draw** | Every Wednesday at 20:00 UTC | Silver+ Luck Tier stakers only |
| **Monthly Mega Draw** | 1st of each month | All valid Raffle Pass holders (boosted pot) |
| **Pressure Mode Mega Draw** | Triggered by conditions | All valid Raffle Pass holders |

## Winner Selection Process

1. **Snapshot** — At draw time, all valid Raffle Passes are snapshotted
2. **Luck Weighting** — Each pass is weighted by the holder's current Luck Score
3. **VRF Request** — A Chainlink VRF request is submitted on-chain
4. **Random Selection** — The VRF response selects a weighted random winner
5. **Payout** — USDC is automatically sent to the winner's wallet
6. **Announcement** — Winner address and amount are published on-chain and in the UI

### Odds Calculation

Your odds of winning any given draw:

```
Your Odds = (Your Raffle Passes × Your Luck Multiplier) / 
            Sum of (All Passes × All Luck Multipliers)
```

**Example:**
- You hold 5 Raffle Passes with a Luck Multiplier of 3x (Gold tier)
- Your weighted entries: 5 × 3 = 15
- Total weighted entries in the draw: 1,000
- Your odds: 15 / 1,000 = **1.5%**

Compare this to someone with 5 passes but no staking (1x multiplier):
- Their weighted entries: 5 × 1 = 5
- Their odds: 5 / 1,000 = **0.5%**

> **Staking gives you 3x better odds in this example — without spending more on passes.**

## Jackpot Transparency

- Pot balance is **publicly visible** on-chain at all times
- A real-time counter on the JACPOT website shows the current pot size
- All draw transactions are verifiable on-chain
- Historical draws, winners, and amounts are displayed on the "Winner Wall"

## Smart Contract Details

- Jackpot contract is **non-upgradeable** after deployment
- No admin function can withdraw from the pot
- Draw execution is permissionless (anyone can trigger it after the scheduled time)
- Emergency pause function requires multi-sig approval (for critical bugs only)
