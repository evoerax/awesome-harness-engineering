# PRD to Plan

Break a PRD into phased implementation plan using vertical slices (tracer bullets).

## Process

1. **Confirm PRD** — should already be in conversation
2. **Explore codebase** — understand architecture, patterns, integration layers
3. **Identify durable decisions** — routes, schema, models, auth approach (won't change across phases)
4. **Draft vertical slices** — thin end-to-end paths, NOT horizontal layers
5. **Quiz user** — present breakdown, iterate until approved
6. **Write plan file** — save to `./plans/`

## Vertical Slice Rules

- Each slice: complete path through ALL layers (schema → API → UI → tests)
- Completed slice is demoable on its own
- Many thin slices > few thick slices
- NO specific file names (will change)
- YES durable decisions (routes, schema shapes)

## Plan Template

```markdown
# Plan: <Feature Name>

## Architectural decisions
- Routes: ...
- Schema: ...
- Key models: ...

---

## Phase 1: <Title>
**User stories**: <list from PRD>
### What to build
End-to-end behavior description.
### Acceptance criteria
- [ ] Criterion 1
- [ ] Criterion 2
```

## Anti-Patterns

- Horizontal slices (all API first, then all UI)
- Too thick phases (not demoable)
- Including implementation details that will change
