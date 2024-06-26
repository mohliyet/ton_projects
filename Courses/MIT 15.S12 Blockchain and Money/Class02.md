# Blockchain Basics and Cryptocurrency
- [Bitcoin Design Features](#bitcoin-design-features)
- [Cryptographic Hash Functions](#cryptographic-hash-functions)
- [Timestamped Appended-only Logs](#timestamped-appended-only-logs)
- [Block Headers and Merkle Trees](#block-headers-and-merkle-trees)
- [Asymmetric Cryptography and Digital Signatures](#asymmetric-cryptography-and-digital-signatures)
- [Bitcoin Address](#bitcoin-address)

## Bitcoin Design Features

Bitcoin and its underlying blockchain technology have several key design features:

- **Blockchain technology**: A type of distributed ledger that maintains a list of records, called blocks, which are linked using cryptography. Each block contains a cryptographic hash of the previous block, a timestamp, and transaction data.

- **Timestamped append-only log**: A record of events, where new data is appended to the end of the log and existing data is not modified. This ensures the integrity and immutability of the data.

- **Auditable database secured by cryptography**: The blockchain is designed to be auditable, meaning that all transactions can be traced and verified. It is secured using cryptographic techniques, including hash functions for tamper resistance and integrity, and digital signatures for consent.

- **Network consensus protocol**: A method used to achieve agreement on a single data value among distributed processes or systems. Bitcoin uses a consensus protocol to address the cost of trust and solve the Byzantine Generals problem.

- **Permissioned and permissionless**: These terms refer to who can participate in the network. In a permissionless blockchain like Bitcoin, anyone can join the network, validate transactions, and create new blocks. In a permissioned blockchain, only authorized participants can do these things.

### Bitcoin - Technical Features

- **Cryptographic hash functions**: Used to ensure the integrity and security of data.
- **Timestamped append-only logs (blocks)**: Used to maintain a secure and verifiable record of all transactions.
- **Block headers and Merkle trees**: Used to structure the blockchain and efficiently verify transaction data.
- **Asymmetric cryptography and digital signatures**: Used to verify the authenticity of transactions.
- **Addresses**: Used to identify participants in transactions.
- **Consensus through proof-of-work**: Used to secure the network and validate new blocks.
- **Network nodes**: Used to maintain, secure, and operate the blockchain network.
- **Native currency**: Bitcoin has its own native currency, with a finite limit of 17 million bitcoins.
- **Transaction inputs and outputs**: Used to specify the sender and receiver of transactions.
- **Unspent transaction output (UTXO)**: A type of digital asset that can be created and consumed by transactions.
- **Scripting language**: Used to specify the conditions under which a transaction output can be spent.

## Cryptographic Hash Functions 

Cryptography is the practice and study of techniques for secure communication in the presence of adversaries. Examples of cryptography include the Scytale Cipher from ancient times, the Enigma Machine used during World War II, and Asymmetric Cryptography, which has been in use since 1976.

Hash functions, often referred to as "digital fingerprints for data", are a specific type of cryptographic tool. They have several key properties:

- They map an input of any size to an output of a fixed size, known as a `hash`.
- They are deterministic, meaning the same input will always produce the same hash.
- They can be computed efficiently, which is important for performance in many cryptographic applications.

### Cryptographic Properties

Hash functions have several key properties that make them useful for cryptography:

- **Preimage resistant (one way)**: It's computationally infeasible to determine x from hash(x).
- **Collision resistant**: It's computationally infeasible to find any two different inputs x and y where hash(x) = hash(y).
- **Avalanche effect**: A small change to the input x results in a significant change in the hash(x).
- **Puzzle friendliness**: Even if you know the hash(x) and part of x, it's still very hard to find the rest of x.

### Uses of Hash Functions

Hash functions have many uses in computer science and cryptography, including:

- **Names**: Hashes can be used as unique identifiers for data.
- **References**: Hashes can be used to verify the integrity of data.
- **Pointers**: Hashes can be used to locate data in a data structure.
- **Commitments**: Hashes can be used to commit to a specific value without revealing it.

### Bitcoin Hash Functions

Bitcoin uses hash functions in several ways:

- **Headers and Merkle trees**: Bitcoin uses the SHA-256 hash function to create block headers and Merkle trees.
- **Bitcoin addresses**: Bitcoin addresses are created using a combination of the SHA-256 and RIPEMD160 hash functions.

## Timestamped Appended-only Logs

In the Bitcoin blockchain, a timestamped append-only log is used to record all transactions. This log is immutable, meaning that once data is added, it cannot be changed or removed. This ensures the integrity and security of the data.
## Block Headers and Merkle Trees

Each block in the Bitcoin blockchain has a block header, which contains the following information:

- **Version**: The version number of the block.
- **Previous block hash**: A reference to the hash of the previous block in the blockchain. This links the blocks together in a chain.
- **Merkle root hash**: The root hash of a Merkle tree of all transactions included in the block. This allows for efficient and secure verification of transactions.
- **Timestamp**: The time when the block was created.
- **Difficulty target**: A measure of how difficult it is to find a new block compared to the easiest it can ever be. It is recalculated every 2016 blocks.
- **Nonce**: A random number that is used in Bitcoin's proof-of-work consensus algorithm. Miners change this value to try to find a hash for the new block that is below the difficulty target.

### Merkle Trees

A Merkle tree, also known as a binary hash tree, is a data structure used in computer science and cryptography. In the context of Bitcoin, it's used to efficiently summarize all the transactions in a block. The Merkle root is the hash of all the hashes of all the transactions in the block, and it's included in the block header. This allows anyone to verify a transaction without having to download the entire blockchain.

## Asymmetric Cryptography and Digital Signatures

Digital signature algorithms involve several steps:

- **Generate Key Pair**: A public key (pk) and private key (sk) are generated from a random number.
- **Signature**: A digital signature (sig) is created from a message (m) and the private key (sk).
- **Verification**: The validity of a signature (sig) is checked for a message (m) using the public key (pk).

Digital signatures have several key properties:

- It's computationally infeasible to find the private key (sk) from the public key (pk).
- All valid signatures verify.
- Signatures are computationally infeasible to forge.

### Bitcoin Digital Signature Function

Bitcoin uses the Elliptic Curve Digital Signature Algorithm (ECDSA) for its digital signatures. The equation y^2 = x^3 + 7 represents the elliptic curve used in Bitcoin's ECDSA.

### Bitcoin Addresses

Bitcoin addresses, which are derived from the public key, are used as the destination for Bitcoin transactions. (This topic needs more elaboration.)
