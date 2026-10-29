# Circuit

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

Circuit (operating publicly as Spoke; legal entity Circuit Routing Limited) builds last-mile delivery route-optimization software. Its products are Route Planner, a free driver app for uploading stops, optimizing multi-stop routes and navigating; Dispatch, a multi-driver delivery-management platform with route planning, live tracking and proof of delivery for courier operations; and Connect, a marketplace that lets retailers discover local couriers and track deliveries. The Spoke Public API (formerly the Circuit for Teams API) is an HTTP/JSON API that lets teams manage plans, stops, unassigned stops, drivers, depots, routes, members and long-running operations programmatically, optimize and distribute plans across drivers, run full-text stop search with a filtering DSL, and subscribe to webhook events for delivery workflows.

**Areas:** Company · Delivery · Logistics · Last Mile Delivery · Route Optimization · Dispatch · Couriers · Fleet Management · Proof of Delivery · Field Service Management

## Circuit on APIs.io

Everything profiled for Circuit is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/circuit/](https://apis.io/providers/circuit/)** — or go straight to one of the APIs or properties below.

### APIs (11)

- [Circuit Depots API](https://apis.io/apis/circuit/circuit-depots-api/) — Endpoints to operate on [Depots](/docs/models/depot) resources. This resource is currently read-only on the API.
- [Circuit Drivers API](https://apis.io/apis/circuit/circuit-drivers-api/) — Endpoints to operate on [Drivers](/docs/models/driver) resources.
- [Circuit Live Plans API](https://apis.io/apis/circuit/circuit-live-plans-api/) — Endpoints to operate on [Plans](/docs/models/plan) resources when it's pending re-optimization and re-distribution. You must use these endpoints to apply…
- [Circuit Live Stops API](https://apis.io/apis/circuit/circuit-live-stops-api/) — Endpoints to operate on [Stop](/docs/models/stop) resources when the plan is already optimized and therefore not writable. All the endpoints return the…
- [Circuit Members API](https://apis.io/apis/circuit/circuit-members-api/) — Endpoints to operate on Members resources.
- [Circuit Operations API](https://apis.io/apis/circuit/circuit-operations-api/) — Endpoints to operate on [Operations](/docs/models/operation) resources.
- [Circuit Plans API](https://apis.io/apis/circuit/circuit-plans-api/) — Endpoints to operate on [Plans](/docs/models/plan) resources.
- [Circuit Routes API](https://apis.io/apis/circuit/circuit-routes-api/) — Endpoints to operate on [Routes](/docs/models/route) resources. This resource is currently read-only on the API.
- [Circuit Stops API](https://apis.io/apis/circuit/circuit-stops-api/) — Endpoints to operate on [Stop](/docs/models/stop) resources. For any [Plans](/docs/models/plan) created before 2023-04-01 the stop collections and all…
- [Circuit Team API](https://apis.io/apis/circuit/circuit-team-api/) — Endpoints to retrieve [Custom Stop Properties](/docs/models/customStopProperty).
- [Circuit Unassigned Stops API](https://apis.io/apis/circuit/circuit-unassigned-stops-api/) — Endpoints to operate on [Unassigned Stop](/docs/models/unassignedStop) resources.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Circuit Webhooks](https://apis.io/asyncapis/circuit/circuit-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [circuit-spoke](https://apis.io/servers/circuit/circuit-spoke/)

#### Collections (11)

Postman and Open Collection request collections.

- [Spoke Depots API](https://apis.io/collections/circuit/open-circuit-depots-api/)
- [Spoke Depots Drivers API](https://apis.io/collections/circuit/open-circuit-drivers-api/)
- [Spoke Depots Live Plans API](https://apis.io/collections/circuit/open-circuit-live-plans-api/)
- [Spoke Depots Live Stops API](https://apis.io/collections/circuit/open-circuit-live-stops-api/)
- [Spoke Depots Members API](https://apis.io/collections/circuit/open-circuit-members-api/)
- [Spoke Depots Operations API](https://apis.io/collections/circuit/open-circuit-operations-api/)
- [Spoke Depots Plans API](https://apis.io/collections/circuit/open-circuit-plans-api/)
- [Spoke Depots Routes API](https://apis.io/collections/circuit/open-circuit-routes-api/)
- [Spoke Depots Stops API](https://apis.io/collections/circuit/open-circuit-stops-api/)
- [Spoke Depots Team API](https://apis.io/collections/circuit/open-circuit-team-api/)
- [Spoke Depots Unassigned Stops API](https://apis.io/collections/circuit/open-circuit-unassigned-stops-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Circuit V1 Overlay](https://apis.io/overlays/circuit/circuit-v1-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Circuit Authentication](https://apis.io/security/circuit/circuit-authentication/)
- [Circuit Domain Security](https://apis.io/security/circuit/circuit-domain-security/)

#### Rate limits (1)

Published request limits.

- [Circuit Rate Limits](https://apis.io/rate-limits/circuit/circuit-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://spoke.com/)
- [Documentation](https://developer.dispatch.spoke.com/)
- [Getting started](https://developer.dispatch.spoke.com/docs/v1/api-examples)
- [API reference](https://developer.dispatch.spoke.com/api/v1)
- [Pricing](https://help.spoke.com/en/collections/385323-spoke-help-products-pricing)
- [Support](https://help.spoke.com/)
- [Terms of service](https://spoke.com/terms)
- [Privacy policy](https://spoke.com/privacy)
- [Status](https://status.spoke.com/)

## API Evangelist rating

**Kin Score 52.6** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 61.9 |
| Contract governance | 4.5 |
| Operational transparency | 78.9 |
| Developer ergonomics | 56.5 |
| Access clarity | 21.1 |

**Agent readiness 28.5** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 24.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/circuit/](https://apis.io/providers/circuit/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Circuit: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/circuit/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
