Simple Blockchain in Python

This is a basic blockchain implementation written in Python.
It demonstrates how transactions, blocks, proof-of-work (mining), and rewards work in a simplified blockchain system.

Features

Create transactions between users

Proof-of-Work mining (adjustable difficulty)

Mining rewards for miners

Genesis block creation

Balance checking for any address

Project Structure
blockchain.py   # Main blockchain implementation
README.md       # Project documentation

How It Works

Transactions are created and added to a pending pool.

Miners pick up pending transactions and create a block.

Each block is hashed using SHA-256 until it meets the difficulty requirement.

The block is added to the blockchain.

Miners receive a reward for successfully mining.

Demo Run
python blockchain.py


Sample Output:

Starting the miner...
Block mined: 000a5f....
Miner1 Balance: 0

Starting the miner again...
Block mined: 000c91....
Miner1 Balance: 50

Example Code
mycoin = Blockchain()

# Add some transactions
mycoin.add_transaction("Alice", "Bob", 100)
mycoin.add_transaction("Bob", "Charlie", 50)

print("Starting the miner...")
mycoin.mine_pending_transactions("Miner1")

print("Miner1 Balance:", mycoin.get_balance("Miner1"))

Requirements

Python 3.x

No external libraries (only built-in modules: hashlib, time, json)

Notes

This is a simplified blockchain for learning purposes only.

It does not include networking, signatures, or consensus algorithms like real blockchains (Bitcoin, Ethereum).

Difficulty and mining rewards can be adjusted in the Blockchain class.
