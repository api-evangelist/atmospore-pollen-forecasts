# Atmospore Pollen Forecasts (atmospore-pollen-forecasts)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Atmospore is an Oslo-based provider of AI-driven global pollen and allergy forecasting. Its model combines GFS weather data with ground-truth observations from professional aerobiology networks to produce species-level forecasts on a ~28 km global grid, covering 25 individual tree, grass and weed species with multilingual metadata (English, Norwegian, Swedish) and published concentration thresholds for low/moderate/high/very-high risk. The surface is delivered three ways: a four-operation REST API at pollenapi.com with a live OpenAPI 3.0.3 contract, a hosted Model Context Protocol server at mcp.atmospore.com exposing the same capability as four agent tools, and a keyless embeddable iframe widget that consumes no API quota. Point forecasts, area averages with min/max across a radius, and severity-ranked top species are all available up to 14 days ahead; species metadata is served unauthenticated.

**APIs.json:** [https://atmospore-pollen-forecasts.apievangelist.com/apis.yml](https://atmospore-pollen-forecasts.apievangelist.com/apis.yml)

## Tags

- weather
- pollen
- allergy
- environmental-data
- health
- geospatial
- forecasting
- smart-home
- mcp
- openapi
- norway
- climate

## Timestamps

- **Created:** 2026-08-03
- **Modified:** 2026-08-09

## APIs

### Atmospore MCP Server

Hosted Model Context Protocol server exposing the Atmospore pollen forecast capability as four agent tools (get_pollen, get_top_species, get_area_average, list_supported_species) plus an atmospore://help resource. JSON-RPC 2.0 over HTTP, authenticated with the same Atmospore API key as the REST API. An MIT-licensed local stdio equivalent is published at github.com/atmospore/atmospore-mcp.

- **Human URL:** [https://atmospore.com/article/mcp](https://atmospore.com/article/mcp)
- **Base URL:** `https://mcp.atmospore.com/mcp`

#### Tags

- mcp
- agents
- pollen
- allergy
- forecasting

#### Properties

- [Tool Crosswalk](mcp/atmospore-pollen-forecasts-tool-crosswalk.yml)
- [Source Code](https://github.com/atmospore/atmospore-mcp)
- [Documentation](https://atmospore.com/article/mcp)
- [Postman Collection](collections/atmospore-pollen-forecasts-pollen-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/atmospore-pollen-forecasts-pollen-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/atmospore-pollen-forecasts-pollen-area-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/atmospore-pollen-forecasts-pollen-area-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/atmospore-pollen-forecasts-pollen-top-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/atmospore-pollen-forecasts-pollen-top-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/atmospore-pollen-forecasts-species-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/atmospore-pollen-forecasts-species-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Atmospore Pollen Forecasts Pollen API

The Pollen API from Atmospore Pollen Forecasts — 1 operation(s) for pollen.

- **Human URL:** [https://atmospore.com/api-docs](https://atmospore.com/api-docs)
- **Base URL:** `https://pollenapi.com`

#### Tags

- Pollen

#### Properties

- [OpenAPI](openapi/atmospore-pollen-forecasts-pollen-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/atmospore-pollen-forecasts-pollen-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/atmospore-pollen-forecasts-pollen-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://atmospore.com/api-docs)
- [API Reference](https://atmospore.com/api-docs)
- [Developer Portal](https://atmospore.com/api-docs)

### Atmospore Pollen Forecasts Pollen Area API

The Pollen Area API from Atmospore Pollen Forecasts — 1 operation(s) for pollen area.

- **Human URL:** [https://atmospore.com/api-docs](https://atmospore.com/api-docs)
- **Base URL:** `https://pollenapi.com`

#### Tags

- Pollen Area

#### Properties

- [OpenAPI](openapi/atmospore-pollen-forecasts-pollen-area-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/atmospore-pollen-forecasts-pollen-area-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/atmospore-pollen-forecasts-pollen-area-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://atmospore.com/api-docs)
- [API Reference](https://atmospore.com/api-docs)
- [Developer Portal](https://atmospore.com/api-docs)

### Atmospore Pollen Forecasts Pollen Top API

The Pollen Top API from Atmospore Pollen Forecasts — 1 operation(s) for pollen top.

- **Human URL:** [https://atmospore.com/api-docs](https://atmospore.com/api-docs)
- **Base URL:** `https://pollenapi.com`

#### Tags

- Pollen Top

#### Properties

- [OpenAPI](openapi/atmospore-pollen-forecasts-pollen-top-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/atmospore-pollen-forecasts-pollen-top-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/atmospore-pollen-forecasts-pollen-top-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://atmospore.com/api-docs)
- [API Reference](https://atmospore.com/api-docs)
- [Developer Portal](https://atmospore.com/api-docs)

### Atmospore Pollen Forecasts Species API

The Species API from Atmospore Pollen Forecasts — 1 operation(s) for species.

- **Human URL:** [https://atmospore.com/api-docs](https://atmospore.com/api-docs)
- **Base URL:** `https://pollenapi.com`

#### Tags

- Species

#### Properties

- [OpenAPI](openapi/atmospore-pollen-forecasts-species-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/atmospore-pollen-forecasts-species-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/atmospore-pollen-forecasts-species-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://atmospore.com/api-docs)
- [API Reference](https://atmospore.com/api-docs)
- [Developer Portal](https://atmospore.com/api-docs)

## Common Properties

- [Issue Tracker](https://github.com/atmospore/atmospore-mcp/issues)
- [License](https://github.com/atmospore/atmospore-mcp/blob/main/LICENSE)
- [Website](https://atmospore.com/)
- [Developer Portal](https://atmospore.com/api-docs)
- [Documentation](https://atmospore.com/api-docs)
- [API Reference](https://atmospore.com/api-docs)
- [Support](https://atmospore.com/contact)
- [GitHub Organization](https://github.com/atmospore)
- [Pricing](https://atmospore.com/plans)
- [Signup](https://atmospore.com/register)
- [Login](https://atmospore.com/login)
- [Terms of Service](https://atmospore.com/terms-of-service)
- [Privacy Policy](https://atmospore.com/privacy-policy)
- [Authentication](authentication/atmospore-pollen-forecasts-authentication.yml)
- [Conventions](conventions/atmospore-pollen-forecasts-conventions.yml)
- [Error Catalog](errors/atmospore-pollen-forecasts-problem-types.yml)
- [Lifecycle](lifecycle/atmospore-pollen-forecasts-lifecycle.yml)
- [Rate Limits](rate-limits/atmospore-pollen-forecasts-rate-limits.yml)
- [Plans](plans/atmospore-pollen-forecasts-plans.yml)
- [Packages](packages/atmospore-pollen-forecasts-packages.yml)
- [S D Ks](packages/atmospore-pollen-forecasts-packages.yml)
- [Sandbox](sandbox/atmospore-pollen-forecasts-sandbox.yml)
- [Components](components/atmospore-pollen-forecasts-components.yml)
- [Conformance](conformance/atmospore-pollen-forecasts-conformance.yml)
- [Domain Security](security/atmospore-pollen-forecasts-domain-security.yml)
- [M C P Server](mcp/atmospore-pollen-forecasts-mcp.yml)
- [Overlay](overlays/atmospore-pollen-forecasts-openapi-overlay.yaml)
- [Examples](examples/_index.yml)
- [Data Model](data-model/atmospore-pollen-forecasts-data-model.yml)
- [Agentic Access](agentic-access/atmospore-pollen-forecasts-agentic-access.yml)
- [Agent Skill](skills/_index.yml)
- [L L Ms Txt](llms/atmospore-pollen-forecasts-llms.txt)
- [Arazzo](arazzo/atmospore-pollen-forecasts-allergy-week-plan.yml) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Arazzo](arazzo/atmospore-pollen-forecasts-regional-risk-board.yml) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)

## Maintainers

**FN:** Atmospore Pollen Forecasts
**Email:** support@atmospore.com
**URL:** https://atmospore.com/
