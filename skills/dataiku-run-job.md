---
name: dataiku-run-job
description: Start a new job, then monitor its status until completion.
api: openapi/dataiku-jobs-api-openapi.yml
operations:
- startJob
- getJob
- listJobs
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/dataiku-jobs-api-openapi.yml ; every operationId checked against the contract
---

# dataiku-run-job

Start a new job, then monitor its status until completion.

## Steps

1. 1. Call `startJob` with required body fields as defined in the contract.
2. 2. Call `getJob` with the `jobId` returned from `startJob` to check status.
3. 3. Optionally repeat `getJob` until the job reaches a terminal state.
4. 4. Use `listJobs` to verify the job appears in the project's job list.

## Rules

- Auth: Include the API key in the `Authorization` header as defined by the `apiKeyAuth` scheme.
- Idempotency: `startJob` creates a new job each call; repeat calls will start separate jobs.
- Pagination: `listJobs` supports pagination as described in its response schema.
