---
name: conga-provision-users
description: Create, update and deactivate Conga Advantage Platform users in bulk, keyed on your own external identifier, and assign roles and permission groups.
api: Conga Advantage Platform REST API
generated: '2026-08-13'
method: generated
source: openapi/conga-user-management.json
operations:
  - POST /api/user-management/v1/users
  - PUT /api/user-management/v1/users/bulk-upsert
  - PUT /api/user-management/v1/users/bulk-upsert-sync
  - GET /api/user-management/v1/users
  - PATCH /api/user-management/v1/users/{userId}
  - DELETE /api/user-management/v1/users/{userId}
  - PUT /api/user-management/v1/users/{userId}/restore
  - PUT /api/user-management/v1/users/{userId}/roles/{roleId}
  - PUT /api/user-management/v1/users/{userId}/permissiongroups
  - POST /api/user-management/v1/users/{userId}/send-welcome-email
---

# Provision Conga platform users from your system of record

Base: `https://rls.congacloud.com` · scope: `api.user-management`

## Sync users idempotently

Do **not** loop `POST /users` and catch duplicates. Conga's upsert endpoints key
on your own identifier:

```
PUT /api/user-management/v1/users/bulk-upsert
Authorization: Bearer <token>
Content-Type: application/json
```

If a user already exists under the platform record identifier the call updates
it; otherwise it creates it. Use `PUT /api/user-management/v1/users/bulk-upsert-sync`
when you need the result in the same request rather than asynchronously.

`ExternalId` is the most widely used cross-reference field in the whole Conga
catalogue (150 occurrences across the specs) — set it on creation so every later
reconciliation is a lookup, not a search.

## Read the partial-failure response

Bulk endpoints return **`207 Multi-Status`**, not `200`. The body carries the ids
that succeeded *and* an error list for the records that failed validation. A
`207` handled as success will silently drop users. 38 operations across the
platform behave this way.

Bulk create and bulk update are **not supported for the `Integration` user
type** — provision integration users one at a time with `POST /users`.

## Assign authorization

```
PUT /api/user-management/v1/users/{userId}/roles/{roleId}
PUT /api/user-management/v1/users/{userId}/permissiongroups
```

`permissiongroups` **appends** to the user's current groups; use
`DELETE /api/user-management/v1/users/{userId}/permissiongroups` to remove.
Check before writing with
`GET /api/user-management/v1/users/{userId}/roles/{roleId}/exists`.

## Deactivate, do not delete

`DELETE /api/user-management/v1/users/{userId}` deactivates. Reverse it with
`PUT /api/user-management/v1/users/{userId}/restore`.

## CSV path

For a first load: `GET /api/user-management/v1/users/templates/download` returns a
template generated from the tenant's current user metadata, and
`POST /api/user-management/v1/users/upload` accepts the filled `.csv`. The file
is validated first — bad field names fail the whole upload with a message, not a
partial import.

## After creation

`POST /api/user-management/v1/users/{userId}/send-welcome-email` re-sends
credentials when the original address was wrong. Not supported for `Integration`
users.
