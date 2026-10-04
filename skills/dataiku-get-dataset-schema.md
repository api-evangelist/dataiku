---
name: dataiku-get-dataset-schema
description: Retrieve the schema of a specific dataset within a project.
api: openapi/dataiku-datasets-api-openapi.yml
operations:
- listDatasets
- getDatasetSchema
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/dataiku-datasets-api-openapi.yml ; every operationId checked against the contract
---

# dataiku-get-dataset-schema

Retrieve the schema of a specific dataset within a project.

## Steps

1. 1. Call `listDatasets` with the path parameter `projectKey` to locate the desired dataset.
2. 2. Call `getDatasetSchema` with path parameters `projectKey` and `datasetName` to obtain the dataset's schema.

## Rules

- Include the API key in the `Authorization` header as required by the `apiKeyAuth` scheme.
- All requests must provide the `projectKey` path parameter; `getDatasetSchema` also requires the `datasetName` path parameter.
