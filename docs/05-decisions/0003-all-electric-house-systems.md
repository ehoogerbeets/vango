# ADR-0003: All-electric house systems (no combustion fuels onboard)

- **Date:** 2026-10-13
- **Status:** `accepted`
- **Deciders:** Edwin
- **Tags:** electrical, climate, galley, plumbing, eco, safety

## Context

The van is an “RV in a van” used weekends through summers, often off-grid, with eco-friendly design as the top philosophy. The base vehicle is an e-Sprinter ([ADR-0002](0002-mercedes-e-sprinter-platform.md)) whose traction battery **cannot** meaningfully power the house (OEM 12V accessory terminal is cellphone-class only). Comfort loads — cooking, heat pump, instant electric hot water, fridge, etc. — therefore need a real house electrical system, and we refuse onboard combustion fuels.

## Decision

**House energy is electricity only.**

There will be **no onboard** diesel, gasoline, propane, or camping-gas systems for heat, cooking, hot water, refrigeration, or generators.

### Electrical topology (house)

- **Separate house battery** — not the drive battery.
- Chemistry target: **LiFePO₄** now; reconsider **lithium solid-state** if commercially practical around purchase/build (~2 years).
- High-output **inverter/charger** required — **120V AC** for cooking/plugs and **240V AC** for instant water heaters.
- Solar PV expected as part of the charge picture (sizing TBD).
- **Solar thermal** used to pre-warm a “warm water” storage tank so instant electric heaters do less work.

### Indoor cooking (installed)

All **120V AC**:

| Appliance | Direction |
|-----------|-----------|
| Cooktop | **2-burner induction** |
| Oven / air-fry / toast | Combo unit (e.g. Ninja Flip Toaster Oven & Air Fryer class) |
| Microwave | Small microwave |

### Climate

- **Heat pump** for active HVAC (heating and cooling path) — **48V DC** model ([ADR-0004](0004-48v-house-dc-bus.md)).
- **No** resistive primary heat and **no** heated mattress-pad strategy for now.
- **Insulation is critical** both for cool-season warmth and for keeping desert heat out while AC runs.

### Refrigeration

- **Fridge / freezer** — **48V DC** model ([ADR-0004](0004-48v-house-dc-bus.md)).

### Hot water

- **Instant electric** heaters at **sink** and **shower** — **240V AC** (adequate tankless units need this much power; 120V is not the product class we’re using).
- **Warm-water storage tank** preheated by a **deployable solar thermal collector** to minimize instant-electric runtime/energy.
- House inverter/shore topology must supply **240V** (typically NA split-phase 120/240).

### Outdoor cooking (allowed exceptions — not house combustion systems)

- Wood **campfire** when the site has one.
- **Electric grill**.
- Ability to **relocate the induction cooktop** to an **exterior AC outlet** on the van.

No hard “electric appliance bans” beyond the combustion rule — energy budget and weight decide.

## Why

- Matches eco-friendly goal; one onboard energy paradigm
- Traction battery cannot supply house loads → honest separate house bank design
- Avoids CO / propane / diesel-heater complexity and emissions inside the envelope
- Induction + heat pump + instant EW + solar thermal is a coherent high-efficiency electric stack
- Outdoor electric/campfire cooking preserves fun without installing gas

## Alternatives considered

### Alternative A — Propane cook / heat / HW

- Pros: Familiar RV pattern; less inverter load
- Cons: Onboard fossil fuel; conflicts with eco + this ADR
- Why not: Explicitly out of scope

### Alternative B — Diesel-fired heater

- Pros: Low electrical draw for cabin heat
- Cons: Diesel onboard; exhaust; conflicts with decision
- Why not: Explicitly out of scope

### Alternative C — Power house from traction battery

- Pros: Huge kWh pool; less duplicate storage
- Cons: e-Sprinter does not support meaningful house export; 12V tap is useless for real loads
- Why not: Not available — separate house battery required

### Alternative D — Resistive heat / heated bedding as primary comfort

- Pros: Simple
- Cons: Harsh on off-grid budget; heat pump + insulation preferred
- Why not: Deferred; not current plan

## Consequences

### Positive

- Clear product filter for appliances and heaters
- House battery / inverter / solar / solar-thermal become first-class architecture
- Exterior AC outlet + movable induction supports outdoor cooking without gas
- Insulation investment pays in both winter shoulder season and desert AC loads

### Negative / trade-offs

- Inverter/charger must be sized for **concurrent or peaky** AC loads — **240V** instant HW is a major spike; 120V cooking separate; heat pump and fridge stay on **48V DC**
- Separate house battery adds cost, weight, and space — must still honor ~2,624 lb payload class with 113 kWh van ([ADR-0002](0002-mercedes-e-sprinter-platform.md))
- Instant electric HW is power-hungry (**240V** class); solar thermal preheat is important, not optional fluff
- Off-grid hot showers compete hard with battery/inverter budget — warm-tank strategy + load management matter
- Deployable solar thermal adds setup convenience risk (vision: ultra-convenient or omit — design the deploy carefully)
- Off-grid ~3 nights is an energy-budget problem across cook + climate + HW

### Follow-ups

- [ ] House battery kWh and mounting location (bus is **48V** — [ADR-0004](0004-48v-house-dc-bus.md))
- [ ] Inverter/charger continuous + surge sizing from **AC** load spreadsheet
- [ ] Solar PV array size / roof layout vs fans / thermal collector stowage
- [ ] Specify 48V heat pump and 48V fridge/freezer products (BTU, capacity, winter performance)
- [ ] Detail warm-tank + dual instant EW plumbing in [water architecture](../02-architecture/water.md)
- [ ] Exterior AC outlet circuit design (GFCI, weatherproofing)
- [ ] Product picks: induction, Ninja-class oven, microwave, electric grill → feature `products.md` + BOM
- [ ] Revisit solid-state house cells near build time

## Links

- Related features: electrical-system, heating-cooling, galley, plumbing, bathroom, insulation
- Related docs: [ADR-0002](0002-mercedes-e-sprinter-platform.md), [electrical architecture](../02-architecture/electrical.md), [climate](../02-architecture/climate.md), [water](../02-architecture/water.md)
- Supersedes: —
- Superseded by: —
