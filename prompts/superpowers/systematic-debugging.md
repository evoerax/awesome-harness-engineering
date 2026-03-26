# Systematic Debugging

Use when encountering any bug, test failure, or unexpected behavior, before proposing fixes.

## Iron Law

```
NO FIXES WITHOUT ROOT CAUSE INVESTIGATION FIRST
```

## Four Phases

### Phase 1: Root Cause Investigation
1. **Read error messages carefully** — stack traces, line numbers, error codes
2. **Reproduce consistently** — exact steps, every time
3. **Check recent changes** — git diff, recent commits, new deps
4. **Gather evidence** — add logging at component boundaries

### Phase 2: Pattern Analysis
1. **Find working examples** — similar code that works correctly
2. **Compare working vs broken** — what's different?
3. **Check dependencies** — version changes, API changes
4. **Verify assumptions** — is X actually what you think it is?

### Phase 3: Hypothesis and Testing
1. **Form one hypothesis** — "I think X causes Y because Z"
2. **Design minimal test** — smallest change to prove/disprove
3. **Test it** — does evidence support hypothesis?
4. **If wrong** — form new hypothesis, don't random-tweak

### Phase 4: Implementation
1. **Write failing test** — reproduces the bug
2. **Fix minimally** — one change, one fix
3. **Verify** — test passes, no regressions

## Stop Signs

- 3 failed fixes → question your understanding, not code
- Time pressure → systematic is faster than thrashing
- "Quick fix" → quick fixes create new bugs
