# Daily Energy Budget

> Status: `researching`  
> Last updated: 2026-10-27

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

**Chosen fridge (2026-10-27):** **Furrion Arctic 10.7** dual-swing. The door has to open from either side. Use **mild-day ~1.1 kWh/day at battery** and **hot-day ~1.6 kWh/day at battery**. The GE Profile stays in the table as the lighter alternate we did not pick (~20 lb, and a hinge that is chosen once).

**ADR note:** ADR-0004’s fridge row is amended. This fridge is **12V** through a 48V→12V DC-DC. The heat pump is locked as the **Webasto Cool Top Trail 48V** (2026-10-28). The unnamed 120V / 1,590 W contender is rejected.

---

## How the bank is supposed to be used (2026-10-27)

The pack size is **not locked**. **12–15 kWh** nameplate (~240–300 lb) is only the payload ceiling named so far. The inventory below was not in the math when that ceiling was written.

- **Trailer-less.** Fridge, lights, moderate cooking, navy showers, plus the electronics on this page. Not three days of desert cooling stored in the van.
- **High desert, cooling into the evening.** Planned with the **trailer and its deployable solar**, which refill the bank. Daytime cooling is a solar load.
- **Cooking.** Foodies: some meals are short, some are long, some are outside on the fire. Budget a **moderate** induction day with **both burners** available. The cooktop nameplate is **3,000 W**.
- **Hot water, once the heaters exist.** Hot sink plus a **short navy shower for each person**, off the house battery. Campground showers are still the real shower.
- **Same time.** The sink heater and **one** induction burner may run together. A shower waits. The heat pump is on the **48V** bus, so it does not fight the inverter with the cooktop. A full 3,000 W cooktop plus a 1,500 W coffee maker is still an inverter problem and is not decided.
- **Surplus to the drive battery (aspirational).** When the house bank is full, a **240V** inverter output would feed a portable Level 2 EVSE (Lectron class) into the **Mercedes charge port** under the front logo, at **3 kW max**. That is about the roof plus the deployed panels together. Nothing under the hood is tapped. This path would spend solar surplus. It is not energy the 3-night reserve has to store, and it is not part of finishing the van. Traction power still does not flow back into the house.

## Daily load rollup (house)

“Typical” is mild weather and that moderate cook, with navy showers once hot water exists. “Desert evening” is a hot day: Furrion’s 95°F fridge figure, plus battery-supplied cooling after the sun is no longer carrying the heat pump. Figures below the fridge row are planning estimates until products are logged.

| Load | Domain | Typical Wh/day @ battery | Desert evening Wh/day | Notes / link |
|------|--------|--------------------------|-----------------------|--------------|
| Fridge / freezer | 12V via DC-DC | **1,065** | **1,630** | Furrion, chosen |
| Heat pump | 48V DC | **0** | **~3,000** | **Webasto Cool Top Trail 48V.** Daytime cool is solar. Evening planning figure is still **~3 kWh** (~2–3 h near the **0.80–1.40 kW** nominal band; peak surge **1.50 kW**). Real duty hours still open. This row moves the bank size more than any other. |
| Lights | **12V** | **~80** | **~80** | Puck and ambient. Small. |
| Induction, some oven / microwave | 120V AC | **~1,650** | **~2,200** | Moderate both-burner day ≈ 1.5 kWh at the outlet, ×~10% inverter loss. Desert row is a longer indoor day. Fire meals are the rest. |
| Instant EW (sink + navy showers) | 240V AC | **~1,200** | **~1,200** | ~8 gal heated ~50°F (about 4 gal of showers + 4 gal of hot sink) ≈ 145 Wh/gal at the battery. Solar-thermal preheat cuts this later. |
| Starlink | 12V via DC-DC | **~2,000** | **~2,000** | **75 W × 24 h**, plus DC-DC loss. On whenever the van is occupied |
| Pump, valves, sensors, UV, controls | 12V / low | **~200** | **~200** | Placeholder. The inventory below splits this family out; this row stays until those Wh exist |
| **Subtotal** | | **~6,200** | **~10,300** | Fridge, Starlink, cook, hot water, a heat-pump guess, and one small row |
| **Contingency** | | +20% | +20% | |
| **Working total** | | **~7.4 kWh** | **~12.4 kWh** | **Still incomplete.** Laptops, lights at 100 W, the wine fridge, and a real heat-pump hour count are not in this total |

---

## Load inventory (2026-10-27)

Everything named so far. **Storage** loads run for hours and move the battery kWh. **Demand** loads have a high nameplate and a short duty, so they size the inverter and the wire, not the 3-night reserve. Rechargeable gadgets count as the energy to refill them, not as their motor watts.

Stated watts are Edwin’s. Where a daily Wh figure appears, the hours are an assumption, marked as such.

### Storage — hours long

