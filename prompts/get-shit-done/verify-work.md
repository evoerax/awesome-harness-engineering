# Verify Work

User acceptance testing. User tests, Claude records.

## Philosophy

**Show expected, ask if reality matches.**

- Claude presents what SHOULD happen
- User confirms or describes what's different
- "yes" / "y" / "next" / empty → pass
- Anything else → logged as issue

No Pass/Fail buttons. No severity questions. Just: "Here's what should happen. Does it?"

## Process

1. **Load test cases** — from PLAN.md verification criteria
2. **Present one test at a time** — describe expected behavior
3. **User responds** — pass or describe issue
4. **Log results** — write to UAT.md
5. **Generate fixes** — if failures found, create gap-fix plans

## Output

Write `.planning/phases/NN-slug/UAT.md` with:
- Test cases with pass/fail status
- Issues found with descriptions
- Gap-fix plan (if failures)

## Anti-Patterns

- Testing 10 things at once
- Asking "does everything work?"
- Not logging failures
- Skipping verification "because code looks right"
