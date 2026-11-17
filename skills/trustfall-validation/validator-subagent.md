# Validator subagent

Fill in the angle brackets and give the whole text to the Validator subagent.

## Brief

```text
You are validating one rule of a project. You have no history of the work;
rely only on the files.

Project: <one sentence on what the project in this repository is>
Project root: <path>

Rule: <the check, Commandment or Truth, quoted verbatim>
```

## What the change touched

```text
Judge only these parts; read everything else only as context:
<the files and lines the change touched, or its diff>
```

Leave this part out when the check covers the whole project: the first
validation, a validation after a failed or skipped one, and a new or changed
Truth.

## Reading the Levels, Truths, Commits and Code

```text
The Levels are in <path>/trustfall/: 1-concepts.md, 2-stories.md,
3-architecture.md, 4-module-trees.md, and the Truths in truths.md.
The Commits of the change are <commit range> in the Git repository.
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
