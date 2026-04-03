# Databricks Genie API Skills

| Property    | Value                                                        |
| ----------- | ------------------------------------------------------------ |
| Name        | databricks-genie                                             |
| Description | AI-powered data assistant — spaces, conversations, and evals |
| Version     | 1.0                                                          |

## Usage

1. Match your task to a file using Quick Lookup below
2. Read the file in `rest/` (HTTP) or `python-sdk/` (SDK)
3. For cross-domain tasks, read multiple files

## Quick Lookup

| Task                                        | File                         |
| ------------------------------------------- | ---------------------------- |
| Create or manage a Genie space              | `genie-spaces-conversations` |
| Start a conversation or send messages       | `genie-spaces-conversations` |
| Execute or download query results           | `genie-spaces-conversations` |
| Send feedback on a message                  | `genie-spaces-conversations` |
| Run benchmark evaluations on a space        | `genie-evals`                |
| Check eval run status or get result details | `genie-evals`                |

## REST API Skills

| File                                 | Scope                                              | Endpoints |
| ------------------------------------ | -------------------------------------------------- | --------- |
| `rest/genie-spaces-conversations.md` | Spaces, conversations, messages, queries, feedback | 17        |
| `rest/genie-evals.md`                | Benchmark evaluation runs and results              | 5         |

## Python SDK Skills

| File                                       | Key Clients |
| ------------------------------------------ | ----------- |
| `python-sdk/genie-spaces-conversations.md` | `w.genie`   |
| `python-sdk/genie-evals.md`                | `w.genie`   |

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
