# Databricks Marketplace API Skills

| Property    | Value                                                             |
| ----------- | ----------------------------------------------------------------- |
| Name        | databricks-marketplace                                            |
| Description | Browse, install, publish, and manage data products on Marketplace |
| Version     | 1.0                                                               |

## Usage

1. Match your task to a file using Quick Lookup below
2. Read the file in `rest/` (HTTP) or `python-sdk/` (SDK)
3. For cross-domain tasks, read multiple files

## Quick Lookup

| Task                                     | File                     |
| ---------------------------------------- | ------------------------ |
| Browse or search listings as a consumer  | `mkt-consumer`           |
| Install or uninstall a data product      | `mkt-consumer`           |
| Request personalized access to a listing | `mkt-consumer`           |
| View providers or fulfillment details    | `mkt-consumer`           |
| Create or manage a provider profile      | `mkt-provider-listings`  |
| Publish, update, or delete a listing     | `mkt-provider-listings`  |
| Upload files for a listing               | `mkt-provider-listings`  |
| Handle incoming personalization requests | `mkt-provider-listings`  |
| View provider analytics dashboards       | `mkt-provider-listings`  |
| Create or manage a private exchange      | `mkt-provider-exchanges` |
| Add/remove listings from an exchange     | `mkt-provider-exchanges` |
| Control exchange access with filters     | `mkt-provider-exchanges` |

## REST API Skills

| File                             | Scope                                                         | Endpoints |
| -------------------------------- | ------------------------------------------------------------- | --------- |
| `rest/mkt-consumer.md`           | Browse listings, install products, personalization, providers | 17        |
| `rest/mkt-provider-listings.md`  | Provider profiles, listings, files, analytics dashboards      | 20        |
| `rest/mkt-provider-exchanges.md` | Private exchanges, listing associations, filters              | 13        |

## Python SDK Skills

| File                                   | Key Clients                                                                                                                                          |
| -------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| `python-sdk/mkt-consumer.md`           | `w.consumer_listings`, `w.consumer_installations`, `w.consumer_fulfillments`, `w.consumer_personalization_requests`, `w.consumer_providers`          |
| `python-sdk/mkt-provider-listings.md`  | `w.provider_listings`, `w.provider_files`, `w.provider_providers`, `w.provider_personalization_requests`, `w.provider_provider_analytics_dashboards` |
| `python-sdk/mkt-provider-exchanges.md` | `w.provider_exchanges`, `w.provider_exchange_filters`                                                                                                |

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
