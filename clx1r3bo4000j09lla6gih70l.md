---
title: "The Complete Developer's Guide to EigenLayer's AVS"
datePublished: Wed Jun 05 2024 11:33:54 GMT+0000 (Coordinated Universal Time)
cuid: clx1r3bo4000j09lla6gih70l
slug: the-complete-developers-guide-to-eigenlayers-avs
tags: web3

---

If you've landed here you're probably curious about AVS (Actively Validated Services) and how it fits into the whole blockchain scene. Whether you're a seasoned blockchain developer or just getting your feet wet, this guide is here to walk you through everything you need to know about AVS.

We'll start with the basics – what an AVS is – and then explore its key components like operators, stakers, and smart contracts. From there, we'll dive into the details of how AVS works, including interaction flow and validation processes. Finally, we'll get hands-on and build a simple "Hello World" AVS together.

Before we get into AVS, let's talk about EigenLayer – the foundation that makes all this magic possible.

## What is EigenLayer

EigenLayer is a protocol built on Ethereum that introduces restaking, a new concept in crypto-economic security. At its core, EigenLayer consists of a series of smart contracts that allow users to "restake" their staked ETH or liquid staking tokens (LSTs) to bootstrap new proof-of-stake (PoS) networks and services within the Ethereum ecosystem in return for additional staking yield/rewards.

