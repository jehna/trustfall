# Constraints

- C1: Trustfall is distributed as a group of Claude Code skills.
  Verify: the Code level consists of skill directories, each with a SKILL.md.
- C2: Every Level except Code is plain text that produces a readable line diff.
  Verify: Level files contain only Markdown, ASCII trees, lists and Mermaid; one item per line.
- C3: A Descent can be run in two modes with the same process: Collaborative, where the Human and the Agent design each Level together and the Human approves it; and Autonomous, where the Agent designs and approves each Level by itself.
  Verify: the skills describe both modes, and the steps of a Descent are identical in both apart from who approves a Level.
- C4: Every check of a Commandment or Constraint is done by a fresh Agent with no history of the work, answering Pass or Fail with evidence.
  Verify: the skills instruct verification through fresh, non-forked subagents that return Pass/Fail with file:line evidence.
