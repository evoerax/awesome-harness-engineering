# Everything Claude Code (ECC)

> Full optimization system — 50K+ stars, Anthropic Hackathon Winner.

## Overview

ECC is a complete AI agent harness optimization system. Not just configs — a full toolbox: skills, agents, commands, hooks, rules, MCP, and continuous learning.

**GitHub:** https://github.com/affaan-m/everything-claude-code
**Stars:** 50K+ | **Forks:** 6K+

## Scale

| Component | Count |
|-----------|-------|
| Agents | 25 |
| Skills | 108 |
| Commands | 57 |
| Hook Events | 20+ |
| Rules | 34 (5 languages) |
| MCP Servers | 14 |
| Internal Tests | 997 |

## 4 Unique Mechanisms

### 1. Continuous Learning v2
Agent learns patterns from sessions automatically.
```
Session → extract patterns → Instinct + confidence score → cluster into Skill
```

### 2. AgentShield
Security auditor built at Claude Code Hackathon. 1282 tests, 102 rules.
```bash
npx ecc-agentshield scan          # Quick scan
npx ecc-agentshield scan --opus   # Red team / blue team / auditor
```

### 3. Hook System (20+ events)
Most comprehensive hook system of any harness. Cross-platform DRY adapter.

### 4. Plankton
Write-time code quality enforcement. Runs 20+ linters on every file edit.

## Languages Supported

TypeScript, Python, Go, Rust, Java/Spring Boot, Kotlin, Swift, Perl, C++, PHP, Django, Laravel

## Platform Support

| Platform | Agents | Commands | Skills | Hooks |
|----------|:------:|:--------:|:------:|:-----:|
| Claude Code | 25 | 57 | 108 | 20+ |
| Cursor | Shared | Shared | Shared | 15 |
| Codex | Shared | Instruction | 10 | ❌ |
| OpenCode | 12 | 31 | 37 | 11 |

## Installation

```bash
# Plugin
/plugin marketplace add affaan-m/everything-claude-code
/plugin install everything-claude-code@everything-claude-code

# Rules (must install manually)
git clone https://github.com/affaan-m/everything-claude-code.git
cd everything-claude-code
./install.sh typescript    # Choose language(s)

# OpenCode
npm install ecc-universal
```
