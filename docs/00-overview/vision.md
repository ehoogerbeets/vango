# Vision & Goals

> Status: `researching`  
> Last updated: 2026-10-25

## Elevator pitch

An RV in a van — not full-time vanlife. Built for weekends through entire summers: deserts, mountains, coasts, cities, and dispersed camping. About ¼–⅓ of nights with hookups; the rest autonomous and off-grid. Designed for two (tall husband + shorter wife), with an eco-minded, modern, space-efficient interior that stays convenient enough that we actually use every feature. Platform: **Mercedes e-Sprinter** LWB high roof ([ADR-0002](../05-decisions/0002-mercedes-e-sprinter-platform.md)); house systems **all-electric** ([ADR-0003](../05-decisions/0003-all-electric-house-systems.md)). Traction battery under the floor forces **wet aft / bed forward** and no mid-van floor drilling ([ADR-0005](../05-decisions/0005-traction-battery-floor-no-drill-zone.md)). Fixed high roof only — stand fully upright, no pop-top or raised-roof conversion.

## Primary goals

Ordered by priority — these are both **goals** and **design philosophies** that every feature decision should respect.

1. **Eco-friendly** — Tread lightly in materials, construction methods, and day-to-day operation.
2. **Sized for a tall person** — Standing / clearance comfort for a 6'2" occupant. A past 6'1" boat ceiling that caused constant head-cracking is explicitly *not* acceptable in retirement. **Hard requirement:** stand fully upright in the finished cabin; **no pop-top, no raised roof**.
3. **Ultra-convenient or omit it** — If a feature is awkward, we won't use it; don't install it.
4. **Complexity is allowed** — Engineering complexity is fine (software background + AI assistance); convenience and maintainability still win.
5. **Space efficiency / multi-use** — Every volume should earn its keep. Bathroom is the flagship example: toilet area + shower area + storage that reclaims unused wet-space volume and moves out of the way easily when the bath is needed (still must satisfy #3).
6. **Maintainability** — Design for easy service. Example: water filters in a spot where swaps are quick and obvious.
7. **Light weight** — Minimize build mass to preserve payload for food, people, and gear.
8. **Modern, calm interior** — Clean contemporary look; calming, beautiful colors; inviting and comfortable — not “grandpa’s RV.”

## Non-goals

- Not a permanent / full-time live-aboard dwelling.
- Must be easy to **winterize** and put away for the off-season (mostly a good-weather van).
- Winter use is occasional (e.g. ski weekends), not a primary design driver for extreme cold-weather full-time living.
- **No pop-top / no aftermarket raised roof** — platform must already allow full standing height for 6'2".
- **Overseas use does not drive design** — North America first. Europe / Australia / New Zealand shipping fantasies are nice-to-haves; may add EU/AU charging adaptability later, but not a v1 requirement.

## Success criteria

We'll know the build worked when we can:

- Spend a **long weekend off-grid without wanting for anything** (target: ~3 nights).
- Enjoy the ritual: grill or fireplace, sunset, cocktails → retire to a **really comfortable bed**.
- Next day: active outings (e-biking, hiking, museums, tours) and back before happy hour — van supports the lifestyle, not the other way around.
- Use the van comfortably across trip lengths from weekends to multi-month seasons without it feeling like a compromise dwelling.
- Walk the cabin at 6'2" without ducking or cracking a head — every day.

## Occupants (design envelope)

| Person | Role | Notes for fit |
|--------|------|----------------|
| Edwin | Primary / tall | 58, **6'2"** — ceiling, bed length, seating, shower height critical |
| Wife | Co-traveler | 60, **5'2"** — reach, step heights, shared ergonomics matter too |

Typical occupancy: **two**. A rare overnight guest uses the **settee**. There is no third mattress and no upper bunk to design.

## Bathroom vision (high level)

Three roles in one efficient footprint:

| Area | Role |
|------|------|
| Toilet | Dedicated toilet space — **low-flow marine electric-flush** + black tank |
| Shower | Dedicated shower space |
| Storage | Reclaims bath/shower volume when wet areas are not in use; swings/moves away conveniently when they are |

Detail lives in [Bathroom feature](../03-features/bathroom/README.md).

## Personas / use cases

| Scenario | Frequency | Must-haves |
|----------|-----------|------------|
| Weekender (local / regional) | Most common | Fast deploy/pack-up; comfort for 1–3 nights; off-grid OK |
| ~1 week visiting kids at university | Common | Easy highway travel; some urban parking; sleep + cook well |
| 2–3 months US & Canada national parks | Seasonal highlight | Sustained off-grid stretches; storage for longer provisioning; dispersed camping |
| Occasional winter (ski, etc.) | Rare | Basic cold tolerance; easy winterize when parked |
| Summer in Europe / AU / NZ (ship van) | Fantasy / later | **Does not drive v1 choices.** Possible later shore-power adapter work for non-NA electrical. |

## Design principles (sticky-note version)

> Eco · Tall-person fit (fixed high roof) · Convenient or cut · Complexity OK if maintainable · Multi-use space · Light · Modern & calm  
> Not full-time. Easy to winterize. An RV in a van. North America first.

## Related

- [Constraints](constraints.md)
- [Glossary](glossary.md)
