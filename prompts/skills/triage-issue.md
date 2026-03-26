# Triage Issue

Investigate a bug, find root cause, create GitHub issue with TDD fix plan.

## Process

### 1. Capture the problem
Ask ONE question: "What's the problem you're seeing?"
Then start investigating immediately. No follow-up questions.

### 2. Explore and diagnose
Find:
- **Where** bug manifests (entry points, UI, API)
- **What** code path is involved
- **Why** it fails (root cause, not symptom)
- **What** related code exists

Look at:
- Related source files and dependencies
- Existing tests
- Recent changes (`git log`)
- Error handling in code path
- Similar patterns that work correctly

### 3. Identify fix approach
- Minimal change to fix root cause
- Affected modules/interfaces
- Behaviors to verify via tests
- Is it regression, missing feature, or design flaw?

### 4. Design TDD fix plan
Ordered list of RED-GREEN cycles:

```markdown
1. **RED**: Write a test that [expected behavior]
   **GREEN**: [Minimal change to make it pass]

2. **RED**: Write a test that [next behavior]
   **GREEN**: [Minimal change to make it pass]

**REFACTOR**: [Any cleanup after all tests pass]
```

### 5. Create GitHub issue
Use `gh issue create`. Share URL.

## Rules

- Tests through public interfaces, not implementation
- One test at a time, vertical slices
- Describe behaviors and contracts, not file paths
- Issue should survive major refactors
