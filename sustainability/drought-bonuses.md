---
description: Treasury-funded jackpot top-ups that ensure the pot stays attractive during slow periods
---

# Drought Bonuses

## Purpose

Drought Bonuses are **treasury-funded injections** into the Jackpot Pot during low-volume periods. They ensure the pot remains attractive even when organic tax revenue is minimal.

## How They Work

### Activation

Drought Bonuses activate automatically when **Pressure Mode** is active (volume below threshold for 3+ days).

### Bonus Tiers

| Drought Duration | Daily Bonus | Source |
| --- | --- | --- |
| Days 1-3 | No bonus (monitoring period) | — |
| Days 4-7 | $500/day | Treasury yield allocation |
| Days 8-10 | $1,000/day | Treasury yield allocation |
| Days 11-14 | $2,500/day | Treasury yield + reserve |
| Day 14+ | Mega Draw forced | Full accumulated pot |

### Bonus Escalation Logic

The longer the drought, the more aggressive the treasury support:

```
Day 1-3:   Monitoring... no action
Day 4:     +$500  → Pot grows faster than organic alone
Day 5:     +$500  → Community notices pot acceleration
Day 6:     +$500  → "The pot is growing even without volume!"
Day 7:     +$500  → Social buzz increases
Day 8:     +$1,000 → Significant daily growth
Day 9:     +$1,000 → New users attracted by pot size
Day 10:    +$1,000 → Volume starting to recover?
Day 11:    +$2,500 → Aggressive push
Day 12:    +$2,500 → "Mega Draw in 2 days!"
Day 13:    +$2,500 → Maximum anticipation
Day 14:    MEGA DRAW TRIGGERED
```

### Total Drought Bonus (14-day cycle)

If a full 14-day Pressure Mode cycle plays out:

| Period | Days | Daily Rate | Subtotal |
| --- | --- | --- | --- |
| Monitoring | 3 | $0 | $0 |
| Tier 1 | 4 | $500 | $2,000 |
| Tier 2 | 3 | $1,000 | $3,000 |
| Tier 3 | 4 | $2,500 | $10,000 |
| **Total** | **14** | — | **$15,000** |

> The treasury contributes up to **$15,000 per drought cycle** to keep the pot attractive. This is funded by the 20% treasury yield allocation for Drought Bonuses.

## Sustainability

### Can the Treasury Afford This?

Drought Bonuses are funded by **treasury yield**, not principal:

- If treasury holds $1M in DeFi at 8% APY = ~$6,600/month yield
- 20% allocated to Drought Bonuses = ~$1,320/month
- A full 14-day drought costs $15,000 — this would require dipping into reserves
- However, full 14-day droughts should be **rare** — most resolve in 5-7 days

### Safety Mechanisms

| Mechanism | Purpose |
| --- | --- |
| **Maximum daily cap** | Prevents excessive treasury drain |
| **Reserve minimum** | Drought Bonuses pause if treasury reserve drops below threshold |
| **Governance override** | Diamond+ stakers can vote to adjust rates |
| **Automatic scaling** | Bonus rates scale with treasury size (larger treasury = larger bonuses) |

## Drought Bonus + Pressure Mode Synergy

The combination creates a powerful narrative:

1. Volume drops → Pressure Mode activates
2. Drought Bonuses start injecting funds → Pot grows faster than expected
3. Community sees pot growing despite low volume → "The protocol is healthy!"
4. Growing pot attracts attention → New users arrive
5. Volume recovers → Mega Draw → Viral moment
6. Cycle resets with more users than before

> Drought Bonuses are the **bridge** that carries the protocol through slow periods until organic growth returns.
