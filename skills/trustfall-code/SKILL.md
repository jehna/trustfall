---
name: trustfall-code
description: Trustfall Level 5 — write the Code that implements all the Levels above and the project's Truths. Use together with the trustfall skill when implementing or changing code in a Trustfall project.
---

# Code

## Code purpose

Code implements all the Levels above, so every part of it can be traced back to
what was agreed above.

## Reading the Truths

Read `trustfall/truths.md` before writing any Code. Truths say what must
hold true of the project: how it is built or what it is. They only affect Code.

## One code unit per Module

Every Module of the Module trees becomes one code unit — a file, a component, a
section — named after the Module. Code may add details of its own, such as configuration
or ignore files, when they serve a Module or a Truth. Code that serves
neither means going back up.

## Writing Code

Write the Code to the project's source code folder. Decisions inside a code
unit — functions, types, wording, libraries — belong to this Level and are
yours to make.

## Validating the Code a change touched

Validate the Code the change touched with the `trustfall-validation` skill. The
work is done only when every Level check, Commandment and Truth passes on
what the change touched.
