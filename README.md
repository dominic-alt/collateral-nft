# 🟧 Satoshi Collateral NFT

## Collateralized NFTs with Yield, Fractional Ownership & Marketplace Functionality on Stacks Layer 2

## Overview

**Satoshi Collateral NFT** is a comprehensive smart contract platform built on the **Stacks L2** protocol, integrating NFTs with **collateralization**, **staking-based yield**, **fractional ownership**, and a **decentralized marketplace**. This ecosystem brings real financial utility to NFTs by allowing users to lock STX tokens as collateral, earn rewards through staking, and share ownership through tokenized fractions — all while preserving Bitcoin compatibility and security.

## Features

### Collateralized NFT Minting

* Mint NFTs by locking STX collateral.
* Enforced **minimum collateral ratio** to ensure stability.
* Supports secure metadata via URI validation.

### NFT Transfers & Marketplace

* Fully compliant NFT transfers.
* Decentralized listing and purchasing logic.
* Auto-calculated **protocol fee** distribution to contract treasury.

### Staking & Yield Generation

* Stake NFTs to earn **automated yield** based on block height.
* Rewards calculated in STX, claimable at any time.
* Dynamic tracking of staking periods and accumulated rewards.

### Fractional Ownership Functions

* Divide NFT ownership into fractional shares.
* Transfer shares securely between principals.
* Track and update fractional records for each token-owner pair.

### Security & Access Control

* Ownership checks for all critical functions.
* Overflow-safe arithmetic.
* URI and recipient validation to prevent malicious inputs.

## Smart Contract Architecture

### Constants

* `min-collateral-ratio`: 150% required by default.
* `protocol-fee`: 2.5% charged on NFT sales.
* `yield-rate`: 5% annual, distributed per block.

### Key Data Structures

* `tokens`: Main NFT storage (owner, URI, collateral, staking status).
* `token-listings`: Active listings for marketplace interactions.
* `fractional-ownership`: Tracks per-token fractional share ownership.
* `staking-rewards`: Maintains reward history and timing.

### Error Handling

Defined comprehensive error codes (e.g., `err-not-token-owner`, `err-overflow`, `err-already-staked`) for transparent debugging and consistent validation.

## Public Functions

### NFT

* `mint-nft(uri, collateral)`: Mint new NFT with STX collateral.
* `transfer-nft(token-id, recipient)`: Send NFT to another principal.

### Marketplace

* `list-nft(token-id, price)`: List your NFT for sale.
* `purchase-nft(token-id)`: Buy listed NFT using STX.

### Fractional Ownership

* `transfer-shares(token-id, recipient, share-amount)`: Send fractional shares.

### Staking

* `stake-nft(token-id)`: Stake NFT to start earning rewards.
* `unstake-nft(token-id)`: Unstake NFT and claim rewards.

### View Functions

* `get-token-info`, `get-listing`, `get-fractional-shares`, `get-staking-rewards`
* `calculate-rewards`: Computes accrued yield since last claim.

## Deployment Notes

* Built for **Clarity** smart contracts (Stacks ecosystem).
* Optimized for **Bitcoin L2 compliance** and scalability.
* Use with a Clarity-compatible IDE like [Clarinet](https://docs.hiro.so/clarinet/get-started) or deploy via [Stacks Explorer](https://explorer.stacks.co).

## Use Cases

* **DeFi-Backed NFTs**: Add financial backing to digital collectibles.
* **NFT Liquidity Pools**: Share ownership among multiple users.
* **Yield-Bearing Digital Assets**: Stake NFTs for passive income.
* **Decentralized NFT Trading**: Trustless marketplace mechanics.

## 🙌 Acknowledgments

Built with ❤️ on the [Stacks](https://www.stacks.co) Layer 2 protocol, inheriting Bitcoin’s security model while enabling rich smart contract capabilities through Clarity.
