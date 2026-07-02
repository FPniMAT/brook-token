````markdown
# Testing Documentation

This directory contains the automated test suite for the **brook-token** smart contracts. The tests are designed to verify correctness, security, and reliability across different contract functionalities before deployment.

---

# Purpose

The purpose of the testing suite is to ensure that all smart contracts behave as expected under both normal and edge-case scenarios.

The tests help to:

- Verify contract functionality.
- Detect bugs before deployment.
- Prevent regressions after code changes.
- Validate security assumptions.
- Improve code reliability and maintainability.

Comprehensive testing is a critical part of the smart contract development lifecycle, helping reduce the risk of vulnerabilities and unexpected behavior on-chain.

---

# Contents

This directory may contain the following files:

| File | Description |
|------|-------------|
| `BrookToken.t.sol` | Unit tests for the Brook Token contract. |
| `Deployment.t.sol` | Tests related to deployment scripts. |
| `Integration.t.sol` | Integration tests between multiple contracts. |
| `Invariant.t.sol` | Invariant tests for protocol consistency. |
| `Fuzz.t.sol` | Fuzz tests using randomized inputs. |
| `Mocks/` | Mock contracts used during testing. |
| `Helpers/` | Shared testing utilities and helper functions. |

> The available test files may vary depending on the current implementation.

---

# Directory Structure

```text
test/
├── BrookToken.t.sol
├── Deployment.t.sol
├── Integration.t.sol
├── Invariant.t.sol
├── Fuzz.t.sol
├── Helpers/
└── Mocks/
```

---

# Test Categories

The project may include several types of automated tests:

### Unit Tests

Validate individual smart contract functions in isolation.

Examples:

- Token transfers
- Approvals
- Minting
- Burning
- Ownership

---

### Integration Tests

Verify interactions between multiple contracts and external components.

Examples:

- Deployment workflow
- Contract interoperability
- Multi-contract transactions

---

### Fuzz Tests

Automatically generate random inputs to identify unexpected behavior and edge cases.

Examples:

- Random transfer amounts
- Random user addresses
- Boundary value testing

---

### Invariant Tests

Ensure critical protocol rules always remain true regardless of transaction order.

Examples:

- Total supply consistency
- Balance accounting
- Access control invariants

---

# Running Tests

Run all tests:

```bash
forge test
```

Run a specific test:

```bash
forge test --match-test testTransfer
```

Run tests with verbose output:

```bash
forge test -vvvv
```

Run fuzz tests:

```bash
forge test
```

Generate a gas report:

```bash
forge test --gas-report
```

Generate code coverage (if supported):

```bash
forge coverage
```

---

# Test Workflow

A recommended workflow for contributors:

1. Build the project.
2. Run the complete test suite.
3. Review failed test cases.
4. Fix issues.
5. Re-run all tests.
6. Submit changes only after all tests pass.

---

# Best Practices

When writing new tests:

- Test one behavior per test case.
- Use descriptive test names.
- Cover success and failure scenarios.
- Include edge-case testing.
- Avoid duplicated test logic.
- Keep tests deterministic whenever possible.
- Add regression tests for fixed bugs.

---

# Continuous Integration

The testing suite is intended to be executed automatically through Continuous Integration (CI) pipelines before code is merged.

Typical CI workflow:

- Install dependencies
- Build contracts
- Run formatting checks
- Execute all tests
- Report coverage
- Fail the build if any test does not pass

---

# Troubleshooting

### Compilation Errors

Run:

```bash
forge build
```

to ensure all contracts compile successfully before testing.

### Failing Tests

- Check recent contract changes.
- Verify expected values.
- Review revert messages.
- Ensure test fixtures are initialized correctly.

### RPC Issues

If tests require a live network, verify that your RPC endpoint is configured and accessible.

---

# Additional Resources

- Foundry Book
- Solidity Documentation
- OpenZeppelin Testing Guidelines

---

# License

This directory is part of the **brook-token** project and follows the same license as the root repository.
````
