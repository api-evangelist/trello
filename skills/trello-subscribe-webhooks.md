---
name: trello-subscribe-webhooks
description: >-
  Subscribe to Trello change events by registering a webhook against a board, list, card or
  member, verify the callback, and validate the HMAC signature on delivery. Use when an
  agent needs to react to Trello changes instead of polling.
api: Trello REST API
base_url: https://api.trello.com/1
operations:
  - post-webhooks
  - post-tokens-token-webhooks
  - get-tokens-token-webhooks
  - get-webhooks-id
  - put-webhooks-id
  - delete-webhooks-id
generated: '2026-09-17'
method: generated
source: >-
  openapi/trello-rest-api-openapi.json,
  https://developer.atlassian.com/cloud/trello/guides/rest-api/webhooks/,
  asyncapi/trello-webhooks-asyncapi.yml
---

# Subscribe to Trello webhooks

## Pick the right create route — this depends on your auth

- **OAuth 2.0 bearer token:** use `post-webhooks` — `POST /1/webhooks`, with the token in
  `Authorization: Bearer`. The nested route below will not work.
- **Legacy Trello Auth key+token:** use `post-tokens-token-webhooks` —
  `POST /1/tokens/{token}/webhooks?key={key}`.

Getting this wrong is the single most common Trello webhook failure.

## Scopes (OAuth 2.0 only)

The access token must be able to **read** the model you want to watch, or creation fails
with `400` or `403`:

| `idModel` type | Required scope |
|---|---|
| Board, List, or Card | `read:board:trello` |
| Workspace (Organization) | `read:organization:trello` |
| Member | `read:member:trello` |
| Enterprise | `read:enterprise:trello` |

Power-Up OAuth 2.0 clients are additionally **workspace-restricted**: the `idModel` must
belong to a workspace the token was authorized for, or you get `403`.

## Steps

1. **Stand up the callback first.** Trello validates it at registration time by sending a
   `HEAD` request. Your endpoint must answer `200` to `HEAD` **before** you call create, or
   registration fails.

2. **Register.** Send `callbackURL`, `idModel` and `description`. Keep the returned webhook
   `id`.

3. **Validate every delivery.** Trello signs each callback with an HMAC-SHA1 digest in the
   `X-Trello-Webhook` header, computed over the request body concatenated with the callback
   URL and keyed on your application secret. Reject anything that does not verify — the
   callback URL is public.

4. **Filter on your side.** A webhook watches exactly one model and fires for **every**
   action on it. There is no server-side event-type filter. The payload carries `action`,
   `model` and `webhook`; branch on `action.type`.

5. **Acknowledge fast.** Return `200` to the `POST`. Do the work asynchronously.

6. **Audit and clean up.** `get-tokens-token-webhooks` lists every webhook a token owns —
  run it periodically, because orphaned webhooks from earlier runs keep delivering.
  `delete-webhooks-id` removes one, permanently.

## Budget

Webhook deliveries are subject to Trello's throughput limits, and the create/list/delete
calls count against the ordinary 300-per-10s key and 100-per-10s token budgets. No
`RateLimit-*` headers exist; a 429 body carries `API_KEY_LIMIT_EXCEEDED` or
`API_TOKEN_LIMIT_EXCEEDED`.

## Undoing it

`delete-webhooks-id` is permanent but harmless — re-register to restore. There is no
partial "pause"; `put-webhooks-id` can set `active=false`, which is the reversible way to
stop deliveries without losing the registration.
