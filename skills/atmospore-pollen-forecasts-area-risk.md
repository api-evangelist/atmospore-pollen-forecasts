---
name: Assess area-wide pollen risk and trend
description: >-
  Aggregate tree/grass/weed pollen across a radius for regional dashboards, smart-home
  automations and health services that need an area risk read rather than a single grid point —
  including the metres-vs-kilometres trap between the REST operation and the MCP tool.
api: openapi/atmospore-pollen-forecasts-openapi-original.json
operations:
  - getSpecies
  - getPollenArea
generated: '2026-08-09'
method: generated
source: openapi/atmospore-pollen-forecasts-openapi-original.json + https://atmospore.com/api-docs
---

# Assess area-wide pollen risk and trend

Use this when a single coordinate is too sharp: a city-wide dashboard, a smart-home ventilation
rule, or "is tree or grass pollen worse in London this week?".

## 1. Call the area operation (`getPollenArea`)

```
GET /v1/pollen-area?lon={lon}&lat={lat}&dt={YYYY-MM-DD}&forecast_days={1-14}&radius={metres}&species={slugs}
```

Send `x-api-key`. `lon`, `lat`, `dt` and `forecast_days` are required; `radius` and `species` are
optional.

**`radius` is in METRES.** Default 25000, maximum 50000. This is the single easiest thing to get
wrong here: the Atmospore MCP tool `get_area_average` takes `radius_km` (default 25), so a value
copied between the two surfaces is off by a factor of 1000. Convert explicitly.

## 2. Ask for aggregates, not species, when the question is categorical

Pass `species=tree_tot,grass_tot,weed_tot` to get the category rollups. Each entry in the response
`species` map then carries `avg`, `min`, `max`, `risk_level`, `display_name` and `category` — the
min/max spread is the point of this operation, and it tells you how uneven the area is.

For a specific allergen, pass its slug instead (resolve slugs from `getSpecies` — unauthenticated,
cache 24h).

## 3. Read the trend

`data[]` has one entry per day across `forecast_days`, each with `date`, `overall_risk` and the
`species` map. To answer "is it getting worse?", compare `avg` for the same key across
consecutive days rather than comparing `overall_risk` labels, which are coarse and will sit flat
across a real rise.

`meta` carries the `location`, the echoed `radius`, `units` (`grains/m³`) and `generated_at`.

## 4. Budget the calls

One area call covers up to 14 days, so fetch the whole horizon once rather than one call per day.
Quotas are per key and monthly (Free 3,000; Starter 15,000; Professional 150,000; Enterprise
1,500,000), enforced with a daily ceiling, and a 429 arrives with no warning headers.

If all you need is a display for a website, the keyless iframe widget at
`https://atmospore.com/widget/{city}` renders the same category split and consumes **no** quota —
see `components/atmospore-pollen-forecasts-components.yml`.

## 5. Failure

`{"error": "<message>"}` with 400 (bad parameters — check `radius` <= 50000 and `forecast_days`
1-14), 401 (no key), 403 (bad key, do not retry), 429 (quota spent). Note that 401 and 403 are
**not** declared with a response body in the published contract even though the API returns one.
