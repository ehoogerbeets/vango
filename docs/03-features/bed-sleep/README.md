# Feature: Bed / Sleep

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-13

## Summary

Comfortable bed for two, with the tall sleeper (6'2") fully accommodated. Per [ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md) / [layout](../../02-architecture/layout.md), the bed sits **more forward** — not the classic rear-garage loft.

## Goals

- “Really comfortable bed” success criterion from vision
- Length/width for 6'2" + partner
- Integrate with multi-use daytime space if needed
- Mount legally on battery-zone floor (**OEM tie-downs**) or other allowed structure

## Non-goals

- Primary bed over a rear cargo garage (rejected for this platform)

## Requirements

### Must

- Sleeping length suitable for 6'2"
- Forward placement relative to aft wet core (shower/galley)
- Floor attaches in mid-van only via **tie-downs** (or non-floor structure)

### Should

- Easy make/break if it converts to lounge
- Light-weight platform/mattress system

### Could

-

## Design notes

- Losing rear garage means storage design must compensate ([storage](../storage/README.md))

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | Bed forward; not over rear garage | Wet aft / tank penetrations aft of axle | Classic garage bed | decided |

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Mattress | | | comfort + light | researching | |

Full list: [products.md](products.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Layout | Zone placement |
| Floor | Tie-down landing |

| Depended on by | Why |
|----------------|-----|
| Storage | Under/around bed volume |

## Risks & open questions

- Exact bed orientation (east-west vs north-south) vs aisle and standing room

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md)
