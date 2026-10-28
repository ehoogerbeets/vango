# Feature: Heating & Cooling

> Status: `researching`  
> Priority: `P1`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-28

## Summary

Cabin heat and cooling under an **all-electric** rule ([ADR-0003](../../05-decisions/0003-all-electric-house-systems.md)). Active HVAC is the **Webasto Cool Top Trail 48V** on the house bus ([ADR-0004](../../05-decisions/0004-48v-house-dc-bus.md)). No diesel heater, no propane furnace.

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
- **Webasto Cool Top Trail 48V** as the active HVAC (heat + cool)
- Serve the **central sleeping area** for most of a hot or cold day, with the cab and the aft zone closed off
- Pair with serious insulation (cool-season retain heat; desert reject heat while AC runs)
- Reserve a blanked **14" × 14"** roof cutout before the first trip so the later install does not recut the roof

### Should

-

### Could

-

## Design notes

- **Not** planning resistive primary heat or heated mattress pads at this time ([ADR-0003](../../05-decisions/0003-all-electric-house-systems.md))
- **Webasto Cool Top Trail 48V:** cool **12,300 BTU** (3.6 kW), heat **11,600 BTU** (3.4 kW). Variable-speed inverter compressor, soft start. Nominal draw **0.80–1.40 kW**, peak surge **1.50 kW**. External shroud **44.1" L × 33.5" W × 8.8" H**, with a **4"** unobstructed perimeter for the intake grills. Drops into a standard **14" × 14"** center roof cutout. Product table: [products.md](products.md)
- **First trip is fair weather.** The heat pump is not installed. The factory cab heater and air conditioner are the only climate system on that trip. Cargo comfort depends on mild weather and an open path from the cab; the cargo box is not on the factory HVAC loop.
- High-desert evening cooling is planned for trips that bring the **trailer and its deployable solar**. The van pack is not sized to store three desert days ([daily energy](../../02-architecture/daily-energy-budget.md)).
- Roof coexistence: the solar canopy bridges the Webasto shroud on high-bar risers, and a **MaxxAir MaxxFan Mini Plus** shares the roof with a lower stationary dome. Stacking and rack choices: [exterior](../exterior/README.md). Dual-MPPT array: [electrical](../../02-architecture/electrical.md).
- A **closable cab partition** lets driving use factory HVAC on the cab only, and lets the night heat pump ignore the cab. A second close-off keeps the far-aft galley/bath out of the night zone. Privacy: the closed cab also blocks sightlines into the living area.

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-25 | Heat pump is **post-MVP hardware**, **in-scope for roof space**, and the **first thing added after MVP** | First trip is fair weather; later install should not recut the roof | Omit the roof opening; install the unit before the first trip | decided |
| 2026-10-27 | Desert evening cooling needs the **trailer and its deployable solar** | A van pack that stores three desert days does not fit the payload | A ~40 kWh van pack | decided |
| 2026-10-28 | Heat pump is the **Webasto Cool Top Trail 48V** | Native 48V matches ADR-0004; soft start; real heat-pump heat, not strip heat | Unnamed **120V, 1,590 W** soft-start unit | decided |
| 2026-10-25 | Design weather is **spring–fall, including high desert**. Below ~40°F is out of season | Matches when a heat pump still delivers | Deep-winter / ski as a design case | decided |
| 2026-10-25 | Condition the **central sleep zone** only, most of the day when needed | Smaller volume, privacy, factory HVAC keeps the cab | Whole-cargo HVAC | decided |

Detail write-ups: [decisions.md](decisions.md) · cross-cutting: [ADRs](../../05-decisions/README.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Heat pump | Webasto Cool Top Trail **48V** | | Native 48V; 12.3k BTU cool / 11.6k BTU heat | preferred | [products](products.md) |

Full list: [products.md](products.md) · master BOM: [../../06-shopping/bom.md](../../06-shopping/bom.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Electrical system | **48V** house bus |
| Exterior / roof rack | Clearance over the 8.8" shroud; 4" intake perimeter |
| Insulation | Keeps desert heat out and shoulder-season heat in |

| Depended on by | Why |
|----------------|-----|
| Layout | Cab partition and aft close-off size the conditioned volume |

## Risks & open questions

- Exact roof station for the 14" cutout vs the MaxxFan cutout and the solar canopy risers
- Evening Wh once real duty hours replace the ~3 kWh planning figure

## Stories (future Jira)

See [stories.md](stories.md). Keep these outcome-oriented so they convert cleanly later.

## References

- [climate architecture](../../02-architecture/climate.md)
- [ADR-0003](../../05-decisions/0003-all-electric-house-systems.md)
- [ADR-0004](../../05-decisions/0004-48v-house-dc-bus.md)
