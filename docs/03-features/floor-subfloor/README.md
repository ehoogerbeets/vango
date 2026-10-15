# Feature: Floor & Subfloor

> Status: `researching`  
> Priority: `P1`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-14

## Summary

Finished floor and subfloor stack under the standing-height budget (~5" shared with ceiling), with a hard **traction-battery keep-out**: no drilling/mounting through the floor from B-pillar to rear axle except **OEM tie-downs** ([ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md)).

**Preferred eco stack:** 1" Hempitecture PlantPanel X → ¼–½" poplar plywood → ~7 mm waterproof engineered bamboo (click-lock). See [products.md](products.md).

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

### Should

- Removable access where service is needed without violating keep-out
- Clear keep-out markings in build docs / templates

### Could

-

## Design notes

- Height stack competes with insulation — coordinate with [insulation](../insulation/README.md) and [walls-ceiling](../walls-ceiling/README.md)
- Layout: [layout architecture](../../02-architecture/layout.md)

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | Battery-zone floor keep-out + tie-down-only mounts | HV safety | Drill-anywhere ICE van habits | decided |

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Insulation (layer 1) | Hempitecture PlantPanel X, 1" | | Plant-based; glued to floor | preferred | [products](products.md) |
| Subfloor (layer 2) | Poplar plywood ¼–½" | | Light + stiff + sustainable | preferred | [products](products.md) |
| Finish floor (layer 3) | Engineered bamboo ~7 mm waterproof click-lock (e.g. AquaGuard) | | Looks + protection | preferred | [products](products.md) |

Full list: [products.md](products.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Van platform | Battery map, tie-down grid |
| Layout | Where cabinets land on tie-downs |

| Depended on by | Why |
|----------------|-----|
| Almost every interior feature | Mounting + height |

## Risks & open questions

- Exact tie-down pattern on target used vans
- Floor stack already ~**1.5–1.8"** — how much ceiling may consume of the remaining ~5" budget
- ¼" vs ½" poplar: stiffness vs height
- Adhesive compatibility: PlantPanel ↔ OEM floor ↔ poplar

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md)
