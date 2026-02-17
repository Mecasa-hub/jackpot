---
description: Frequently asked questions about JACPOT
---

# FAQ

## General

### What is JACPOT?
JACPOT is the first Engage-to-Win DeFi protocol. It combines a gamified jackpot system, revolutionary Luck Staking mechanics, and a sustainable treasury model. The more you engage with the protocol, the better your odds of winning the jackpot.

### How is JACPOT different from other lottery/raffle protocols?
Unlike PoolTogether or similar protocols where odds are purely based on deposit size, JACPOT rewards **engagement**. Your odds are multiplied by your Luck Score, which grows through staking, daily missions, and streaks. Active participants have dramatically better odds than passive ones.

### Is JACPOT a gambling platform?
No. JACPOT is a DeFi protocol with gamified engagement mechanics. Raffle Passes are consumable NFTs, not gambling tickets. All outcomes are determined by Chainlink VRF (provably fair on-chain randomness). However, users should review the [Risks & Disclaimers](risks-and-disclaimers.md) and ensure compliance with local regulations.

### What chain is JACPOT on?
JACPOT is deployed on Base. We plan to expand to additional chains in Phase 6 of our roadmap.

---

## Token

### What is the JACPOT token?
JACPOT is the ERC-20 token at the center of the JACPOT ecosystem. It has a 5% buy tax and 5% sell tax, both collected in USDC and sent to the Jackpot Pot.

### Why is there a tax?
The tax is the primary funding mechanism for the jackpot. Every buy and sell contributes to the prize pool, creating a continuously growing pot that rewards the community.

### Is the tax always 5/5%?
Yes. The tax rate is hardcoded in the smart contract and cannot be changed after deployment. There are no hidden taxes or variable rates.

### Are wallet-to-wallet transfers taxed?
No. Only buys and sells on DEXs are taxed. Wallet-to-wallet transfers are tax-free.

### Can the team mint more tokens?
No. The total supply is fixed at deployment. There is no mint function in the contract. The supply can never be increased.

---

## Staking & Luck

### What is Luck?
Luck is a non-transferable, non-tradeable on-chain score that multiplies your odds in every raffle draw. It's earned through staking tokens, completing daily missions, and maintaining streaks.

### Do I earn tokens or USDC from staking?
No. Staking earns you **Luck**, not tokens or yield. This is intentional — it avoids inflationary emissions while giving stakers a powerful advantage in raffles.

### What happens if I unstake?
Unstaking triggers a **50% Luck Decay** — half of your accumulated Luck Score is instantly destroyed. This is designed to reward long-term commitment.

### Can I partially unstake?
Yes, but the 50% Luck penalty applies to your **total** Luck Score regardless of how much you unstake. This prevents gaming through gradual unstaking.

### What are Luck Shards?
Luck Shards are small additive bonuses to your Luck Score, earned through Daily Missions and Mystery Crates. They're non-transferable and permanent once earned.

### What are the Luck Tiers?

| Tier | Luck Required | Raffle Multiplier |
| --- | --- | --- |
| 🥉 Bronze | 100 | 1.2x |
| 🥈 Silver | 500 | 1.5x |
| 🥇 Gold | 2,000 | 2.0x |
| 💎 Diamond | 10,000 | 3.0x |
| 👑 Legendary | 50,000 | 5.0x |

### How long does it take to reach each tier?
It depends on how many tokens you stake and how consistently you engage. A rough guide:
- Bronze: 1-2 days
- Silver: 1-2 weeks
- Gold: 1-2 months
- Diamond: 3-6 months
- Legendary: 6-12+ months

---

## Raffle & Jackpot

### How do I enter the raffle?
Buy Raffle Passes from the dApp using USDC. Each pass gives you entries into the next draw, with your odds multiplied by your Luck Score.

### How much do Raffle Passes cost?

