# System Architecture

Cross-feature design: how major systems fit together. Individual features own detail; this folder owns the big picture and interfaces.

| Doc | Purpose |
|-----|---------|
| [Layout](layout.md) | Floor plan, zones, ergonomics |
| [Electrical](electrical.md) | Power architecture overview |
| [Daily energy budget](daily-energy-budget.md) | Wh/day rollup → battery & solar sizing |
| [Water](water.md) | Fresh / grey / hot water overview |
| [Climate](climate.md) | Heat, cooling, insulation strategy |
| [Payload budget & balance](weight-and-balance.md) | Running weight vs 2,624 lb payload |
| [Interfaces](interfaces.md) | What systems depend on each other |

## Rule of thumb

If a choice affects **more than one feature**, document it here (and/or as an ADR). Feature folders link back.
