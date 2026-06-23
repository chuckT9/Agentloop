# Research Loop

Paste this into your AI tool. Give it a research question. It will search, synthesize, and report automatically.

## Loop Specification

### GOAL
Answer a research question with evidence from multiple sources, cited properly.

### PLAN
1. Understand the question. Clarify scope and depth needed.
2. Identify key search terms and sub-questions.
3. Search for sources. Evaluate each for credibility.
4. Extract relevant information from top sources.
5. Synthesize findings into a coherent answer.
6. Identify gaps, contradictions, and uncertainties.
7. Write the final report with citations.

### EXECUTE
- For each source, note: title, author, date, URL, key claims.
- Distinguish between facts, opinions, and speculation.
- Track which sources agree and which contradict.
- Quote directly when precision matters.

### VERIFY Checklist
- [ ] At least 3 independent sources consulted
- [ ] Sources are recent (or age is noted)
- [ ] No single source dominates the answer
- [ ] Contradictions are acknowledged, not hidden
- [ ] Claims are attributed to sources
- [ ] Uncertainty is expressed where appropriate
- [ ] The original question is actually answered

### FIX Rules
- If all sources agree, note the consensus strength.
- If sources disagree, present both sides with evidence.
- If no credible sources found, say so — don't speculate.
- If the question is too broad, narrow it and explain why.

### STOP Conditions
```
STOP when:
- Question is answered with supporting evidence
- Sources are cited properly
- Limitations are acknowledged

STOP and ASK when:
- Question is ambiguous after initial research
- Sources are contradictory and resolution requires judgment
- Topic requires specialized domain knowledge
- Research reveals the question needs reformulation
```

### Output Format
```
## Research Report

### Question
[The original question]

### Executive Summary
[2-3 sentence answer]

### Findings
1. [Finding with citation]
2. [Finding with citation]

### Contradictions / Debates
[Points where sources disagree]

### Limitations
[What this research couldn't answer]

### Sources
1. [Title — Author — Date — URL]
2. [Title — Author — Date — URL]
```
