# Feature: Windows & Ventilation

> Status: `researching`  
> Priority: `P0`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-14

## Summary

Add cabin glazing for daylight and views (MVP), plus optional tint / smart film / bug screens for comfort. Cargo shell has no factory windows — we cut in aftermarket units.

## Goals

- Daylight and views without compromising standing-height / eco / weight goals
- Thermal control via insulated windows + film/coating options
- Optional: doors open with bug screens; privacy via PDLC

## Non-goals

- Factory glass in cargo sides (we add aftermarket)
- PDLC / heavy film on windshield / cab (ceramic coat path instead)

## Requirements

### Must (MVP)

- Cabin windows for daylight and views

### Should

- Double-pane / insulated units to reduce HVAC load
- Light weight vs glass where practical

### Could (post-MVP)

- Bug screens on side slider + rear doors
- Greenfilm static cling tint
- Ceramic coating (in/out), including windshield
- Adhesive PDLC on cabin acrylic only
- Blackout coverings (see [requirements](../../01-van/requirements.md))
- Roof fan (under rack)

## Design notes

- Preferred unit: **Arctic Tern Overland** classic double-pane acrylic — [products.md](products.md)
- Tint preference: Greenfilm G-Cling 70; ceramic as alternate; PDLC needs acrylic compatibility check
- Roof real estate shared with PV, thermal, fans — [exterior](../exterior/README.md)

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-14 | Prefer Arctic Tern Overland double-pane acrylic | Light + insulated acrylic for cabin | Glass RV windows (heavier) | proposed |

Detail write-ups: [decisions.md](decisions.md) · cross-cutting: [ADRs](../../05-decisions/README.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Cabin windows | Arctic Tern Overland classic double-pane acrylic | | Light, insulated | preferred | [products](products.md) |
| Cling tint | Greenfilm USA G-Cling 70 | | Eco cling | preferred | [products](products.md) |
| Ceramic coat | Migliore Strata / Cerakote | | In+out; windshield OK | researching | [products](products.md) |
| Smart film | Intelligent Glass PDLC (candidate) | | Cabin acrylic only | researching | [products](products.md) |

Full list: [products.md](products.md) · master BOM: [../../06-shopping/bom.md](../../06-shopping/bom.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Layout | Cut locations vs furniture / wet core |
| Insulation / climate | Thermal budget |

| Depended on by | Why |
|----------------|-----|
| Interior finish | Trim, blackout, privacy |
| Heating & cooling | Solar gain / loss |

## Risks & open questions

- Arctic Tern cut templates vs e-Sprinter skin / ribs
- Cling / PDLC warranty and adhesion on acrylic
- Bug-screen mounting that stays convenient (vision #3)

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [Requirements — material preferences](../../01-van/requirements.md#material-preferences-eco)
- https://ternoverland.com/classic-windows/
