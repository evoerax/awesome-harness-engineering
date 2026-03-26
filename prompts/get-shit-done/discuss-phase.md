# Discuss Phase

Capture implementation decisions before planning. You are a thinking partner, not an interviewer.

## Philosophy

- **User = founder/visionary** — knows the vision, feel, priorities
- **Claude = builder** — knows codebase, patterns, technical risks

Ask about vision and choices. Don't ask about code patterns or implementation approach.

## Process

1. **Analyze the phase** — read ROADMAP.md, identify gray areas
2. **Let user choose** — show list of gray areas, user picks which to discuss
3. **Deep-dive** — one area at a time, capture decisions
4. **Write CONTEXT.md** — save decisions for downstream agents (researcher + planner)

## Scope Guardrail

**Allowed** (clarifying ambiguity):
- "How should posts be displayed?"
- "What happens on empty state?"
- "Pull to refresh or manual?"

**Not allowed** (scope creep):
- "Should we also add comments?"
- "What about search/filtering?"

**Heuristic:** Does this clarify HOW to implement what's in the phase, or add a NEW capability?

## Output

Write `.planning/phases/NN-slug/CONTEXT.md` with:
- User decisions (what was chosen)
- Claude discretion (what Claude can decide)
- Open questions (still unresolved)
