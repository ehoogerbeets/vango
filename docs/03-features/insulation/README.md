# Feature: Insulation

> Status: `researching`  
> Priority: `P1`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-25

## Summary

Plant-based insulation. The floor is already **1" PlantPanel X**. The ceiling uses the same hemp board, packed into the roof ribs so it does not spend the standing-height budget. Large wall cavities get hemp. Small voids that a board cannot fill get **wool**, stuffed in.

## Goals

- Keep the ~5" floor + ceiling + clearance budget for a 6'2" stance ([constraints](../../00-overview/constraints.md))
- Stay on the eco material path (hemp and wool, not foam as the default)
- Support the later heat pump by slowing heat through the central sleep zone

## Non-goals

- A foam-first shell
- Ceiling insulation that hangs below the ribs and steals headroom

## Requirements

### Must

- Floor: **1" Hempitecture PlantPanel X**, glued down — [floor](../floor-subfloor/README.md)
- Ceiling: PlantPanel in the roof-rib bays. Planning assumption: those ribs are about **2–2.5" deep**, so the board fills existing depth. **Confirm rib depth on the van** before buying thickness
- Walls: hemp board in the large cavities
- Wool only where the opening is too small or too irregular for a board

### Should

- Same hemp product family as the floor, so offcuts and adhesives stay consistent
- Ceiling thickness follows the measured rib, including a thicker sheet or a stack, rather than a second layer below the ribs

### Could

-

## Design notes

The finish ceiling is a separate thin panel ([walls and ceiling](../walls-ceiling/README.md)). Insulation stops at the rib face. Only that finish panel comes out of the standing-height budget.

Floor stack is already ~1.5–1.8" of the ~5" budget. Do not add ceiling insulation thickness on top of that.

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-25 | Ceiling insulation is **PlantPanel inside the roof ribs** | High-R without giving up headroom | A hemp layer hung below the ribs; foam to save thickness | decided |
| 2026-10-25 | **Hemp for large cavities, wool for small voids** | Board where it fits; stuff wool where a board will not | Wool everywhere; foam in the small holes | decided |

Detail write-ups: [decisions.md](decisions.md) · cross-cutting: [ADRs](../../05-decisions/README.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Floor + ceiling + large wall bays | Hempitecture PlantPanel X | | Same board as the floor. Ceiling thickness = measured rib depth | preferred | [products](products.md) |
| Small voids | Wool (product open) | | Stuffable | researching | [products](products.md) |

Full list: [products.md](products.md) · master BOM: [../../06-shopping/bom.md](../../06-shopping/bom.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Van | Measured ceiling-rib depth sets PlantPanel thickness |
| Floor | Shares the 1" floor layer and the standing-height budget |

| Depended on by | Why |
|----------------|-----|
| Walls & ceiling | Finish panel sits on the rib-face insulation |
| Heating & cooling | Shell performance for the later heat pump |

## Risks & open questions

- Actual e-Sprinter high-roof rib depth (assumed ~2–2.5", not measured)
- Which wool product, and how it stays put in a vibrating van
- PlantPanel thicknesses stocked, versus stacking the 1" floor sheet in a deeper rib

## Stories (future Jira)

See [stories.md](stories.md). Keep these outcome-oriented so they convert cleanly later.

## References

- [Floor & subfloor](../floor-subfloor/README.md)
- [Walls & ceiling](../walls-ceiling/README.md)
