# AgentLoop

> **Stop prompting. Start looping.** Design autonomous AI workflows that run, verify, and self-correct — no code required.

You type a prompt. AI gives an answer. You check it. It's wrong. You rephrase. It's still wrong. You give up.

**AgentLoop fixes this.** Instead of one-shot prompts, you give your AI a **loop** — a structured cycle of Plan → Execute → Verify → Fix that runs until the job is actually done.

**[中文版](README_CN.md)**

| Version | Last Verified | Disclaimer |
|---------|---------------|------------|
| v0.1.0 | 2026-06-23 | Community project, not affiliated with any AI vendor |

---

## ⭐ If this project helps you, please give it a Star!

- ⭐ **1 click, 0 cost** — just hit the Star button at the top right
- 🧑‍🎓 **Made for students & beginners** — no coding, no setup, just paste
- 🤖 **Works with ANY AI agent** — Claude, ChatGPT, Cursor, Copilot, Hermes, Codex
- 📋 **Copy-paste ready** — pick a loop, paste it, done

> *Your star = more people discover that AI can work in loops, not just prompts.*

---

## How it works in 30 seconds

```
You give your AI a task
        ↓
Instead of a single prompt, you paste a Loop template
        ↓
AI follows the loop: Plan → Execute → Verify → Fix
        ↓
If verification fails, AI fixes it automatically
        ↓
AI stops only when ALL checks pass
```

**No API. No code. No server.** Just a markdown file you paste into your AI tool.

## What's inside?

| File | What it does |
|------|-------------|
| `AGENTS.md` | The core specification — paste this into any AI tool |
| `loops/code-review.md` | Loop for reviewing and fixing code |
| `loops/debugging.md` | Loop for finding and fixing bugs |
| `loops/data-analysis.md` | Loop for analyzing datasets |
| `loops/writing.md` | Loop for writing and editing |
| `loops/research.md` | Loop for research and fact-finding |
| `loops/email.md` | Loop for drafting and polishing messages |
| `docs/LOOP-DESIGN.md` | How to design your own loops |
| `examples/` | Real-world loop examples |

## Quick Start (2 steps)

### Step 1: Pick a Loop

Browse `loops/` and pick one that matches your task:
- `code-review.md` — reviewing code
- `debugging.md` — finding and fixing bugs
- `data-analysis.md` — analyzing data
- `writing.md` — writing and editing
- `research.md` — research questions
- `email.md` — drafting messages

### Step 2: Paste It

**ChatGPT:** Paste the loop content at the start of your conversation.

**Claude:** Paste it in the project instructions or at the start of the chat.

**Cursor / Copilot:** Add it to your project's `.cursorrules` or system instructions.

**Hermes Agent:** Drop it in your skills folder or paste in AGENTS.md.

Then give your AI a task. It will follow the loop automatically.

## Design Your Own Loop

Every loop has 6 elements:

1. **Goal** — What's the end state?
2. **Plan** — What are the steps?
3. **Execute** — Do each step, show work
4. **Verify** — Checklist of observable conditions
5. **Fix** — If verification fails, repair and re-verify
6. **Stop** — When to declare done (or ask for help)

See `docs/LOOP-DESIGN.md` for the full guide.

## The Golden Rules

1. **One step at a time.** Complete → Verify → Next.
2. **Show your work.** Report what changed each iteration.
3. **Fail loud.** Don't hide errors.
4. **Two-strike rule.** Same error twice = stop and ask human.
5. **Track state.** Know where you are in the loop.
6. **Human checkpoints.** Pause at major milestones.

## Real-world Cases

### Case 1: Student writes a thesis chapter
A graduate student needs to write the methodology chapter. Instead of asking AI to "write it", she pastes the **writing loop**. The AI writes section by section, self-reviews academic tone, checks figure references, and stops only when all checks pass. Result: polished draft in 2 iterations instead of 5 re-prompts.

### Case 2: Developer debugs a production error
A developer gets a traceback. He pastes the **debugging loop**. The AI reads the error, traces the execution path, lists 3 hypotheses, tests each one, applies the fix, and verifies the error is gone. Root cause identified in 1 loop cycle.

### Case 3: Researcher analyzes experimental data
A researcher has a dataset from her experiments. She pastes the **data-analysis loop**. The AI profiles the data, cleans it, runs exploratory analysis, generates visualizations, and produces a summary report with actionable findings. All in one loop, no re-prompting needed.

### Case 4: Anyone writes a professional email
You need to email your professor about a collaboration idea. You paste the **email loop**. The AI drafts the message, checks tone (formal enough?), removes filler, and produces a concise, clear email. No more staring at a blank compose window.

See `examples/` for full loop templates used in these cases.

## Who is this for?

- **Students** using AI for homework, research, writing
- **Developers** using AI for code review, debugging, refactoring
- **Researchers** using AI for literature review, data analysis
- **Anyone** who's tired of re-prompting the same AI 5 times

## How is this different from ResearchOS?

| | AgentLoop | ResearchOS |
|---|---|---|
| Focus | How AI **works** (process) | What AI **knows** (memory) |
| Format | Loop templates | Knowledge base |
| Usage | Paste a loop, AI runs it | Paste a KB, AI reads it |
| Together | AgentLoop + ResearchOS = AI that knows AND does |

## License

MIT — use it, modify it, share it.