![EigenLayer: Bringing Ethereum-Level Trust to Middleware | by Jiawei | IOSG  Ventures | Medium](https://miro.medium.com/v2/resize:fit:1400/1*mTUDV71LQsQJWVvjWhLUyg.png align="center")

In simple terms, EigenLayer is like a multi-tool for the blockchain world. It allows you to take the security and validation power from one place and use it in many different ways. Whether it's for securing data, running new virtual machines, or connecting different blockchains, EigenLayer makes it easier and more efficient.

Alright, let's get to the heart of the matter – what exactly is an AVS?

## What is AVS

AVS stands for Actively Validated Services. It's a fancy term for a system that needs its own way of verifying data and transactions in a distributed manner. Think of it as a custom validator for all sorts of blockchain-related services.

![AVS Architecture Overview](https://docs.eigenlayer.xyz/assets/images/avs-architecture-v1-e6f15772a975b86e146bcec3d98c9042.png align="left")

You might be wondering what kinds of services we're talking about here. Well, AVS can be used for:

* **Sidechains**: These are like parallel blockchains that run alongside a main blockchain.
    
* **Data Availability Layers**: Systems ensuring data is accessible and secure.
    
* **New Virtual Machines**: Custom environments for executing smart contracts.
    
* **Keeper Networks**: Networks that manage tasks like liquidations and upkeep of certain protocols.
    
* **Oracle Networks**: Services that bring off-chain data to the blockchain.
    
* **Bridges**: Connect different blockchains to enable asset transfers.
    
* **Threshold Cryptography Schemes**: Advanced cryptographic methods for secure multi-party operations.
    
* **Trusted Execution Environments**: Secure areas in a main processor.
    

In a nutshell, an AVS is any system that needs its own unique way of validating information to make sure everything is legit and secure. Each AVS has its own set of smart contracts that handle things like which operators are running the service and how much stake is securing it.

Pretty cool, right? Now that we've got a handle on what an AVS is, let's dive into the key components that make it all work.

## Key Components of AVS

To understand how AVS works, we need to break it down into its core components: Operators, Stakers, and Smart Contracts. Each of these plays a crucial role in ensuring the system runs smoothly and securely.

### Operators

Operators are the backbone of AVS. They are responsible for running the off-chain client software specific to the AVSs they've opted into. Here's what they do:

* **Run Client Software**: Operators run specialized software that performs tasks required by the AVS. This could involve anything from computing data to verifying transactions.
    
* **Register with EigenLayer**: To become an operator, they must register with EigenLayer's DelegationManager contract. This registration is essential because it authorizes them to participate in the AVS.
    
* **Execute Tasks**: Once registered, operators listen for tasks emitted by AVS contracts, perform the required computations or validations, and submit their results back to the AVS.
    
* **Security Role**: Operators contribute to the security of the AVS by ensuring that tasks are completed accurately and reliably.
    

### Smart Contracts

Smart Contracts are the glue that holds everything together. They manage the logic and state of the AVS. Here’s how they function:

* **Core Logic**: Smart contracts define the rules and operations of the AVS. They handle everything from task generation to validation and reward distribution.
    
* **Interaction with Operators and Stakers**: They manage interactions between operators and stakers. For example, contracts handle operator registration, task assignment, result submission, and reward distribution.
    
* **State Management**: Each AVS has its own set of contracts that maintain the state relevant to its operation. This includes information about operators, stakers, and the tasks being processed.
    
* **Security and Reliability**: Smart contracts ensure that all operations are executed in a secure and predictable manner, reducing the risk of errors or malicious activities.
    

Together, these components create a robust system that allows AVS to operate efficiently and securely. Operators perform the necessary tasks, stakers provide the security, and smart contracts orchestrate the entire process.

## How AVS Works

To understand how AVS (Actively Validated Services) operates, it's crucial to break down the interaction flow and the validation process. These elements ensure that the AVS functions efficiently and securely.

### Interaction Flow

The interaction flow in an AVS involves sevral key steps that enable operators and smart contracts to work together seamlessly. Here’s a step-by-step look at how this process typically unfolds:

1. **Task Generation**: The AVS smart contract generates tasks that need validation or computation. These tasks could range from data verification to complex cryptographic calculations.
    
2. **Event Emission**: Once a task is created, the smart contract emits an event. This event signals that a new task is available for operators to pick up.
    
3. **Operator Listening**: Operators, who run the off-chain client software, listen for these events. They continuously monitor the AVS smart contracts for new tasks.
    
4. **Task Execution**: Upon detecying a new task, operators perform the required computation or validation off-chain. This could involve calculations, data processing, or verifying transactions.
    
5. **Result Submission**: After completing the task, operators submit their results back to the AVS smart contract. This submission includes proofs or signatures that validate the accuracy of their work.
    
6. **Aggregation (if needed)**: For tasks requiring consensus or multiple validations, an aggregation step may occur. Here, results from various operators are combined to form a single aggregated proof or signature.
    
7. **On-Chain Verification**: The AVS smart contract then verifies the submitted results. This involves checking the validity of proofs or signatures to ensure they meet the required criteria.
    
8. **Reward Distribution**: If the results are verified successfully, operators are rewarded for their work. Rewards are distributed according to predefined rules set by the AVS smart contract.
    

### Validation Process

The validation process is critical to ensuring the integrity and security of the AVS. Here’s how it typically works:

1. **Task Assignment**: Tasks are picked up by operators who have registered with EigenLayer's DelegationManager contract. This ensures that only authorized operators can participate.
    
2. **Proof Generation**: Operators perform the required validation or computation tasks and generate proofs. These proofs are cryptographic evidence that the task was completed correctly.
    
3. **Proof Submission**: Operators submit their proofs back to the AVS smart contract. The submission process is designed to be secure and tamper-proof.
    
4. **Consensus Mechanism**: In cases where multiple operators are involved, a consensus mechanism ensures that the majority agrees on the validity of the proof. This can involve techniques like BLS (Boneh-Lynn-Shacham) signature aggregation for efficiency.
    
5. **On-Chain Verification**: The AVS smart contract verifies the proofs on-chain. This involves checking the cryptographic signatures and ensuring that the results meet the criteria defined in the contract.
    
6. **Slashing (if necessary)**: If an operator submits an invalid proof or fails to complete the task, slashing conditions may apply. This means the operator could lose part of their staked assets as a penalty for non-compliance or malicious behavior.
    
7. **Finalization**: Once the proofs are verified, the task is considered complete. The AVS smart contract updates its state to reflect the successful validation, and operators are rewarded accordingly.
    

By following these steps, AVS ensures a secure and efficient process for validating tasks. This interaction flow and validation process are fundamental to maintaining the integrity and reliability of services built on the EigenLayer platform.

## Building Your First "Hello World" AVS

Alright, now that we've got a handle on what AVS is and how it works, let's roll up our sleeves and build our first "Hello World" AVS. This part is all about getting your hands dirty and seeing how it all comes together.

We'll use the [Hello World AVS repo](https://github.com/suhailkakar/hello-world-avs) as our starting point. Here's how you can clone the repo and get things set up.

### Prerequisites

Before we jump in, make sure you have these installed on your machine:

* Node.js and npm
    
* Foundry (Ethereum dev toolkit)
    
* Docker
    

#### Setting Up Your Development Environment

1. **Clone the Repo**  
    Open your terminal and run:
    
    ```plaintext
    git clone https://github.com/suhailkakar/hello-world-avs.git
    cd hello-world-avs
    ```
    
2. **Install Dependencies**  
    Run this to install the necessary dependencies:
    
    ```plaintext
    npm install
    ```
    
3. **Ensure Docker is Running**  
    Make sure Docker is installed and running.
    
4. **Start the Chain with Contracts Deployed**  
    Run this command to build the contracts, start an Anvil chain, deploy the contracts to it, and keep the chain running in your terminal:
    
    ```plaintext
    make start-chain-with-contracts-deployed
    ```
    
5. **Start the Operator** Open a new terminal tab and run:
    
    ```plaintext
    make start-operator
    ```
    
    This will compile the AVS software and start monitoring for new tasks.
    

### Understanding the Code

Let's break down the key parts of the repo and see what's going on under the hood.

1. **Contracts** The `contracts` folder has the Solidity smart contracts that define the AVS logic. Key contracts include:
    
    * `HelloWorldServiceManager.sol`: Manages the "Hello World" tasks and operator responses.
        
    * `ERC20Mock.sol`: A mock ERC20 token contract used for testing.
        
    
    Here's a peek inside `HelloWorldServiceManager.sol`:
    
    ```solidity
    pragma solidity ^0.8.9;
    
    import "@eigenlayer/contracts/libraries/BytesLib.sol";
    import "@eigenlayer/contracts/core/DelegationManager.sol";
    import "@eigenlayer-middleware/src/unaudited/ECDSAServiceManagerBase.sol";
    import "@eigenlayer-middleware/src/unaudited/ECDSAStakeRegistry.sol";
    import "@openzeppelin-upgrades/contracts/utils/cryptography/ECDSAUpgradeable.sol";
    import "@eigenlayer/contracts/permissions/Pausable.sol";
    import {IRegistryCoordinator} from "@eigenlayer-middleware/src/interfaces/IRegistryCoordinator.sol";
    import "./IHelloWorldServiceManager.sol";
    
    contract HelloWorldServiceManager is 
        ECDSAServiceManagerBase,
        IHelloWorldServiceManager,
        Pausable
    {
        using BytesLib for bytes;
        using ECDSAUpgradeable for bytes32;
    
        uint32 public latestTaskNum; // The latest task index
        mapping(uint32 => bytes32) public allTaskHashes; // mapping of task indices to all tasks hashes
        mapping(address => mapping(uint32 => bytes)) public allTaskResponses; // mapping of task indices to responses
    
        event NewTaskCreated(uint32 indexed taskIndex, Task task);
        event TaskResponded(uint32 indexed taskIndex, Task task, address operator);
    
        struct Task {
            string name;
            uint32 taskCreatedBlock;
        }
    
        modifier onlyOperator() {
            require(
                ECDSAStakeRegistry(stakeRegistry).operatorRegistered(msg.sender) == true, 
                "Operator must be the caller"
            );
            _;
        }
    
        constructor(
            address _avsDirectory,
            address _stakeRegistry,
            address _delegationManager
        )
            ECDSAServiceManagerBase(
                _avsDirectory,
                _stakeRegistry,
                address(0), // hello-world doesn't need to deal with payments
                _delegationManager
            )
        {}
    
        function createNewTask(string memory name) external {
            Task memory newTask = Task({
                name: name,
                taskCreatedBlock: uint32(block.number)
            });
            allTaskHashes[latestTaskNum] = keccak256(abi.encode(newTask));
            emit NewTaskCreated(latestTaskNum, newTask);
            latestTaskNum++;
        }
    
        function respondToTask(
            Task calldata task,
            uint32 referenceTaskIndex,
            bytes calldata signature
        ) external onlyOperator {
            require(
                operatorHasMinimumWeight(msg.sender),
                "Operator does not have the required weight"
            );
            require(
                keccak256(abi.encode(task)) == allTaskHashes[referenceTaskIndex],
                "supplied task does not match the one recorded in the contract"
            );
            require(
                allTaskResponses[msg.sender][referenceTaskIndex].length == 0,
                "Operator has already responded to the task"
            );
    
            bytes32 messageHash = keccak256(abi.encodePacked("Hello, ", task.name));
            bytes32 ethSignedMessageHash = messageHash.toEthSignedMessageHash();
            address signer = ethSignedMessageHash.recover(signature);
    
            require(signer == msg.sender, "Message signer is not operator");
            allTaskResponses[msg.sender][referenceTaskIndex] = signature;
    
            emit TaskResponded(referenceTaskIndex, task, msg.sender);
        }
    
        function operatorHasMinimumWeight(address operator) public view returns (bool) {
            return ECDSAStakeRegistry(stakeRegistry).getOperatorWeight(operator) >= ECDSAStakeRegistry(stakeRegistry).minimumWeight();
        }
    }
    ```
    
    * This contract does a few key things:
        
        * **Task Creation**: The `createNewTask` function lets anyone create a new task. It emits an event that operators can pick up.
            
        * **Task Response**: The `respondToTask` function is for operators to respond to tasks. It checks that the operator is legit and that the response is correct before recording it.
            
        * **Weight Check**: The `operatorHasMinimumWeight` function checks if an operator has enough stake to participate.
            
2. **Deployment Scripts** The `scripts` folder has scripts for deploying the contracts to the local blockchain. These scripts use Foundry to automate the deployment process.
    
    Example deployment script:
    
    ```solidity
    pragma solidity ^0.8.9;
    
    import {HelloWorldServiceManager} from "../src/HelloWorldServiceManager.sol";
    
    contract HelloWorldDeployer {
        HelloWorldServiceManager public helloWorldServiceManager;
    
        function run() external {
            // Deploy the HelloWorldServiceManager contract
            helloWorldServiceManager = new HelloWorldServiceManager(
                address(avsDirectory),
                address(stakeRegistry),
                address(delegationManager)
            );
    
            // Log the deployed contract address
            console.log("HelloWorldServiceManager deployed at:", address(helloWorldServiceManager));
        }
    }
    ```
    
    3. **Running the Show** Once you’ve got everything set up, it’s time to run the show. Here’s the basic flow:
        
        * The AVS consumer requests a "Hello World" message to be generated and signed.
            
        * The AVS picks up the request and emits an event for operators.
            
        * An operator takes the request, generates the message, and signs it.
            
        * The operator submits the signed message back to the AVS.
            
        * If everything checks out, the submission is accepted.
            
        
        This simple flow highlights the core mechanics of how AVSs work. You can get more sophisticated with different requests, operator coordination, and various security measures, but this "Hello World" example is a great place to start.
        

## **Conclusion**

That's all for this article. I hope you found it useful. If you need any help, feel free to leave a comment or send me a dm on [**Twitter**](https://twitter.com/SuhailKakar).

Let's connect on [**Twitter**](https://twitter.com/suhailkakar) and [**LinkedIn**](https://linkedin.com/in/suhailkakar/).

👋 Thanks for reading! See you next time.