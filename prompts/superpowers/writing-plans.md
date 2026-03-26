# Writing Plans

Use when you have a spec for a multi-step task, before touching code.

## Core Idea

Break work into bite-sized tasks (2-5 minutes each). Each task has: exact files, code, verification steps. A fresh engineer with zero context should be able to follow your plan.

## Plan Structure

```markdown
# [Feature] Implementation Plan

**Goal:** One sentence what this builds
**Architecture:** 2-3 sentences approach
**Tech Stack:** Key technologies

---

### Task 1: [Component Name]

**Files:**
- Create: `exact/path/to/file.py`
- Modify: `exact/path/to/existing.py:123-145`
- Test: `tests/exact/path/to/test.py`

- [ ] Step 1: Write failing test
  ```python
  def test_specific():
      assert function(input) == expected
  ```

- [ ] Step 2: Implement minimal code
  ```python
  def function(input):
      return expected
  ```

- [ ] Step 3: Run tests, verify all green
- [ ] Step 4: Commit
```

## Rules

- **2-5 minutes per step** — if longer, split into sub-steps
- **Exact file paths** — no guessing
- **Complete code in plan** — not pseudocode
- **One commit per task** — atomic, revertable
- **Tests first** — every task starts with a test

## Anti-Patterns

- Vague steps like "implement the feature"
- Missing file paths
- Skipping tests
- Tasks longer than 15 minutes
