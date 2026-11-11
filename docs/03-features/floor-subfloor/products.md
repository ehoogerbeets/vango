# Products — Floor & Subfloor

Purchase and brand decisions for this feature. Mirror important rows into the [master BOM](../../06-shopping/bom.md).

Preferred eco stack from [requirements](../../01-van/requirements.md#material-preferences-eco).

## Active choices

| SKU / item | Brand | Model | Qty | Est. unit $ | Est. total $ | Why this one | Vendor | Status | URL |
|------------|-------|-------|-----|-------------|--------------|--------------|--------|--------|-----|
| Valley fill | Manton Cork | Premium facing-grade cork sheet, **⅜"** | TBD | | | OEM floor beads are **⅜" tall**. Cut strips into the valleys, flush with the rib tops | Manton Cork | preferred | https://www.mantoncork.com/cork_sheets/3-8-thick-natural-cork-sheets/ |
| Floor insulation (cap) | Hempitecture | PlantPanel I, **¾"** | TBD | | | Stock interior board. Flat sheet over the cork and rib tops. Sealed before close-in | Hempitecture | preferred | |
| Hemp sealer | Smart BioHemp | Wood Protectant (plant-based wood sealer) | TBD | | | PlantPanel takes on water; seal it before it is closed in | Smart BioHemp | preferred | https://smartbiohemp.com/products/smart-biohemp-wood-protectant |
| Subfloor (stability) | — | Aluminum sheet, **⅛"** | TBD | | | Floated on adhesive for stiffness. A wood subfloor is too heavy. About **1.8 lb/ft²** | | preferred | |
| Adhesive | AFM Safecoat | Almighty Adhesive | TBD | | | Zero-VOC glue for cork, hemp, and aluminum joints | AFM | preferred | https://afmsafecoat.com/products/adhesives-caulk/safecoat-almighty-adhesive |
| Finish floor | AquaGuard (candidate) | Carbonized Stranded Waterproof Engineered Bamboo, **~7 mm** click-lock | TBD | | | Looks + wear + water resistance | | preferred | |

## Stack (preferred)

```
van metal floor (OEM beads ~⅜" tall)
  → ⅜" cork strips in the valleys, flush with rib tops (AFM Safecoat Almighty Adhesive)
  → ¾" PlantPanel I flat cap over cork + rib tops, sealed (Smart BioHemp Wood Protectant)
  → zero-VOC adhesive (same)
  → ⅛" aluminum sheet, floated for stability
  → ~7 mm waterproof engineered bamboo click-lock
```

The click-lock floor floats. It is not a glue line. The aluminum is floated on adhesive, not screwed into the battery-zone floor.

Approx. build-up **above the rib tops:** **~1.15"** (¾" hemp + ⅛" aluminum + ~7 mm bamboo). The cork fills the valleys only and does not add height. Must fit the standing-height budget with the ceiling.

## Rejected / not chosen

| Item | Contender | Why rejected | Date |
|------|-----------|--------------|------|
| Subfloor | Poplar plywood, ¼–½" | Too heavy for the subfloor | 2026-11-02 |
| Valley fill | CNC carve ⅜" pockets into a 1" hemp board | Soft board (~7 lb/ft³); ribs are not a repeating cut; a proud spot rocks the whole panel | 2026-11-02 |
| Valley fill | Rip ⅜" strips sideways from 2" PlantPanel X | Full panels cut like wood; a ⅜"-tall stick crushes and will not stay flush | 2026-11-02 |
| Floor cap | PlantPanel X, 1" | Not a stock thickness. Catalog is 2" X and ¾" I | 2026-11-02 |

## Notes

- Glue-down layers avoid mid-van drill into the battery keep-out ([ADR-0005](../../05-decisions/0005-traction-battery-floor-no-drill-zone.md)).
- OEM floor beads are **⅜" tall**. Cargo bed length on the 170" is about **173–174"**, but the valleys are interrupted by tie-down cups, panel joints, and wheelhouses. Cut cork into segments measured on the van. Floor images (no bead dimensions): Featherbuilt Sprinter 170 Planning Kit at `~/Documents/Van Go Project/Featherbuilt Sprinter 170 Planning Kit.pdf` (paid / copyrighted; not in git). Floor / battery keep-out rules: [Supplemental BEG for eSprinter (Edition 2023-8)](https://www.mbvans.com/content/dam/mb-vans/us/upfitter/08302023_eSprinter_907_BEG_Edition2023-8_en.pdf) (mbvans.com; copyrighted — link only).
- Manton ⅜" facing-grade cork is composition cork with a polyurethane binder. Their roll/sheet data lists density **10–14 lb/ft³**, **30–45%** compression at 100 psi, and **>75%** recovery. Unroll and flatten before cutting. Confirm with Manton that this facing grade is the 10–14 lb/ft³ composition line.
- PlantPanel cuts like wood for panel sizing (circular saw, table saw, Bahco insulation saw). That does not make a thin rip strip a good valley fill.
- PlantPanel is susceptible if it gets wet. Seal the board, including cut edges, before the aluminum and the finish floor close it in. Confirm the sealer still lets the adhesive bond, or keep sealer off the glue faces.
- Almighty Adhesive is the zero-VOC candidate for the buried joints (van floor / cork / hemp / aluminum). The AFM sheet lists **0% volatile by volume and by weight**, HAPs at zero, and no off-gassing expected at room temperature. The hot VOC number is under 35 g/L near 240°F. It is listed for subfloor and for metal. Sample it on the OEM floor coating, cork, hemp, and aluminum.
- ⅛" aluminum sheet is about **1.8 lb/ft²**. It is for stability, floated on adhesive. Alloy and temper are still open. Join sheets without screws into the battery-zone floor.
- Mirror the floor hemp into [insulation products](../insulation/products.md). Walls and ceiling may use a different PlantPanel thickness.
