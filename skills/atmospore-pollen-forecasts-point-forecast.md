---
name: Get a species-level pollen forecast for a place
description: >-
  Resolve Atmospore's species catalogue, then fetch a point pollen forecast for a coordinate and
  date range, and read the risk levels correctly. Use for "what's the pollen in <city> this week?"
  and for allergy-specific questions about a named species.
api: openapi/atmospore-pollen-forecasts-openapi-original.json
operations:
  - getSpecies
  - getPollenForecast
generated: '2026-08-09'
method: generated
source: openapi/atmospore-pollen-forecasts-openapi-original.json + https://atmospore.com/api-docs
---

# Get a species-level pollen forecast for a place

Base URL `https://pollenapi.com`. Everything is a GET.

## 1. Authenticate

Send `x-api-key: <key>` on every request except `getSpecies`. Keys come from
https://atmospore.com/account (free tier: 3,000 requests/month, no card).

There is no test mode and no sandbox host — a development call spends production quota.

## 2. Resolve the species catalogue first (`getSpecies`)

```
GET /v1/species
```

No API key. Returns 25 species keyed by slug, each with `display_name`, `category`
(`tree`|`grass`|`weed`), localised `names` (`en`, `sv`, `no`), `risk_thresholds` (four
concentration cut-points) and `risk_labels`.

Cache this for 24 hours — the response carries `Cache-Control: max-age=86400`. Never guess a
species slug; resolve it here. Group selectors `tree`, `grass`, `weed` and `all` are also valid
values for the `species` filter.

## 3. Fetch the forecast (`getPollenForecast`)

```
GET /v1/pollen?lon={lon}&lat={lat}&dt={YYYY-MM-DD}&forecast_days={1-14}&species={slugs}
```

- `lon`, `lat`, `dt` and `forecast_days` are all **required**. Omitting any of them is a 400.
- `forecast_days` must be 1-14.
- `species` is optional and comma-separated; omit it to get every species.
- Coordinates work anywhere on land — the model is global at ~28 km resolution. If the user names
  a city, resolve its coordinates yourself before calling.

Response: `meta` (`location`, `units` = `grains/m³`, `generated_at`) plus `data[]`, one entry per
day, each with `date`, `overall_risk` and a `species` map of `{value, risk_level, display_name,
category}`.

## 4. Report the answer

- Values are **grains/m³**. Always state the unit.
- `risk_level` is one of `low`, `moderate`, `high`, `very high` — prefer it over the raw number
  when speaking to a person; the thresholds differ per species and come from `getSpecies`.
- `overall_risk` is the daily rollup across all species; a specific allergy question should be
  answered from that species' own entry, not the rollup.
- `meta.generated_at` tells you how fresh the run is. Forecasts refresh daily and are refined as
  the target date approaches.

## 5. Handle failure

Errors are a flat `{"error": "<message>"}` — not RFC 9457. Branch on the status:

| Status | Meaning | What to do |
|---|---|---|
| 400 | Invalid parameters | Check required params, `forecast_days` 1-14, and species slugs against `getSpecies`. |
| 401 | Missing API key | Add the `x-api-key` header. |
| 403 | Invalid API key | Do **not** retry — reissue the key at https://atmospore.com/account. |
| 429 | Daily quota exceeded | Stop. Back off to the next day or upgrade at https://atmospore.com/plans. |

There are no rate-limit response headers, so you cannot pace ahead of a 429 — cache aggressively
instead. All operations are GET and safe to retry on transport failure; there is no idempotency
key because there are no writes.

Keep the `apigw-requestid` response header if you need to report a problem to support.
