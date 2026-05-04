# PRIMM-AI+ Starter Kit v2.0 (Phase 2)

This folder contains the workbench setup for learning Python with
**PRIMM-AI+** (Predict, Run, Investigate, Modify, Make + AI) inside
**Claude Code**.

**Version 2.0** adds the `/tdg` command for Test-Driven Generation
cycles and extends the concept map to cover Chapters 47-49
(Primitive Types, Strings and Collections, Functions as Contracts).

## What's in here

- **`CLAUDE.md`** — the rules Claude Code follows when you work in this
  folder. Includes the concept map for Chapters 42-49 so Claude Code
  adapts to your current level.

- **`.claude/commands/`** — eight slash commands that scaffold the five
  PRIMM stages, TDG cycles, and two utilities:

  | Command | Purpose |
  |---|---|
  | `/predict <file>` | Predict stage — Claude Code refuses to reveal output until you commit to a prediction |
  | `/investigate <file>` | Investigate stage — Socratic questions about mechanics |
  | `/modify <file>` | Modify stage — you edit, Claude Code reviews and hints |
  | `/make <description>` | Make stage — spec first, then implement, then review |
  | `/primm <topic>` | Full five-stage PRIMM cycle on any topic |
  | `/tdg <description>` | Full TDG cycle: Specify (stub + tests) → Check types → Generate → Verify → Read |
  | `/bug <error>` | Debug helper — classify the bug type before fixing |
  | `/parsons <file or topic>` | Scrambled-line puzzle for structural understanding |

## What changed from v1.0

| Change | Details |
|---|---|
| New command: `/tdg` | Guides student through full Test-Driven Generation cycle |
| Concept map extended | Added Ch 47 (types + expressions), Ch 48 (strings + collections), Ch 49 (function contracts) |
| Command count | 7 → 8 |

## How to use

1. Copy this entire folder structure into the root of your chapter or
   project workspace.
2. Open a terminal in that folder.
3. Start Claude Code: `claude`
4. Verify CLAUDE.md is loaded by asking Claude Code: *"What rules am I
   working under?"* It should describe PRIMM-AI+ and the eight commands.
5. Try a slash command: `/tdg convert celsius to fahrenheit`
