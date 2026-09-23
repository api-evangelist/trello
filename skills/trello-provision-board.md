---
name: trello-provision-board
description: >-
  Stand up a new Trello board with its lists and labels from scratch, using the Trello
  REST API v1. Use when an agent must create a working board structure (for example a
  kanban pipeline or an intake queue) rather than operate on one that already exists.
api: Trello REST API
base_url: https://api.trello.com/1
operations:
  - post-boards
  - post-boards-id-lists
  - post-boards-id-labels
  - get-boards-id-lists
  - get-boards-id-labels
  - put-boards-id
  - put-boards-id-members
generated: '2026-09-17'
method: generated
source: openapi/trello-rest-api-openapi.json + conventions/trello-conventions.yml
---

# Provision a Trello board

## Before you call anything

- **Auth.** Either `key` + `token` as query parameters, or an OAuth 2.0 bearer token in
  `Authorization`. Board creation needs `write:board:trello`; inviting members needs
  `write:board:membership:trello`.
- **There is no idempotency mechanism.** Trello publishes no `Idempotency-Key` header and
  no dedup window. If `post-boards` times out you do **not** know whether the board was
  created. Before retrying, call `get-members-id-boards` for the authenticated member and
  look for a board with the name you sent.
- **Rate budget.** 300 requests per 10 seconds per API key, 100 per 10 seconds per token.
  No `RateLimit-*` or `Retry-After` headers exist — you cannot read your remaining budget,
  only discover exhaustion as a 429. More than 200 429s on one key in a 10s window locks
  that key out for the rest of the window, so back off rather than retry hard.

## Steps

1. **Create the board.** `post-boards` — `POST /1/boards/`.
   Send `name` (required) and, if the board belongs to a workspace, `idOrganization`.
   Set `defaultLists=false` unless you want Trello's default To Do / Doing / Done; you are
   about to create your own.
   Keep the returned `id` — every later call is anchored to it.

2. **Create the lists, left to right.** `post-boards-id-lists` —
   `POST /1/boards/{id}/lists`, once per column, with `name` and `pos`.
   `pos` accepts `top`, `bottom`, or a float. Creating in order with `pos=bottom` gives you
   left-to-right ordering without computing positions.

3. **Create the labels.** `post-boards-id-labels` — `POST /1/boards/{id}/labels`, with
   `name` and `color`. Colors come from the `Color` schema in the spec.

4. **Verify what you built.** `get-boards-id-lists` and `get-boards-id-labels`. Do this
   even on a clean run — it is the only confirmation you have, and it is how you detect a
   partially-applied provisioning after a timeout.

5. **Invite people (optional).** `put-boards-id-members` — `PUT /1/boards/{id}/members` by
   email, or `put-boards-id-members-idmember` for a known member id.

## Undoing it

Board creation is reversible: `put-boards-id` with `closed=true` closes the board, and the
same operation with `closed=false` reopens it, with no time limit. `delete-boards-id` is
**permanent** — prefer closing.

## Errors you will actually see

- `400` — missing or invalid `name`, or an `idOrganization` you cannot write to.
- `401` — plain-text body `invalid token`. The user revoked access; re-authorize.
  Do not retry.
- `403` — a plan or object limit was reached (free workspaces cap at 10 open boards), or
  an OAuth 2.0 Power-Up client reached outside its authorized workspace.
- `429` — JSON body with `API_KEY_LIMIT_EXCEEDED` or `API_TOKEN_LIMIT_EXCEEDED`. The
  symbolic code tells you which ceiling you hit; there is no header to read.
