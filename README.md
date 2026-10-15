# VanGo — Camper Van Build Planner

Planning docs for a camper van build, managed like a software project: decisions first, build later as Agile/Scrum work (epics → stories → tasks in Jira).

## How this repo works

| Phase | What we do here |
|-------|-----------------|
| **Now** | Capture vision, constraints, features, and decisions in Markdown |
| **Later (build)** | Turn features into Jira epics/stories and execute in sprints |

## Document map

```
docs/
├── 00-overview/          Vision, goals, constraints, glossary
├── 01-van/               Base vehicle selection & specs
├── 02-architecture/      System-level design (power, water, layout)
├── 03-features/          One folder per build feature (epics)
├── 04-backlog/           Cross-cutting backlog notes & sprint ideas
├── 05-decisions/         Architecture Decision Records (ADRs)
├── 06-shopping/          Master BOM, vendors, budget rollup
└── templates/            Copy-paste templates for new docs
```

Start here:

1. [Vision & goals](docs/00-overview/vision.md)
2. [Constraints](docs/00-overview/constraints.md)
3. [Feature index](docs/03-features/README.md)
4. [Decision log](docs/05-decisions/README.md)

## Conventions

- **One decision = one record** — use ADRs for cross-cutting choices; feature folders for feature-scoped choices.
- **Always record *why*** — options considered, rejected alternatives, and trade-offs.
- **Products get a Product Choice block** — brand, model, link, price estimate, status.
- **Status values:** `idea` · `researching` · `decided` · `purchased` · `installed` · `deferred` · `rejected`
- **Jira mapping (later):** each feature folder ≈ Epic; each story in `stories.md` ≈ Story; checklist items ≈ Tasks/Sub-tasks.

## Status legend (features)

| Status | Meaning |
|--------|---------|
| `idea` | Not researched yet |
| `researching` | Options being compared |
| `decided` | Approach chosen; may still need product picks |
| `ready` | Specced enough to become Jira tickets |
| `building` | In progress during the build phase |
| `done` | Complete |
| `deferred` | Parked intentionally |
| `rejected` | Explicitly out of scope |
