---
name: trustfall-code
description: Trustfall Level 5 — write the Code that implements all the Levels above and the project's Constraints. Use together with the trustfall skill when implementing or changing code in a Trustfall project.
---

# Code

## Code purpose

Code implements all the Levels above, so every part of it can be traced back to
what was agreed above.

## Reading the Constraints

Read `trustfall/constraints.md` before writing any Code. Constraints say how the
project is built, and they only affect Code.

## One code unit per Module

Every Module of the Module trees becomes one code unit — a file, a component, a
section — named after the Module. Code may add details of its own, such as configuration
or ignore files, when they serve a Module or a Constraint. Code that serves
neither means going back up.

## Writing Code

Write the Code to the project's source code folder. Decisions inside a code
unit — functions, types, wording, libraries — belong to this Level and are
yours to make.

## Validating Code against the Levels above

Validate with the `trustfall-validation` skill. The work is done only when a full run of
the `trustfall-validation` skill passes every Level check, Constraint check and
Commandment.