| Load | Domain as listed | Stated | Daily energy | Notes |
|------|------------------|--------|--------------|-------|
| Fridge / freezer | 12V | Furrion average | **1.1–1.6 kWh** | Already in the rollup |
| Wine / beer fridge | 12V (iCompact / slim class) | | **TBD** | Second compressor. Not in the rollup |
| Lights | 12V | **100 W total** | ~0.4 kWh if 4 h | Replaces the 80 Wh guess. Patio floods and the driving flood bank are separate |
| Starlink | 12V list | **75 W**, **112 W** peak | **1.8 kWh** at the dish | On the whole time anyone is in the van, including work days. About **2.0 kWh** at the battery after the 48V→12V DC-DC |
| Linksys mesh Wi-Fi | 12V list | | small | Hours not set |
| Weboost | 12V list | | small | Hours not set |
| Van-controls tablet | electronics | | small if the screen sleeps | |
| MacBook Pro + MacBook Air | USB-C or their chargers | | ~0.5 kWh on a work day | Not every camping day |
| Sound system | electronics | | **TBD** | Separate from the two Sonos Roams, which are rechargeable |
| Humidifier, ultrasonic | 12V list | **25 W** | 0.1 kWh at 4 h | |
| Heat pump | **48V DC** | Webasto Cool Top Trail: **0.80–1.40 kW** nominal, **1.50 kW** peak | **~0.8–1.4 kWh per hour it runs** | Soft-start inverter compressor. Cool 12.3k BTU / heat 11.6k BTU. Two evening hours near mid-band ≈ the ~3 kWh planning figure. A long afternoon still empties a 12–15 kWh pack by itself |
| Dehumidifier | listed with the heat pump | | **TBD** | May be the heat pump’s dry mode, not a second machine |
| PDLC window film | 12V list | | **TBD** | Power while the film is clear. Area not set |
| Security cameras | Google or SimpliSafe | | **TBD** | Base station is the continuous piece |
| GoBluTech AR3 UVC | **12V ~1 A** via buck-boost | ~12 W while filling | Flow-sensor UV. Energy is fill time × ~12 W — small next to the fridge. Not a 120V circuit |
| Off-grid draft pump | **12V** | while drafting | Lakes / jerry cans into the fill manifold. Intermittent |
| Demand pump | 12V | | intermittent |
| Reverse osmosis | 12V list, with the pump | | while making water | The trailer page still puts the RO machine on the trailer |
| Smoke / CO | 12V or its own battery | | tiny | |

### Demand — short duty, high watts

| Load | Domain as listed | Stated | Notes |
|------|------------------|--------|-------|
| 2-burner induction | 120V dedicated | **3,000 W** | Nameplate. Moderate-day energy in the rollup is still ~1.5 kWh at the outlet |
| Microwave / convection / air fryer | 120V dedicated | **1,500 W** | One circuit for that combo |
| Keurig K-Slim / K-Mini, or Nespresso | 120V outlet | **1,500 W** | A brew is minutes. Plumbed PEX feed still stands |
| Instant Pot Duo Crisp | 120V outlet | **1,500 W** | A cycle, not an all-day load |
| Hair dryer | 120V outlet | **1,800 W** | Very occasional |
| Hand mixer | 120V outlet | **400 W** | |
| Outdoor grill | 120V, side GFCI | | Watts not set |
| Mini dishwasher, in-sink or countertop | 120V dedicated | | Watts not set. Also a grey-water load |
| Garbage disposal | 120V dedicated | | Seconds at a time |
| LG TV / 4K monitor | 120V dedicated | | Watts not set |
| Side GFCI | 120V dedicated | | The grill and anything else outdoors |
| Winch, front | **12V**, if ever | **15,000–18,000 lb** | Aspirational. Not in the energy total. A full pull is hundreds of amps and wants its own battery |
| 4-point leveling jacks | 12V list | **500 W** | A minute or two. Also named under electronics |
| Electric-flush macerating toilet | 12V | | Seconds per flush |
| Grey and black dump valves | 12V | | Seconds |
| Fold-out step | 12V list | | Seconds |
| Patio flood lights | 12V list | | |
| Forward flood-light bank | 12V list | | For driving. Hours if used on the road |
| Hotel-style safe (laptops and valuables) | 12V list | | Motor is a short run. Sized for the two laptops |
| Magnetic cabinet locks | 12V list | | |
| Tank level sensors, leak detectors | 12V | | Tiny. Leak-detector class: a Govee-style sensor |

### Rechargeables — count the refill, not the motor

USB-C for phones, laptops, watches, and AirPods. Also portable batteries, a camera, a bike / kayak / tire air pump, a 3 W food thermometer, two Sonos Roam speakers, a Black+Decker cordless handheld vacuum, flashlights, electric lanterns, a rechargeable Buzbug-class bug zapper, a DeWalt DCB094 charger for tool packs, a Shark Ninja Blast blender, coffee and spice grinders, and an electric toothbrush. Prefer a 12V Oral-B charger if one exists, so the brush does not need the inverter.

A planning bunch for all of these together is a few hundred Wh on a day they actually get charged. Not in the rollup total yet.

### 240V

