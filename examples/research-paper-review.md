# Example: Research Paper Review Loop

A real-world example of a custom loop designed for academic paper review.

## Context

You're a researcher. You need to review papers for:
- Experimental methodology validity
- Statistical analysis correctness
- Literature coverage
- Writing quality

## The Loop (paste this into your AI tool)

### GOAL
Review the given research paper and produce a structured review report with specific, actionable feedback.

### PLAN
1. Read the abstract and conclusion first. Understand the paper's claim.
2. Read the full paper. Note the methodology and key results.
3. Check: Are the experiments well-designed?
4. Check: Is the statistical analysis correct?
5. Check: Is the literature review comprehensive?
6. Check: Is the writing clear and logical?
7. Write the review report.

### EXECUTE
For each check:
- State what you're evaluating
- Quote specific sections (with page/line numbers)
- Give your assessment with reasoning
- Suggest specific improvements

### VERIFY Checklist
- [ ] Every major claim in the paper has been evaluated
- [ ] Statistical methods are checked against standard practices
- [ ] At least 3 related papers are referenced to assess literature coverage
- [ ] All feedback is specific (quotes page numbers, suggests alternatives)
- [ ] Tone is constructive, not dismissive
- [ ] No personal opinions stated as facts

### FIX Rules
- If you can't evaluate a technical claim (outside your knowledge), say so.
- If the paper is outside your domain, flag it and stop.
- Don't rewrite the paper. Suggest improvements with examples.

### STOP Conditions
```
STOP when:
- All 4 checks are complete
- Review report is written
- All checklist items pass

STOP and ASK when:
- Paper topic is outside your expertise
- Statistical method is unfamiliar
- You're unsure if a criticism is fair
```

## Output

```
## Paper Review Report

### Paper: [Title]
### Recommendation: Accept / Minor Revision / Major Revision / Reject

### 1. Methodology Assessment
[Evaluation with specific quotes]

### 2. Statistical Analysis
[Evaluation with specific quotes]

### 3. Literature Coverage
[Assessment with related papers mentioned]

### 4. Writing Quality
[Assessment with specific examples]

### Summary of Required Changes
1. [Most critical change]
2. [Second most critical]
3. [Third]

### Minor Issues
- [Page X, Line Y: typo/grammar]
- [Page X, Line Y: unclear sentence]
```
