# Norwegian Cabin (Hytte) Monitoring — UML Project

A spec-driven mock-up of a remote monitoring system for a Norwegian cabin (*hytte*), modelled in UML. The system tracks the three things a cabin owner cares about while away: **inside temperature**, **energy consumption**, and **security**.

> University project — Systemmodellering og -arkitektur (TSD2080-1 26H), 2nd year, 1st semester, USN.

---

## Overview

Cabins are often remote and left empty for weeks, so problems — a frozen pipe, a spike in power use, a break-in — can go unnoticed until it is too late. This project models a system that reads sensors inside the cabin, checks them against safe thresholds, and pushes an alert to the owner's phone when something is wrong.

The aim of the assignment was not to ship production code, but to **design** the system using a specification-driven AI flow and to **model** its structure and behaviour in UML.

## What it monitors

- **Temperature** — warns the owner when the inside temperature drops toward freezing (frost / burst-pipe risk).
- **Energy consumption** — flags abnormally high power usage.
- **Security** — reports door and motion events.

## Approach: spec-driven development

Rather than prompting an AI agent turn by turn, the system is built from a written **specification** that serves as the source of truth: the agent plans against it, breaks it into tasks, and implements them while we review at checkpoints. The UML models below capture the design that the specification describes.

## System models (UML)

All diagrams live in [`docs/diagrams/`](docs/diagrams/README.md), with editable sources (`.puml` / `.mmd`) next to the rendered images.

![Use case diagram](docs/diagrams/usecase.png)

| Diagram | What it shows |
|---------|---------------|
| [Use case](docs/diagrams/usecase.png) | What the system does, and for whom |
| [Class](docs/diagrams/classdiagram.png) | The structure: classes and their relationships |
| [Sequence](docs/diagrams/sequence.png) | How components interact over time |
| [Activity](docs/diagrams/activity.png) | The monitoring cycle's decision logic |
| [State machine](docs/diagrams/statemachine.png) | The system's operating modes |

## Repository structure

​```
.
├── docs/
│   └── diagrams/     UML sources (.puml/.mmd) + rendered .png + README
├── specs/            specification / constitution files (spec-driven flow)
├── src/              mock-up implementation
└── README.md
​```

## Regenerating the diagrams

Four diagrams use PlantUML and one (the sequence diagram) uses Mermaid. See [`docs/diagrams/README.md`](docs/diagrams/README.md) for the exact commands.

## Team

- Sergiu — [@your-github-username](https://github.com/your-github-username)
- [@teammate-username](https://github.com/teammate-username)
- [@teammate-username](https://github.com/teammate-username)
- [@teammate-username](https://github.com/teammate-username)

Group repository: <link to the group repo, if it is public>

## License

<Optional — e.g. MIT. Remove this section if you would rather not add one.>
