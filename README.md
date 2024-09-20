# Turbin3 Solana Project 

This project demonstrates interaction with the Solana blockchain using a variety of scripts. Below is a detailed explanation of each file and its purpose, along with instructions on how to run them.

#### Final-Program Transaction

```
https://explorer.solana.com/tx/3DiWvgkQ2W2CfCqhFWLdwc86FjEtX2vqKALBENjEEQkrvL5hojFNLaEZzj3hJeTzJEFhim9LaUK4TEKyjakKfB7R?cluster=devnet
```

# Prerequisites
Before running the scripts, make sure you have the following installed:

```
Node.js
Yarn package manager
Solana CLI (for generating wallets)
```
Make sure you have cloned the project and run yarn to install the necessary dependencies.

# Files
Each file in the directory is explained below.
## 1. wba_prereq.ts
This file defines the configuration of the program and how it interacts with the Solana blockchain. It specifies the version, name, and address of the program using the WbaPrereq type. The instructions included (such as complete and update) outline the accounts and arguments required. It also includes account structures like Q2Prereq2024, error codes like InvalidGithubAccount, and various data types.

```
yarn wba_prereq
```

## 2. airdrop.ts
This script transfers 2 SOL to a specific wallet on the Solana devnet. It imports necessary modules like Connection, Keypair, and LAMPORTS_PER_SOL. The wallet’s private key is retrieved from the wallet JSON file, and a Keypair is generated. Using a Connection object, it connects to the Solana devnet and requests 2 SOL for the specified wallet through requestAirdrop.

```
yarn airdrop
```

## 3. enroll.ts
This script is used to send the complete instruction to a program on the Solana blockchain. It imports modules like Connection, Keypair, Program, and AnchorProvider. The IDL and WbaPrereq definitions are imported from the program description file. The script retrieves the private key from wallet.json and generates a Keypair. It then connects to the devnet and calculates the account address using findProgramAddressSync. Finally, it sends the complete instruction along with your Github data.

```
yarn enroll
```

## 4. keygen.ts
This script generates a new Solana wallet. It uses Keypair.generate() to create a new keypair and prints both the public and private keys to the console.

```
yarn keygen
```

## 5. transfer.ts
This script transfers SOL from one wallet to another. It imports necessary modules like Transaction, SystemProgram, Connection, Keypair, and sendAndConfirmTransaction. After determining the public key of the second wallet, it creates a transfer transaction, signs it, and publishes it on the Solana devnet.

```
yarn transfer
```

## 6. dev-wallet.json

This file contain byte arrays representing the secret keys for various Solana wallets used in this project. The secret keys are critical for accessing these wallets on the Solana blockchain.



# Result

```
//First Transaction
https://explorer.solana.com/tx/52T192Wk2DwTYZtouJFVn28Cpzou7gmjdTn4CZkxbwwfcHMbyqFLg5esPABV6QrkiQgoUgo7o55UvoKkCmFQoZMg?cluster=devnet
```

```
//Second-Transfer Transaction
https://explorer.solana.com/tx/29r7oqps8H1KFBRgTTtroHwjxoSZRYGqGhfE1nrst5SJq2JK8ZWCZ5dhC2YBoUE5P6tYT8UBGAP1uead27gGgmG4?cluster=devnet
```

