# Atmospore Pollen Forecasts (atmospore-pollen-forecasts)

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
