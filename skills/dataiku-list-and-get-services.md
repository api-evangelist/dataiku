---
name: dataiku-list-and-get-services
description: Retrieve a summary of all deployed services and then fetch detailed information for each service.
api: openapi/dataiku-services-api-openapi.yml
operations:
- listServices
- getService
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/dataiku-services-api-openapi.yml ; every operationId checked against the contract
---

# dataiku-list-and-get-services

Retrieve a summary of all deployed services and then fetch detailed information for each service.

## Steps

1. 1. Call `listServices` – no query parameters; include the `Authorization` header with the API key.
2. 2. For each `serviceId` returned, call `getService` – path parameter `serviceId`; include the `Authorization` header.

## Rules

- Authentication: Provide the API key in the `Authorization` header (apiKeyAuth).
- No rate limiting is documented; exhaustion returns no specific HTTP code.
