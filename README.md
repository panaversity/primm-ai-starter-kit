# PRIMM-AI+ Starter Kit

A workbench configuration for learning Python with **Claude Code** using the **PRIMM-AI+** framework (Predict, Run, Investigate, Modify, Make + AI).

Part of [The AI Agent Factory](https://github.com/panaversity/agentfactory) book, Part 4: Programming in the AI Era.

---

## What This Is

PRIMM-AI+ is a research-validated method for learning to program. You read code before you write it. You predict what a program does before you run it. You investigate how it works before you modify it. AI assists at every stage but never does your thinking for you.

This starter kit configures Claude Code to enforce that discipline automatically through three layers:

| Layer | File | What it does |
|---|---|---|
| **House rules** | `CLAUDE.md` | Tells Claude Code to ask for your prediction before revealing answers, give hints instead of solutions, and demand a spec before writing code |
| **Stage guides** | `.claude/commands/*.md` | Seven slash commands that walk you through each PRIMM stage step by step |
| **Mode awareness** | Built into Claude Code | Plan Mode (Shift+Tab) blocks file edits during thinking stages |

## Quick Start

### 1. Install Claude Code

Follow the instructions at [claude.ai/download](https://claude.ai/download). Requires Node.js 18+.

### 2. Create your project folder

```bash
mkdir primm-practice
cd primm-practice
```

### 3. Clone this starter kit into your project

```bash
git clone https://github.com/panaversity/primm-ai-starter-kit.git .
```

Or download and unzip from the [latest release](https://github.com/panaversity/primm-ai-starter-kit/releases).

### 4. Start Claude Code

```bash
claude
```

### 5. Verify the setup

Check that Claude Code loaded the house rules:

```
What rules are you following for this session?
```

It should describe PRIMM-AI+ and the three rules. Then type `/` to confirm the seven slash commands appear.

---

## Slash Commands

| Command | Stage | What it does |
|---|---|---|
| `/predict <file>` | Predict | Refuses to reveal output until you commit to a prediction and confidence rating |
| `/investigate <file>` | Investigate | Asks you to explain in your own words first, then probes with Socratic questions |
| `/modify <file>` | Modify | You edit the file; Claude Code reviews and gives hints, never solutions |
| `/make <description>` | Make | Demands a written spec in plain English before any code |
| `/primm <topic>` | All five | Runs a complete Predict-Run-Investigate-Modify-Make cycle on any topic |
| `/bug <error>` | Debug | Asks you to classify the bug type before showing the fix |
| `/parsons <file or topic>` | Practice | Generates a scrambled-line puzzle to test structural understanding |

There is no `/run` command. Running code is your job. Type `python file.py` yourself. The act of running is part of the comprehension loop.

---

## The Three Rules

These are encoded in `CLAUDE.md` so Claude Code enforces them automatically:

1. **Try first, then ask AI.** Make your own attempt before asking for help. During Predict, Claude Code will ask for your prediction before answering.
2. **Do not skip stages.** Each stage builds on the previous one. Claude Code will flag if you try to Modify before Predicting and Running.
3. **Write things down.** Predictions, trace tables, explanations. Claude Code will prompt you to record your thinking.

If you say "skip the scaffolding," Claude Code complies immediately. The rules build habits, not cages.

---

## How It Adapts to Your Level

At the start of each session, Claude Code asks which chapter you are working on. It uses a concept map to match complexity to your level:

| Chapter | Phase | Concepts you know |
|---|---|---|
| 42 | 1 | PRIMM-AI+ method, variables, print(), strings, + for joining, str() |
| 43 | 1 | Ten Axioms, Error Taxonomy (5 bug types), conceptual reasoning |
| 44 | 1 | uv, pyproject.toml, pyright, ruff, pytest, git |
| 45 | 1 | Type annotations, int/float/str/bool, arithmetic, f-strings, assert, trace tables |
| 46 | 1 | TDG cycle, first test, first AI-generated implementation |

The concept map grows as new chapters are written. If your chapter is not in the table, Claude Code will ask what concepts you have covered.

---

## File Structure

```
primm-ai-starter-kit/
├── CLAUDE.md                    # House rules Claude Code reads every session
├── README.md                    # This file
└── .claude/
    └── commands/
        ├── predict.md           # Predict stage scaffold
        ├── investigate.md       # Socratic investigation
        ├── modify.md            # Review and hint, never solve
        ├── make.md              # Spec-first, then implement
        ├── primm.md             # Full five-stage cycle
        ├── bug.md               # Classify-before-fix
        └── parsons.md           # Scrambled-line puzzles
```

---

## Design Decisions

**Why no `/run` command?** Running code is the one stage where AI delegation damages learning. You type `python file.py` yourself because comparing your prediction to the actual output is where understanding happens.

**Why a session-start question instead of a config file?** Asking "which chapter are you working on?" is simpler than expecting students to edit a configuration file every chapter. Claude Code adapts automatically.

**Why an override clause?** Learning frameworks should build habits, not become obstacles. When you know a concept and want to move fast, saying "skip the scaffolding" is enough.

---

## Part of The AI Agent Factory

This starter kit is used in [The AI Agent Factory](https://github.com/panaversity/agentfactory) book, starting at Chapter 42 (The PRIMM-AI+ Framework) and continuing through all chapters in Part 4: Programming in the AI Era.

The kit evolves as new chapters are written. Each phase may add new slash commands or update the concept map. The version you install in Chapter 42 works for all subsequent chapters.

## Research Basis

PRIMM was created by Sue Sentance and Jane Waite (2017) and tested with 493 students across 13 schools in England. Students who learned with PRIMM outperformed those who did not.

- Sentance, S., Waite, J., and Kallia, M. (2019). "Teaching computer programming with PRIMM: a sociocultural perspective." *Computer Science Education*, 29(2-3), 136-176.
- [PRIMM Portal](https://primmportal.com)
- [Computing Education Research](https://computingeducationresearch.org/projects/primm/)

---

## License

MIT
