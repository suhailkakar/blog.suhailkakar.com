---
title: "The Developer's Guide to Zero-Knowledge and zkSync Era ∎"
datePublished: Fri Feb 02 2024 15:59:41 GMT+0000 (Coordinated Universal Time)
cuid: cls4tzhzg000w09l7cn3v4ky2
slug: the-developers-guide-to-zero-knowledge-and-zksync-era
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1706888924661/18d2b27e-661f-4894-94be-4c74938fe933.png
tags: programming, web-development, web3

---

Imagine you're a magician with a secret trick, and you want to prove to your audience that you can perform the trick without revealing how it's done. This is the essence of Zero-Knowledge Proofs (zkPs) - a cryptographic concept that allows one entity to prove to another that a statement is true, without giving away any information other than the veracity of the statement itself.

zkPs was first introduced in a 1985 paper by Shafi Goldwasser and Silvio Micali titled “The Knowledge Complexity of Interactive Proof-Systems.” The paper showcased the remarkable possibility of a prover convincing a verifier of the truth of a statement about a data point without spilling any additional information about the data itself. Zero-knowledge proofs can be interactive, requiring the prover to convince each verifier anew, or non-interactive, where a single proof suffices for verification by anyone in possession of it.

zkPs are like the secret ingredients in privacy-preserving technologies and blockchain scalability efforts. They're particularly quite useful in blockchain contexts, where they can validate transactions under a cloak of invisibility. This means you can confirm a transaction happened and is valid, without spilling the beans on the transaction's contents. It's like saying, "Trust me, the magic happened," and being able to prove it without showing your hand. This property is a game-changer for enhancing both privacy and security on the blockchain, ensuring that while transactions are transparent and verifiable, they're also confidential and secure.

At the heart of how zkPs operate, imagine a dance between a verifier and a prover. The verifier challenges the prover to execute a series of actions that only someone with knowledge of a secret could perform accurately. If the prover is merely guessing, the verifier's tests will likely expose the inaccuracies, affirming the proof's validity with a high probability. It's a choreographed performance where the prover's knowledge is the star of the show, yet the secret itself remains backstage, unseen.

