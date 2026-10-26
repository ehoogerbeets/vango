# Feature: Heating & Cooling

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-13

## Summary

Cabin heat and cooling under an **all-electric** rule ([ADR-0003](../../05-decisions/0003-all-electric-house-systems.md)). **48V DC heat pump** ([ADR-0004](../../05-decisions/0004-48v-house-dc-bus.md)). No diesel heater, no propane furnace.

## Goals

- Comfort for **spring through fall**, including **high-desert afternoons**. Not planned for camping below about **40°F** (heat-pump output falls off; those trips wait)
- The conditioned volume is the **central sleeping area** only. Cab and the far-aft wet/galley zone are closed off at night
- Energy-efficient enough for ~3-night off-grid targets when paired with insulation + electrical design
- Convenient controls; maintainable service access
- **First post-MVP install** after the fair-weather shakedown

## Non-goals

- No combustion heating of any kind onboard
- Not optimizing for full-time deep-winter living
- Not conditioning the cab (factory HVAC) or the far-aft wet/galley zone at night

## Requirements

### Must

- Electric-only active climate systems
- Compatible with e-Sprinter platform constraints ([ADR-0002](../../05-decisions/0002-mercedes-e-sprinter-platform.md))
- **48V DC heat pump** as the active HVAC approach (heat + cool path)
- Serve the **central sleeping area** for most of a hot or cold day, with the cab and the aft zone closed off
- Pair with serious insulation (cool-season retain heat; desert reject heat while AC runs)

### Should

-

### Could

-

## Design notes

- **Not** planning resistive primary heat or heated mattress pads at this time ([ADR-0003](../../05-decisions/0003-all-electric-house-systems.md))
- Brand / BTU TBD — voltage domain is locked at **48V DC** ([ADR-0004](../../05-decisions/0004-48v-house-dc-bus.md))
- **First trip is fair weather.** The heat pump is not installed. The factory cab heater and air conditioner are the only climate system on that trip. Cargo comfort depends on mild weather and an open path from the cab; the cargo box is not on the factory HVAC loop.
- Before the first trip, **choose the heat pump and reserve its roof opening** (blanked until install). The rest of the roof is solar. Size the house battery for the heat pump running **most of the day** in high-desert heat, even though the unit is absent on trip one ([daily energy](../../02-architecture/daily-energy-budget.md)).
- A **closable cab partition** lets driving use factory HVAC on the cab only, and lets the night heat pump ignore the cab. A second close-off keeps the far-aft galley/bath out of the night zone. Privacy: the closed cab also blocks sightlines into the living area.


## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-25 | Heat pump is **post-MVP hardware**, **in-scope for battery and roof space**, and the **first thing added after MVP** | First trip is fair weather; later install should not resize the bank or recut the roof | Omit HVAC from the energy budget; install the unit before the first trip | decided |
| 2026-10-25 | Design weather is **spring–fall, including high desert**. Below ~40°F is out of season | Matches when a heat pump still delivers | Deep-winter / ski as a design case | decided |
| 2026-10-25 | Condition the **central sleep zone** only, most of the day when needed | Smaller volume, privacy, factory HVAC keeps the cab | Whole-cargo HVAC | decided |

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
