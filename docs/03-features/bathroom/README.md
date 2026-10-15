# Feature: Bathroom

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-13

## Summary

Toilet + shower + storage in a space-efficient footprint **toward the rear of the van** so drains gravity-feed under-mount tanks behind the rear axle ([ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md)). When wet areas are idle, storage occupies that volume and moves away easily when bath is needed.

## Goals

- Dedicated **toilet area**
- Dedicated **shower area** (usable for 6'2" / comfortable for 5'2")
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
- Standing / shower clearance suitable for 6'2"
- **Low-flow marine electric-flush toilet** (conventional marine style, not composting/cassette-as-primary)
- Black tank + dump path for toilet waste (**tank + floor penetrations aft of rear axle only**)
- **Aft placement** with galley wet core ([layout](../../02-architecture/layout.md))
- Easy to winterize with the rest of the van

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

-

## Stories (future Jira)

See [stories.md](stories.md). Keep these outcome-oriented so they convert cleanly later.

## References

-
