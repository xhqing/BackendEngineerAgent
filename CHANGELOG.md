# CHANGELOG

## [Unreleased]

### 变更（CLAUDE.md 删去「由 Claude Code 自动加载」说明句）

- **为什么改**：用户 2026-09-12 要求 CLAUDE.md 不再强调本文由 Claude Code 加载，团队全部项目的 CLAUDE.md 统一清理此类语句。
- **改了什么**（2026-09-12）：`.claude/CLAUDE.md` 开头角色定位行删去句尾「本文件由 Claude Code 在每次会话开头自动加载。」，角色描述本身保留。

### 变更（全局规则路径与通用能力句式更新：rules 废弃 + find-skill 删除联动）

- **为什么改**：①全局通用规则已全部迁入 `~/.claude/CLAUDE.md`、`~/.claude/rules/` 目录废弃，本项目两处指向旧目录的引用失效；②全局 find-skill skill 已删（实际使用中从未用到），通用能力句式不再提及。均系 2026-09-12 用户指出后的联动清理。
- **改了什么**：`.claude/CLAUDE.md`：①「遵守通用工作规则（见全局 `~/.claude/rules/`）」与「通用工作纪律（三个规则文件名）见全局 `~/.claude/rules/`」两处改指 `~/.claude/CLAUDE.md`（三个规则文件已随目录废弃并入全局 CLAUDE.md，文件名列表一并移除）；②「（anysearch 实时搜索、find-skill 找 skill 等）」→「（anysearch 实时搜索等）」。子项目 CC-Bridge 副本已按超集规则同步（不另记其 CHANGELOG）。

### 变更（README 移除 Last Commit 动态徽章：徽章组合合规清理）

- **为什么改**：commit skill 第 9l 步检测（2026-09-09）——徽章规矩为静态徽章（License / Version / Type），Last Commit 属 GitHub 动态时间徽章、随仓库变动、不在允许范围；Visits/day (14d) 访问量徽章为团队集中部署的 endpoint 例外、保留不动。
- **改了什么**：README.md 与 README_cn.md 徽章区各删除 Last Commit 徽章一行，其余徽章与正文不变。

### 变更（项目迁移收尾：CLAUDE.md 子项目清单路径更新）

- **为什么改**：项目现址在 `~/Developer/`（`~/Documents/Projects/` 旧址已弃用，2026-09-08 迁移收尾时发现子项目清单仍指旧路径 `~/Documents/Projects/CC-BRIDGE`），避免后续会话被引导到不存在的位置。
- **改了什么**：`.claude/CLAUDE.md` 子项目清单中 CC-Bridge 路径更新为 `~/Developer/CC-Bridge`（大小写同时修正为现目录名）；子项目 CC-Bridge 仓库内 `.claude/CLAUDE.md` 的同款行已同步更新（超集关系保持一致）。

### 变更（措辞统一 fleet → team / 舰队 → 团队：README 中英双语 + logo 措辞跟随全局统一）

- **为什么改**：用户 2026-08-16 已把 xhqing 主页 README 的自称从「舰队 / fleet」改为「团队 / team」，但本仓 README 中英两版与 logo 副标题仍是 fleet 旧措辞——外部读者沿「主页 → 各 agent 仓库」浏览会看到两种自称并存；2026-08-21 用户裁定全 fleet 存量一次清零、统一为团队 / team。
- **改了什么**：`README.md` 5 处 fleet → team（Anvil 引言、owns 句、Position in the fleet 节标题及表内 2 处、末段）；`README_cn.md` 对应 5 处舰队 / fleet → 团队（「在 fleet 中的位置」→「在团队中的位置」等）；`assets/logo.svg` 副标题「Server-side foundation for the fleet」→「for the team」。仅改措辞，职责、结构、徽章均不变。

### 变更（Visitors 徽章更名 Visits/day (14d)：alt 文本与 xhqing 集中统计新 label 对齐）

- **为什么改**：用户要求（2026-08-17）访问量徽章名需表达「最近半月日均访问量」口径——xhqing 集中统计侧的 badge JSON label 已从 `Visitors` 改为 `Visits/day (14d)`（`Visits/day` 是 shields.io 表达日均的惯例写法、`(14d)` 标注 14 天滚动窗口），各仓 README 的徽章 alt 文本同步对齐，避免 alt 与徽章实际显示文字脱节。
- **改了什么**：README 徽章区 `alt="Visitors"` → `alt="Visits/day (14d)"`，仅改 alt 文本，endpoint URL、数据源、徽章口径均不变（口径改动记 xhqing 仓库 CHANGELOG，本仓只改 alt）。