![What is Zero Knowledge Proof and zkEVM | by Nufail.Eth | Medium](https://miro.medium.com/v2/resize:fit:800/1*IKlwtidbgDjIAsnWMoGcmg.png align="left")

## zkEVM - zkPs **role in smart contracts**

Imagine the Ethereum Virtual Machine (EVM) as a bustling city where all the smart contracts (which are like the city's citizens) live and work. Now, envision the zkEVM as a special kind of city, one that's cloaked in a layer of magic—this is the "zero-knowledge" part. The zkEVM is a special version of this city that's been upgraded to keep certain things secret while still letting everyone know that everything's running as it should.

### How does zkEVM work?

Glad you asked! The magic of the zkEVM lies in its ability to let smart contracts do their thing—whether that's moving digital money like Ethereum around, making decisions based on certain rules, or even creating unique digital collectibles—without spilling the beans/share more details of their transactions. It's like if you could vote on a new law in the city without having to tell anyone which way you voted. Everyone can see the law was passed fairly, but your vote remains your secret.

![Overview of how a zkEVM works.](https://assets-global.website-files.com/5f75fe1dce99248be5a892db/65675d8eff1c480b81c999ce_6552522be9152231644ce192_65244ac2003d8bac78f2c202_how-a-zkevm-works-1024x576.png align="left")

This secret-keeping is super important for keeping things efficient and private. Normally, the EVM has to show all its work, kind of like when a teacher asks you to show how you solved a math problem. But with zkEVM, it's like being able to prove you got the right answer without having to show every step of your work. This not only keeps your math secret but also saves a lot of space on the chalkboard.

Two main points to remember while working with zkEVMs are:

* **Privacy:** It keeps things under wraps. Just like how you might not want everyone knowing what you bought at the store, companies and individuals might not want all their blockchain transactions out in the open. zkEVM helps with that.
    
* **Scalability:** By not having to show all its work, the zkEVM can handle a lot more transactions at once. It's like being able to fit more people into our magical city without making it feel crowded.
    

## **zkSync** - Layer 2 scaling solution

zkSync is a Layer 2 scaling solution for Ethereum, designed to address two of the main challenges faced by blockchain technology today: scalability and high transaction fees. It uses a technology called zk-rollups to move the bulk of transaction processing off the main Ethereum chain (Layer 1) onto a parallel system (Layer 2), while still ensuring the security and integrity of transactions.

### How zkSync works:

* **zk-rollups:** At its core, zkSync utilizes zk-rollups, a type of rollup that uses zero-knowledge proofs to aggregate and verify transactions off-chain before submitting a single, compressed transaction to the Ethereum blockchain. This process significantly reduces the data needed to be processed by the Ethereum network, leading to faster transaction times and lower fees.
    
* **Zero-Knowledge Proofs:** The "zk" in zkSync stands for "zero-knowledge," the one we've talked a lot earlier - a cryptographic method that allows one party (the prover) to prove to another party (the verifier) that a statement is true without revealing any information beyond the validity of the statement itself. In the context of zkSync, this means transactions can be validated without exposing any details about the transactions themselves, enhancing privacy and security.
    
* **Smart Contracts and EVM Compatibility:** zkSync aims to be fully compatible with Ethereum smart contracts, meaning developers can deploy their existing Ethereum applications on zkSync with minimal changes. This compatibility is crucial for ensuring that zkSync can support a wide range of applications and use cases.
    

### **Advantages and Limitation of zkSync**

* **Scalability:** By processing transactions off-chain and aggregating them into a single transaction on-chain, zkSync can handle significantly more transactions than the Ethereum mainnet alone.
    
* **Lower Fees:** The efficiency of zk-rollups translates to lower transaction costs for users, making it more economical to execute transactions and interact with applications.
    
* **Security:** Despite off-chain processing, the security model of zkSync leverages the underlying security of the Ethereum mainnet, ensuring that assets and transactions are secure.
    
* **Privacy:** The use of zero-knowledge proofs provides a level of privacy for transactions, as the content of transactions is not directly exposed on the blockchain.
    
* **Complexity and Implementation Cost:** One of the primary challenges with zkSync is its heavy reliance on Zero-Knowledge Proofs (ZKPs). While ZKPs are groundbreaking for maintaining privacy and scalability, they are complex and expensive to implement. This complexity can present a steep learning curve for developers and might increase the upfront costs of developing and deploying applications on zkSync​​.
    
* **Withdrawal Speeds:** Users have faced slow speeds when withdrawing funds back to the Layer 1 (L1) Ethereum protocol. This is because users have to wait for their transactions to be finalized in a single batch, potentially leading to delays compared to direct Layer 1 transactions​​.
    
* **Computational Power for dApps:** Proving every transaction batch in zkSync requires significant computational power. This requirement can make decentralized applications (dApps) less common on ZK rollups due to the computational demands. Additionally, the issue of Ethereum Virtual Machine (EVM) compatibility also hinders the development and deployment of dApps on zkSync, as not all features and functions may be fully supported
    

> Though most of these limitations are pretty common among L2 and zkEVMs.

---

## Add zkSync to Metamask

In order to interact with any website built on zkSync or just to see our balance, we need to add zkSync into Metamask.  
  
Open up your Metamask wallet and click on the Network on the left hand side. click “Add Network" and scroll down the "Networks" menu and click on "Add a Network Manually".

Fill in the following details for the zkSync network:

#### zkSync Mainnet

* Network Name: `zkSync Era Mai`[`n`](https://docs.zksync.io/build/quick-start/add-zksync-to-metamask.html#sepolia-testnet-network-info)`net`
    
* RPC URL: [`https://mainnet.era.zksync.io`](https://mainnet.era.zksync.io)
    
* Chain ID: `32`[`4`](https://docs.zksync.io/build/quick-start/add-zksync-to-metamask.html#sepolia-testnet-network-info)
    
* Currency Symbol: `ETH`
    
* Block Explore[r](https://docs.zksync.io/build/quick-start/add-zksync-to-metamask.html#sepolia-testnet-network-info) URL: [`https://explorer.zksync.io/`](https://explorer.zksync.io/)
    

#### Sepolia testnet

* Network Name: `zkSync` [`E`](https://docs.zksync.io/build/quick-start/add-zksync-to-metamask.html#sepolia-testnet-network-info)`ra Sepolia Testnet`
    
* RPC URL: [`https://sepolia.era.zksync.dev`](https://sepolia.era.zksync.dev)
    
* Chain ID: `3`[`0`](https://docs.zksync.io/build/quick-start/add-zksync-to-metamask.html#sepolia-testnet-network-info)`0`
    
* Currency Symbol: `ETH`
    
* Block Explore[r](https://docs.zksync.io/build/quick-start/add-zksync-to-metamask.html#sepolia-testnet-network-info) URL: [`https://sepolia.explorer.zksync.io/`](https://sepolia.explorer.zksync.io/)
    

Click on "Save" to add the zkSync network to MetaMask.

## Building and Deploying on zkSync

Our journey begins with deploying a simple smart contract on the zkSync Era testnet. This basic contract will be capable of storing and updating a greeting message, serving as a foundational step to understanding smart contract development on zkSync.

Before diving into the deployment, ensure you have the following prerequisites ready:

* A development environment with Node.js installed.
    
* Either yarn or npm as package manager
    
* A private key from a wallet like MetaMask
    

### Step 1: Fund Your Wallet

To interact with the zkSync testnet, you'll need testnet ETH. You can obtain this through faucets or by bridging SepoliaETH to the zkSync Sepolia testnet using the zkSync bridge. You can check your balance on zkSync Sepolia explorer.

### Step 2: Create and Configure the Project

You can either use Atlas IDE for a quick setup or to manually create a project using `zksync-cli`. For the manual route, run `npx zksync-cli create hello-zksync` in your terminal, and select "Contracts" and "Hardhat + Solidity" when prompted. This will scaffold a new project with a predefined structure, including the smart contract you'll be working with, located in `/contracts/Greeter.sol`.

The contract, `Greeter.sol`, is a straightforward Solidity contract that includes functions to set and retrieve a greeting message. This simplicity makes it an ideal candidate for a first project on zkSync. You can learn more about this contract here

Next, compile the smart contract using `zksolc` for Solidity contracts. This prepares your contract for deployment by generating the necessary artifacts. Run `yarn compile` to compile your project.

### Step 3: Deploy and Verify the Contract

With your contract compiled, you're ready to deploy it to the zkSync Era testnet. The project includes a deployment script in `/deploy/deploy.ts` that simplifies this process. Run this script with `yarn deploy` to deploy your contract. The script also handles contract verification, allowing you to view your contract's source code on the zkSync block explorer.

After deployment, interact with your contract using the script located in `/deploy/interact.ts`. This script demonstrates how to read from and write to your smart contract on the blockchain. Run it with `yarn interact` to see the results of interacting with your contract in real-time.

## **Conclusion**

That's all for this article. I hope you found it useful. If you need any help, feel free to leave a comment or send me a dm on [**Twitter**](https://twitter.com/SuhailKakar).

Let's connect on [**Twitter**](https://twitter.com/suhailkakar) and [**LinkedIn**](https://linkedin.com/in/suhailkakar/).

👋 Thanks for reading! See you next time.##