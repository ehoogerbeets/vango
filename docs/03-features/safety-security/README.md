# Feature: Safety & Security

> Status: `researching`  
> Priority: `P1`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-25

## Summary

First trip carries a **fire extinguisher** and nothing else from this list. Smoke and CO detectors, cameras, a safe, and magnetic cabinet locks stay off the van until a later trip.

## Goals

- A reachable extinguisher on the shakedown trip
- Leave mounts and habits that do not depend on cameras or a safe

## Non-goals

- A camera or alarm system for v1
- Stealth hardware. City nights are quiet and blacked out, and the van may look like a camper ([constraints](../../00-overview/constraints.md))

## Requirements

### Must

- **Fire extinguisher** mounted where either person can reach it, including from the bed path
- Secured for highway travel

### Should

- Mount location that stays clear of the aisle and the settee guest

### Could

- Smoke detector
- CO detector
- Hotel-style safe, permanently attached
- Security cameras and motion detectors
- Magnetic cabinet locks for driving

## Design notes

The extinguisher is the only safety item in the [MVP list](../../01-van/requirements.md). The could-list matches the old nice-to-haves and is not scheduled.

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-25 | First trip: **fire extinguisher only** | The one safety item chosen for the shakedown | Smoke, CO, cameras, safe, and cabinet locks on trip one | decided |

Detail write-ups: [decisions.md](decisions.md) · cross-cutting: [ADRs](../../05-decisions/README.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Fire extinguisher | | | First trip | researching | [products](products.md) |

Full list: [products.md](products.md) · master BOM: [../../06-shopping/bom.md](../../06-shopping/bom.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Layout | A mount that is reachable and out of the aisle |

| Depended on by | Why |
|----------------|-----|
| MVP requirements | First-trip safety item |

## Risks & open questions

- Extinguisher class (galley electrical fire vs ordinary combustibles) and size vs a tight mount
- Whether smoke and CO move up before any winter or hookup trip

## Stories (future Jira)

See [stories.md](stories.md). Keep these outcome-oriented so they convert cleanly later.

## References

- [Requirements](../../01-van/requirements.md)
