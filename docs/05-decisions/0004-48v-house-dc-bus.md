# ADR-0004: 48V DC house bus for major DC appliances

- **Date:** 2026-10-13
- **Status:** `accepted`
- **Deciders:** Edwin
- **Tags:** electrical, climate, galley

## Context

House loads are all-electric ([ADR-0003](0003-all-electric-house-systems.md)) with a separate house battery. Cooking remains **120V AC**; instant hot water is **240V AC**. Climate and refrigeration run on **48V DC**, reducing inverter runtime and cable losses versus a 12V-centric design.

## Decision

The house electrical system uses a **48V DC** bus for major DC appliances, including:

| Appliance | Voltage |
|-----------|---------|
| Heat pump | **48V DC** |
| Fridge / freezer | **48V DC** *(under review — 12V candidates via DC-DC; see [daily energy budget](../02-architecture/daily-energy-budget.md))* |

House battery chemistry remains LiFePO₄ (or solid-state later) per ADR-0003; pack topology should align with the **48V** bus (exact series string / BMS TBD).

Inverter/charger AC domains: **120V** for induction, oven/air-fryer, microwave, exterior outlet; **240V** for instant electric HW.

## Why

- Heat pump and fridge/freezer chosen as 48V DC models — bus must match
- 48V reduces current (and thus cable gauge / losses) vs 12V for the same power
- Keeps continuous loads (fridge, climate) off the inverter when possible → better off-grid efficiency

## Alternatives considered

### Alternative A — 12V DC heat pump and fridge

- Pros: Huge 12V accessory ecosystem
- Cons: High current for compressor loads; heavier cabling; not our product direction
- Why not: Selected appliances are 48V

### Alternative B — 120V AC heat pump and fridge

- Pros: Simple “everything on inverter” mental model
- Cons: Inverter must run for fridge 24/7 and for climate; idle/conversion losses
- Why not: Prefer DC for these continuous / large loads

### Alternative C — 24V DC bus

- Pros: Middle ground on current vs 12V
- Cons: Doesn’t match chosen 48V heat pump / fridge
- Why not: Appliance choice drives 48V

## Consequences

### Positive

- Clear voltage domains: **48V DC** (climate, refrigeration) vs **120V AC** (cooking, plugs) vs **240V AC** (instant HW)
- Better efficiency story for multi-day off-grid

### Negative / trade-offs

- 48V component ecosystem is smaller than 12V — plan purchases carefully
- Cabin lights are **12V puck and ambient** (2026-10-26), on a derived 12V branch. The 2026-10-25 native-48V light choice is withdrawn: travel-hardened fixtures are 12V. Pumps and valves may share that branch
- Safety: 48V needs proper fusing, service discipline, and clear labeling

### Follow-ups

- [ ] House battery pack voltage / BMS / kWh sizing
- [x] Lights are **12V puck and ambient** (2026-10-26). Pumps and valves are still open
- [ ] Pick heat pump and fridge/freezer products → feature `products.md` + BOM
- [ ] Update load spreadsheet: DC vs AC columns

## Links

- Related features: electrical-system, heating-cooling, galley
- Related docs: [ADR-0003](0003-all-electric-house-systems.md), [electrical architecture](../02-architecture/electrical.md)
- Supersedes: —
- Superseded by: —
