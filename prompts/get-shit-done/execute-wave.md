# Execute Phase

Wave-based parallel execution. Each plan runs in fresh 200k context.

## Core Principle

Orchestrator coordinates, not executes. Each subagent loads full plan context. Orchestrator: discover plans → analyze deps → group waves → spawn agents → collect results.

## Wave Execution

```
WAVE 1 (parallel)          WAVE 2 (parallel)          WAVE 3
┌─────────┐ ┌─────────┐    ┌─────────┐ ┌─────────┐    ┌─────────┐
│ Plan 01 │ │ Plan 02 │ →  │ Plan 03 │ │ Plan 04 │ →  │ Plan 05 │
│ User    │ │ Product │    │ Orders  │ │ Cart    │    │ Checkout│
│ Model   │ │ Model   │    │ API     │ │ API     │    │ UI      │
└─────────┘ └─────────┘    └─────────┘ └─────────┘    └─────────┘
     ↑           ↑              ↑           ↑              ↑
     └───────────┴──────────────┴───────────┘
       Dependencies: Plan 03 needs Plan 01 + 02
```

## Process

1. **Discover plans** — find all PLAN.md files in the phase
2. **Analyze dependencies** — which plans depend on which
3. **Group into waves** — independent plans = same wave
4. **Spawn agents** — one subagent per plan (or sequential if no Task tool)
5. **Handle checkpoints** — verify between waves
6. **Collect results** — gather SUMMARY.md from each plan

## Fallback

If subagent spawning doesn't work, use sequential inline execution. Never block indefinitely — verify via filesystem and git state.

## Agent

- `gsd-executor` — executes plan tasks, commits, creates SUMMARY.md
