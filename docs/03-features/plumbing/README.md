# Feature: Plumbing

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-27

## Summary

Fresh / grey / black water with a dual-input fill manifold, rain intake, a fill-side **GoBluTech PURBLU AR3 UVC**, **PEX-A** house distribution (including coffee-maker feed), accumulator, tank sensors, app dump valves, fresh drain/winterize, and **240V** instant HW + solar thermal. Architecture: [water](../../02-architecture/water.md).

## Goals

- Reliable water for weekends through multi-month trips
- Keep the fresh tank clean: **no raw water in**, AR3 on every fill path
- **PEX-A** for easy install, flexibility, and repair
- Steady pressure via accumulator; high fixture flow because filters are not on the demand-pump loop
- Fill from shore hose or a 12V draft pump; top up from roof rain when practical
- See tank levels and dump grey/black from an **app**
- Winterize with compressed air at the shore inlet (30–40 PSI). No RV antifreeze
- Easy filter swaps with a clear wrench radius
- Minimize instant-electric energy via solar thermal preheat

## Non-goals

- No propane / gas water heating
- Overseas norms do not drive v1
- Drinking untreated rain straight from the roof

## Requirements

### Must

- Shore fill + 12V off-grid draft + rain → shared manifold → **GoBluTech AR3 UVC** → fresh tank
- Fresh tank → pre-pump strainer → demand pump → accumulator → fixtures (no second filter/UV train)
- All fresh pressurized distribution in **PEX-A**
- Thin PEX run to **coffee maker** off the clean pressurized loop
- AR3 on **12V** through a buck-boost (12.0–12.5 V)
- Manual **bypass** and **filter inline** valves. Bypass isolates the AR3 and connects the shore inlet to house distribution for the blow-out. Filter inline is the only fill path into the tank
- Shore inlet is standard city-water thread so a brass blow-out plug threads on. Blow-out air stays at **30–40 PSI**
- AR3 bowls come off with a wrench, cartridges are stored dry, and the empty bowls go back on before the UV-chamber air blast
- Instant electric heaters at sink and shower — **240V AC**
- Warm-water storage tank + deployable solar thermal
- **Side quick-connect** for deployable water/glycol solar thermal collector → warm/hot tank loop
- Electric **level sensors** on fresh, grey, and black, on the **first trip**
- **Electric ball valves** on grey and black dump paths, on the **first trip**. A waste tank with no way to empty it is not a finished plumbing system
- Fresh-tank **dump**, low-point drains left open for the winter, and a **quick-connect** strainer on the demand-pump inlet. Procedure: [water architecture](../../02-architecture/water.md#winterize-fresh-side)
- Grey tank + black tank (toilet — see bathroom)
- Filters + UV + accumulator + valves + sensors in accessible service locations
- Light-weight tanks/materials where practical (~2,624 lb payload class)

### Should

- Manual override if app or power fails (valve fail-safe design TBD)
- Solar thermal and rain gear convenient enough to actually use
- Clear labeling of fill ports (pressurized vs trickle) and of **bypass** vs **filter inline**

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
| 2026-10-13 | Multi-stage filters + UV on the drinking path | Particulate polish + kill bacteria/viruses | Minimal filter only | superseded |
| 2026-10-27 | **GoBluTech AR3 UVC** on the **fill** side, before the tank | No raw water in the tank; keep filter pressure drop off the demand pump | Post-pump medium/fine/UV train; raw water into the tank | decided |
| 2026-10-27 | Dual fill manifold: shore inlet + **12V** draft pump; rain into the same manifold | Campgrounds and lakes / jerry cans share one AR3 | Separate filter trains per inlet | decided |
| 2026-10-13 | **PEX-A** distribution | Flexible, easy install/repair | Copper / PEX-B-only / rigid | decided |
| 2026-10-13 | Thin PEX to coffee maker | Convenience — no manual filling | Pitcher-only | decided |
| 2026-10-13 | Accumulator | Stable pressure; less pump cycling | Pump-only | decided |
| 2026-10-13 | Dual fill + rain intake | Flexibility + eco | Single fill only | decided |
| 2026-10-13 | Level sensors on all three tanks | Know status without crawling | Sight tubes only | decided |
| 2026-10-13 | Electric ball valves grey+black + app | Convenient dump | Manual dump only | decided |
| 2026-10-13 | Fresh drain / winterize path | Easy seasonal storage | Partial drain hacks | decided |
| 2026-10-27 | Winterize with **compressed air** at the shore inlet, **30–40 PSI**, no antifreeze | Mild coastal storage. Antifreeze tastes and complicates spring start | RV antifreeze in the lines | decided |
| 2026-10-27 | AR3 **bypass** vs **filter inline**. Bypass is winterize-only | Fixture blow-out skips the cartridges; a 10–15 s inline blast clears the UV chamber. Fill never skips the AR3 | Blowing air through wet cartridges; a second winterize port | decided |
| 2026-10-13 | Under-mount tanks + dump penetrations aft of rear axle only | Battery under floor | Mid-van under-mount / battery-floor drill | decided |
| 2026-10-25 | Fresh tank is **~35 gal**, inside on the passenger wheel well | Trailer-less 3 days inside the 30–40 gal band | Stock ~20–22 gal wheel-well tank | decided |
| 2026-10-27 | Grey **~26 gal**, black **~9 gal** | Waste sum equals fresh (RO reject returns to waste). ~3:1 grey:black | 60/40 split; waste tanks larger than fresh | decided |
| 2026-10-25 | Rain is drinking water **after fill filtration and UV** | Same treatment as hose water | Utility-only rain; skipping rain capture | decided |
| 2026-10-27 | Rain joins the **AR3 fill manifold** | One purification path for shore, draft, and rain | A second rain-only filter train | decided |

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Fill filter + UV | GoBluTech | **PURBLU AR3 UVC** 5-inch | Fill-side 4-stage; 12V ~1 A; keeps tank clean | preferred | [products](products.md) |
| AR3 buck-boost | | 12V → 12.0–12.5 V | Protect UV from charge spikes | preferred | |
| Off-grid draft pump | | 12V submersible / marine transfer | Lakes, streams, jerry cans into the fill manifold | preferred | |
| Pre-pump strainer | | Quick-connect at the pump inlet | Protect the pump; pulls off so the pump can run a few seconds dry | researching | |
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
| Grey tank | | **~26 gal** under floor, driver side, aft of axle | ~3:1 with black; sum equals fresh | preferred | |
| Black tank | | **~9 gal** under floor, driver side, aft of axle | Low-flow marine toilet | preferred | |
| Level sensors (×3) | | | app integration | researching | |
| Electric ball valve (grey) | | | app actuated | researching | |
| Electric ball valve (black) | | | app actuated | researching | |
| Fresh tank dump valve | | | Drained before the pump is bumped dry | researching | |
| Low-point drain valves | | | Left open for the winter | researching | |
| Shore blow-out plug | | Brass, city thread → Schrader or 1/4" QC | Kept with the van. Compressor is the portable one, regulated to 30–40 PSI | preferred | |
| AR3 filter wrench | | Fits the 5-inch bowls | Canister removal for drying and winterize | preferred | |

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
- Bypass left on by mistake would put unfiltered shore water at the faucets. Valves need a clear label, and bypass stays a winterize position
- A hard freeze is outside this blow-out. Design weather is above about 40°F

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [water architecture](../../02-architecture/water.md)
- [ADR-0003](../../05-decisions/0003-all-electric-house-systems.md)
