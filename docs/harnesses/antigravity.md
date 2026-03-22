# Antigravity

> Google's skills-first AI coding agent, Gemini-based.

## Overview

Antigravity is Google's skills-first coding agent, using Gemini as the underlying model. Supports SKILL.md format and installation via standard directory conventions.

## Key Features

| Feature | Details |
|---------|---------|
| **Hooks** | ❌ |
| **Skills** | SKILL.md format |
| **Config** | `~/.gemini/antigravity/` (global) or `.agent/` (local) |
| **Context** | Antigravity context files |

## Installation

```bash
# Global
mkdir -p ~/.gemini/antigravity/skills/pua
curl -o ~/.gemini/antigravity/skills/pua/SKILL.md ...

# Local
mkdir -p .agent/skills/pua
curl -o .agent/skills/pua/SKILL.md ...

# Via install script
./install.sh --target antigravity typescript
```

## Tools That Support Antigravity

- ✅ PUA
- ✅ Get Shit Done
- ✅ Everything Claude Code

## Links

- Antigravity documentation
