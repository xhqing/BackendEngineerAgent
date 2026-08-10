# CHANGELOG

## [0.1.0] - 2026-08-10

### 新增

- 项目初始化：按 fleet 脚手架约定（2026-07-13 立）新建后端开发工程师 Agent——目录名 `BackendEngineerAgent`、拟人名 **Anvil**（铁砧，匠人系，与 Tinker / Mason 同源）。
- 角色定位：负责所有后端开发工作；目前唯一在手项目为 **CC-BRIDGE**（Claude Code 上游桥接框架，Node.js），由其维护与迭代。
- 项目标配文件齐全：角色化 `CLAUDE.md`、中英双语 `README.md` / `README_cn.md`（含 logo、License / Last Commit / Type 三枚徽章，不含 Stars 数量徽章）、`assets/logo.svg`（Anvil 铁砧主题，蓝色系渐变，与 Prometheus 的橙红区分）、`LICENSE.md`（MIT，版权人归一为 All Contributors）、`.gitignore`、`VERSION`（0.1.0）、`CHANGELOG.md`、`.claude/settings.json` 与 `.claude/settings.local.example.json`（本机配置模板）、`.claude/settings.local.json`（本机，已 gitignore）。
- 不复制通用能力：`.claude/` 不放置 anysearch / find-skill 等通用副本（「通用能力开源单一出口」规则，2026-08-09 立），通用能力一律从全局 `~/.claude/` 或 CapabilityManagerAgent 的 `claude/` 开源镜像获取。
- 新增「子项目 `.claude/` 自动同步」规则（CLAUDE.md 新一节）：本项目 `.claude/` 为权威源，各子项目 `.claude/` 为其超集——本项目 `.claude/` 下除 `CLAUDE.md` 外的内容变更（新增 / 修改 / 删除）后自动同步到所有子项目（当前清单：CC-BRIDGE），子项目独有内容保留不动，同步后 diff 核对；`CLAUDE.md` 各项目独有、不逐字节同步，仅要求子项目含「由 Anvil 负责」的归属说明。原因：确保用户只操作子项目（如 CC-BRIDGE）时，其 `.claude/` 也包含本项目的完整内容，体现项目归 Anvil 负责；超集关系自动维护、不再手工逐次同步。
- 修订「子项目 `.claude/` 自动同步」规则的 `CLAUDE.md` 部分（2026-08-10 用户再立）：从「`CLAUDE.md` 例外（各项目独有、不逐字节同步、只要求归属说明）」改为「**`CLAUDE.md` 内容同样超集**——实现方式不限、效果等价即可：最简单是把本项目 `CLAUDE.md` 内容直接加进子项目 `CLAUDE.md`，也可放子项目 `rules/` 下再 `@` 引用」，总述同步补「`CLAUDE.md` 的内容同样覆盖到子项目」。原因：用户要求 CLAUDE.md 的**所有内容**也保持超集关系，只要效果等价、不限制存放文件；原「例外」表述已不再成立。落实：已将本项目 CLAUDE.md 全文并入 CC-BRIDGE `.claude/CLAUDE.md`（带指代说明「本项目指 BackendEngineerAgent」、标题降级为 `###` 避免层级冲突）。
