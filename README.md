# Trustfall

> Agent skills that build trust in code by designing it on five reviewable Levels

Code is the hardest thing to review. Trustfall describes a project on five
Levels — Concepts, User stories, Architecture, Module trees and Code — and
designs each Level only from the Levels above it. Every Level is small, plain
Markdown and validated against the Levels above by fresh agents with no history
of the work. When you trust the upper Levels, you can trust what follows from
them, whether the code was written by an agent or a teammate.

## Installing / Getting started

Install the skills into your project with the cross-agent installer:

```shell
npx skills add jehna/trustfall
```

Then ask your agent to start Trustfall:

```text
Let's design this project with Trustfall.
```

The agent loads the `trustfall` skill, asks you about the project, and starts
the Descent from the first Level, Concepts. Each Level is written to a
`trustfall/` folder in your project.

### Initial Configuration

Without the installer, copy or symlink the folders in `skills/` to your agent's
skills folder:

| Agent                               | Project folder    |
| ----------------------------------- | ----------------- |
| Claude Code                         | `.claude/skills/` |
| Codex, Antigravity, Pi and OpenCode | `.agents/skills/` |

## Developing

Trustfall is designed with Trustfall. Its own Levels are in `trustfall/` and the
skills in `skills/`. The skills are linked as project skills for every agent, in
`.claude/skills/` and `.agents/skills/`, so working on Trustfall uses the
current skills.

```shell
git clone https://github.com/jehna/trustfall.git
cd trustfall/
npm install
```

`npm install` installs the Markdown linter and formatter and a Husky pre-commit
hook that formats and lints every staged Markdown file.

### Building

There is nothing to build; the skills are plain Markdown. Format and check them
with:

```shell
npm run format
npm run check
```

`format` rewrites every Markdown file with Prettier, and `check` fails if any
file is unformatted or breaks a markdownlint rule.

### Deploying / Publishing

Push to the default branch; the installer reads the skills straight from the
repository.

## Features

- Five Levels, each designed only from the Levels above it
- One skill per Level, loaded one at a time
- Validation by subagents with no history of the work
- Commandments that hold in every project, kept apart from its Constraints
- Works with Claude Code, Codex, Antigravity, Pi and OpenCode

## Configuration

Each project configures Trustfall through its Constraints in
`trustfall/constraints.md`. The agent asks for them before writing Code.

### Constraint

Type: `Markdown list item`  
Default: none

A rule for how the project is built. It only affects Code.

Example:

```markdown
- C1: Every User story is covered by a browser test.
  Verify: for each story ID there is a browser test that names it, and the tests pass.
```

## Contributing

If you'd like to contribute, please fork the repository and use a feature
branch. Pull requests are warmly welcome. Change the highest Level your change
touches first, and Descend from there.

## Links

- Repository: <https://github.com/jehna/trustfall/>
- Issue tracker: <https://github.com/jehna/trustfall/issues>
- Agent Skills installer: <https://github.com/vercel-labs/skills>

## Licensing

The license has not been chosen yet.
