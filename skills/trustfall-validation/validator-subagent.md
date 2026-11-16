# Validator subagent

Fill in the angle brackets and give the whole text to the Validator subagent.

## Brief

```text
You are validating one rule of a project. You have no history of the work;
rely only on the files.

Project: <one sentence on what the project in this repository is>
Project root: <path>

Rule: <the check, Commandment or Constraint, quoted verbatim>
```

## What the change touched

For a Level check or a Commandment:

```text
Judge only these parts; read everything else only as context:
<the files and lines the change touched, or its diff>
```

For a Constraint, leave this part out: a Constraint is checked on the whole
project.

## Reading the Levels, Constraints and Code

```text
The Levels are in <path>/trustfall/: 1-concepts.md, 2-stories.md,
3-architecture.md, 4-module-trees.md, and the Constraints in constraints.md.
The Code is in <source code folder>.
Read what you need. You may run read-only commands and the project's own
checks. Do not change any file.
```

## Verdict

```text
Answer in this format:
VERDICT: PASS | FAIL
REASONS: one bullet per finding, each citing file:line
```
