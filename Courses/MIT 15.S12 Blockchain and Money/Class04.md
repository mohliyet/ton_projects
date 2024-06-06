# Blockchain Basics and Transactions, UTXO and Script Code
- [Transaction Inputs and Outputs](#transaction-inputs-and-outputs)
- [Unspent Transactions Output (UTXO)](#unspent-transactions-output-utxo)
- [Scripting Language](#scripting-language)
- [Blockchain Design - Putting it All Together](#blockchain-design-putting-it-all-together)
- [Bitcoin's Academic Pedigree](#bitcoins-academic-pedigree)

## Transaction Inputs and Outputs

Bitcoin transactions consist of inputs and outputs. Here's a more detailed explanation:

- **Transaction Format:** Every Bitcoin transaction has a specific format that includes inputs and outputs.

- **Inputs:** Each input refers to a previous transaction's output. It includes the previous transaction's ID, an index, and a signature. The signature is generated using the private key associated with the previous transaction's output.

- **Outputs:** Each output includes a value (the amount of Bitcoin being transferred) and a public key, which is the Bitcoin address of the recipient.

- **Lock Time:** This is a parameter that can be set to indicate the earliest time or earliest block when the transaction can be added to the blockchain. If the lock time is not set (or set to zero), the transaction can be added to any block.

- **Turing Complete:** This term refers to a system capable of performing any computational task given enough resources. Bitcoin Script, the language used to write the conditions for spending bitcoins, is not Turing complete. It lacks certain features like loops, which is a design choice to avoid potential issues with infinite loops during transaction verification.

- **Multiple Inputs and Outputs:** A single Bitcoin transaction can have multiple inputs and outputs. This allows for more complex transactions, such as those involving multiple senders or recipients.

- **Coinbase Transaction:** This is a special type of transaction that's included in each new block. It's the transaction that rewards the miner for solving the proof-of-work puzzle. The input of a coinbase transaction is the block reward.

- **Block Reward Halving:** The block reward halves approximately every 210,000 blocks, which is roughly every four years. As of 2018, the block reward is 12.5 bitcoins. It started at 50 bitcoins per block when Bitcoin was first launched.

- **100 Block Maturity Rule:** The bitcoins earned from a coinbase transaction cannot be spent until 100 more blocks have been added to the blockchain. This is to ensure the stability of the block containing the coinbase transaction.
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