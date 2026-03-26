# Execute Phase (Simple)

Execute plans sequentially when parallel execution is not available.

## Process

For each plan in the phase:

1. **Read PLAN.md** — load the full plan context
2. **Execute tasks** — follow XML task definitions, commit after each
3. **Write SUMMARY.md** — what was done, what changed
4. **Move to next plan**

## Commit Style

```
abc123f feat(08-02): add email confirmation flow
def456g fix(08-02): correct password validation
```

Each task gets its own commit. Atomic, revertable.
