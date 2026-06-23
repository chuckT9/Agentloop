# AgentLoop — Core Specification

> Paste this file into your AI tool's system prompt, project instructions, or AGENTS.md.
> Your AI will automatically follow the loop pattern defined here.

## What is a Loop?

A loop is NOT a single prompt. A loop is a **repeating cycle** your AI follows:

```
Goal → Plan → Execute → Verify → Fix → Repeat (or Stop)
```

Your AI doesn't just answer once. It **works until the job is done**.

## How to Use

1. Pick a loop template from `loops/` (or design your own)
2. Copy the template into your AI tool's instructions
3. Give your AI a task
4. It runs the loop automatically. You review at checkpoints.

That's it. No code. No setup. Just paste.

## Loop Structure (6 Elements)

Every loop has 6 parts. You MUST define all 6:

### 1. GOAL — What are we building?

Define the end state. Be specific.

```
Good:  "Generate a Python script that reads CSV, cleans data, outputs summary stats"
Bad:   "Help me with data analysis"
```

### 2. PLAN — How do we get there?

Break the goal into numbered steps. Your AI will follow these in order.

```
1. Read and understand the input file
2. Identify missing values and outliers
3. Apply cleaning transformations
4. Generate summary statistics
5. Output results to file
```

### 3. EXECUTE — Do the work

Your AI runs each step. After each step, it MUST:
- Report what it did
- Show the output
- Check for errors before moving on

### 4. VERIFY — Did it work?

After execution, your AI checks its own work:
- Does the output match the goal?
- Are there errors or warnings?
- Does the result make sense?

```
Verification checklist:
- [ ] Output file exists and is readable
- [ ] No NaN values remain
- [ ] Column count matches input
- [ ] Summary stats are within expected ranges
```

### 5. FIX — Repair what's broken

If verification fails, your AI:
- Identifies the specific failure
- Proposes a fix
- Applies the fix
- Re-runs verification

**Critical rule:** If the same fix fails 2 times, STOP and ask the human.

### 6. STOP — When to exit the loop

Define clear exit conditions:

```
STOP when ALL of these are true:
- All verification checks pass
- No errors or warnings remain
- Output matches the goal

STOP and ASK HUMAN when:
- The same error occurs 3 times
- A decision requires domain expertise
- The task scope has changed
```

## The Golden Rules

1. **One step at a time.** Never skip ahead. Complete → Verify → Next.
2. **Show your work.** Every iteration, report what changed.
3. **Fail loud.** If something breaks, say so immediately. Don't hide errors.
4. **Two-strike rule.** Same error twice = stop and ask.
5. **Track state.** Keep a running log of what's been done, what's left, what failed.
6. **Human checkpoints.** After major milestones, pause and ask for review.

## State Tracking

Your AI maintains a state file throughout the loop:

```markdown
## Loop State
- Current step: 3/5
- Completed: Read input ✓, Clean data ✓
- In progress: Generate summary
- Failed: (none)
- Next: Output results
- Iterations: 1
```

This prevents the AI from losing track in long loops.

## Writing Your Own Loop

See `docs/LOOP-DESIGN.md` for the full guide. Quick version:

1. Pick a real task you do repeatedly
2. Break it into the 6 elements above
3. Write the verification checklist
4. Set stop conditions
5. Test it. Refine. Ship it.
