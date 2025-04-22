---
layout: post
title: "Week1: Notes on MIT OpenCourse: Blockchain and Money"
date: 2025-04-21 22:39:00 -0400
categories: Web3
tags: [Web3]
---

My purpose: Know basic concepts and be able to explain them well, understand how the current blockchain applications (2025)
fit into the money system and fit into 2018's blockchain visionary back then, and think about what other applications that blockchain could have an edge on.

## Session 1: Intro 

- Blockchain technology core: How do you move money peer to peer without a centralized Intermediary; Blockchain provides P2P alternative and solves cost of trust
- Role of Finance: Moving, Allocating, Pricing of money and risk throughout the economy
- Role of Money: store of value, scale of unit, medium of exchange
- Money is a social and economic construct

## Session 2: Money, Ledgers, and Bitcoin

- Ledger: principal records of accounts: economic activity, financial relationships
- Type of ledgers: 
  - Transaction vs. balance: e.g. bitcoin is transaction ledger, eth is balance ledger
  - General ledger vs. sub/supporting ledger: sub ledger is specialized for one category, e.g. salary, and sub ledger has more details. 
  - Single entry ledger vs. double entry book keeping
- Characteristics of good ledger: Immutable, Consistency/ Timestamped/ Ownership/ Accuracy/ Description of Transaction/ Comprehensive
- Payment system: A method to amend & record changes in ledgers for money
- Fiat Currency: 
  - Social & Economic Consensus
  - Represented by Central Bank Liabilities & Commercial Bank Deposits 
  - Relies upon System of Ledgers Integrated into Fractional Banking System 
  - Accepted for Taxes 
  - Notes & Coins are Legal Tender for All Debts Public & Private 
  - Unique Tax Treatment 
- Design of money: token vs. account based, physical vs. digital, private sector vs. central bank, widely accessible vs. wholesale


## Session 3: Blockchain Basics & Cryptography: 

- Blockchain technologies: 
  - Timestamped append-only log (compressed with index of Merkel Tree, making it searchable later)
- Secured through hash functions (Deterministic and efficiently computed, mapping input to fixed length output) & Digital signature (public private key cryptography, signature is generated from private key and message, but verifiable with public key and message)
- Bitcoin Address: determined by public key:
  - Private key ----(elliptic curve multiplication)---> public key ----(double hash, sha256 + ripemd160)---> public key hash -------(base58Check encode)-----> bitcoin address

## Session 4: Blockchain Basics & Consensus 

*000000000000000000012c1b3d30a308a6a23b440182940bf1e0d7000b2b81e8 (20/04/2025 - 12:11)*

(19 leading 0s)

- Decentralized Network Consensus
  - Consensus through Proof of Work
  - Native currency (Economic Incentive System)
  - Network (Full nodes, lightweight nodes, miners, wallets)

- How does bitcoin wallet address gets generated so making sure there's no collision: bitcoin uses 256 bit private key, after hashing and shrinking, it's 2^160 possible addresses.
  - It takes 2^80 ~= 1.2 ×10²⁴ hashes to have a collision (a)
  - NVIDIA RTX 4090 can do 1billion SHA-256 hashes/sec (b)
  - It takes a/b = 1.2 × 10^15 seconds ~= 38 million years for a NVIDIA RTX 4090 GPU to have a collision

## Session 5: Blockchain Basics and Transactions, UTXO, and Script Code

- Bitcoin technical feature part 3: Transaction Script and UTXO
  - Transaction Inputs & Outputs (inputs >= output, input - output = fee)
  - Unspent Transaction Output (UTXO) set
  - Scripts
- UTXO must be spent as a whole, they are stored in a nodes' local LevelDB instance. UTXO is analogous to a bill, I can only hand over 100$ bill, and get the exchange back or tip the exchange (miner fee).
- Coinbase transaction: the first transaction in a block, it is the reward giving back to the miner, it also uses a nonce.


## Session 6: Smart Contracts and Dapps

- Smart Contracts: A set of promises, specialized in digital form, including protocols, within which the parties perform on these promises. 
- Smart Contract Potential Use cases: Digital Identity, Securities, Derivatives, Mortgages, Supply Chain, Clinical Trials 

## Optional Readings

Some optional readings I find interesting and could come back to if I find time:

1. [NISTIR 8202: Blockchain Technology Overview](https://csrc.nist.gov/CSRC/media/Publications/nistir/8202/draft/documents/nistir8202-draft.pdf)
2. [MIT: How Blockchain Works](https://blockchain.mit.edu/how-blockchain-works/)
3. [A Short Guide to Blockchain Consensus Protocols](https://www.coindesk.com/markets/2017/03/04/a-short-guide-to-blockchain-consensus-protocols)
4. [Clark Paper: The Design Philosophy of the DARPA Internet Protocols](https://queue.acm.org/detail.cfm?id=3136559) (Recommended by Gary, read more than 6 times)
5. [Making Sense of Cryptoeconomics](https://www.coindesk.com/markets/2017/08/19/making-sense-of-cryptoeconomics)
6. [State of the DApps: 5 Observations from Usage Data (April 2018)](https://medium.com/@mccannatron/state-of-the-dapps-5-observations-from-usage-data-april-2018-a3e9da01bc22)
7. [Bitcoin Whitepaper](https://bitcoin.org/bitcoin.pdf)
8. [Ethereum Whitepaper](https://ethereum.org/en/whitepaper/)