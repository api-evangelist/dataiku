---
name: dataiku-create-and-get-project
description: Create a new Dataiku project and then retrieve its details.
api: openapi/dataiku-projects-api-openapi.yml
operations:
- createProject
- getProject
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/dataiku-projects-api-openapi.yml ; every operationId checked against the contract
---

# dataiku-create-and-get-project

Create a new Dataiku project and then retrieve its details.

## Steps

1. 1. Call `createProject` with the required Authorization header and the request body fields defined in the contract.
2. 2. Call `getProject` with the required Authorization header and the path parameter `projectKey` returned from the creation step.

## Rules

- Auth: Include an `Authorization` header with the API key (apiKeyAuth).
