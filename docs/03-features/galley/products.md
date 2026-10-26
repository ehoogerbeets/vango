# Products — Galley

Purchase and brand decisions for this feature. Mirror important rows into the [master BOM](../../06-shopping/bom.md).

Energy math for fridge candidates: [daily energy budget](../../02-architecture/daily-energy-budget.md).

## Active choices

| SKU / item | Brand | Model | Qty | Est. unit $ | Est. total $ | Why this one | Vendor | Status | URL |
|------------|-------|-------|-----|-------------|--------------|--------------|--------|--------|-----|
| Fridge / freezer | GE Profile | **PPV10R5YRSS** 9.8 cu ft 12V top-freezer | 1 | ~$1,900 | | Medium 12V; reversible hinges; 60×23.5×25.8 in; 13.5 A nameplate | GE | candidate | https://www.geappliances.com/appliance/GE-Profile-9-8-cu-ft-12V-DC-Top-Freezer-Refrigerator-PPV10R5YRSS |
| Fridge / freezer | Furrion Arctic | **10.7 cu ft** 12V dual-swing + bottom freezer drawer | 1 | | | True dual-swing; 59⅞×23⅝×26³⁄₁₆ in; ~82–125 Ah/day @ 12V (75–95°F) | Furrion / Lippert | candidate | https://furrion.com/products/107-cuft-12v-french-door-refrigerator-french-door-10-7-cf-12v-refrigerator |
| Induction cooktop | | 2-burner 120V | 1 | | | | | researching | |
| Oven / air-fryer | | Ninja Flip class 120V | 1 | | | | | researching | |
| Microwave | | Small 120V | 1 | | | | | researching | |
| Coffee maker | | Plumbed PEX feed | 1 | | | | | researching | |

## Rejected / not chosen

| Item | Contender | Why rejected | Date |
|------|-----------|--------------|------|
| | | | |

## Notes

- Both fridge candidates are **12V DC** → feed from house **48V** via DC-DC (see electrical architecture). Updates ADR-0004 “48V fridge” assumption.
- Furrion publishes average **3.4 A @ 75°F** / **5.2 A @ 95°F** ([spec CCD-0008148](https://lci-support-doc.s3.amazonaws.com/furrion_refrigeration/specs/ccd-0008148.pdf)). GE publishes **13.5 A** nameplate only — daily Ah needs logging or third-party tests.
- Prefer dual-swing if layout needs door opening either side; GE is reversible (pick hinge side), not simultaneous dual-swing.
- Weight logged in [payload budget](../../02-architecture/weight-and-balance.md): Furrion **139 lb**, GE class **~119 lb**.
