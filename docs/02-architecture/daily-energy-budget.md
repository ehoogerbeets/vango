# Daily Energy Budget

> Status: `researching`  
> Last updated: 2026-10-15

Running estimate of **house** electrical energy use (not traction). Used later to size the **48V house battery** and **solar PV** for ~3 off-grid nights ([vision](../00-overview/vision.md), [electrical](electrical.md)).

All figures are planning estimates — replace with measured / datasheet averages as products lock.

## How we use this page

1. List continuous and intermittent loads (Wh/day or Ah/day at a stated voltage).
2. Convert everything to **Wh/day at the house battery** (include DC-DC and inverter losses).
3. Battery usable kWh ≥ (daily Wh × nights without sun × margin) / 1000.
4. Solar array sized for a poor-sun day that can still replace a typical day’s use (plus charge losses).

**House bus reminder:** pack is **48V** ([ADR-0004](../05-decisions/0004-48v-house-dc-bus.md)). A **12V fridge** is fed through a **48V→12V DC-DC** (efficiency assumed **~92%** until measured).

Conversion helpers:

| From | To Wh/day |
|------|-----------|
| Ah/day @ 12V | × 12 |
| Ah/day @ 48V | × 48 |
| Average amps continuous @ 12V | × 12 × 24 |
| W continuous | × 24 |

---

## Fridge candidates (medium 12V, dual-hinge class)

Direction: **medium residential-style 12V compressor fridge**, dual-hinge / dual-swing preferred for layout flexibility. Both candidates are ~24" wide × ~60" tall — classic RV cutout class.

| | **GE Profile 9.8 cu ft** | **Furrion Arctic 10.7 cu ft** |
|--|-------------------------|------------------------------|
| Model (example) | PPV10R5YRSS | FCR10DCGBA-*-DS (dual swing) |
| Capacity | 9.8 cu ft | 10.7 cu ft (fridge 7.8 + freezer 2.9) |
| Voltage | 12V DC | 12V DC |
| Door | Top-freezer; **reversible** hinges | Bottom freezer drawer; **dual-swing** fridge door |
| Exterior (H × W × D) | **60 × 23.5 × 25.8 in** | **59⅞ × 23⅝ × 26³⁄₁₆ in** |
| Recessed depth | — | 22⁷⁄₁₆ in |
| Weight (net) | ~119 lb (related GE 9.8 class) | **139 lb** |
| Nameplate / peak | **13.5 A** @ 12V (~162 W) | Compressor **≤10 A**; defrost 10 A; standby 0.2 A |
| Published average draw | *Not published* (only nameplate) | **3.4 A** avg @ **75°F**; **5.2 A** avg @ **95°F** (datasheet “Amp/hr”) |
| **Est. Ah/day @ 12V** | **~40–80 Ah** class estimate (forum / duty-cycle; confirm with logging) | **~82 Ah** @ 75°F; **~125 Ah** @ 95°F |
| **Est. Wh/day @ 12V** | **~480–960 Wh** | **~980 Wh** @ 75°F; **~1,500 Wh** @ 95°F |
| **Est. Wh/day at 48V battery** (+8% DC-DC loss) | **~520–1,040 Wh** | **~1,065 Wh** @ 75°F; **~1,630 Wh** @ 95°F |

Sources (verify before purchase):

