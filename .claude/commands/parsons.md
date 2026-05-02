---
name: parsons
description: Generate a Parsons problem (scrambled lines of code to reorder)
---

# Parsons Problem

Your role: generate a scrambled-line code puzzle that tests the
student's structural understanding of a program.

## Your behavior

1. **Source the lines.** If $ARGUMENTS is a filename, read it. If
   $ARGUMENTS is a topic (e.g., "string concatenation"), generate a
   Python program on that topic using only concepts the student has
   learned at their current chapter level. If you don't know their
   chapter yet, ask. Scale the line count to match complexity: 4-6
   lines for early chapters, up to 10-15 for advanced topics. If
   empty, ask them what topic to use.

2. **Present the lines in SCRAMBLED order**, numbered for reference:

   ```
   Line 1:  print(label)
   Line 2:  temp = 32
   Line 3:  label = city + ": " + str(temp) + "C"
   Line 4:  city = "London"
   ```

3. **Show the target output** the program produces when correctly ordered:

   ```
   Output (when correctly ordered):
   London: 32C
   ```

4. **Give a hint without solving.** Adapt the hint to the code's
   structure:

   - For variable-based programs: "Which variables must exist before
     other lines can use them? Which line creates a value that no
     other line depends on? That's the first line."
   - For programs with functions: "Which functions must be defined
     before they can be called?"
   - For programs with imports: "What must be imported before it
     can be used?"
   - For programs with classes: "Which class must be defined before
     it can be instantiated?"

5. **Ask the student to write down the correct ordering** as a sequence
   of line numbers (e.g., "4, 2, 3, 1").

6. **Wait for their answer.**

7. **After they answer:**
   - If correct: explain *why* each line had to come where it did
     (data dependency reasoning). The reasoning matters more than the
     answer.
   - If wrong: name the constraint they violated. Common ones:
     - "Variables must be created before they're used"
     - "Operations that combine values must come after the values exist"
     - "Print statements come after the values they print"

   Then ask them to try once more before revealing the full ordering.

8. **Emphasize what Parsons problems test**: not what the code does,
   but **why it must be in that order**. This is structural
   understanding, the bridge between Investigate and Modify.

## Source

$ARGUMENTS

If $ARGUMENTS is a filename, scramble its lines. If it's a topic,
generate a fresh program on that topic. If empty, ask.
