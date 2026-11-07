<div align="center">

<img src="./banner.svg" alt="CointMU: a private Proof-of-Work blockchain network" width="100%">

<br>

[![Docs](https://img.shields.io/badge/📖_Docs-coint--mu--docs.vercel.app-3c8772?style=for-the-badge)](https://coint-mu-docs.vercel.app)
[![npm](https://img.shields.io/npm/v/cointmu-cli?style=for-the-badge&logo=npm&label=cointmu-cli&color=cb3837)](https://www.npmjs.com/package/cointmu-cli)
[![Chain ID](https://img.shields.io/badge/Chain_ID-1912-6fe0b8?style=for-the-badge&labelColor=0b1613)](#-network-at-a-glance)
[![Consensus](https://img.shields.io/badge/Consensus-Ethash_PoW-14382d?style=for-the-badge)](#-network-at-a-glance)
[![Mobile](https://img.shields.io/badge/📱_Mobile-Muvo-6fe0b8?style=for-the-badge&labelColor=0b1613)](https://github.com/Cointmu-ORG/CointMU-MobileApp)

**[🚀 Quick start](#-quick-start)** · **[🧩 Projects](#-projects)** · **[🏗️ Architecture](#%EF%B8%8F-architecture)** · **[🌐 Network](#-network-at-a-glance)** · **[🤝 Contributing](#-contributing)**

</div>

---

## ✨ What is CointMU?

CointMU is a **private, Ethereum-compatible Proof-of-Work blockchain** built at Universitas Muhammadiyah Yogyakarta (UMY). It's a hands-on playground: run a node, mine blocks, send transactions, deploy contracts, and watch it all happen from your laptop or your phone.

<table>
<tr>
<td align="center" width="25%">⛏️<br><b>Mine</b><br><sub>Feel real PoW mining, hash by hash</sub></td>
<td align="center" width="25%">👛<br><b>Wallet</b><br><sub>Desktop and mobile, you hold the keys</sub></td>
<td align="center" width="25%">🔍<br><b>Explore</b><br><sub>Blocks, transactions, node dashboard</sub></td>
<td align="center" width="25%">📜<br><b>Build</b><br><sub>Deploy Solidity contracts on a private chain</sub></td>
</tr>
</table>

---

## 🧩 Projects

| | Project | What it does | Stack |
|:-:|---|---|---|
| 🖥️ | **[CointMU-App](https://github.com/Cointmu-ORG/CointMU-App)** | Desktop app with a bundled Geth node, wallet, miner control, block explorer and node dashboard. Windows, Linux and macOS. | ![Electron](https://img.shields.io/badge/Electron-47848F?logo=electron&logoColor=white) ![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB) |
| 📱 | **[CointMU-MobileApp](https://github.com/Cointmu-ORG/CointMU-MobileApp)** ✨ *new* | **Muvo**, a non-custodial mobile wallet for CointMU. Android and iOS. | ![Expo](https://img.shields.io/badge/Expo-000020?logo=expo&logoColor=white) ![React Native](https://img.shields.io/badge/React_Native-20232A?logo=react&logoColor=61DAFB) ![ethers](https://img.shields.io/badge/ethers_v6-2535a0) |
| ⌨️ | **[CointMU-CLI](https://github.com/Cointmu-ORG/CointMU-CLI)** | `cmu`, the command line for creating wallets, sending transactions and mining. | ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white) ![npm](https://img.shields.io/badge/npm-cointmu--cli-cb3837?logo=npm&logoColor=white) |
| 📖 | **[CointMU-Docs](https://github.com/Cointmu-ORG/CointMU-Docs)** | Guides and references, live at [coint-mu-docs.vercel.app](https://coint-mu-docs.vercel.app). | ![VitePress](https://img.shields.io/badge/VitePress-646CFF?logo=vite&logoColor=white) |
| 🤖 | **[CointMU-Bot](https://github.com/Cointmu-ORG/CointMU-Bot)** | Mining feed bot that announces new blocks on Telegram and Discord. | ![Telegram](https://img.shields.io/badge/Telegram-26A5E4?logo=telegram&logoColor=white) ![Discord](https://img.shields.io/badge/Discord-5865F2?logo=discord&logoColor=white) |
| 📈 | **[CointMU-Telemetry](https://github.com/Cointmu-ORG/CointMU-Telemetry)** | Monitoring for the network: errors, logs, metrics and dashboards. | ![Grafana](https://img.shields.io/badge/Grafana-F46800?logo=grafana&logoColor=white) ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?logo=prometheus&logoColor=white) |

---

## 🏗️ Architecture

```mermaid
flowchart LR
    subgraph Clients["👤 Clients"]
        CLI["⌨️ cmu CLI"]
        APP["🖥️ Desktop App"]
        MOB["📱 Muvo Mobile"]
    end

    subgraph Net["⛓️ CointMU Network · Chain ID 1912"]
        direction TB
        RPC["🔌 RPC nodes"]
        MINERS["⛏️ Miners (Ethash)"]
        RPC <--> MINERS
    end

    subgraph Watch["👀 Observability"]
        BOT["🤖 Mining Feed Bot"]
        TEL["📈 Telemetry"]
    end

    CLI --> RPC
    APP --> RPC
    MOB --> RPC
    Net -.-> BOT
    Net -.-> TEL
```

---

## 🚀 Quick start

<details open>
<summary><b>⌨️ &nbsp;Command line</b> &nbsp;<sub>fastest way in</sub></summary>

<br>

```bash
npm install -g cointmu-cli
cmu create
```

Then follow the [CLI guide](https://coint-mu-docs.vercel.app) to connect to the network and start mining.

</details>

<details>
<summary><b>🖥️ &nbsp;Desktop app</b> &nbsp;<sub>wallet, miner and explorer in one window</sub></summary>

<br>

Grab the latest build for Windows, Linux or macOS from [CointMU-App](https://github.com/Cointmu-ORG/CointMU-App). The app bundles its own Geth node, so there's nothing else to install.

</details>

<details>
<summary><b>📱 &nbsp;Mobile wallet (Muvo)</b> &nbsp;<sub>Android and iOS</sub></summary>

<br>

Muvo is a non-custodial wallet, so your keys stay on your device. Setup and build instructions are in [CointMU-MobileApp](https://github.com/Cointmu-ORG/CointMU-MobileApp).

</details>

<details>
<summary><b>📜 &nbsp;Deploying smart contracts</b></summary>

<br>

> [!IMPORTANT]
> The chain has no `PUSH0` opcode, so compile with **Solidity ≤ 0.8.19**. Newer compilers emit bytecode that this network can't execute.

</details>

> [!TIP]
> New here? Start with the [docs](https://coint-mu-docs.vercel.app), then install the CLI and mine your first block.

---

## 🌐 Network at a glance

| | |
|---|---|
| 🆔 **Chain ID** | `1912` |
| ⛏️ **Consensus** | Proof of Work (Ethash) |
| 🧱 **Client** | Geth `1.10.26` |
| 📜 **Solidity** | `≤ 0.8.19` (no `PUSH0`) |
| 📖 **Connection details** | See the [docs](https://coint-mu-docs.vercel.app) |

---

## 🤝 Contributing

Contributions are welcome across all projects. Open an issue to discuss what you'd like to change, or send a pull request straight to the relevant repository. Each repo has its own guidelines and security policy, so please check there first. For security problems, report them privately instead of opening a public issue.

---

<div align="center">

<sub>Built with ⛏️ at <b>Universitas Muhammadiyah Yogyakarta</b></sub>

</div>
