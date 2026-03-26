# Improve Codebase Architecture

Explore codebase, find architectural friction, propose deepening refactors.

## What is a Deep Module?

Small interface hiding large implementation. More testable, more AI-navigable.

```
Good:  deep module  — simple API, complex internals
Bad:   shallow module — complex API, thin internals
```

## Process

### 1. Explore naturally
Note friction points:
- Understanding one concept requires bouncing between many files?
- Modules so shallow that interface ≈ implementation?
- Pure functions extracted just for testability, but bugs hide in calling?
- Tightly-coupled modules creating integration risk?
- Untested or hard-to-test code?

**The friction you encounter IS the signal.**

### 2. Present candidates
For each opportunity:
- **Cluster**: modules involved
- **Coupling reason**: shared types, call patterns
- **Test impact**: what boundary tests would replace

Ask user: "Which to explore?"

### 3. User picks

### 4. Frame the problem
Write user-facing explanation of constraints, dependencies, rough sketch.

### 5. Design multiple interfaces (parallel)
Spawn 3+ sub-agents, each with different constraint:
- Agent 1: "Minimize interface — 1-3 entry points max"
- Agent 2: "Maximize flexibility"
- Agent 3: "Optimize for most common caller"

### 6. Compare and recommend
Be opinionated — user wants a strong read, not a menu.

### 7. Create GitHub issue
RFC as `gh issue create`.
