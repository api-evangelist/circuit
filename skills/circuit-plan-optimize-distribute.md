---
name: Build, optimize and distribute a delivery plan
description: Create a route plan, add stops, optimize the routes, and distribute them across drivers using the Spoke Public API v1.
api: openapi/circuit-v1-openapi-original.json
operations: [createPlan, importStops, createStop, optimizePlan, distributePlan, getOperation, listPlanStops]
---

# Build, optimize and distribute a delivery plan

Use the Spoke Public API v1 (`https://api.spoke.com/public/v1`) to turn a list of
addresses into optimized driver routes.

## Auth
Send your API key as HTTP Basic (`-u yourApiKey:`) or as `Authorization: Bearer yourApiKey`.
Every request with a body must send `Content-Type: application/json`. HTTPS only.

## Steps
1. **Create a plan** — `createPlan` (`POST /plans`). Supply the plan title, date and
   depot. The response `id` is `plans/{planId}`.
2. **Add stops** — for many stops use `importStops` (`POST /plans/{planId}/stops:import`);
   for a single stop use `createStop` (`POST /plans/{planId}/stops`). Batch import is
   rate-limited to 100 req / 10 min but handles up to 1,000 stops per minute.
3. **Optimize** — `optimizePlan` (`POST /plans/{planId}:optimize`). This is a
   long-running operation: the response is an operation resource (`operations/{id}`).
   Poll `getOperation` (`GET /operations/{operationId}`) until it completes. Optimization
   is rate-limited to 100 req / 10 min.
4. **Distribute** — once optimized, `distributePlan` (`POST /plans/{planId}:distribute`)
   assigns the optimized routes to drivers. It also returns an operation to poll.
5. **Verify** — `listPlanStops` (`GET /plans/{planId}/stops`) to confirm assignments.

## Rules
- Arrays are replaced wholesale on PATCH — send the full array, not a partial one.
- Handle `409` conflicts: `plan_already_optimized`, `plan_already_distributed`,
  `plan_optimization_in_progress`, `no_drivers_available`. See errors/circuit-error-codes.yml.
- On `429`, back off exponentially with jitter. See rate-limits/circuit-rate-limits.yml.
