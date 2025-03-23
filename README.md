# BITCOIN SCRIPTING - Team DECRYPTORS

## Team Members

- **Nidarsana M** - Roll no: 230004031 - [GitHub Profile](https://github.com/Nidarsana02)
- **Nandini Kumari** - Roll no: 230001056 - [GitHub Profile](https://github.com/dini-5002)
- **Tripti Anand** - Roll no: 230001078 - [GitHub Profile](https://github.com/Tripti1298) 

## Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Installation](#installation)
- [How it works?](#how-it-works)
  - [SegWit Transactions](#segwit-transactions)
  - [Legacy Transactions](#legacy-transactions)
- [Results and Analysis](#results-and-analysis)
- [Conclusion](#conclusion)

## Overview
This project analyzes Bitcoin transactions by comparing **SegWit (Segregated Witness) transactions** with **Legacy transactions**. The analysis covers transaction size, weight, and efficiency to understand the improvements SegWit brings to the Bitcoin network.


## Project Structure
```
|-- Legacy.ipynb        # Jupyter Notebook analyzing Legacy transactions
|-- SegWit.ipynb        # Jupyter Notebook analyzing SegWit transactions
|-- README.md           # Project documentation
```

## Requirements
The following are required to be installed:
- Python 3.x
- `python-bitcoinrpc` package
- A running Bitcoin Core node with RPC enabled
- Bitcoin Core testnet setup with sufficient balance.

### Install Dependencies
```sh
pip install python-bitcoinrpc
```

## Configuration
Modify the `rpc_user`, `rpc_password`, `rpc_host`, and `rpc_port` fields in the scripts to match your Bitcoin Core configuration (`bitcoin.conf`).

## Files
- `Legacy.ipynb`: Demonstrates transactions using Legacy addresses (P2PKH).
- `SegWit.ipynb`: Demonstrates using SegWit addresses (P2SH-SegWit and P2WPKH).

## Features
### Legacy Transactions
- Ensures the wallet is loaded or created.
- Generates Legacy Bitcoin addresses (P2PKH).
- Funds an address and performs transactions between addresses.
- Creates, signs, and broadcasts raw transactions.
- Decodes transactions and extracts `scriptSig`.

### SegWit Transactions
- Uses P2SH-SegWit and Native SegWit (P2WPKH) addresses.
- Creates and signs transactions with SegWit-specific witness data.
- Extracts and verifies redeem scripts and public key hashes.

## Running the Notebooks
```sh
# Ensure your Bitcoin Core node is running and properly configured

# Start Jupyter Notebook
jupyter notebook
```

Then navigate to `Legacy.ipynb` or `SegWit.ipynb` and execute the cells step by step.

## Running the Bitcoin Script Debugger (`btcdeb`)

### SSH Login:
To access the server, run the following command in your terminal:
```sh
ssh -x <username>@<server-ip>
```
**Password:** `<password>`

If you encounter any issues logging in, let me know.

### Running `btcdeb`
Once logged in, use `btcdeb` to debug Bitcoin scripts:
```sh
btcdeb ["<signature1> <signature2>"] [<scriptPubKey>]
```

Replace `<signature1>`, `<signature2>`, and `<scriptPubKey>` with actual transaction values.


## License
This project is released under the MIT License.
