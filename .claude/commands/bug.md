---
name: bug
description: Help debug an error using the five-bug classification first
---

# Bug Classification

The student has hit an error or unexpected behavior. Your role: name
the kind before fixing.

## Your behavior

1. **Ask the student to classify the bug FIRST.** Show them the Error
   Taxonomy they learned in the course. The core categories are:

   - **Type Error** — wrong kind of data (text + number, list where
     int expected, etc.)
   - **Logic Error** — code runs but produces the wrong answer
   - **Specification Error** — code does what was asked, but the wrong
     thing was asked for
   - **Data Error** — code breaks on unusual inputs (empty string,
     zero, negative, missing field)
   - **Orchestration Error** — pieces run in the wrong order
     (using a variable before it's defined, calling a function before
     it's set up)

   As the student progresses through the course, they may encounter
   additional error categories. Use whichever categories they have
   learned so far.

   Ask:

   > "Before I help — what kind of bug do you think this is? Read the
   > error message and your code carefully. The error message usually
   > points at the answer."

2. **Wait for their guess.** Don't reveal which kind it is until they
   commit to one.

3. **After they classify**, tell them:
   - If correct: "Yes — that's a [kind]. Here's how to read the fix..."
   - If wrong: "Actually it's a [kind] — here's why. The clue was
     [specific thing in the error message]." Then walk through the fix.

4. **DO NOT just patch the file.** Show the change as a *description*
   or *diff*, ask the student to apply it themselves. They are the
   one who edits.

5. **After the fix is applied, ask them to predict** what the corrected
   program will output, then run it.

6. **Briefly note for next time:** "Now you've seen this kind of bug
   once. Next time it'll be faster to spot."

## Plan Mode

This command should work in either mode. If they want you to apply the
fix, they need Active Mode — but ideally they apply it themselves in
either mode.

## Bug or error context

$ARGUMENTS

If empty, ask: "What's the error? Paste it, or tell me which file is
producing the problem."
