# Feature: Plumbing

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-25

## Summary

Fresh / grey / black water with dual fill, rain intake, **coarse → medium → fine → UV** treatment, **PEX-A** distribution (including coffee-maker feed), accumulator, tank sensors, app dump valves, fresh drain/winterize, and **240V** instant HW + solar thermal. Architecture: [water](../../02-architecture/water.md).

## Goals

- Reliable water for weekends through multi-month trips
- Clean fresh tank via fill filtration; drinking path via multi-stage filters + UV
- **PEX-A** for easy install, flexibility, and repair
- Steady pressure via accumulator
- Fill from hose or trickle; top up from roof rain when practical
- See tank levels and dump grey/black from an **app**
- Empty / winterize fresh easily
- Easy filter + UV lamp service
- Minimize instant-electric energy via solar thermal preheat

## Non-goals

- No propane / gas water heating
- Overseas norms do not drive v1
- Drinking untreated rain straight from the roof

## Requirements

### Must

- Pressurized fill + trickle fill + rain → fill filtration → fresh tank
- Fresh → coarse/strainer → pump → accumulator → **medium → fine → UV** → fixtures
- All fresh pressurized distribution in **PEX-A**
- Thin PEX run to **coffee maker** (after treatment train)
- Instant electric heaters at sink and shower — **240V AC**
- Warm-water storage tank + deployable solar thermal
- **Side quick-connect** for deployable water/glycol solar thermal collector → warm/hot tank loop
- Electric **level sensors** on fresh, grey, and black (app-readable)
- **Electric ball valves** on grey and black dump paths (app open/close)
- Dedicated fresh tank **drain / winterize** path
- Grey tank + black tank (toilet — see bathroom)
- Filters + UV + accumulator + valves + sensors in accessible service locations
- Light-weight tanks/materials where practical (~2,624 lb payload class)

### Should

- Manual override if app or power fails (valve fail-safe design TBD)
- Solar thermal and rain gear convenient enough to actually use
- Clear labeling of fill ports (pressurized vs trickle)

### Could

-

## Design notes

- Full flow diagrams: [water architecture](../../02-architecture/water.md)
- App / telemetry: [connectivity](../connectivity/README.md)
- **240V** HW drives inverter topology: [electrical](../../02-architecture/electrical.md)

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | Instant EW + solar thermal warm tank | ADR-0003 | Propane HW | decided |
| 2026-10-15 | Side quick-connect for water/glycol solar thermal | Deploy collector without roof plumbing dance | Hard-plumbed roof-only collector | proposed |
| 2026-10-13 | Instant EW **240V** | Real tankless power needs | 120V tankless | decided |
| 2026-10-13 | Coarse + medium + fine filters + UV | Particulate polish + kill bacteria/viruses | Minimal filter only | decided |
| 2026-10-13 | **PEX-A** distribution | Flexible, easy install/repair | Copper / PEX-B-only / rigid | decided |
| 2026-10-13 | Thin PEX to coffee maker | Convenience — no manual filling | Pitcher-only | decided |
| 2026-10-13 | Accumulator | Stable pressure; less pump cycling | Pump-only | decided |
| 2026-10-13 | Dual fill + rain intake | Flexibility + eco | Single fill only | decided |
| 2026-10-13 | Level sensors on all three tanks | Know status without crawling | Sight tubes only | decided |
| 2026-10-13 | Electric ball valves grey+black + app | Convenient dump | Manual dump only | decided |
| 2026-10-13 | Fresh drain / winterize path | Easy seasonal storage | Partial drain hacks | decided |
| 2026-10-13 | Under-mount tanks + dump penetrations aft of rear axle only | Battery under floor | Mid-van under-mount / battery-floor drill | decided |
| 2026-10-25 | Fresh tank is **~35 gal**, inside on the passenger wheel well | Trailer-less 3 days inside the 30–40 gal band | Stock ~20–22 gal wheel-well tank | decided |
| 2026-10-25 | Rain is drinking water **after fill filtration and UV** | Same treatment as hose water | Utility-only rain; skipping rain capture | decided |

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Fill filtration | | | Before tank | researching | |
| Coarse filter / pre-pump strainer | | | Protect pump | researching | |
| Medium filter | | | | researching | |
| Fine filter | | | | researching | |
| UV irradiator | | | Bacteria/viruses; service access | researching | |
| PEX-A + fittings system | | | Whole-van distribution | researching | |
| Demand pump | | | Voltage TBD | researching | |
| Accumulator | | | | researching | |
| Coffee-maker PEX stub / valve | | | Thin line | researching | |
| Instant EW 240V (sink) | | | | researching | |
| Instant EW 240V (shower) | | | | researching | |
| Solar thermal collector | | | deployable water or glycol | researching | |
| Thermal quick-connect (side) | | | Ext. port → warm/hot tank loop | researching | |
| Warm tank | | | | researching | |
| Fresh tank | | **~35 gal** passenger wheel well | Inside galley base | preferred | |
| Grey / black tanks | | | light-weight, under floor aft | researching | |
| Level sensors (×3) | | | app integration | researching | |
| Electric ball valve (grey) | | | app actuated | researching | |
| Electric ball valve (black) | | | app actuated | researching | |
| Fresh drain / winterize valve | | | | researching | |

Full list: [products.md](products.md) · master BOM: [../../06-shopping/bom.md](../../06-shopping/bom.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Electrical system | **240V** instant EW; DC for pump/valves/sensors |
| Connectivity | App for levels + valve control |
| Layout | Tank, service access, fill/dump port placement |
| Exterior / roof | Rain capture, solar thermal stowage |
| Bathroom | Shower HW; black tank / toilet |

| Depended on by | Why |
|----------------|-----|
| Galley | Sink cold/HW |
| Bathroom | Shower + toilet flush water |

## Risks & open questions

- **240V** instant HW peak vs inverter/battery — need load management; avoid HW + big cook simultaneously if undersized
- Valve default on power loss; manual dump override
- Rain potability standard
- Black + grey weight when full vs payload

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [water architecture](../../02-architecture/water.md)
- [ADR-0003](../../05-decisions/0003-all-electric-house-systems.md)
