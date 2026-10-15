# Chosen Van Specs

Platform decision: [ADR-0002](../05-decisions/0002-mercedes-e-sprinter-platform.md). Prefer measured / window-sticker values at purchase.

| Spec | Value | Source |
|------|-------|--------|
| Make / model | Mercedes e-Sprinter **cargo** | Decision |
| Year / VIN | TBD at purchase (~1.5–2 yr) | |
| Wheelbase | **170"** | Decision |
| Roof | Factory **high roof** | Decision |
| Drive motor | **201 HP** | Decision |
| Traction battery | **113 kWh** | Decision |
| Est. range | **~249 mi** | Planning comparison |
| DC fast charge | **~115 kW** max class | Planning comparison |
| Home charge | Level 2 **11.5 kW** (already owned) | Decision |
| Cargo volume | **~488 cu ft** | Planning comparison |
| Payload (113 kWh) | **2,624 lb** | Mercedes site — *load budget, not GVWR*; confirm sticker |
| Payload (class figure) | ~3,516 lb cited in broader comparisons | Other configs |
| GVWR | **9,370 lb** | Mercedes site (confirm sticker) |
| GCWR | **11,023 lb** | Mercedes site |
| Max towing | **5,000 lb** | Mercedes site; also limited by GCWR − vehicle weight |
| Curb / empty van (derived) | **~6,746 lb** | GVWR − payload; confirm sticker |
| Raw interior standing height | **6'7"** before floor/ceiling | Planning |
| Height budget after 6'2" person | **~5"** for floor + ceiling + overhead clearance | Derived |
| Factory windows | Typically **none** (cargo) | Decision — we add |
| Factory tow package | **No** — aftermarket later | Decision |
| Traction battery under-floor span | **B-pillar → rear axle** | [ADR-0005](../05-decisions/0005-traction-battery-floor-no-drill-zone.md) |
| Floor drill in battery span | **No** (tie-downs / tiny OEM spots only) | Drill underside→up if ever near pack |
| Under-mount tank zone | **Behind rear axle only** | ADR-0005 |
| OEM cargo tie-downs | Map at purchase — cabinetry attach grid | Mid-van floor mounts |

## Standing-height stack (design budget)

```mermaid
flowchart TD
  raw["6'7\" raw interior"] --> minus["minus 6'2\" occupant"]
  minus --> budget["5\" budget: floor + ceiling + overhead clearance"]
```

Track actual material thicknesses in floor / insulation / ceiling feature docs.

## Photos & diagrams

<!-- Link or drop files under docs/01-van/assets/ later. -->

-
