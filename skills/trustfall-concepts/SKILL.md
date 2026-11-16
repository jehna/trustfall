---
name: trustfall-concepts
description: Trustfall Level 1 — design the Concepts of a project, its shared vocabulary, in trustfall/1-concepts.md. Use together with the trustfall skill when creating or changing Concepts.
---

# Concepts

## Concept purpose

Concepts give everyone working on the project a shared vocabulary, so we can
communicate efficiently. Every later Level speaks in these words.

Concepts are the topmost Level: there are no Levels above to read.

## Concept format

`trustfall/1-concepts.md` holds one or more ASCII trees in `text` code blocks:

````markdown
# Concepts

```text
Task — a single thing the user intends to get done
├── Description — free text saying what the Task is about
└── Status — where the Task is in its life
    ├── Todo — not yet done
    └── Done — completed
```
````

- Every Item is one line: `Name — definition`.
- Names are capitalised; later Levels use them with exactly this spelling.
- A child is a part of its parent, or a kind of it. When a parent has both
  parts and kinds, group the kinds under their own node so the two do not mix.
- A Concept is a thing in the project's domain. Behaviour belongs to User
  stories; technology belongs to Architecture.
- One meaning has one name, and one name has one meaning.
