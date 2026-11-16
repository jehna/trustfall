---
name: trustfall-validation
description: Trustfall validation — holds the immutable Commandments and validates Levels, Code and Constraints with Validator subagents that have no history of the work. Use after writing any Trustfall Level, while writing Code, and always before calling Trustfall work done.
---

# Validation

## Commandments

Commandments are Trustfall's own rules. They hold in every project, are kept
apart from the project's Constraints, and can never be changed or overridden.

1. **Descent.** Each Level is designed only from the Levels above it.
2. **Fidelity.** Every Item derives from the Levels above, and each Level
   matches what all the Levels above specify.
3. **Going back up.** Nothing agreed on a Level is changed silently from a
   Level below it.
4. **Bite-sized Items.** Every Item is digestible on its own.
5. **Simplicity.** Nothing exists that the Levels above do not need.
6. **Constraints affect only Code.** Levels 1–4 never depend on a Constraint.
7. **Validated before done.** Nothing is done until every Level check,
   Constraint and Commandment passes.

Every Commandment is its own check.

## Level checks

Run the checks for the Level that was written, each as its own check:

| Level        | Checks                                                                                                                                                     |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Concepts     | Every Concept has one name and one meaning. Concepts contain no behaviour or technology.                                                                   |
| User stories | Every story uses only Concepts. Every Concept is used by a story.                                                                                          |
| Architecture | Every story is possible with the drawn Blocks and edges. Every Block and edge has a source above. Only Mermaid diagrams of Blocks, nothing inside them.    |
| Module trees | Every Block has one tree and every tree a Block. Every edge is implemented by a Module. Every Module has a source above. Names are obvious, no duplicates. |
| Code         | Every Module has a code unit. Every code unit belongs to a Module or a Constraint. No behaviour beyond the User stories.                                   |

Capitalised terms on any Level must be Concepts; Module names and Code may use
plain language.

A full run, before work is called done, must pass every Level check, every
Commandment and every Constraint.

## Constraint checks

Every Constraint in `trustfall/constraints.md` is its own check, using its
`Verify:` line.

## One Validator subagent per check

Give every check to its own subagent that has no history of the work: a fresh
subagent, never a fork of the current conversation. Launch all checks at once
so they run in parallel, and brief each one with
[validator-subagent.md](validator-subagent.md). Tell it only the check, never
what you built or what you expect.

If the agent cannot start subagents, ask the user to open a fresh session for
each check and paste the brief there.

## Light model for mechanical checks

Run mechanical checks, where lists must match, on a light model. Run checks
that need interpretation, such as definitions or level of detail, on a
stronger model.

## Reporting Verdicts

Show the user every Verdict with its reasons. A Fail
is never explained away. Fix it on the Level where it belongs, going back up if
needed, and run that check again with a new Validator subagent.
