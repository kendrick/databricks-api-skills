# Databricks Model Serving API Skills

| Property    | Value                                                                    |
| ----------- | ------------------------------------------------------------------------ |
| Name        | databricks-model-serving                                                 |
| Description | Create, configure, query, and manage model serving endpoints             |
| Version     | 1.0                                                                      |

## Usage

1. Match your task to a file using Quick Lookup below
2. Read the file in `rest/` (HTTP) or `python-sdk/` (SDK)

## Quick Lookup

| Task                                                    | File                |
| ------------------------------------------------------- | ------------------- |
| Create, list, get, or delete a serving endpoint         | `serving-endpoints` |
| Update endpoint config, rate limits, or AI Gateway      | `serving-endpoints` |
| Create or update provisioned throughput endpoints        | `serving-endpoints` |
| Query a serving endpoint                                | `serving-endpoints` |
| Get logs, metrics, or OpenAPI schema                    | `serving-endpoints` |
| Manage serving endpoint permissions                     | `serving-endpoints` |
| Update tags or notification settings                    | `serving-endpoints` |

## REST API Skills

| File                            | Scope                                                              | Endpoints |
| ------------------------------- | ------------------------------------------------------------------ | --------- |
| `rest/serving-endpoints.md`     | CRUD, config, AI Gateway, provisioned throughput, query, permissions | 20        |

## Python SDK Skills

| File                                  | Key Clients            |
| ------------------------------------- | ---------------------- |
| `python-sdk/serving-endpoints.md`     | `w.serving_endpoints`  |

## Auth

### REST

```
Authorization: Bearer <PAT-or-OAuth-token>
Base URL: https://<workspace-host>
```

### Python SDK

```python
from databricks.sdk import WorkspaceClient
w = WorkspaceClient()  # auto-detects from env or .databrickscfg
```
