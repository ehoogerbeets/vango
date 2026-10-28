# Feature: Windows & Ventilation

> Status: `researching`  
> Priority: `P1`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-28

## Summary

Cabin glazing is its own project. It completes the van, and it sits at the top of that list, after the first trip. Cargo shell has no factory windows — we cut in aftermarket units. The **MaxxAir MaxxFan Mini Plus** is the roof vent that finishes with the climate / solar canopy stack. Tint, smart film, and extra bug screens stay aspirational.

## Goals

- Daylight and views without compromising standing-height / eco / weight goals
- Thermal control via insulated windows + film/coating options
- Optional: doors open with bug screens; privacy via PDLC

## Non-goals

- Factory glass in cargo sides (we add aftermarket)
- PDLC / heavy film on windshield / cab (ceramic coat path instead)

## Requirements

### Must

- Cabin windows for daylight and views. This project completes the van; it is not on the first trip ([requirements](../../01-van/requirements.md))
- **MaxxAir MaxxFan Mini Plus** (00-03801 class) in a second **14" × 14"** roof cutout. Completes the van with the heat-pump / solar canopy work

### Should

- Double-pane / insulated units to reduce HVAC load
- Light weight vs glass where practical

### Could (post-MVP)

- Bug screens on side slider + rear doors
- Greenfilm static cling tint
- Ceramic coating (in/out), including windshield
- Adhesive PDLC on cabin acrylic only

## Design notes

- Preferred unit: **Arctic Tern** dual-pane acrylic awning window, Classic or Flat — [products.md](products.md). Includes propped openings, an integral bug screen, and an integral blackout shade with a reflective face.
- Cling tint, a ceramic coat, and PDLC are aspirational. Confirm any of them with Tern before they touch the acrylic. Their notes treat the pane as not a film-tint product.
- Cuts from the floor plan ([layout](../../02-architecture/layout.md)): driver’s wall **behind the long settee**; one **in the sliding door**; passenger wall **behind the induction cooktop** (also the cook vent); **passenger rear door**. Optional extra on the driver’s wall **forward of the toilet**, cabinets around it. The driver’s rear door is not called out. The sash screen does not cover a fully open sliding door.
- City nights need **blackout and quiet**, and the van may still look like a camper. The Tern integral blackout shade is the cabin darkening. No stealth exterior.
- **MaxxFan Mini Plus:** fixed, stationary exterior rain shroud at **4.1"** (open or closed). Motorized louvers handle exhaust without the dome rising. Align rack crossbars so the rear horizontal exhaust louvers stay wide open. Lives under the solar canopy with about **5.4–5.9"** of plenum above the dome ([climate](../../02-architecture/climate.md), [exterior](../exterior/README.md)).

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-14 | Prefer Arctic Tern Overland double-pane acrylic | Light + insulated acrylic for cabin | Glass RV windows (heavier) | proposed |
| 2026-10-27 | Windows are their own project and **complete the van**, high on that list | Daylight is wanted, and the cuts should not be tangled with the first-trip galley | Windows on the first trip; windows folded into the galley build | decided |
| 2026-10-28 | Roof fan is the **MaxxAir MaxxFan Mini Plus**, and it completes the van | Fixed **4.1"** shroud fits under the solar canopy; no rising lid into the panels | Leaving the roof fan aspirational; a rising-lid MaxxFan Deluxe under the canopy | decided |

Detail write-ups: [decisions.md](decisions.md) · cross-cutting: [ADRs](../../05-decisions/README.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Cabin windows | Arctic Tern Overland classic double-pane acrylic | | Light, insulated | preferred | [products](products.md) |
| Roof fan | MaxxAir MaxxFan Mini Plus (00-03801) | | Fixed 4.1" shroud under the canopy | preferred | [products](products.md) |
| Cling tint | Greenfilm USA G-Cling 70 | | Eco cling, if tint is ever added | aspirational | [products](products.md) |
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
