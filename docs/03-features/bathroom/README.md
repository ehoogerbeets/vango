# Feature: Bathroom

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-13

## Summary

Toilet + shower + storage in a space-efficient footprint **toward the rear of the van** so drains gravity-feed under-mount tanks behind the rear axle ([ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md)). When wet areas are idle, storage occupies that volume and moves away easily when bath is needed.

## Goals

- Dedicated **toilet area**
- Dedicated **shower area** in the end state (usable for 6'2" / comfortable for 5'2"). **Not on the first trip** — toilet and a cold sink ship first. Habit once it exists: **navy showers** in the van, real showers at campgrounds
- **Storage area** that reclaims unused bath/shower volume
- Transitions must be quick and convenient — no wrestling with the layout every use
- Align with eco, light weight, maintainability, and modern calm aesthetic

## Non-goals

- Not solving overseas plumbing/electrical norms in v1
- Not a full residential bath if that fights space/weight/convenience (decide later)

## Requirements

### Must

- Toilet area, shower area, and storage area as distinct roles (may share footprint over time)
- Storage moves/swings clear of toilet and shower without hassle
- Standing / shower clearance suitable for 6'2" when the shower is built
- First trip: toilet + cold sink. Leave aft volume and grey-tank capacity so a later navy-shower stall does not require a new tank
- **Low-flow marine electric-flush toilet** (conventional marine style, not composting/cassette-as-primary)
- Black tank + dump path for toilet waste (**tank + floor penetrations aft of rear axle only**)
- **Aft, on the driver’s side**, so the toilet and shower gravity-drain to grey and black tanks on that same side ([layout](../../02-architecture/layout.md))
- Easy to winterize with the rest of the van
- Night trips are common: a clear, dark-friendly path from the bed to this toilet without disturbing the bed

### Should

- Filters / service points accessible (shared plumbing maintainability goal)
- Materials and methods consistent with eco-friendly philosophy

### Could

-

## Design notes

- Flagship example of multi-use space from [vision](../../00-overview/vision.md)
- Layout integration TBD in [layout architecture](../../02-architecture/layout.md)
- Water / HW / flush supply: [water architecture](../../02-architecture/water.md)
- Electric flush is a house DC load — confirm product voltage vs 48V bus / DC-DC

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | Low-flow marine electric-flush toilet + black tank | Familiar flush experience; low water use | Composting; cassette-as-primary | decided |
| 2026-10-13 | Bathroom / shower aft | Gravity to aft under-mount tanks; no battery-floor penetrations | Forward wet bath; rear garage layout | decided |
| 2026-10-25 | Indoor shower is **post-MVP** | First trip is toilet + cold sink | Shower stall on the first trip | decided |
| 2026-10-25 | End-state shower habit is a **navy shower**; campgrounds for a real shower | Sizes water use without a residential shower | Daily full showers in the van | decided |

Detail write-ups: [decisions.md](decisions.md) · cross-cutting: [ADRs](../../05-decisions/README.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Marine electric-flush toilet | | | Low-flow | researching | |
| Black tank | | | Size TBD | researching | |

Full list: [products.md](products.md) · master BOM: [../../06-shopping/bom.md](../../06-shopping/bom.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Plumbing | Flush water, shower HW, grey/black tanks |
| Electrical | Electric flush; instant EW |

| Depended on by | Why |
|----------------|-----|
| Layout | Wet-zone footprint + multi-use storage |

## Risks & open questions

- Aft volume has to hold a later shower stall without moving the toilet or the tanks
- Grey tank sized for navy showers even while the stall is still post-MVP

## Stories (future Jira)

See [stories.md](stories.md). Keep these outcome-oriented so they convert cleanly later.

## References

-
