# Design an Interface

Generate multiple radically different interface designs, then compare.

## Process

### 1. Gather Requirements
- What problem does this module solve?
- Who are the callers?
- Key operations?
- Constraints?
- What to hide inside vs expose?

### 2. Generate Designs (Parallel Sub-Agents)

Spawn 3+ sub-agents simultaneously. Each produces a **radically different** approach.

```
Agent 1: "Minimize method count — 1-3 methods max"
Agent 2: "Maximize flexibility — support many use cases"
Agent 3: "Optimize for the most common case"
Agent 4: "Take inspiration from [specific paradigm]"
```

Each outputs:
1. Interface signature (types/methods)
2. Usage example
3. What it hides internally
4. Trade-offs

### 3. Compare

- **Interface simplicity**: fewer methods, simpler params
- **General-purpose vs specialized**: flexibility vs focus
- **Implementation efficiency**: does shape allow efficient internals?
- **Depth**: small interface hiding complexity (good) vs large interface thin impl (bad)

### 4. Synthesize

Ask user: "Which fits your primary use case? Any elements from other designs?"

## Key Insight (from "A Philosophy of Software Design")

Your first idea is unlikely to be the best. Multiple designs reveal trade-offs you'd miss with one approach.
