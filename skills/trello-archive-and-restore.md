---
name: trello-archive-and-restore
description: >-
  Remove Trello work safely and put it back. Trello's destructive surface is archive-based
  and reversible, with a handful of genuinely permanent deletes — this skill tells an agent
  which is which before it acts. Use for any cleanup, bulk-close or rollback task.
api: Trello REST API
base_url: https://api.trello.com/1
operations:
  - put-cards-id
  - put-lists-id-closed
  - post-lists-id-archiveallcards
  - post-lists-id-moveallcards
  - put-boards-id
  - get-lists-id-cards
  - delete-cards-id
  - delete-boards-id
generated: '2026-09-17'
method: generated
source: openapi/trello-rest-api-openapi.json + conventions/trello-conventions.yml (reversibility)
---

# Archive and restore in Trello

## The rule

**Archive, do not delete.** In Trello almost every "remove" is a boolean flip that the same
operation can flip back, with no time limit. The deletes are the exceptions, and they are
irreversible.

| Action | Operation | Reversible? | How to reverse |
|---|---|---|---|
| Archive a card | `put-cards-id` with `closed=true` | Yes, unlimited | same op, `closed=false` |
| Archive a list | `put-lists-id-closed` with `value=true` | Yes, unlimited | same op, `value=false` |
| Archive every card in a list | `post-lists-id-archiveallcards` | Yes, but **only if you saved the ids** | `put-cards-id` `closed=false`, per card |
| Close a board | `put-boards-id` with `closed=true` | Yes, unlimited | same op, `closed=false` |
| Delete a card | `delete-cards-id` | **No** | — |
| Delete a board | `delete-boards-id` | **No** | — |
| Delete a checklist / label / webhook | `delete-checklists-id`, `delete-labels-id`, `delete-webhooks-id` | **No** | recreate by hand |

## The trap: archiveAllCards

`post-lists-id-archiveallcards` archives an unbounded number of cards in one call, and the
response does **not** return the ids of what it archived. There is no bulk unarchive.

So: **call `get-lists-id-cards` first and keep the ids.** Without that snapshot the
operation is effectively irreversible even though each individual card is not. If the list
is large, prefer `post-lists-id-moveallcards` into a holding list — moving is trivially
reversible and needs no snapshot.

## Before any destructive call

- **No dry-run mode exists.** Trello publishes no preview/simulate flag on any write. The
  snapshot in the step above is your only rehearsal.
- **No idempotency.** A retried archive is harmless (it is a set-to-true, not a toggle), but
  a retried `post-cards` or `post-lists-id-moveallcards` is not. Know which you are retrying.
- **Leave a trail.** `post-cards-id-actions-comments` on an affected card, or a comment on a
  tracking card, is the only record a human will have of why an agent archived something.

## Errors

- `401` — plain-text `invalid token`; the user revoked access. Re-authorize, do not retry.
- `403` — the token lacks write permission on the board, or an OAuth 2.0 Power-Up client
  reached outside its authorized workspace.
- `404` — the model is already gone. On a cleanup task treat this as success, not failure.
- `429` — back off; the body's symbolic code says whether the key or the token ceiling was
  hit. Bulk cleanup is exactly the workload that trips the 300-per-10s key limit.
