# Tesla Energy (tesla-energy)

Tesla Energy is Tesla's solar generation and battery storage business unit, encompassing residential Powerwall, utility-scale Megapack, retrofit solar panels, and the Solar Roof. The Fleet API exposes energy_sites endpoints that let partners and owners read live power, calendar history, and site info, and write backup reserve, operation mode (self_consumption, backup, autonomous), storm mode, time-of-use settings, and off-grid vehicle charging reserve — the same control surface that powers the Tesla app and integrators like Autobidder, Tesla Electric (virtual power plant), and third-party home energy dashboards.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/tesla-energy/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/tesla-energy/refs/heads/main/apis.yml)

## Scope

- **Position:** Producing
- **Access:** 3rd-Party

## Tags

- Energy
- Clean Energy
- Solar
- Battery Storage
- Powerwall
- Megapack
- Solar Roof
- Virtual Power Plant
- IoT
- Grid Services
- Home Energy
- Utility Scale

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Tesla Fleet Energy API

The energy_sites surface of the Tesla Fleet API. Provides OAuth-authenticated read access to Powerwall, Solar, and Megapack site state — site info, live status, calendar history, programs — and write access to backup reserve, operation mode, storm mode, time-of-use settings, and off-grid vehicle charging reserve. Requires energy_device_data (read) and energy_cmds (write) scopes.

- **Human URL:** [https://developer.tesla.com/docs/fleet-api/endpoints/energy](https://developer.tesla.com/docs/fleet-api/endpoints/energy)
- **Base URL:** `https://fleet-api.prd.na.vn.cloud.tesla.com/api/1`

#### Tags

- Energy
- Powerwall
- Solar
- Megapack
- Fleet API
- Energy Sites
- Backup Reserve
- Storm Mode
- Time Of Use
- Virtual Power Plant

#### Properties

- [Documentation](https://developer.tesla.com/docs/fleet-api/endpoints/energy)
- [Authentication](https://developer.tesla.com/docs/fleet-api/authentication/overview)
- [Documentation](https://developer.tesla.com/docs/fleet-api/products/energy-products)
- [Documentation](https://developer.tesla.com/docs/fleet-api/virtual-key/overview)
- [OpenAPI](openapi/tesla-energy-fleet-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/tesla-energy-fleet-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/tesla-energy-fleet-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/tesla-energy-site-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/tesla-energy-live-status-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/tesla-energy-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/tesla-energy-live-status-example.json)
- [Example](examples/tesla-energy-site-info-example.json)
- [Spectral Rules](rules/tesla-energy-rules.yml)

## Common Properties

- [Portal](https://www.tesla.com/energy)
- [Portal](https://developer.tesla.com/)
- [Documentation](https://developer.tesla.com/docs/fleet-api)
- [Documentation](https://developer.tesla.com/docs/fleet-api/endpoints/energy)
- [Documentation](https://developer.tesla.com/docs/fleet-api/products/energy-products)
- [Authentication](https://developer.tesla.com/docs/fleet-api/authentication/overview)
- [Authentication](https://developer.tesla.com/docs/fleet-api/authentication/third-party-tokens)
- [Rate Limits](https://developer.tesla.com/docs/fleet-api/billing-and-limits)
- [Billing](https://developer.tesla.com/docs/fleet-api/billing-and-limits)
- [Changelog](https://developer.tesla.com/docs/fleet-api/announcements)
- [F A Q](https://developer.tesla.com/docs/fleet-api/support/faq)
- [Support](https://developer.tesla.com/docs/fleet-api/support/contact)
- [GitHub Organization](https://github.com/teslamotors)
- [SDK](https://github.com/teslamotors/vehicle-command)
- [SDK](https://github.com/tdorssers/TeslaPy)
- [SDK](https://github.com/timdorr/tesla-api)
- [Postman](https://documenter.getpostman.com/view/781424/2s9YRCWB4f) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Website](https://www.tesla.com)
- [Website](https://www.tesla.com/powerwall)
- [Website](https://www.tesla.com/megapack)
- [Website](https://www.tesla.com/solarpanels)
- [Website](https://www.tesla.com/solarroof)
- [Website](https://www.tesla.com/electric)
- [Website](https://www.tesla.com/autobidder)
- [LinkedIn](https://www.linkedin.com/company/tesla-motors)
- [Terms of Service](https://www.tesla.com/legal)
- [Privacy Policy](https://www.tesla.com/legal/privacy)
- [Plans](plans/tesla-energy-plans-pricing.yml)
- [Rate Limits](rate-limits/tesla-energy-rate-limits.yml)
- [Fin Ops](finops/tesla-energy-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