- GE Profile dims / 13.5 A: [GE Appliances PPV10R5YRSS](https://www.geappliances.com/appliance/GE-Profile-9-8-cu-ft-12V-DC-Top-Freezer-Refrigerator-PPV10R5YRSS), dealer listings
- Furrion Arctic 10.7 dual-swing: [spec sheet CCD-0008148](https://lci-support-doc.s3.amazonaws.com/furrion_refrigeration/specs/ccd-0008148.pdf), [Furrion product page](https://furrion.com/products/107-cuft-12v-french-door-refrigerator-french-door-10-7-cf-12v-refrigerator)

**Planning pick for budget math (until decided):** use **Furrion mild-day ~1.1 kWh/day at battery** and **hot-day ~1.6 kWh/day at battery** as the fridge line item. GE may be similar or slightly lower if duty cycle is kind; treat GE as **~0.7–1.1 kWh/day** until measured.

**ADR note:** ADR-0004 assumed a **48V** fridge. These candidates are **12V** — still compatible with a 48V pack via DC-DC, but the ADR wording should be amended when we lock the product (heat pump can stay 48V).

---

## Daily load rollup (house)

Fill Wh/day as products firm up. “Typical day” = mild weather, modest cooking, no long showers on instant EW. “Hot / heavy” = desert heat + more HVAC + more HW.

| Load | Domain | Typical Wh/day @ battery | Hot / heavy Wh/day | Notes / link |
|------|--------|--------------------------|--------------------|--------------|
| Fridge / freezer | 12V via DC-DC | **1,065** | **1,630** | Furrion planning figures above |
| Heat pump | 48V DC | TBD | TBD | Not on the first trip. **Still sizes the battery:** most of a high-desert day, **central sleep zone only**, spring–fall (not below ~40°F). |
| Lights | 12V | TBD | TBD | LED — usually small |
| Fresh pump + valves + sensors | 12V | TBD | TBD | Intermittent |
| UV water irradiator | TBD | TBD | TBD | Often hours/day while using water |
| Connectivity (Pi, Wi‑Fi, Ruuvi, weather) | 12V / low | TBD | TBD | Small vs fridge |
| Induction / microwave / oven | 120V AC | TBD | TBD | Burst loads; include inverter loss (~10%) |
| Instant EW (sink/shower) | 240V AC | TBD | TBD | Huge when used; solar thermal cuts this |
| Phantom / standby | mixed | TBD | TBD | BMS, always-on controls |
| **Subtotal (known)** | | **~1,065** | **~1,630** | Fridge only so far |
| **Contingency (planning)** | | +20% | +20% | Until other rows filled |
| **Working total (fridge-led draft)** | | **~1.3 kWh** | **~2.0 kWh** | **Placeholder — not build-ready** |

---

## Battery sizing sketch (method only)

Example once daily Wh is known:

\[
E_{\text{usable,kWh}} \ge \frac{E_{\text{day,Wh}} \times N_{\text{nights}} \times M}{1000}
\]

- \(N_{\text{nights}}\) ≈ **3** (off-grid target)
- \(M\) ≈ **1.2–1.4** (weather, aging, DoD policy)

With **only** the fridge draft totals above (other loads still TBD):

| Scenario | Day Wh | ×3 nights ×1.3 margin | Usable kWh (floor) |
|----------|--------|------------------------|--------------------|
| Mild, fridge-only draft | 1,300 | 5,070 | **~5 kWh** |
| Hot, fridge-only draft | 2,000 | 7,800 | **~8 kWh** |

Real house bank will be **larger** once heat pump, cooking, and HW are added — this table is a sanity check that the fridge alone already wants multi-kWh storage. The heat pump is absent on the fair-weather first trip and **still included** in the bank size. Trailer solar can top the bank up later through a van-wall DC-DC inlet; a week without the trailer cannot count on that array.

LiFePO₄ nameplate vs usable: apply BMS / DoD policy (e.g. 80–90% usable) when picking pack kWh.

---

## Solar sizing sketch (method only)

Poor-sun day harvest should cover a typical day (plus charge controller + DC-DC losses):

\[
P_{\text{array,W}} \approx \frac{E_{\text{day,Wh}}}{H_{\text{sun}} \times \eta}
\]

- \(H_{\text{sun}}\) = effective full-sun hours (site/season; often **2–4** for conservative van planning)
- \(\eta\) ≈ **0.7–0.8** (soiling, angle, controller, temperature)

Example: **1,300 Wh/day**, 3 sun-hours, η 0.75 → ~**580 W** array — again **fridge-led draft only**.

Deployable ground PV ([requirements](../01-van/requirements.md)) can supplement roof when parked.

---

## Open work

- [ ] Lock fridge SKU (GE Profile vs Furrion Arctic dual-swing vs other)
- [ ] Amend [ADR-0004](../05-decisions/0004-48v-house-dc-bus.md) for 12V fridge via DC-DC if we keep these candidates
- [ ] Add heat pump Wh/day (mild vs hot/cold)
- [ ] Add cooking + instant HW duty-cycle estimates
- [ ] Add lights / pump / controls / UV
- [ ] Pick house battery kWh and PV watts from completed rollup
- [ ] Log real fridge Ah/day after install (shunt)

## Related

- [Electrical architecture](electrical.md)
- [Payload budget & balance](weight-and-balance.md) — battery/solar mass must fit payload
- [Galley products](../03-features/galley/products.md)
- [Electrical-system feature](../03-features/electrical-system/README.md)
