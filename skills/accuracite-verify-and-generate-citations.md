---
name: accuracite-verify-and-generate-citations
description: Verify a set of citations and then generate supporting citations for a claim.
api: openapi/accuracite-openapi.json
operations:
- generateCitations
- verifyCitation
generated: '2026-10-02'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/accuracite-openapi.json ; every operationId checked against the contract
---

# accuracite-verify-and-generate-citations

Verify a set of citations and then generate supporting citations for a claim.

## Steps

1. 1. Call `generateCitations` with the request body fields `claim` and optional `maxResults`.
2. 2. Call `verifyCitation` with the request body field `citations` (the list returned from the previous step).

## Rules

- Auth: Include the API key in the `X-API-Key` header (ApiKeyAuth).
- Idempotency: Both endpoints are POST and do not guarantee idempotent behavior.
