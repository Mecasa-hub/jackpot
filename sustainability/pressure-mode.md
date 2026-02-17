---
description: How JACPOT turns low trading volume into explosive jackpot events
---

# Pressure Mode

## The Problem It Solves

Every tax-token project faces the same existential threat: **low trading volume**. When volume drops:
- Tax revenue shrinks
- Jackpot grows slowly
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

1. **Jackpot draws are PAUSED** — No weekly or mini draws occur
2. **The pot keeps accumulating** — Tax revenue and pass sales still flow in
3. **A Pressure Gauge appears** on the UI — visual indicator showing the pot growing
4. **Community anticipation builds** — Social media buzz about the growing pot
5. **Drought Bonuses activate** — Treasury tops up the pot (see [Drought Bonuses](drought-bonuses.md))

### The Pressure Gauge

```
┌─────────────────────────────────────────┐
│         PRESSURE MODE ACTIVE            │
│                                         │
│  Jackpot: $127,450 USDC                │
│                                         │
│  ░░░░░░░░░░░░░░░████████  72%          │
│                                         │
│  Days in Pressure: 8 / 14              │
│  Mega Draw triggers in: 6 days         │
│  OR when volume recovers               │
│                                         │
│  🔥 Drought Bonus Active: +$2,500/day  │
└─────────────────────────────────────────┘
```

### Resolution: The Mega Draw

Pressure Mode ends in one of two ways:

#### Option A: Volume Recovery
- Daily volume returns above the threshold for 2 consecutive days
- Normal draw schedule resumes with the **accumulated mega pot**
- The first draw after recovery is a **Mega Draw** event

#### Option B: Maximum Timer
- If volume doesn't recover within **14 days**, a Mega Draw is **forced**
- This ensures the pot is always distributed within a reasonable timeframe
- After the forced Mega Draw, the cycle resets

## The Psychology

### Why Pressure Mode Creates Hype

| Traditional Project | JACPOT |
| --- | --- |
| Low volume → small rewards → users leave | Low volume → pot grows → anticipation builds |
| Silence during slow periods | "The pot is at $150K and counting!" |
| No reason to check the project | Daily Pressure Gauge updates create engagement |
| Death spiral | Mega Draw creates viral moment → volume spike |

### The Viral Loop

```
Low Volume → Pressure Mode Activates
    │
    ▼
Pot Grows Daily (Tax + Drought Bonus)
    │
    ▼
Community Posts: "Pot is at $XXK!"
    │
    ▼
New Users Discover Project
    │
    ▼
New Users Buy Tokens + Raffle Passes
    │
    ▼
Volume Increases → Pressure Mode Ends
    │
    ▼
MEGA DRAW → Winner Announced
    │
    ▼
"Someone just won $75K!" → Viral Moment
    │
    ▼
Massive Volume Spike → Cycle Resets
```

## Pressure Mode Parameters

| Parameter | Value | Governance |
| --- | --- | --- |
| Volume Threshold | 3% of 30-day MA | Diamond+ vote |
| Activation Delay | 3 consecutive days below threshold | Fixed |
| Maximum Duration | 14 days | Diamond+ vote |
| Recovery Confirmation | 2 consecutive days above threshold | Fixed |
| Drought Bonus Rate | See [Drought Bonuses](drought-bonuses.md) | Diamond+ vote |

## Historical Pressure Events

Once live, this section will display:
- Date and duration of each Pressure Mode activation
- Pot size at activation vs. at Mega Draw
- Winner details and prize amount
- Volume before, during, and after each event

> Every Pressure Mode event becomes a **story** — and stories drive growth.
