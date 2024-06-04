# Class 03: Blockchain Basics and Consensus
- [Bitcoin Technical Features](#bitcoin-technical-features)
- [Decentralized Networks](#decentralized-networks)
- [Consensus Through Proof-of-Work](#consensus-through-proof-of-work)
- [Bitcoin Mining](#bitcoin-mining)
- [Native Currency](#native-currency)
- [Network](#network)
- [Other Consensus Protocols](#other-consensus-protocols)

## Bitcoin Technical Features Summary

### Cryptographic and Timestamped Logs
- Utilizes cryptographic hash functions for security. These functions transform input data into a fixed-size string of characters, which is a "digest" that is unique to each unique input.
- Employs timestamped append-only logs (blocks) for data integrity. Each block contains a timestamp and a link to the previous block, forming a chronological chain.
- Uses block headers and Merkle trees for efficient data verification. Block heclearaders contain metadata about the block, and Merkle trees allow for efficient and secure verification of large data structures.
- Applies asymmetric cryptography and digital signatures for transaction validation. This ensures that only the owner of a Bitcoin address can spend the bitcoins associated with it.
- Bitcoin addresses are used for transaction destinations. These addresses are derived from the public key of a public-private key pair.

### Decentralized Network Consensus
- Achieves consensus through the Proof-of-Work mechanism. This requires network participants (miners) to perform a certain amount of computational work to add new blocks to the blockchain.
- Bitcoin serves as the native currency within the network. It is used to reward miners for their work and to pay transaction fees.
- The network is decentralized, with no central authority. This means that no single entity has control over the entire network.

### Transaction Script and UTXO
- Transactions are composed of inputs and outputs. Inputs refer to the source of the bitcoins, and outputs refer to the destination.
- The Unspent Transaction Output (UTXO) set tracks spendable Bitcoins. Only the outputs of confirmed transactions that have not been spent can be included in the UTXO set.
- A scripting language is used to specify transaction conditions. This allows for a variety of transaction types, including multi-signature transactions and time-locked transactions.

Digital signatures guarding against tampering and impersonation.
## Decentralized Networks

### Byzantine Generals Problem
The Byzantine Generals Problem is a situation in distributed computing where components of a system must agree on a strategy to avoid catastrophic system failure, but some components may fail and give incorrect information. In the context of blockchain, this problem is analogous to nodes in the network deciding whether to validate a transaction (attack) or not (retreat).

### Blockchain
Blockchain is a type of decentralized network that is permissionless, meaning anyone can join and participate in the network. The security of a blockchain network is based on its consensus protocol and the use of a native currency.

### Hashcash and Proof-of-Work
In 1997, Adam Back proposed a system called Hashcash to address email spam and denial of service attacks. Hashcash introduced the concept of proof-of-work, which requires computational work to find a hash within a predetermined range. The difficulty of this task is defined by the number of leading zeros in the hash output. Despite the computational effort required to find a valid hash, the proof-of-work can be efficiently verified by other participants in the network.
## Consensus Through Proof-of-Work
Proof-of-Work (PoW) is a consensus algorithm used in blockchain technology. It requires network participants (miners) to perform a certain amount of computational work to add new blocks to the blockchain.

### Innovation - Chained PoW for Distributed Network Consensus and Timestamping
The use of PoW in blockchain is innovative because it allows for consensus and timestamping in a distributed network. Each block contains a timestamp and a link to the previous block, forming a chronological chain.

### Blockchain - Consensus Supports Longest Chain
In blockchain networks, the longest chain (i.e., the chain with the most proof-of-work) is considered the valid one. This rule helps to maintain consensus across the decentralized network.

### Stale Blocks
Stale blocks are blocks that were successfully mined but not included on the blockchain, often because another block at the same height was added first.

### Difference Between Bitcoin and Bitcoin Cash
Bitcoin and Bitcoin Cash are two different cryptocurrencies. Bitcoin Cash was created from a hard fork of Bitcoin in 2017 to increase the block size limit, allowing for more transactions to be processed per block.

### PoW Difficulty
The difficulty level in PoW adjusts approximately every two weeks (or every 2016 blocks) to maintain an average block generation time of 10 minutes. The difficulty is defined by the number of leading zeros required in the hash output. Currently, the hash output requires at least 19 leading zeros out of 64 hexadecimal characters.

### Recent Block
A recent block in the Bitcoin blockchain at height 846485 has the following hash: 0000000000000000000155d0146c733fffc9d6e33d88779e2832a0e836b75666.

### The Genesis Block
The first block in the Bitcoin blockchain (the "genesis block") has a hash that starts with a certain number of leading zeros. The exact number of leading zeros and the full hash can be found in the Bitcoin blockchain records.

### Difficulty Level Over Time
The difficulty level in PoW has changed significantly since 2009. In 2009, the difficulty level was 1. As of now, the difficulty level is much higher due to the increased computational power of the network. The exact current difficulty level can be found on various Bitcoin blockchain explorers.