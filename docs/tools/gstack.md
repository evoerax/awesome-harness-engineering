# gstack

> YC CEO's AI software factory — virtual engineering team.

## Overview

gstack turns Claude Code into a manageable virtual engineering team: CEO, engineering manager, designer, QA, release engineer. Built by YC CEO Garry Tan — 600K+ lines of production code in 60 days.

**GitHub:** https://github.com/garrytan/gstack
**Author:** Garry Tan (YC President & CEO)

## Core Data

| Metric | Value |
|--------|-------|
| Production code | 600K+ lines in 60 days |
| Test coverage | 35% |
| Daily output | 10-20K lines |
| Skills | 21 |

## Workflow

```
Think → Plan → Build → Review → Test → Ship → Reflect
/office-hours → /plan-ceo-review → /plan-eng-review → implementation → /review → /qa → /ship → /retro
```

## 21 Skills

### Core (15)
| Skill | Role |
|-------|------|
| `/office-hours` | YC Office Hours — 6 forcing questions |
| `/plan-ceo-review` | CEO — find hidden 10-star product |
| `/plan-eng-review` | Eng Manager — lock architecture |
| `/plan-design-review` | Senior Designer — 0-10 score |
| `/design-consultation` | Design Partner — design system |
| `/review` | Staff Engineer — find CI-passing bugs |
| `/investigate` | Debugger — systematic root cause |
| `/qa` | QA Lead — real browser testing |
| `/ship` | Release Engineer — test+push+PR |
| `/retro` | Eng Manager — weekly retro |

### Power Tools (6)
| Skill | Function |
|-------|----------|
| `/codex` | OpenAI Codex second opinion |
| `/careful` | Destroy command warnings |
| `/freeze` | Edit lock to one directory |
| `/guard` | careful + freeze combo |
| `/unfreeze` | Remove edit restriction |
| `/gstack-upgrade` | Self-update |

## 3 Unique Features

### 1. Real Browser
Compiled Chromium daemon, persistent state, ~100ms/command.
```bash
$B goto https://staging.app.com
$B screenshot /tmp/check.png
$B diff https://staging.app.com https://prod.app.com
```

### 2. Template Generation
SKILL.md generated from `.tmpl` templates for multi-platform support.

### 3. Wave-Based Sprint
10-15 sprints running in parallel via Conductor. Each sprint is self-contained.

## Boil the Lake Principle

AI makes "complete" cost near-zero. Always choose the complete option.

| Task | Human Team | CC+gstack | Compression |
|------|-----------|-----------|-------------|
| Scaffolding | 2 days | 15 min | ~100x |
| Test writing | 1 day | 15 min | ~50x |
| Feature impl | 1 week | 30 min | ~30x |
| Bug fix | 4 hours | 15 min | ~20x |

## Platform Support

| Platform | Skills | Browser | Full Support |
|----------|:------:|:-------:|:------------:|
| Claude Code | 21 | ✅ | ✅ |
| Codex | 21 | ✅ | ✅ |
| Gemini CLI | 21 | ✅ | ✅ |
| Cursor | 21 | ✅ | ✅ |

## Installation

```bash
git clone https://github.com/garrytan/gstack.git ~/.claude/skills/gstack
cd ~/.claude/skills/gstack && ./setup
```
