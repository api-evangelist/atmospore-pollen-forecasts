# Atmospore Pollen Forecasts

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

**Areas:** Weather · Pollen · Allergy · Environmental Data · Health · Geospatial · Forecasting · Smart Home · MCP · OpenAPI · Norway · Climate

## Atmospore Pollen Forecasts on APIs.io

Everything profiled for Atmospore Pollen Forecasts is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/atmospore-pollen-forecasts/](https://apis.io/providers/atmospore-pollen-forecasts/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [Atmospore MCP Server](https://apis.io/apis/atmospore-pollen-forecasts/atmospore-mcp-server/) — Hosted Model Context Protocol server exposing the Atmospore pollen forecast capability as four agent tools (get_pollen, get_top_species, get_area_average,…
- [Atmospore Pollen Forecasts Pollen API](https://apis.io/apis/atmospore-pollen-forecasts/atmospore-pollen-forecasts-pollen-api/) — The Pollen API from Atmospore Pollen Forecasts — 1 operation(s) for pollen.
- [Atmospore Pollen Forecasts Pollen Area API](https://apis.io/apis/atmospore-pollen-forecasts/atmospore-pollen-forecasts-pollen-area-api/) — The Pollen Area API from Atmospore Pollen Forecasts — 1 operation(s) for pollen area.
- [Atmospore Pollen Forecasts Pollen Top API](https://apis.io/apis/atmospore-pollen-forecasts/atmospore-pollen-forecasts-pollen-top-api/) — The Pollen Top API from Atmospore Pollen Forecasts — 1 operation(s) for pollen top.
- [Atmospore Pollen Forecasts Species API](https://apis.io/apis/atmospore-pollen-forecasts/atmospore-pollen-forecasts-species-api/) — The Species API from Atmospore Pollen Forecasts — 1 operation(s) for species.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (2)

Multi-step workflows that chain operations into a business task.

- [Plan an allergy week for a location](https://apis.io/arazzos/atmospore-pollen-forecasts/atmospore-pollen-forecasts-allergy-week-plan/)
- [Build a regional pollen risk board](https://apis.io/arazzos/atmospore-pollen-forecasts/atmospore-pollen-forecasts-regional-risk-board/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [atmospore](https://apis.io/servers/atmospore-pollen-forecasts/atmospore/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Atmospore Pollen Forecasts Agentic Access](https://apis.io/agentic-access/atmospore-pollen-forecasts/atmospore-pollen-forecasts-agentic-access/)

#### Examples (3)

Example requests and responses.

- [Atmospore Pollen Forecasts Pollen 401](https://apis.io/examples/atmospore-pollen-forecasts/atmospore-pollen-forecasts-pollen-401/)
- [Atmospore Pollen Forecasts Pollen 403](https://apis.io/examples/atmospore-pollen-forecasts/atmospore-pollen-forecasts-pollen-403/)
- [Atmospore Pollen Forecasts Species 200](https://apis.io/examples/atmospore-pollen-forecasts/atmospore-pollen-forecasts-species-200/)

#### Collections (4)

Postman and Open Collection request collections.

- [Atmospore Forecast Pollen API](https://apis.io/collections/atmospore-pollen-forecasts/open-atmospore-pollen-forecasts-pollen-api/)
- [Atmospore Pollen Forecast Pollen Area API](https://apis.io/collections/atmospore-pollen-forecasts/open-atmospore-pollen-forecasts-pollen-area-api/)
- [Atmospore Pollen Forecast Pollen Top API](https://apis.io/collections/atmospore-pollen-forecasts/open-atmospore-pollen-forecasts-pollen-top-api/)
- [Atmospore Pollen Forecast Species API](https://apis.io/collections/atmospore-pollen-forecasts/open-atmospore-pollen-forecasts-species-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Atmospore Pollen Forecasts Openapi Overlay](https://apis.io/overlays/atmospore-pollen-forecasts/atmospore-pollen-forecasts-openapi-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Atmospore Pollen Forecasts Authentication](https://apis.io/security/atmospore-pollen-forecasts/atmospore-pollen-forecasts-authentication/)
- [Atmospore Pollen Forecasts Domain Security](https://apis.io/security/atmospore-pollen-forecasts/atmospore-pollen-forecasts-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Atmospore Pollen Forecasts Plans](https://apis.io/plans/atmospore-pollen-forecasts/atmospore-pollen-forecasts-plans/)

#### Rate limits (1)

Published request limits.

- [Atmospore Pollen Forecasts Rate Limits](https://apis.io/rate-limits/atmospore-pollen-forecasts/atmospore-pollen-forecasts-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://atmospore.com/)
- [Documentation](https://atmospore.com/api-docs)
- [API reference](https://atmospore.com/api-docs)
- [Pricing](https://atmospore.com/plans)
- [Support](https://atmospore.com/contact)
- [Blog](https://atmospore.com/blog/)
- [Terms of service](https://atmospore.com/terms-of-service)
- [Privacy policy](https://atmospore.com/privacy-policy)
- [GitHub](https://github.com/atmospore)

## API Evangelist rating

**Kin Score 54.1** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 68.3 |
| Contract quality | 52.9 |
| Contract governance | 4.5 |
| Operational transparency | 34.2 |
| Developer ergonomics | 61.3 |
| Access clarity | 69.7 |

**Agent readiness 36.2** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | na |
| MCP Server | verified |
| Auth Clarity | bearer (partial credit) |
| Idempotency | na |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | na |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | na |

**Regulatory alignment 31.3** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/atmospore-pollen-forecasts/](https://apis.io/providers/atmospore-pollen-forecasts/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Atmospore Pollen Forecasts: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/atmospore-pollen-forecasts/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
