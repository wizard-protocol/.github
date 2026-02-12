<p align="center">
  <img src="assets/wizard-hat.svg" alt="Wizard" width="80" />
</p>

<h1 align="center">wizard</h1>

<p align="center">
  <strong>Peer-to-peer decentralized exchange on Cardano</strong>
</p>

<p align="center">
  Trustless token swaps · No batchers · No intermediaries
</p>

---

### What is Wizard?

Wizard is a P2P DEX protocol on [Cardano](https://cardano.org) that lets users trade tokens directly with each other — no centralized order matching, no batchers, no middlemen.

You place an order. Someone fills it. The smart contract enforces the trade. That's it.

### ✨ Features

- **🔒 Trustless** — All trades enforced on-chain. No custody risk.
- **💱 Limit Orders** — Set your price, walk away. Orders live on-chain until filled or cancelled.
- **📊 Oracle Pricing** — Auto-limit orders that track market price with configurable premium/discount and floor protection.
- **🔗 Composable** — Native integration with Minswap and other Cardano DEX protocols.
- **⚡ Partial Fills** — Orders can be partially filled, maximizing liquidity.
- **🛡️ Secure** — Double-satisfaction prevention, output index uniqueness, and flexible multisig authorization.

### How It Works

```
  ┌──────────┐                        ┌──────────┐
  │  Maker   │ ─── create order ────► │ Wizard   │
  │          │                        │ Validator │
  └──────────┘                        └────┬─────┘
                                           │
  ┌──────────┐      fill order             │
  │  Taker   │ ◄───── trustless swap ──────┘
  │          │
  └──────────┘
```

1. **Create** — Lock tokens in the Wizard validator with your price
2. **Fill** — A taker submits a transaction satisfying the price condition
3. **Settle** — The validator ensures both parties get exactly what's owed
4. **Cancel** — Only the owner can withdraw unfilled funds

### Pricing Modes

| Mode | How it works |
|------|-------------|
| **Fixed Price** | Static limit order — *"I want X tokens for Y tokens"* |
| **Auto Limit** | Oracle-tracked price with premium/discount and minimum floor protection |

### Architecture

```
Wizard.Web  →  Wizard.API  →  Wizard.Sync  (chain indexer)
                            →  Wizard.Tx    (transaction builder)
```

| Component | Stack | Purpose |
|-----------|-------|---------|
| **Validator** | Aiken | On-chain smart contract |
| **Wizard.Sync** | .NET | Chain indexer with rollback support |
| **Wizard.API** | .NET | Backend serving indexed data |
| **Wizard.Tx** | .NET / Chrysalis | Cardano transaction builder |
| **Wizard.Web** | Next.js | Trading interface |

### Repositories

| Repo | Description |
|------|-------------|
| [**Wizard.Offchain**](https://github.com/wizard-protocol/Wizard.Offchain) | Off-chain stack — indexer, API, tx builder, frontend |
| [**P2P**](https://github.com/wizard-protocol/P2P) | On-chain validators (Aiken) |

---

<p align="center">
  Built by <a href="https://github.com/SAIB-Inc">SAIB</a> · Cardano 💜
</p>
