## <img src="assets/wizard-hat.svg" alt="" width="28" /> wizard — Composable liquidity infrastructure for Cardano

### The Problem

AMMs on Cardano mandate shared liquidity pools — dual-token deposits, impermanent loss, fragmented liquidity across isolated pools, and limited options for market makers who want fine-grained control over their capital.

### What Wizard Does

Wizard is a **P2P global orderbook** that sits alongside AMM DEXes and aggregators as composable liquidity infrastructure. Instead of pooling funds with strangers, you deploy your own automated strategies — non-custodial, on-chain, and fully configurable.

**Auto-Limit Orders** — Orders that automatically track market price via oracle feeds. Set a premium (distance from mid-price), and your order updates itself. No manual repricing, no extra transaction fees.

**Automated Market Making** — Deploy single-side or two-way strategies with auto-compounding and inventory management. Grid-based order placement for multi-level positioning across price ranges.

**Strategy Marketplace** — Create, list, and monetize your market making strategies. Others subscribe and deploy them on their own capital — non-custodial, always.

### How It Works

```
You deposit tokens
  → Configure strategy (premiums, grid levels, allocation)
    → Orders auto-update with market price
      → Fills compound back into new orders
        → Your capital works while you sleep
```

- **One-Way** — Buy-only accumulation or sell-only distribution
- **Two-Way** — Balanced bid/ask market making around mid-price
- **Stablecoin MM** — Automated arbitrage between pegged stablecoins
- **Custom Grids** — Multi-level orders with per-level inventory allocation

### Why It Matters

Wizard doesn't compete with DEXes — it **feeds them**. Every strategy populates a global orderbook with liquid, composable limit orders that aggregators and other protocols can route through. More strategies → deeper orderbook → better prices for everyone.

**Built with [Aiken](https://aiken-lang.org)** — clean, auditable smart contracts. Small attack surface. No unnecessary complexity.
