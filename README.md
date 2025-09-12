\# Welcome to your bounty repo  
This file contains information around how to set-up your README.md and prepare for our collaboration.

\*\*Bug Bounties use two repos\*\*:

\- a bug bounty repo (this one), which is used for scoping your bug bounty and for providing information to wardens  
\- a submissions repo, where issues are submitted

Ultimately, when we launch the bug bounty, this repo will be made public and will contain links to the in-scope files to be reviewed and all the information needed for bounty participants.

\*\*Action item for sponsors:\*\*

\- \[ \] Modify the contents of this README.md file. Describe how your code is supposed to work with links to any relevent documentation and any other criteria/details that the C4 Wardens should keep in mind when reviewing.

# 

# Blackhole Bug Bounty

| Risk Score | Payout |
| :---- | :---- |
| Critical |  $\[100,000 worth of $BLACK\] |
| High | $\[25,000 worth of $BLACK\]  |

Payouts are handled by the Blackhole Foundation directly and are denominated in USD. Payouts will be made in $BLACK calculated at the current exchange rate listed on Coingecko on the day of disbursement. 

The researcher must clearly demonstrate the vulnerability in the code without relying on any previously known issues, and must provide a fully functional proof of concept (PoC) to validate the finding. For all critical and high-severity vulnerabilities, submission of a working PoC is mandatory to qualify for a payout. 

## Background on Blackhole

Blackhole is a decentralized exchange (DEX) backed by the Avalanche Foundation. It is purpose-built to be the Liquidity and Trading Hub for all blockchain projects on Avalanche. By leveraging Avalanche’s highly scalable and low-latency infrastructure, Blackhole delivers rapid, cost-effective, and secure trading experiences-key advantages for DeFi users and protocols operating within the Avalanche ecosystem.

## What is Blackhole?

Drawing inspiration from DeFi trailblazers, Blackhole integrates:

* **Vote-escrowed token model** (inspired by Curve Finance)  
* **ve(3,3) model** (derived from Solidly, Aerodrome, and Velodrome)  
* **clAMM Pools** (Uniswap V3)  
* **Custom fees per pool** (Uniswap V4)

Yet, Blackhole takes it a step further by introducing fundamental enhancements to the vote-escrowed model by introducing two distinct veNFTs:

* **Singularity veNFT**: Empowers users to lock protocol tokens ranging from a week up to four years, mirroring Curve’s proven vote-escrow mechanism.  
* **Supermassive veNFT:** Introduces permanent token locking by burning tokens, removing them from the supply forever. Supermassives unlock powerful benefits:  
  1. Voting power that lasts: it never decays over time  
  2. Rebase Boost: extra 10% on your rebase rate  
  3. Extra 10% voting power boost

Participants can choose to either mint a Singularity veNFT with a flexible lock-up period of up to 4 years, or to mint a Supermassive NFT by reducing the token supply. The Supermassive veNFT sets Blackhole apart from other ve(3,3) protocols, where communities must rely on founders to repeatedly re-lock their team tokens every four years. With Blackhole, the team exclusively receives Supermassive veNFTs, tied to team tokens that are permanently burned and removed from circulation. This eliminates any need to trust the team’s future actions, as their tokens are verifiably gone forever by ensuring no future selling pressure is coming from the team. This bold mechanism aligns all stakeholders with the protocol’s long-term success, while the community can independently verify burned tokens on-chain. Trust nothing; verify everything.

Further solidifying its innovative edge, Blackhole introduces Genesis Pools, a novel feature designed to revolutionize pre-TGE liquidity seeding. This solution enhances the protocol’s foundation, offering capital efficiency and confidence for projects launching on Avalanche. Blackhole isn’t just a DEX, it’s a beacon of trustless innovation, built to empower and unite the DeFi ecosystem.

## How Does Blackhole Work?

