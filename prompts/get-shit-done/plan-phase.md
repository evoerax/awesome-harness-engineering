# Plan Phase

Create executable atomic tasks with integrated research and verification.

## Process

```
Research → Plan → Verify → Done
(max 3 revision loops)
```

## XML Task Structure

```xml
<task type="auto">
  <name>Create login endpoint</name>
  <files>src/api/auth/login.ts</files>
  <action>
    Use jose for JWT (not jsonwebtoken - CommonJS issues).
    Validate credentials against users table.
    Return httpOnly cookie on success.
  </action>
  <verify>curl -X POST localhost:3000/api/auth/login returns 200 + Set-Cookie</verify>
  <done>Valid credentials return cookie, invalid return 401</done>
</task>
```

## Rules

- **2-5 minutes per task** — if longer, split
- **Exact file paths** — no guessing
- **Built-in verification** — each task has verify + done criteria
- **Fresh context** — each plan is self-contained
- **Vertical slices** — end-to-end, not horizontal layers

## Vertical vs Horizontal Slicing

```
✅ GOOD: Plan 01 — User feature end-to-end (model + API + UI)
❌ BAD:  Plan 01 — All models, Plan 02 — All APIs, Plan 03 — All UI
```

## Agents

- `gsd-phase-researcher` — researches technical approaches
- `gsd-planner` — creates detailed plans from scope
- `gsd-plan-checker` — reviews plan quality (max 3 loops)
