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

Usable roof length on the 170" WB is about **160"**. The Webasto takes **44.1"** of that length; about **115.9"** remains for the main solar runway. Vertical stack over the AC:

| Level | Height | What |
|-------|--------|------|
| 0 | Roof sheet | Van metal |
| 1 | **+4.1"** | MaxxFan Mini Plus stationary dome |
| 2 | **+8.8"** | Webasto Cool Top Trail shroud |
| 3 | **+9.5"–10.0"** | Bottom of elevated solar panels on high-bar risers |

That leaves about **5.4"–5.9"** of open plenum over the fan and about **0.7"–1.2"** of breathing gap over the Webasto top exhaust. The Webasto also needs a **4"** clear perimeter for its intake grills. Rack and dual-MPPT canopy details: [exterior](../03-features/exterior/README.md) · [electrical](electrical.md).

## Major decisions (links)

| Topic | Status | Doc / ADR |
|-------|--------|-----------|
| No combustion heat | accepted | [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) |
| Heat pump (not resistive / mattress pads) | accepted | [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) |
| Heat pump voltage **48V DC** | accepted | [ADR-0004](../05-decisions/0004-48v-house-dc-bus.md) |
| Heat pump product **Webasto Cool Top Trail 48V** | accepted | [heating-cooling](../03-features/heating-cooling/README.md) · handoff 2026-10-28 |
| Roof fan **MaxxAir MaxxFan Mini Plus** | accepted | [windows-ventilation](../03-features/windows-ventilation/README.md) · handoff 2026-10-28 |
| Insulation materials | open | |
| Exact roof stations for the two 14" cutouts | open | Must clear crossbars behind the MaxxFan exhaust louvers |

## Related

- [Insulation](../03-features/insulation/README.md)
- [Heating & cooling](../03-features/heating-cooling/README.md)
- [Windows & ventilation](../03-features/windows-ventilation/README.md)
- [Exterior](../03-features/exterior/README.md) — roof rack and solar canopy
