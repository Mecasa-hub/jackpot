---
description: How VORTEX turns low trading volume into explosive vortex events
---

# Pressure Mode

## The Problem It Solves

Every tax-token project faces the same existential threat: **low trading volume**. When volume drops:
- Tax revenue shrinks
- Vortex grows slowly
- Users lose interest
- Volume drops further
- Death spiral

**Pressure Mode turns this weakness into a feature.**

## How Pressure Mode Works

### Activation

Pressure Mode activates automatically when:
- Daily trading volume falls below the **Volume Threshold** for **3 consecutive days**
- The Volume Threshold is set at 3% of the 30-day moving average

### What Happens During Pressure Mode

1. **Vortex draws are PAUSED** — The conditional vortex check is suspended
2. **Daily Small Wins continue** — 25 winners are still selected every day (if tickets are sold)
3. **The pot keeps accumulating** — Tax revenue still flows in from every trade
4. **A Pressure Gauge appears** on the UI — visual indicator showing the pot growing
5. **Drought Bonuses activate** — Treasury injects funds into the pot daily (see [Drought Bonuses](drought-bonuses.md))
6. **Community anticipation builds** — Social media buzz about the growing pot

> **Key difference from normal days:** During Pressure Mode, the no-winner protocol does NOT activate either — no 15% staker distribution. 100% of the pot accumulates until the Mega Draw.

### The Pressure Gauge

```
┌─────────────────────────────────────────┐
│         🔥 PRESSURE MODE ACTIVE 🔥      │
│                                         │
│  Vortex Pot: $127,450 USDC             │
│                                         │
│  ░░░░░░░░░░░░░░░████████  72%          │
│                                         │
│  Days in Pressure: 8 / 14              │
│  Mega Draw triggers in: 6 days         │
│  OR when volume recovers               │
│                                         │
│  💰 Drought Bonus Active: +$2,500/day  │
│  🎁 Daily Small Wins: Still running!   │
└─────────────────────────────────────────┘
```

### What Keeps Running During Pressure Mode

| Feature | Status | Notes |
| --- | --- | --- |
| **Daily Small Wins** | ✅ Active | 25 winners daily, must share on X to claim |
| **Mystery Crates** | ✅ Active | Enhanced drop rates (2x during ORANGE+) |
| **Daily Missions** | ✅ Active | Bonus missions added |
| **Luck Staking** | ✅ Active | 3x Luck Shard earnings during RED tier |
| **Streak System** | ✅ Active | Users maintain streaks |
| **Vortex Draw** | ❌ Paused | Pot accumulates for Mega Draw |
| **No-Winner Distribution** | ❌ Paused | 100% stays in pot |

### Resolution: The Mega Draw

Pressure Mode ends in one of two ways:

#### Option A: Volume Recovery
- Daily volume returns above the threshold for 2 consecutive days
- The next day's vortex draw becomes a **Mega Draw** event
- The accumulated mega pot is distributed using the standard split:
  - 50% → Winner
  - 35% → Rollover
  - 10% → LP & Buyback
  - 5% → Treasury

#### Option B: Maximum Timer (14 Days)
- If volume doesn't recover within **14 days**, a Mega Draw is **forced**
- This ensures the pot is always distributed within a reasonable timeframe
- After the forced Mega Draw, the cycle resets

## Pressure Mode Example

```
Day 1-3: Volume drops below threshold
         Monitoring... Small Wins continue normally

Day 4:   PRESSURE MODE ACTIVATES
         Pot: $15,000
         Drought Bonus: +$500/day
         Small Wins: 25 winners from ticket sales
         Vortex: PAUSED (pot accumulates)

Day 7:   Pot: $15,000 + $2,000 tax + $2,000 drought = $19,000
         Drought Bonus escalates: +$1,000/day
         Community buzzing: "Pot almost at $20K!"

Day 10:  Pot: $25,000
         Drought Bonus escalates: +$2,500/day
         New users arriving attracted by pot size

Day 12:  Volume recovers! 2 consecutive days above threshold

Day 13:  🏆 MEGA DRAW
         Pot: $30,000
         Winner: $15,000 (50%)
         Rollover: $10,500 (35%)
         LP/Buyback: $3,000 (10%)
         Treasury: $1,500 (5%)

         Winner shares on social media → VIRAL MOMENT
         Volume spikes → Normal daily draws resume
```

## The Psychology

### Why Pressure Mode Creates Hype

| Traditional Project | VORTEX |
| --- | --- |
| Low volume → small rewards → users leave | Low volume → pot grows → anticipation builds |
| Silence during slow periods | "The pot is at $30K and counting!" |
| No reason to check the project | Daily Pressure Gauge updates + Small Wins keep users engaged |
| Death spiral | Mega Draw creates viral moment → volume spike |

### The Viral Loop

```
Low Volume → Pressure Mode Activates
    │
    ├── Small Wins continue (25 tweets/day from winners)
    │
    ▼
Pot Grows Daily (Tax + Drought Bonus)
    │
    ▼
Community Posts: "Mega pot is at $XXK!"
    │
    ▼
New Users Discover Project
    │
    ▼
New Users Buy Tokens + Tickets
    │
    ▼
Volume Increases → Pressure Mode Ends
    │
    ▼
MEGA DRAW → Winner Announced
    │
    ▼
"Someone just won $15K!" → Viral Moment
    │
    ▼
Massive Volume Spike → Normal Daily Draws Resume
```

## Pressure Mode Parameters

| Parameter | Value | Governance |
| --- | --- | --- |
| Volume Threshold | 3% of 30-day MA | Diamond+ vote |
| Activation Delay | 3 consecutive days below threshold | Fixed |
| Maximum Duration | 14 days | Diamond+ vote |
| Recovery Confirmation | 2 consecutive days above threshold | Fixed |
| Drought Bonus Rate | See [Drought Bonuses](drought-bonuses.md) | Diamond+ vote |
| Small Wins during Pressure | Always active | Fixed |

## Historical Pressure Events

Once live, this section will display:
- Date and duration of each Pressure Mode activation
- Pot size at activation vs. at Mega Draw
- Winner details and prize amount
- Volume before, during, and after each event
- Number of Small Win winners during the pressure period

> Every Pressure Mode event becomes a **story** — and stories drive growth.
