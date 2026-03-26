# TDD (Vertical Slices)

Test-driven development with integration-style tests and vertical slicing.

## Core Principle

Tests verify behavior through public interfaces, not implementation details. Code can change entirely; tests shouldn't.

## Good vs Bad Tests

| Good Tests | Bad Tests |
|-----------|----------|
| Integration-style | Coupled to implementation |
| Exercise public APIs | Mock internal collaborators |
| Describe WHAT system does | Verify HOW it does it |
| Survive refactors | Break when you refactor |

## Anti-Pattern: Horizontal Slices

```
WRONG (horizontal):
  RED:   test1, test2, test3, test4, test5
  GREEN: impl1, impl2, impl3, impl4, impl5

RIGHT (vertical):
  RED→GREEN: test1→impl1
  RED→GREEN: test2→impl2
  RED→GREEN: test3→impl3
```

## Workflow

### 1. Planning
- Confirm interface changes needed
- Confirm which behaviors to test (prioritize)
- Identify deep module opportunities
- Get user approval

### 2. Tracer Bullet
Write ONE test → fails → minimal code → passes

### 3. Incremental Loop
For each remaining behavior: RED → GREEN

### 4. Refactor
After all tests pass:
- Extract duplication
- Deepen modules
- Apply SOLID where natural
- Run tests after each step

## Checklist Per Cycle

```
[ ] Test describes behavior, not implementation
[ ] Test uses public interface only
[ ] Test would survive internal refactor
[ ] Code is minimal for this test
[ ] No speculative features added
```
