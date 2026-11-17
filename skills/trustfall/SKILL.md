---
name: trustfall
description: Trustfall maximises trust between a human and an agent or a teammate by describing a project on five Levels — Concepts, User stories, Architecture, Module trees and Code — each derived only from the Levels above it. Use when starting a Trustfall project, when changing anything in a project that has a `trustfall/` folder, or when the user mentions Trustfall, Descent, Levels, Truths or Commandments.
---

# Trustfall

## Purpose

Code is the hardest thing to review. Trustfall builds trust by describing the
whole project on several Levels and validating that each Level matches what all
the Levels above it specify. A reviewer who trusts the upper Levels can then
trust everything below them.

Each Level is made of Items: single things that are digestible on their own.

Levels say **what** is built. Truths say what must hold true of the project:
how it is built or what it is. They only affect Code. Commandments are
Trustfall's own rules; they come from the `trustfall-validation` skill and can
never be changed or overridden.

## Level map

| #   | Level        | Skill                    | File in the Trustfall folder     |
| --- | ------------ | ------------------------ | -------------------------------- |
| 1   | Concepts     | `trustfall-concepts`     | `trustfall/1-concepts.md`        |
| 2   | User stories | `trustfall-user-stories` | `trustfall/2-stories.md`         |
| 3   | Architecture | `trustfall-architecture` | `trustfall/3-architecture.md`    |
| 4   | Module trees | `trustfall-module-trees` | `trustfall/4-module-trees.md`    |
| 5   | Code         | `trustfall-code`         | the project's source code folder |

Truths live in `trustfall/truths.md`.

## Descent from the topmost Level

Always start from Level 1 and work down one Level at a time. Load the skill of
the Level you are on, and only that one.

On every Level, make the Level perfect for what is known from the Levels above
it. Do not read or consider the Levels below; work already done there must not
bias the design.

A Level is finished when its Items pass validation. Only then descend.

## Reading the Levels above

Before designing a Level, read every Level file above it and nothing below it.
Use the exact names of Concepts from Level 1 on every Level.

## Writing Items

Write the Level to its file in the Trustfall folder, as Markdown, in the format
its Level skill gives.

## Validating the Items a change touched

After writing a Level, validate the Items the change touched with the
`trustfall-validation` skill: run the Level checks between this Level and the
Levels above. Fix every failing check before descending.

## Going back up

If something cannot be done with what the Levels above give, stop. Do not
change, reinterpret or extend an upper Level silently from below. Go back up to
the highest Level that needs to change, change it there, validate it, and
Descend again one Level at a time.

Going back up is a decision, not a failure; it is how the project ends up
modelled perfectly.

## Asking the initial Truths before Code

In the first Descent, after Module trees and right before Code, ask the user what
must hold true of the project: languages, tools, tests, formats, conventions,
licence. Write each answer as a Truth in `trustfall/truths.md`:

```markdown
- T1: Every User story is covered by a browser test.
  Verify: for each story ID there is a browser test that names it, and the tests pass.
```

Every Truth has a stable ID, a statement and a `Verify:` line that tells a
Validator subagent how to check it.

## Preferring simplicity

Keep every Level as simple as possible so there is nothing extra to review: no
Item, file, Block or Module that the Levels above do not need. When two designs
both satisfy the Levels above, choose the smaller one.
