# PRD to Issues

Break a PRD into independently-grabbable GitHub issues using vertical slices.

## Process

1. **Locate PRD** — GitHub issue number or URL
2. **Explore codebase** — optional
3. **Draft vertical slices** — thin end-to-end paths
4. **Quiz user** — present breakdown, iterate
5. **Create GitHub issues** — using `gh issue create`

## Slice Types

| Type | Meaning |
|------|---------|
| **HITL** | Human In The Loop — needs human interaction (arch decision, design review) |
| **AFK** | Away From Keyboard — can implement and merge without human |

Prefer AFK over HITL where possible.

## Issue Template

```markdown
## Parent PRD
#<prd-issue-number>

## What to build
End-to-end behavior description.

## Acceptance criteria
- [ ] Criterion 1
- [ ] Criterion 2

## Blocked by
- Blocked by #<issue-number> (if any)
Or "None - can start immediately"

## User stories addressed
- User story 3
- User story 7
```

## Rules

- Create in dependency order (blockers first)
- Do NOT close or modify the parent PRD issue
- Each issue independently grabbable
