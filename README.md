# Upgradeable Smart Contracts

A hands-on project exploring upgradeable smart contracts in Solidity using Foundry.

This repository focuses on understanding how smart contracts can be upgraded after deployment while preserving state and storage. The project covers proxy patterns, storage layout considerations, initialization logic, and common security risks associated with upgradeable systems.

## Topics Covered

- Proxy Architecture
- Transparent Proxy Pattern
- UUPS Proxy Pattern
- Delegatecall Mechanics
- Initializers vs Constructors
- Storage Layout Management
- Upgrade Authorization
- Upgrade Safety Checks
- Upgradeable Contract Security Considerations

## Tech Stack

- Solidity
- Foundry
- OpenZeppelin Upgradeable Contracts

## Learning Objectives

- Understand why upgradeability exists
- Learn how proxy contracts work under the hood
- Implement upgradeable smart contracts
- Manage storage safely across upgrades
- Identify common upgradeability vulnerabilities
- Explore real-world upgrade patterns used in DeFi protocols

## Key Concepts

### Proxy Contract

The proxy stores state and forwards calls to an implementation contract using `delegatecall`.

### Implementation Contract

Contains the business logic executed through the proxy.

### Initializer

Since constructors are not executed through proxies, initialization logic is moved into dedicated initializer functions.

### Storage Layout

Storage slots must remain compatible across upgrades to avoid corrupting contract state.

## Security Notes

Upgradeable contracts introduce additional attack surfaces:

- Unauthorized upgrades
- Storage collisions
- Initialization vulnerabilities
- Malicious implementations
- Delegatecall risks

Always review upgrade mechanisms carefully during audits.

## Learning Journey

Part of my Web3 Security and Smart Contract Auditing journey.

Built while studying upgradeable smart contracts through Updraft and Foundry.

---

**Builder:** 0xscarfac3
