# Class 03: Blockchain Basics and Consensus
- [Bitcoin Technical Features](#bitcoin-technical-features)
- [Decentralized Networks](#decentralized-networks)
- [Consensus Through Proof-of-Work](#consensus-through-proof-of-work)
- [Bitcoin Mining](#bitcoin-mining)
- [Native Currency and Economic Incentive Systems](#native-currency-and-economic-incentive-systems)
- [Network Participants in Blockchain](#network-participants-in-blockchain)
- [Other Consensus Protocols](#other-consensus-protocols)

## Bitcoin Technical Features

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
A recent block in the Bitcoin blockchain at height 846485 has the following hash: `0000000000000000000155d0146c733fffc9d6e33d88779e2832a0e836b75666`.

### The Genesis Block
The inaugural block of the Bitcoin blockchain, known as the "Genesis Block," possesses a unique hash:` 000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f`. This hash begins with a specific number of leading zeros, a characteristic that can be verified within the Bitcoin blockchain records. The Genesis Block holds a significant place in Bitcoin's history, marking the start of the decentralized cryptocurrency.

### Difficulty Level Over Time
The difficulty level in PoW has changed significantly since 2009. In 2009, the difficulty level was 1. As of now, the difficulty level is much higher due to the increased computational power of the network. The exact current difficulty level can be found on various Bitcoin blockchain explorers.

## Bitcoin Mining

Bitcoin mining has evolved significantly since its inception, with advancements in technology leading to increased hashing power.

### CPUs (2009 - 2010)
In the early days of Bitcoin, from 2009 to 2010, mining was primarily done using Central Processing Units (CPUs). These could perform between 2 to 20 million hashes per second (MH/s).

### GPUs (2010 - 2013)
As the network grew, miners started using Graphics Processing Units (GPUs) to increase their hashing power. From 2010 to 2013, a GPU could perform between 20 to 300 million hashes per second (MH/s).

### ASICs (2013 - 2018)
The introduction of Application Specific Integrated Circuits (ASICs) in 2013 marked a significant leap in mining technology. ASICs are hardware systems specifically designed for mining cryptocurrencies. They are much more efficient than CPUs and GPUs. From 2013 to 2018, an ASIC could perform between 4 to 16 tera hashes per second.

### Modern Mining Factories
Today, large-scale mining operations use thousands of ASICs to mine Bitcoin. These modern mining factories have enormous computational power and contribute significantly to the total hashing power of the Bitcoin network.

### Bitcoin Mining Hashrate Distribution
The distribution of Bitcoin's hashrate is an important aspect of the network's security. If too much hashing power is controlled by one entity, the network can become vulnerable to a 51% attack. To prevent this, miners often join mining pools, where they combine their hashing power and share the rewards. This leads to a more decentralized distribution of hashing power. The operators of these mining pools play a crucial role in maintaining the balance of power in the Bitcoin network.

## Native Currency and Economic Incentive Systems

Different blockchain networks have their own native currencies and economic incentive systems. The monetary policies of these networks can vary widely.

### Bitcoin (BTC)
Bitcoin, denoted as BTC, is created through a process known as mining. Each block mined adds new bitcoins to the network through a coinbase transaction. 

- The monetary policy of Bitcoin is encoded in the Bitcoin Core software. 
- Initially, the reward for mining a block was 50 bitcoins. 
- This reward halves approximately every four years (or every 210,000 blocks). This event is known as a "halving."
- In 2018, the block reward was 12.5 bitcoins, resulting in an inflation rate of approximately 4.1%.
- As of 2018, there were 17.3 million bitcoins in circulation. The total supply of bitcoins is capped at 21 million, which is expected to be reached around the year 2040.
- Bitcoin also has a market-based transaction fee mechanism. Miners can choose which transactions to include in a block based on the transaction fees offered.

### Ethereum (ETH)
Ethereum, denoted as ETH, also has its own native currency and monetary policy.

- In 2018, the reward for mining a block was 3 ETH, resulting in an inflation rate of approximately 7.4%.
- There was a proposal in November 2018 to reduce the block reward to 2 ETH.
- Transaction fees in Ethereum are paid in "gas." Each operation in a transaction requires a certain amount of gas, and the total gas cost is paid to the miner in ETH. As of 2018, 1 ETH was equivalent to 1 billion gas.

## Network Participants in Blockchain

In a blockchain network, there are several types of participants, each playing a unique role:

### Full Nodes
Full nodes are the most important players in the network. They store the entire blockchain and have the ability to validate all transactions. This means they keep a complete copy of the ledger, from the genesis block to the most recent one.

### Pruning Nodes
Pruning nodes also store the blockchain and validate transactions, but they prune (remove) old transactions that have been fully spent and are no longer needed. This helps to save storage space while still maintaining the integrity of the blockchain.

### Lightweight Nodes (SPV Nodes)
Simplified Payment Verification (SPV) nodes, also known as lightweight nodes, only store the headers of the blocks in the blockchain. They rely on full nodes to provide them with the rest of the block data when needed. This makes them more suitable for devices with limited storage capacity.

## 

### Miners
Miners are participants who perform Proof-of-Work (PoW) to create new blocks. They do not necessarily need to be full nodes. Miners compete to solve a mathematical problem, and the first one to solve it gets to add the next block to the blockchain and receive the block reward.

### Mining Pool Operators
Mining pool operators manage mining pools, which are groups of miners who combine their computational resources to increase their chances of mining a block. The block reward is then shared among the pool members.

### Wallets
Wallets are software applications that allow users to store, view, send, and receive transactions. They also create key pairs, which are used for signing transactions and proving ownership of funds.

### Mempool
The mempool is a pool of unconfirmed but validated transactions waiting to be included in a block. Miners select transactions from the mempool to include in the new block they are trying to mine. 

## Other Consensus Protocols

Blockchain technology has evolved to include a variety of consensus protocols beyond Proof-of-Work (PoW). These alternative protocols often involve the randomized or delegated selection of nodes to validate the next block, with additional mechanisms to confirm the validators' work.

### Randomized Selection Protocols

Randomized selection may be based on several factors:

- **Proof-of-Stake (PoS):** In PoS, the next block validator is chosen based on their stake in the native currency of the blockchain. The more currency a node holds, the higher the chance it has to be selected as the next block validator.

- **Proof-of-Activity (PoA):** PoA is a hybrid of PoW and PoS. It combines mining (as in PoW) with a randomized selection process (as in PoS) to select the next block validator.

- **Proof-of-Burn (PoB):** In PoB, nodes "burn" or permanently remove coins from circulation to get a chance to validate the next block. The idea is that by burning coins, nodes demonstrate their long-term commitment to the network.

- **Proof-of-Capacity (PoC):** PoC is based on the amount of storage space a node has. The more storage space a node can offer to the network, the higher the chance it has to be selected as the next block validator.

### Delegated Selection Protocols

Delegated selection may be based on a tiered system of nodes. In these systems, certain nodes have more authority or responsibility than others.

- **DASH:** DASH uses a hybrid consensus protocol that combines PoW with a tiered system of "masternodes." Masternodes are powerful nodes that perform special functions in the network and are rewarded for their work.

- **NEO:** NEO uses a delegated protocol of "professional nodes." These nodes are trusted entities in the network that have been delegated the responsibility of validating blocks.

Despite these alternatives, many major permissionless blockchain applications still use PoW due to its proven security and decentralization properties.