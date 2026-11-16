# Concepts

```text
Trustfall — a way of working that maximises trust between a Human and an Agent or a teammate
├── Commandment — a rule that comes from Trustfall itself and can never be changed or overridden
├── Constraint — a rule the Human sets for one project
├── Descent — working through the Levels one at a time from the top down, starting from the highest Level a change touches
│   ├── Level — one layer of the project's description, derived only from the Levels above it
│   │   ├── 1 Concepts — what the project talks about
│   │   ├── 2 User stories — what the project must let its users do
│   │   ├── 3 Architecture — the big blocks of the project and how they connect
│   │   ├── 4 Module trees — what each Architecture block is made of
│   │   └── 5 Code — the implementation
│   ├── Mode — how each Level gets approved
│   │   ├── Collaborative — the Human and the Agent design each Level together, and the Human approves it
│   │   └── Autonomous — the Agent designs and approves each Level by itself
│   └── Ascent — interrupting a Descent to change a higher Level that a lower Level found lacking
└── Participant — someone taking part in a project
    ├── Human — the reviewer whose trust Trustfall builds
    ├── Agent — designs Levels and writes Code
    └── Verifier — a fresh Agent with no history of the work, checking one Commandment or Constraint
        └── Verdict — the Verifier's answer: Pass or Fail, with evidence
```
