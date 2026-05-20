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

**Fastest path for any agent**: Send this repository link to your agent and ask it to install the skill.

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/Walaxy/offload-blockers.git "${CODEX_HOME:-$HOME/.codex}/skills/offload-blockers"
```

After installation, restart Codex or open a new session so the skill is discovered.

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

**最快捷的方式**：把这个仓库链接发送给你的 agent，让它安装这个 skill。

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/Walaxy/offload-blockers.git "${CODEX_HOME:-$HOME/.codex}/skills/offload-blockers"
```

安装后，重启 Codex 或打开一个新会话，让 skill 被重新发现。

## 仓库结构

- `SKILL.md`：skill 行为和决策规则
- `agents/openai.yaml`：UI 元数据
- `README.md`：给 GitHub 浏览者看的概览和示例

## 说明

这个仓库刻意保持精简。skill 逻辑定义在 `SKILL.md` 中；
这个 README 只用于 GitHub 仓库浏览。
