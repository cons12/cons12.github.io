---
layout: post
title: "Week2: Notes on UCB MOOC: Intro to DeFi"
date: 2025-04-28 22:59:00 -0400
categories: Web3
tags: [Web3]
---

Thoughts: Lec1 - Lec4 in this course supplements the MIT Blockchain and Money course. While the MIT course is more conceptual and is good at 
emphasis on understanding the concept. This course is more detail oriented, with a lot more execution details.
I enjoy learning about basis of rollup technologies from session 2 for scaling blockchain, and writing and deploying my first Solidity
project in Session 4.

## Session 1: Introduction and Overview of DeFi

1. What is DeFi: 
   - Financial assets controlled by the user (non-custodial)
   - No one can single-handedly censor a transaction execution
   - No one can single-handedly censor a protocol execution
2. Flash loans: pools lend assets within one transaction, the assets are paid back by the end of the transaction, and interest is paid on the lent amounts.
3. Market manipulation:
   1. Wash trading: A form of market manipulation where the same trader (or colluding traders) simultaneously buys and sells a security to create a false appearance of market activity.
   2. Market cornering: Acquiring enough control of a particular asset or commodity so that the trader can manipulate the price.
   3. Bear raiding: A strategy where traders try to drive down the price of a stock by short selling and spreading negative rumors or sentiment.


## Session 2: Introduction to Blockchain Technology

1. Consensus layer -> Compute layer (blockchain computer) -> applications (DApps, smart contracts) -> user-facing tools (cloud servers)
2. Digital Signature:
   - Discrete-log signatures: Schnorr and ECDSA, short signatures (48 or 64 bytes) and public keys (32 bytes)
3. Scaling:
   - Bitcoin vs Ethereum vs Visa: 5 vs 20 vs 24,000 (Tx/sec)
   - Approaches:
     - Faster consensus: modern blockchains (Solana, Polkadot, Avalanche)
     - Payment Channels (e.g., Lightning), participants can only touch chain when a channel is created or closed.
     - Layer 2 approaches: zkRollup, Optimistic Rollup (Batch many transactions into a single Tx)
4. Rollups
   - Main tool: SNARK: Verifier’s run time is *much* less than running C
   - zk: a Rollup coordinator compresses a thousand Tx into one on-chain proof (SNARK) for verifiers, so verifiers don't have to verify each transaction individually.
   - optimistic: Coordinator posts Tx data on chain without a proof, if a posted Tx is invalid, anyone can submit a fraud proof and win a reward, Rollup server gets slashed.

5. Interoperability: Enable a user to move funds/assets to another system.
   Composability: Enable a DApp on one blockchain to call a DApp on another.


## Session 3: Introduction to Traditional Finance

- A financial system works well if: 
  - Goods are allocated to the people who value them the most. 
  - People willingly participate in the system.
- Properties of Financial Assets: 
  - Financial assets are composable ("Value Additivity")
  - How you divide/add up assets does not affect their value.
- Trading Venues: 13 Exchanges, 33 Equity ATS, OTC venues 
- Trading cost: spread = Ask - Bid
- DTCC: monopoly clearing house
- Payments: 3% of GDP in 2000. 
  - Interbank payments are settled through various wholesale platforms such as Fedwire, CHIPS; Use of these platforms includes a small nominal cost and implicit costs such as collateral requirements and daylight overdraft limits. 
  - Banks make loans that are partially backed by deposits; most of the money in circulation is privately created by commercial banks. (Fractional reserve banking)


## Session 4: Smart Contracts

- Smart contracts: neither smart nor contracts. Just programmable objects on blockchain.
- Dutch Auction: price only goes down over time, the first offer gets the bid.
- Difference between fungible and non-fungible: 
  - Non-fungible: each asset in a series has a distinct ID, attributes 
  - Fungible: the assets are interchangeable, can be summed up
- https://remix.ethereum.org/ - Playground for Solidity