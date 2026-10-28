# Products — Galley

Purchase and brand decisions for this feature. Mirror important rows into the [master BOM](../../06-shopping/bom.md).

Energy math for fridge candidates: [daily energy budget](../../02-architecture/daily-energy-budget.md).

## Active choices

| SKU / item | Brand | Model | Qty | Est. unit $ | Est. total $ | Why this one | Vendor | Status | URL |
|------------|-------|-------|-----|-------------|--------------|--------------|--------|--------|-----|
| Fridge / freezer | Furrion Arctic | **10.7 cu ft** 12V dual-swing + bottom freezer drawer | 1 | | | Door opens from either side; 59⅞×23⅝×26³⁄₁₆ in; ~82–125 Ah/day @ 12V (75–95°F); 139 lb | Furrion / Lippert | preferred | https://furrion.com/products/107-cuft-12v-french-door-refrigerator-french-door-10-7-cf-12v-refrigerator |
| Induction cooktop | | 2-burner 120V | 1 | | | | | researching | |
| Oven / air-fryer | | Ninja Flip class 120V | 1 | | | | | researching | |
| Microwave | | Small 120V | 1 | | | | | researching | |
| Coffee maker | Keurig or Nespresso | **Keurig Mini** or a Nespresso pod machine | 1 | | | Plumbed PEX feed; short 120V heat cycle | | preferred | |
| Countertop | Paperstone | Recycled-paper solid surface | 1 | | | Eco counter; induction inset and sink cutout | | preferred | https://paperstoneproducts.com/products/ |

## Rejected / not chosen

| Item | Contender | Why rejected | Date |
|------|-----------|--------------|------|
| Fridge / freezer | GE Profile PPV10R5YRSS 9.8 cu ft | Reversible hinge, not dual-swing. About 20 lb lighter, and we still picked the door that opens from either side | 2026-10-27 |

## Notes

- The Furrion is **12V DC**, fed from the house **48V** bank via DC-DC. ADR-0004’s original 48V fridge line is amended.
- Furrion publishes average **3.4 A @ 75°F** / **5.2 A @ 95°F** ([spec CCD-0008148](https://lci-support-doc.s3.amazonaws.com/furrion_refrigeration/specs/ccd-0008148.pdf)).
- Weight logged in [payload budget](../../02-architecture/weight-and-balance.md): **139 lb**.
