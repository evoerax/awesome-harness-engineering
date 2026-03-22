# Awesome Harness Engineering

[English](README.md) | **简体中文**

> 跨平台 AI 编程 Agent 工具精选集 — 适用于 Claude Code、Cursor、Codex、OpenClaw 等。

---

## 这是什么？

AI 编程 Agent 的能力取决于两件事：**运行平台（Harness）** 和 **扩展工具（Tool）**。

本项目探索、对比、记录最好的**工具**（Superpowers、PUA、Get Shit Done 等）和最好的**平台**（Claude Code、Cursor、Codex、OpenClaw 等）。

两个维度：

```
平台（在哪运行）                    工具（做什么）
├── Claude Code                     ├── Superpowers — 工作流引擎（TDD、调试、代码审查）
├── Cursor                          ├── PUA — 压力驱动（不让AI放弃）
├── Codex                           ├── Get Shit Done — 上下文工程 + 规格驱动开发
├── OpenClaw                        ├── Everything Claude Code — 全面优化系统
├── OpenCode                        ├── gstack — 虚拟工程团队（YC CEO 的系统）
├── Gemini CLI                      └── ...
├── Antigravity
└── ...
```

---

## 平台（Harnesses）

AI 编程 Agent 运行的平台。

| 平台 | 维护者 | 核心特点 |
|------|-------|---------|
| [Claude Code](docs/harnesses/claude-code.md) | Anthropic | 原生 hooks、plugins、agents、commands |
| [Cursor](docs/harnesses/cursor.md) | Anysphere | IDE 集成、15+ 种 hook 事件 |
| [Codex](docs/harnesses/codex.md) | OpenAI | AGENTS.md 指令式、沙箱 |
| [OpenClaw](docs/harnesses/openclaw.md) | 社区 | Skill 优先、社区插件 |
| [OpenCode](docs/harnesses/opencode.md) | 社区 | 20+ 种插件事件、原生工具 |
| [Gemini CLI](docs/harnesses/gemini-cli.md) | Google | 扩展系统、GEMINI.md 上下文 |
| [Antigravity](docs/harnesses/antigravity.md) | Google | Skills 优先、基于 Gemini |

→ 详细对比见 [docs/harnesses/](docs/harnesses/)

---

## 工具（Tools）

扩展编程 Agent 的技能、工作流和系统。

| 工具 | Stars | 核心理念 |
|------|-------|---------|
| [Superpowers](docs/tools/superpowers.md) | — | 工作流引擎：TDD + 调试 + 代码审查 |
| [PUA](docs/tools/pua.md) | 350+ | 压力驱动：不让 AI 放弃 |
| [Get Shit Done](docs/tools/get-shit-done.md) | — | 上下文工程：每个任务 fresh context |
| [Everything Claude Code](docs/tools/everything-claude-code.md) | 50K+ | 全面系统：25 agents、108 skills、57 commands |
| [gstack](docs/tools/gstack.md) | — | 虚拟工程团队（YC CEO 的系统） |

→ 深度解析见 [docs/tools/](docs/tools/)

---

## 工具 × 平台 支持矩阵

| 工具 | Claude Code | Cursor | Codex | OpenClaw | OpenCode | Gemini |
|------|:-----------:|:------:|:-----:|:--------:|:--------:|:------:|
| Superpowers | ✅ | ✅ | ✅ | ❌ | ✅ | ✅ |
| PUA | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Get Shit Done | ✅ | ❌ | ✅ | ✅ | ✅ | ✅ |
| Everything Claude Code | ✅ | ✅ | ✅ | ❌ | ✅ | ❌ |
| gstack | ✅ | ✅ | ✅ | ❌ | ❌ | ✅ |

---

## 对比

### 设计哲学

| 工具 | 哲学 |
|------|------|
| Superpowers | "按正确的方式做" — TDD、系统化调试 |
| PUA | "你敢放弃试试" — 压力 + 方法论 |
| Get Shit Done | "告诉我你要什么，我建" — 上下文工程 |
| Everything Claude Code | "给你所有可能需要的" — 完整工具箱 |
| gstack | "像团队一样运作" — 角色分工、CEO 思维 |

### 规模对比

| 工具 | Skills | Agents | Commands | Hooks |
|------|:------:|:------:|:--------:|:-----:|
| Superpowers | 14 | 1 | 3 | 1 |
| PUA | 7 | 3 | 5 | 1 |
| Get Shit Done | — | 16 | 50 | 4 |
| Everything Claude Code | 108 | 25 | 57 | 20+ |
| gstack | 21 | 0 | 21 | 0 |

### 独特能力

| 工具 | 独特能力 |
|------|---------|
| Superpowers | Git worktrees 隔离开发 |
| PUA | 企业压力测试 + Benchmark 数据 |
| Get Shit Done | 波浪式并行执行 + fresh context |
| Everything Claude Code | 持续学习 + AgentShield 安全审计 |
| gstack | 真实浏览器（Chromium daemon，~100ms/命令） |

---

## 项目结构

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

## 贡献

欢迎贡献。添加新工具、更新平台支持、修正错误。

1. Fork 本仓库
2. 添加内容
3. 提交 PR

---

## 许可证

MIT
