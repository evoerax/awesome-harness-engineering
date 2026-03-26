# Test-Driven Development (TDD)

Use when implementing any feature or bugfix, before writing implementation code.

## Iron Law

```
NO PRODUCTION CODE WITHOUT A FAILING TEST FIRST
```

Wrote code before the test? Delete it. Start over. No exceptions.

## RED → GREEN → REFACTOR

### RED — Write Failing Test
- Write ONE minimal test showing what should happen
- Run it. Verify it FAILS for the RIGHT reason
- If it passes: test is wrong, fix the test

### GREEN — Minimal Code to Pass
- Write the LEAST code to make the test pass
- Run all tests. Verify ALL green
- Don't over-engineer. Don't add features the test doesn't require

### REFACTOR — Clean Up
- Improve code structure
- Run tests after EACH change — must stay green
- Extract functions, remove duplication, improve names

## Anti-Patterns

- Writing code first, tests later → delete, start over
- "I'll keep this as reference" → no, delete
- Tests pass immediately → test is wrong
- Skipping TDD "just this once" → that's rationalization
