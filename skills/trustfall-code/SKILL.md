---
name: trustfall-code
description: Trustfall Level 6 — write the Code that implements all the Levels above and the project's Truths, one planned Commit at a time. Use together with the trustfall skill when implementing or changing code in a Trustfall project.
---

# Code

## Code purpose

Code implements all the Levels above, one Commit at a time, so every part of it
can be traced back to what was agreed above.

## Reading the Truths

Read `trustfall/truths.md` before writing any Code. Truths say what must
hold true of the project: how it is built or what it is. They only affect
Commits and Code.

## One code unit per Module

Every Module of the Module trees becomes one code unit — a file, a component, a
section — named after the Module. Code may add details of its own, such as configuration
or ignore files, when they serve a Module or a Truth. Code that serves
neither means going back up.

## Writing Code one Commit at a time

Write the Code to the project's source code folder one planned Commit at a
time, in the planned order. Write only what the Commit's message says, then
make the Commit. Decisions inside a code unit — functions, types, wording,
libraries — belong to this Level and are yours to make.

When the Code shows that the plan was wrong, change the plan and rewrite the
Commits with the `trustfall-commits` skill. When the plan cannot be made with
what the Levels above give, go back up.

## Running the project's own checks on every Commit

Before making a Commit, run the project's own checks on exactly what the Commit
holds, for example with `git stash --keep-index --include-untracked`, the checks
and `git stash pop`. A Commit that fails them is not made.

## Validating the Commits and Code a change touched

Validate the Commits and Code the change touched with the
`trustfall-validation` skill once the change is done, not after every Commit.
The work is done only when every Level check, Commandment and Truth passes on
what the change touched.
