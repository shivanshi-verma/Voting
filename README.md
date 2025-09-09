# Decentralized Voting System

## 🚀 System Workflow

This project outlines a decentralized voting system built on an Ethereum Virtual Machine (EVM) compatible blockchain. The system's workflow is broken down into distinct phases, from election setup to result declaration.

### 🗳 Election Setup

The *admin* initiates the process by launching the system on a blockchain network. They then create a new election instance, filling in crucial details like election name and candidate information. This action effectively starts the election, making it live for voter participation.

### 📝 Voter Registration & Verification

Prospective voters connect to the same blockchain network and register themselves. During registration, their blockchain account address, name, and phone number are sent to the admin's verification panel. The admin reviews this information against their records. Upon successful verification, the admin approves the user, granting them the eligibility to vote.

### ✍ Casting Votes & Election Closure

Once approved, the voter can cast their vote for a preferred candidate from the voting page. The system ensures each eligible voter can only vote once. After a predetermined period, or when the admin decides, the election is officially ended. At this point, voting is closed, and the final results are displayed, with the winner prominently announced.

---

## 💻 Setting up the Development Environment

This section guides you through setting up the necessary tools and configuring the project for local development.

### 📋 Requirements

* *Node.js*: A JavaScript runtime environment.
* *Truffle*: A development framework for Ethereum.
* *Ganache (CLI)*: A personal Ethereum blockchain for development.
* *Metamask*: A browser extension that acts as a crypto wallet and gateway to blockchain applications.

### ⚙ Getting the Requirements

1.  *Node.js*: Download and install Node.js from the [official website](https://nodejs.org/).
2.  *Truffle & Ganache*: Open your terminal or command prompt and use the Node Package Manager (npm) to install Truffle and Ganache globally.
    bash
    npm install -g truffle
    npm install -g ganache-cli
    
3.  *Metamask*: Install the Metamask browser extension from the [official site](https://metamask.io/).

---

### 🛠 Configuring the Project

1.  *Clone the Repository*:
    bash
    git clone https://github.com/shivanshi-verma/Voting.git
    cd dVoting
    

2.  *Run the Local Blockchain*:
    Start the Ganache CLI. *Keep this terminal window open* as the blockchain network needs to be running for the entire development session.
    bash
    ganache-cli
    

3.  *Configure Metamask*:
    * Open Metamask in your browser.
    * Click on the network dropdown and select "Add Network."
    * Choose "Add a network manually."
    * Enter the following details:
        * *Network Name*: Ganache
        * *New RPC URL*: http://127.0.0.1:8545
        * *Chain ID*: 1337
    * Save the network.
    * Import accounts into Metamask by using the private keys provided by ganache-cli in your terminal.

4.  *Deploy Smart Contracts*:
    Navigate to the dVoting directory and use Truffle to deploy the smart contracts to your local Ganache network.
    bash
    truffle migrate
    
    * *Note*: Use truffle migrate --reset for re-deployments after making changes.

5.  *Launch the Frontend*:
    Navigate into the client directory, install the dependencies, and start the development server.
    bash
    cd client
    npm install
    npm start
    
    Your decentralized voting application is now running and ready for use!
