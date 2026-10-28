# Feature: Exterior & Awning

> Status: `researching`  
> Priority: `P1`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-28

## Summary

Outside shell integrations: **aftermarket trailer hitch**, a **perimeter roof rack** that carries a continuous solar canopy over the Webasto and MaxxFan, **roof rainwater capture**, aft under-mount tank packaging, a van-wall socket for the trailer, and a constrained **sliding-door step** under [ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md).

## Goals

- Capture rain from the roof for filtered top-up of the fresh tank (eco)
- Carry a **flat solar canopy** over the ~160" usable roof, with high-bar risers over the Webasto shroud and a solid front fairing
- Coexist with the **Webasto Cool Top Trail**, the **MaxxFan Mini Plus**, deployable solar thermal, rain capture, and other roof gear
- Convenient enough that rain capture actually gets used / maintained
- Safe, convenient entry at the sliding door despite battery-zone keep-out

## Non-goals

- Using untreated roof runoff as drinking water without filtration
- Overseas ferry/height rules driving v1 (beyond e-Sprinter envelope)
- Free drilling under the sliding door through the traction-battery floor span

## Requirements

### Must

- Rain collection path from roof → debris / first-flush strategy (TBD) → plumbing **fill manifold → GoBluTech AR3** → fresh tank
- Not compromise standing-height / roof stack carelessly
- Light-weight where possible
- Respect battery-zone **no-drill** rules for any under-vehicle hardware ([ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md))
- Aft under-mount tanks/plumbing protected for road debris / clearance
- **Trailer hitch, shocks, and exterior paint are shop work, and they happen before the rest of the build.** The hitch is needed on the first trip: bikes on a hitch rack for short trips, the gear trailer for long ones ([storage](../storage/README.md)). Shock spec is still open. Paint uses one palette with the interior, set by the designer before the van goes to the shop. A front bumper and winch are aspirational and may never be built ([requirements](../../01-van/requirements.md))
- Van-wall socket for the trailer: DC-DC surplus charge into the house bank, and the warm-tank hoses from the trailer’s solar water heater
- Two camp sockets: **50A shore** (120/240V; 30A pedestals via adapter) and **J1772**

### Should

- Leaf screens / cleanouts that are easy to service
- Clear isolation so rain path can be shut off when unwanted
- Sliding-door step: evaluate the **thin/small notch** in the restricted area; otherwise portable step

### Could

- Outdoor sprinkle is the bathroom handheld on a hook at the **back**, not a second shower. Ground platform, not a body step. Awning still later
- Side **quick-connect** for deployable solar thermal (plumbing owns loop; exterior owns mounting/port) — [water](../../02-architecture/water.md)
- Mount point for external **weather station** ([connectivity](../connectivity/README.md))

## Design notes

- Dual fill ports (pressurized + trickle) are plumbing-side; rain is a third intake into the same fill-filtration → tank story
- Roof real estate contention: PV, thermal collector stowage, fans, heat pump exterior, rain gutters, weather station
- Swing-out under-mount step at slider is **hard** — battery under floor; notch-only candidate
- Thermal quick-connect should be convenient at camp (side wall, reachable) and capped/protected when traveling
- Hitch bike rack candidate: **QuikrStuff Mach 2** (2 e-bikes). Confirm rear-door swing with the rack tilted
- Roof reserves a blanked **14" × 14"** cutout for the **Webasto Cool Top Trail 48V** until that post-MVP install ([heating-cooling](../heating-cooling/README.md)). A second **14" × 14"** cutout takes the **MaxxAir MaxxFan Mini Plus**; crossbars must stay clear of the fan’s rear horizontal exhaust louvers
- **Solar canopy rack** (track-mounted perimeter, 170" high roof). Two candidates; either needs a solid **front fairing** from the top of the windshield to the leading edge of the array so highway air cannot lift the canopy:
  - **Orion Van Gear Sprinter Stealth+** — side rails ~5.4" off the track; flush crossbars only ~1.5–2.5" over the roof ribs. Needs the **Orion Roof Rack Riser Bar Kit (+4" to +5")** where the rack overlaps the Webasto
  - **Vann Camp Roof Rack (170" WB, high roof)** — low-profile perimeter. Needs custom high-bar crossbar offsets over the AC shroud
- **Stacking at the AC bridge** (roof sheet → fan dome **4.1"** → Webasto shroud **8.8"** → panel underside **9.5–10.0"**): about **5.4–5.9"** of plenum over the fan and **0.7–1.2"** of breathing gap over the Webasto top exhaust. The Webasto also needs a **4"** clear intake perimeter. Full height table: [climate](../../02-architecture/climate.md). Dual-MPPT wiring: [electrical](../../02-architecture/electrical.md)

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | Roof rain capture → filter → fresh tank | Eco top-up | No rain system | decided |
| 2026-10-25 | That rain is **drinking water after fill filters and UV** | Same standard as hose water | Utility-only rain tank | decided |
| 2026-10-27 | Rain joins the **AR3 fill manifold** | One purification path with shore and draft fills | A rain-only second filter train | decided |
| 2026-10-13 | No free drill for slider step in battery zone | HV safety | ICE-van style step mounts | decided |
| 2026-10-25 | **Hitch is MVP** | Bike rack on short trips; trailer on long trips | Hitch as a later add | decided |
| 2026-10-25 | Shop installs **hitch, shocks, exterior paint**. Edwin builds the rest | Split the jobs that need a shop | A shop conversion; DIY hitch and paint | decided |
| 2026-10-27 | **Shocks and exterior paint are MVP**, and the shop does them before the conversion | They have to happen before the rest of the build | Leaving them until the van is otherwise finished | decided |
| 2026-10-27 | **Winch and its bumper are aspirational** | We may never need them. Not part of finishing the van | Treating the winch as a planned shop install | decided |
| 2026-10-25 | Short-trip bikes on a **QuikrStuff Mach 2** hitch rack | Keeps bikes out of the cabin | Bikes inside; trailer required for any ride | candidate |
| 2026-10-25 | Exterior **50A** shore socket plus a **J1772** socket into the **house** battery | 50A covers later 240V water heat; 30A sites use an adapter. Traction stays on the factory front port | 30A inlet as the only shore socket; J1772 into the traction pack | decided |
| 2026-10-28 | Continuous solar canopy on a perimeter rack, with **high-bar risers** over the Webasto and a **front fairing** | Flat array over the full ~160" roof without choking the AC exhaust | Flush-only rack; panels that stop short of the heat pump | decided |
| 2026-10-28 | Rack shortlist: **Orion Stealth+** (with riser kit) or **Vann Camp 170" high-roof** (with custom high bars) | Both are track-mounted perimeter racks that can clear the 8.8" shroud | A rack that cannot clear the Webasto | researching |

Detail write-ups: [decisions.md](decisions.md) · [water architecture](../../02-architecture/water.md) · [climate](../../02-architecture/climate.md)

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Roof rack | Orion Van Gear | Sprinter Stealth+ + riser bar kit | Track-mounted; +4–5" risers over the Webasto | researching | [products](products.md) |
| Roof rack (alt) | Vann Camp | 170" WB high-roof rack | Low-profile perimeter; needs custom high bars over the AC | researching | [products](products.md) |
| Front fairing | | Solid windshield-to-array deflector | Stops highway lift under the canopy | preferred | |
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

- Rain is drinking water after the **GoBluTech AR3**. First-flush / leaf screen before the fill manifold is still open
- Convenience of any deployable bits vs vision rule

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [water architecture](../../02-architecture/water.md)
