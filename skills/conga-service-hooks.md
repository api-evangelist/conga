---
name: conga-service-hooks
description: Register Conga Hooks so the Advantage Platform pushes on data change or on a schedule, instead of polling 2,136 REST operations.
api: Conga Advantage Platform REST API
generated: '2026-08-13'
method: generated
source: openapi/conga-extensibility.json, asyncapi/conga-webhooks.yml
operations:
  - GET /api/extensibility/v1/servicehooks/rules/supported-event-types
  - POST /api/extensibility/v1/servicehooks/rules
  - GET /api/extensibility/v1/servicehooks/rules
  - GET /api/extensibility/v1/servicehooks/rules/{name}
  - PATCH /api/extensibility/v1/servicehooks/rules/{name}
  - DELETE /api/extensibility/v1/servicehooks/rules/{name}
  - GET /api/extensibility/v1/servicehooks/datachangerules/supported-event-types
  - POST /api/extensibility/v1/servicehooks/datachangerules
  - GET /api/extensibility/v1/servicehooks/rules/cancellation/settings
  - PUT /api/extensibility/v1/servicehooks/rules/cancellation/settings
  - GET /api/extensibility/v1/callbacks
  - PUT /api/extensibility/v1/callbacks
---

# Get pushed to instead of polling: Conga Hooks

Base: `https://rls.congacloud.com/api/extensibility/v1` · scope: `api.custom-api`

Conga has no published event catalog and no AsyncAPI document, so the event
surface is easy to miss. It exists, and it is the correct alternative to polling
a platform with a 100 req/s ceiling.

## 1. Ask the tenant what it can fire

```
GET /api/extensibility/v1/servicehooks/rules/supported-event-types
GET /api/extensibility/v1/servicehooks/datachangerules/supported-event-types
```

**Start here, always.** The supported event types are served at runtime from the
tenant and are not published anywhere on developer.conga.com. Any list you carry
in code will drift. Read it, then build against what this tenant actually
supports.

## 2. Create a rule

```
POST /api/extensibility/v1/servicehooks/rules
```

A service hooks rule is either a **data change** rule or a **schedule** rule —
Conga's own description is "Validates and creates the data change or schedule
rule". Data-change rules can also be managed through the narrower
`/servicehooks/datachangerules` family.

Rules are addressed **by name**, not by id:

```
GET    /api/extensibility/v1/servicehooks/rules/{name}
PATCH  /api/extensibility/v1/servicehooks/rules/{name}
DELETE /api/extensibility/v1/servicehooks/rules/{name}
```

Name them deterministically from your own system so re-registration is
idempotent.

## 3. Cancellation tokens

```
GET /api/extensibility/v1/servicehooks/rules/cancellation/settings
PUT /api/extensibility/v1/servicehooks/rules/cancellation/settings
```

Both hook families expose a cancellation-token setting. Conga does not document
the semantics, but the presence of a cancellation token on an event rule implies
a hook can halt or veto the operation that triggered it. Treat hook handlers as
**on the critical path** until you have confirmed otherwise with Conga — a slow
handler may be a slow save.

## 4. Callback contracts are a different thing

```
GET /api/extensibility/v1/callbacks
PUT /api/extensibility/v1/callbacks
GET /api/extensibility/v1/callbacks/modules
```

A callback contract binds a named platform extension point in a module to a
customer **custom-code project and class** running inside Conga. That is
in-platform dispatch, not an outbound HTTP webhook to your service. Do not
confuse the two: `/callbacks` runs your code in Conga, `/servicehooks` reacts to
Conga events.

## What is not published

Payload schemas, signing/verification, retry policy and delivery guarantees are
all undocumented. Verify them against a live tenant before depending on
at-least-once delivery. See `asyncapi/conga-webhooks.yml`.
