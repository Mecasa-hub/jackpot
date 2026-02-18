---
description: Simple on-chain raffle tickets — your entry to every daily draw
---

# Raffle Tickets

## Overview

Raffle tickets are **simple on-chain entries** that grant participation in VORTEX's daily draws. There are no NFTs, no complex mechanics — just buy a ticket and you're in.

> **Design Philosophy:** Raffle tickets are intentionally simple. The complexity and competitive advantage come from Luck Staking, not from the ticket itself.

## How Tickets Work

### Purchase

| Parameter | Value |
| --- | --- |
| **Currency** | USDC |
| **Price** | Fixed per ticket (set by protocol) |
| **Validity** | Current day's draw only |
| **Per-Wallet Cap** | Maximum tickets per wallet per day (anti-whale) |
| **Purchase Method** | On-chain transaction via VORTEX DApp |

### Ticket Lifecycle

```
Buy Ticket → Entered in Today's Draws → Draw Occurs → Ticket Expires
     │                                        │
     │                                        ├── Win → Claim Prize
     │                                        └── Lose → Ticket Consumed
     │
     └── Revenue → Treasury
```

- Tickets are **single-use** — each ticket is valid for one day's draws only
- Tickets are **non-transferable** — they cannot be sold or traded
- Unused tickets **expire at 00:00 UTC** if not entered in a draw
- All ticket revenue flows to the **Treasury** (not the Vortex Pot)

## Two-Tier Daily Draw

Every ticket purchased enters you into **both** daily draw tiers:

### Tier 1: Small Wins (Guaranteed Daily)

| Parameter | Value |
| --- | --- |
| **Winners Per Day** | 25 |
| **Funding** | 10% of daily ticket sales |
| **Selection** | Chainlink VRF (random, Luck-weighted) |
| **Claim Requirement** | Winner must share on X (Twitter) to claim |

Small Wins are distributed across four prize categories:

| Category | Winners | Share of Small Win Pool |
| --- | --- | --- |
| 🥇 **Top Prize** | 1 | 50% |
| 🥈 **Runner Up** | 4 | 35% |
| 🥉 **Lucky Pick** | 10 | 10% |
| 🎁 **Micro Win** | 10 | 5% |

### Tier 2: Vortex Draw (Conditional)

| Parameter | Value |
| --- | --- |
| **Winners** | 1 (if triggered) |
| **Funding** | 4% of the 5% buy/sell trading tax |
| **Trigger** | Internal protocol parameters met |
| **Selection** | Chainlink VRF (Luck-weighted) |

The Vortex draw only triggers when internal conditions are satisfied. If not triggered:
- **85%** of the pot rolls over to the next day (growing the vortex)
- **15%** is distributed to VORTEX token stakers as USDC rewards

## Luck-Weighted Selection

Tickets are **not equal**. Your Luck Score from staking multiplies the weight of each ticket:

```
Your Effective Entries = Tickets Purchased × Luck Score
```

### Example

| Player | Tickets | Luck Score | Effective Entries | Relative Odds |
| --- | --- | --- | --- | --- |
| Alice | 3 | 5,000 | 15,000 | 55.6% |
| Bob | 5 | 500 | 2,500 | 9.3% |
| Carol | 1 | 8,000 | 8,000 | 29.6% |
| Dave | 5 | 100 | 500 | 1.9% |
| Eve | 10 | 100 | 1,000 | 3.7% |

> **Key Insight:** Carol with 1 ticket and high Luck outperforms Bob and Dave with 5 tickets each. Luck Staking is the real competitive advantage.

## Revenue Flow

All ticket sale revenue flows to the **Treasury**, which allocates it as follows:

| Allocation | Percentage | Purpose |
| --- | --- | --- |
| 🎁 **Small Wins Pool** | 10% | Funds the 25 daily Small Win prizes |
| 🍀 **Staker Rewards** | 5% | USDC rewards distributed to VORTEX stakers |
| 🏦 **Treasury Reserve** | 5% | Operations, development, DeFi yield deployment |
| 📣 **Hype Vault** | Variable | Counter-cyclical marketing fund |

> **Important:** The Vortex Pot is funded by **4% of the 5% buy/sell trading tax** (the remaining 1% goes to the Team) — not by ticket sales. These are two independent revenue streams.

## Anti-Whale Protections

| Measure | Description |
| --- | --- |
| **Per-Wallet Daily Cap** | Maximum number of tickets any single wallet can purchase per day |
| **Luck Weighting** | Long-term small stakers can outperform short-term whales |
| **Tiered Draw Pools** | Some draws are exclusive to specific tiers, protecting smaller holders |
| **No Bulk Discounts** | Every ticket costs the same regardless of quantity |

## Claiming Prizes

### Small Wins
1. Winner is selected via Chainlink VRF
2. Winner receives notification in the DApp
3. Winner **must share their win on X (Twitter)** using the provided template
4. Upon verification of the post, prize is released to the winner's wallet
5. Unclaimed prizes (no X post within 48 hours) roll back into the Small Wins pool

### Vortex
1. Winner is selected via Chainlink VRF
2. Prize is automatically sent to the winner's wallet
3. No social sharing requirement for vortex wins (but encouraged)

## Key Takeaways

- ✅ **Simple on-chain tickets** — no NFTs, no complexity
- ✅ **Daily draws** — 25 guaranteed winners every day + conditional vortex
- ✅ **Luck-weighted** — staking gives you a massive competitive advantage
- ✅ **Anti-whale** — per-wallet caps and Luck weighting level the playing field
- ✅ **Viral marketing** — Small Win winners share on X to claim, driving organic growth
- ✅ **Transparent revenue** — ticket sales fund treasury; trading tax funds vortex
