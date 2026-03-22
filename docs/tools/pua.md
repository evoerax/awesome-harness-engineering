# PUA

> Stress-driven problem solving — don't let AI give up.

## Overview

PUA uses enterprise pressure techniques to force AI agents to exhaust all solutions before giving up. Named after Chinese workplace "PUA" culture — systematic pressure + structured methodology.

**GitHub:** https://github.com/tanweai/pua
**Stars:** 350+

## Core Idea

AI has 5 bad patterns:
- **Brute force retry** — same command 3 times, then "I can't solve this"
- **Blame shifting** — "Try manual handling" / "Might be an environment issue"
- **Tool neglect** — has WebSearch but doesn't search
- **Spinning wheels** — tweaks same line, no real progress
- **Passive waiting** — fixes surface issue, waits for user

## 3 Iron Rules

1. **Exhaust everything** — no "can't solve" before trying all methods
2. **Act first, ask later** — use tools first, questions must include diagnostic results
3. **Be proactive** — end-to-end delivery, don't wait for user

## 4-Level Pressure Escalation

| Failures | Level | PUA Talk | Action |
|----------|-------|----------|--------|
| 2x | L1 | "You can't even fix this bug, how can I give you a bonus?" | Switch to fundamentally different approach |
| 3x | L2 | "What's the underlying logic? Where's the handle?" | Search + read source + list 3 hypotheses |
| 4x | L3 | "I'm giving you 3.25. This 3.25 is to motivate you." | 7-item checklist + 3 new hypotheses |
| 5x+ | L4 | "Other models can solve this. You might be graduating soon." | Panic mode: minimal PoC + isolated env |

## 12 Enterprise Flavor Packs

| Flavor | Source | Example Quote |
|--------|--------|--------------|
| 🟠 Alibaba | 阿里巴巴 | "底层逻辑、闭环、owner意识" |
| 🟡 ByteDance | 字节跳动 | "ROI算过了吗？追求极致" |
| 🔴 Huawei | 华为 | "烧不死的鸟是凤凰" |
| 🟢 Tencent | 腾讯 | "赛马机制，赛不过就换一匹" |
| ⚫ Baidu | 百度 | "你不是个AI模型吗？深度搜索了吗？" |
| 🟣 PDD | 拼多多 | "你不干，有的是人替你干" |
| 🔵 Meituan | 美团 | "做难而正确的事" |
| 🟦 JD | 京东 | "别跟我讲过程，我只看结果" |
| 🟧 Xiaomi | 小米 | "永远相信美好的事情即将发生" |
| 🟤 Netflix | Netflix | "Keeper Test — would I fight to keep you?" |
| ⬛ Musk | Elon Musk | "Extremely hardcore. Ship or die." |
| ⬜ Jobs | Steve Jobs | "A players hire A players." |

## Benchmark (18 experiments)

| Metric | Improvement |
|--------|-------------|
| Fix count | **+36%** |
| Verification | **+65%** |
| Hidden issues found | **+50%** |

## Platform Support

| Platform | Skills | Commands | Agents | Hooks |
|----------|:------:|:--------:|:------:|:-----:|
| Claude Code | ✅ | ✅ | ✅ | ✅ |
| Cursor | ✅ | ❌ | ❌ | ❌ |
| Codex | ✅ | ✅ | ❌ | ❌ |
| OpenCode | ✅ | ❌ | ❌ | ❌ |
| OpenClaw | ✅ | ❌ | ❌ | ❌ |
| Gemini CLI | ✅ | ❌ | ❌ | ❌ |
| VSCode Copilot | ✅ | ✅ | ❌ | ❌ |
| Kiro | ✅ | ❌ | ❌ | ❌ |
| CodeBuddy | ✅ | ❌ | ❌ | ❌ |

## Installation

### Claude Code
```bash
claude plugin marketplace add tanweai/pua
claude plugin install pua@pua-skills
```

### Others
```bash
# SKILL.md installation
mkdir -p ~/.config/opencode/skills/pua
curl -o ~/.config/opencode/skills/pua/SKILL.md \
  https://raw.githubusercontent.com/tanweai/pua/main/skills/pua/SKILL.md
```
