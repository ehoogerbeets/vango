# Decisions — Bed / Sleep

Feature-scoped decision log. Promote to an [ADR](../../05-decisions/README.md) if the choice affects multiple features.

## Template for each decision

### D-{{NN}}: {{Title}}

- **Date:**
- **Status:** `proposed` | `accepted` | `superseded` | `rejected`
- **Context:**
- **Decision:**
- **Why:**
- **Alternatives considered:**
  - Option A —
  - Option B —
- **Consequences:**
- **Supersedes / superseded by:**

---

## Log

### D-01: Elevator bed over settee — lift for day, settle for sleep

- **Date:** 2026-10-25
- **Status:** `proposed`
- **Context:** Need a comfortable bed for two without permanently consuming lounge / standing space. Daytime living wants the bed out of the way; night sleeping must not rock with van motion or wind.
- **Decision:** Build an **automatic (push-button) elevator bed** that raises toward the ceiling by day and lowers onto the **settee / chair-back structure** at night so sleep loads go into furniture, not the lift mechanism.
- **Why:**
  - Matches vision multi-use + convenience (button, not wrestling cushions)
  - Industry kits explicitly say hanging belts/actuators are for **moving** the platform — sleepers need a **secondary support** (cabinets / ledges / settee backs)
  - Eliminates swing / bounce when turning over or when the van is buffeted
- **Alternatives considered:**
  - Option A — Fixed bed (wastes daytime lounge)
  - Option B — Manual fold / rock-and-roll only (fails “ultra-convenient”)
  - Option C — Sleep hanging only on straps/actuators (unstable; unsafe; against kit guidance)
- **Consequences:** Settee and chair backs become structural sleep supports; lift system sized for platform + mattress + bedding only; ceiling/wall mounts must respect battery-zone floor keep-out (prefer walls / roof structure / tie-downs).
- **Supersedes / superseded by:** —

### D-02: Lift mechanism class — ranked shortlist

- **Date:** 2026-10-25
- **Status:** `researching` (shortlist; not purchased)
- **Context:** Need push-button raise/lower. Evaluate on **weight** (heaviest priority), ease-of-use, repair/replacement, reliability — see [README scoring](README.md#evaluation-criteria-our-priorities).
- **Decision:** Shortlist **C (synced linear actuators)** or **A (nylon strap kit)**. Prefer C when minimizing mass; prefer A for simplest appliance-like kit. **Defer B (HappiJac)** unless payload opens up. Eliminate E/F; treat D as last-resort DIY only.
- **Why:** Weight-biased weighted scores: C **4.40**, A **4.15**, B **3.20**. B wins raw reliability but loses the payload contest; settle-on-settee already covers night structural needs.
- **Alternatives considered:** Full table in README.
- **Consequences:** Budget lift mass ~40–110 lb class (not 200+); plan actuator sync *or* strap service; manual lower still required.
- **Supersedes / superseded by:** —

### D-03: Actuator geometry + optional guest mid-height

- **Date:** 2026-10-25
- **Status:** `proposed`
- **Context:** Clarify how actuators move the bed; consider lowering halfway so the settee can be a temporary guest bed.
- **Decision:** Prefer **hang-from-above** (or wall-track) geometry so the lounge stays clear. Treat **guest mid-height** as an optional third position: settee sleeper below; platform locked mid-travel with **mechanical pins/ledges** (not motor-only). Upper-bunk sleeping on the half-down platform is out of scope unless separately rated. Primary couple sleep remains fully down on settee backs.
- **Why:** Push-from-below columns fight settee guest use; hang-from-above matches elevator + lounge; actuators/HappiJac stop-any-height well; straps can mid-stop but need latches for under-bed safety.
- **Alternatives considered:**
  - Option A — Push-from-below through settee (possible, harder guest packaging)
  - Option B — Guest sleeps on hanging upper only (rejected without secondary supports)
- **Consequences:** Control box needs a mid preset or easy jog-to-height; add latch design to settee/walls; verify headroom for settee guest under mid platform.
- **Supersedes / superseded by:** —

### D-04: N–S queen-class, thin latex, light “ceiling” platform, unmade stow

- **Date:** 2026-10-25
- **Status:** `proposed`
- **Context:** Tall sleeper needs length along the van; raised bed steals headroom; payload favors ultra-light deck; user hates making the bed for looks.
- **Decision:** Sleep **north–south**. Target **queen-class** width (~60") if measured clear width allows; else custom/short queen. Mattress **~3" (max 4")**, prefer **natural latex**. Platform: **breathable CF tube frame + slats** (DragonPlate-class), not a sealed sandwich—porous/perforated ceiling skin + lights. Elevator must **stow bedding unmade**. Design for sleepers **220 + 210 lb** (~700 lb with dynamic margin).
- **Why:** E–W won’t fit; thin latex + airflow fights moisture; sealed decks trap sweat; CF 1" slats need short spans / many sticks; unmade stow is a primary convenience goal.
- **Alternatives considered:**
  - Option A — Full residential king (too wide)
  - Option B — Thick hybrid mattress (steals headroom)
  - Option C — Sealed honeycomb “ceiling” under mattress (moisture risk)
- **Consequences:** Prefer 2×1" side rails + center spine + 1×1" slats @ ~2.5–3"; mid-span tees via pockets/plates (not cube-only); coupon-test slat span; bedding retention + perforated underside skin.
- **Supersedes / superseded by:** —
