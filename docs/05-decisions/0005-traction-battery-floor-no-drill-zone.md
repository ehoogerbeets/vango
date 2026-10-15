# ADR-0005: Traction battery floor no-drill zone and layout consequences

- **Date:** 2026-10-13
- **Status:** `accepted`
- **Deciders:** Edwin
- **Tags:** van, safety, layout, plumbing, floor, exterior

## Context

The Mercedes e-Sprinter’s **drive (traction) battery** sits under the floor from roughly the **B-pillar to the rear axle**. Drilling into that floor risks catastrophic damage to the HV battery. This is a hard physical/safety constraint that forces an atypical camper layout compared with common ICE van builds (rear garage + bed over the axle).

## Decision

### No-drill / restricted floor zone

| Rule | Detail |
|------|--------|
| Zone | Under-floor traction battery area: **B-pillar → rear axle** |
| Drilling | **No drilling** in the floor in that zone (for mounts, plumbing penetrations, etc.) |
| Tiny exceptions | Only the **very small** OEM-safe drillable spots exist there — not useful for tanks or major mounts |
| Drill direction (anywhere near battery) | If a permitted hole is ever used, **drill from the underside upward** so you can see you are not entering the battery pack |
| Furniture / cabinets in zone | **Do not** through-bolt to the floor in the battery zone |
| Allowed floor attachments in zone | Only to **existing OEM tie-down points** (pre-drilled). Layout/cabinetry **must be designed around those tie-down locations** |
| Under-mount tanks in battery zone | **Forbidden** — no room under the pack, and no legal path to drill dump/fill penetrations through that floor |
| Under-mount tanks allowed | **Behind the rear axle only** |
| Grey/black dump line floor penetrations | **Behind the rear axle only** |

### Layout consequence (accepted direction)

Because wet drains need short gravity runs to aft under-mount tanks and aft floor penetrations:

- **Shower** and **kitchen sink** (wet galley) belong toward the **rear** of the van
- **Bed** moves **forward** relative to the common “rear garage + bed over garage” pattern
- We **reject** the typical rear-garage / platform-bed-over-garage primary layout for this platform

### Side step

A swing-out / under-mount **entry step** at the sliding door is difficult because that area overlaps the no-drill / battery zone. There may be a **very thin/small notch** in the restricted area where a step *might* mount — treat as a constrained research item, not a free-for-all drill zone.

## Why

- HV battery safety — non-negotiable
- Under-mount tanks and sewer penetrations are incompatible with the battery sandwich
- Gravity drainage to aft tanks implies wet core aft → bed forward
- Tie-downs are the only honest structural attach points on that floor span

## Alternatives considered

### Alternative A — In-cabin tanks over the battery floor (no under-mount)

- Pros: Avoids under-vehicle packaging behind axle
- Cons: Eats interior volume/payload geometry; still need dump plumbing routes; may still want some aft penetration strategy
- Why not (for now): Direction is under-mount **aft of rear axle**; interior tanks remain a fallback if aft packaging fails

### Alternative B — Classic rear garage + bed over garage, galley forward

- Pros: Familiar vanlife pattern; easy bike/gear loading
- Cons: Long drain runs or illegal penetrations over the battery; fights gravity to aft tanks
- Why not: Incompatible with dump penetration + under-mount tank rules

### Alternative C — Drill carefully through battery-zone floor anyway

- Pros: Layout freedom
- Cons: Unacceptable HV risk
- Why not: Explicitly forbidden

## Consequences

### Positive

- Clear keep-out map for fabricators and future-us
- Layout problem is framed early: **wet aft, sleep forward**
- Cabinetry engineering centers on **tie-down grid** in the mid/aft battery span

### Negative / trade-offs

- Loses the popular rear garage geometry — gear storage must be redesigned (side, forward, or other)
- All under-vehicle water hardware crowded **behind the rear axle** (ground clearance, departure angle, crash/stone risk)
- Sliding-door step may be compromised or custom/notch-only
- Long house systems (electrical runs, etc.) must respect floor keep-out for penetrations too

### Follow-ups

- [ ] Map exact B-pillar → axle keep-out and photograph/measure OEM tie-down grid on a real van
- [ ] Confirm any OEM-documented drill zones / service docs for e-Sprinter floor
- [ ] Design aft under-mount tank package (fresh/grey/black as applicable) + penetration plate behind axle
- [ ] Layout v1 sketch: shower + galley aft, bed forward, storage strategy without rear garage
- [ ] Research sliding-door step in the thin notch; fallback = portable step
- [ ] Update floor build so “floating” cabinetry lands on tie-downs, not random lag screws into battery floor

## Links

- Related docs: [constraints](../00-overview/constraints.md), [layout](../02-architecture/layout.md), [water](../02-architecture/water.md), [ADR-0002](0002-mercedes-e-sprinter-platform.md)
- Related features: floor-subfloor, bathroom, galley, bed-sleep, storage, exterior, plumbing
- Supersedes: —
- Superseded by: —
