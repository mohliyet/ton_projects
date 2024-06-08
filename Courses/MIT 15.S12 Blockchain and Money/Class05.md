# Smart Contracts and DApps

1. [Smart Contracts](#smart-contracts)
2. [Blockchain Design with Smart Contracts](#blockchain-design-with-smart-contracts)
3. [DApps and Token Sales](#dapps-and-token-sales)
4. [Legal Issues of Smart Contracts](#legal-issues-of-smart-contracts)

Please review these sections before the class to familiarize yourself with the topics.

## Smart Contracts

Smart contracts were first proposed by Nick Szabo in 1996. He defined them as:

- "A set of promises, specified in digital form, including protocols within which the parties perform on these promises."

This definition can be broken down as follows:

- **A set of promises:** Smart contracts represent agreements between parties, just like traditional contracts. These agreements are made up of promises that each party commits to fulfill.

- **Specified in digital form:** Unlike traditional contracts, which are usually written in natural language, smart contracts are written in code. This code specifies the terms of the contract in a precise and unambiguous way.

- **Including protocols:** Smart contracts include protocols, or rules, that govern how the contract is executed. These protocols automate the execution of the contract, ensuring that the terms of the contract are fulfilled as soon as the conditions in the contract are met.

- **Within which the parties perform on these promises:** The parties to a smart contract fulfill their promises within the framework provided by the contract. The contract not only specifies the promises, but also enforces them.

However, it's important to note that despite their name, smart contracts may not always be "smart" or even legally recognized as contracts. The term "smart" refers to the automation of the contract, but the contract itself is only as good as the code it's written in. If the code is flawed, the contract could behave in unexpected ways. Furthermore, whether a smart contract is legally recognized as a contract can depend on the jurisdiction and the specific circumstances.

## Technical Features
| Technical Features | Bitcoin (BTC) | Ethereum (ETH) |
| --- | --- | --- |
| Cryptographic hash functions | Uses SHA-256 | Uses Keccak-256 |
| Timestamped append-only logs (blocks) | Yes | Yes |
| Block headers and Merkle trees | Single Merkle tree | Multiple Merkle trees (state, transactions, receipts) |
| Asymmetric cryptography and digital signatures | Uses ECDSA | Uses ECDSA and ED25519 |
| Addresses | Base58Check encoding | Hexadecimal (derived from the public key) |
| Decentralized Network Consensus | Proof of Work | Currently Proof of Work, transitioning to Proof of Stake |
| Native currency | Bitcoin (BTC) | Ether (ETH) |
| Network | Peer-to-peer | Peer-to-peer |
| Transaction inputs and outputs | Uses UTXO model | Uses account-based model |
| Unspent Transaction Output (UTXO) set | Yes | No |
| Script language for transactions | Bitcoin Script | Solidity, Vyper, and others |

## BTC vs ETH
- Founder: Satoshi Nakamoto - Vatalik Buterin 
- Genesis: January 2009 - July 2015
- Code: Non Turing (script) - Turing Complete (Solidity, Serpent, LLL,or Mutan)
- Ledger: UTXO-transaction - state-account based
 Merkle Trees: Transaction - Transactions, state, storage, receipts (w/nonces)
 - blocktime: 10min - 14 min
 - consensus: pow - pow 
 - hash function: sha 256 - ethash
 - currency: btc - eth 
 - mining: asic - gpu
 - hashrate: 54 exahash/s - 260 terahash/s
 - pre-sale: none - ico and prerelease of 72m eth