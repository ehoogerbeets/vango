# Feature: Exterior & Awning

> Status: `researching`  
> Priority: `P1`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-15

## Summary

Outside shell integrations: **aftermarket trailer hitch**, **roof rainwater capture**, aft under-mount tank packaging, a van-wall socket for the trailer, and a constrained **sliding-door step** under [ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md).

## Goals

- Capture rain from the roof for filtered top-up of the fresh tank (eco)
- Coexist with solar PV, deployable solar thermal, fans, and other roof gear
- Convenient enough that rain capture actually gets used / maintained
- Safe, convenient entry at the sliding door despite battery-zone keep-out

## Non-goals

- Using untreated roof runoff as drinking water without filtration
- Overseas ferry/height rules driving v1 (beyond e-Sprinter envelope)
- Free drilling under the sliding door through the traction-battery floor span

## Requirements

### Must

- Rain collection path from roof → debris / first-flush strategy (TBD) → plumbing **fill filtration** → fresh tank
- Not compromise standing-height / roof stack carelessly
- Light-weight where possible
- Respect battery-zone **no-drill** rules for any under-vehicle hardware ([ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md))
- Aft under-mount tanks/plumbing protected for road debris / clearance
- **Trailer hitch on the first trip.** Short trips: bikes on a hitch rack. Long trips: tow the gear trailer ([storage](../storage/README.md))
- Van-wall socket for the trailer: DC-DC surplus charge into the house bank, and the warm-tank hoses from the trailer’s solar water heater
- Two camp sockets: **50A shore** (120/240V; 30A pedestals via adapter) and **J1772**

### Should

- Leaf screens / cleanouts that are easy to service
- Clear isolation so rain path can be shut off when unwanted
- Sliding-door step: evaluate the **thin/small notch** in the restricted area; otherwise portable step

### Could

- Awning / outdoor shower rinse integration later
- Side **quick-connect** for deployable solar thermal (plumbing owns loop; exterior owns mounting/port) — [water](../../02-architecture/water.md)
- Mount point for external **weather station** ([connectivity](../connectivity/README.md))

## Design notes

- Dual fill ports (pressurized + trickle) are plumbing-side; rain is a third intake into the same fill-filtration → tank story
- Roof real estate contention: PV, thermal collector stowage, fans, heat pump exterior, rain gutters, weather station
- Swing-out under-mount step at slider is **hard** — battery under floor; notch-only candidate
- Thermal quick-connect should be convenient at camp (side wall, reachable) and capped/protected when traveling
- Hitch bike rack candidate: **QuikrStuff Mach 2** (2 e-bikes). Confirm rear-door swing with the rack tilted
- Roof also reserves a cutout for the future 48V heat pump, uncut or blanked until that unit is chosen ([heating-cooling](../heating-cooling/README.md))

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | Roof rain capture → filter → fresh tank | Eco top-up | No rain system | decided |
| 2026-10-13 | No free drill for slider step in battery zone | HV safety | ICE-van style step mounts | decided |
| 2026-10-25 | **Hitch is MVP** | Bike rack on short trips; trailer on long trips | Hitch as a later add | decided |
| 2026-10-25 | Short-trip bikes on a **QuikrStuff Mach 2** hitch rack | Keeps bikes out of the cabin | Bikes inside; trailer required for any ride | candidate |
| 2026-10-25 | Exterior **50A** shore socket plus a **J1772** socket into the **house** battery | 50A covers later 240V water heat; 30A sites use an adapter. Traction stays on the factory front port | 30A inlet as the only shore socket; J1772 into the traction pack | decided |

Detail write-ups: [decisions.md](decisions.md) · [water architecture](../../02-architecture/water.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Rain gutters / collection | | | | researching | |
| First-flush / debris screen | | | | researching | |

Full list: [products.md](products.md) · master BOM: [../../06-shopping/bom.md](../../06-shopping/bom.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Plumbing | Fill filtration into fresh tank |
| Electrical / roof layout | PV and other roof citizens |

| Depended on by | Why |
|----------------|-----|
| Plumbing / water | Rain as intake source |

## Risks & open questions

- First-flush design and when we treat rain as potable vs utility-only
- Convenience of any deployable bits vs vision rule

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [water architecture](../../02-architecture/water.md)
