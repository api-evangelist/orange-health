# Orange Health

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

Orange Health Labs is an Indian at-home diagnostics laboratory serving Bengaluru, Delhi, Gurgaon, Noida and Hyderabad, offering 60-minute home sample collection and test results within about six hours. Its Partner API (documented on Apiary as the "Partner API Public Order Flow") lets healthcare partners, employers and apps check location serviceability and slots, create home-collection, lab-drop-off and health-camp orders, track order status, reschedule, cancel and add on tests, and pull structured investigation-level test results. Order lifecycle transitions (order.created through order.completed / order.cancelled) are delivered as HMAC-SHA256 signed webhooks. Authentication is an api_key request header.

**Areas:** Company · Mobile · Healthcare · Diagnostics · Lab Testing · Home Collection · Webhook · India

## Orange Health on APIs.io

Everything profiled for Orange Health is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/orange-health/](https://apis.io/providers/orange-health/)** — or go straight to one of the APIs or properties below.

### APIs (4)

- [Orange Health Orders API](https://apis.io/apis/orange-health/orange-health-orders-api/) — Create and manage diagnostic collection orders.
- [Orange Health Results API](https://apis.io/apis/orange-health/orange-health-results-api/) — Retrieve order status and structured test results.
- [Orange Health Serviceability API](https://apis.io/apis/orange-health/orange-health-serviceability-api/) — Check whether a location is serviceable and fetch available slots.
- [Orange Health Orange Health Partner API](https://apis.io/apis/orange-health/orange-health-orange-health-partner-api-api/) — The Orange Health Partner API API from Orange Health — 0 operation(s) for orange health partner api.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Orange Health Webhooks](https://apis.io/asyncapis/orange-health/orange-health-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [orange-health-partner](https://apis.io/servers/orange-health/orange-health-partner/)

#### Collections (3)

Postman and Open Collection request collections.

- [Orange Health Partner Orders API](https://apis.io/collections/orange-health/open-orange-health-orders-api/)
- [Orange Health Partner Orders Results API](https://apis.io/collections/orange-health/open-orange-health-results-api/)
- [Orange Health Partner Orders Serviceability API](https://apis.io/collections/orange-health/open-orange-health-serviceability-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Orange Health Partner Overlay](https://apis.io/overlays/orange-health/orange-health-partner-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Orange Health Authentication](https://apis.io/security/orange-health/orange-health-authentication/)
- [Orange Health Domain Security](https://apis.io/security/orange-health/orange-health-domain-security/)
- [Orange Health Vulnerability Disclosure](https://apis.io/security/orange-health/orange-health-vulnerability-disclosure/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.orangehealth.in/)
- [Documentation](https://orangehealth.docs.apiary.io/)
- [API reference](https://orangehealth.docs.apiary.io/)
- [Support](https://www.orangehealth.in/corporate-partners)
- [Blog](https://www.orangehealth.in/blog)
- [Terms of service](https://www.orangehealth.in/terms)
- [Privacy policy](https://www.orangehealth.in/privacy-policy)

## API Evangelist rating

**Kin Score 21.5** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 21.0 |
| Contract governance | 4.5 |
| Operational transparency | 18.4 |
| Developer ergonomics | 29.2 |
| Access clarity | 0.0 |

**Agent readiness 33.9** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
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

**Regulatory alignment 18.0** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/orange-health/](https://apis.io/providers/orange-health/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Orange Health: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/orange-health/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
