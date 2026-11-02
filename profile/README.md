<div align="center">

# CointMU

**A private Proof-of-Work blockchain network, with the tools to build, mine, and run on it.**

[![Docs](https://img.shields.io/badge/docs-coint--mu--docs.vercel.app-3c8772?style=flat-square)](https://coint-mu-docs.vercel.app)
[![npm](https://img.shields.io/npm/v/cointmu-cli?style=flat-square&label=cointmu-cli)](https://www.npmjs.com/package/cointmu-cli)
[![Chain ID](https://img.shields.io/badge/chain%20ID-1912-555?style=flat-square)](https://coint-mu-docs.vercel.app/docs/guide/network-setup)

</div>

---

CointMU is an Ethereum-compatible PoW network (Geth, chain ID `1912`) built at Universitas Muhammadiyah Yogyakarta for teaching and research. Students can deploy smart contracts, mine blocks, and see what happens on a real chain without spending real money.

## Projects

| Repository | Description |
| --- | --- |
| [**CointMU-App**](https://github.com/Cointmu-ORG/CointMU-App) | Desktop client (Electron + React) that bundles a Geth node, wallet, miner control, block explorer, and node dashboard. Ships with a companion browser extension wallet. Windows, Linux, macOS. |
| [**CointMU-CLI**](https://github.com/Cointmu-ORG/CointMU-CLI) | `cmu`: the developer toolkit. Scaffold ERC20/ERC721 projects, compile Solidity, run tests on a local DevNet, deploy, and manage wallets from the terminal. |
| [**CointMU-Docs**](https://github.com/Cointmu-ORG/CointMU-Docs) | Documentation for the network, the app, and every CLI command. Built with VitePress. |
| [**CointMU-Bot**](https://github.com/Cointmu-ORG/CointMU-Bot) | Mining feed bot. Announces every mined block on Telegram and Discord and alerts when a node goes down. |
| [**CointMU-Telemetry**](https://github.com/Cointmu-ORG/CointMU-Telemetry) | Observability stack: GlitchTip for app error reports, plus Loki, Prometheus, and Grafana for node logs, chain metrics, and UPS monitoring. |

## Quick start

```bash
# Install the CLI
npm install -g cointmu-cli

# Scaffold a new contract project
cmu create
```

Want a wallet or want to mine? Grab the desktop app from the [CointMU-App releases](https://github.com/Cointmu-ORG/CointMU-App/releases).

Full guides: **[coint-mu-docs.vercel.app](https://coint-mu-docs.vercel.app)**

## Network

| | |
| --- | --- |
| Consensus | Proof of Work (Ethash) |
| Client | Geth 1.10.26 |
| Chain ID | `1912` |
| Solidity | `0.8.19` or lower (no `PUSH0` support, so `solc 0.8.20+` won't work) |

## Contributing

All repos are public, and anyone can open a pull request without an invite. Read the `CONTRIBUTING.md` in the repo you're working on first. PRs to `main` are reviewed and merged by the maintainers.

Found a bug? Open an issue in the matching repository. For security issues, follow that repo's `SECURITY.md` instead of opening a public issue.

<div align="center">
<sub>Made at Universitas Muhammadiyah Yogyakarta</sub>
</div>
