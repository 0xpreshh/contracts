# WASM Build Profile and Binary Size Investigation

## Overview

Soroban smart contracts compiled for WebAssembly (`wasm32v1-none` target) must remain compact to minimize deployment gas fees and on-chain storage costs.

## Binary Size Budget

- **Target Size Budget**: 250 KB (256,000 bytes) maximum per compiled contract (`.wasm`).
- **Enforcement**: Automated in CI `.github/workflows/ci.yml` via the `wasm-build` job following release compilation.

## Build Optimization Strategies

1. **Release Profile Configuration (`Cargo.toml`)**:
   - `opt-level = "z"`: Optimize binary specifically for size.
   - `lto = true`: Enable Link-Time Optimization across workspace crates.
   - `codegen-units = 1`: Maximize size reduction by running single-threaded optimization passes.
   - `panic = "abort"`: Strip panic unwinding overhead.
   - `strip = true`: Strip symbols and debug metadata.

2. **Common Dependency Sharing**:
   - Shared business logic resides in `mergefi-common` crate to avoid code duplication across contracts.