* Protocol Design: [https://docs.blackhole.xyz/protocol-design](https://docs.blackhole.xyz/protocol-design)  
* Technical details: [https://docs.google.com/document/d/1iQyP3XjMiDiYE6YibP-QObtVZ3zyANLNDnvgOBPmnQc/edit?tab=t.v5ekfm7l18j4](https://docs.google.com/document/d/1iQyP3XjMiDiYE6YibP-QObtVZ3zyANLNDnvgOBPmnQc/edit?tab=t.v5ekfm7l18j4)  
* Blackhole Whitepaper[https://docs.blackhole.xyz/](https://docs.blackhole.xyz/)  
* Website: [https://blackhole.xyz](https://blackhole.xyz/)  
* Twitter: [https://x.com/BlackholeDex](https://x.com/BlackholeDex)  
* Discord: [https://discord.gg/blackholedex](https://discord.gg/blackholedex)

## Scope & Severity Criteria

### Severity

Critical \- Loss of user funds  
Severe \- Temporary denial of service, incorrect calculations,

The payout for smart contract vulnerabilities is based on the total value of funds at risk due to the reported issue. This is determined by the maximum value of funds held in the affected contract(s) at the time the report is submitted.

Payout ratios for critical and high severity bugs are awarded based on the total value at risk (TVL) in currently deployed contracts. Payout ratios are applied as follows:

* below $50,000,000 – 50% of the category bounty  
* $50,000,000 to $125,000,000 – 75% of the category bounty  
* Above $125,000,000 – 100% of the category bounty

### Smart Contracts in Scope

* AMM Pools  
  * Pair.sol  
  * PairFee.sol  
  * PairFactory.sol  
  * PairGenerator.sol   
  * RouterV2.sol  
  * RouterHelper.sol  
  * TokenHandler.sol  
* VE(3,3)  
  * GaugeManager.sol  
  * GaugeFactory.sol  
  * GaugeFactoryCL.sol  
  * GaugeExtraRewarder.sol  
  * GaugeOwner.sol  
  * GaugeV2.sol  
  * GaugeCL.sol  
  * MinterUpgrdeable.sol  
  * RewardsDistributor.sol  
  * VotingEscrow.sol  
  * VotingDelegationLib  
  * VotingBalanceLogicLib  
  * BribeFactoryV3.sol  
  * Bribes.sol  
  * VoterV3.sol  
  * VeArtProxy.sol  
* CL Implementation  
  * CustomPoolDeployer.sol   
  * AlgebraPoolApiStorage.sol   
* API Helper  
  * AlgebraPoolApi.sol  
  * BlackHolePairApiV2.sol  
  * GenesisPoolApi  
  * RewardApi  
  * TokenApi  
  * TradeHelper  
  * VeNFTApiV1  
* GenesisPool  
  * GenesisPoolManager.sol  
  * GenesisPoolFactory.sol  
  * GenesisPool.sol  
  * Interfaces  
* AVM   
  * AutoVotingEscrowManager.sol  
  * AutoVotingEscrow.sol  
  * SetterTopNPoolStrategy.sol   
  * SetterVoterWeightStrategy.sol   
  * FixedAuction.sol 

[https://github.com/BlackHoleDEX/Contracts](https://github.com/BlackHoleDEX/Contracts)

### Out-of-Scope

* VeNFTApi.sol  
* ChainLink  
  * AutomationBase.sol  
  * AutomationCompatible.sol  
  * AutomationCompatibleInterface.sol  
  * EpochController.sol  
* Governance:  
  * Governor.sol  
  * IGovernor.sol  
  * L2Governor.sol  
  * L2GovernorCountingSimple.sol  
  * L2GovernorVotes.sol  
  * L2GovernorVotesQuorumFraction.sol  
* Fan.sol  
* Thenian.sol  
* Interfaces:  
  * IUniswapV2Pair.sol  
  * IUniswapRouterETH  
  * IWrappedBribeFactory  
* BlackGovernor.sol  
* TradeHelper.sol

## Known Issues

Bug reports covering previously-discovered bugs listed below are not eligible for a reward within this program. This includes known issues that the project is aware of but has consciously decided not to “fix”, necessary code changes, or any implemented operational mitigating procedures that can lessen potential risk. Every issue opened in the repo, closed PRs, previous contests and audits are out of scope.

* Flawed getsmNFTPastVotes() Function Left Publicly Exposed  
  * When the timestamp is before first lock it returns the wrong value: Not an issue anymore as it's an unused variable.   
* VotingEscrow: delegateBySig():: **DOMAIN\_TYPEHASH** variable is wrong  
  * While defining variable it doesn’t consider the version but being used in the function.: Acknowledged.  
* GaugeCL.sol: getReward(uint256 tokenId, bool isBonusReward)::   
  * This function is not being used for claiming CL Pool’s emission. It has inherent flaw, when it calls **farmingCenter.claimReward** the msg.sender in farmingCenter contract will be GaugeCL which won't work as msg.sender should be user. So we’re using multiCall from the client directly to call FarmingCenter.ClaimReward.   
* GaugeFactoryCL.sol: createGauge:   
  * While creating Gauge for CL pool We’re transferring 10^-8 black which is not an issue as it can’t be exploited because of sufficient require statement to create Gauge


Additionally, any \*\*previously reported\*\* vulnerabilities mentioned in past audit reports are not eligible for a reward. See also: https://docs.blackhole.xyz/security

## Previous Audits

Previous audits can be found below: https://docs.blackhole.xyz/security

## Specific Types of Issues

The following are excluded from reward eligibility under this bug bounty program:

* Exploits already carried out by the reporter that have caused damage / loss of funds.  
* Vulnerabilities requiring access to leaked keys, credentials, or other sensitive secrets.  
* Vulnerabilities requiring access to privileged accounts or roles   
* Issues originating from third-party services outside our control (e.g., AWS, Cloudflare, etc).  
* Informational findings

Theoretical vulnerabilities which can be introduced by a trusted role in an upgradeable contract will be reviewed on a case-by-case basis as severe issues. Our philosophy is that only smart contracts that do not store or have access to anything of value should be upgradable. 

## Additional Context

### Trusted Roles Roles: [https://docs.google.com/document/d/1iQyP3XjMiDiYE6YibP-QObtVZ3zyANLNDnvgOBPmnQc/edit?tab=t.6rbnob5qq00t](https://docs.google.com/document/d/1iQyP3XjMiDiYE6YibP-QObtVZ3zyANLNDnvgOBPmnQc/edit?tab=t.6rbnob5qq00t)

Owner:[https://docs.google.com/document/d/1iQyP3XjMiDiYE6YibP-QObtVZ3zyANLNDnvgOBPmnQc/edit?tab=t.i4d1qm5kpy66](https://docs.google.com/document/d/1iQyP3XjMiDiYE6YibP-QObtVZ3zyANLNDnvgOBPmnQc/edit?tab=t.i4d1qm5kpy66)

### Miscellaneous

Employees of Blackhole and their family members are ineligible for bounties.  
