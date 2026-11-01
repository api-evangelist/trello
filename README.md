# Trello

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

Trello is a web-based, kanban-style, list-making application from Atlassian that lets teams organize tasks, projects and workflows as boards, lists and cards. Its public REST API v1 at https://api.trello.com/1 exposes 261 operations across boards, lists, cards, checklists, labels, custom fields, attachments, members, workspaces, enterprises, actions, notifications, search, webhooks, tokens and Power-Up plugins, with a first-party OpenAPI 3.0.0 definition published by Atlassian. Authorization is an API key plus user token, or OAuth 2.0 3LO with ten granular scopes, generally available since 15 September 2026. Trello also ships a webhook surface signed with HMAC-SHA1, a browser client library (client.js), and the Power-Ups framework for extending the Trello board UI. The platform publishes no MCP server and no A2A agent card, no idempotency mechanism and no rate-limit response headers.

**Areas:** Project Management · Kanban · Task Management · Collaboration · Productivity · Workflows · Boards · Atlassian

## Trello on APIs.io

Everything profiled for Trello is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/trello/](https://apis.io/providers/trello/)** — or go straight to one of the APIs or properties below.

### APIs (20)

- [Trello Webhooks API](https://apis.io/apis/trello/webhooks-api/) — The Trello Webhooks API allows developers to receive real-time notifications when changes occur on Trello models such as boards, lists, and cards. Rather…
- [Trello Power-Ups](https://apis.io/apis/trello/power-ups/) — Trello Power-Ups are a framework for extending and integrating with the Trello platform. Power-Ups allow developers to add custom functionality to Trello…
- [trello Actions API](https://apis.io/apis/trello/trello-actions-api/) — Operations for retrieving and managing actions, which represent activity events that occur on Trello objects such as boards, lists, and cards.
- [trello Boards API](https://apis.io/apis/trello/trello-boards-api/) — Operations for creating, retrieving, updating, and deleting boards, as well as managing board memberships, lists, cards, labels, and other board-level…
- [trello Cards API](https://apis.io/apis/trello/trello-cards-api/) — Operations for creating, retrieving, updating, and deleting cards, including managing card attachments, checklists, comments, labels, members, and stickers.
- [trello Checklists API](https://apis.io/apis/trello/trello-checklists-api/) — Operations for creating, retrieving, updating, and deleting checklists and their check items on cards.
- [trello Labels API](https://apis.io/apis/trello/trello-labels-api/) — Operations for creating, retrieving, updating, and deleting labels on boards and cards.
- [trello Lists API](https://apis.io/apis/trello/trello-lists-api/) — Operations for creating, retrieving, updating, and archiving lists on boards.
- [trello Members API](https://apis.io/apis/trello/trello-members-api/) — Operations for retrieving and updating member profiles, boards, organizations, and notification settings.
- [trello Notifications API](https://apis.io/apis/trello/trello-notifications-api/) — Operations for retrieving and managing member notifications about activity on boards, cards, and other Trello objects.
- [trello Organizations API](https://apis.io/apis/trello/trello-organizations-api/) — Operations for creating, retrieving, updating, and deleting Trello workspaces (organizations), including managing workspace members and settings.
- [trello Plugins API](https://apis.io/apis/trello/trello-plugins-api/) — Operations for managing Power-Up plugins, including listing, updating, and creating plugin marketplace listings.
- [trello Search API](https://apis.io/apis/trello/trello-search-api/) — Operations for searching across Trello boards, cards, members, and organizations using query strings.
- [trello Tokens API](https://apis.io/apis/trello/trello-tokens-api/) — Operations for retrieving and deleting API tokens and their associated webhooks.
- [trello Webhooks API](https://apis.io/apis/trello/trello-webhooks-api/) — Operations for creating, retrieving, updating, and deleting webhooks that deliver real-time notifications when Trello models change.
- [Trello Applications API](https://apis.io/apis/trello/trello-applications-api/) — The Applications API from Trello — 1 operation(s) for applications.
- [Trello Batch API](https://apis.io/apis/trello/trello-batch-api/) — The Batch API from Trello — 1 operation(s) for batch.
- [Trello Emoji API](https://apis.io/apis/trello/trello-emoji-api/) — The Emoji API from Trello — 1 operation(s) for emoji.
- [Trello Enterprises API](https://apis.io/apis/trello/trello-enterprises-api/) — The Enterprises API from Trello — 19 operation(s) for enterprises.
- [Trello Custom Fields API](https://apis.io/apis/trello/trello-custom-fields-api/) — Operations for creating, retrieving, updating, and deleting custom field definitions and their values on boards and cards.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Trello Webhooks Events](https://apis.io/asyncapis/trello/trello-webhooks-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/webhook](https://apis.io/channels/trello/webhook/)

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/trello/](https://apis.io/graphqls/trello/trello-graphql/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [trello (candidate)](https://apis.io/servers/trello/trello-candidate/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Trello Agentic Access](https://apis.io/agentic-access/trello/trello-agentic-access/)

#### JSON Schema (3)

The data models the API reads and writes.

- [Trello Board](https://apis.io/schemas/trello/trello-board/)
- [Trello Card](https://apis.io/schemas/trello/trello-card/)
- [Trello Webhook Payload](https://apis.io/schemas/trello/trello-webhook-payload/)

#### JSON Structure (2)

Data models expressed in JSON Structure.

- [Trello Board Structure](https://apis.io/json-structure/trello/trello-board-structure/)
- [Trello Card Structure](https://apis.io/json-structure/trello/trello-card-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Trello Context](https://apis.io/jsonld/trello/trello-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Trello Vocabulary](https://apis.io/vocabularies/trello/trello-vocabulary/)

#### Collections (15)

Postman and Open Collection request collections.

- [Trello REST Actions API](https://apis.io/collections/trello/open-trello-actions-api/)
- [Trello REST Actions Boards API](https://apis.io/collections/trello/open-trello-boards-api/)
- [Trello REST Actions Cards API](https://apis.io/collections/trello/open-trello-cards-api/)
- [Trello REST Actions Checklists API](https://apis.io/collections/trello/open-trello-checklists-api/)
- [Trello REST Actions CustomFields API](https://apis.io/collections/trello/open-trello-customfields-api/)
- [Trello REST Actions Labels API](https://apis.io/collections/trello/open-trello-labels-api/)
- [Trello REST Actions Lists API](https://apis.io/collections/trello/open-trello-lists-api/)
- [Trello REST Actions Members API](https://apis.io/collections/trello/open-trello-members-api/)
- [Trello REST Actions Notifications API](https://apis.io/collections/trello/open-trello-notifications-api/)
- [Trello REST Actions Organizations API](https://apis.io/collections/trello/open-trello-organizations-api/)
- [Trello REST Actions Plugins API](https://apis.io/collections/trello/open-trello-plugins-api/)
- [Trello REST API](https://apis.io/collections/trello/open-trello-rest-api/)
- [Trello REST Actions Search API](https://apis.io/collections/trello/open-trello-search-api/)
- [Trello REST Actions Tokens API](https://apis.io/collections/trello/open-trello-tokens-api/)
- [Trello REST Actions Webhooks API](https://apis.io/collections/trello/open-trello-webhooks-api/)

#### Overlays (19)

OpenAPI overlays, including conversational phrasing for each operation.

- [Trello Actions Api Phrasing Overlay](https://apis.io/overlays/trello/trello-actions-api-phrasing-overlay/)
- [Trello Applications Api Phrasing Overlay](https://apis.io/overlays/trello/trello-applications-api-phrasing-overlay/)
- [Trello Batch Api Phrasing Overlay](https://apis.io/overlays/trello/trello-batch-api-phrasing-overlay/)
- [Trello Boards Api Phrasing Overlay](https://apis.io/overlays/trello/trello-boards-api-phrasing-overlay/)
- [Trello Cards Api Phrasing Overlay](https://apis.io/overlays/trello/trello-cards-api-phrasing-overlay/)
- [Trello Checklists Api Phrasing Overlay](https://apis.io/overlays/trello/trello-checklists-api-phrasing-overlay/)
- [Trello Custom Fields Api Phrasing Overlay](https://apis.io/overlays/trello/trello-custom-fields-api-phrasing-overlay/)
- [Trello Emoji Api Phrasing Overlay](https://apis.io/overlays/trello/trello-emoji-api-phrasing-overlay/)
- [Trello Enterprises Api Phrasing Overlay](https://apis.io/overlays/trello/trello-enterprises-api-phrasing-overlay/)
- [Trello Labels Api Phrasing Overlay](https://apis.io/overlays/trello/trello-labels-api-phrasing-overlay/)
- [Trello Lists Api Phrasing Overlay](https://apis.io/overlays/trello/trello-lists-api-phrasing-overlay/)
- [Trello Members Api Phrasing Overlay](https://apis.io/overlays/trello/trello-members-api-phrasing-overlay/)
- [Trello Notifications Api Phrasing Overlay](https://apis.io/overlays/trello/trello-notifications-api-phrasing-overlay/)
- [Trello Organizations Api Phrasing Overlay](https://apis.io/overlays/trello/trello-organizations-api-phrasing-overlay/)
- [Trello Plugins Api Phrasing Overlay](https://apis.io/overlays/trello/trello-plugins-api-phrasing-overlay/)
- [Trello Rest Api Overlay](https://apis.io/overlays/trello/trello-rest-api-overlay/)
- [Trello Search Api Phrasing Overlay](https://apis.io/overlays/trello/trello-search-api-phrasing-overlay/)
- [Trello Tokens Api Phrasing Overlay](https://apis.io/overlays/trello/trello-tokens-api-phrasing-overlay/)
- [Trello Webhooks Api Phrasing Overlay](https://apis.io/overlays/trello/trello-webhooks-api-phrasing-overlay/)

#### Governance rules (3)

Spectral rulesets for the provider's contracts.

- [Trello — asyncapi rules](https://apis.io/rules/trello/trello-asyncapi-spectral-rules/)
- [Trello — jsonschema rules](https://apis.io/rules/trello/trello-jsonschema-spectral-rules/)
- [Trello API Rules](https://apis.io/rules/trello/trello-spectral-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Trello Authentication](https://apis.io/security/trello/trello-authentication/)
- [Trello Domain Security](https://apis.io/security/trello/trello-domain-security/)
- [Trello Trust Center](https://apis.io/security/trello/trello-trust-center/)
- [Trello Vulnerability Disclosure](https://apis.io/security/trello/trello-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Trello Scopes](https://apis.io/scopes/trello/trello-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Trello Plans Pricing](https://apis.io/plans/trello/trello-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Trello Rate Limits](https://apis.io/rate-limits/trello/trello-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Trello Finops](https://apis.io/finops/trello/trello-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://trello.com/)
- [Documentation](https://developer.atlassian.com/cloud/trello/rest/)
- [Getting started](https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/)
- [API reference](https://developer.atlassian.com/cloud/trello/rest/)
- [Pricing](https://trello.com/pricing)
- [Sign up](https://trello.com/signup)
- [Support](https://support.atlassian.com/trello/)
- [Blog](https://www.atlassian.com/blog/trello)
- [Terms of service](https://www.atlassian.com/legal/cloud-terms-of-service)
- [Privacy policy](https://www.atlassian.com/legal/privacy-policy)
- [GitHub](https://github.com/trello)
- [Status](https://trello.status.atlassian.com/)

## API Evangelist rating

**Kin Score 73.3** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 66.5 |
| Contract governance | 45.5 |
| Operational transparency | 97.4 |
| Developer ergonomics | 66.1 |
| Access clarity | 76.3 |

**Agent readiness 28.7** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | mostly (partial credit) |

**Regulatory alignment 43.1** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/trello/](https://apis.io/providers/trello/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Trello: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/trello/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
