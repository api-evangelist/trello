# Trello GraphQL Schema

This document describes a conceptual GraphQL schema for the Trello API. Trello exposes a REST API at `https://api.trello.com/1/` with key/token authentication. This GraphQL schema maps the core Trello domain model into a typed, queryable graph suitable for use with tools that translate GraphQL operations into REST calls or for documentation and tooling purposes.

## Source

- REST API Reference: https://developer.atlassian.com/cloud/trello/rest/
- GitHub Organization: https://github.com/trello
- Developer Documentation: https://developer.atlassian.com/cloud/trello/

## Authentication

Trello uses API key + token authentication. All requests must include:

- `key` — your API key obtained from https://trello.com/app-key
- `token` — an OAuth 1.0a token authorized by a Trello user

## Domain Model Overview

The Trello domain is organized around the following primary entities:

### Boards

A `Board` is the top-level organizational unit in Trello. Each board belongs to a `Workspace` (formerly Organization) and contains `List` objects. Boards support customization via `BoardPreferences`, `BoardBackground`, `BoardPlugin` (Power-Up), `CustomField`, and `Label` definitions. Members are attached via `BoardMembership` records.

### Lists

A `List` belongs to a single `Board` and contains ordered `Card` objects. Lists can be archived but not deleted. `ListPreferences` control per-list behaviors.

### Cards

`Card` is the central unit of work. Cards belong to a `List` and `Board`, and can have `Attachment`, `Checklist`, `Label`, `CustomFieldItem`, `CoverImage`, and `Member` associations. Card history is tracked through `CardAction` records. Cards support `CardAging` visual effects (Premium) and can be filtered via `CardFilter`.

### Members and Organizations

A `Member` represents a Trello user account. `MemberProfile` holds extended user details. Members belong to boards and workspaces through `BoardMembership` and `OrganizationMembership` records. `Organization` (Workspace) aggregates boards and members.

### Actions and Notifications

`Action` records capture every change made to a Trello entity (card moved, member added, comment posted, etc.). `Reaction` objects attach emoji reactions to actions. `Notification` objects deliver action summaries to members.

### Power-Ups

`PowerUp` extends board functionality. Each `PowerUp` declares `PowerUpCapability` entries (card-buttons, board-buttons, card-badges, etc.) and renders UI via `PowerUpIframe`. Power-Ups authenticate using `ClientToken` objects.

### Webhooks

`Webhook` objects subscribe to model-level change events and deliver JSON payloads to a callback URL. Webhook requests are signed with HMAC-SHA1 using the token secret.

### Authentication Tokens and Keys

`Token` objects represent authorized access grants. `TokenPermission` entries describe what models and operations a token may access. `APIKey` identifies the developer application.

### Search

`Search` operations query across boards, cards, members, and organizations. Results are typed as `SearchResult` containing typed sub-result lists.

### Templates

`Template` objects are pre-built board configurations available from the Trello template gallery, organized by `TemplateCategory`.

### Enterprise

`EnterpriseAdmin` provides organization-wide governance capabilities including SSO, member management, and cross-workspace visibility.

## Schema File

See `trello-schema.graphql` for the full GraphQL type definitions.

## Usage Notes

- All IDs are opaque strings (Trello uses alphanumeric IDs, not integers).
- Date fields use ISO 8601 format (`String` typed as datetime).
- Pagination is cursor-based where supported; some list endpoints use `before`/`since`/`limit` parameters.
- Mutations map to REST POST/PUT/DELETE operations on the underlying API.
- `pos` fields represent floating-point position values used for ordering within lists and boards.
