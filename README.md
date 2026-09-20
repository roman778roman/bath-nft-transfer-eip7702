# NFT Batch Sender

A browser-based tool for fast batch transfer of NFTs from a connected wallet to a secure recovery wallet.

The application is designed for situations where a wallet may be compromised and NFTs need to be moved to another wallet as quickly as possible.

## Features

- 🔗 Connect directly to **Amber Wallet**
- 🔍 Scan the connected wallet for NFTs
- 🖼️ Detect NFTs available in the wallet
- ✅ Identify NFTs that can be transferred
- 🚫 Filter out unsupported or non-transferable assets
- 📦 Batch multiple NFT transfers into a single operation
- ⚡ Uses **EIP-7702** for supported transfer workflows
- 🔐 Send recovered NFTs to a designated secure wallet
- 🌐 Runs directly in the browser
- 📄 No backend server required

## EIP-7702

The application uses **EIP-7702** to enable batch transaction workflows on compatible networks.

EIP-7702 allows an externally owned account (EOA) to temporarily delegate execution to a smart-contract implementation, making more advanced transaction batching and recovery workflows possible while retaining control of the original wallet.

## Supported Networks

The application is designed to work with EVM-compatible networks supporting the required transaction and EIP-7702 functionality.

Currently supported networks include:

- Arbitrum
- Optimism
- BNB Smart Chain
- Polygon
- Other compatible EVM networks

Network support depends on the availability of the required EIP-7702 functionality and the implementation used by the application.

## How It Works

1. Open `nft-batch-sender.html`.
2. Connect **Amber Wallet**.
3. The application scans the connected wallet.
4. NFTs available for transfer are identified.
5. Unsupported or non-transferable NFTs are excluded.
6. The application prepares the batch transfer.
7. The destination recovery wallet is specified.
8. The transaction is reviewed in Amber Wallet.
9. The user signs the transaction.
10. The selected NFTs are transferred to the secure wallet.

## Emergency Recovery

The primary use case is recovering assets from a wallet that may have been compromised.

```text
Compromised Wallet
       │
       ▼
Connect Amber Wallet
       │
       ▼
Scan NFTs
       │
       ▼
Check Transferability
       │
       ├── Unsupported → Excluded
       │
       ▼
Transferable NFTs
       │
       ▼
EIP-7702 Batch Operation
       │
       ▼
Secure Recovery Wallet
```

## Security

This is a self-custody recovery tool.

**Important:**

- Never enter your seed phrase or private key into the application.
- Verify the destination address before signing.
- Carefully review every transaction in Amber Wallet.
- Only use the application with wallets and assets you own or are authorized to recover.
- Blockchain transactions are irreversible.
- Always test the application with a small-value wallet before using it with valuable assets.

## Running Locally

No build system is required.

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

Open the HTML file in a compatible browser:

```text
nft-batch-sender.html
```

## Project Structure

```text
.
├── nft-batch-sender.html
└── README.md
```

## Disclaimer

This software is provided for educational and legitimate asset-recovery purposes.

The user is responsible for verifying wallet addresses, network selection, transaction parameters, and asset ownership before signing any transaction.

The authors are not responsible for losses resulting from incorrect addresses, unsupported assets, smart-contract behavior, network issues, transaction fees, wallet compromise, or user error.

**Never provide your seed phrase or private key to this application or to anyone else.**
