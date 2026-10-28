# Feature: Bathroom

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-25

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
- The shower is the **rearmost** slice of that side, directly in front of the **driver’s rear door**. Opening that door exposes the shower hardware
- One **low-flow handheld** on a long hose, with two parks: one aimed into the stall, and one on the **back of the van** for an outside sprinkle
- Outside use stands on a **small platform set on the ground**, so feet stay out of the mud. It is not a step bolted to the van
- Shower hot and cold are in the compressed-air blow-out with the rest of the van ([water](../../02-architecture/water.md#winterize-fresh-side))
- Night trips are common: a clear, dark-friendly path from the bed to this toilet without disturbing the bed

### Should

- Filters / service points accessible (shared plumbing maintainability goal)
- Materials and methods consistent with eco-friendly philosophy

### Could

-

## Design notes

- Flagship example of multi-use space from [vision](../../00-overview/vision.md)
- The stall is post-MVP, with the indoor navy shower. The rear-door slice, the long hose, and the outside hook have to be left in the first-trip layout so this does not move the toilet or the tanks
- The mirror lives on the galley cabinet beside the sink, not in this stall ([interior finish](../interior-finish/README.md))
- A ground platform lives with the camp kit (van or trailer), not as bodywork
- Water / HW / flush supply: [water architecture](../../02-architecture/water.md)
- Electric flush is a house DC load — confirm product voltage vs 48V bus / DC-DC

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | Low-flow marine electric-flush toilet + black tank | Familiar flush experience; low water use | Composting; cassette-as-primary | decided |
| 2026-10-13 | Bathroom / shower aft | Gravity to aft under-mount tanks; no battery-floor penetrations | Forward wet bath; rear garage layout | decided |
| 2026-10-25 | Indoor shower is **post-MVP** | First trip is toilet + cold sink | Shower stall on the first trip | decided |
| 2026-10-25 | End-state shower habit is a **navy shower**; campgrounds for a real shower | Sizes water use without a residential shower | Daily full showers in the van | decided |
| 2026-10-25 | Shower is the driver’s-side volume **against the rear door**, and the same handheld also sprinkles outside | Open the door, park the head on the back of the van, stand on a ground platform | A separate outdoor shower; a side-door rinse | decided |

Detail write-ups: [decisions.md](decisions.md) · cross-cutting: [ADRs](../../05-decisions/README.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Marine electric-flush toilet | | | Low-flow | researching | |
| Black tank | | **~9 gal** | With ~26 gal grey; sum equals the 35 gal fresh tank | preferred | |

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
- Grey is **~26 gal** and black is **~9 gal**, summing to the 35 gal fresh tank. Confirm the marine toilet’s flush volume still fits in 9 gal for three days

## Stories (future Jira)

See [stories.md](stories.md). Keep these outcome-oriented so they convert cleanly later.

## References

-
