# QA Browser

Real browser testing — agent can "see" web pages, find visual bugs.

## Why Real Browser

Claude is "blind" — it can write code but can't see web pages. Real browser gives it eyes.

## Key Difference

| Approach | Speed | State | Auth |
|----------|-------|-------|------|
| New browser each time | 3-5s per command | ❌ Lost | ❌ Re-login |
| Persistent daemon | ~100ms per command | ✅ Kept | ✅ Kept |

## Commands

```bash
$B goto https://staging.app.com
$B screenshot /tmp/check.png
$B fill @e3 "test@example.com"
$B click @e5
$B text                    # read page content
$B console                 # check JS errors
$B network                 # check failed requests
$B responsive /tmp/layout  # 3 screenshots (mobile/tablet/desktop)
$B diff https://staging.app.com https://prod.app.com
```

## Process

1. Open the app in browser
2. Click through user flows
3. Screenshot each state
4. Check console for errors
5. Check network for failures
6. Fix issues found
7. Re-verify after fix

## Anti-Patterns

- Testing without screenshots (no evidence)
- Not checking console/network (missing errors)
- Skipping "re-verify" step after fix
