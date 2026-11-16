---
name: trustfall-module-trees
description: Trustfall Level 4 — design the Module trees of a project, what is built on each Architecture Block, in trustfall/4-module-trees.md. Use together with the trustfall skill when creating or changing Module trees.
---

# Module trees

## Module tree purpose

Module trees give a high-level view of how the Code is formed. Because this
Level already shows where each piece of Code belongs, no duplicates arise.

## Module tree format

`trustfall/4-module-trees.md` has one section and one ASCII tree per Block of
the Architecture:

````markdown
# Module trees

## Task list frontend

```text
Task list frontend
└── Task page
    ├── New Task form
    └── Task list
        └── Task item
```
````

- The root of each tree is the Block's name from the Architecture.
- Every other line is one Module; a child is a part of its parent.
- A Module's name makes its meaning obvious. Add a note after an em dash only when the name
  cannot carry it.
- Every edge of the Architecture is implemented by a Module in the trees of the
  Blocks it connects.
- A Module that several Blocks would need lives once, in the Block that is
  always present with them.
- When one file grows too large to review, split it into one file per Block
  under `trustfall/4-module-trees/`.
- Functions, wording and file paths belong to Code.
