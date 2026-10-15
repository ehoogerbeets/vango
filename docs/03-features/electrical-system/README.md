# Feature: Electrical System

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-13

## Summary

Separate house electrical system for the e-Sprinter: **48V DC** battery bus for heat pump and fridge/freezer, plus inverter/charger with **120V AC** (cooking/plugs) and **240V AC** (instant water heaters). Traction battery is not a house source ([ADR-0002](../../05-decisions/0002-mercedes-e-sprinter-platform.md), [ADR-0003](../../05-decisions/0003-all-electric-house-systems.md), [ADR-0004](../../05-decisions/0004-48v-house-dc-bus.md)).

## Goals

- Power ~3 off-grid nights without want
- Efficient continuous loads on 48V DC
- Maintainable, well-labeled, serviceable layout
- Light enough for ~2,624 lb payload class

## Non-goals

- Powering the house from the drive battery
- Onboard generator / combustion charging

## Requirements

### Must

- Separate house battery (LiFePO₄; solid-state later if practical)
- **48V DC** bus supporting heat pump + fridge/freezer
- Inverter/charger sized for induction, oven/microwave, exterior AC (**120V**) and instant EW (**240V**)
- Solar PV charging into the house bank (sizing TBD)
- North America shore power **120/240V** capable (v1)
- DC power for pump, toilet, dump valves, tank sensors / controls

### Should

- Clear voltage-domain labeling (48V DC vs 120V AC vs 240V AC)
- Convenient access to fuses, shunts, BMS, inverter

### Could

- Derived 12V bus for lights / small electronics

## Design notes

- Architecture overview: [electrical architecture](../../02-architecture/electrical.md)

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | Separate house battery | No traction export | V2L / traction tap | decided |
| 2026-10-13 | 48V DC bus | Heat pump + fridge are 48V DC | 12V / 24V / all-AC | decided |

Detail write-ups: [decisions.md](decisions.md) · ADRs: 0003, 0004

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| House battery 48V | | | LiFePO₄ first | researching | |
| Inverter/charger | | | High AC output | researching | |
| Solar charge controller | | | 48V nominal | researching | |

Full list: [products.md](products.md) · master BOM: [../../06-shopping/bom.md](../../06-shopping/bom.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Layout | Tech locker / cable routes |
| Roof / exterior | Solar PV |

| Depended on by | Why |
|----------------|-----|
| Heating & cooling | 48V heat pump |
| Galley | 48V fridge; 120V cook |
| Plumbing | **240V** instant HW; DC valves/sensors |

## Risks & open questions

- AC load peaks vs inverter size
- Whether lights/pumps are native 48V or 12V derived

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [ADR-0003](../../05-decisions/0003-all-electric-house-systems.md)
- [ADR-0004](../../05-decisions/0004-48v-house-dc-bus.md)
