# Van & Conversion Requirements

> Status: `researching`  
> Last updated: 2026-10-14

Platform is locked ([ADR-0002](../05-decisions/0002-mercedes-e-sprinter-platform.md)). This doc defines what the **MVP conversion** must deliver for a first usable trip, optional post-MVP adds, plus platform capacity targets.

## MVP must-haves

Minimum for a shakedown / first real trip. Features that are awkward or unused should still be omitted per [vision](../00-overview/vision.md) — but nothing below is optional for MVP.

| Capability | Notes | Feature |
|------------|-------|---------|
| Bed | Comfortable sleep for two | [bed-sleep](../03-features/bed-sleep/README.md) |
| Electrical system | House batteries; lights; cooktop; fridge/freezer; shore power; AC / 12V / USB outlets | [electrical-system](../03-features/electrical-system/README.md), [galley](../03-features/galley/README.md) |
| Cold water system | Fresh, grey, and black tanks + plumbing | [plumbing](../03-features/plumbing/README.md) |
| Flush toilet | In bathroom area | [bathroom](../03-features/bathroom/README.md) |
| Kitchen sink + faucet | Cold water at MVP | [galley](../03-features/galley/README.md), [plumbing](../03-features/plumbing/README.md) |
| Settee | Seating for living / dining | layout / interior |
| Table | Eating and working | layout / galley |
| Storage cabinets | Food, clothes, sundries | [storage](../03-features/storage/README.md) |
| Countertop | Food prep surface | [galley](../03-features/galley/README.md) |
| Windows | Daylight and views | [windows-ventilation](../03-features/windows-ventilation/README.md) |

## Nice-to-haves (post-MVP)

Optional — add only if we see the need. Payload, complexity, and “ultra-convenient or omit” still apply. Some items already appear in architecture notes as design intent; they remain **non-MVP** until promoted.

### Climate & ventilation

| Item | Notes |
|------|-------|
| 12/48V heat pump | Cabin heat/cool on house bus |
| Low-profile roof fan | Under roof rack for ventilation |
| Bathroom exhaust fan | Clear odor; vent shower moisture |
| Bug screens (side slider + rear doors) | Leave doors open without bugs |
| Outdoor “patio” lights | Outside sliding door |
| Forward-facing flood lights | Night driving |

### Electrical, solar & charging

| Item | Notes |
|------|-------|
| Roof rack + solar PV | Roof-mounted panels |
| Deployable ground solar | External plug + dedicated MPPT |
| External J1772 for house batteries | Shore / EVSE-style input to house pack |
| 240V Level 2 charger | Plug routed to front for Mercedes J1772 traction port |
| GFCI socket on van side | Exterior convenience outlet |
| Air pump | Van tires, e-bike tires, inflatable toys |
| Raspberry Pi central brain | Control hub; run OpenVan |
| iPad | OpenVan app display / control |

### Water

| Item | Notes |
|------|-------|
| Hot/warm water tank | Stored warm water |
| Instant electric water heaters | Point-of-use / boost |
| Shower area | Wet-bath capability |
| Electric ball valves | Grey + black dump |
| Tank sensors | Fresh, grey, black |
| Water leak detectors | |
| Reverse osmosis (grey → fresh) | Recovery filter — high complexity; promote only with strong need |

### Galley & living

| Item | Notes |
|------|-------|
| Microwave | |
| Toaster oven / air-fryer | |
| Minibar | |
| Garbage + recycling pails | |
| Mirror | Dressing, shaving, make-up |
| Bed raise/lower jacks | |
| External monitor | For laptops |
| Cabin / cab screen or door | Close cabin off from passenger area |
| Blackout window coverings | Insulation + sleep darkening |

### Exterior & chassis

| Item | Notes |
|------|-------|
| Spare tire rack | Back door |
| Utility box | Back door |
| Electric-extending awning | Side of van |
| Trailer hitch | Aftermarket |
| Electric fold-out step | Under sliding door |
| Winch | Front bumper |
| 4-point leveling jacks | |

### Windows & glazing

| Item | Notes |
|------|-------|
| Greenfilm USA G-Cling static tint | Preferred eco cling option — see [windows products](../03-features/windows-ventilation/products.md) |
| Ceramic coating (in + out) | Less effective than dedicated film; e.g. Migliore Strata, Cerakote glass coat — OK on windshield |
| Adhesive PDLC smart tint | Cabin acrylic only (not front); confirm acrylic compatibility |

## Material preferences (eco)

Preferred stack / products — not locked until install. Detail in feature `products.md`.

### Floor stack

| Layer | Role | Preferred material |
|-------|------|--------------------|
| 1 | Insulation | **1" PlantPanel X** (Hempitecture), glued to van floor |
| 2 | Stability / light / sustainable | **½" or ¼" poplar plywood**, glued to insulation |
| 3 | Finish / protection | **~7 mm** waterproof click-lock engineered bamboo (e.g. AquaGuard Carbonized Stranded) |

Height note: ~1.5–1.8" of the ~5" standing-height budget (floor + ceiling + clearance).

### Cabin windows

| Item | Preferred | Notes |
|------|-----------|-------|
| Window unit | **Arctic Tern Overland** classic double-pane acrylic | [ternoverland.com/classic-windows](https://ternoverland.com/classic-windows/) |
| Tint (preferred) | **Greenfilm USA G-Cling 70** static cling | [product](https://greenfilmusa.com/products/g-cling-70-static-cling-window-tint) |
| Tint (alt) | Ceramic coat in/out | Migliore Strata or Cerakote glass protectant |
| Smart film | Self-adhesive PDLC (research) | [Intelligent Glass](https://intelligentglass.net/products/self-adhesive-switchable-smart-film/) — verify on acrylic |

### Connectivity

| Item | Notes |
|------|-------|
| Starlink | |
| weBoost | Cellular booster |
| Mesh Wi‑Fi | |

### Safety & security

| Item | Notes |
|------|-------|
| Security cameras + motion detectors | |
| Smoke / CO detectors | Strong candidate to promote early |
| Hotel-style safe | Permanently attached; laptops etc. |
| Magnetic cabinet locks | Stay locked while driving |

## Deal-breakers

- Pop-top or aftermarket raised roof
- Propane / fossil house systems ([ADR-0003](../05-decisions/0003-all-electric-house-systems.md))
- Mid-van floor drilling over traction battery ([ADR-0005](../05-decisions/0005-traction-battery-floor-no-drill-zone.md))

## Dimensions & capacity targets

| Attribute | Target | Hard max/min? |
|-----------|--------|---------------|
| Exterior length | e-Sprinter 170" WB cargo | Platform |
| Exterior height | Factory high roof | Hard — no roof raise |
| Interior standing height | Full upright for **6'2"** (~5" build stack from 6'7" raw) | Hard |
| Wheelbase | **170"** | Decision |
| Payload | **2,624 lb** (Mercedes site; confirm sticker) | Hard budget |
| Fuel type | Battery electric (traction) | Hard |
| House energy | All-electric, **48V** house DC | Hard — ADR-0003 / 0004 |
| Drivetrain (2WD/AWD/4WD) | As available on chosen used unit | Soft |

## Related

- [Candidates](candidates.md)
- [Selection](selection.md)
- [Specs](specs.md)
- [Constraints](../00-overview/constraints.md)
- [Features index](../03-features/README.md)
- [Floor products](../03-features/floor-subfloor/products.md)
- [Windows products](../03-features/windows-ventilation/products.md)
