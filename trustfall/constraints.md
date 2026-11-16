# Constraints

- C1: The skills work on the most common agents: Claude Code, Codex, Antigravity, Pi and OpenCode.
  Verify: the skills use only the shared Agent Skills format (a folder per skill with a SKILL.md and name/description frontmatter) and no agent-specific features without a fallback.
- C2: Every Level except Code is Markdown.
  Verify: every Level file in the Trustfall folder is a .md file, and the skills instruct writing Levels as Markdown.
- C3: All Markdown is linted and formatted before every commit.
  Verify: The project's Markdown linter and formatter is automated to pass on every .md file on precommit hook.
- C4: README uses the template from https://github.com/jehna/readme-best-practices
  Verify: README.md follows the section structure of the template at https://github.com/jehna/readme-best-practices.
