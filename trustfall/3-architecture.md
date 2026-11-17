# Architecture

## Loading the Levels

```mermaid
flowchart TD
  trustfall[Trustfall skill]
  load@{ shape: f-circ }
  concepts[1 Concepts skill]
  stories[2 User stories skill]
  architecture[3 Architecture skill]
  modules[4 Module trees skill]
  commits[5 Commits skill]
  code[6 Code skill]
  levels[(Trustfall folder in the file system)]
  trustfall -- loads one Level at a time, from the topmost, with the Levels above it --- load
  load --> concepts & stories & architecture & modules & commits & code
  trustfall -- reads the Levels above --> levels
  trustfall -- before Commits, writes the initial Truths asked from the user --> levels
```

## Writing Items and Code

```mermaid
flowchart TD
  trustfall[Trustfall skill]
  code[6 Code skill]
  levels[(Trustfall folder in the file system)]
  source[(Source code folder in the file system)]
  trustfall -- writes the current Level's Items --> levels
  code -- reads the Truths --> levels
  code -- writes --> source
```

## Making Commits

```mermaid
flowchart TD
  commits[5 Commits skill]
  code[6 Code skill]
  levels[(Trustfall folder in the file system)]
  git[(Git repository)]
  checks[Project's own checks]
  commits -- reads the Truths --> levels
  code -- runs on every Commit before making it --> checks
  code -- makes the planned Commits, one at a time --> git
  commits -- rewrites the Commits not yet shared --> git
```

## Validating

```mermaid
flowchart TD
  trustfall[Trustfall skill]
  code[6 Code skill]
  validation[Validation skill holding the Commandments]
  subagent[Validator subagent with no history]
  levels[(Trustfall folder in the file system)]
  source[(Source code folder in the file system)]
  git[(Git repository)]
  trustfall -- validates the Items a change touched against the Levels above with --> validation
  code -- validates the Commits and Code a change touched against the Levels above with --> validation
  validation -- validates the Commandments and the Truths on what a change touched, and a new or changed Truth on the whole project, with --> subagent
  subagent -- reads Levels and Truths --> levels
  subagent -- reads --> source
  subagent -- reads the Commits of a change --> git
  subagent -- returns Pass, or Fail with its reasons --> validation
```
