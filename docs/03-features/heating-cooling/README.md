# Feature: Heating & Cooling

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-13

## Summary

Cabin heat and cooling under an **all-electric** rule ([ADR-0003](../../05-decisions/0003-all-electric-house-systems.md)). **48V DC heat pump** ([ADR-0004](../../05-decisions/0004-48v-house-dc-bus.md)). No diesel heater, no propane furnace.

## Goals

- Comfort for good-weather primary season; occasional winter use
- Energy-efficient enough for ~3-night off-grid targets when paired with insulation + electrical design
- Convenient controls; maintainable service access

## Non-goals

- No combustion heating of any kind onboard
- Not optimizing for full-time deep-winter living

## Requirements

### Must

- Electric-only active climate systems
- Compatible with e-Sprinter platform constraints ([ADR-0002](../../05-decisions/0002-mercedes-e-sprinter-platform.md))
- **48V DC heat pump** as the active HVAC approach (heat + cool path)
- Pair with serious insulation (cool-season retain heat; desert reject heat while AC runs)

### Should

-

### Could

-

## Design notes

- **Not** planning resistive primary heat or heated mattress pads at this time ([ADR-0003](../../05-decisions/0003-all-electric-house-systems.md))
- Brand / BTU TBD — voltage domain is locked at **48V DC** ([ADR-0004](../../05-decisions/0004-48v-house-dc-bus.md))


## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| | | | | |

Detail write-ups: [decisions.md](decisions.md) · cross-cutting: [ADRs](../../05-decisions/README.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| | | | | researching | |

Full list: [products.md](products.md) · master BOM: [../../06-shopping/bom.md](../../06-shopping/bom.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| | |

| Depended on by | Why |
|----------------|-----|
| | |

## Risks & open questions

-

## Stories (future Jira)

See [stories.md](stories.md). Keep these outcome-oriented so they convert cleanly later.

## References

-
