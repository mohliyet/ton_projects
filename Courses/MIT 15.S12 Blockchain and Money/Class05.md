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

## Smart Contract Platforms

- **Ethereum (2015)**: With a market value of $22 billion in 2018, Ethereum is a decentralized, open-source blockchain that features smart contract functionality. It is the most actively used blockchain.

- **EOS (2018)**: EOS had a market value of $5 billion and completed a $4.2 billion year-long Initial Coin Offering (ICO) in July 2018. EOS.IO is a blockchain protocol powered by the native cryptocurrency EOS. The protocol emulates most of the attributes of a real computer including hardware.

- **NEO (2016)**: NEO, with a market value of $1.1 billion, is a blockchain platform and cryptocurrency designed to build a scalable network of decentralized applications. It uses a delegated Byzantine Fault Tolerance (dBFT) consensus mechanism and supports a wider range of programmable languages.

- **Ethereum Classic (2016)**: Ethereum Classic, valued at $1.1 billion, is a decentralized platform that runs smart contracts. It is a continuation of the original Ethereum blockchain - the classic version preserving untampered history; free from external interference and subjective tampering of transactions. It was created from the DAO hard fork.

- **LISK (2016)**: LISK, with a market value of $360 million, is a blockchain application platform and cryptocurrency. It offers an all-round solution for Node.js and JavaScript developers to deploy their own blockchain applications. It uses side chains and allows developers to code in JavaScript.

- **Stratis (2017)**: Stratis, valued at $150 million, is a powerful and flexible blockchain Development Platform designed for the needs of real-world financial services businesses and other organizations that want to develop, test and deploy applications on the blockchain.

## Potential Use Cases of Smart Contracts

Smart contracts have a wide range of potential applications across various industries. Here are some examples:

- **Digital Identity**: Smart contracts can be used to create and manage digital identities, providing a secure and immutable record of a person's identity.

- **Securities & Trade Finance**: In the financial industry, smart contracts can be used to automate the trading of securities and manage trade finance operations, reducing the need for intermediaries and increasing efficiency.

- **Derivatives & Financial Data**: Smart contracts can be used to create and manage financial derivatives, and to securely store and handle financial data.

- **Mortgages & Land Titles**: In the real estate industry, smart contracts can be used to automate the process of issuing mortgages and recording land titles, reducing the potential for fraud and making the process more efficient.

- **Supply Chain & Auto Insurance**: In the supply chain industry, smart contracts can be used to track goods as they move through the supply chain, providing a transparent and immutable record of their journey. This technology can also be applied to auto insurance, automating claims processing and reducing fraud.

- **Clinical Trials & Cancer Research**: In the healthcare industry, smart contracts can be used to manage clinical trials, ensuring that data is recorded accurately and transparently. This technology can also be used in cancer research, helping to manage and analyze large amounts of data.

## Decentralized Applications (DApps)

Decentralized Applications, also known as DApps, are applications that run on a decentralized blockchain network. Unlike traditional applications, which run on centralized servers, DApps leverage the power of blockchain technology to create a decentralized, secure, and transparent environment for executing code and processing transactions.

Key characteristics of DApps include:

- **Decentralization**: DApps run on a peer-to-peer network of computers rather than a single computer or server. This ensures that no single entity has control over the application, enhancing security and reliability.

- **Native Tokens**: DApps generally have a native token or cryptocurrency that is used for transactions within the application. These tokens can serve various purposes, such as incentivizing user participation or compensating network participants for their work.

- **Smart Contracts**: DApps typically run as a smart contract on top of a blockchain platform. A smart contract is a self-executing contract with the terms of the agreement directly written into code. This allows for automated, trustless transactions and eliminates the need for intermediaries.

- **Open Source**: Most DApps are open source, meaning their source code is publicly accessible. This promotes transparency and allows anyone to review, use, or modify the code.

- **Immutable**: Once data is recorded on the blockchain, it cannot be altered or deleted. This immutability provides a trustworthy and tamper-proof record of transactions.

- **Consensus Mechanisms**: DApps use consensus mechanisms such as Proof of Work (PoW) or Proof of Stake (PoS) to validate transactions and secure the network.

## Initial Coin Offerings (ICOs) - Crowdfunding for Investment and Consumption

- **Proceeds used to build networks**: The funds raised through an ICO are typically used to develop the proposed blockchain network or digital platform. This can include hiring developers, marketing the platform, and covering other operational costs.

