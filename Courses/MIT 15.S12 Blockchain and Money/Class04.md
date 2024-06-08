# Blockchain Basics and Transactions, UTXO and Script Code
- [Transaction Inputs and Outputs](#transaction-inputs-and-outputs)
- [Unspent Transactions Output (UTXO)](#unspent-transactions-output-utxo)
- [Scripting Language](#scripting-language)
- [Blockchain Design - Putting it All Together](#blockchain-design-putting-it-all-together)
- [Bitcoin's Academic Pedigree](#bitcoins-academic-pedigree)

## Transaction Inputs and Outputs

Bitcoin transactions consist of inputs and outputs. Here's a more detailed explanation:

- **Transaction Format:** Every Bitcoin transaction has a specific format that includes inputs and outputs.

- **Coinbase:** The term "coinbase" refers to the first transaction in a block, also known as a coinbase transaction. This transaction is created by miners and includes the block reward (newly minted bitcoins) and any transaction fees from the transactions included in the block.

- **Inputs:** Each input refers to a previous transaction's output. It includes the previous transaction's ID, an index, and a signature. The signature is generated using the private key associated with the previous transaction's output.

- **Outputs:** Each output includes a value (the amount of Bitcoin being transferred) and a public key, which is the Bitcoin address of the recipient.

- **Lock Time:** This is a parameter that can be set to indicate the earliest time or earliest block when the transaction can be added to the blockchain. If the lock time is not set (or set to zero), the transaction can be added to any block.

- **Turing Complete:** This term refers to a system capable of performing any computational task given enough resources. Bitcoin Script, the language used to write the conditions for spending bitcoins, is not Turing complete. It lacks certain features like loops, which is a design choice to avoid potential issues with infinite loops during transaction verification.

- **Multiple Inputs and Outputs:** A single Bitcoin transaction can have multiple inputs and outputs. This allows for more complex transactions, such as those involving multiple senders or recipients.

- **Coinbase Transaction:** This is a special type of transaction that's included in each new block. It's the transaction that rewards the miner for solving the proof-of-work puzzle. The input of a coinbase transaction is the block reward.

- **Block Reward Halving:** The block reward halves approximately every 210,000 blocks, which is roughly every four years. As of 2018, the block reward is 12.5 bitcoins. It started at 50 bitcoins per block when Bitcoin was first launched.

- **100 Block Maturity Rule:** The bitcoins earned from a coinbase transaction cannot be spent until 100 more blocks have been added to the blockchain. This is to ensure the stability of the block containing the coinbase transaction.

- **Merkle Tree:** The coinbase transaction is recorded as the first transaction in the Merkle Tree, a data structure used to efficiently summarize all the transactions in a block.

- **Arbitrary Data:** The coinbase transaction may include up to 100 bytes of arbitrary data. This is often used for additional nonce values or to include messages. For example, the genesis block included a headline from The Times: `The Times 03/Jan/2009 Chancellor on brink of second bailout for banks`.

## Unspent Transaction Output (UTXO)

The Unspent Transaction Output (UTXO) model is a fundamental concept in Bitcoin's transaction management. Here's a more detailed explanation:

- **Definition:** UTXOs are the outputs of previous transactions that have not yet been spent. They are the "inputs" for new transactions.

- **UTXO Set:** The UTXO set contains all currently unspent transaction outputs. This set is crucial for validating new transactions. When a new transaction is made, it uses UTXOs as inputs, and these UTXOs are removed from the UTXO set.

- **Efficiency:** The UTXO model speeds up the transaction validation process. Instead of scanning the entire blockchain to find unspent outputs, one can simply check the UTXO set. This makes the transaction validation process more efficient.

- **Storage:** In Bitcoin Core, the UTXO set is stored using a LevelDB database called `chainstate`. This database is updated every time a block is added to the blockchain. It removes the UTXOs that were spent (used as inputs) in the transactions included in the block, and adds the outputs of these transactions as new UTXOs.

- **UTXO and Wallets:** Bitcoin wallets manage the UTXOs owned by their respective private keys. When you send bitcoins, your wallet selects UTXOs as inputs to create the transaction. The selection strategy can vary (e.g., some wallets select UTXOs to minimize transaction fees).

- **Change Addresses:** If the value of the UTXOs used as inputs exceeds the amount being sent in a transaction, the excess amount is sent back to the sender as "change" via a change address. This is similar to receiving change in a cash transaction. The change output becomes a new UTXO and can be used in future transactions.


## Bitcoin Script 

Bitcoin Script is the programming language used within the Bitcoin protocol to process transactions. Here are some key points about Bitcoin Script:

- **Stack-Based:** Bitcoin Script is a stack-based language, meaning it processes instructions in a last-in, first-out order. This is similar to other stack-based languages like Forth.

- **Not Turing-Complete:** Unlike most programming languages, Bitcoin Script is not Turing-complete. This means it doesn't have loops or complex flow control capabilities. This is a design choice to avoid potential issues with infinite loops during transaction verification.

- **Flexible Instructions:** Bitcoin Script provides a flexible set of instructions for transaction validation and signature authentication. This means it can handle a variety of different transaction types, not just simple transfers of bitcoin from one person to another.

Bitcoin transactions typically involve Unspent Transaction Outputs (UTXOs). Each UTXO contains a script, and these scripts typically fall into a few common types:

1. **Pay-to-PubkeyHash (P2PKH):** This is the most common type of transaction, making up 81% of all transactions. In a P2PKH transaction, the bitcoins are sent to the hash of the recipient's public key (which is represented by a Bitcoin address). The recipient can spend the bitcoins by providing a signature that corresponds to the public key.

2. **Pay-to-ScriptHash (P2SH):** This type of transaction makes up 18% of all transactions. In a P2SH transaction, the bitcoins are sent to the hash of a script. The recipient can spend the bitcoins by providing the original script along with the data that makes the script evaluate to true.

3. **M of N Multisig:** This type of transaction makes up 0.7% of all transactions. In a multisig transaction, the bitcoins can be spent if M out of N possible signatures are provided. This is often used for escrow or shared wallet services.

4. **Pay-to-Pubkey (P2PK):** This type of transaction makes up 0.1% of all transactions. In a P2PK transaction, the bitcoins are sent directly to a public key. The recipient can spend the bitcoins by providing a signature that corresponds to the public key.

## Preparation for Next Class

To prepare for the next class, please review the following materials. These readings will deepen your understanding of smart contracts, DApps, and alternative smart contract platforms:

1. **Smart Contracts: 12 Use Cases for Business and Beyond:** This document by the Chamber of Digital Commerce explores various applications of smart contracts in different industries. It discusses how smart contracts can be used to automate business processes, improve transparency, and reduce the risk of fraud.

2. **State of the DApps: 5 Observations from Usage Data:** This article by McCann analyzes usage data from decentralized applications (DApps) to draw insights about their performance, user behavior, and trends in the DApp market.

3. **Ethereum Competitors: Guide to the Alternative Smart Contract Platforms:** This guide by Blockonomi provides an overview of blockchain platforms other than Ethereum that support smart contracts. It compares their features, advantages, and disadvantages to help readers understand the landscape of smart contract platforms.

Please ensure you understand the key points from these materials before the next class, as they will form the basis of our discussion.