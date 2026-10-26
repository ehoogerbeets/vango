# Feature: Storage & Organization

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-13

## Summary

Gear storage without relying on a classic **rear garage** (aft is wet core + under-mount tanks). Must still carry weekender through multi-month trip kit, including possible e-bike/hiking gear — just not in the usual rear cave.

## Goals

- Replace rear-garage capacity with other volumes (under-bed forward, wall, galley, exterior, etc.)
- Multi-use bathroom storage that swings clear (vision)
- Light-weight organizers; attach mid-van via **OEM tie-downs** where floor-mounted

## Non-goals

- Primary rear garage under a platform bed (incompatible with ADR-0005 layout)

## Requirements

### Must

- Storage plan that works with **wet aft / sleep forward** ([layout](../../02-architecture/layout.md))
- No drilling battery-zone floor for mounts — tie-downs or walls/ceiling structure

### Should

- Convenient access for high-frequency items
- Secure for highway travel

### Could

- Exterior boxes (weight/aero trade)

## Design notes

- Bathroom multi-use drawers are part of this story ([bathroom](../bathroom/README.md))
- **Clothes in the van:** driver’s side, at the **front of the cabinet run aft of the settee**, a narrow closet **only shirt-and-jacket height**, about **4–6 hangers**. **80–90%** of clothing is in drawers. Bulk overflow rides on the trailer
- **Van carries about a week.** Short trips put bikes on a hitch rack ([exterior](../exterior/README.md)). Longer trips tow a small trailer so bikes, camp kit, extra water, and extra energy stay out of the van’s payload.

### Trailer kit (direction, 2026-10-25)

The trailer has its own electrical system. It can feed **excess charge into the van** through a DC-DC converter and a dedicated socket on the van wall. It is not required for a week in the van.

| On the trailer | Role |
|----------------|------|
| 2 e-bike spots | Long-trip bike storage |
| A few kWh of batteries | Trailer loads and a surplus to send to the van |
| Deployable solar | Trailer array, not the van roof |
| MPPT, small inverter/charger, charging hardware | Trailer house system |
| DC-DC feed + van-wall socket | Surplus energy into the van’s 48V bank |
| Toolbox | Repairs on long trips |
| Solo stove | Outdoor cooking |
| Firewood, small axe, shovel, handheld electric chainsaw | Campfire kit |
| Extra fresh tank | **~15 gal**, extends the van’s 3-day supply |
| Reverse osmosis | **Grey → fresh first** (also frees grey-tank room), then river/lake. Seawater can be cut |
| Deployable parabolic solar water heater + hoses | Connects to the van warm-tank socket |
| Food, clothes, and bulk storage | Long-trip overflow |

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | No classic rear garage as primary storage | Aft reserved for wet + tanks | Garage + bed-over | decided |
| 2026-10-25 | Long trips use a **trailer**; the van stays a week-capable vehicle | Bikes, extra water, RO, solar, and camp kit are heavy and occasional | Rear garage; carrying the long-trip kit in the van | decided |

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| | | | | researching | |

Full list: [products.md](products.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Layout / bed / galley / bathroom | Volume owners |

| Depended on by | Why |
|----------------|-----|
| Trip use cases | Pack-out success |

## Risks & open questions

- Trailer weight vs e-Sprinter tow rating (5,000 lb) and GCWR (11,023 lb), tongue weight on the hitch, and the range cost of towing
- Trailer battery voltage and the van-wall socket (match the 48V house bank)
- Reverse osmosis on grey water vs seawater are different machines and different energy loads
- Which week-trip items must remain in the van when the trailer stays home

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md)
