# OpenCode

> Open source AI coding agent with rich plugin system.

## Overview

OpenCode has the most sophisticated hook/plugin system with 20+ event types — more than Claude Code. Supports JS plugins with native tools.

## Key Features

| Feature | Details |
|---------|---------|
| **Hooks** | 20+ event types (most of any harness) |
| **Plugins** | JS plugin system (`plugin` field in config) |
| **Native Tools** | 6 built-in tools |
| **Config** | `opencode.json` |
| **Skills** | SKILL.md format |
| **Context** | `AGENTS.md` |

## Hook Events (more than Claude Code)

| OpenCode Event | Claude Code Equivalent |
|---------------|----------------------|
| `tool.execute.before` | PreToolUse |
| `tool.execute.after` | PostToolUse |
| `session.created` | SessionStart |
| `session.deleted` | SessionEnd |
| `session.idle` | Stop |
| `file.edited` | — |
| `file.watcher.updated` | — |
| `message.updated` | — |
| `lsp.client.diagnostics` | — |
| `tui.toast.show` | — |

## Plugin Example

```javascript
export const MyPlugin = async ({ client, directory }) => {
  return {
    config: async (config) => {
      config.skills.paths.push(mySkillsDir);
    },
    'experimental.chat.system.transform': async (_input, output) => {
      output.system.push(myBootstrapContent);
    }
  };
};
```

## Tools That Support OpenCode

- ✅ Superpowers
- ✅ PUA
- ✅ Get Shit Done
- ✅ Everything Claude Code

## Links

- [OpenCode GitHub](https://github.com/nicholasgasior/opencode)
