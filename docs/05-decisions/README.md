# Architecture Decision Records (ADRs)

Cross-cutting decisions that multiple features must respect. Feature-local choices stay in that feature's `decisions.md`.

## Index

| ID | Title | Status | Date |
|----|-------|--------|------|
| ADR-0001 | Record architecture decisions | accepted | 2026-10-13 |
| ADR-0002 | Mercedes e-Sprinter as base vehicle | accepted | 2026-10-13 |
| ADR-0003 | All-electric house systems (no combustion fuels onboard) | accepted | 2026-10-13 |
| ADR-0004 | 48V DC house bus for major DC appliances | accepted | 2026-10-13 |
| ADR-0005 | Traction battery floor no-drill zone and layout consequences | accepted | 2026-10-13 |

## How to add one

1. Copy [../templates/adr.md](../templates/adr.md)
2. Name it `NNNN-short-slug.md` (e.g. `0004-house-battery-topology.md`)
3. Add a row to the index above
4. Link from affected feature READMEs

Number sequentially; never reuse IDs. Supersede instead of deleting.
