# Payload Budget & Balance

> Status: `researching`  
> Last updated: 2026-10-15

Running **payload** tracker for the e-Sprinter 113 kWh. Payload is tight — every heavy choice must earn its keep (vision: light weight). Platform: [ADR-0002](../05-decisions/0002-mercedes-e-sprinter-platform.md).

**Rule:** When a product is preferred or purchased, add/update its row here (and feature `products.md`). Definition of Done for build stories also requires this.

## Capacity envelope

| Item | Weight (lb) | Notes |
|------|-------------|-------|
| GVWR | **9,370** | Mercedes site (confirm sticker at purchase) |
| GCWR | **11,023** | Mercedes site |
| Max towing | **5,000** | Also limited by GCWR − actual vehicle weight |
| Curb / empty van (derived) | **~6,746** | GVWR − payload; confirm sticker |
| **Payload budget** | **2,624** | Build + fluids + people + cargo + gear |
| Broader class payload | ~3,516 | Other configs — **do not** plan against this |

```
Payload 2,624 lb
  ├─ Fixed build (cabinets, floor, electrical, windows, …)
  ├─ Semi-fixed fluids (fresh/grey/black — count FULL for worst case)
  ├─ People (typical trip)
  └─ Cargo / food / toys / margin
```

We must stay ≤ **2,624 lb** for the **worst realistic load** (full tanks + two people + trip gear), not just the empty conversion.

## Budget summary (roll-up)

Update totals when line items change.

| Bucket | Est. lb | Confidence | Notes |
|--------|---------|------------|-------|
| A. Fixed build (known line items) | **~139** | high | Furrion fridge only — see below |
| B. House battery (ceiling only) | **~240–300** | low | **12–15 kWh** if that ceiling holds. Size is not locked; the load inventory is still open |
| C. Fluids (tanks **full**) | **~584** | low | Fresh 292 + grey 217 + black 75. Shells and the warm tank still out |
| D. People (typical) | **430** | high | 220 + 210 lb |
| E. Trip cargo / food / gear | **TBD** | — | Reserve deliberately; don’t spend it on build |
| **Sum (A–D)** | **~1,400–1,450** | | No cabinets, floor, solar, inverter, tank shells, or cargo yet |
| **Payload limit** | **2,624** | | |
| **Remaining** | **~1,150–1,250** | | Only if the bank stays inside 12–15 kWh. A larger pack spends this remainder |

**Working discipline:** treat remaining payload as already claimed by unknown systems. Prefer **light first**, then spend weight only where convenience or safety demands it.

---

## Line items — current selections

Weights are **installed / shipping net** where known. Prefer datasheet net weight. Mark confidence: high = datasheet, med = catalog class, low = guess.

### Galley

| Item | Status | Est. lb | Conf. | Source / notes |
|------|--------|---------|-------|----------------|
| Fridge / freezer | preferred | **139** | high | **Furrion Arctic 10.7** dual-swing, chosen 2026-10-27 — [daily energy](daily-energy-budget.md) |
| Induction cooktop (2-burner) | researching | TBD | | |
| Oven / air-fryer | researching | TBD | | Post-MVP leaning |
| Microwave | researching | TBD | | Post-MVP leaning |
| Sink / faucet / counter materials | researching | TBD | | |

### Electrical

| Item | Status | Est. lb | Conf. | Source / notes |
|------|--------|---------|-------|----------------|
| House battery (48V LiFePO₄) | researching | **~240–300** if the ceiling holds | low | 12–15 kWh is a payload ceiling, not a locked size. See [daily energy](daily-energy-budget.md) |
| Inverter / charger | researching | TBD | | 120/240V capable |
| Solar PV + rack + fairing | post-MVP | TBD | | Dual-MPPT canopy on Orion or Vann Camp perimeter rack with high-bar risers |
| Webasto Cool Top Trail 48V | preferred | TBD | | Roof heat pump. Footprint 44.1×33.5×8.8" |
| MaxxAir MaxxFan Mini Plus | preferred | TBD | | Fixed 4.1" shroud under the canopy |
| DC-DC, busbars, wire, panels | researching | TBD | | 12V fridge feed included |
| Lights / outlets | researching | TBD | | Usually small |

### Water / plumbing

| Item | Status | Est. lb | Conf. | Source / notes |
|------|--------|---------|-------|----------------|
| Fresh tank (empty) | researching | TBD | | |
| Fresh water (**full**) | researching | **~292** | low | **35 gal × 8.34 lb/gal**. Tank shell still TBD |
| Grey water (**full**) | preferred | **~217** | low | **26 gal × 8.34**. Tank shell still TBD |
| Black water (**full**) | preferred | **~75** | low | **9 gal × 8.34**. Tank shell still TBD |
| Warm / hot tank + fluid | post-MVP | TBD | | Water or glycol |
| GoBluTech AR3 UVC | preferred | **~12** | high | Dry weight ~11.7 lb. Fill-side mount |
| Pump, PEX, valves, draft pump | researching | TBD | | |
| Instant EW (×2) | post-MVP | TBD | | |
| Solar thermal collector | post-MVP | TBD | | Deployable — may live outside payload when stowed on ground |

