# Tesla Energy (tesla-energy)

Tesla Energy is Tesla's solar generation and battery storage business unit, encompassing residential Powerwall, utility-scale Megapack, retrofit solar panels, and the Solar Roof. The Fleet API exposes `energy_sites` endpoints that let partners and owners read live power, calendar history, and site info, and write backup reserve, operation mode, storm mode, time-of-use settings, and off-grid vehicle charging reserve — the same control surface that powers the Tesla app, Autobidder, and Tesla Electric (Texas VPP).

**APIs.json:** [apis.yml](apis.yml)

**Portal:** [https://developer.tesla.com/](https://developer.tesla.com/)
**Energy product portal:** [https://www.tesla.com/energy](https://www.tesla.com/energy)
**Energy endpoints documentation:** [https://developer.tesla.com/docs/fleet-api/endpoints/energy](https://developer.tesla.com/docs/fleet-api/endpoints/energy)

## Tags

Energy, Clean Energy, Solar, Battery Storage, Powerwall, Megapack, Solar Roof, Virtual Power Plant, IoT, Grid Services, Home Energy, Utility Scale

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Products

| Product | Customer | Capacity / Power |
|---|---|---|
| Powerwall 3 | Residential | 13.5 kWh, 11.5 kW continuous (integrated inverter); stackable to 10 units |
| Megapack 2XL | Utility / IPP / commercial | Up to 3.9 MWh per unit, containerized DC architecture |
| Solar Roof | Residential | Integrated solar shingles, paired with Powerwall and Tesla Solar Inverter |
| Solar Panels | Residential | Retrofit photovoltaic panels paired with Tesla Solar Inverter |
| Tesla Solar Inverter | Residential | String inverter with cellular connectivity and OTA updates |
| Autobidder | Utility / IPP | Real-time energy trading and dispatch software for storage assets |
| Tesla Electric | Residential (Texas) | Retail electricity provider with VPP participation for Powerwall owners |

## APIs

### Tesla Fleet Energy API

The `energy_sites` surface of the Tesla Fleet API. Read access (`energy_device_data` scope) for products, site info, live status, calendar history, and programs; write access (`energy_cmds` scope) for backup reserve, operation mode, storm mode, time-of-use settings, and off-grid vehicle charging reserve.

**Human URL:** [https://developer.tesla.com/docs/fleet-api/endpoints/energy](https://developer.tesla.com/docs/fleet-api/endpoints/energy)
**Base URL:** `https://fleet-api.prd.na.vn.cloud.tesla.com/api/1`

- [OpenAPI](openapi/tesla-energy-fleet-api-openapi.yml)
- [JSON Schema — Energy Site](json-schema/tesla-energy-site-schema.json)
- [JSON Schema — Live Status](json-schema/tesla-energy-live-status-schema.json)
- [JSON-LD context](json-ld/tesla-energy-context.jsonld)
- [Example — Site Info](examples/tesla-energy-site-info-example.json)
- [Example — Live Status](examples/tesla-energy-live-status-example.json)
- [Spectral rules](rules/tesla-energy-rules.yml)
- [Vocabulary](vocabulary/tesla-energy-vocabulary.yml)

#### Naftiko capabilities

| Capability | Scope | Surface |
|---|---|---|
| [Sites (read)](capabilities/fleet-energy-sites.yaml) | `energy_device_data` | `/products`, `/energy_sites/{id}/site_info`, `/live_status`, `/calendar_history`, `/programs` |
| [Backup Reserve](capabilities/fleet-energy-backup-reserve.yaml) | `energy_cmds` | `/energy_sites/{id}/backup` |
| [Operation Mode](capabilities/fleet-energy-operation.yaml) | `energy_cmds` | `/energy_sites/{id}/operation` |
| [Storm Mode](capabilities/fleet-energy-storm-mode.yaml) | `energy_cmds` | `/energy_sites/{id}/storm_mode` |
| [Time Of Use / Off-Grid Charging](capabilities/fleet-energy-time-of-use.yaml) | `energy_cmds` | `/energy_sites/{id}/time_of_use_settings`, `/off_grid_vehicle_charging_reserve` |

#### Endpoints at a glance

| Method | Path | Scope | Purpose |
|---|---|---|---|
| GET | `/products` | `energy_device_data` | Discover energy sites (and vehicles) on the account |
| GET | `/energy_sites/{site_id}/site_info` | `energy_device_data` | Static site config — components, address, version |
| GET | `/energy_sites/{site_id}/live_status` | `energy_device_data` | Real-time power flow and state-of-charge |
| GET | `/energy_sites/{site_id}/calendar_history` | `energy_device_data` | Historical energy/power/self-consumption/savings/TOU buckets |
| GET | `/energy_sites/{site_id}/programs` | `energy_device_data` | VPP and grid-services participation status |
| POST | `/energy_sites/{site_id}/backup` | `energy_cmds` | Set backup reserve percent (0-100) |
| POST | `/energy_sites/{site_id}/operation` | `energy_cmds` | Set mode: self_consumption, backup, or autonomous |
| POST | `/energy_sites/{site_id}/storm_mode` | `energy_cmds` | Enable/disable Storm Mode pre-charging |
| POST | `/energy_sites/{site_id}/time_of_use_settings` | `energy_cmds` | Update TOU tariff schedule and optimization |
| POST | `/energy_sites/{site_id}/off_grid_vehicle_charging_reserve` | `energy_cmds` | Set EV reserve floor for islanded operation |

## Pricing, rate limits, and FinOps

- [Plans](plans/tesla-energy-plans-pricing.yml) — Fleet API metered tiers plus reference hardware pricing for Powerwall, Megapack, Solar Roof, and Solar Panels.
- [Rate limits](rate-limits/tesla-energy-rate-limits.yml) — per-site and per-partner daily request budgets across `energy_device_data` (read) and `energy_cmds` (write) scopes.
- [FinOps](finops/tesla-energy-finops.yml) — FOCUS-aligned cost surfaces covering Fleet API metering and one-time hardware capex.

## SDKs and developer tooling

- [teslamotors/vehicle-command (Go)](https://github.com/teslamotors/vehicle-command) — Tesla's official Go SDK and `tesla-http-proxy`. Vehicle-focused, but the HTTP proxy issues authenticated calls that can be reused for energy_sites endpoints.
- [tdorssers/TeslaPy](https://github.com/tdorssers/TeslaPy) — community Python SDK with first-class `Battery` and `SolarPanel` classes covering live status, calendar history, backup, operation, storm mode, time-of-use, off-grid reserve, and programs.
- [timdorr/tesla-api](https://github.com/timdorr/tesla-api) — long-standing community documentation of the Owner API and Fleet API, including energy endpoints.
- [Tesla Postman collection](https://documenter.getpostman.com/view/781424/2s9YRCWB4f).

## Business context

- 2024 energy revenue: $10.1B (+67% YoY); 2023 battery deployments: 31.4 GWh (+113% YoY).
- Megapack factories: Lathrop, CA (40 GWh/yr) and Shanghai Megafactory (online 2025).
- Tesla Electric operates in Texas as a retail electricity provider with VPP dispatch for Powerwall owners.
- Autobidder is Tesla's real-time market-bidding platform for utility-scale Megapack deployments.

## Run

[Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Maintainer

- **Kin Lane** — [API Evangelist](https://apievangelist.com) — info@apievangelist.com
