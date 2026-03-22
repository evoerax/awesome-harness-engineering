# Claude Code

> Anthropic's official AI coding agent CLI.

## Overview

Claude Code is Anthropic's native coding agent — the most feature-complete harness with full support for skills, agents, commands, hooks, and plugins.

## Key Features

| Feature | Details |
|---------|---------|
| **Hooks** | 8 event types (PreToolUse, PostToolUse, SessionStart, SessionEnd, Stop, etc.) |
| **Plugins** | Plugin marketplace with `/plugin install` |
| **Agents** | Native subagent support |
| **Commands** | Slash commands (`/command`) |
| **Skills** | Auto-discovered from `.claude/skills/` |
| **Rules** | Always-follow guidelines from `~/.claude/rules/` |
| **MCP** | Model Context Protocol server support |
| **Context** | `CLAUDE.md` + `AGENTS.md` |

## Hook Events

| Event | When |
|-------|------|
| `PreToolUse` | Before tool execution |
| `PostToolUse` | After tool execution |
| `SessionStart` | Session starts (startup/clear/compact) |
| `SessionEnd` | Session ends |
| `Stop` | Agent stops |
| `PreCompact` | Before context compaction |
| `Notification` | Notification events |
| `UserPromptSubmit` | User submits prompt |

## Installation Locations

```
~/.claude/
├── agents/           # Subagent definitions
├── commands/         # Slash commands
├── skills/           # Skills
├── rules/            # Always-follow rules
├── plugins/          # Installed plugins
└── settings.json     # Global settings + hooks
```

## Tools That Support Claude Code

- ✅ Superpowers
- ✅ PUA
- ✅ Get Shit Done
- ✅ Everything Claude Code
- ✅ gstack

## Links

- [Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Plugin Reference](https://code.claude.com/docs/en/plugins-reference)