| Load | Stated | Notes |
|------|--------|-------|
| Portable Level 2 EVSE into the Mercedes charge port | **3 kW max** | **Aspirational.** Lectron class. Would run when the **house bank is full**, fed by the house inverter’s 240V output. Surplus solar to traction. Does not open the hood. Not part of finishing the van |
| Instant sink and shower heaters | from the water architecture | Still **240V**. This inventory did not replace them. They and the EVSE both want 240V; whether they ever run together is open |

---

## Battery sizing sketch (method only)

Example once daily Wh is known:

\[
E_{\text{usable,kWh}} \ge \frac{E_{\text{day,Wh}} \times N_{\text{nights}} \times M}{1000}
\]

- \(N_{\text{nights}}\) ≈ **3** (off-grid target)
- \(M\) ≈ **1.2–1.4** (weather, aging, DoD policy)

Using the working totals above, \(N = 3\), \(M = 1.3\):

| Scenario | Day Wh | ×3 nights ×1.3 | Usable kWh (floor) |
|----------|--------|----------------|--------------------|
| Mild, no evening cooling | 7,400 | 28,900 | **~29 kWh** |
| Desert, cooling into the evening | 12,400 | 48,400 | **~48 kWh** |

**Payload ceiling, not a locked pack (2026-10-27):** **12–15 kWh** nameplate (~240–300 lb at ~20 lb/kWh) is as heavy a house bank as the payload conversation has allowed. It is not the answer to this inventory. The ~40 kWh / ~1,000 lb pack that would store three desert evenings still does not fit. At ~85% depth of discharge, 12–15 kWh is about **10–13 kWh** usable. Starlink is now in the rollup. Laptops, lights at 100 W, and the wine fridge are still not:

| What the cap holds | Days in the bank |
|--------------------|------------------|
| Mild day in the rollup (~7.4 kWh) | About **one** sunless day, and a second only if the roof puts a lot back. |
| Desert evening in the rollup (~12.4 kWh) | About **one** day, and the ceiling is already full. |

High-desert trips that cool into the evening happen **with the trailer and its deployable solar**, which refill the bank through the van-wall inlet. The van does not store three desert days by itself. Trailer-less use is the mild column: fridge, lights, moderate cooking, navy showers. Daytime cooling, when the heat pump exists, is still a solar load.

LiFePO₄ nameplate vs usable: apply BMS / DoD policy (e.g. 80–90% usable) when picking pack kWh.

---

## Solar sizing sketch (method only)

Poor-sun day harvest should cover a typical day (plus charge controller + DC-DC losses):

\[
P_{\text{array,W}} \approx \frac{E_{\text{day,Wh}}}{H_{\text{sun}} \times \eta}
\]

- \(H_{\text{sun}}\) = effective full-sun hours (site/season; often **2–4** for conservative van planning)
- \(\eta\) ≈ **0.7–0.8** (soiling, angle, controller, temperature)

Example: the **mild ~7,400 Wh/day**, 3 sun-hours, η 0.75 → about **3,300 W** of array to replace that day. Roof plus deployed panels are described as about **3 kW** together, which is why a mild day is not something the roof replaces alone. The aspirational traction EVSE is capped at that same 3 kW. Daytime desert cooling is an extra solar load on top of this.

Deployable trailer PV can supplement the roof when the trailer is along. It does not count on a trailer-less week.

---

## Open work

- [x] Lock fridge SKU — **Furrion Arctic 10.7** dual-swing (2026-10-27)
- [x] Amend [ADR-0004](../05-decisions/0004-48v-house-dc-bus.md) — fridge is 12V via DC-DC; heat pump stays 48V
- [x] Heat pump product — **Webasto Cool Top Trail 48V** (2026-10-28). Evening Wh still uses a **~3 kWh** planning figure until real duty hours exist
- [x] Add cooking + instant HW duty-cycle estimates (moderate both-burner day; navy showers + hot sink)
- [ ] Split the combined ~200 Wh placeholder into lights, pump, UV, and controls
- [ ] House battery kWh is **not locked**. 12–15 kWh is a payload ceiling only. Revisit after the inventory rows have hours
- [x] Heat-pump voltage locked **48V** with the Webasto. The 120V / 1,590 W contender is rejected
- [x] Starlink hours — on the whole time the van is occupied, **75 W** average, **~1.8 kWh/day** at the dish
- [ ] Set laptop days and light hours — those still move the mild-day total
- [ ] Inverter kW: 3,000 W induction, 1,500 W oven, and 1,800 W hair dryer. The heat pump is on 48V DC and does not size the inverter. Simultaneous AC use is open. The 3 kW 240V EVSE is aspirational and does not size this inverter
- [ ] Roof watts, once a real daily Wh exists. Dual-MPPT canopy layout is locked; total array watts are not. The aspirational EVSE stays capped near the roof-plus-deployed ceiling
- [ ] Log real fridge Ah/day after install (shunt)

## Related

- [Electrical architecture](electrical.md)
- [Payload budget & balance](weight-and-balance.md) — battery/solar mass must fit payload
- [Galley products](../03-features/galley/products.md)
- [Electrical-system feature](../03-features/electrical-system/README.md)
