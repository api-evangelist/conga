---
name: conga-contract-lifecycle
description: Drive a Conga CLM contract from creation through clauses, obligations, review and activation, including amend and cancel.
api: Conga Advantage Platform REST API
generated: '2026-08-13'
method: generated
source: openapi/conga-contracts.json, openapi/conga-review.json
operations:
  - POST /api/clm/v1/contracts
  - POST /api/clm/v1/contracts/query
  - GET /api/clm/v1/contracts/{contractId}
  - PUT /api/clm/v1/contracts/{contractId}
  - POST /api/clm/v1/contracts/{contractId}/clauses/bulk
  - POST /api/clm/v1/contracts/{contractId}/documents
  - POST /api/clm/v1/clauses/{clauseId}/obligations
  - POST /api/clm/v1/contracts/obligations/fulfillments/query
  - POST /api/clm/v1/contracts/{contractId}/activate
  - POST /api/clm/v1/contracts/{contractId}/amend
  - POST /api/clm/v1/contracts/{contractId}/cancel
  - POST /api/clm/v1/contracts/{contractId}/clone
  - POST /api/clm/v1/contracts/createoffline
  - POST /api/clm/v1/contracts/storeexecuted
  - POST /api/clm/v1/accounts/{accountId}/contracts/hierarchy/query
---

# Run a contract through Conga CLM

Base: `https://rls.congacloud.com` · path prefix `/api/clm/v1`

## Reads are POSTs

This is the single most surprising thing about the CLM service: list and search
operations are `POST .../query`, not `GET`. `POST /api/clm/v1/contracts/query`
returns contract records; `GET /api/clm/v1/contracts/{contractId}` returns one.
The same pattern applies to clause obligations, activity history and account
contract hierarchies. Do not look for a `GET /contracts` — there isn't one.

## 1. Create

```
POST /api/clm/v1/contracts
```

Two alternative entry points exist for contracts that did not originate in
Conga:

- `POST /api/clm/v1/contracts/createoffline` — create the contract and import its
  document. Use `/createoffline/large` above the small-file threshold.
- `POST /api/clm/v1/contracts/storeexecuted` — record an already-signed contract.
  `/storeexecuted/large` for big documents.

Picking the wrong one puts the contract in the wrong lifecycle state; an executed
contract stored as a draft will be routed for signature again.

## 2. Clauses

```
POST   /api/clm/v1/contracts/{contractId}/clauses/bulk
PUT    /api/clm/v1/contracts/{contractId}/clauses/bulk
DELETE /api/clm/v1/contracts/{contractId}/clauses/bulk
POST   /api/clm/v1/contracts/{contractId}/clauses      # read (query)
```

Prefer the bulk forms — single-clause writes on a long agreement are the fastest
way to hit the 100 req/s limit.

## 3. Obligations and fulfillment

Obligations hang off clauses, and fulfillments off obligations:

```
POST /api/clm/v1/clauses/{clauseId}/obligations
POST /api/clm/v1/clauses/{clauseId}/obligations/query
POST /api/clm/v1/contracts/obligations/fulfillments/query
```

`/contracts/obligations/fulfillments/query` is the "what is due" listing — the
one an agent should poll for post-signature obligation tracking.

## 4. Review

Reviews and reviewers live in their own service
(`openapi/conga-review.json`, `/review/...`) and attach to a contract at
`/api/clm/v1/contracts/{contractId}/reviews`.

## 5. Activate, amend, cancel

```
POST /api/clm/v1/contracts/{contractId}/activate
POST /api/clm/v1/contracts/{contractId}/amend
POST /api/clm/v1/contracts/{contractId}/cancel
POST /api/clm/v1/contracts/{contractId}/clone
```

Amendment creates a related record rather than mutating the original — read the
relationship graph with
`POST /api/clm/v1/accounts/{accountId}/contracts/hierarchy/query` (or the
contract-scoped form) instead of assuming a flat list.

## Documents

`POST /api/clm/v1/contracts/{contractId}/documents` adds a contract document.
Authoring against that document happens in X-Author
(`openapi/conga-x-author.json`, a separate host:
`https://xauthor-prod-rls10.congacloud.com`), and signature in Conga Sign — see
`skills/conga-send-for-signature.md`.

## Error handling

CLM declares `400`, `401`, `403`, `404` and `500`. Errors return a bare
`{ "Message": "..." }` with no code — you cannot branch on error identity, so
branch on status and log the message. See `errors/conga-problem-types.yml`.
