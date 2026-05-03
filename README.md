# Trello

Trello is a visual collaboration and project management platform, now part of Atlassian, that organizes work into boards, lists, and cards. The developer platform provides REST APIs, webhooks, and a Power-Up framework for building integrations and extending Trello functionality.

**Website:** [https://trello.com](https://trello.com)  
**API Docs:** [https://developer.atlassian.com/cloud/trello/rest/](https://developer.atlassian.com/cloud/trello/rest/)  
**Developer Portal:** [https://developer.atlassian.com/cloud/trello/](https://developer.atlassian.com/cloud/trello/)

## APIs

### Trello REST API
The Trello REST API provides programmatic access to boards, lists, cards, members, labels, checklists, and other resources. Authentication uses API key and token query parameters.

- **Base URL:** `https://api.trello.com`
- **Authentication:** API Key + Token (query params)
- **OpenAPI:** [openapi/trello-rest-api-openapi.yml](openapi/trello-rest-api-openapi.yml)

### Trello Webhooks API
Real-time notifications when Trello models change, delivered via HTTP POST to a callback URL. Webhook requests are signed with HMAC-SHA1.

- **AsyncAPI:** [asyncapi/trello-webhooks-asyncapi.yml](asyncapi/trello-webhooks-asyncapi.yml)

### Trello Power-Ups
Framework for extending Trello boards with custom fields, buttons, badges, and third-party integrations.

- **Docs:** [https://developer.atlassian.com/cloud/trello/power-ups/](https://developer.atlassian.com/cloud/trello/power-ups/)

## Artifacts

| Type | File |
|---|---|
| OpenAPI | [openapi/trello-rest-api-openapi.yml](openapi/trello-rest-api-openapi.yml) |
| AsyncAPI | [asyncapi/trello-webhooks-asyncapi.yml](asyncapi/trello-webhooks-asyncapi.yml) |
| JSON Schema (Board) | [json-schema/trello-board-schema.json](json-schema/trello-board-schema.json) |
| JSON Schema (Card) | [json-schema/trello-card-schema.json](json-schema/trello-card-schema.json) |
| JSON Schema (Webhook Payload) | [json-schema/trello-webhook-payload-schema.json](json-schema/trello-webhook-payload-schema.json) |
| JSON Structure (Board) | [json-structure/trello-board-structure.json](json-structure/trello-board-structure.json) |
| JSON Structure (Card) | [json-structure/trello-card-structure.json](json-structure/trello-card-structure.json) |
| JSON-LD Context | [json-ld/trello-context.jsonld](json-ld/trello-context.jsonld) |
| Spectral Rules | [rules/trello-spectral-rules.yml](rules/trello-spectral-rules.yml) |
| Vocabulary | [vocabulary/trello-vocabulary.yml](vocabulary/trello-vocabulary.yml) |

## Capabilities

### Shared Definitions

| File | Description |
|---|---|
| [capabilities/shared/trello-rest-api.yaml](capabilities/shared/trello-rest-api.yaml) | Full Trello REST API consumed definition (boards, cards, lists, members, search, webhooks) |

### Workflow Capabilities

| File | Description |
|---|---|
| [capabilities/project-management.yaml](capabilities/project-management.yaml) | Unified project management capability for teams (boards, cards, lists, members, search) |

## Examples

- [examples/trello-get-board-cards-example.json](examples/trello-get-board-cards-example.json)

## Common Properties

- [Developer Portal](https://developer.atlassian.com/cloud/trello/)
- [Documentation](https://developer.atlassian.com/cloud/trello/rest/)
- [Privacy Policy](https://www.atlassian.com/legal/privacy-policy)
- [Terms of Service](https://www.atlassian.com/legal/cloud-terms-of-service)
- [Support](https://support.atlassian.com/trello/)

## Maintainers

**FN:** Kin Lane  
**Email:** kin@apievangelist.com

## Tags

Atlassian, Boards, Cards, Collaboration, Kanban, Project Management, Task Management
