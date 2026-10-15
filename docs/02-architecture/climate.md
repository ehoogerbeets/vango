# Climate Architecture

> Status: `researching`

**Governing ADRs:** [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) (all-electric) · [ADR-0004](../05-decisions/0004-48v-house-dc-bus.md) (**48V DC** heat pump).

## Design goals

- Winter capability: occasional / shoulder seasons
- Summer capability: desert heat with AC — insulation must keep heat **out**
- Condensation control: TBD
- Energy: **48V DC** heat pump on house bus (not inverter AC)

## Strategy layers

1. **Insulation & air sealing** — dual purpose: retain heat in cool weather; reject heat in desert summers
2. **Ventilation & moisture**
3. **Active heat** — **48V DC heat pump** only (current plan)
4. **Active cooling** — same heat pump / AC path
5. **Window / cover treatments**

## Major decisions (links)

| Topic | Status | Doc / ADR |
|-------|--------|-----------|
| No combustion heat | accepted | [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) |
| Heat pump (not resistive / mattress pads) | accepted | [ADR-0003](../05-decisions/0003-all-electric-house-systems.md) |
| Heat pump voltage **48V DC** | accepted | [ADR-0004](../05-decisions/0004-48v-house-dc-bus.md) |
| Insulation materials | open | |
| Roof fan(s) | open | |
| Heat pump product (brand/BTU) | open | |

## Related

- [Insulation](../03-features/insulation/README.md)
- [Heating & cooling](../03-features/heating-cooling/README.md)
- [Windows & ventilation](../03-features/windows-ventilation/README.md)
