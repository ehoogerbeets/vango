# Electrical Architecture

> Status: `researching`

**Governing ADRs:** [ADR-0002](../05-decisions/0002-mercedes-e-sprinter-platform.md) · [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) · [ADR-0004](../05-decisions/0004-48v-house-dc-bus.md)

## Design goals

- Target off-grid nights: ~3 without want
- Shore power: North America v1 — expect **120/240V** capability for instant HW (50A RV-style pedestal class TBD)
- Home charge (traction): Level 2 **11.5 kW** already owned; DCFC on road trips
- House storage: **separate 48V** LiFePO₄ bank (or solid-state later) — not the 113 kWh drive battery
- **48V DC** bus for heat pump + fridge/freezer (and other DC loads as designed)
- Inverter/charger: **120V + 240V** AC output — cooking mostly 120V; **instant HW is 240V**
- Solar PV: TBD sizing (charge into 48V house)
- Solar thermal: deployable collector preheats warm-water tank (see [water](water.md))
- Controls power for tank sensors + electric dump valves (app) — see [connectivity](../03-features/connectivity/README.md)

## Voltage domains

| Domain | Used for |
|--------|----------|
| **48V DC** | Heat pump, fridge/freezer, house battery bus; other DC TBD |
| **120V AC** | Induction, oven/air-fryer, microwave, exterior outlet (and similar) |
| **240V AC** | Instant electric water heaters (sink + shower) — high power |
| Low-voltage DC (12V?) | Lights / small electronics / many pumps & valves — derive from 48V TBD |

## Block diagram

```mermaid
flowchart TD
  solar[Solar PV] --> sc[48V charge controller]
  shore[Shore NA 120/240] --> ic[Inverter / charger]
  sc --> batt[House battery 48V LiFePO4]
  ic --> batt
  traction[e-Sprinter 113 kWh traction] -.->|no house export| x[Not connected to house]

  batt --> dc48[48V DC bus]
  dc48 --> hp[Heat pump]
  dc48 --> fridge[Fridge / freezer]
  dc48 --> other48[Other DC TBD]

  batt --> dcdc[DC-DC / 12V?]
  dcdc --> lv[Pump / toilet / valves / sensors / controls]

  batt --> inv[Inverter]
  inv --> ac120[120V AC]
  ac120 --> cook[Induction / oven / microwave]
  ac120 --> ext[Exterior outlet]
  inv --> ac240[240V AC]
  ac240 --> hw[Instant EW sink + shower]
```

\* Solid-state house cells OK if practical at build time.

## Known major loads (direction)

| Load | Power domain | Notes |
|------|--------------|-------|
| Heat pump | **48V DC** | HVAC |
| Fridge / freezer | **48V DC** | |
| 2-burner induction | 120V AC | Indoor + movable to exterior outlet |
| Combo oven / air-fry / toast | 120V AC | e.g. Ninja Flip class |
| Small microwave | 120V AC | |
| Instant electric HW (×2) | **240V AC** | Sink + shower; solar thermal preheat reduces duty |
| Exterior AC outlet | 120V AC | Grill / outdoor induction |
| Demand pump | DC TBD | |
| Electric dump ball valves | DC + controls | Grey + black; app actuated |
| Tank level sensors | Low power DC / controls | Fresh + grey + black → app |
| UV water irradiator | TBD (often 12V or 120V) | After fine filter; serviceable lamp |
| Marine electric toilet | DC TBD | |

## Major decisions (links)

| Topic | Status | Doc / ADR |
|-------|--------|-----------|
| No combustion fuels | accepted | [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) |
| Separate house battery | accepted | [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) |
| **48V DC** bus + heat pump + fridge | accepted | [ADR-0004](../05-decisions/0004-48v-house-dc-bus.md) |
| Instant HW on **240V AC** | accepted | [water](water.md) |
| House kWh | open | |
| 12V derived bus for lights/valves/etc. | open | |
| Inverter topology (split-phase 120/240) | open | Must feed 240V EW + 120V cook |
| Solar PV size | open | |
| Exterior AC circuit | open | GFCI / weatherproof |

## Interfaces

- Depends on: roof layout (PV + thermal stowage + fans), insulation, weight (~2,624 lb payload class)
- Provides to: galley, climate, plumbing (incl. 240V HW, valves, sensors), lights, pumps, devices
