---
description: Security measures, audit plans, and risk mitigation strategies
---

# Security & Audits

## Security Philosophy

JACPOT follows a **defense-in-depth** approach to security:

1. **Minimize attack surface** — Simple contracts with minimal admin functions
2. **Immutability where possible** — Core contracts are non-upgradeable
3. **Multiple audits** — Independent audits from reputable firms
4. **Bug bounty** — Ongoing incentive for white-hat researchers
5. **Transparency** — All code open-source, all transactions on-chain

## Audit Plan

| Phase | Auditor | Scope | Status |
| --- | --- | --- | --- |
| **Pre-launch Audit 1** | TBD (Audit Firm 1) | All core contracts | Planned |
| **Pre-launch Audit 2** | TBD (Audit Firm 2) | All core contracts (independent) | Planned |
| **Post-launch Review** | TBD (Audit Firm 3) | Live deployment verification | Planned |
| **Ongoing** | Community + Bug Bounty | Continuous | Ongoing |

## Bug Bounty Program

JACPOT will launch a bug bounty program on Immunefi (e.g., Immunefi):

| Severity | Reward |
| --- | --- |
| **Critical** (fund loss) | Up to $50,000 |
| **High** (fund risk) | Up to $20,000 |
| **Medium** (functionality) | Up to $5,000 |
| **Low** (informational) | Up to $1,000 |

## Smart Contract Security Measures

### Token Contract

| Measure | Detail |
| --- | --- |
| **Ownership renounced** | After launch, no admin can modify token parameters |
| **No mint function** | Supply is fixed at deployment — cannot be inflated |
| **No pause function** | Token transfers cannot be paused by anyone |
| **No blacklist** | No ability to freeze individual wallets |
| **Max wallet limit** | Prevents single wallet from holding excessive supply |
| **Max transaction limit** | Prevents large single trades from manipulating price |

### Jackpot Contract

| Measure | Detail |
| --- | --- |
| **No admin withdrawal** | No function exists to withdraw pot funds manually |
| **Permissionless draws** | Anyone can trigger a draw after the scheduled time |
| **Emergency pause** | Multi-sig only, for critical bugs — pauses draws, not deposits |
| **Immutable distribution** | 50/35/10/5 split is hardcoded, cannot be changed |

### Staking Contract

| Measure | Detail |
| --- | --- |
| **No admin stake/unstake** | Only the user can manage their own stake |
| **Luck Score integrity** | Luck cannot be manually adjusted by anyone |
| **Proxy upgrades** | Only for Luck formula adjustments, governed by Diamond+ vote |
| **Timelock** | All proxy upgrades have a 48-hour timelock |

## Operational Security

### Multi-Sig Configuration

- Treasury: 3-of-5 multi-sig (Gnosis Safe)
- Emergency pause: 3-of-5 multi-sig
- All signers are publicly known (doxxed or reputable entities)
- No single point of failure

### Key Management

- Deployer keys are **burned** after contract deployment and renouncement
- Multi-sig keys are held by independent parties
- Hardware wallets required for all signers

### Monitoring

- Real-time monitoring of all contract interactions
- Automated alerts for unusual activity (large transactions, rapid state changes)
- 24/7 incident response team

## Known Risks & Mitigations

| Risk | Likelihood | Impact | Mitigation |
| --- | --- | --- | --- |
| Smart contract bug | Low | Critical | Multiple audits + bug bounty |
| Chainlink VRF failure | Very Low | Medium | Draw postponement (no fund loss) |
| Oracle manipulation | Very Low | High | Chainlink's decentralized oracle network |
| Flash loan attack | Low | Medium | Tax mechanism + snapshot-based draws |
| Front-running draws | Low | Low | VRF makes prediction impossible |
| Treasury DeFi exploit | Low | Medium | Diversified deployment + reserve buffer |
| Regulatory action | Medium | High | Legal structure + compliance review |

## Open Source

All JACPOT smart contracts will be:
- Published on GitHub under MIT
- Verified on block explorer (source code readable)
- Accompanied by comprehensive documentation
- Available for community review before mainnet deployment
