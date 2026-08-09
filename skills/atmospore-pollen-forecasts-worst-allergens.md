---
name: Rank the worst allergens for a place and week
description: >-
  Use Atmospore's ranked top-species operation to answer "what's blowing right now?" and
  "which allergen is worst this week?", with the species catalogue supplying the human names
  and the risk thresholds.
api: openapi/atmospore-pollen-forecasts-openapi-original.json
operations:
  - getSpecies
  - getPollenTop
generated: '2026-08-09'
method: generated
source: openapi/atmospore-pollen-forecasts-openapi-original.json + https://atmospore.com/api-docs
---

# Rank the worst allergens for a place and week

Answers "what pollen is highest in Bergen right now?" or "this week's worst allergens" in one
call, instead of fetching the full forecast and sorting it yourself.

## 1. Resolve names once (`getSpecies`)

```
GET /v1/species
```

Unauthenticated, cacheable for 24 hours. You need it for `display_name`, `category` and
`risk_thresholds`. `getPollenTop` returns `display_name` inline, but the thresholds only exist
here — use them if you want to explain *why* a value counts as high.

## 2. Get the ranked list (`getPollenTop`)

```
GET /v1/pollen-top?lon={lon}&lat={lat}&dt={YYYY-MM-DD}&forecast_days={1-14}
```

Send `x-api-key`. All four parameters are required. Unlike `getPollenForecast`, this operation
takes **no `species` filter** — it always ranks across the whole catalogue.

Response `data[]` is ordered highest-severity first. Each entry: `species` (slug),
`display_name`, `category`, `max`, `avg`, `risk_level`. `meta.date_range` echoes the window that
was aggregated, and `meta.units` is `grains/m³`.

Note there is no `limit` parameter in the REST contract — truncate client-side. (The MCP tool
`get_top_species` takes a `limit`; that truncation happens in the MCP wrapper, not the API.)

## 3. Turn it into an answer

- Lead with the top one or two entries by `max`, named with `display_name`, not the slug.
- `max` is the worst single day in the range and `avg` is the mean across it — say which you are
  quoting. "Birch peaks at 480 grains/m³ (high) this week, averaging 210" is honest; "birch is 480"
  is not.
- Group by `category` (`tree` / `grass` / `weed`) when the user asks a broad question. For a
  category-level trend over an area, switch to `getPollenArea` and its `tree_tot`/`grass_tot`/
  `weed_tot` aggregates.
- If the user names their allergy, filter this list to that species rather than reporting the
  overall winner.

## 4. Failure and cost

Same envelope as everywhere else: `{"error": "<message>"}`, with 400 / 401 / 403 / 429. A 403
means the key is bad — do not retry. A 429 means the plan quota is spent; there are no
rate-limit headers to warn you first, so cache the ranked list per (location, week) rather than
recomputing it per user request.
