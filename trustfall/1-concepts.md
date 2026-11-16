# Concepts

```text
Trustfall — a way of working that maximises trust between a Human and an Agent or a teammate; "the project" below means any project built with Trustfall
├── Descent — working through the Levels one at a time, always starting from the topmost Level
│   └── Level — one layer of the project's description, derived only from the Levels above it, the "what" of this project
│       ├── Level types
│       │   ├── 1 Concepts — what the project talks about
│       │   ├── 2 User stories — what the project must let its users do
│       │   ├── 3 Architecture — only self-contained Mermaid diagrams of the Blocks of the project and how they connect
│       │   │   └── Block — a concrete technology the project does not implement itself, named after the one instance of it the project has, e.g. Orders service (a Node.js service), Task database (a PostgreSQL database)
│       │   ├── 4 Module trees — what is built on each Block
│       │   └── 5 Code — the implementation
│       └── Item — one single thing on a Level, digestible on its own
├── Constraint — a rule that describes "how" things are done in one project. Only affects code.
└── Commandment — a rule that comes from Trustfall itself and can never be changed or overridden
```
