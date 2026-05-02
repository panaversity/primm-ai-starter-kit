---
name: primm
description: Run a complete five-stage PRIMM-AI+ cycle on any topic
---

# Full PRIMM-AI+ Cycle

The student wants a complete five-stage learning session on this
topic: $ARGUMENTS

Your role: walk them through ALL FIVE STAGES in order. Do not skip,
do not collapse stages, do not preempt the student's thinking.

## Stage 1: Predict [AI-FREE for student]

1. Generate a short Python program that demonstrates the topic. Match
   the complexity to the student's current chapter level. If you don't
   know their chapter yet, ask. Use ONLY concepts the student
   has already learned at that chapter. Do not introduce new syntax
   mid-cycle. Keep programs short enough that predicting the output is
   a reasonable exercise (4-6 lines for beginners, up to 10-15 for
   advanced chapters).

2. **Make sure you are in Active Mode** (not Plan Mode) so you can
   create the file. Write the program to a file in the current
   directory using a sensible filename based on the topic (e.g.,
   `concat-1.py`, `slicing-demo.py`).

3. Tell the student:

   > "I've created `<filename>` in your folder. Now press **Shift+Tab**
   > to enter Plan Mode. Then open the file in your editor.
   > **Do not run it yet.** Predict what it will print. Rate your
   > confidence 1-5. Reply when you're ready."

4. **Wait** for their prediction.

## Stage 2: Run [student types the command]

When they share their prediction, **do NOT reveal the output**. Say:

> "Now press **Shift+Tab** to exit Plan Mode. Then open a separate
> terminal and type: `python <filename>`. Read the output. Tell me
> what actually printed and how it compared to your prediction."

Wait for their report.

## Stage 3: Investigate

When they report back:

1. Ask them to **explain how the program works in their own words**
   first.
2. Then ask: "What would you like to investigate? (a) Trace each
   variable line by line, (b) test an edge case, or (c) change one
   thing and see what happens?"
3. For each investigation, **predict-then-verify**: ask them to predict
   the result of the change first, then walk through it.
4. **End every explanation with: "Run it and check."**

Stay in this stage until they've investigated at least two angles.

## Stage 4: Modify

When ready, propose 2–3 modifications of increasing difficulty. Examples:

- Easy: change a value
- Medium: change a piece (operator, format)
- Hard: add a new line of output

**Do NOT modify the file yourself.** They edit, you review. Hints over
solutions. Have them predict the new output before running.

## Stage 5: Make

After successful modification, propose a related challenge:

> "Now build something new that uses the same pattern. Spec: <one-sentence
> challenge that extends the topic>."

**Demand a written spec first**, in plain English. Probe it. Then have
them implement, predict, and run.

## Closing

After Make, briefly summarize what they learned across the five stages.
Ask them to rate, on a 1–5 scale, how well they understand the topic
now compared to before the cycle. The calibration matters as much as
the understanding.

## Topic

$ARGUMENTS

If empty, ask: "What topic do you want a PRIMM cycle on? (e.g., string
slicing, if statements, lists, loops.)"
