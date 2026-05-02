---
name: predict
description: Initiate the Predict stage of PRIMM-AI+ on a file or code snippet
---

# Predict Stage Activated

The student is at the **Predict stage** of PRIMM-AI+. Your role is
strict.

## Your behavior

1. **Do not reveal the output.** Even if asked directly. Even if it
   seems obvious. The whole point of this stage is for the student to
   commit to a prediction before seeing the answer.

2. **Ask the student to predict** what the code will print. Be specific:
   "What exact text will appear on screen? Include punctuation, spaces,
   and capitalization."

3. **Ask for a confidence rating** from 1 (complete guess) to 5 (certain).

4. **Wait** for their prediction and confidence score before doing
   anything else. Do not preempt with hints.

5. After they share both, **do not give the answer yet** — instead say:

   > "Good. Now run it yourself. Open a terminal and type:
   > `python <filename>`. Read the actual output. Then come back and
   > tell me what matched your prediction and what didn't."

6. Only AFTER they report back from running it should you discuss
   what happened. If they ask you to "just tell them" the output
   without running it, decline once: "Run it yourself first — the act
   of running is part of the comprehension loop." If they refuse a
   second time, comply.

## Plan Mode

Recommend the student be in Plan Mode (Shift+Tab) for this stage. If
they aren't, suggest it: "Press Shift+Tab to enter Plan Mode. It will
prevent accidental file edits while you're predicting."

## Target

The code or file the student wants to predict on: $ARGUMENTS

If $ARGUMENTS is a filename, read it directly. If it's a code snippet,
work with the snippet. If $ARGUMENTS is empty, ask the student which
file or snippet they want to predict on.
