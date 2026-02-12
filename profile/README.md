## <img src="assets/wizard-hat.svg" alt="" width="28" /> wizard — Peer-to-peer liquidity on Cardano

### The Problem

Decentralized exchanges on Cardano still rely on centralized components — batchers that sequence transactions, operators that extract value, and intermediaries that add latency and trust assumptions to what should be a trustless system.

### The Vision

Wizard removes the middleman entirely. It's a **peer-to-peer liquidity protocol** where every trade is a direct swap between two parties, enforced purely by on-chain smart contracts.

No batchers. No operators. No MEV extraction. Just math.

### How Wizard Works

- **You set a price** — Place a limit order on-chain with your terms
- **Someone takes it** — A counterparty fills your order (fully or partially)
- **The contract settles** — Both sides get exactly what was agreed, or the transaction fails
- **You stay in control** — Only you can cancel your order and reclaim your funds

Orders can track oracle prices automatically with floor protection, or use simple fixed pricing. Your choice.

### Why It Matters

Wizard brings a trustless peer-to-peer liquidity layer to Cardano. It composes natively with existing protocols like Minswap, turning isolated liquidity into a connected network — not competing with DEXes, but making them more powerful.

**Built with [Aiken](https://aiken-lang.org)** — clean, auditable smart contracts. ~200 lines of validator logic. Small attack surface. No unnecessary complexity.
