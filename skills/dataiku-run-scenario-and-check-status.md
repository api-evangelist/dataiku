---
name: dataiku-run-scenario-and-check-status
description: Run a Dataiku scenario and retrieve its execution status.
api: openapi/dataiku-scenarios-api-openapi.yml
operations:
- runScenario
- getScenarioRunStatus
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/dataiku-scenarios-api-openapi.yml ; every operationId checked against the contract
---

# dataiku-run-scenario-and-check-status

Run a Dataiku scenario and retrieve its execution status.

## Steps

1. 1. Call `runScenario` with the required path parameters `projectKey` and `scenarioId`. Include the `Authorization` header as defined by the `apiKeyAuth` scheme.
2. 2. Call `getScenarioRunStatus` with the same `projectKey` and `scenarioId` to poll the scenario's execution status. Include the `Authorization` header.

## Rules

- Authentication: Provide an API key in the `Authorization` header (apiKeyAuth).
- Idempotency: Not applicable for these operations.
- Pagination: Not applicable for the listed operations.
- Errors: Follow the HTTP status codes returned by the API (e.g., 4xx for client errors, 5xx for server errors).
