---
description: The engine that rewards loyalty with probability
---

# Luck Staking

## What is Luck Staking?

**Luck Staking** is JACPOT's revolutionary staking mechanism that rewards long-term holders with **increased winning probability** rather than inflationary token emissions.

When you stake JACPOT tokens, you accumulate a **Luck Score** — a non-transferable, non-tradeable on-chain metric that directly multiplies your odds in every daily draw.

> **Key Insight:** You can't buy Luck. You can only earn it through time and commitment.

## How It Works

### Staking Mechanics

1. **Deposit** JACPOT tokens into the Luck Staking contract
2. **Accumulate** Luck Score every block/epoch based on your staked amount
3. **Compound** your Luck through daily engagement (missions, crates, streaks)
4. **Multiply** your raffle odds proportionally to your Luck Score

### Luck Score Formula

```
Luck Score = (Staked Amount × Time Multiplier × Streak Bonus) + Luck Shards
```

| Component | Description |
| --- | --- |
| **Staked Amount** | Number of JACPOT tokens locked in the staking contract |
| **Time Multiplier** | Increases logarithmically with staking duration |
| **Streak Bonus** | Multiplier from consecutive daily engagement |
| **Luck Shards** | Bonus points earned from missions and crates |

### Time Multiplier Growth

| Duration Staked | Time Multiplier |
| --- | --- |
| 0–7 days | 1.0x |
| 1–4 weeks | 1.25x |
| 1–3 months | 1.5x |
| 3–6 months | 2.0x |
| 6–12 months | 2.5x |
| 12+ months | 3.0x (max) |

> The time multiplier uses a logarithmic curve — early staking provides the fastest growth, rewarding early adopters.

## Luck Decay (Unstaking Penalty)

To prevent "stake-and-dump" strategies, JACPOT implements a **50% Luck Decay** penalty:

- **Unstaking** any amount triggers an immediate **50% reduction** in your total Luck Score
- **Selling** tokens also triggers Luck Decay proportional to the sell amount
- Luck Score **cannot go negative** — minimum is always 0

### Why 50%?

The penalty is calibrated to:
- Make short-term speculation unprofitable (you lose months of accumulated Luck)
- Allow legitimate exits without total punishment (you keep 50%)
- Create a strong psychological incentive to hold through volatility

## Luck and Raffle Odds

Your Luck Score directly affects your probability of winning in every daily draw:

```
Your Win Probability = (Your Luck Score × Tickets Held) / Σ(All Participants' Luck × Tickets)
```

### Example Scenario

| Player | Luck Score | Tickets | Weighted Entries | Win Probability |
| --- | --- | --- | --- | --- |
| Alice (3 months staked) | 5,000 | 2 | 10,000 | 47.6% |
| Bob (1 week staked) | 500 | 5 | 2,500 | 11.9% |
| Carol (6 months staked) | 8,000 | 1 | 8,000 | 38.1% |
| Dave (no staking) | 100 (base) | 5 | 500 | 2.4% |

> **Notice:** Carol has better odds than Bob despite buying fewer tickets — her Luck Score from 6 months of staking gives her a massive advantage.

## Tier System Integration

Your Luck Score and staking duration determine your **Tier**, which unlocks progressive benefits:

| Tier | Requirement | Key Benefits |
| --- | --- | --- |
| 🥉 **Bronze** | Stake any amount | Basic draw entry, daily missions |
| 🥈 **Silver** | 10,000+ JACPOT staked, 30+ days | Better crate odds, streak bonuses |
| 🥇 **Gold** | 50,000+ JACPOT staked, 90+ days | Exclusive tier-only draws, priority support |
| 💎 **Diamond** | 200,000+ JACPOT staked, 180+ days | VIP draws, governance voting, premium crates |
| 👑 **Legendary** | 500,000+ JACPOT staked, 365+ days | Maximum multipliers, exclusive events, advisory role |

## Staking Strategies

### 🐢 The Long Game (Recommended)
- Stake early, stake consistently
- Complete daily missions for Luck Shards
- Never unstake — let your Time Multiplier compound
- **Best for:** Patient holders who want maximum odds over time

### ⚡ The Active Player
- Moderate stake with high daily engagement
- Focus on streak bonuses and mission completion
- Use Luck Shards strategically for multiplicative boosts
- **Best for:** Users who enjoy daily interaction

### 🎯 The Ticket Buyer
- Minimal or no staking
- Relies on ticket volume rather than Luck Score
- Lower odds per ticket but still eligible for all draws
- **Best for:** Casual participants who prefer simplicity

## Key Takeaways

- ✅ Luck Staking rewards **time and engagement**, not just capital
- ✅ **Zero inflation** — no new tokens are minted for staking rewards
- ✅ **50% Luck Decay** creates strong holding incentive
- ✅ Luck is **non-transferable** — it cannot be bought or sold
- ✅ Long-term stakers have a **compounding advantage** that grows over time
- ✅ Stakers earn **USDC rewards** from ticket sales and treasury yield
