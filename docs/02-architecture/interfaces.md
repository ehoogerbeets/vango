# System Interfaces

Dependency map so we don't design features in isolation.

| From → To | Interface / dependency | Notes |
|-----------|------------------------|-------|
| Traction battery → Layout | No-drill floor B-pillar→axle; wet aft / bed forward | [ADR-0005](../05-decisions/0005-traction-battery-floor-no-drill-zone.md) |
| Traction battery → Water | Under-mount tanks + dump penetrations only aft of rear axle | |
| Traction battery → Floor/furniture | OEM tie-downs only in battery span | |
| Layout → Electrical | Tech locker location, cable runs; no casual floor penetrations mid-van | |
| Layout → Water | Aft wet core → aft tanks | |
| Roof → Electrical | Solar + fans + heat pump clearance | |
| Insulation → Climate | R-value targets | |
| Electrical → Galley | Induction / fridge loads | |
| Electrical → Climate | 48V heat pump | |
| Exterior → Entry | Sliding-door step constrained by battery zone | |

## Build order implications

1. Vehicle + map battery keep-out + tie-down grid + roof / windows
2. Insulation & sound (thin floor/ceiling stacks)
3. Aft under-mount tank / penetration design
4. Electrical backbone
5. Plumbing backbone (aft wet)
6. Structural furniture on tie-downs / allowed structure
7. Finish surfaces & appliances
8. Commissioning & shakedown trips