| Tier | Price | Entries |
| --- | --- | --- |
| Common | $5 | 1 |
| Rare | $20 | 5 |
| Epic | $75 | 20 |
| Legendary | $250 | 75 |
| Mythic | $1,000 | 350 |

### When are draws held?
- **Weekly Draw:** Every Friday at 20:00 UTC
- **Mini Draw:** Every Wednesday at 20:00 UTC (Silver+ tier only)
- **Monthly Mega Draw:** 1st of each month
- **Quarterly Championship:** Every 3 months

### How much does the winner get?
The winner receives **50% of the Jackpot Pot** in USDC, sent directly to their wallet. The remaining 50% is split: 35% rollover, 10% LP & buyback, 5% treasury.

### What if nobody wins?
100% of the pot rolls over to the next draw. The team never receives funds from a no-winner scenario.

### How do I know the draw is fair?
All draws use **Chainlink VRF** — a cryptographically provable random number generator. Every draw can be independently verified on-chain using the "Verify Draw" tool on the dApp.

### Are Raffle Passes reusable?
No. Passes are **burned** (consumed) after each draw. You need to buy new passes for each draw cycle.

### Can I trade Raffle Passes?
Yes. Raffle Passes are ERC-1155 NFTs and can be traded on secondary NFT marketplaces before the draw snapshot.

---

## Daily Engagement

### What are Daily Missions?
Three on-chain tasks generated daily for each staker. Complete them to earn Luck Shards. Complete all three for a "Perfect Day" bonus.

### What are Mystery Crates?
Daily claimable reward boxes for stakers. Contents range from Luck Shards to free Raffle Passes to small USDC rewards. Determined by Chainlink VRF.

### What is the Streak System?
Claiming your Mystery Crate on consecutive days builds a streak. Your streak multiplies your Luck accumulation rate, up to 2x at 30+ days. Missing a day resets your streak.

### What happens if I miss a day?
Your streak resets to 0, and your Streak Multiplier returns to 1.0x. Your Luck Score itself is preserved — only the multiplier resets.

---

## Treasury & Sustainability

### Where does the treasury money come from?
The treasury receives 5% of each jackpot distribution, plus 15% of the token supply (vested). It generates additional yield by deploying capital into DeFi protocols.

### What is the Hype Vault?
A dedicated marketing fund that saves during high-volume periods and automatically deploys marketing spend during low-volume periods. It's the protocol's self-healing immune system.

### What is Pressure Mode?
When trading volume drops below a threshold for 3+ days, Pressure Mode activates. Draws are paused, the pot accumulates, and Drought Bonuses kick in. It resolves with a Mega Draw when volume recovers or after 14 days.

### Can the team access the jackpot funds?
No. The Jackpot Contract has no admin withdrawal function. Funds can only be distributed through draws or the hardcoded allocation split.

---

## Security

### Are the contracts audited?
Yes. JACPOT undergoes multiple independent security audits before mainnet deployment. Audit reports will be published publicly.

### Is there a bug bounty?
Yes. A bug bounty program is live on Immunefi with rewards up to $50,000 for critical vulnerabilities.

### Can the team change the contracts?
The Token and Jackpot contracts are **non-upgradeable**. The Staking contract uses a proxy pattern for Luck formula adjustments only, governed by Diamond+ tier community vote with a 48-hour timelock.

### Is the team doxxed?
Team is KYC'd via a reputable verification service. Details available on the website.

---

## Getting Help

### Where can I get support?
- **Discord:** discord.gg/jacpot
- **Twitter/X:** x.com/jacpotprotocol
- **Telegram:** t.me/jacpotprotocol
- **Documentation:** You're reading it!

### I found a bug. What should I do?
If it's a **security vulnerability**, please report it through our bug bounty program on Immunefi. Do NOT disclose security issues publicly.

For **non-security bugs**, report them in the #bug-reports channel on Discord.

### How can I contribute?
Join our Discord community! We welcome:
- Feedback and suggestions
- Community content creation
- Translation help
- Beta testing participation
- Development contributions (open-source)
