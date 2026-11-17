# Truths

- T1: The skills work on the most common agents: Claude Code, Codex, Antigravity, Pi and OpenCode.
  Verify: the skills use only the shared Agent Skills format (a folder per skill with a SKILL.md and name/description frontmatter) and no agent-specific features without a fallback. This project installs agent-specific project level skills for all agents.
- T2: Every Level except Code is Markdown.
  Verify: every Level file in the Trustfall folder is a .md file, and the skills instruct writing Levels as Markdown.
- T3: All Markdown is formatted and linted automatically before every commit by a Husky pre-commit hook, so it cannot be forgotten.
  Verify: `npm install` installs a Husky pre-commit hook that formats and lints every staged .md file and blocks the commit on a lint error.
- T4: README uses the template from <https://github.com/jehna/readme-best-practices>
  Verify: README.md follows the section structure of the template at <https://github.com/jehna/readme-best-practices>.
- T5: Validator subagents run in parallel.
  Verify: the skills instruct launching every Validator subagent of a validation run at once.
- T6: README tells the reader to read the files in the Trustfall folder and links to each of them.
  Verify: README.md tells the reader to read the files in `trustfall/` and links to every file in that folder.
