# offload-blockers

Offload incidental blockers to a sub-agent so the main agent can stay on architecture, product behavior, and final integration.

## What it does

This skill is for tasks that are blocked by incidental execution work rather than product work.
Use it when the immediate problem is runtime setup, dependencies, build or test harnesses,
browser automation, local services, containers, fixtures, generated artifacts, or
machine-specific toolchain issues.

## Example prompts

This skill is configured for implicit invocation. Because it is designed to
trigger automatically, users do not need to call it explicitly, so example
prompts are not required here.

## Installation

Fastest path for any agent: Send this repository link to your agent and ask it to install the skill.

### Option 1: clone into the Codex skills directory

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/Walaxy/offload-blockers.git "${CODEX_HOME:-$HOME/.codex}/skills/offload-blockers"
```

After installation, restart Codex or open a new session so the skill is discovered.

## Use with other coding agents

This repository is a Codex skill. Other agents do not load it natively, so use
the repository as the source of truth and map it to the agent's own instruction
format.

### Claude Code

Clone or open this repository in your workspace, then ask Claude Code to read
`SKILL.md`. If you want persistent project instructions, copy the behavior into
`CLAUDE.md` or a project subagent under `.claude/agents/`.

### Cursor

Clone or open this repository in your workspace, then ask Cursor to read
`SKILL.md`. Mirror the behavior in `.cursor/rules` or `AGENTS.md`.

### Any other agent

Send this repository link to your agent and ask it to install the skill in its
own instruction system. If it supports project instructions, copy the decision
rule, common blockers, delegation protocol, and boundary rules from `SKILL.md`.

### Pi and similar agents

Use the same approach: give the agent this repository link, ask it to read
`SKILL.md`, and then place the extracted behavior into whatever project-level
instruction mechanism it supports.

## Repository structure

- `SKILL.md`: skill behavior and decision rules
- `agents/openai.yaml`: UI metadata
- `README.md`: GitHub-facing overview and examples

## Notes

This repository is intentionally small. The skill logic lives in `SKILL.md`;
this README is only for humans browsing the GitHub repo.

---

# offload-blockers

将零碎阻塞项委派给 sub-agent，让主 agent 保持在架构、产品行为和最终集成上。

## 功能说明

这个 skill 用于处理执行层阻塞，而不是产品层工作。
当当前问题是运行时配置、依赖安装、构建或测试 harness、浏览器自动化、
本地服务、容器、fixtures、生成产物，或者机器相关的工具链问题时使用。

## 示例提示词

由于这个 skill 已配置为自动触发，用户无需显式调用，因此这里不需要保留
示例提示词。

## 安装方式

最快捷的方式：把这个仓库链接发送给你的 agent，让它安装这个 skill。

### 方式一：克隆到 Codex skills 目录

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/Walaxy/offload-blockers.git "${CODEX_HOME:-$HOME/.codex}/skills/offload-blockers"
```

安装后，重启 Codex 或打开一个新会话，让 skill 被重新发现。

## 与其他 coding agents 配合使用

这个仓库是面向 Codex 的 skill。其他 agent 不能原生加载它，因此请把
本仓库作为唯一事实来源，再映射到各自的指令系统中。

### Claude Code

先把这个仓库克隆到你的工作区，或者直接让 Claude Code 读取
`SKILL.md`。如果你希望有持久的项目指令，可以把相关行为复制到
`CLAUDE.md`，或者放进 `.claude/agents/` 里的项目 subagent。

### Cursor

先把这个仓库克隆到你的工作区，或者直接让 Cursor 读取 `SKILL.md`。
然后把相同的行为写入 `.cursor/rules` 或 `AGENTS.md`。

### 其他任何 agent

把这个仓库链接发送给你的 agent，让它在自己的指令系统里安装这个 skill。
如果它支持项目级指令，就把 `SKILL.md` 里的决策规则、常见阻塞项、委派流程
和边界规则复制过去。

### Pi 和类似的 agent

做法相同：把这个仓库链接发给 agent，让它读取 `SKILL.md`，然后把提炼出的
行为写入它支持的项目级指令系统。

## 仓库结构

- `SKILL.md`：skill 行为和决策规则
- `agents/openai.yaml`：UI 元数据
- `README.md`：给 GitHub 浏览者看的概览和示例

## 说明

这个仓库刻意保持精简。skill 逻辑定义在 `SKILL.md` 中；
这个 README 只用于 GitHub 仓库浏览。
