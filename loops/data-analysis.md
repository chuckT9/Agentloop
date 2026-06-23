# Data Analysis Loop

Paste this into your AI tool. Give it a dataset. It will explore, clean, analyze, and report automatically.

## Loop Specification

### GOAL
Analyze the given dataset and produce actionable insights with visualizations.

### PLAN
1. Load the data. Report shape, columns, dtypes.
2. Profile the data: missing values, duplicates, outliers.
3. Clean: handle missing values, fix types, remove duplicates.
4. Explore: distributions, correlations, patterns.
5. Analyze: answer the specific question asked.
6. Visualize: create charts that tell the story.
7. Summarize: write the findings in plain language.

### EXECUTE
After each step, output:
- What you did
- Key numbers (rows before/after, correlations, etc.)
- Any warnings or anomalies
- Preview of the data (first 5 rows)

### VERIFY Checklist
- [ ] Data loaded correctly (row count matches source)
- [ ] No unexpected NaN values in key columns
- [ ] Data types are correct (numbers are numeric, dates are datetime)
- [ ] Outliers identified and handled (not silently dropped)
- [ ] Visualizations are readable and labeled
- [ ] Statistical claims have supporting evidence
- [ ] Conclusions follow from the data (no overclaiming)

### FIX Rules
- Lost rows during cleaning? Report exactly how many and why.
- Correlation != causation. Always note this.
- If a column has >50% missing values, flag it — don't silently fill.
- If a visualization is unclear, try a different chart type.

### STOP Conditions
```
STOP when:
- All analysis steps complete
- Visualizations are generated
- Summary report is written
- All checklist items pass

STOP and ASK when:
- Data is ambiguous (multiple valid interpretations)
- Analysis direction unclear after profiling
- Statistical test choice requires domain knowledge
- Results contradict expectations significantly
```

### Output Format
```
## Data Analysis Report

### Dataset Overview
- Rows: X, Columns: X
- Time range: X to X (if applicable)
- Missing data: X% overall

### Key Findings
1. [Finding with supporting numbers]
2. [Finding with supporting numbers]

### Visualizations
[Charts with titles and labels]

### Recommendations
1. [Actionable recommendation]
2. [Actionable recommendation]

### Data Quality Notes
- [Any issues found in the data]
```
