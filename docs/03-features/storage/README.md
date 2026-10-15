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

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | No classic rear garage as primary storage | Aft reserved for wet + tanks | Garage + bed-over | decided |

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

- Where bulky items (e-bikes?) go without a rear garage

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md)
