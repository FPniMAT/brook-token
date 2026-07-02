````markdown
# Deployment Scripts

This directory contains the deployment and automation scripts used to deploy the **brook-token** smart contracts to EVM-compatible blockchain networks.

The scripts are written for the **Foundry** framework and are designed to streamline the deployment process while ensuring consistency across development, testing, and production environments.

---

# Purpose

The purpose of this directory is to:

- Automate smart contract deployment.
- Simplify deployments across multiple networks.
- Reduce manual configuration errors.
- Enable repeatable and consistent deployments.
- Support verification and post-deployment tasks.

Deployment scripts help developers launch contracts efficiently without manually interacting with blockchain nodes.

---

# Contents

This folder may contain the following files:

| File | Description |
|------|-------------|
| `Deploy.s.sol` | Main deployment script for the Brook Token contract. |
| `Verify.s.sol` | Contract verification script (optional). |
| `Upgrade.s.sol` | Upgrade script for upgradeable contracts (if applicable). |
| `HelperConfig.s.sol` | Network configuration helper. |
| `Interactions.s.sol` | Scripts for interacting with deployed contracts. |

> The available scripts may vary depending on the current implementation.

---

# Directory Structure

```text
script/
├── Deploy.s.sol
├── Verify.s.sol
├── Upgrade.s.sol
├── HelperConfig.s.sol
└── Interactions.s.sol
```

---

# Prerequisites

Before running deployment scripts, ensure you have:

- Foundry installed
- A funded wallet
- RPC endpoint for your target network
- Private key stored securely
- Environment variables configured

---

# Environment Variables

Create a `.env` file in the project root.

Example:

```env
PRIVATE_KEY=your_private_key
RPC_URL=https://your-network-rpc-url
ETHERSCAN_API_KEY=your_api_key
```

> **Never commit your `.env` file or private keys to GitHub.**

---

# Build Contracts

Compile contracts before deployment.

```bash
forge build
```

---

# Run Local Deployment

Deploy using a local Anvil node.

```bash
forge script script/Deploy.s.sol \
    --rpc-url http://127.0.0.1:8545 \
    --broadcast
```

---

# Deploy to Testnet

Example deployment:

```bash
forge script script/Deploy.s.sol \
    --rpc-url $RPC_URL \
    --private-key $PRIVATE_KEY \
    --broadcast
```

---

# Verify Contract

If supported, verify the deployed contract.

```bash
forge verify-contract \
    <CONTRACT_ADDRESS> \
    src/BrookToken.sol:BrookToken \
    $ETHERSCAN_API_KEY
```

---

# Dry Run

Simulate deployment without broadcasting transactions.

```bash
forge script script/Deploy.s.sol
```

This allows developers to inspect transactions before sending them to the blockchain.

---

# Deployment Workflow

Typical deployment process:

1. Configure environment variables.
2. Compile contracts.
3. Run the deployment script.
4. Broadcast transactions.
5. Verify the deployed contract.
6. Record deployed contract addresses.
7. Perform post-deployment testing.

---

# Best Practices

- Double-check the target network before deployment.
- Use a dedicated deployment wallet.
- Keep private keys secret.
- Test on a local network or testnet before deploying to mainnet.
- Verify deployed contracts whenever possible.
- Store deployment addresses for future reference.

---

# Troubleshooting

### Deployment fails

- Verify your RPC URL.
- Ensure the wallet has sufficient funds.
- Check that the contract compiles successfully.

### Invalid private key

Confirm your `.env` file is loaded correctly and the key is formatted without extra quotes or spaces.

### Gas estimation issues

- Increase the gas limit if necessary.
- Ensure the target network is operational.
- Retry the deployment after confirming network status.

---

# Additional Resources

- Foundry Documentation
- Solidity Documentation
- OpenZeppelin Contracts

---

# License

This directory is part of the brook-token project and follows the same license as the root repository.
````
