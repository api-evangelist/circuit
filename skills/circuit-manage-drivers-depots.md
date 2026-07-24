---
name: Set up depots and drivers
description: Create depots and onboard drivers (individually or in bulk) so plans can be optimized and distributed with the Spoke Public API v1.
api: openapi/circuit-v1-openapi-original.json
operations: [createDepot, setMainDepot, listDepots, createDriver, importDrivers, listDrivers, updateDriver]
---

# Set up depots and drivers

Depots and drivers are prerequisites for optimizing and distributing plans.

## Auth
API key via HTTP Basic (`-u yourApiKey:`) or `Authorization: Bearer yourApiKey`;
`Content-Type: application/json` on bodies; HTTPS only.

## Steps
1. **Create a depot** — `createDepot` (`POST /depots`). Set a start address so
   optimization can evaluate the plan (missing start address raises
   `depot_missing_start_address`).
2. **Set the main depot** — `setMainDepot` (`POST /depots/{depotId}:setMain`) if you
   operate a single primary depot.
3. **Onboard drivers** — for one driver use `createDriver` (`POST /drivers`), which is
   rate-limited to 1 req/sec. For many drivers use `importDrivers`
   (`POST /drivers:import`) — limited to 2 req/min but imports up to 100 drivers/min.
4. **Verify** — `listDepots` (`GET /depots`) and `listDrivers` (`GET /drivers`).
5. **Update** — `updateDriver` (`PATCH /drivers/{driverId}`) for changes.

## Rules
- A driver's depot must match a plan's depot to be assignable (else optimization fails).
- List endpoints paginate with `nextPageToken`; resend it as `pageToken` with all
  original query params. See conventions/circuit-conventions.yml.
