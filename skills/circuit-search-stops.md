---
name: Search stops with the filtering DSL
description: Run full-text and structured searches across all stop documents using the Spoke Public API v1 stop search endpoint and its SQL-inspired filtering DSL.
api: openapi/circuit-v1-openapi-original.json
operations: [searchStops, getStop, listCustomStopProperties]
---

# Search stops with the filtering DSL

`searchStops` (`GET /stops:search`) searches across all stop documents, including
unassigned stops, within your permitted data lifecycle.

## Auth
API key via HTTP Basic (`-u yourApiKey:`) or `Authorization: Bearer yourApiKey`.

## Steps
1. **Keyword search** — pass `keyword` for fuzzy full-text search across text fields,
   sorted by relevance: `GET /stops:search?keyword=london`.
2. **Structured filter** — pass `filter` with the DSL. Field, operator, value:
   `address.countryCode = "DE"`. Operators: `=`, `!=`, `~=` (substring), `>`, `>=`,
   `<`, `<=`, combined with `and`/`or` and parentheses. String comparisons with
   `>`/`<` require ISO-8601 dates. URL-encode the filter string.
3. **Custom properties** — filter on custom properties by ID:
   `custom_property.0234-5678-0abc-def3 = "value"`. Resolve IDs with
   `listCustomStopProperties` (`GET /team/customStopProperties`).
4. **Immediate reads** — the search index lags the realtime API; for a stop you just
   created, read it directly with `getStop` (`GET /plans/{planId}/stops/{stopId}`).

## Rules
- Results paginate with `nextPageToken` — resend as `pageToken` plus all original params.
- Read endpoints are limited to 10 req/sec; back off on `429`.
