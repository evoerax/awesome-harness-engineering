# Context Engineering

Solve context rot — the quality degradation as Claude fills its context window.

## Core Idea

Claude's output quality is proportional to context quality. Manage file size and structure to keep output stable.

## Managed Files

| File | Purpose | Always Loaded? | Size Limit |
|------|---------|:--------------:|------------|
| PROJECT.md | Project vision | ✅ | Strict |
| REQUIREMENTS.md | v1/v2 requirements | ✅ | Strict |
| ROADMAP.md | Phase roadmap | ✅ | Strict |
| STATE.md | Decisions, blockers, current state | ✅ | Strict |
| research/ | Domain knowledge | ✅ | Moderate |
| PLAN.md | Current atomic tasks | During execution | Relaxed |

## Size Limits

Set file size caps based on Claude's quality degradation threshold. Below threshold = sustained quality output.

## Context Monitor

Inject warnings when context is running low:
- **35% remaining** → Warning: wrap up current task
- **25% remaining** → Critical: stop immediately, save state

## Anti-Patterns

- Dumping everything into one huge file
- No size limits on context files
- Ignoring context warnings
- Keeping stale information in always-loaded files
