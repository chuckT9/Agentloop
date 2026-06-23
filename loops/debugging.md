# Debugging Loop

Paste this into your AI tool. Give it an error or bug. It will diagnose, fix, and verify automatically.

## Loop Specification

### GOAL
Find the root cause of the bug and produce a verified fix.

### PLAN
1. Read the error message carefully. Identify the error type.
2. Read the relevant code. Understand what it's supposed to do.
3. Reproduce: trace the execution path that triggers the bug.
4. Hypothesize: what could cause this? List 2-3 possibilities.
5. Test hypotheses one by one (narrowest scope first).
6. Apply the fix.
7. Verify: run the code again, confirm the error is gone.

### EXECUTE
- For each hypothesis:
  - State the hypothesis clearly
  - Show the evidence for/against
  - If confirmed, apply fix. If rejected, move to next.
- After fixing, show the diff (before → after).

### VERIFY Checklist
- [ ] Original error no longer occurs
- [ ] Fix doesn't introduce new errors
- [ ] Fix addresses root cause, not symptom
- [ ] Code still passes existing tests (if any)
- [ ] Edge cases considered (null, empty, overflow)

### FIX Rules
- Smallest possible change first. Don't refactor while debugging.
- If the bug is in a dependency, check for version issues before modifying code.
- If you can't reproduce it, ask for more context (input, environment, steps).

### STOP Conditions
```
STOP when:
- Bug is fixed and verified
- No new errors introduced
- Root cause is documented

STOP and ASK when:
- Bug can't be reproduced
- Fix would require major refactoring
- Multiple valid fixes exist with different tradeoffs
- Bug is in third-party code (suggest workaround, don't modify library)
```

### Output Format
```
## Debug Report

### Error
[Error message and traceback]

### Root Cause
[What caused it and why]

### Fix Applied
[Code diff: before → after]

### Verification
- Original error: ✅ Gone
- New errors: ✅ None
- Edge cases: [tested / noted]
```
