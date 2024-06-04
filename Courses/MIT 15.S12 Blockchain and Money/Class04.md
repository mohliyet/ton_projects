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