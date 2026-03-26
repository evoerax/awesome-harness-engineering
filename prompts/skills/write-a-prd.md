# Write a PRD

Create a Product Requirements Document through user interview and codebase exploration.

## Process

1. **Ask the user** — long, detailed description of the problem and potential solutions
2. **Explore codebase** — verify assertions, understand current state
3. **Interview relentlessly** — every aspect, every branch of the design tree
4. **Sketch modules** — major modules to build/modify, look for deep modules
5. **Write PRD** — submit as GitHub issue

## PRD Template

```markdown
## Problem Statement
The problem from the user's perspective.

## Solution
The solution from the user's perspective.

## User Stories
1. As an <actor>, I want a <feature>, so that <benefit>
2. As a mobile user, I want to see balance, so that I can make better decisions.

## Implementation Decisions
- Modules to build/modify
- Interfaces changes
- Architectural decisions
- Schema changes
- API contracts

## Testing Decisions
- What makes a good test
- Which modules to test
- Prior art in codebase

## Out of Scope
What's NOT included.

## Further Notes
Any additional context.
```

## Key Principle

Deep modules — small interface, large implementation. Look for opportunities to extract them.
