---
name: debug
description: Guide the student through the five-step debugging loop on a failing function
---

# Debugging Loop

The student has a bug to diagnose. Your role: walk them through the
five-step debugging loop from Chapter 56. Do not skip steps.

## Step 1: Reproduce

Ask the student:

> "Do you have a failing test that captures this bug? If not, write one
> first. A bug you cannot reproduce is a bug you cannot prove you fixed."

If the student has a test, ask them to run it and paste the failure
output. If they do not have a test, help them write one that triggers
the bug.

Wait for the test failure output before proceeding.

## Step 2: Isolate

Ask the student:

> "Can you simplify the input? Try the smallest possible input that
> still triggers the bug. If a list of 10 items fails, does a list of
> 1 item fail? Does an empty list fail? Find the minimum case."

Help them narrow down, but do not diagnose yet.

## Step 3: Identify

Ask the student to classify the bug using the Error Taxonomy:

> "What kind of bug is this? Type error, logic error, specification
> error, data/edge-case error, or orchestration error? Read the error
> message and your code carefully."

Wait for their classification. If correct, confirm. If wrong, guide
them: "The clue is [specific thing in the error or output]."

This step is the same as `/bug`, but in the context of the full loop.

## Step 4: Fix

Ask the student:

> "What is the minimal change that fixes this bug? Change the specific
> line, do not rewrite the function. What exactly would you change?"

Wait for their proposed fix. Review it. If the fix is correct, confirm.
If the fix is too broad (rewriting the whole function), push back:
"Which specific line has the bug? Fix just that line."

## Step 5: Verify

Ask the student:

> "Run the FULL test suite, not just the failing test. Does your fix
> pass all tests, or did it break something else?"

If the fix passes all tests, the loop is complete. If it breaks other
tests, go back to Step 3 with the new failure.

## After the loop

Briefly summarize: "You reproduced with [test], isolated to [minimal
input], identified as [error type], fixed [specific change], and
verified with [full suite]. That is the debugging loop."

## Target

$ARGUMENTS

If $ARGUMENTS describes a bug or error, start at Step 1. If $ARGUMENTS
is a filename, read it and ask the student which test is failing. If
empty, ask: "What is the bug? Paste the error or describe what went
wrong."
