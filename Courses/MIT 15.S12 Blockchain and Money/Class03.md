# Class 03: Blockchain Basics and Consensus
- [Bitcoin Technical Features](bitcoin-technical-features)
- [Consensus Through Proof-of-Work](#consensus-through-proof-of-work)
- [Bitcoin Mining](#bitcoin-mining)
- [Native Currency](#native-currency)
- [Network](#network)
- [Other Consensus Protocols](#other-consensus-protocols)

## Bitcoin Technical Features Summary

### Cryptographic and Timestamped Logs
- Utilizes cryptographic hash functions for security. These functions transform input data into a fixed-size string of characters, which is a "digest" that is unique to each unique input.
- Employs timestamped append-only logs (blocks) for data integrity. Each block contains a timestamp and a link to the previous block, forming a chronological chain.
- Uses block headers and Merkle trees for efficient data verification. Block headers contain metadata about the block, and Merkle trees allow for efficient and secure verification of large data structures.
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
<!-- # Consensus Through Proof-f-Work -->
