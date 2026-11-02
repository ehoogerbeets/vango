# Feature: Floor & Subfloor

> Status: `researching`  
> Priority: `P1`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-11-02

## Summary

Finished floor and subfloor stack under the standing-height budget (~5" shared with ceiling), with a hard **traction-battery keep-out**: no drilling/mounting through the floor from B-pillar to rear axle except **OEM tie-downs** ([ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md)).

**Preferred eco stack:** ⅜" cork in the OEM floor valleys → sealed ¾" PlantPanel I flat cap → ⅛" aluminum sheet floated on adhesive for stability → ~7 mm waterproof engineered bamboo (click-lock). Glue lines are a zero-VOC adhesive. See [products.md](products.md).

## Goals

- Preserve 6'2" standing height (thin stack)
- Safe vs HV battery
- Provide a flat, modern finish floor
- Land cabinetry loads on structure that is allowed (tie-downs, walls, aft zone)

## Non-goals

- Through-bolting furniture into the battery floor span
- Under-mount tank penetrations mid-van

## Requirements

### Must

- **No floor drilling** in B-pillar → rear axle battery zone (aside from uselessly small OEM-safe spots)
- Any work near the pack: understand underside first; **drill from bottom upward** if a permitted hole is used
- Furniture/cabinets over the battery span attach via **existing tie-down points** (layout designed to those)
- Controlled penetrations for water dumps **only behind rear axle**
- Light-weight materials; eco-minded where practical
- Fill the **⅜" OEM floor valleys** so the hemp cap sits flat on the rib tops

### Should

- Removable access where service is needed without violating keep-out
- Clear keep-out markings in build docs / templates

### Could

-

## Design notes

- Height stack competes with insulation — coordinate with [insulation](../insulation/README.md) and [walls-ceiling](../walls-ceiling/README.md)
- Layout: [layout architecture](../../02-architecture/layout.md)
- Floor plan / metal-floor images (no bead dimensions): Featherbuilt Sprinter 170 Planning Kit at `~/Documents/Van Go Project/Featherbuilt Sprinter 170 Planning Kit.pdf` (paid / copyrighted; not in git)

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | Battery-zone floor keep-out + tie-down-only mounts | HV safety | Drill-anywhere ICE van habits | decided |
| 2026-11-02 | Subfloor is **⅛" aluminum sheet**, floated on adhesive for stability | A wood subfloor is too heavy; aluminum stiffens the soft hemp | ¼–½" poplar plywood | decided |
| 2026-11-02 | **Seal the PlantPanel** before it is closed in | The hemp board takes on water | Leaving the board raw | decided |
| 2026-11-02 | Glue lines are a **zero-VOC** adhesive (no off-gas in the closed van) | Cabin air | A conventional construction adhesive | decided |
| 2026-11-02 | Fill the **⅜" floor valleys with ⅜" cork**, then a flat **¾" PlantPanel I** cap | Cork is stock at ⅜"; PlantPanel I is the stock interior board; hemp strips and CNC pockets are unreliable | CNC carve pockets in 1" hemp; rip ⅜" strips from 2" PlantPanel X; 1" PlantPanel X (not stock) | decided |

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Valley fill | Manton Cork, ⅜" facing-grade sheet | | Matches the OEM bead height | preferred | [products](products.md) |
| Insulation (flat cap) | Hempitecture PlantPanel I, ¾" | | Stock board; sealed; glued over cork + ribs | preferred | [products](products.md) |
| Hemp sealer | Smart BioHemp Wood Protectant | | Board is susceptible if it gets wet | preferred | [products](products.md) |
| Subfloor (stability) | Aluminum sheet, ⅛" | | Floated on adhesive; wood is too heavy | preferred | [products](products.md) |
| Adhesive | AFM Safecoat Almighty Adhesive | | Zero-VOC glue for cork, hemp, and aluminum | preferred | [products](products.md) |
| Finish floor | Engineered bamboo ~7 mm waterproof click-lock (e.g. AquaGuard) | | Looks + protection | preferred | [products](products.md) |

Full list: [products.md](products.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Van platform | Battery map, tie-down grid, measured valley segments |
| Layout | Where cabinets land on tie-downs |

| Depended on by | Why |
|----------------|-----|
| Almost every interior feature | Mounting + height |

## Risks & open questions

- Exact tie-down pattern on target used vans
- Floor stack above the rib tops is ~**1.15"** (¾" hemp + ⅛" aluminum + ~7 mm bamboo) — how much ceiling may consume of the remaining ~5" budget
- Valley lengths are not published. Cargo bed is ~**173–174"** on the 170", but beads stop at tie-downs, joints, and wheelhouses. Measure and cut cork in segments
- Whether the sealer blocks the adhesive. Seal cut edges and any face that can see water; confirm glue faces still bond
- Adhesive on the OEM floor coating, cork, hemp, and aluminum (sample all joints)
- Alloy and temper of the ⅛" sheet, and how the sheets join over the battery keep-out without screws into the van floor
- Confirm with Manton that the facing-grade ⅜" sheet is the 10–14 lb/ft³ composition cork on their data sheet

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md)
- Featherbuilt Sprinter 170 Planning Kit — `~/Documents/Van Go Project/Featherbuilt Sprinter 170 Planning Kit.pdf` (paid / copyrighted; not in git). Floor / layout images; no bead dimensions
- [Supplemental BEG for eSprinter (Edition 2023-8)](https://www.mbvans.com/content/dam/mb-vans/us/upfitter/08302023_eSprinter_907_BEG_Edition2023-8_en.pdf) — official mbvans.com copy (copyrighted; link only). See [van references](../../01-van/references/README.md)
