---
name: trustfall-validation
description: Trustfall validation — holds the immutable Commandments and validates Levels, Code and Truths with Validator subagents that have no history of the work. Use after writing any Trustfall Level, while writing Code, and always before calling Trustfall work done.
---

# Validation

## Commandments

Commandments are Trustfall's own rules. They hold in every project, are kept
apart from the project's Truths, and can never be changed or overridden.

1. **Descent.** Each Level is designed only from the Levels above it.
2. **Fidelity.** Every Item derives from the Levels above, and each Level
   matches what all the Levels above specify.
3. **Going back up.** Nothing agreed on a Level is changed silently from a
   Level below it.
4. **Bite-sized Items.** Every Item is digestible on its own.
5. **Simplicity.** Nothing exists that the Levels above do not need.
6. **Truths affect only Code.** Levels 1–4 never depend on a Truth.
7. **Validated before done.** Nothing is done until every Level check,
   Truth and Commandment passes.

Every Commandment is its own check.

## Level checks

Run the checks for the Level that was written, each as its own check:

| Level        | Checks                                                                                                                                                                                                                |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Concepts     | Every Concept has one name and one meaning. Concepts contain no behaviour or technology.                                                                                                                              |
| User stories | Every capitalised term in a story is a Concept. Every Concept is used by a story.                                                                                                                                     |
| Architecture | Every story is possible with the drawn Blocks and edges. Every Block and edge has a source above. Only Mermaid diagrams of Blocks, nothing inside them.                                                               |
| Module trees | Every Block has one tree and every tree a Block. Every edge is implemented by a Module. Every Module has a source above. Names are obvious, no duplicates; Modules that implement different edges are not duplicates. |
| Code         | Every Module has a code unit. Every code unit and every detail Code adds serves a Module or a Truth. No behaviour beyond the User stories.                                                                            |

A capitalised term in the middle of a sentence on any Level must be a Concept,
in any word form, such as Descend for Descent.
A word that starts with a lowercase letter is plain language and needs no
Concept. Block names, Module names and Code may use plain language.

## Truth checks

Every Truth in `trustfall/truths.md` is its own check, using its
`Verify:` line.

## Checking only what a change touched

After a change, validate only what it touched: the Items and Code in its diff,
and every Item and code unit that refers to, or is referred to by, something
the diff changed or removed. Run the Level checks of every Level the change
touched, every Commandment and every Truth on those parts only; the Levels
above them are read as they are, not judged. A check that matches two lists,
such as every Concept is used by a story, compares the whole lists. A new or
changed Truth is checked on the whole project.

The first validation of a project, and any validation after a failed or skipped
one, checks the whole project.

Before work is called done, every Level check, Commandment and Truth must
pass on what the change touched. Everything else passed when it last changed,
so the whole project then passes every Level check, Truth and Commandment.

## One Validator subagent per check

Give every check to its own subagent that has no history of the work: a fresh
subagent, never a fork of the current conversation. Launch all checks at once
so they run in parallel, and brief each one with
[validator-subagent.md](validator-subagent.md). Tell it only the check and the
parts the change touched, never what you built or what you expect.

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
