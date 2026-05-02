# PRIMM-AI+ Starter Kit

This folder contains the workbench setup for learning Python with
**PRIMM-AI+** (Predict, Run, Investigate, Modify, Make + AI) inside
**Claude Code**.

## What's in here

- **`CLAUDE.md`** — the rules Claude Code follows when you work in this
  folder. Read it once. It tells Claude Code to be your learning
  partner, not your ghostwriter.

- **`.claude/commands/`** — seven slash commands that scaffold the five
  PRIMM stages plus two utilities:

  | Command | Purpose |
  |---|---|
  | `/predict <file>` | Predict stage — Claude Code refuses to reveal output until you commit to a prediction |
  | `/investigate <file>` | Investigate stage — Socratic questions about mechanics |
  | `/modify <file>` | Modify stage — you edit, Claude Code reviews and hints |
  | `/make <description>` | Make stage — spec first, then implement, then review |
  | `/primm <topic>` | Full five-stage cycle on any topic |
  | `/bug <error>` | Debug helper — classify the bug type before fixing |
  | `/parsons <file or topic>` | Scrambled-line puzzle for structural understanding |

## How to use

1. Copy this entire folder structure into the root of your chapter or
   project workspace.
2. Open a terminal in that folder.
3. Start Claude Code: `claude`
4. Verify CLAUDE.md is loaded by asking Claude Code: *"What rules am I
   working under?"* It should describe PRIMM-AI+ and the three rules.
5. Try a slash command: `/primm string concatenation`

That's it. Now go through Chapter 42.
