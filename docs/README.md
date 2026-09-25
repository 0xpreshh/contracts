# MergeFi Design Documents

This directory contains design documents and analyses for the MergeFi contracts.

- **[access-control-audit.md](access-control-audit.md)** — Function-by-function audit of every public entrypoint across the three contracts, comparing documented access levels against actual runtime enforcement.

- **[escrow-crowdfunding-design.md](escrow-crowdfunding-design.md)** — Design for multi-sponsor crowdfunding in the escrow contract, enabling multiple sponsors to co-fund the same issue.

- **[maintenance-pool-pagination-analysis.md](maintenance-pool-pagination-analysis.md)** — Analysis of pagination strategies, batch enumeration, and memory boundaries for maintenance pool deposit and contributor tracking.

- **[milestones-crowdfunding-design.md](milestones-crowdfunding-design.md)** — Design for multi-sponsor crowdfunding in the milestones contract, enabling proportional contribution tracking and refund.

- **[pause-circuit-breaker-design.md](pause-circuit-breaker-design.md)** — Design for emergency pausing and circuit breaker mechanisms across contracts for admin operations.

- **[real-network-integration-testing.md](real-network-integration-testing.md)** — Guidelines and execution strategy for integration testing against live Stellar testnet and local sandbox environments.

- **[recovery-address-justification.md](recovery-address-justification.md)** — Security justification and operational model for emergency admin/sponsor recovery addresses and fund protection.

- **[refund-permissionless-analysis.md](refund-permissionless-analysis.md)** — Analysis of the `refund` function's permissionless-after-deadline path, including economics, griefing vectors, and sponsor control guarantees.

- **[replay-nonce-safety-analysis.md](replay-nonce-safety-analysis.md)** — Analysis of transaction replay prevention, nonce tracking, and Soroban invocation idempotency.

- **[two-key-admin-oracle-design.md](two-key-admin-oracle-design.md)** — Architectural design for two-key admin and oracle role separation for automated milestone settlements.

- **[upgrade-storage-migration-design.md](upgrade-storage-migration-design.md)** — Migration patterns, footprint management, and storage compatibility plans for contract upgrades.

- **[wasm-build-profile-investigation.md](wasm-build-profile-investigation.md)** — Analysis of WASM build optimization, compiler flags, and contract binary size budgets.

