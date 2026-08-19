---
name: conga-authenticate
description: Mint an OAuth 2.0 access token for the Conga Advantage Platform REST API and make an authenticated call, in the correct region.
api: Conga Advantage Platform REST API
generated: '2026-08-13'
method: generated
source: authentication/conga-authentication.yml, scopes/conga-scopes.yml, well-known/conga-rls-na-openid-configuration.json
operations:
  - POST /api/v1/auth/connect/token
  - GET /api/user-management/v1/users
---

# Authenticate against the Conga Advantage Platform

Every Conga API call carries `Authorization: Bearer <token>`. There is no API-key
mode. Get this wrong and you will read the platform's most common error: a bare
`401` with a `{ "Message": ... }` body and no machine-readable code.

## 1. Pick the region

The platform is regionally partitioned and **tokens are not portable across
regions**. Use the login host that matches the tenant:

| Region | Authorization server | API gateway |
| --- | --- | --- |
| NA | `https://login-rls.congacloud.com/api/v1/auth` | `https://rls.congacloud.com` |
| EU | `https://login.congacloud.eu/api/v1/auth` | `https://rls.congacloud.eu` |
| AU | `https://login.congacloud.au/api/v1/auth` | `https://rls.congacloud.au` |

Each publishes OIDC discovery at
`<authorization server>/.well-known/openid-configuration` — read it rather than
hard-coding endpoints.

## 2. Mint the token (client_credentials)

```
POST https://login-rls.congacloud.com/api/v1/auth/connect/token
Content-Type: application/x-www-form-urlencoded

grant_type=client_credentials
&client_id=<integration user client id>
&client_secret=<integration user secret>
&scope=api.user-management api.data
```

Credentials belong to an **Integration User**, created and rotated through
`GET /api/user-management/v1/users/{integrationUserId}/secret` and
`PATCH /api/user-management/v1/users/{integrationUserId}/secret`.

Ask only for the scopes you need. The scopes are real and published in the
discovery document, one per service: `api.cart`, `api.catalog`, `api.quote`,
`api.order`, `api.document-management`, `api.user-management`, `api.metadata`,
`api.data`, `api.localization`, `api.revenue-admin`, `api.custom-api`,
`api.email`, `doc-gen.composer`, `sign`, `sign.provisioning`. See
`scopes/conga-scopes.yml` for the service each one maps to.

## 3. Call the API

```
GET https://rls.congacloud.com/api/user-management/v1/users?limit=50&page=1
Authorization: Bearer <access_token>
user-id: <platform user id>
```

On an API-to-API connection also send the `user-id` header — the platform
resolves the caller's permissions from it, and omitting it produces a `403` that
looks like a scope problem but is not.

## Gotchas

- The OpenAPI documents declare a single `apiKey` scheme named `Bearer` in the
  `Authorization` header. That is an artifact of the generator, not a second auth
  mode — it is the same OAuth bearer token.
- `page` cannot be sent without `limit`. Defaults are `page=1`, `limit=1000`
  (max 10000). Read the total off the `Content-Range` response header.
- An empty collection returns `204`, not `200` with an empty array.
- Rate limits are 100 req/s in production and 25 req/s in development; exhaustion
  returns `429`. No `RateLimit-*` headers are published — back off on the status.
