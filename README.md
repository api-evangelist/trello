# trello (trello)

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

Trello is a web-based, kanban-style, list-making application that allows users to organize tasks, projects, and workflows using boards, lists, and cards.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/trello/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/trello/refs/heads/main/apis.yml)

## Timestamps

- **Modified:** 2026-05-19

## APIs

### Trello REST API

The Trello REST API provides programmatic access to Trello boards, lists, cards, members, labels, checklists, and other resources that make up the Trello project management platform. Developers can create, read, update, and delete Trello objects, manage team collaboration workflows, and automate task management processes. The API uses key and token based authentication and returns JSON responses for all endpoints.

- **Human URL:** [https://developer.atlassian.com/cloud/trello/rest/](https://developer.atlassian.com/cloud/trello/rest/)
- **Base URL:** `https://api.trello.com`

#### Tags

- Atlassian
- Boards
- Cards
- Collaboration
- Kanban
- Project Management
- Task Management

#### Properties

- [Documentation](https://developer.atlassian.com/cloud/trello/rest/)
- [OpenAPI](openapi/trello-rest-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/trello-rest-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trello-rest-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Trello Webhooks API

The Trello Webhooks API allows developers to receive real-time notifications when changes occur on Trello models such as boards, lists, and cards. Rather than polling the REST API for updates, webhooks push event data to a specified callback URL via HTTP POST requests containing JSON payloads. Webhook requests are signed with HMAC-SHA1 for verification, and webhooks are scoped to the permissions of the token used to create them.

- **Human URL:** [https://developer.atlassian.com/cloud/trello/guides/rest-api/webhooks/](https://developer.atlassian.com/cloud/trello/guides/rest-api/webhooks/)
- **Base URL:** `https://api.trello.com`

#### Tags

- Events
- Notifications
- Real-Time
- Webhooks

#### Properties

- [Documentation](https://developer.atlassian.com/cloud/trello/guides/rest-api/webhooks/)
- [AsyncAPI](asyncapi/trello-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/trello-rest-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trello-rest-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Trello Power-Ups

Trello Power-Ups are a framework for extending and integrating with the Trello platform. Power-Ups allow developers to add custom functionality to Trello boards, including custom fields, board buttons, card buttons, card badges, and card detail sections. The Power-Up framework provides a client library with utilities and helpers for interacting with the Trello interface, managing authorization, and accessing the REST API from within the Power-Up context.

- **Human URL:** [https://developer.atlassian.com/cloud/trello/power-ups/](https://developer.atlassian.com/cloud/trello/power-ups/)
- **Base URL:** `https://api.example.com`

#### Tags

- Customization
- Extensions
- Integrations
- Plugins

#### Properties

- [Documentation](https://developer.atlassian.com/cloud/trello/power-ups/)
- [Postman Collection](collections/trello-rest-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/trello-rest-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/trello)
- [LinkedIn](https://www.linkedin.com/company/atlassian)
- [JSON-LD](json-ld/trello-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/trello-board-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/trello-card-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/trello-webhook-payload-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/trello-board-structure.json)
- [JSON Structure](json-structure/trello-card-structure.json)
- [Spectral Rules](rules/trello-spectral-rules.yml)
- [Vocabulary](vocabulary/trello-vocabulary.yml)
- [Features](undefined)
