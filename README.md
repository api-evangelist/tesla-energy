# Tesla Energy (tesla-energy)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
