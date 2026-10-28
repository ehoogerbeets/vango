# Products — Electrical System

Purchase and brand decisions for this feature. Mirror important rows into the [master BOM](../../06-shopping/bom.md).

## Active choices

| SKU / item | Brand | Model | Qty | Est. unit $ | Est. total $ | Why this one | Vendor | Status | URL |
|------------|-------|-------|-----|-------------|--------------|--------------|--------|--------|-----|
| Cabin lights | | **12V** puck and ambient | TBD | | | Travel-hardened 12V fixtures, off a 48V→12V DC-DC | | preferred | |
| MPPT #1 | | High-voltage input, 48V battery out | 1 | | | Main canopy series string (Voc about 72–144 V). Charge Vmp into the bank about **58–65 V** | | researching | |
| MPPT #2 | Victron (candidate) | SmartSolar **100/20** class | 1 | | | Isolated side-channel N-type string (Voc about 90–100 V) so Webasto shade never throttles Zone 1 | | researching | |
| Main canopy panels | | Residential-grade 12V or 24V, series string | TBD | | | Fill the clear ~115.9" runway ahead/aft of the Webasto | | researching | |
| Side-channel panels | Renogy / BougeRV (candidates) | Narrow N-type, Voc ≈ 45–50 V each | 2 | | | Series pair beside the Webasto shroud | | researching | |

## Rejected / not chosen

| Item | Contender | Why rejected | Date |
|------|-----------|--------------|------|
| Cabin lights | Native 48V LEDs | Travel-hardened puck and ambient fixtures are 12V | 2026-10-26 |
| Single MPPT for the whole roof | One controller for main + side panels | Shade on the Webasto side gaps would throttle the main runway string | 2026-10-28 |

## Notes

- Inverter has to cover a **3,000 W** induction cooktop, a **1,500 W** oven circuit, a **1,500 W** coffee maker, and an occasional **1,800 W** hair dryer. The **Webasto** heat pump is on **48V DC** and does not size the inverter. The sink heater and one burner may still run together; a shower waits. Simultaneous use of the big nameplates is not decided.
- A **240V** feed from the house inverter into a portable EVSE at **3 kW max**, plugged into the Mercedes charge port when the house bank is full, is **aspirational**. It does not size the inverter that finishes the van.
- House battery kWh is not locked. **12–15 kWh** (~240–300 lb) is only the payload ceiling. See the [daily energy budget](../../02-architecture/daily-energy-budget.md) and the [payload tally](../../02-architecture/weight-and-balance.md).
- Dual-MPPT canopy layout and rack stack: [electrical architecture](../../02-architecture/electrical.md) · [exterior](../exterior/README.md).
