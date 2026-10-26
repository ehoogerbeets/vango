# Van & Conversion Requirements

> Status: `researching`  
> Last updated: 2026-10-25

Platform is locked ([ADR-0002](../05-decisions/0002-mercedes-e-sprinter-platform.md)). This doc defines what the **MVP conversion** must deliver for a first usable trip, optional post-MVP adds, plus platform capacity targets.

## MVP must-haves

Minimum for a shakedown / first real trip. Features that are awkward or unused should still be omitted per [vision](../00-overview/vision.md) — but nothing below is optional for MVP.

| Capability | Notes | Feature |
|------------|-------|---------|
| Bed | Comfortable sleep for two; **push-button elevator** raises to ceiling by day, **settles on settee / chair backs** at night | [bed-sleep](../03-features/bed-sleep/README.md) |
| Electrical system | House batteries; lights; cooktop; fridge/freezer; shore power; AC / 12V / USB outlets | [electrical-system](../03-features/electrical-system/README.md), [galley](../03-features/galley/README.md) |
| Cold water system | Fresh, grey, and black tanks + plumbing | [plumbing](../03-features/plumbing/README.md) |
| Flush toilet | In bathroom area | [bathroom](../03-features/bathroom/README.md) |
| Kitchen sink + faucet | Cold water at MVP. Indoor shower and hot water wait | [galley](../03-features/galley/README.md), [plumbing](../03-features/plumbing/README.md) |
| Settee | Seating for living / dining | layout / interior |
| Table | Eating and working | layout / galley |
| Storage cabinets | Food, clothes, sundries | [storage](../03-features/storage/README.md) |
| Countertop | Food prep surface | [galley](../03-features/galley/README.md) |
| Windows | Daylight and views | [windows-ventilation](../03-features/windows-ventilation/README.md) |
| Trailer hitch | Aftermarket. Short trips carry bikes on a hitch rack. Longer trips tow a gear trailer | [exterior](../03-features/exterior/README.md), [storage](../03-features/storage/README.md) |
| Fire extinguisher | First-trip safety item. Smoke, CO, cameras, a safe, and cabinet locks wait | [safety-security](../03-features/safety-security/README.md) |

## Nice-to-haves (post-MVP)

Optional — add only if we see the need. Payload, complexity, and “ultra-convenient or omit” still apply. Some items already appear in architecture notes as design intent; they remain **non-MVP** until promoted.

### Climate & ventilation

| Item | Notes |
|------|-------|
| 12/48V heat pump | Cabin heat/cool on house bus. **Not installed for the first trip** (fair weather; factory cab HVAC only). Still pick the unit, reserve its roof opening, and **size the house battery as if it is installed** |
| Low-profile roof fan | Under roof rack for ventilation |
| Bathroom exhaust fan | Clear odor; vent shower moisture |
| Bug screens (side slider + rear doors) | Leave doors open without bugs |
| Outdoor “patio” lights | Outside sliding door |
| Forward-facing flood lights | Night driving |

### Electrical, solar & charging

| Item | Notes |
|------|-------|
| Roof rack + solar PV | **As much roof PV as the heat-pump opening leaves.** Goal: replace a moderate-use day. **Hood solar too**, if it survives hood heat and the wipers. Shore power covers the rest |
| Deployable ground solar | External plug + dedicated MPPT |
| External J1772 | One exterior **J1772** into the **house** battery (home EVSE or a campsite). Traction keeps the factory front port |
| 240V Level 2 charger | **50A shore socket** on the van (120/240V). A 30A pedestal plugs in through an adapter. Traction J1772 port stays at the front of the Mercedes |
| GFCI socket on van side | Exterior convenience outlet |
| Air pump | Van tires, e-bike tires, inflatable toys |
| Raspberry Pi central brain | Control hub; run OpenVan |
| iPad | OpenVan app display / control |

### Water

| Item | Notes |
|------|-------|
| Hot/warm water tank | Stored warm water |
| Instant electric water heaters | Point-of-use / boost |
| Deployable solar thermal collector | Lives on the **trailer**: deployable frame, flexible mirror formed into a parabola, black pipe at the focal line. Hoses to the van’s warm-tank socket |
| Side quick-connect for solar thermal | External port on van side; routed to warm/hot water heater |
| Shower area | Wet-bath capability. End-state habit is a **navy shower** in the van plus real showers at campgrounds. First trip has toilet + cold sink only |
| Electric ball valves | Grey + black dump |
| Tank sensors | Fresh, grey, black |
| Water leak detectors | |
| Reverse osmosis (grey → fresh) | On the **trailer**. Priority: **grey → fresh** (recovers water and frees grey-tank room), then river/lake. Seawater is optional and can be cut. The van’s own grey tank still holds a trailer-less 3 days |

### Galley & living

| Item | Notes |
|------|-------|
| Microwave | |
| Toaster oven / air-fryer | |
| Minibar | |
| Garbage + recycling pails | |
| Mirror | Dressing, shaving, make-up |
| External monitor | For laptops |
| Cabin / cab screen or door | Close the cab while driving and at night so factory HVAC and the heat pump each serve their own volume. Also blocks sightlines |
| Blackout window coverings | Insulation + sleep darkening |

### Exterior & chassis

| Item | Notes |
|------|-------|
| Spare tire rack | Back door |
| Utility box | Back door |
| Electric-extending awning | Side of van |
| Trailer hitch | Promoted to MVP — see must-haves. Bike rack candidate: **QuikrStuff Mach 2** |
| Electric fold-out step | Under sliding door |
| Winch + front bumper | **Shop install.** In the build, not a first-trip must. See [constraints](../00-overview/constraints.md) |
| Shocks upgrade | **Shop.** Spec still open |
| Exterior paint | **Shop.** Color waits on the shared interior/exterior palette |
| 4-point leveling jacks | |

### Windows & glazing

| Item | Notes |
|------|-------|
| Greenfilm USA G-Cling static tint | Preferred eco cling option — see [windows products](../03-features/windows-ventilation/products.md) |
| Ceramic coating (in + out) | Less effective than dedicated film; e.g. Migliore Strata, Cerakote glass coat — OK on windshield |
| Adhesive PDLC smart tint | Cabin acrylic only (not front); confirm acrylic compatibility |

### Connectivity

| Item | Notes |
|------|-------|
| Starlink | |
| weBoost | Cellular booster |
| Mesh Wi‑Fi | |
| External weather station | Temp, pressure, wind, humidity |
| RuuviTag Pro (interior) | Internal temp, humidity, pressure — BLE sensors |

### Safety & security

| Item | Notes |
|------|-------|
| Security cameras + motion detectors | |
| Smoke / CO detectors | Not on the first trip. Extinguisher is the MVP safety item |
| Hotel-style safe | Permanently attached; laptops etc. |
| Magnetic cabinet locks | Stay locked while driving |

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
