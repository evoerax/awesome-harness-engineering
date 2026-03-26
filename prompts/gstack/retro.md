# Weekly Retro

Engineering retrospective — what did we ship, what can we improve.

## Process

1. **Analyze commit history** — what was done this week
2. **Count per-person** — who did what
3. **Identify patterns** — shipping streak, blockage, quality
4. **Generate report** — with praise and growth areas

## Output Format

```markdown
## Week of [date]

### Shipped
- Feature A (PR #42)
- Bug fix B (PR #43)

### Per-Person
| Person | Commits | PRs | Streak |
|--------|---------|-----|--------|
| Alice  | 12      | 3   | 🔥 5 days |
| Bob    | 8       | 2   | 3 days |

### Growth Areas
- Test coverage dropped to 72%
- 3 PRs without review

### Praise
- Alice: shipped auth refactor in 1 day
- Bob: caught critical race condition
```

## Anti-Patterns

- Not doing retros ("too busy")
- Retros without action items
- Only focusing on negatives
