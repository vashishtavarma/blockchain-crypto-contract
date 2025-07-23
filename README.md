# DextroChain & Dextrocoins

**DextroChain** is a decentralized blockchain application built with Python and Flask, simulating cryptocurrency transactions. **Dextrocoins ICO** is a smart contract in Solidity to manage the sale and tracking of Dextrocoins.

## Features

### DextroChain (Python/Flask)
- Blockchain creation, mining, and validation (see `Blockchain/blockchain.py`)
- Transaction support and decentralized node management (see `Cryptocurrency/dextrocoin.py`)
- RESTful API endpoints for mining, transactions, and chain management

### Dextrocoins ICO (Solidity)
- Max supply: 1,000,000 Dextrocoins
- Conversion: 1,000 Dextrocoins per USD invested
- Investment tracking and functions to buy/sell coins (see `SmartContract/code.txt`)

## Requirements

All Python dependencies are listed in `requirements.txt` using the `name==version` format. Example:
```
Flask==3.1.0
requests==2.32.3
```
Install them with:
```
pip install -r requirements.txt
```

## Project Structure

- `Blockchain/blockchain.py`: Minimal blockchain implementation with mining and validation logic.
- `Cryptocurrency/dextrocoin.py`: Full-featured blockchain with transaction pool, node network, and REST API.
- `Cryptocurrency/dextrocoin5001.py`, `dextrocoin5002.py`, `dextrocoin5003.py`: Instances for running nodes on different ports.
- `SmartContract/code.txt`: Solidity contract for Dextrocoins ICO.
- `requirements.txt`: Python dependencies.

## Running the Project

### 1. Python Blockchain & Cryptocurrency
- Run the blockchain node:
  ```
  python Blockchain/blockchain.py
  ```
- Run the cryptocurrency node (for each port/node):
  ```
  python Cryptocurrency/dextrocoin.py
  # or for multi-node:
  python Cryptocurrency/dextrocoin5001.py
  python Cryptocurrency/dextrocoin5002.py
  python Cryptocurrency/dextrocoin5003.py
  ```

### 2. Solidity Smart Contract
- Deploy `SmartContract/code.txt` using Remix IDE or any Solidity-compatible tool.
- Interact with contract functions: buy, sell, and view equity.

## Workflow
- All files and folders listed in `.gitignore` are excluded from documentation and version control.
- To update dependencies, modify `requirements.txt` in `name==version` format and re-install.
- Follow the structure above for running and extending the project.

---

For more details, see the code comments in each file or open an issue for help.
