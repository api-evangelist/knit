---
name: knit-syncs-list-and-trigger
description: List existing syncs and then trigger a new sync.
api: openapi/knit-syncs-api-openapi.yml
operations:
- listSyncs
- triggerSync
generated: '2026-10-20'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/knit-syncs-api-openapi.yml ; every operationId checked against the contract
---

# knit-syncs-list-and-trigger

List existing syncs and then trigger a new sync.

## Steps

1. 1. `listSyncs` – no required fields or headers beyond authentication.
2. 2. `triggerSync` – send the `idempotencyId` header and include any required request body fields as defined by the API.

## Rules

- Include the `Authorization` header with the API key for all requests.
- Send the `idempotencyId` header on the `triggerSync` write operation.
