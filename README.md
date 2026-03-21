# Trello (trello)
Trello is a visual collaboration and project management platform, now part of Atlassian, that organizes work into boards, lists, and cards. Their developer platform provides REST APIs, webhooks, and a Power-Up framework for building integrations and extending Trello functionality.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/trello/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Project Management, Kanban, Collaboration, Task Management, Atlassian, Webhooks, Integrations

## Timestamps

- **Created:** 2025-03-05
- **Modified:** 2026-03-20

## APIs

### Trello REST API
The Trello REST API provides programmatic access to Trello boards, lists, cards, members, labels, checklists, and other resources that make up the Trello project management platform. Developers can create, read, update, and delete Trello objects, manage team collaboration workflows, and automate task management processes. The API uses key and token based authentication and returns JSON responses for all endpoints.

**Human URL:** [https://developer.atlassian.com/cloud/trello/rest/](https://developer.atlassian.com/cloud/trello/rest/)


#### Tags:

 - Project Management, Kanban, Boards, Cards, Collaboration, Task Management, Atlassian

#### Properties

- [Documentation](https://developer.atlassian.com/cloud/trello/rest/)
- [OpenAPI](openapi/trello-rest-api-openapi.yml)

### Trello Webhooks API
The Trello Webhooks API allows developers to receive real-time notifications when changes occur on Trello models such as boards, lists, and cards. Rather than polling the REST API for updates, webhooks push event data to a specified callback URL via HTTP POST requests containing JSON payloads. Webhook requests are signed with HMAC-SHA1 for verification, and webhooks are scoped to the permissions of the token used to create them.

**Human URL:** [https://developer.atlassian.com/cloud/trello/guides/rest-api/webhooks/](https://developer.atlassian.com/cloud/trello/guides/rest-api/webhooks/)


#### Tags:

 - Webhooks, Events, Notifications, Real-Time

#### Properties

- [Documentation](https://developer.atlassian.com/cloud/trello/guides/rest-api/webhooks/)
- [AsyncAPI](asyncapi/trello-webhooks-asyncapi.yml)

### Trello Power-Ups
Trello Power-Ups are a framework for extending and integrating with the Trello platform. Power-Ups allow developers to add custom functionality to Trello boards, including custom fields, board buttons, card buttons, card badges, and card detail sections. The Power-Up framework provides a client library with utilities and helpers for interacting with the Trello interface, managing authorization, and accessing the REST API from within the Power-Up context.

**Human URL:** [https://developer.atlassian.com/cloud/trello/power-ups/](https://developer.atlassian.com/cloud/trello/power-ups/)


#### Tags:

 - Extensions, Plugins, Integrations, Customization

#### Properties

- [Documentation](https://developer.atlassian.com/cloud/trello/power-ups/)

## Common Properties

- [Portal](https://developer.atlassian.com/cloud/trello/)
- [Documentation](https://developer.atlassian.com/cloud/trello/rest/)
- [Website](https://trello.com/)
- [PrivacyPolicy](https://www.atlassian.com/legal/privacy-policy)
- [TermsOfService](https://www.atlassian.com/legal/cloud-terms-of-service)
- [Support](https://support.atlassian.com/trello/)
- [Blog](https://blog.trello.com/)
- [Login](https://trello.com/login)

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
