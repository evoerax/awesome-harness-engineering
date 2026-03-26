# Code Review

Pre-landing PR review — find bugs that pass CI but break in production.

## What Makes This Different

Normal review: "is the code clean?"
This review: "will this break in prod?"

## Check List

1. **SQL Safety** — injection risks, N+1 queries, missing indexes
2. **LLM Trust Boundary** — are you trusting AI output without validation?
3. **Conditional Side Effects** — code that works in test but fails in prod
4. **Error Handling** — what happens when external service is down?
5. **Race Conditions** — concurrent access patterns
6. **Data Migration** — will this break existing data?
7. **Rollback Plan** — can you undo this deploy?

## Process

1. Read the diff against base branch
2. Check each item above
3. Categorize issues:
   - **Critical**: must fix before merge
   - **Important**: fix before merge
   - **Minor**: note for later
4. Report with reasoning

## Anti-Patterns

- Reviewing only style, missing logic errors
- Not checking if tests actually test the right thing
- Approving "because CI passed"
