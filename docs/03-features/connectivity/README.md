# Feature: Connectivity

> Status: `researching`  
> Priority: `P2`  
> Jira Epic: _TBD (build phase)_  
> Last updated: 2026-10-15

## Summary

Van telemetry and control — at minimum, an **app** to read **fresh / grey / black tank levels** and to **open/close electric ball valves** on the grey and black dump paths ([water](../../02-architecture/water.md)). Post-MVP: outdoor weather station + interior **RuuviTag Pro** sensors into OpenVan.

## Goals

- Convenient dump and tank awareness without crawling under the van every time
- Reliable enough for travel use; fail-safe when offline/power-loss (with plumbing)
- Align with “ultra-convenient or omit” — if the app path is flaky, design manual backup
- Optional climate awareness: outside weather + inside zones (temp / humidity / pressure)

## Non-goals

- Full smart-home sprawl for its own sake
- Cloud dependency that bricks dumping when internet is down (prefer local control)

## Requirements

### Must

- App (or equivalent UI) shows **level** for fresh, grey, black
- App can **open/close** grey dump electric ball valve
- App can **open/close** black dump electric ball valve
- Works with plumbing sensors/valves ([plumbing](../plumbing/README.md))

### Should

- Local/offline control (van Wi‑Fi / Bluetooth / similar) so a dump station works without cell service
- Manual mechanical/electrical override documented and reachable

### Could (post-MVP)

- Alerts (tank high/low)
- Broader house electrical / climate telemetry
- **External weather station** — temperature, pressure, wind, humidity
- **RuuviTag Pro** sensors inside — temperature, humidity, pressure (BLE → OpenVan / Pi brain)
- Starlink, weBoost, mesh Wi‑Fi ([requirements](../../01-van/requirements.md))

## Design notes

- Security: don’t expose dump valves on the open internet without strong auth
- Power: valves and sensors need house DC even when “camping quiet”
- RuuviTags are battery BLE beacons — Pi/OpenVan needs a BLE radio in range; place tags in cabin zones that matter (sleep, bath, galley)
- Weather station mount must coexist with roof rack / PV / fans ([exterior](../exterior/README.md))

## Decisions

| Date | Decision | Why | Alternatives rejected | Status |
|------|----------|-----|----------------------|--------|
| 2026-10-13 | App control for grey/black dump valves + tank levels | Convenience | Manual-only dump/levels | decided |
| 2026-10-15 | Prefer RuuviTag Pro for interior env sensing | Proven BLE env tags; low power | Wired DHT-only sprawl | proposed |

## Product / brand choices

| Item | Brand / model | Est. cost | Why | Status | Link |
|------|---------------|-----------|-----|--------|------|
| Controller / hub | Raspberry Pi (candidate) | | OpenVan brain | researching | |
| App / UI | OpenVan + iPad | | | researching | |
| Interior env | RuuviTag Pro | | Temp / humidity / pressure | preferred | [products](products.md) |
| Weather station | TBD | | Ext. temp / pressure / wind / humidity | researching | [products](products.md) |

Full list: [products.md](products.md)

## Dependencies

| Depends on | Why |
|------------|-----|
| Plumbing | Sensors + electric ball valves |
| Electrical | Power for controls |

| Depended on by | Why |
|----------------|-----|
| Plumbing UX | Dump / monitor experience |

## Risks & open questions

- Fail-safe valve state on power loss
- Auth / remote access threat model

## Stories (future Jira)

See [stories.md](stories.md).

## References

- [water architecture](../../02-architecture/water.md)
