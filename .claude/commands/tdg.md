---
name: tdg
description: Run a complete Test-Driven Generation cycle on a function specification
---

# TDG Cycle

The student wants to run a Test-Driven Generation cycle. Your role:
guide them through the five TDG steps in order. Do not skip steps,
do not write the implementation before the student has written the
specification.

## Step 1: Specify

Ask the student to write:

1. A function stub with type annotations and `...` body
2. At least two test assertions that define correct behavior

If $ARGUMENTS describes what the function should do, help the student
translate that into a stub and tests. Do NOT write the stub for them.
Ask guiding questions:

- "What should the function be called?"
- "What types go in? What type comes out?"
- "What are two input-output pairs you know are correct?"

Wait for the student to write the stub and tests.

## Step 2: Check types

Ask the student to run `uv run pyright`. The stub should pass (types
are correct, body is `...`). If pyright reports errors, help the
student fix the type annotations before proceeding.

## Step 3: Generate

Only after the stub and tests exist and pyright passes, say:

> "Your specification is ready. Now ask me to implement the function.
> Say: 'Implement the function that passes these tests. Do not modify
> the tests.'"

Wait for the student to ask. Then generate the implementation.

## Step 4: Verify

Ask the student to run `uv run pytest -v`. If tests pass (GREEN),
proceed to Step 5. If tests fail (RED):

- Ask the student to read the failure output
- Ask them to classify the error using `/bug` (type, logic,
  specification, data, or orchestration error)
- Help them write a specific re-prompt that names the failing test,
  states the wrong value, and identifies the cause
- Re-generate and verify again

## Step 5: Read

After GREEN, ask the student to read the generated code. Use the
PRIMM method from Chapter 45:

- "Predict what the function returns for an input NOT in your tests"
- "Does the implementation use a real formula or hardcoded values?"
- "Would this function work for edge cases like zero, negative
  numbers, or empty strings?"

The cycle is complete when the student can explain what the generated
code does and why it works.

## Target

$ARGUMENTS

If $ARGUMENTS describes a function (e.g., "convert kg to pounds"),
guide the student through specifying it. If empty, ask: "What
function do you want to build? Describe it in one sentence."
