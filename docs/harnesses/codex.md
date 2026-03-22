# Codex

> OpenAI's AI coding agent — CLI and macOS app.

## Overview

Codex uses `AGENTS.md` for instruction-based configuration. No native hook support yet — enforcement is via instructions and sandbox settings. Supports multi-agent workflows.

## Key Features

| Feature | Details |
|---------|---------|
| **Hooks** | ❌ Not yet (instruction-based) |
| **Config** | `.codex/config.toml` |
| **Agents** | AGENTS.md + `.codex/agents/` role files |
| **Skills** | `.agents/skills/` (SKILL.md format) |
| **MCP** | Command-based MCP servers |
| **Sandbox** | Strict/yolo profiles |
| **Context** | `AGENTS.md` |

## Multi-Agent

```toml
[features]
multi_agent = true

[agents.explorer]
description = "Read-only codebase evidence gathering"

[agents.reviewer]
description = "Correctness, security, and test review"
```

## Installation Locations

```
~/.codex/
├── config.toml       # Top-level config
├── agents/           # Agent role definitions
└── skills/           # Skills (SKILL.md)
```

## Tools That Support Codex

- ✅ Superpowers
- ✅ PUA
- ✅ Get Shit Done
- ✅ Everything Claude Code
- ✅ gstack

## Links

- [Codex GitHub](https://github.com/openai/codex)