## [0.1.0] - 2026-08-10

### 变更（Visitors 徽章 alt 文本首字母大写：README 访问量徽章命名统一）

- **为什么改**：用户指令（2026-08-16）「Visitors 徽章全局统一，首字母大写」——配合全局 `~/.claude/CLAUDE.md`「徽章英文首字母必须大写」新规，集中统计上线时挂的访问量徽章 `alt="visitors"` 为小写存量，与 badge JSON label（`Visits/day`）及大写规范不一致，本次一次收口。
- **改了什么**：README（EN/CN）徽章区 visitors 徽章 `alt="visitors"` → `alt="Visitors"`，仅改 alt 显示文本，endpoint URL 与数据源不变。

### 新增（README 访问量徽章——舰队集中式访问统计）

- **为什么改**：全舰队上线集中式「真去重」访问统计（图片徽章方案无法去重，走官方 Traffic API 路线）：统计集中部署在 xhqing 仓库（`scripts/update_traffic.py` + 每日 GitHub Action），各 fleet 仓库只需在 README 挂徽章、零运行负担。
- **改了什么**：README（EN/CN）徽章区新增 visitors 徽章（shields.io endpoint 指向 `xhqing/xhqing` 仓库 `traffic/badges/<repo>.json`，由每日采集的官方 Traffic API 数据更新）。徽章数字含义：按日去重访客的累计（GitHub 只提供每日 uniques，跨天不去重），自 2026-08-16 起累计。

### 新增

- 项目初始化：按 fleet 脚手架约定（2026-07-13 立）新建后端开发工程师 Agent——目录名 `BackendEngineerAgent`、拟人名 **Anvil**（铁砧，匠人系，与 Tinker / Mason 同源）。
- 角色定位：负责所有后端开发工作；目前唯一在手项目为 **CC-BRIDGE**（Claude Code 上游桥接框架，Node.js），由其维护与迭代。
- 项目标配文件齐全：角色化 `CLAUDE.md`、中英双语 `README.md` / `README_cn.md`（含 logo、License / Last Commit / Type 三枚徽章，不含 Stars 数量徽章）、`assets/logo.svg`（Anvil 铁砧主题，蓝色系渐变，与 Prometheus 的橙红区分）、`LICENSE.md`（MIT，版权人归一为 All Contributors）、`.gitignore`、`VERSION`（0.1.0）、`CHANGELOG.md`、`.claude/settings.json` 与 `.claude/settings.local.example.json`（本机配置模板）、`.claude/settings.local.json`（本机，已 gitignore）。
- 不复制通用能力：`.claude/` 不放置 anysearch / find-skill 等通用副本（「通用能力开源单一出口」规则，2026-08-09 立），通用能力一律从全局 `~/.claude/` 或 CapabilityManagerAgent 的 `claude/` 开源镜像获取。
- 新增「子项目 `.claude/` 自动同步」规则（CLAUDE.md 新一节）：本项目 `.claude/` 为权威源，各子项目 `.claude/` 为其超集——本项目 `.claude/` 下除 `CLAUDE.md` 外的内容变更（新增 / 修改 / 删除）后自动同步到所有子项目（当前清单：CC-BRIDGE），子项目独有内容保留不动，同步后 diff 核对；`CLAUDE.md` 各项目独有、不逐字节同步，仅要求子项目含「由 Anvil 负责」的归属说明。原因：确保用户只操作子项目（如 CC-BRIDGE）时，其 `.claude/` 也包含本项目的完整内容，体现项目归 Anvil 负责；超集关系自动维护、不再手工逐次同步。
- 修订「子项目 `.claude/` 自动同步」规则的 `CLAUDE.md` 部分（2026-08-10 用户再立）：从「`CLAUDE.md` 例外（各项目独有、不逐字节同步、只要求归属说明）」改为「**`CLAUDE.md` 内容同样超集**——实现方式不限、效果等价即可：最简单是把本项目 `CLAUDE.md` 内容直接加进子项目 `CLAUDE.md`，也可放子项目 `rules/` 下再 `@` 引用」，总述同步补「`CLAUDE.md` 的内容同样覆盖到子项目」。原因：用户要求 CLAUDE.md 的**所有内容**也保持超集关系，只要效果等价、不限制存放文件；原「例外」表述已不再成立。落实：已将本项目 CLAUDE.md 全文并入 CC-BRIDGE `.claude/CLAUDE.md`（带指代说明「本项目指 BackendEngineerAgent」、标题降级为 `###` 避免层级冲突）。
