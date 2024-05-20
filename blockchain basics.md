# Blockchain Basics

## Distributed Ledger
A ledger is a record or a database that is shared across several nodes (computers) in a network. Each node maintains a copy of the ledger to prevent a single point of failure and all copies are updated and validated simultaneously. In the context of blockchain, this ledger is a record of transactions.

## Blocks
The "block" in blockchain refers to the list of transactions. These transactions are bundled into a block, which is then added to the chain of previous transactions.

## Linked Using Cryptography
Each block is linked to the one before it and after it through a process called hashing. This is a cryptographic process where a unique code (hash) is generated for each block based on its contents. This hash is stored in the next block, creating a link between the two. This ensures that the blocks remain in the correct sequence and that previous transactions cannot be tampered with.

## Cryptographic Hash of the Previous Block
Each block contains a unique code, known as a hash. This hash is created from the information in the previous block. If someone tries to alter the information, the hash will change, alerting the system to the tampering.

## Timestamp
Each block contains a timestamp when the block was created. This helps to maintain the order of transactions and blocks in the blockchain.

## Transaction Data
This is the actual data that is stored in the blocks. In the case of Bitcoin, this data is a record of the sender, receiver, and amount of coins. For other blockchains, it could be any type of data, such as contracts, records, or other information.

In summary, a blockchain is a chain of blocks, where each block contains a list of transactions. These blocks are linked using cryptographic hashes, ensuring the integrity and immutability of the data.