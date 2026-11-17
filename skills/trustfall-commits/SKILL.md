---
name: trustfall-commits
description: Trustfall Level 5 — plan the Commits of a change as the perfect story of how it would be built in a perfect world, before any Code is written. Use together with the trustfall skill when planning, making or rewriting Commits in a Trustfall project.
---

# Commits

## Commit purpose

Commits tell the perfect story of how a change is built, as it would be built
in a perfect world. They are planned before any Code is written, so the change
is reviewed one small step at a time and never as one huge diff.

## Reading the Truths

Read `trustfall/truths.md` before planning. A Truth may need a Commit of its
own, such as setting up a tool the project must use, or say how Commits are
written.

## Planning the perfect story

Plan every Commit of the change before writing any Code. Keep the plan in your
context and write it to no file; each Commit becomes real only when the Code
Level makes it.

- Every Commit is one atomic step: it does one thing, and every line it
  changes serves that thing.
- Every Commit passes the project's own checks on its own, so each Commit
  builds only on the Commits before it.
- Every Commit derives from the Levels above.
- Together the Commits make the whole change and nothing more.

When the whole change is one atomic step, its one Commit carries both the Items
it changed on the Levels above and its Code. A larger change may first make one
Commit of the Items it changed on the Levels above, followed by the Commits of
its Code.

## Commit format

```text
Add Task list with a form for new Tasks

Users need to see what is left and to add what they intend to get done.
```

- The title says what the Commit does.
- The body says why.

## Rewriting the Commits not yet shared

Whenever the plan changes, rewrite the Commits not yet shared so the history
still reads as the perfect story: fold a change into the Commit it belongs to,
reorder, split or drop Commits. Never rewrite Commits already shared with
others.

To fold a change into an earlier Commit without an interactive editor:

```shell
git commit --fixup=<commit>
GIT_SEQUENCE_EDITOR=: git rebase -i --autosquash <commit>~1
```
