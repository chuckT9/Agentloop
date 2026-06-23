# How to Design Your Own Loop

A step-by-step guide to creating loop templates for any task.

## Step 1: Pick a Real Task

Don't design a loop in the abstract. Start with a task you actually do repeatedly.

Good candidates:
- Tasks where you correct the AI multiple times
- Tasks where you have a mental checklist
- Tasks where the AI forgets steps
- Tasks where quality varies wildly between attempts

Bad candidates:
- One-off questions ("What is X?")
- Creative exploration with no clear endpoint
- Tasks requiring real-time data you can't provide

## Step 2: Write the Goal

The goal is a single sentence that describes the **end state**. Not the process — the result.

Template:
```
[Action] a [deliverable] that [quality criteria] for [audience/purpose].
```

Examples:
```
"Generate a Python script that processes sales data and outputs a summary report."
"Write a blog post about machine learning for beginners, under 1000 words."
"Review this code for security vulnerabilities and suggest fixes."
```

## Step 3: Break Into Steps (Plan)

List the numbered steps. Each step should be:
- **Atomic**: one action per step
- **Verifiable**: you can check if it was done
- **Ordered**: dependencies flow downward

Rule of thumb: 3-8 steps. Fewer than 3 = too simple for a loop. More than 8 = too complex, break into sub-loops.

## Step 4: Define the Verification Checklist

This is the most important part. A loop without verification is just a prompt with extra words.

For each step, ask: "How do I know this was done correctly?"

Checklist format:
```
- [ ] [Observable condition]
- [ ] [Observable condition]
```

Good checklist items:
```
- [ ] Script runs without errors on test data
- [ ] Output file contains expected columns
- [ ] No hardcoded values in the code
```

Bad checklist items:
```
- [ ] Code is good (not measurable)
- [ ] Analysis is thorough (subjective)
- [ ] Writing is clear (who decides?)
```

## Step 5: Set Stop Conditions

Two types:

**Success conditions** — when to stop and declare done:
```
STOP when:
- All checklist items pass
- Output meets the goal
```

**Escalation conditions** — when to stop and ask the human:
```
STOP and ASK when:
- Same error occurs 3 times
- Decision requires domain expertise
- Scope has expanded beyond original goal
```

## Step 6: Add the Golden Rules

Include these in every loop:

1. One step at a time. Complete → Verify → Next.
2. Show your work. Report what changed each iteration.
3. Fail loud. Don't hide errors.
4. Two-strike rule. Same error twice = stop and ask.
5. Track state. Know where you are in the loop.
6. Human checkpoints. Pause at major milestones.

## Step 7: Test and Refine

Run your loop 3 times with real tasks. Each time, note:
- Where did the AI get stuck?
- What did it skip?
- Where did you have to intervene?
- What verification did it miss?

Update the loop based on these findings. A good loop improves with use.

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Too vague ("improve the code") | Specific ("fix all type errors and add error handling") |
| No verification | Add a checklist with observable conditions |
| No stop condition | Define when to stop AND when to ask |
| Too many steps | Break into sub-loops or simplify |
| No state tracking | Add a "Loop State" section |
| AI skips steps | Add "Complete each step before moving to the next" |
