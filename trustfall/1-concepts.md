# Concepts

```text
Project — a piece of software whose design is described in Levels and governed by Rules
├── Level — one layer of the Project's description, derived only from the Levels above it
│   ├── Concept map — what the Project talks about
│   ├── User stories — what the Project must let its users do
│   ├── Architecture — the big blocks of the Project and how they connect
│   ├── Module trees — what each Architecture block is made of
│   └── Code — the implementation
├── Rule — something every Level must obey
│   ├── Commandment — a Rule that comes from Trustfall itself and can never be changed or overridden
│   └── Constraint — a Rule the Human sets for this Project
└── Change — a modification to the Project, starting from the highest Level it touches

Descent — working through the Levels one at a time, from the top down
├── Mode — how each Level gets approved during a Descent
│   ├── Collaborative — the Human and the Agent design each Level together, and the Human approves it
│   └── Autonomous — the Agent designs and approves each Level by itself
└── Ascent — interrupting a Descent to change a higher Level that a lower Level found lacking

Participant — someone taking part in a Project
├── Human — the reviewer whose trust Trustfall builds
├── Agent — designs Levels and writes Code
└── Verifier — a fresh Agent with no history of the work, checking one Rule
    └── Verdict — the Verifier's answer: Pass or Fail, with evidence
