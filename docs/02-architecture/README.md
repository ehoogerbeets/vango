# System Architecture

Cross-feature design: how major systems fit together. Individual features own detail; this folder owns the big picture and interfaces.

| Doc | Purpose |
|-----|---------|
| [Layout](layout.md) | Floor plan, zones, ergonomics |
| [Electrical](electrical.md) | Power architecture overview |
| [Water](water.md) | Fresh / grey / hot water overview |
| [Climate](climate.md) | Heat, cooling, insulation strategy |
| [Weight & balance](weight-and-balance.md) | Payload budget across systems |
| [Interfaces](interfaces.md) | What systems depend on each other |

## Rule of thumb

If a choice affects **more than one feature**, document it here (and/or as an ADR). Feature folders link back.
