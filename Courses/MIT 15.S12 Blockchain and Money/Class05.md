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
| Cryptographic hash functions | Yes | Yes |
| Timestamped append-only logs (blocks) | Yes | Yes |
| Block headers and Merkle trees | Yes | Yes (more than one) |
| Asymmetric cryptography and digital signatures | Yes | Yes |
| Addresses | Yes | Yes |
| Decentralized Network Consensus | Yes | Yes |
| Proof of Work/Proof of Stake (needs more elaboration) | Yes | Yes |
| Native currency | Yes | Yes |
| Network | Yes | Yes |
| Transaction inputs and outputs | Yes | No (uses state transitions) |
| Unspent Transaction Output (UTXO) set | Yes | No (uses account-based model) |
| Script language for transactions | Yes | Yes (supports 7 languages) |