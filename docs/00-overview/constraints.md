# Constraints

> Status: `researching`  
> Last updated: 2026-10-13

Hard limits that every feature and purchase decision must respect. Soft / aspirational items stay in [vision](vision.md).

## Budget

| Category | Cap / target | Notes |
|----------|--------------|-------|
| Base vehicle | **~$42K–$47K** used target | New ~$70–80K; see [ADR-0002](../05-decisions/0002-mercedes-e-sprinter-platform.md) |
| Conversion total | TBD | Light-weight + all-electric stack |
| Contingency % | TBD | |
| Annual operating | TBD | Traction + house charging energy |

## Timeline

| Milestone | Target | Notes |
|-----------|--------|-------|
| Planning complete | ongoing → retirement | Docs now; tickets later |
| Vehicle purchased | **~1.5–2 years** from 2026-10 | Used / fleet leftover target |
| Build start (retirement) | with / after purchase | |
| First trip | TBD | |

## Physical / vehicle

| Constraint | Value | Notes |
|------------|-------|-------|
| Base vehicle | **Mercedes e-Sprinter cargo** LWB 170", high roof, 201 HP, 113 kWh + DCFC | [ADR-0002](../05-decisions/0002-mercedes-e-sprinter-platform.md) |
| Vehicle budget (target) | **~$42K–$47K** used | New ~$70–80K rejected for now |
| Standing height | Full upright for **6'2"** | Raw bay **6'7"** → **~5"** for floor+ceiling+clearance |
| Roof type | Factory high-roof only | **No pop-top, no raised-roof conversion** |
| Payload budget | **~2,624 lb** with 113 kWh (confirm sticker) | Drives light-weight everything |
| House energy | **Electricity only** + separate house battery | [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) |
| House DC bus | **48V** | Heat pump + fridge/freezer — [ADR-0004](../05-decisions/0004-48v-house-dc-bus.md) |
| Traction→house power | **Not available** meaningfully | 12V tap cellphone-class only |
| Home charging | Level 2 **11.5 kW** (owned) | DCFC required for road trips |
| Tow package | Aftermarket later | Not factory |
| Max length / height / weight | e-Sprinter envelope | Exterior height still matters for garages, ferries, trees |
| Driveway / garage fit | TBD | |
| License / insurance class | TBD | |
| Electrical market (v1) | North America | Shore power / charging designed for NA first |
| Traction battery under floor | **B-pillar → rear axle** | [ADR-0005](../05-decisions/0005-traction-battery-floor-no-drill-zone.md) |
| Floor drill in battery zone | **Forbidden** (tiny OEM spots only; not for tanks/mounts) | If ever drilling near pack: **from underside upward** |
| Floor mounts in battery zone | **OEM tie-downs only** | Cabinetry/layout must hit those points |
| Under-mount tanks | **Behind rear axle only** | No tanks under battery span |
| Grey/black floor penetrations | **Behind rear axle only** | Drives wet core aft |
| Layout pattern | **Wet aft (shower + galley), bed forward** | Not classic rear-garage + bed-over-garage |
| Sliding-door under-mount step | Highly constrained | Possible thin notch only; research |

## Lifestyle

| Constraint | Value | Notes |
|------------|-------|-------|
| Occupants (typical / max) | 2 / TBD | Couple; sizes 6'2" and 5'2" |
| Climate / seasons | Mostly good-weather | Easy winterize; occasional winter trips |
| Off-grid nights target | ~3 nights without want | Longer trips mix ~¼–⅓ hookups |
| Stealth / urban camping | TBD | Some city nights expected |
| Pets | TBD | |
| Overseas use | Nice-to-have | Europe / AU / NZ do **not** drive v1 design |

## Skills & build approach

<!-- DIY vs pro shop, tools available, willingness to learn systems (electrical, plumbing, carpentry). -->

-

## Soft preferences (not hard constraints)

- Eco material stack for floor and window treatments — see [requirements — material preferences](../01-van/requirements.md#material-preferences-eco)


## Related

- [Vision](vision.md)
- [Budget rollup](../06-shopping/budget.md)
