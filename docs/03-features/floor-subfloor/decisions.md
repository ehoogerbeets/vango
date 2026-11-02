# Decisions — Floor & Subfloor

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

### D-01: Three-layer eco floor stack

- **Date:** 2026-10-14
- **Status:** `superseded`
- **Context:** Need insulation + stiffness + finished wear surface without drilling the battery-span floor; eco materials preferred.
- **Decision:** Prefer **1" PlantPanel X** (glue) → **¼–½" poplar plywood** (glue) → **~7 mm waterproof engineered bamboo** click-lock.
- **Why:** Plant-based insulation, light sustainable subfloor, durable water-resistant finish; glue-down respects keep-out.
- **Alternatives considered:**
  - Option A — Foam board + marine ply + vinyl
  - Option B — Thicker single-sheet subfloor (eats height / weight)
- **Consequences:** ~1.5–1.8" of standing-height budget; must validate adhesives and poplar thickness.
- **Supersedes / superseded by:** Superseded by D-02 (aluminum subfloor, sealed hemp, zero-VOC adhesive).

### D-02: Aluminum subfloor, sealed hemp, zero-VOC glue

- **Date:** 2026-11-02
- **Status:** `accepted`
- **Context:** The wood subfloor is too heavy. PlantPanel takes on water if it gets wet. Glue sits in a closed van, so it cannot off-gas. The battery-span floor still cannot be drilled. The aluminum is for stability, not a structural wood replacement.
- **Decision:** Seal the hemp with **Smart BioHemp Wood Protectant**. Float a **⅛" aluminum sheet** on the hemp with **AFM Safecoat Almighty Adhesive** (zero VOC). Finish remains **~7 mm waterproof engineered bamboo** click-lock, floating on the aluminum.
- **Why:** Drops the wood subfloor weight, keeps water out of the hemp, and keeps the glue lines from off-gassing. Glue-down still respects the keep-out.
- **Alternatives considered:**
  - Option A — ¼–½" poplar plywood subfloor (D-01)
  - Option B — Leave the hemp unsealed
  - Option C — A conventional construction adhesive
- **Consequences:** Aluminum sheet is about **1.8 lb/ft²**. Confirm the sealer does not block the adhesive, and sample the adhesive on the OEM floor coating, cork, hemp, and aluminum. Alloy, temper, and how the sheets join are still open.
- **Supersedes / superseded by:** Supersedes D-01. Hemp thickness and valley detail refined in D-03.

### D-03: Cork valley fill + ¾" PlantPanel I flat cap

- **Date:** 2026-11-02
- **Status:** `accepted`
- **Context:** OEM Sprinter floor beads are **⅜" tall**. A flat hemp board needs support in the valleys or it bridges and soft spots. PlantPanel X is stocked at **2"**; PlantPanel I at **¾"**. There is no stock ⅜" or 1" PlantPanel board. The board cuts like wood for panel sizing, but a ⅜"-tall rip strip crushed at the saw fence will not stay flush. CNC pockets in a soft ~7 lb/ft³ board will fuzz, and the rib pattern is interrupted by tie-downs and joints.
- **Decision:** Fill the valleys with **⅜" Manton Cork** facing-grade composition cork sheets, cut to segments measured on the van, glued flush with the rib tops. Cap with sealed **¾" PlantPanel I**. Then the floated **⅛" aluminum** from D-02.
- **Why:** Cork is sold at the bead height, knifes cleanly, and is denser than PlantPanel (~10–14 lb/ft³). The ¾" I board is what Hempitecture stocks for interior use. Above the rib tops the stack is about **1.15"** (¾" + ⅛" + ~7 mm).
- **Alternatives considered:**
  - Option A — CNC carve ⅜" valleys into a 1" hemp board
  - Option B — Rip ⅜" strips sideways from 2" PlantPanel X and lay them in the valleys
  - Option C — Stack thinner cork sheets (¼" + ⅛") instead of a single ⅜" sheet
- **Consequences:** Cork does not add standing height (it only fills below the rib tops). Valley lengths are not published; cargo bed is ~173–174" on the 170", but beads are segmented. Floor images without bead dimensions: Featherbuilt Sprinter 170 Planning Kit at `~/Documents/Van Go Project/Featherbuilt Sprinter 170 Planning Kit.pdf` (paid / copyrighted; not in git). Confirm Manton facing grade matches their 10–14 lb/ft³ composition data.
- **Supersedes / superseded by:** Refines the hemp layer in D-02.
