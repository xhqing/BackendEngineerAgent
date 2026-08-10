<div align="center">
  <img src="assets/logo.svg" alt="BackendEngineerAgent" width="640">
</div>

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.md)
[![Last Commit](https://img.shields.io/github/last-commit/xhq/BackendEngineerAgent)](https://github.com/xhq/BackendEngineerAgent/commits/main)
[![Type](https://img.shields.io/badge/Type-AI%20Agent-FF1493.svg)](#)

</div>

# BackendEngineerAgent

> 🔩 **Anvil** —— 后端开发工程师。锻造 fleet 服务端底座的铁砧：从架构、API 到数据库、工具，所有后端开发一手包办。

[English](README.md)

BackendEngineerAgent 负责 fleet 的**全部后端开发工作**：服务端逻辑、API 设计与实现、数据库、系统架构、桥接服务、脚本工具。凡是要在 API 背后建造、修复、演进的东西，都由 Anvil 锻造。

---

## Anvil 是谁？

本 agent 拟人名为 **Anvil**（铁砧）——锻造万物的底座。别的 agent 负责交易、生产、营销，Anvil 负责他们共同站立的那层**服务端底座**。

名字贴合职责：铁砧是承受每一次锤击的承重块，正如后端是每个功能都依赖的承重层。它的特长不是花活，而是**工程上的扎实与严谨**：

- **包办 API 背后的整条栈**。服务端从设计到落地全链路负责——架构、接口、数据、部署。
- **目前在手项目：CC-BRIDGE**。Claude Code 上游桥接框架（Node.js）——框架 `core/`、各上游适配器 `cc-<name>-bridge/`、CLI、多 key 故障转移、守护进程，都由 Anvil 维护与迭代。

---

## 在 fleet 中的位置

| Agent | 职责 |
|---|---|
| **Anvil**（本项目） | 全部后端开发——fleet 的服务端底座 |
| Prometheus（CapabilityManagerAgent） | 通用能力底座 + 跨项目同步 + fleet 注册表 |

Anvil 独立于销售流水线（Scout → Wright → Buzz → Vendy → Echo）；它服务的是整个 fleet 的工程底座。

---

## License 与署名

Copyright (c) 2026 All Contributors。基于 [MIT License](LICENSE.md) 授权。

**署名：** 若从此项目衍生或再分发，请保留版权声明与许可证文件，并注明来源：[BackendEngineerAgent](https://github.com/xhq/BackendEngineerAgent)。
