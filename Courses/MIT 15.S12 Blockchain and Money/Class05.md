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
| Feature | Bitcoin (BTC) | Ethereum (ETH) |
| --- | --- | --- |
| Founder | Satoshi Nakamoto (Pseudonymous person or group) | Vitalik Buterin |
| Genesis (Launch Date) | January 2009 | July 2015 |
| Code | Non Turing (script) - Limited scripting language | Turing Complete (Solidity, Serpent, LLL, Mutan) - Supports complex programming |
| Ledger | UTXO-transaction - Uses Unspent Transaction Output model | State-account based - Uses an account model where the state (balance) of all accounts is stored |
| Merkle Trees | Transaction - Uses a single Merkle tree for transactions | Transactions, state, storage, receipts (w/nonces) - Uses multiple Merkle trees |
| Blocktime | 10 min - Average time to mine a block | Approximately 14 sec - Faster block times |
| Consensus | PoW (Proof of Work) - Miners solve complex mathematical problems | PoW (Proof of Work) - Transitioning to PoS (Proof of Stake) |
| Hash Function | SHA-256 - A cryptographic hash function | Ethash - A cryptographic hash function designed for Ethereum |
| Currency | BTC | ETH |
| Mining | ASIC (Application-Specific Integrated Circuit) - Specialized hardware | GPU (Graphics Processing Unit) - General purpose hardware |
| Hashrate | 54 exahash/s - Measure of computational power | 260 terahash/s - Measure of computational power |
| Pre-sale | None | ICO and pre-release of 72M ETH - Initial Coin Offering and pre-release of Ether |
| Rewards | 12.5 BTC/block - Reward for mining a block | 2 ETH/block (is the value still the same) - Reward for mining a block |
| Monetary Policy | Halves every 210,000 blocks (approximately every 4 years) - Decreasing supply over time | Fixed, but changes by updates (was 5/block: proposal to 2) - Supply determined by network updates |
| Fees | Voluntary - Transaction fees are optional but incentivize faster confirmation | Needed and market based - Transaction fees (gas) are required and vary based on network congestion |