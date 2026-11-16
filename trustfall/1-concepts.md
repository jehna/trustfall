# Concepts

```text
Trustfall — a way of working that maximises trust between a Human and an Agent or a teammate
├── Descent — working through the Levels one at a time, always starting from the topmost Level
│   └── Level — one layer of what the project is, derived only from the Levels above it
│       ├── Level types
│       │   ├── 1 Concepts — what the project talks about
│       │   ├── 2 User stories — what the project must let its users do
│       │   ├── 3 Architecture — only self-contained Mermaid diagrams of the Blocks of the project and how they connect
│       │   │   └── Block — a named instance of a technology the project uses but does not implement, e.g. Task database (PostgreSQL)
│       │   ├── 4 Module trees — what is built on each Block
│       │   └── 5 Code — the implementation
│       └── Item — one single thing on a Level, digestible on its own
├── Constraint — a rule that describes "how" things are done in one project. Only affects code.
└── Commandment — a rule that comes from Trustfall itself and can never be changed or overridden
```
