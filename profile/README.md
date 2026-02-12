<p align="center">
  <h1 align="center">🧙 Wizard Protocol</h1>
  <p align="center">
    <strong>Peer-to-peer decentralized exchange on Cardano</strong>
  </p>
  <p align="center">
    Trustless token swaps. No batchers. No intermediaries.
  </p>
</p>

---

## What is Wizard?

Wizard is a P2P DEX protocol on Cardano that lets users trade tokens directly with each other — no centralized order matching, no batchers, no middlemen.

You place an order. Someone fills it. The smart contract enforces the trade. That's it.

### Key Features

- **🔒 Trustless** — All trades enforced by on-chain validators. No custody risk.
- **💱 Limit Orders** — Set your price, walk away. Orders live on-chain until filled or cancelled.
- **📊 Oracle-Powered Pricing** — Auto-limit orders that track market price with configurable premium/discount and floor protection.
- **🔗 Composable** — Native integration with Minswap and other Cardano DEX protocols.
- **⚡ Partial Fills** — Orders can be partially filled, maximizing liquidity.
- **🛡️ Battle-Tested Security** — Double-satisfaction prevention, output index uniqueness, and flexible multisig authorization.

### How It Works

```
┌─────────────┐     on-chain      ┌─────────────┐
│  Alice       │ ──── order ────► │  Validator   │
│  (maker)     │                  │  (Aiken)     │
└─────────────┘                  └──────┬──────┘
                                        │
┌─────────────┐     fill order          │
│  Bob         │ ◄──────────────────────┘
│  (taker)     │   trustless swap
└─────────────┘
```

1. **Create** — Alice locks tokens in the Wizard validator with her price
2. **Fill** — Bob submits a transaction that satisfies the price condition
3. **Settle** — The validator ensures both parties get exactly what's owed
4. **Cancel** — Only the order owner can withdraw unfilled funds

### Architecture

| Component | Description |
|-----------|-------------|
| **Wizard Validator** | Aiken smart contract (~200 LOC) — the on-chain brain |
| **Wizard.Sync** | Chain indexer — follows the blockchain and indexes protocol events |
| **Wizard.API** | Backend API — serves indexed data to the frontend |
| **Wizard.Tx** | Transaction builder — constructs Cardano transactions |
| **Wizard.Web** | Frontend — the user-facing trading interface |

### Pricing Modes

| Mode | Description |
|------|-------------|
| **FixedPrice** | Static limit order — "I want X tokens for Y tokens" |
| **AutoLimit** | Oracle-tracked price with premium/discount and minimum floor |

## Repositories

| Repo | Description |
|------|-------------|
| [Wizard.Offchain](https://github.com/wizard-protocol/Wizard.Offchain) | Off-chain stack: indexer, API, tx builder, frontend |
| [P2P](https://github.com/wizard-protocol/P2P) | Smart contract validators (Aiken) |

## Tech Stack

- **On-chain:** [Aiken](https://aiken-lang.org) (Cardano smart contracts)
- **Off-chain:** .NET / C# (Chrysalis tx builder)
- **Frontend:** Next.js / TypeScript
- **Indexer:** Custom chain sync with rollback support

## Built by [SAIB](https://github.com/SAIB-Inc)

---

<p align="center">
  <sub>Building the future of P2P trading on Cardano 💜</sub>
</p>
