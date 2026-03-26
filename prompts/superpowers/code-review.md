# Code Review

Use when completing tasks, implementing features, or before merging.

## When to Review

**Mandatory:**
- After each task in development
- After completing major feature
- Before merge to main

**Optional but valuable:**
- When stuck (fresh perspective)
- Before refactoring (baseline check)
- After fixing complex bug

## What to Check

1. **Plan alignment** — does code do what was specified?
2. **Test coverage** — are edge cases tested? Are tests meaningful?
3. **Code quality** — clear names, small functions, no duplication
4. **Security** — no hardcoded secrets, input validation, error handling
5. **Performance** — no obvious N+1, unnecessary allocations
6. **Integration** — does it break existing functionality?

## How to Review

```
1. Read the plan/requirements first
2. Read the diff (git diff BASE..HEAD)
3. Check tests pass
4. Check for issues:
   - Critical: must fix before proceeding
   - Important: fix before proceeding
   - Minor: note for later
5. Report findings with reasoning
```

## Anti-Patterns

- Reviewing without understanding the plan
- Nitpicking style instead of catching logic errors
- Approving without actually reading the code
- Skipping review "because it's small"
