# ADR-0002: Mercedes e-Sprinter as base vehicle

- **Date:** 2026-10-13
- **Status:** `accepted`
- **Deciders:** Edwin
- **Tags:** van, platform, electrical, weight, tall-person-fit

## Context

We need a factory high-roof cargo van that can become an “RV in a van” for two people, with full standing height for a 6'2" occupant (no pop-top, no raised-roof conversion). House systems will be all-electric ([ADR-0003](0003-all-electric-house-systems.md)). Purchase is planned for retirement in **~1.5–2 years**, likely from the **used / fleet-leftover** market where low-mile e-Sprinters are priced far below new MSRP.

## Decision

Buy a **Mercedes e-Sprinter cargo van** configured as:

| Attribute | Choice |
|-----------|--------|
| Body | **Cargo** (windowless from factory — we add windows as we choose) |
| Wheelbase | Long — **170"** |
| Roof | **High roof** (factory) |
| Drive motor | **201 HP** |
| Traction battery | **113 kWh** |
| DC fast charge | Yes — up to **~115 kW** (platform capability) |
| Tow package | **Not from factory** — aftermarket later (cost + brand choice) |
| Purchase timing | Retirement window, **~1.5–2 years** from 2026-10 |
| Purchase channel | Prefer **used / fleet leftovers** (~$42K–$47K observed) over new dealer (~$70K–$80K) |

Standing height plan: brochure/raw interior height **6'7"** before floor/ceiling. After 6'2" stature, **~5" total** remains for floor stack + ceiling stack + overhead clearance. Build stacks must fit that budget.

## Why

- **Reliability, space, aesthetics** — Mercedes preferred over the compared EV vans.
- **Used-market price** — fleet leftovers often near-new miles at roughly half of new MSRP; loss of federal new-EV incentive is more than offset by purchase price.
- **Range** — best among compared options at an estimated **249 miles**.
- **Battery size** — 113 kWh competitive with ProMaster EV and well above e-Transit.
- Factory high roof is the only path that matches the no-pop-top / no-raised-roof constraint while targeting 6'2" standing room (with careful floor/ceiling design).
- Cargo body: cheaper, more common, and we control window placement/count.
- Aftermarket tow later: lower upfront cost and freer brand selection.

## Alternatives considered

Comparison snapshot used for the decision (planning figures — re-verify at purchase time):

| Criterion | e-Sprinter | Ford e-Transit | Ram ProMaster EV | Winner |
|-----------|------------|----------------|------------------|--------|
| Reliability (our judgment) | Best | — | — | e-Sprinter |
| Space / packaging (our judgment) | Best | — | — | e-Sprinter |
| New price | Higher | Lower | — | e-Transit (new) |
| Used price (observed) | **~$42–47K** fleet leftovers | — | — | **e-Sprinter (used)** |
| Battery size | **113 kWh** | Significantly less | Competitive | e-Sprinter / ProMaster |
| Est. max range | **249 mi** | Lower | Lower | **e-Sprinter** |
| Max payload | **3,516 lb** class; **2,624 lb** with 113 kWh (Mercedes site; confirm sticker) | **4,201 lb** | **3,020 lb** | e-Transit |
| Peak HP | 201 | 266 | **268** | ProMaster |
| Max DC fast charge | ~115 kW | ~115 kW | **150 kW** | ProMaster |
| Cargo volume | 488 cu ft | 487 cu ft | **524 cu ft** | ProMaster |
| Aesthetics | Best | — | — | e-Sprinter |
| Accessories ecosystem | Strong | Strong | Distant third | e-Transit ≈ e-Sprinter |
| Ease of repair (NA) | Harder (dealers exist) | **Best** | Middle | e-Transit |
| Ease of repair (Europe) | Best | — | — | e-Sprinter |

### Alternative A — Ford e-Transit

- Pros: Lower new price; best NA repair ease; highest payload
- Cons: Smaller battery / less range; loses on reliability/space/esthetics judgment; used e-Sprinter undercuts on price in our shopping window
- Why not: Overall fit favors e-Sprinter for this project

### Alternative B — Ram ProMaster EV

- Pros: Highest peak HP and DCFC rate; largest cargo volume
- Cons: Accessories ecosystem weak; loses on reliability/esthetics preference; payload mid-pack
- Why not: Not the preferred platform

### Alternative C — Pop-top or raised-roof conversion

- Pros: Cheaper donor possible
- Cons: Explicitly rejected in vision/constraints
- Why not: Hard constraint — factory high roof only

### Alternative D — Buy new from dealer at $70–80K

- Pros: Full new-EV incentives / warranty simplicity possible
- Cons: Large premium vs low-mile used fleet units at $42–47K
- Why not: Used path preferred unless market changes at retirement

## Consequences

### Positive

- Platform locked for layout, window plan, electrical, and weight work
- Cargo shell → intentional glazing plan ([windows-ventilation](../03-features/windows-ventilation/README.md))
- Eco + EV travel story is coherent with [ADR-0003](0003-all-electric-house-systems.md)
- Home **Level 2 (11.5 kW)** already available; DCFC assumed for road trips

### Negative / trade-offs

- **Payload is tight** with the 113 kWh battery — light-weight build is mandatory ([weight & balance](../02-architecture/weight-and-balance.md))
- Standing height has only **~5"** for floor + ceiling + clearance — every millimeter of stack-up matters
- Under-floor pack creates **no-drill floor zone** and forces wet-aft layout — [ADR-0005](0005-traction-battery-floor-no-drill-zone.md)
- NA service network favors Ford; we accept Mercedes dealer dependency
- Lower peak HP and DCFC vs ProMaster EV — acceptable trade

### Follow-ups

- [ ] At purchase: lock year, VIN, window sticker GVWR / curb / **payload**, charge curves, warranty remaining
- [ ] Measure actual interior height of candidate vans (confirm 6'7")
- [ ] Set numeric floor and ceiling build-up budgets that preserve 6'2" standing + desired overhead clearance
- [ ] Map battery keep-out + OEM tie-down grid ([ADR-0005](0005-traction-battery-floor-no-drill-zone.md))
- [ ] Aftermarket tow package research (when needed)
- [ ] Window placement plan (cargo → camper)
- [ ] Track used-market pricing as retirement approaches

## Links

- Related features: layout, windows-ventilation, electrical-system, insulation, floor-subfloor, walls-ceiling, plumbing
- Related docs: [selection](../01-van/selection.md), [specs](../01-van/specs.md), [candidates](../01-van/candidates.md), [ADR-0003](0003-all-electric-house-systems.md), [ADR-0005](0005-traction-battery-floor-no-drill-zone.md)
- Supersedes: —
- Superseded by: —