- **Tokens usually issued prior to being functional**: In most ICOs, tokens are issued to investors before the underlying platform or network is fully developed or functional. These tokens often represent future access to a service or product that the network will offer.

- **Development, while open, is largely centralized**: Although the code for the blockchain network or platform is usually open-source, the development process is often centralized with a core team of developers making the key decisions.

- **Promoters allocate themselves 'premined' tokens**: In many ICOs, a portion of the tokens is 'premined', or created before the public sale, and allocated to the project's founders or developers. This can serve as a form of compensation or incentive for the team.

- **Tokens are fungible and transferable**: Tokens issued in an ICO are usually fungible, meaning each token is identical to every other token; they are interchangeable like coins of the same denomination. These tokens can be transferred between users within the platform's ecosystem.

- **Scarcity is fostered with preset 'Monetary policy'**: The total supply of tokens is often fixed or governed by a preset monetary policy. This creates scarcity, which can drive up the value of the tokens if the platform becomes popular or successful.

- **Purchasers anticipate profits through appreciation**: Investors in an ICO typically anticipate that the value of the tokens they purchase will increase over time. This expected appreciation is often a key motivation for participation in an ICO.

# Legal Issues - Contracts
- **Lecturer**: Larry Lessig

A contract is a legally binding agreement between two or more parties, which is enforceable by law. It involves a promise or performance given in exchange for a promise or performance. 

There are four key aspects discussed in the context of contracts:

1. **Performance for Performance**: This refers to the terms of the contract, which can be expressed or implied. Expressed terms are those that are explicitly stated and agreed upon by the parties involved. Implied terms, on the other hand, are not explicitly stated but are considered an integral part of the contract.

2. **Implied Terms by a Legal System**: The state or legal system has an interest in your contract. It cares about the kind of contract, its effect, the terms, and taxation. These factors can influence the enforcement and interpretation of the contract.

3. **Aim of the Contract**: The objective of a contract is not to eliminate risk but rather to allocate it. This means determining who will bear the risk if something goes wrong. Allocation matters whenever there is a system to process the breach of contract.

4. **Clarity**: While clarity is often sought in contracts, obscurity can also have value. For instance, parties may choose to leave certain terms vague to allow for flexibility in the future.

Understanding these aspects can help in the creation, interpretation, and enforcement of contracts. 

## Reading Assignment for Class06

The following reading materials will provide valuable insights into various aspects of blockchain technology:

1. **[Geneva Report Chapter 2 (pages 9 - 16)](../../Readings/The%20Geneva%20Report.pdf)**: Authored by Casey, Crane, Gensler, Johnson, and Narula, this chapter provides an in-depth analysis of blockchain technology and its potential impact on the financial industry.

2. **[On the Scalability of Blockchains](Readings/On the scalability of blockchains.pdf)**: This article discusses the challenges and potential solutions to scaling blockchain networks. It's a crucial read to understand the technical limitations of blockchains and how they can be overcome.

3. **[Transaction Speeds: How Do Cryptocurrencies Stack Up To Visa Or PayPal?](./path/to/TransactionSpeeds.pdf)**: Published on howmuch.net, this article compares the transaction speeds of various cryptocurrencies with traditional payment systems like Visa and PayPal.

4. **[Layer2 / The Lightning Network](./path/to/Layer2_LightningNetwork.pdf)**: This resource from the Digital Currency Initiative provides an overview of Layer 2 solutions, specifically focusing on the Lightning Network. These solutions aim to increase the transaction capacity of blockchain networks.

5. **[Top 8 Privacy Coins](./path/to/Top8PrivacyCoins.pdf)**: This article from Invest In Blockchain explores the top privacy-focused cryptocurrencies. It's a great resource to understand the importance of privacy in blockchain transactions and the different approaches taken by various cryptocurrencies.

6. **[On Sharding Blockchains](./path/to/ShardingBlockchains.pdf)**: This article from the Ethereum Wiki provides an introduction to sharding, a technique for improving the scalability of blockchain networks.

7. **[ZkLedger: Privacy Auditing for Distributed Ledgers](./path/to/ZkLedger.pdf)**: Authored by Narula, Vasquez, and Virza, this paper discusses ZkLedger, a framework that enables privacy-preserving auditing for distributed ledgers.

Please replace `./path/to/` with the actual path to your PDF files. Ensure you understand the key points from each reading as they will form the basis for our next class discussion.