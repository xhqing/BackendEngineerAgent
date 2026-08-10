# CHANGELOG

## [0.1.0] - 2026-08-10

### 新增

- 项目初始化：按 fleet 脚手架约定（2026-07-13 立）新建后端开发工程师 Agent——目录名 `BackendEngineerAgent`、拟人名 **Anvil**（铁砧，匠人系，与 Tinker / Mason 同源）。
- 角色定位：负责所有后端开发工作；目前唯一在手项目为 **CC-BRIDGE**（Claude Code 上游桥接框架，Node.js），由其维护与迭代。
- 项目标配文件齐全：角色化 `CLAUDE.md`、中英双语 `README.md` / `README_cn.md`（含 logo、License / Last Commit / Type 三枚徽章，不含 Stars 数量徽章）、`assets/logo.svg`（Anvil 铁砧主题，蓝色系渐变，与 Prometheus 的橙红区分）、`LICENSE.md`（MIT，版权人归一为 All Contributors）、`.gitignore`、`VERSION`（0.1.0）、`CHANGELOG.md`、`.claude/settings.json` 与 `.claude/settings.local.example.json`（本机配置模板）、`.claude/settings.local.json`（本机，已 gitignore）。
- 不复制通用能力：`.claude/` 不放置 anysearch / find-skill 等通用副本（「通用能力开源单一出口」规则，2026-08-09 立），通用能力一律从全局 `~/.claude/` 或 CapabilityManagerAgent 的 `claude/` 开源镜像获取。
