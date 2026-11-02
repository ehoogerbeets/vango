# Climate Architecture

> Status: `researching`

**Governing ADRs:** [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) (all-electric) · [ADR-0004](../05-decisions/0004-48v-house-dc-bus.md) (**48V DC** heat pump).

## Design goals

- Winter capability: occasional / shoulder seasons (design weather stays above about **40°F**)
- Summer capability: desert heat with AC — insulation must keep heat **out**
- Condensation control: TBD
- Energy: **Webasto Cool Top Trail 48V** on the house bus (not inverter AC)

## Strategy layers

1. **Insulation & air sealing** — dual purpose: retain heat in cool weather; reject heat in desert summers
2. **Ventilation & moisture** — **MaxxAir MaxxFan Mini Plus** (fixed 4.1" rain shroud) plus Tern window vents
3. **Active heat** — **Webasto Cool Top Trail 48V** only
4. **Active cooling** — same heat pump
5. **Window / cover treatments**

## Roof climate stack

Usable roof length on the 170" WB is about **160"**. The Webasto takes **44.1"** of that length and stands above the solar plane; about **115.9"** remains for the main solar runway. Panel tops sit flush with the rack and fairing when the hardware allows it. On the Orion Stealth+ that plane is **5.4"** (rail and fairing). A typical **30 mm** frame then puts the panel underside near **4.2"**; a **35 mm** frame lands it near **4.0"**.

| Level | Height | What |
|-------|--------|------|
| 0 | Roof sheet | Van metal |
| 1 | **+4.1"** | MaxxFan Mini Plus stationary dome, under the panels |
| 2 | **~+4.0"–4.2"** | Underside of panels whose tops are flush with the rack and fairing |
| 3 | **+5.4"** | Top of the rack, the fairing, and the solar panels |
| — | **+8.8"** | Webasto Cool Top Trail shroud, above the panel plane |

The **4.1"** fan fits under that underside. A **30 mm** frame is the one that clears it; a **35 mm** frame is tight against the same datum, so prefer the shallower frame when holding the top at **5.4"**. Crossbars still stay off the fan’s rear exhaust louvers. The Webasto does not fit under this plane, so panels do not bridge it. It keeps a **4"** clear perimeter for its intake grills. Rack and dual-MPPT details: [exterior](../03-features/exterior/README.md) · [electrical](electrical.md).

## Major decisions (links)

| Topic | Status | Doc / ADR |
|-------|--------|-----------|
| No combustion heat | accepted | [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) |
| Heat pump (not resistive / mattress pads) | accepted | [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) |
| Heat pump voltage **48V DC** | accepted | [ADR-0004](../05-decisions/0004-48v-house-dc-bus.md) |
| Heat pump product **Webasto Cool Top Trail 48V** | accepted | [heating-cooling](../03-features/heating-cooling/README.md) · handoff 2026-10-28 |
| Roof fan **MaxxAir MaxxFan Mini Plus** | accepted | [windows-ventilation](../03-features/windows-ventilation/README.md) · handoff 2026-10-28 |
| Panel tops **flush with the rack and fairing**; fan under that plane, Webasto above it | accepted | [exterior](../03-features/exterior/README.md) · 2026-10-30 |
| Insulation materials | open | |
| Exact roof stations for the two 14" cutouts | open | Must clear crossbars behind the MaxxFan exhaust louvers |

## Related

- [Insulation](../03-features/insulation/README.md)
- [Heating & cooling](../03-features/heating-cooling/README.md)
- [Windows & ventilation](../03-features/windows-ventilation/README.md)
- [Exterior](../03-features/exterior/README.md) — roof rack and solar canopy
