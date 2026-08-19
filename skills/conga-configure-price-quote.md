---
name: conga-configure-price-quote
description: Run the Conga CPQ configure-price-quote flow - launch a cart against a business object, add and price line items, apply adjustments, and finalize back to the quote.
api: Conga Advantage Platform REST API
generated: '2026-08-13'
method: generated
source: openapi/conga-cart-v1.json, openapi/conga-catalog.json, openapi/conga-quote.json
operations:
  - POST /api/cart/v1/business-objects/{businessObjectId}/carts/activate
  - GET /api/cart/v1/business-objects/{businessObjectId}/carts/active
  - POST /api/cart/v1/carts/{cartId}/items
  - GET /api/cart/v1/carts/{cartId}/items
  - PATCH /api/cart/v1/carts/{cartId}/items
  - POST /api/cart/v1/carts/{cartId}/adjustments
  - GET /api/cart/v1/carts/{cartId}/applicable-rules
  - GET /api/cart/v1/carts/{cartId}/items/errors
  - GET /api/cart/v1/carts/{cartId}/items/{lineitemId}/waterfallchart
  - POST /api/cart/v1/carts/{cartId}/finalize
  - GET /api/cart/v1/carts/{cartId}/finalize
  - POST /api/cart/v1/carts/{cartId}/abandon
---

# Configure, price and quote with Conga CPQ

Base: `https://rls.congacloud.com` · scopes: `api.cart`, `api.catalog`, `api.quote`

## 1. A cart always belongs to a business object

You do not create a cart in isolation. Launch it against the record it prices —
normally a Quote:

```
POST /api/cart/v1/business-objects/{businessObjectId}/carts/activate
```

`GET /api/cart/v1/business-objects/{businessObjectId}/carts/active` returns the
read-only active cart for that object. If the quote changed underneath you, use
`POST /api/cart/v1/business-objects/{businessObjectId}/carts/reactivate`, which
re-syncs quote fields into the cart.

> `POST /api/cart/v1/business-objects/{businessObjectId}/reactivate` is
> **deprecated** in Conga's own spec, which tells you to use the
> `/carts/reactivate` form. Do not use the deprecated path.

## 2. Add line items

```
POST   /api/cart/v1/carts/{cartId}/items
PATCH  /api/cart/v1/carts/{cartId}/items
GET    /api/cart/v1/carts/{cartId}/items
```

Products come from the catalog service (`api.catalog`): products, categories,
price lists, product groups, option groups and features.

For ramped/term deals use the ramp family
(`/items/ramps`, `/items/{itemId}/ramp-lines`,
`PUT /items/{itemId}/ramp-lines/split`) rather than modelling periods yourself.
Usage pricing lives at `/items/{itemId}/usage-tiers`.

## 3. Check what the rules did

CPQ mutates the cart asynchronously through rules. Before trusting totals:

```
GET /api/cart/v1/carts/{cartId}/applicable-rules
GET /api/cart/v1/carts/{cartId}/applicable-attribute-rules
GET /api/cart/v1/carts/{cartId}/items/errors
```

`/items/errors` returns line-item persistence errors that do **not** surface as a
non-2xx on the write call. Poll it after every batch mutation.

## 4. Discounts and explainability

```
POST /api/cart/v1/carts/{cartId}/adjustments
GET  /api/cart/v1/carts/{cartId}/items/{lineitemId}/waterfallchart
```

The waterfall chart is the price-derivation trace — list price down to net
through every adjustment. It is the right answer to "why is this the price?".

## 5. Finalize

```
POST /api/cart/v1/carts/{cartId}/finalize
GET  /api/cart/v1/carts/{cartId}/finalize
```

Finalizing writes the priced configuration back to the business object. Read the
`GET` form to confirm the finalized state before moving on to document generation
or signature. Abandon a working cart with
`POST /api/cart/v1/carts/{cartId}/abandon`.

## Collaboration

Multi-party carts go out through `/carts/collaboration-request` and come back via
`POST /api/cart/v1/carts/{cartId}/collaboration-request/{id}/submit-for-merge`.
