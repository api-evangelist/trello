# trello (trello)

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
