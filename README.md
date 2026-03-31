# Web3 Casino Game Hub

A multi-game **Web3 casino** demo repository: **Solana** Anchor programs (jackpot / VRF), **EVM** (Hardhat) contracts, **Sui** SDK samples, and several browser games with Node backends — **Plinko**, **Mine**, **Roulette** (CLI), **Baccarat** (engine), and **Blackjack** (multi-chain app + API).

## Repository layout

| Path | Description |
|------|-------------|
| `contract/` | Solana **Anchor** workspace — `jackpot_smart_contract` (ORAO VRF, devnet config in `Anchor.toml`). |
| `Frontend/plinko/` | Plinko **React** client + **Express** + **Socket.IO** + **MongoDB** server. |
| `Frontend/Mine/` | Mine game **React** + **Express** + Socket.IO backend. |
| `Frontend/Roulette/` | Roulette **TypeScript** CLI (`roulette/`), Solidity + Rust program stubs under `program-solidity` / `program-rust`. |
| `Frontend/Baccarat/` | Standalone **Baccarat** rules / roadmap **JavaScript** engine. |
| `Frontend/Blackjack/` | Blackjack **React** app, **REST API**, **Hardhat** EVM contracts, **Solana** program folder, **Sui** Move + TS SDK. |

## Prerequisites

- **Node.js** 20 LTS (recommended 20.18+ for newest `@solana/*` tooling).
- **Rust** + **Solana** + **Anchor** CLI for `contract/` and Solana programs (see each `Anchor.toml`).
- **MongoDB** where Plinko / Mine backends expect a database (configure env / `config.json`).

## Quick start (per package)

Each subproject has its own `package.json`. From the relevant folder:

```bash
npm install
npm run dev
# or: npm start, npm run build — see that package's scripts
```

Examples:

- **Plinko UI:** `Frontend/plinko/plinko-fe` → `npm start`
- **Plinko API:** `Frontend/plinko/plinko-be` → `npm run dev`
- **Jackpot contract (Anchor):** `contract/` → use Anchor CLI (`anchor build`, `anchor test`) as documented in `programs/`.

## Security notes

- Replace placeholder keys, RPC URLs, and program IDs before any mainnet use.
- This repo is intended for **development and learning**; audit contracts and backends before production.

## License

See individual subfolders' `LICENSE` / `package.json` fields (mixed MIT / ISC).
