# Feature: Walls & Ceiling

> Status: `researching`  
> Priority: `P1`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-25

## Summary

Wall and ceiling finishes over the hemp and wool shell. Walls are **painted carbon or aluminum plate**. The ceiling is the **thinnest paintable or fabric-faced panel** that still looks finished, and it is the only ceiling layer that spends standing height. Cabinet faces stay maple veneer over balsa-core carbon ([interior finish](../interior-finish/README.md)). Paint color for the plates, the ceiling, and the outside of the van is one palette, still open, with a designer friend.

## Goals

- A 6'2" person stands upright. Ceiling finish stays thin because insulation already fills the ribs
- A calm surface overhead. Paint or fabric, not a second wood ceiling
- Wall plates that can be painted once the palette exists
- Walls durable enough for daily contact, still light

## Non-goals

- A maple ceiling to match the cabinets
- Stretch fabric as the ceiling
- Leaving the hemp face exposed as the finished ceiling

## Requirements

### Must

- Ceiling finish is a **thin paintable or fabric-faced panel**
- That panel is applied at the rib face, over PlantPanel that stays inside the ribs ([insulation](../insulation/README.md))
- Finish thickness is counted against the ~5" floor + ceiling + clearance budget
- Walls are **carbon or aluminum plate**, painted. Carbon versus aluminum is still open
- Do not lock colors until the designer palette covers interior plates and the shop’s exterior paint

### Should

- Wall plate can be thicker than the ceiling panel. Headroom applies to the ceiling, not the walls
- Service access for wiring stays possible without destroying the lining

### Could

-

## Design notes

Raised-bed underside is its own surface (the “ceiling” you see in the lounge by day) and is specified in [bed / sleep](../bed-sleep/README.md). This feature is the van’s structural ceiling, visible when the bed is down and around the bed opening.

No brand for the thin panel yet. Pick it for thickness and a finished face, then for weight.

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-25 | Ceiling finish is the **thinnest paintable or fabric-faced panel** | Headroom. Insulation is already in the ribs | Maple ceiling; stretch fabric; exposed hemp | decided |
| 2026-10-25 | Walls are **painted carbon or aluminum plate** | A paintable shell, separate from maple cabinet faces | Fabric walls; maple wall panels; the ceiling panel reused on the walls | decided |
| 2026-10-25 | **Color scheme is open** | A designer friend sets interior and exterior colors together | Picking colors before that consult | decided |

Detail write-ups: [decisions.md](decisions.md) · cross-cutting: [ADRs](../../05-decisions/README.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Ceiling panel | | Thin, paintable or fabric-faced | Only ceiling layer in the height budget | researching | [products](products.md) |
| Wall plates | | Carbon or aluminum, painted | Shell lining, not the maple cabinets | researching | [products](products.md) |

Full list: [products.md](products.md) · master BOM: [../../06-shopping/bom.md](../../06-shopping/bom.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Insulation | Rib-fill PlantPanel is the substrate |
| Floor stack | Shares the standing-height budget |

| Depended on by | Why |
|----------------|-----|
| Interior finish | Ceiling is not the maple cabinet face |
| Bed / sleep | Structural ceiling vs the bed’s underside |

## Risks & open questions

- How thin a panel can be and still hide ribs and fasteners
- Carbon plate versus aluminum plate on the walls (weight, paint, and the standing of the eco goal)
- Paint versus fabric on the ceiling, once a panel exists
- The actual colors, after the designer consult

## Stories (future Jira)

See [stories.md](stories.md). Keep these outcome-oriented so they convert cleanly later.

## References

- [Insulation](../insulation/README.md)
- [Interior finish](../interior-finish/README.md)
