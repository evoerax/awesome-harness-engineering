# Get Shit Done (GSD)

> Context engineering + spec-driven development — solve context rot.

## Overview

GSD solves "context rot" — the quality degradation that happens as Claude fills its context window. Each task runs in a fresh 200k context.

**GitHub:** https://github.com/glittercowboy/get-shit-done
**Author:** TÂCHES

## Core Idea

Claude's output quality is proportional to context quality. GSD manages context files and size limits to keep output stable.

## Workflow (5-step loop)

```
/new-project → /discuss-phase → /plan-phase → /execute-phase → /verify-work → /ship
```

1. **Discuss** — Capture implementation decisions
2. **Plan** — Research + create atomic task plans (XML format)
3. **Execute** — Wave-based parallel execution, each plan in fresh context
4. **Verify** — User acceptance testing
5. **Ship** — Create PR

## 4 Core Mechanisms

### 1. Context Engineering
Managed files with size limits based on Claude's quality thresholds.

### 2. Wave-Based Parallel Execution
Independent plans run in parallel, dependent plans in sequence. Each plan gets fresh 200k context.

### 3. XML Structured Plans
```xml
<task type="auto">
  <name>Create login endpoint</name>
  <files>src/api/auth/login.ts</files>
  <action>Use jose for JWT...</action>
  <verify>curl returns 200 + Set-Cookie</verify>
  <done>Valid creds return cookie</done>
</task>
```

### 4. Context Monitor Hook
Injects warnings when context usage is high (35% warning, 25% critical).

## Scale

| Component | Count |
|-----------|-------|
| Commands | 50 |
| Agents | 16 |
| Hooks | 4 |
| Workflows | 49 |

## Platform Support

| Platform | Commands | Agents | Hooks |
|----------|:--------:|:------:|:-----:|
| Claude Code | ✅ | ✅ | ✅ |
| OpenCode | ✅ | ✅ | ❌ |
| Gemini CLI | ✅ | ✅ | ❌ |
| Codex | ✅ | ✅ | ❌ |
| Copilot | ✅ | ✅ | ❌ |
| Antigravity | ✅ | ✅ | ❌ |

## Installation

```bash
npx get-shit-done-cc@latest
# Choose: Runtime + Location
```

Non-interactive:
```bash
npx get-shit-done-cc --claude --global
npx get-shit-done-cc --all --global
```