### Floor / insulation / interior

| Item | Status | Est. lb | Conf. | Source / notes |
|------|--------|---------|-------|----------------|
| PlantPanel X 1" (floor) | preferred | TBD | | Area × sheet weight — [floor products](../03-features/floor-subfloor/products.md) |
| Poplar plywood ¼–½" | preferred | TBD | | |
| Engineered bamboo ~7 mm | preferred | TBD | | |
| Wall / ceiling insulation | researching | TBD | | |
| Wall / ceiling finish | researching | TBD | | |

### Windows / exterior

| Item | Status | Est. lb | Conf. | Source / notes |
|------|--------|---------|-------|----------------|
| Arctic Tern Overland windows (set) | preferred | TBD | | Per-window × count |
| Tint / PDLC / coatings | researching | TBD | | Small vs glass |
| Hitch + QuikrStuff Mach 2 bike rack | MVP | TBD | | Hitch is first-trip. Tongue weight counts on payload when a rack or trailer is attached |
| Awning, other racks, step | post-MVP | TBD | | Easy to blow the budget |

### Furniture / living

| Item | Status | Est. lb | Conf. | Source / notes |
|------|--------|---------|-------|----------------|
| Bed lift mechanism | MVP | TBD (~40–220) | low | Strap/actuator kits lighter; HappiJac-class heavier — [bed-sleep](../03-features/bed-sleep/README.md) |
| Bed platform + mattress | MVP | TBD | | Lands on settee at night |
| Settee (structural sleep land) | MVP | TBD | | Must carry two adults + van motion |
| Table | MVP | TBD | | |
| Storage cabinets (food/clothes) | MVP | TBD | | Structure + doors — often heavier than expected |
| Toilet (marine electric flush) | MVP | TBD | | |

### People & cargo (not build, but spend payload)

| Item | Status | Est. lb | Conf. | Source / notes |
|------|--------|---------|-------|----------------|
| Occupants ×2 | typical | **430** | high | **220 + 210 lb** measured |
| Food / water jugs / clothes | typical | TBD | | |
| E-bikes / toys | optional | TBD | | Often the budget-breaker — may need hitch rack / leave home |

---

## Fancy footwork (stay under 2,624)

Ordered tactics when the roll-up gets tight:

1. **Omit or defer** — the aspirational list (awning, winch, and the rest) is not required to call the van finished. Hitch is already MVP. Leveling jacks are part of finishing the van.
2. **Smaller / lighter SKU** — e.g. GE fridge (~119 lb) vs Furrion (139 lb); thinner poplar; fewer cabinets.
3. **Count fluids honestly** — size tanks for need, not fantasy; optional travel with partial fresh if grey/black must be empty for weigh-in.
4. **Structure light** — honeycomb, poplar, aluminum where it still feels solid; no “boat teak everywhere.”
5. **Roof weight last** — PV, rack, fan, weather station compete with payload *and* CG height.
6. **People + toys budget is sacred** — don’t “use” the last 400 lb on build; leave it for life aboard.
7. **Weigh the finished van** — CAT scale before first long trip; reconcile this sheet.

Hard stop: if build + full fluids + people + minimum gear > 2,624, cut build weight — do not plan to overload.

---

## Balance notes

- Traction battery is already under the floor (mid) — house batteries and water tanks shift CG; prefer **aft wet weight** already driven by [ADR-0005](../05-decisions/0005-traction-battery-floor-no-drill-zone.md).
- Roof loads (PV, rack, fan) raise CG — keep light.
- Side-to-side: fridge and galley on one side may need opposing storage mass.
- Axle ratings: TBD from window sticker at purchase (GAWR front/rear) — payload may be limited by an axle before GVWR in some loadings.

## Open work

- [ ] Confirm GVWR / curb / payload / GAWR on purchase sticker
- [ ] Measure or datasheet every preferred product into line items
- [ ] Size tanks → full-fluid lb
- [ ] Size house battery from energy budget → lb
- [ ] Floor stack lb from area takeoff
- [ ] Set a hard **reserve** lb for people + gear (proposal: ≥400 lb) and never spend it on build
- [ ] CAT scale after major build phases

## Related

- [Daily energy budget](daily-energy-budget.md) — battery/solar size → weight
- [Van specs](../01-van/specs.md)
- [Constraints](../00-overview/constraints.md)
- [Galley products](../03-features/galley/products.md)
- [Floor products](../03-features/floor-subfloor/products.md)
