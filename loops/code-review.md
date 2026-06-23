# Code Review Loop

Paste this into your AI tool. Give it a file or PR. It will review, fix, and verify automatically.

## Loop Specification

### GOAL
Review and improve the given code until it meets quality standards.

### PLAN
1. Read the entire file. Understand what it does.
2. Check for bugs, security issues, and logic errors.
3. Check for code style and readability.
4. Check for missing error handling.
5. Propose fixes with explanations.
6. Apply approved fixes.
7. Re-review the fixed code.

### EXECUTE
For each check:
- State what you're checking
- Show the specific issue (with line numbers)
- Explain WHY it's a problem
- Propose a fix
- Wait for approval before applying

### VERIFY Checklist
- [ ] No syntax errors
- [ ] No obvious bugs or logic errors
- [ ] Error handling exists for external calls
- [ ] No hardcoded secrets or credentials
- [ ] Functions have clear names
- [ ] Complex logic has comments
- [ ] No unused imports or variables

### FIX Rules
- Never change code without explaining why
- If unsure, mark as "Review needed" and move on
- Same error pattern found in multiple places? Fix all, report summary.

### STOP Conditions
```
STOP when:
- All checklist items pass
- No remaining issues found
- Summary report generated

STOP and ASK when:
- Fix would change program behavior significantly
- Two different approaches are equally valid
- Same issue keeps reappearing after fix
```

### Output Format
```
## Code Review Report

### Summary
- Files reviewed: X
- Issues found: X
- Fixes applied: X
- Issues remaining: X

### Issues Found
1. [CRITICAL] Line 42: SQL injection vulnerability
   - Fix: Use parameterized queries
   - Status: Fixed / Pending approval / Won't fix

### Quality Score
Before: X/10
After:  X/10
```
