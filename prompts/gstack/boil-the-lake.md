# Boil the Lake

A principle: when AI makes the marginal cost near-zero, always choose the complete option.

## The Principle

Human effort has cost. AI effort has near-zero marginal cost.

| Task | Human Team | CC+gstack | Compression |
|------|-----------|-----------|-------------|
| Scaffolding | 2 days | 15 min | ~100x |
| Test writing | 1 day | 15 min | ~50x |
| Feature impl | 1 week | 30 min | ~30x |
| Bug fix | 4 hours | 15 min | ~20x |

**Implication:** Don't cut corners. Don't choose "good enough." Choose complete.

## Anti-Patterns (STOP)

- "Choose B, 90% value, less code" (A is only 70 more lines)
- "Skip edge cases to save time" (edge cases take minutes)
- "Put test coverage in follow-up PR" (tests are cheapest)
- "MVP is fine for now" (when you can ship complete in same time)

## Apply To

- **Features** — ship complete, not partial
- **Tests** — full coverage, not "enough"
- **Error handling** — all cases, not happy path only
- **Documentation** — full docs, not TODOs
