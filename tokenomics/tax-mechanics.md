---
description: How the 5/5% tax works under the hood
---

# Tax Mechanics

## How Tax Collection Works

The 5% buy/sell tax is split into two streams: **4% funds the Vortex Pot** and **1% goes to the Team**. This split is deployer-adjustable via the smart contract.

### Buy Tax (5%)
When a user buys VORTEX on a DEX:
1. The swap is executed through the VORTEX smart contract
2. 5% of the transaction value is calculated
3. This 5% is automatically swapped to **USDC** via the DEX router
4. **4%** of the USDC is sent to the **Vortex Pot**
5. **1%** of the USDC is sent to the **Team wallet**
6. The user receives 95% of the expected tokens

### Sell Tax (5%)
When a user sells VORTEX on a DEX:
1. The user initiates a sell of X tokens
2. 5% of the tokens are intercepted by the contract
3. These tokens are swapped to **USDC** via the DEX router
4. **4%** of the USDC is sent to the **Vortex Pot**
5. **1%** of the USDC is sent to the **Team wallet**
6. The remaining 95% of tokens are sold as normal

### Transfer Tax (0%)
Wallet-to-wallet transfers are **tax-free**. This allows:
- Moving tokens between personal wallets
- Sending tokens to friends
- Interacting with the staking contract without tax

## Tax Flow Diagram

```
User Buys VORTEX          User Sells VORTEX
       │                            │
       ▼                            ▼
   5% Tax (USDC)              5% Tax (USDC)
       │                            │
       └────────────┬───────────────┘
                    │
              ┌─────┴─────┐
              │           │
           4% (80%)    1% (20%)
              │           │
              ▼           ▼
     ┌──────────────┐  ┌──────────┐
     │  VORTEX POT  │  │   TEAM   │
     │  (Prize Pool) │  │  WALLET  │
     └──────┬───────┘  └──────────┘
            │
   ┌────────┴────────┐
   │                 │
Winner Drawn?     No Winner?
   │                 │
   ▼                 ▼
50% → Winner    15% → Stakers (USDC)
35% → Rollover  85% → Rollover
10% → LP/Buyback
 5% → Treasury
```

> **Important:** The 4/1 split between Vortex Pot and Team is **deployer-adjustable** via the smart contract. The default configuration directs 80% of tax revenue (4%) to the prize pool and 20% (1%) to the team.

## Tax Revenue Examples

| Daily Trading Volume | 5% Tax Collected | 4% → Vortex Pot | 1% → Team |
| --- | --- | --- | --- |
| $50,000 | $2,500 | +$2,000/day | $500/day |
| $100,000 | $5,000 | +$4,000/day | $1,000/day |
| $500,000 | $25,000 | +$20,000/day | $5,000/day |
| $1,000,000 | $50,000 | +$40,000/day | $10,000/day |
| $5,000,000 | $250,000 | +$200,000/day | $50,000/day |

> On days when no vortex winner is drawn, 85% of the pot rolls over and continues growing with the next day\u2019s tax revenue.

## Anti-Gaming Measures

| Measure | Purpose |
| --- | --- |
| **Minimum transaction size** | Prevents dust attacks that clog the swap mechanism |
| **Swap threshold** | Tax USDC is batched and swapped when accumulated amount hits threshold (reduces gas) |
| **Blacklist for contracts** | Prevents MEV bots from exploiting tax arbitrage |
| **Max wallet limit** | Prevents single wallet from accumulating excessive supply |
| **Max transaction limit** | Prevents large single trades from manipulating price |

## Tax Exemptions

The following addresses are exempt from tax:
- Staking contract
- Liquidity pool management
- Treasury operations
- Protocol-owned contracts

> Tax exemptions are hardcoded and cannot be modified post-deployment for security.
