---
name: offload-blockers
description: "Offload incidental blockers to a sub-agent so the main agent can stay focused on architecture, product behavior, and final integration. Use when the main task is blocked by incidental execution work: runtime setup, dependencies, build or test harnesses, browser automation, local services, containers, fixtures, generated artifacts, or machine-specific toolchain issues."
---

# Offload Blockers

Use this skill to keep incidental execution problems out of the main agent's context. Treat setup, tooling, and harness failures as delegated blockers unless they affect the product design, correctness, or user-visible behavior.

## Decision Rule

Offload the work when the next step is primarily to make something run.

Keep the work in the main agent when the next step changes architecture, business logic, security posture, data contracts, public APIs, or user-facing behavior.

## Common Blockers

- Missing or incompatible runtime versions, packages, browsers, drivers, CLIs, or system tools.
- Failed commands involving `python3`, `pip`, `node`, `npm`, `pnpm`, `bun`, `playwright`, `docker`, `brew`, `xcode-select`, or local services.
- Configuration gaps in test runners, browser automation, mock servers, fixtures, ports, environment variables, permissions, certificates, or proxies.
- Test execution failures where the immediate issue is harness setup rather than application behavior.

## Delegation Protocol

1. State the intended outcome and the blocker in one sentence.
2. Provide only the minimum local context: repository path, failed command, key error lines, and expected success condition.
3. Limit the sub-agent's scope to clearing the blocker.
4. Require the sub-agent to report commands run, files changed, validation performed, and any remaining blocker.

Prefer an `explorer` for read-only diagnosis. Prefer a `worker` for an isolated setup fix or test-harness patch. Do not delegate broad refactors or design decisions.

## Boundaries

- Do not let the delegated agent change architecture, domain logic, API contracts, or security-sensitive behavior.
- If the blocker requires product-code changes, bring the decision back to the main agent before editing.
- If the delegated attempt starts expanding into unrelated cleanup, stop and narrow the task.
- If the blocker is resolved, return immediately to the main agent's original objective.

## Result Handling

Use the delegated result as an implementation detail, not as a new workstream. Integrate only the parts needed to unblock the original task. Keep the final user-facing summary focused on the original objective, with blocker-handling details limited to commands, changed files, and remaining risks when relevant.
