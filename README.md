# Peer-to-Peer Blockchain Network Simulation
This is a peer-to-peer blockchain network implementation where multiple nodes operate independently. Each node maintains its own copy of the blockchain and processes transactions locally. Nodes communicate with each other to share blocks and register peers, forming a decentralized network. A consensus algorithm ensures that all nodes resolve conflicts and agree on a consistent and valid version of the chain.

## Main Features
1. Create and run multiple blockchain nodes
2. Add transactions through a web interface
3. Mine blocks with Proof of Work
4. Register peer nodes
5. Run consensus to resolve chain conflicts
6. View blocks and transactions visually in the browser
   
## Steps to run the code
1. Clone the repository
2. Install dependencies
   ```bash
   pip install flask requests
   ```
3. To start three blockchain nodes (peers), open three separate terminals and run the following commands:
    ```bash
    python node.py 5000
    ```
    ```bash
    python node.py 5001
    ```
    ```bash
    python node.py 5002
    ```
    Each node will run independently in their respective ports
## Workflow
**Step - 1: Register Peers -**
Use the "Register Node" form to connect nodes with each other.

**Step - 2: Add Transaction -**
Fill in sender, receiver, and amount → click "Add Transaction".

**Step - 3: Mine Block -**
Click "Mine" to add the transaction into the blockchain.

**Step - 4: Run Consensus -**
Click "Resolve Conflict" to sync chains with other peers.

**Step - 5: View Chain -**
See the chain and peers listed on the homepage.
## Demo video
<a href="https://www.youtube.com/watch?v=MoFDihKRCxE">
  <img src="https://i9.ytimg.com/vi/MoFDihKRCxE/maxresdefault.jpg?v=6873b4f7&sqp=CITszsMG&rs=AOn4CLBrW7tWvsLuA1fGQlf0YEQ1soH0rQ" width="400"/>
</a>

## Endpoints
**GET /chain** — Returns the full blockchain  
**POST /add_transaction** — Adds a new transaction  
**POST /mine** — Mines a new block  
**POST /register_node** — Registers a peer node  
**POST /consensus** — Resolves conflicts and syncs chains  
**GET /nodes** — Lists registered peers

## Key Concepts
1. The genesis block is the first block in the chain, created manually without a previous hash and used to initialize the blockchain.

2. Each node runs independently with its own blockchain and can add transactions, mine blocks, and sync with other nodes.

3. Mining uses a proof of work system where a valid hash must be found to add a block, ensuring security and difficulty.

4. The consensus algorithm helps nodes agree on the longest valid chain when conflicts occur between different copies of the blockchain.

5. Every block contains transaction data, a nonce, and a hash that links it to the previous block, forming a secure and verifiable chain.


