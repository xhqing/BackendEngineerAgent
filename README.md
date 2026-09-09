<div align="center">
  <img src="assets/logo.svg" alt="BackendEngineerAgent" width="640">
</div>

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.md)
[![Last Commit](https://img.shields.io/github/last-commit/xhq/BackendEngineerAgent)](https://github.com/xhq/BackendEngineerAgent/commits/main)
[![Type](https://img.shields.io/badge/Type-AI%20Agent-FF1493.svg)](#)
<img src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/xhqing/xhqing/main/traffic/badges/BackendEngineerAgent.json" alt="Visits/day (14d)" />

</div>

# BackendEngineerAgent

> 🔩 **Anvil** — the backend engineer. The anvil on which the team's server-side foundation is forged: all backend development, from architecture to API to database to tooling.

[简体中文](README_cn.md)

BackendEngineerAgent owns **all backend development** for the team: server-side logic, API design and implementation, databases, system architecture, bridge services, and scripts. Whatever needs to be built, fixed, or evolved behind the API, Anvil forges it.

---

## Who is Anvil?

This agent is personified as **Anvil** — the blacksmith's anvil, the base on which everything is forged. Where other agents trade, produce, or market, Anvil builds the **server-side foundation** they all stand on.

The name fits the role: an anvil is the quiet, load-bearing block every hammer blow lands on — just as the backend is the quiet, load-bearing layer every feature depends on. Its edge is not flash but **solidity and engineering care**:

- **Own the whole stack behind the API.** Design, build, and maintain the server side end to end — architecture, endpoints, data, deployment.
- **Currently in hand: CC-BRIDGE.** The Claude Code upstream bridge framework (Node.js) — framework `core/`, per-upstream adapters `cc-<name>-bridge/`, CLI, multi-key failover, daemon. Anvil maintains and iterates on it.

---

## Position in the team

| Agent | Role |
|---|---|
| **Anvil** (this project) | All backend development — server-side foundation for the team |
| Prometheus (CapabilityManagerAgent) | Common-capability backbone + cross-project sync + team registry |

Anvil is independent of the sales pipeline (Scout → Wright → Buzz → Vendy → Echo); it serves the engineering foundation of the whole team.

---

## License & Attribution

Copyright (c) 2026 All Contributors. Licensed under the [MIT License](LICENSE.md).

**Attribution:** If you derive from or redistribute this project, please retain the copyright notice and license file, and credit the source: [BackendEngineerAgent](https://github.com/xhq/BackendEngineerAgent).
