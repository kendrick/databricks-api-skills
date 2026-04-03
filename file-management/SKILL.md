# Databricks File Management API Skills

| Property    | Value                                                    |
| ----------- | -------------------------------------------------------- |
| Name        | databricks-file-management                               |
| Description | Upload, download, and manage files via Files API or DBFS |
| Version     | 1.0                                                      |

## Usage

1. Match your task to a file using Quick Lookup below
2. Read the file in `rest/` (HTTP) or `python-sdk/` (SDK)
3. **Prefer Files API for new work** — DBFS is legacy

## Quick Lookup

| Task                                          | File        |
| --------------------------------------------- | ----------- |
| Upload or download files on volumes/workspace  | `files-api` |
| Create, list, or delete directories            | `files-api` |
| Get file or directory metadata                 | `files-api` |
| Stream large file uploads (legacy)             | `dbfs-api`  |
| Read/write files on dbfs:/ paths (legacy)      | `dbfs-api`  |
| Move or rename files (legacy only)             | `dbfs-api`  |

## REST API Skills

| File                  | Scope                                           | Endpoints |
| --------------------- | ----------------------------------------------- | --------- |
| `rest/files-api.md`   | Modern Files API — volumes and workspace files  | 8         |
| `rest/dbfs-api.md`    | Legacy DBFS — streaming uploads, file ops       | 10        |

## Python SDK Skills

| File                        | Key Clients |
| --------------------------- | ----------- |
| `python-sdk/files-api.md`   | `w.files`   |
| `python-sdk/dbfs-api.md`    | `w.dbfs`    |

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
