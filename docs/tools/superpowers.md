# Superpowers

> Workflow engine for coding agents — TDD, debugging, code review.

## Overview

Superpowers gives coding agents a structured workflow: brainstorm → plan → TDD → debug → review → ship. Not just configs — a complete methodology.

**GitHub:** https://github.com/obra/superpowers

## Core Idea

Agent doesn't write code directly. Instead:
1. Step back — "What do you actually want?"
2. Discuss requirements
3. Break into small tasks
4. TDD each task
5. Auto code review
6. Merge

## 14 Skills

| Category | Skills |
|----------|--------|
| **Collaboration** | brainstorming, writing-plans, executing-plans, dispatching-parallel-agents |
| **Testing** | test-driven-development (RED-GREEN-REFACTOR) |
| **Debugging** | systematic-debugging, verification-before-completion |
| **Review** | requesting-code-review, receiving-code-review |
| **Git** | using-git-worktrees, finishing-a-development-branch |
| **Meta** | writing-skills, using-superpowers |

## Unique Feature

**Git Worktrees** — isolated development in separate branches without affecting the main workspace.

## Platform Support

| Platform | Skills | Commands | Agents | Hooks |
|----------|:------:|:--------:|:------:|:-----:|
| Claude Code | ✅ | ✅ | ✅ | ✅ |
| Cursor | ✅ | ✅ | ✅ | ✅ |
| OpenCode | ✅ | ❌ | ❌ | ❌ |
| Codex | ✅ | ❌ | ❌ | ❌ |
| Gemini CLI | ✅ | ❌ | ❌ | ❌ |

## Installation

### Claude Code
```bash
/plugin marketplace add obra/superpowers-marketplace
/plugin install superpowers@superpowers-marketplace
```

### Cursor
```text
/add-plugin superpowers
```

### OpenCode
```json
{ "plugin": ["superpowers@git+https://github.com/obra/superpowers.git"] }
```

### Codex
```bash
git clone https://github.com/obra/superpowers.git ~/.codex/superpowers
ln -s ~/.codex/superpowers/skills ~/.agents/skills/superpowers
```

### Gemini CLI
```bash
gemini extensions install https://github.com/obra/superpowers
```
