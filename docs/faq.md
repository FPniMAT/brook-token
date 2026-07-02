# Frequently Asked Questions (FAQ)

This document answers common questions about the **brook-token** project. It is intended to help developers, contributors, and users quickly resolve common issues and better understand the project's functionality.

---

# Purpose

The purpose of this FAQ is to:

- Answer frequently asked questions.
- Help troubleshoot common issues.
- Reduce repetitive support requests.
- Guide new contributors and users.
- Provide quick references for common development tasks.

---

# General Questions

### What is brook-token?

Brook Token is an ERC-20 compatible smart contract built for EVM-compatible blockchains. It serves as a foundation for blockchain applications, decentralized finance (DeFi), governance systems, and other Web3 use cases.

---

### Which blockchain networks are supported?

Brook Token can be deployed to any EVM-compatible blockchain, including Ethereum, Polygon, Arbitrum, Base, Optimism, BNB Chain, Avalanche, and other compatible networks.

---

### Is the token ERC-20 compliant?

Yes. Brook Token follows the ERC-20 standard, making it compatible with most wallets, exchanges, and decentralized applications.

---

# Development

### Which framework does this project use?

The project uses **Foundry** for smart contract development, testing, and deployment.

---

### How do I build the project?

Run:

```bash
forge build
```

---

### How do I run all tests?

```bash
forge test
```

---

### How do I format the code?

```bash
forge fmt
```

---

### How do I generate a gas report?

```bash
forge test --gas-report
```

---

# Deployment

### How do I deploy the contracts?

Use the deployment script:

```bash
forge script script/Deploy.s.sol --broadcast
```

Make sure your RPC endpoint and private key are properly configured.

---

### Where should I store my private key?

Private keys should **never** be committed to the repository. Store them securely using environment variables, hardware wallets, or a secret management solution.

---

### Can I deploy to a local blockchain?

Yes. You can deploy to a local Anvil instance for testing and development before deploying to a public network.

---

# Security

### Is the project audited?

Audit status depends on the current release. Always check the repository for the latest security reviews and audit reports.

---

### Does the project support upgradeable contracts?

This depends on the implementation. Review the contract architecture and deployment documentation to determine whether upgradeability is supported.

---

### How can I report a security vulnerability?

Please report security issues privately to the project maintainers. Avoid publicly disclosing vulnerabilities until they have been reviewed and resolved.

---

# Token

### Can new tokens be minted?

Minting capabilities depend on the contract implementation. Refer to the smart contract documentation for details.

---

### Can tokens be burned?

If burning functionality is implemented, authorized users or token holders may permanently remove tokens from circulation according to the contract's rules.

---

### Where can I find the contract address?

The official contract address should be published in the project's documentation or release notes after deployment.

---

# Integration

### Which wallets are supported?

Any wallet supporting ERC-20 tokens and EVM-compatible networks should be compatible, including MetaMask, Rabby Wallet, Coinbase Wallet, Trust Wallet, and OKX Wallet.

---

### Can exchanges list Brook Token?

Yes. Since Brook Token follows the ERC-20 standard, centralized and decentralized exchanges can integrate it after completing their own listing and verification procedures.

---

### How do I integrate Brook Token into my application?

Refer to the **Integration Guide** for information about contract interactions, wallet integration, and supported ERC-20 functions.

---

# Troubleshooting

### My transaction failed. What should I check?

Common causes include:

- Insufficient token balance
- Insufficient gas
- Incorrect network
- Invalid contract address
- Contract execution reverted

---

### Why doesn't my wallet display the token?

Verify that:

- You are connected to the correct network.
- The correct contract address has been added.
- The token decimals are correct.
- Your wallet has synchronized with the blockchain.

---

### Why are my tests failing?

Possible reasons include:

- Contracts do not compile.
- Dependencies are missing.
- Test expectations are incorrect.
- Environment configuration is incomplete.

Run:

```bash
forge build

forge test -vvvv
```

to obtain detailed output.

---

# Contributing

### How can I contribute?

You can contribute by:

- Fixing bugs
- Adding new features
- Improving documentation
- Writing tests
- Reviewing Pull Requests
- Reporting issues

Please read the **Developer Guide** before contributing.

---

### Do I need to write tests for new features?

Yes. Every new feature or bug fix should include appropriate unit or integration tests to maintain code quality and reliability.

---

# Additional Resources

For more information, see:

- Root `README.md`
- Developer Guide
- Security Practices
- Integration Guide
- Token Economics
- Foundry Documentation
- Solidity Documentation
- OpenZeppelin Contracts

---

# License

This FAQ is part of the **brook-token** project and is distributed under the same license as the root repository.
