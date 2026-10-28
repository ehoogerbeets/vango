# Feature: Galley

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-25

## Summary

Cooking and food prep for two, located **aft near the shower** so the sink can gravity-drain to under-mount tanks behind the rear axle ([ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md)). Installed appliances are **electric only** ([ADR-0003](../../05-decisions/0003-all-electric-house-systems.md)). Outdoor campfire / grill cooking is allowed as a lifestyle exception.

## Goals

- Convenient enough that we cook for real (vision: omit if awkward)
- Support weekenders through multi-month trips
- Align with eco, light weight, modern calm look

## Non-goals

- No propane / camping-gas cooktop or oven onboard
- Overseas voltage norms do not drive v1

## Requirements

### Must

- No combustion fuels as installed galley energy
- Work within e-Sprinter electrical / weight budgets ([ADR-0002](../../05-decisions/0002-mercedes-e-sprinter-platform.md))
- **Aft, on the sliding-door / passenger side.** The tall fridge is the end **toward the bed**; the counter continues **aft toward the rear doors**. Sink drains across to the driver-side grey tank behind the axle ([layout](../../02-architecture/layout.md))
- Cabinetry over battery floor span uses **OEM tie-downs only** if floor-mounted
- **2-burner induction** cooktop (120V AC, **3,000 W** nameplate) on the first trip
- **Fridge / freezer** — **Furrion Arctic 10.7** cu ft, **12V DC**, dual-swing door; powered from 48V house via DC-DC — see [daily energy budget](../../02-architecture/daily-energy-budget.md)
- Combo **oven / air-fryer** and a **microwave** share a **1,500 W** circuit. They complete the van after the first trip; the brand waits ([requirements](../../01-van/requirements.md))
- **Pod coffee maker** — **Keurig K-Slim / K-Mini** or a **Nespresso** — with a dedicated thin **PEX-A** feed. Same timing as the oven: after MVP, brand still open — [water](../../02-architecture/water.md)
- Countertop is **Paperstone** (recycled-paper solid surface), with the induction inset and the sink cut into it
- The cabinet face beside the sink carries the mirror. That mirror is its own project ([interior finish](../interior-finish/README.md))
- Induction can move to **exterior AC outlet** for outdoor cooking
- **Normal dinner is indoors** on the 2-burner induction (2026-10-25). Outdoor grill stays available; it is not the usual meal
- **Electric grill** for outdoor use; wood campfire when the site has one

### Should

- Convenient deploy for outdoor induction (vision: ultra-convenient or omit)
- Coffee maker plumbing includes an easy shutoff for service

### Could

-

## Design notes

- Cook loads are inverter **120V AC**; fridge stays on **DC** (12V via DC-DC — inverter not required for refrigeration)
- Coordinate AC peaks with instant HW ([electrical architecture](../../02-architecture/electrical.md))
- Fridge is the **Furrion Arctic 10.7** dual-swing. GE Profile 9.8 was the lighter one-hinge alternate — [products.md](products.md)
- Coffee line is post-UV treated water. Both candidates are reservoir pod machines, so the chosen one has to accept a pressurized (or regulated) feed, or a small bypass of its tank
- Paperstone is the eco counter. It is a paper composite, not the maple-veneer cabinet panel and not stainless

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | Plumbed thin PEX feed to coffee maker | Convenience | Manual fill only | decided |
| 2026-10-15 | Target medium ~10 cu ft **12V** dual-hinge fridge | Residential capacity + DC efficiency | Propane absorption; tiny compressor fridges | decided |
| 2026-10-27 | Fridge is the **Furrion Arctic 10.7** dual-swing | The door has to open from either side | GE Profile reversible hinge (lighter, one side at a time) | decided |
| 2026-10-25 | Counter is **Paperstone** | Eco paper-composite surface | Solid-surface generic, butcher block, stainless, maple cabinet panel | decided |
| 2026-10-25 | Coffee is a **Keurig Mini or Nespresso** pod machine | Small, plumbed, short heat cycle | Drip brewer; espresso boiler; kettle plus a manual brewer | decided |

Detail write-ups: [decisions.md](decisions.md) · cross-cutting: [ADRs](../../05-decisions/README.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Coffee maker (plumbed) | Keurig Mini or Nespresso | Pod machine | Accepts thin PEX feed | preferred | |
| Countertop | Paperstone | Paper-composite solid surface | Eco; induction and sink cutouts | preferred | |
| Induction cooktop | | | 2-burner | researching | |
| Oven / air-fryer | | | Ninja Flip class | researching | |
| Microwave | | | Small | researching | |
| Fridge / freezer 12V | Furrion Arctic **10.7** dual-swing | | Door opens from either side | preferred | [products](products.md) |

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
