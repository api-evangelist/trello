---
name: trello-triage-card
description: >-
  Create and triage a Trello card end to end — file it into a list, label it, assign it,
  attach context and comment on it — using the Trello REST API v1. This is the marquee
  write flow of the Trello API and the one most agent tasks reduce to.
api: Trello REST API
base_url: https://api.trello.com/1
operations:
  - post-cards
  - get-cards-id
  - put-cards-id
  - post-cards-id-idlabels
  - post-cards-id-idmembers
  - post-cards-id-actions-comments
  - post-cards-id-attachments
  - get-boards-id-labels
  - get-boards-id-members
  - get-lists-id-cards
generated: '2026-09-17'
method: generated
source: openapi/trello-rest-api-openapi.json + conventions/trello-conventions.yml
---

# Triage a Trello card

## Before you call anything

- **Auth.** `key`+`token`, or an OAuth 2.0 bearer token with `write:board:trello`.
- **No idempotency.** A retried `post-cards` creates a **second card**. Before any retry,
  call `get-lists-id-cards` on the destination list and look for your card. If you need
  reliable dedup, write a caller-owned marker into `desc` and search for it first.
- **Ids carry no type prefix.** A Trello id is a bare 24-char hex string, so `idList`,
  `idBoard` and `idMembers` are indistinguishable by shape. Never guess which one an id is.

## Steps

1. **Resolve the destination list id.** You need `idList` and you cannot derive it from a
   list name. Use `get-boards-id-lists` on the board, or `get-search` with a board-scoped
   query.

2. **Create the card.** `post-cards` — `POST /1/cards`.
   Required: `idList`. Useful: `name`, `desc`, `pos`, `due`, `idLabels`, `idMembers`.
   Setting labels and members here saves two round trips over doing it in steps 3 and 4.

3. **Add a label** (if not set at creation). `post-cards-id-idlabels` —
   `POST /1/cards/{id}/idLabels` with `value` = the label id. Label ids are **per board**;
   fetch them with `get-boards-id-labels` and cache per board.

4. **Assign a member.** `post-cards-id-idmembers` — `POST /1/cards/{id}/idMembers` with
   `value` = the member id, resolved via `get-boards-id-members`. Assigning someone who is
   not a board member fails.

5. **Attach context.** `post-cards-id-attachments` — `POST /1/cards/{id}/attachments`,
   either a `url` or a file upload.

6. **Comment.** `post-cards-id-actions-comments` — `POST /1/cards/{id}/actions/comments`
   with `text`. Comments are the audit trail an agent should leave: say what you did and
   why, because Trello gives a human no other view of an agent's reasoning.

7. **Move or update later.** `put-cards-id` — `PUT /1/cards/{id}` changes `idList`
   (the "move to the next column" action), `name`, `desc`, `due`, `dueComplete` and
   `closed`.

## Undoing it

- Archive: `put-cards-id` with `closed=true`. Restore: the same call with `closed=false`,
  no time limit. **Prefer this over deleting.**
- `delete-cards-id` is permanent with no published undelete.
- Removing a label or member is a `DELETE` on the same sub-resource, and is fully reversible
  by re-adding.

## Reading a card back

`get-cards-id` supports `fields=` (a comma-separated allowlist, or `all`). Use it. The
default payload is large, most collection endpoints are unpaginated, and a request that
pulls a board's cards with `actions=all&filter=all` returns `429 API_TOO_MANY_CARDS_REQUESTED`.
