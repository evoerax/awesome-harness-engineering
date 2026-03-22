# Awesome Harness Engineering

**English** | [简体中文](README.zh-CN.md)

> Curated collection of AI coding agent tools designed to work across harnesses — Claude Code, Cursor, Codex, OpenClaw, and beyond.

---

## What is this?

AI coding agents are only as good as the harness they run in — and the tools that extend them.

This repo explores, compares, and documents the best **tools** (Superpowers, PUA, Get Shit Done, etc.) that run on top of the best **harnesses** (Claude Code, Cursor, Codex, OpenClaw, etc.).

Two dimensions:

```
Harnesses (where they run)          Tools (what they do)
├── Claude Code                     ├── Superpowers — workflow engine (TDD, debugging, code review)
├── Cursor                          ├── PUA — stress-driven problem solving (企业PUA话术)
├── Codex                           ├── Get Shit Done — context engineering + spec-driven dev
├── OpenClaw                        ├── Everything Claude Code — full optimization system
├── OpenCode                        ├── gstack — virtual engineering team (YC CEO's system)
├── Gemini CLI                      └── ...
├── Antigravity
└── ...
```

---

## Harnesses

The platforms where AI coding agents run.

| Harness | Maintainer | Key Feature |
|---------|-----------|-------------|
| [Claude Code](docs/harnesses/claude-code.md) | Anthropic | Native hooks, plugins, agents, commands |
| [Cursor](docs/harnesses/cursor.md) | Anysphere | IDE integration, 15+ hook events |
| [Codex](docs/harnesses/codex.md) | OpenAI | AGENTS.md instruction-based, sandbox |
| [OpenClaw](docs/harnesses/openclaw.md) | Community | Skill-first, community plugins |
| [OpenCode](docs/harnesses/opencode.md) | Community | 20+ plugin events, native tools |
| [Gemini CLI](docs/harnesses/gemini-cli.md) | Google | Extension system, GEMINI.md context |
| [Antigravity](docs/harnesses/antigravity.md) | Google | Skills-first, Gemini-based |

→ See [docs/harnesses/](docs/harnesses/) for detailed comparisons.

---

## Tools

The skills, workflows, and systems that extend coding agents.

| Tool | Stars | Core Idea |
|------|-------|-----------|
| [Superpowers](docs/tools/superpowers.md) | — | Workflow engine: TDD + debugging + code review |
| [PUA](docs/tools/pua.md) | 350+ | Stress-driven: don't let AI give up |
| [Get Shit Done](docs/tools/get-shit-done.md) | — | Context engineering: fresh context per task |
| [Everything Claude Code](docs/tools/everything-claude-code.md) | 50K+ | Full system: 25 agents, 108 skills, 57 commands |
| [gstack](docs/tools/gstack.md) | — | Virtual engineering team (YC CEO's system) |

→ See [docs/tools/](docs/tools/) for deep dives.

---

## Tool × Harness Support Matrix

| Tool | Claude Code | Cursor | Codex | OpenClaw | OpenCode | Gemini |
|------|:-----------:|:------:|:-----:|:--------:|:--------:|:------:|
| Superpowers | ✅ | ✅ | ✅ | ❌ | ✅ | ✅ |
| PUA | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Get Shit Done | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ |
| Everything Claude Code | ✅ | ✅ | ✅ | ❌ | ✅ | ❌ |
| gstack | ✅ | ✅ | ✅ | ❌ | ❌ | ✅ |

---

## Comparison

### By Philosophy

| Tool | Philosophy |
|------|-----------|
| Superpowers | "Do it the right way" — TDD, systematic debugging |
| PUA | "Don't you dare give up" — stress + method |
| Get Shit Done | "Tell me what you want, I'll build it" — context engineering |
| Everything Claude Code | "Here's everything you might need" — full toolbox |
| gstack | "Act like a team" — role-based, CEO-level thinking |

### By Scale

| Tool | Skills | Agents | Commands | Hooks |
|------|:------:|:------:|:--------:|:-----:|
| Superpowers | 14 | 1 | 3 | 1 |
| PUA | 7 | 3 | 5 | 1 |
| Get Shit Done | — | 16 | 50 | 4 |
| Everything Claude Code | 108 | 25 | 57 | 20+ |
| gstack | 21 | 0 | 21 | 0 |

### By Unique Feature

| Tool | Unique Feature |
|------|---------------|
| Superpowers | Git worktrees for isolated development |
| PUA | Enterprise stress-testing (企业PUA话术) + Benchmark data |
| Get Shit Done | Wave-based parallel execution + fresh context |
| Everything Claude Code | Continuous learning + AgentShield security |
| gstack | Real browser (Chromium daemon, ~100ms/command) |

---

## Project Structure

```
awesome-harness-engineering/
├── README.md
├── README.zh-CN.md
└── docs/
    ├── harnesses/
    │   ├── claude-code.md
    │   ├── cursor.md
    │   ├── codex.md
    │   ├── openclaw.md
    │   ├── opencode.md
    │   ├── gemini-cli.md
    │   └── antigravity.md
    └── tools/
        ├── superpowers.md
        ├── pua.md
        ├── get-shit-done.md
        ├── everything-claude-code.md
        └── gstack.md
```

---

## Contributing

Contributions welcome. Add new tools, update platform support, fix inaccuracies.

1. Fork the repo
2. Add your content
3. Submit a PR

---

## License

MIT
