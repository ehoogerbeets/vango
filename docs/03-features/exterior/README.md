# Feature: Exterior & Awning

> Status: `researching`  
> Priority: `P1`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-13

## Summary

Outside shell integrations: **roof rainwater capture**, aft under-mount tank packaging visibility/protection, and a constrained **sliding-door step** story under [ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md).

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

### Should

- Leaf screens / cleanouts that are easy to service
- Clear isolation so rain path can be shut off when unwanted
- Sliding-door step: evaluate the **thin/small notch** in the restricted area; otherwise portable step

### Could

- Awning / outdoor shower rinse integration later

## Design notes

- Dual fill ports (pressurized + trickle) are plumbing-side; rain is a third intake into the same fill-filtration → tank story
- Roof real estate contention: PV, thermal collector stowage, fans, heat pump exterior, rain gutters
- Swing-out under-mount step at slider is **hard** — battery under floor; notch-only candidate

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | Roof rain capture → filter → fresh tank | Eco top-up | No rain system | decided |
| 2026-10-13 | No free drill for slider step in battery zone | HV safety | ICE-van style step mounts | decided |

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
