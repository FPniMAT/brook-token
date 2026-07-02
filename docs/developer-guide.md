# Developer Guide

Welcome to the **brook-token** developer guide. This document provides everything contributors need to set up the development environment, understand the project workflow, follow coding standards, and submit high-quality contributions.

---

# Purpose

The purpose of this guide is to:

- Help new contributors get started quickly.
- Establish a consistent development workflow.
- Define coding standards and best practices.
- Explain testing and code review expectations.
- Ensure high-quality, maintainable code contributions.

Whether you're fixing bugs, adding features, or improving documentation, following this guide will help keep the project organized and reliable.

---

# Prerequisites

Before contributing, ensure you have the following installed:

- Git
- Foundry
- Solidity Compiler (via Foundry)
- Node.js (if frontend or scripting support is required)
- A code editor (VS Code recommended)

Verify your Foundry installation:

```bash
forge --version

cast --version

anvil --version
```

---

# Project Setup

Clone the repository:

```bash
git clone https://github.com/FPniMAT/brook-token.git

cd brook-token
```

Install dependencies:

```bash
forge install
```

Compile the project:

```bash
forge build
```

Run the complete test suite:

```bash
forge test
```

---

# Project Structure

```text
brook-token/
├── contracts/
├── script/
├── test/
├── docs/
├── lib/
├── foundry.toml
└── README.md
```

---

# Development Workflow

A typical development workflow is:

1. Fork the repository.
2. Create a new feature branch.
3. Implement your changes.
4. Write or update tests.
5. Format the code.
6. Run all tests.
7. Commit your changes.
8. Open a Pull Request.

---

# Branch Naming

Use descriptive branch names.

Examples:

```
feature/add-burning

feature/governance-module

fix/token-transfer

docs/update-readme

test/fuzz-tests
```

---

# Coding Standards

Follow these best practices when writing Solidity code:

- Write clear and readable code.
- Keep functions focused on a single responsibility.
- Minimize duplicated logic.
- Use meaningful variable and function names.
- Prefer modular contract architecture.
- Document all public and external functions.
- Avoid unnecessary gas consumption.

---

# Formatting

Format your code before committing.

```bash
forge fmt
```

Never submit unformatted code.

---

# Static Analysis

Run analysis tools whenever possible.

Recommended tools:

- Slither
- Mythril
- Solhint

These tools help detect potential vulnerabilities and improve code quality.

---

# Testing

Every new feature should include corresponding tests.

Run all tests:

```bash
forge test
```

Verbose output:

```bash
forge test -vvvv
```

Generate a gas report:

```bash
forge test --gas-report
```

Generate coverage (if supported):

```bash
forge coverage
```

---

# Documentation

Whenever new functionality is introduced:

- Update relevant README files.
- Document public interfaces.
- Explain configuration changes.
- Add usage examples when appropriate.

Documentation should evolve alongside the codebase.

---

# Commit Guidelines

Write clear, concise commit messages.

Examples:

```
feat: add burn functionality

fix: prevent unauthorized minting

docs: update deployment guide

test: improve fuzz coverage

refactor: simplify token initialization
```

---

# Pull Request Guidelines

Before submitting a Pull Request:

- Ensure all tests pass.
- Format the code.
- Update documentation if necessary.
- Include a clear description of the changes.
- Reference related issues when applicable.

A good Pull Request should explain:

- What changed
- Why it changed
- How it was tested
- Any breaking changes

---

# Code Review Process

Contributions are reviewed for:

- Correctness
- Readability
- Security
- Performance
- Maintainability
- Documentation quality
- Test coverage

Feedback should be addressed before merging.

---

# Best Practices

Contributors are encouraged to:

- Keep Pull Requests focused.
- Avoid unrelated changes.
- Write reusable code.
- Follow existing project patterns.
- Consider security implications.
- Maintain backward compatibility whenever possible.

---

# Reporting Issues

When reporting bugs, include:

- Description of the issue
- Steps to reproduce
- Expected behavior
- Actual behavior
- Environment details
- Relevant logs or screenshots

Detailed reports help resolve issues more efficiently.

---

# Getting Help

If you have questions:

- Review the project documentation.
- Search existing issues.
- Open a new discussion or issue if needed.
- Ask maintainers for clarification before implementing large changes.

---

# Contributing

All contributions—whether code, documentation, testing, or suggestions—are welcome and appreciated. By contributing, you help improve the quality, security, and usability of the brook-token project.

---

# License

This guide is part of the **brook-token** project and is distributed under the same license as the root repository.
