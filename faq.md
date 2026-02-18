---
description: Frequently Asked Questions about JACPOT
---

# FAQ

## General

### What is JACPOT?
JACPOT is the first **Engage-to-Win** decentralized protocol on Base. It combines a gamified jackpot system, Luck Staking mechanics, and a sustainable treasury model to reward active participation with better odds of winning real prizes.

### What chain is JACPOT on?
JACPOT is deployed on **Base**, an Ethereum Layer 2 network. You'll need ETH on Base for gas fees and USDC on Base for purchasing raffle tickets.

### Is JACPOT a lottery?
JACPOT is a **DeFi protocol with gamified mechanics**. The jackpot system uses provably fair randomness (Chainlink VRF) and is fully transparent on-chain. Unlike traditional lotteries, JACPOT rewards long-term engagement through the Luck Staking system.

---

## Token & Tokenomics

### What is the total supply?
**1,000,000,000 (1 billion)** JACPOT tokens. The supply is fixed — no minting function exists.

### What is the buy/sell tax?
**5% on both buys and sells.** The tax is collected in USDC — **4% flows to the Jackpot Pot** and **1% goes to the Team**. The split is deployer-adjustable.

### Does staking mint new tokens?
**No.** JACPOT has zero inflation. Staking earns you **Luck** (a probability multiplier), not additional tokens. Your share of the total supply is never diluted.

### How does the token generate revenue?
Two independent streams:
- **Trading Tax (5%)** → 4% funds the Jackpot Pot, 1% goes to the Team
- **Raffle Ticket Sales (USDC)** → 100% flows to the Treasury for staker rewards, operations, and ecosystem growth

---

## Luck Staking

### What is Luck?
**Luck** is a non-transferable, non-tradeable on-chain score that accumulates when you stake JACPOT tokens. It directly multiplies your odds in every daily draw.

### How do I earn Luck?
- **Stake JACPOT tokens** — Luck accumulates based on amount staked × time × streak bonus
- **Complete daily missions** — Earn Luck Shards that boost your score
- **Claim Mystery Crates** — Random Luck Shard rewards daily
- **Maintain streaks** — Consecutive daily engagement multiplies shard earnings up to 3x

### What happens if I unstake?
Unstaking triggers a **50% Luck Decay penalty** — you immediately lose half your accumulated Luck Score. This is designed to reward long-term commitment.

### Can I buy or transfer Luck?
**No.** Luck is soulbound to your wallet and can only be earned through staking and engagement. It cannot be purchased, sold, or transferred.

---

## Raffle & Draws

### How do I enter the raffle?
Purchase **raffle tickets** with USDC through the JACPOT DApp. Each ticket enters you into that day's draws. Tickets are valid for the current day only.

### How often are draws held?
**Every day.** There are two tiers:
1. **Small Wins** — 25 guaranteed winners daily
2. **Jackpot Draw** — Conditional, triggers when internal protocol parameters are met

### How are winners selected?
All draws use **Chainlink VRF** (Verifiable Random Function) for provably fair, tamper-proof randomness. Winners are selected with **Luck-weighted probability** — higher Luck Scores mean better odds.

### What are the Small Wins?
25 winners are selected every day from all ticket holders. Prizes are distributed across four categories:
- 🥇 Top Prize (1 winner) — 50% of Small Win pool
- 🥈 Runner Up (4 winners) — 35%
- 🥉 Lucky Pick (10 winners) — 10%
- 🎁 Micro Win (10 winners) — 5%

### Do I need to share on X (Twitter) to claim?
**For Small Wins: Yes.** Winners must share a pre-filled post on X to claim their prize. This creates organic viral marketing. You have 48 hours to claim. **For Jackpot wins: No** — jackpot prizes are auto-claimed.

### What happens when nobody wins the jackpot?
- **85%** of the pot rolls over to the next day, making the jackpot bigger
- **15%** is distributed to JACPOT stakers as USDC rewards
- This means stakers earn even when there's no winner

### What is Pressure Mode?
When trading volume drops below a threshold for 3 consecutive days, **Pressure Mode** activates:
- Jackpot draws pause to let the pot accumulate
- Daily Small Wins continue as normal (25 winners daily)
- Treasury injects drought bonuses into the pot
- After 14 days, a **forced Mega Draw** guarantees a winner

---

## Daily Engagement

### What are Daily Missions?
Simple on-chain tasks that reset every 24 hours. Completing them earns Luck Shards and maintains your engagement streak. Examples: claim crate, check leaderboard, buy a ticket.

### What are Mystery Crates?
Daily claimable rewards available to all stakers. Each crate contains randomized rewards based on a tiered rarity system (Common → Legendary). Higher staking tiers get better crate odds.

### What are Luck Shards?
Non-transferable bonus points earned through daily engagement. They have dual utility:
- **Accumulate** them for a passive Luck Score multiplier (up to +20%)
- **Spend** them on tactical boosts (bonus tickets, Luck boosts, streak shields)

### What happens if I miss a day?
Your engagement streak resets to 0. You can purchase a **Streak Shield** (5,000 Luck Shards) to protect your streak for one missed day.

---

## Treasury & Sustainability

### Where does ticket revenue go?
100% of raffle ticket sales flow to the **Treasury**, which allocates funds to:
- 10% → Small Wins pool (daily prizes)
- 5% → Staker rewards (USDC)
- 5% → Development and operations
- 5% → Reserves
- 75% → DeFi yield deployment (Aave, Compound)

### How does the treasury generate yield?
Idle treasury funds are deployed into **on-chain DeFi strategies** (lending protocols like Aave and Compound) to generate sustainable yield. This provides a revenue floor even during zero-volume periods.

### What is the Hype Vault?
A self-healing marketing fund that saves during high-volume periods and automatically deploys marketing spend during low-volume periods. It ensures the protocol can always fund growth campaigns when they're needed most.

### Can the project survive low volume?
Yes. JACPOT has multiple sustainability layers:
- Jackpot pot rolls over and grows during low volume
- Treasury DeFi yield provides baseline revenue
- Pressure Mode builds anticipation for Mega Draws
- Hype Vault funds counter-cyclical marketing
- Daily Small Wins maintain engagement regardless of volume

---

## Security & Trust

### Is the randomness fair?
Yes. All draws use **Chainlink VRF**, which provides cryptographically verifiable randomness that cannot be manipulated by the team, miners, or any third party.

### Are the smart contracts audited?
Smart contract audits will be completed before mainnet launch. Audit reports will be published publicly.

### Can the team access the jackpot funds?
The Jackpot Pot is managed by smart contracts with transparent on-chain rules. Fund movements are publicly verifiable on the blockchain.

### Is the team doxxed?
Team information and vesting schedules are detailed in the [Supply Distribution](tokenomics/supply-distribution.md) section.
