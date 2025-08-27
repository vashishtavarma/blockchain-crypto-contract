# DextroChain & Dextrocoins

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

**DextroChain** is a decentralized blockchain application built with Python and Flask, simulating cryptocurrency transactions. **Dextrocoins ICO** is a smart contract in Solidity to manage the sale and tracking of Dextrocoins.

## 🚀 Features

### DextroChain (Python/Flask)
- ⛏️ Blockchain creation, mining, and validation
- 💰 Transaction support and decentralized node management  
- 🌐 RESTful API endpoints for mining, transactions, and chain management
- 🔗 Multi-node network synchronization
- ✅ Chain validation and consensus mechanism

### Dextrocoins ICO (Solidity)
- 🪙 Max supply: 1,000,000 Dextrocoins
- 💱 Conversion: 1,000 Dextrocoins per USD invested
- 📊 Investment tracking and functions to buy/sell coins
- 🔒 Secure smart contract implementation

## 📋 Requirements

- Python 3.8 or higher
- Flask web framework
- Git (for version control)

## 🛠️ Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd blockchain-crypto-contract
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## 📁 Project Structure

```
blockchain-crypto-contract/
├── Blockchain/
│   └── blockchain.py              # Basic blockchain implementation
├── Cryptocurrency/
│   ├── dextrocoin.py             # Main cryptocurrency node
│   ├── dextrocoin5001.py         # Node instance for port 5001
│   ├── dextrocoin5002.py         # Node instance for port 5002
│   └── dextrocoin5003.py         # Node instance for port 5003
├── SmartContract/
│   └── code.txt                  # Solidity ICO smart contract
├── requirements.txt              # Python dependencies
├── .gitignore                   # Git ignore rules
└── LICENSE                      # MIT License
```

## 🚀 Quick Start

### 1. Basic Blockchain
```bash
python Blockchain/blockchain.py
```
This starts a basic blockchain on `http://localhost:5000`

### 2. Cryptocurrency Network
For a single node:
```bash
python Cryptocurrency/dextrocoin.py
```

For a multi-node network:
```bash
# Terminal 1
python Cryptocurrency/dextrocoin5001.py

# Terminal 2  
python Cryptocurrency/dextrocoin5002.py

# Terminal 3
python Cryptocurrency/dextrocoin5003.py
```

### 3. Smart Contract Deployment
Deploy `SmartContract/code.txt` using:
- [Remix IDE](https://remix.ethereum.org/)
- Truffle
- Hardhat
- Any Solidity-compatible development environment

## 📡 API Endpoints

### Blockchain Endpoints
- `GET /mine_block` - Mine a new block
- `GET /get_chain` - Get the full blockchain
- `GET /is_valid` - Validate the blockchain

### Cryptocurrency Endpoints
- `POST /add_transaction` - Add a new transaction
- `POST /connect_node` - Connect a new node to the network
- `GET /replace_chain` - Replace chain with longest valid chain

### Example API Usage
```bash
# Mine a block
curl http://localhost:5000/mine_block

# Add a transaction
curl -X POST http://localhost:5000/add_transaction \
  -H "Content-Type: application/json" \
  -d '{"sender": "alice", "receiver": "bob", "amount": 10}'

# Connect nodes
curl -X POST http://localhost:5001/connect_node \
  -H "Content-Type: application/json" \
  -d '{"nodes": ["http://127.0.0.1:5002", "http://127.0.0.1:5003"]}'
```

## 🔒 Security

- ✅ No hardcoded API keys or sensitive data
- ✅ Environment variables should be used for any future API integrations
- ✅ Proof-of-work consensus mechanism
- ✅ Transaction validation and digital signatures

## 🧪 Testing

Test the blockchain functionality:
1. Start multiple nodes
2. Mine blocks on different nodes
3. Add transactions
4. Test network synchronization
5. Validate chain integrity

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

This is an educational project for learning blockchain and cryptocurrency concepts. Not intended for production use or real financial transactions.

## 📞 Support

For questions or issues:
- Open an issue on GitHub
- Check the code comments for implementation details
- Review the API documentation above

---

**Happy Blockchain Development! 🚀**
