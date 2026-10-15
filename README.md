# Uniswap v4 MEV-Shield Hook (Dynamic Volatility Fee)

A production-grade Uniswap v4 Hook designed to mitigate toxic order flow, prevent predatory MEV (Sandwich attacks), and dynamically adjust swap fees based on real-time block-level slippage and pool volatility.

## Architecture Overview
This project implements the Uniswap v4 `BaseHook` architecture:
- **`beforeSwap`**: Evaluates gas-price deviations and block-level trade volumes to identify sandwich attempt clusters.
- **`afterSwap`**: Dynamically adjusts protocol LP fee share based on realized pool volatility.

## Tech Stack
- **Framework:** Foundry / Forge
- **Solidity Version:** ^0.8.24
- **Standards:** Uniswap v4 Periphery, OpenZeppelin v5.0 Contracts

## Testing & Audit Readiness
- Comprehensive invariant and fuzz testing suites via Foundry.
- Static analysis executed via Slither and Aderyn.
- Fully compatible with Areta Security Audit criteria.

## License
MIT License
