# Cursor

> AI-first code editor by Anysphere.

## Overview

Cursor is an IDE-based harness with deep VS Code integration. It supports more hook events than Claude Code (15+ vs 8), with rules using YAML frontmatter + globs format.

## Key Features

| Feature | Details |
|---------|---------|
| **Hooks** | 15+ event types (more than Claude Code) |
| **Rules** | YAML frontmatter with `globs` and `alwaysApply` |
| **Agents** | Via `AGENTS.md` at root |
| **Skills** | Shared + bundled in `.cursor/skills/` |
| **Commands** | `.cursor/commands/` |
| **MCP** | `.cursor/mcp.json` |
| **Context** | `AGENTS.md` |

## Hook Events (15+)

| Event | When |
|-------|------|
| `sessionStart` | Session starts |
| `beforeShellExecution` | Before running shell commands |
| `afterFileEdit` | After file edit |
| `beforeMCPExecution` | Before MCP tool call |
| `afterMCPExecution` | After MCP tool call |
| `beforeSubmitPrompt` | Before prompt submission |
| `beforeTabFileRead` | Before tab file read |
| ... | and more |

## Rules Format

```yaml
---
description: "TypeScript coding style"
globs: ["**/*.ts", "**/*.tsx"]
alwaysApply: false
---
```

## Installation Locations

```
~/.cursor/
├── rules/            # Rules (YAML frontmatter)
├── commands/         # Commands
├── skills/           # Skills
├── hooks/            # Hook scripts
└── mcp.json          # MCP config
```

## Tools That Support Cursor

- ✅ Superpowers
- ✅ PUA
- ✅ Everything Claude Code
- ✅ gstack

## Links

- [Cursor Website](https://cursor.com)
