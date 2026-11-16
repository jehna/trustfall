---
name: trustfall-user-stories
description: Trustfall Level 2 — design the User stories of a project, what it must let its users do, in trustfall/2-stories.md. Use together with the trustfall skill when creating or changing User stories.
---

# User stories

## User story purpose

User stories write down what the project must let its users do, so its
behaviour can be validated without knowing how it is built.

## User story format

`trustfall/2-stories.md` is one Markdown list:

```markdown
# User stories

- S1: I want to add a new Task so that I remember to do it.
- S2: I want to mark a Task Done so that I see what is left.
```

- Every Item is one line: `S<n>: I want <capability> so that <reason>.`
- IDs are stable. Once a story has been validated, its ID is never renumbered
  or reused.
- Domain words are the capitalised Concepts from Level 1, spelled exactly the
  same. A missing Concept means going back up to Level 1.
- Every Concept is used by at least one story.
- A story describes behaviour a user can observe; screens, storage and
  technology belong to lower Levels.
