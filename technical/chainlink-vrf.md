---
description: How Chainlink VRF ensures provably fair randomness in all VORTEX draws
---

# Chainlink VRF Integration

## Why Chainlink VRF?

Fairness is **non-negotiable** for a raffle-based protocol. Users must trust that:
- The team cannot influence draw outcomes
- No one can predict or manipulate the random number
- Every draw result is verifiable on-chain

**Chainlink VRF (Verifiable Random Function)** is the industry standard for on-chain randomness. It provides:

| Feature | Benefit |
| --- | --- |
| **Cryptographic proof** | Every random number comes with a proof that it was generated fairly |
| **On-chain verification** | Anyone can verify the proof on-chain |
| **Tamper-proof** | Neither the oracle, the team, nor miners can manipulate the result |
| **Battle-tested** | Used by hundreds of protocols, billions in value secured |

## How It Works in VORTEX

### Vortex Draws

```
1. Draw time arrives (e.g., Friday 20:00 UTC)
   │
2. Anyone calls triggerDraw() on the Vortex Contract
   │
3. Vortex Contract snapshots all valid Raffle Passes
   │
4. Vortex Contract calls VRF Consumer → requestRandomWinner()
   │
5. VRF Consumer sends request to Chainlink VRF Coordinator
   │
6. Chainlink node generates random number + cryptographic proof
   │
7. Chainlink calls fulfillRandomWords() on VRF Consumer
   │
8. VRF Consumer forwards random number to Vortex Contract
   │
9. Vortex Contract uses random number to select weighted winner
   │
10. Winner is announced, prize distributed, passes burned
```

### Mystery Crates

Mystery Crate outcomes also use Chainlink VRF:

```
1. User calls claimDailyCrate() on Staking Contract
   │
2. Staking Contract requests random number from VRF Consumer
   │
3. Chainlink returns random number
   │
4. Random number determines crate rarity:
   │   0-59:    Common (60%)
   │   60-84:   Rare (25%)
   │   85-96:   Epic (12%)
   │   97-99.4: Legendary (2.5%)
   │   99.5+:   Mythic (0.5%)
   │
5. Reward distributed based on rarity
```

## VRF Configuration

| Parameter | Value | Rationale |
| --- | --- | --- |
| **VRF Version** | V2.5 | Latest version with improved gas efficiency |
| **Key Hash** | [CHAIN-specific] | Determines the Chainlink node used |
| **Confirmations** | 3 blocks | Balance between speed and security |
| **Callback Gas** | 500,000 (draws) / 200,000 (crates) | Sufficient for winner selection logic |
| **Subscription** | Funded by protocol | LINK tokens maintained by treasury |

## Verification

### How Users Can Verify Fairness

1. **Find the draw transaction** on the block explorer
2. **Locate the VRF request ID** in the transaction logs
3. **Find the fulfillment transaction** from Chainlink
4. **Verify the proof** — the cryptographic proof confirms the random number was generated from the request, not chosen by anyone
5. **Check the winner selection** — the weighted random selection algorithm is open-source and deterministic given the random number

### Verification Tools

- VORTEX will provide a **"Verify Draw" page** on the website
- Input any draw ID to see: VRF request, random number, proof, winner selection math
- All data sourced directly from on-chain events

## Cost

| Operation | Estimated VRF Cost |
| --- | --- |
| Daily Draw | ~0.5 LINK |
| Mini Draw | ~0.5 LINK |
| Monthly Mega Draw | ~0.5 LINK |
| Daily Mystery Crates (per user) | ~0.1 LINK |

VRF costs are funded by the protocol's Chainlink subscription, maintained by the treasury.

> For high-volume crate claims, the protocol may implement **batch VRF requests** — a single random number used to derive multiple crate outcomes, reducing cost significantly.

## Fallback Mechanism

In the unlikely event of Chainlink VRF downtime:

1. Draws are **postponed** (not cancelled)
2. The pot continues to accumulate
3. Once VRF is restored, the draw executes with the accumulated pot
4. No manual intervention is possible — the contract waits for VRF

> There is **no backdoor** for the team to execute draws without VRF. This is enforced at the smart contract level.
