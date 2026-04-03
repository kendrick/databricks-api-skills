Title: Update an installation | Consumer Installations API | REST API reference

URL Source: https://docs.databricks.com/api/workspace/consumerinstallations/update

Markdown Content:
## Update an installation

Public preview

`PUT/api/2.1/marketplace-consumer/listings/{listing_id}/installations/{installation_id}`

This is a update API that will update the part of the fields defined in the installation table as well as interact with external services according to the fields not included in the installation table

1.   the token will be rotate if the rotateToken flag is true
2.   the token will be forcibly rotate if the rotateToken flag is true and the tokenInfo field is empty

API scopes (preview):[`marketplace`](https://docs.databricks.com/api/workspace/api/scopes#marketplace)

### Path parameters

[`listing_id`](https://docs.databricks.com/api/workspace/consumerinstallations/update#listing_id)required string

[`installation_id`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation_id)required string

### Request body

[`installation`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation)required object

[`catalog_name`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-catalog_name)string

[`error_message`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-error_message)string

[`id`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-id)string

[`installed_on`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-installed_on)int64

[`listing_id`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-listing_id)string

[`listing_name`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-listing_name)string

[`recipient_type`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-recipient_type)string

Enum: `DELTA_SHARING_RECIPIENT_TYPE_DATABRICKS | DELTA_SHARING_RECIPIENT_TYPE_OPEN`

[`repo_name`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-repo_name)string

[`repo_path`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-repo_path)string

[`share_name`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-share_name)string

[`status`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-status)string

Enum: `INSTALLED | FAILED`

[`token_detail`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-token_detail)object

[`tokens`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-tokens)Array of object

[`rotate_token`](https://docs.databricks.com/api/workspace/consumerinstallations/update#rotate_token)boolean

### Responses

**200** Request completed successfully.

Request completed successfully.

[`installation`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation)object

[`catalog_name`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-catalog_name)string

[`error_message`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-error_message)string

[`id`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-id)string

[`installed_on`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-installed_on)int64

[`listing_id`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-listing_id)string

[`listing_name`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-listing_name)string

[`recipient_type`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-recipient_type)string

Enum: `DELTA_SHARING_RECIPIENT_TYPE_DATABRICKS | DELTA_SHARING_RECIPIENT_TYPE_OPEN`

[`repo_name`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-repo_name)string

[`repo_path`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-repo_path)string

[`share_name`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-share_name)string

[`status`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-status)string

Enum: `INSTALLED | FAILED`

[`token_detail`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-token_detail)object

[`tokens`](https://docs.databricks.com/api/workspace/consumerinstallations/update#installation-tokens)Array of object

# Request samples

JSON

{

"installation":{

"catalog_name":"string",

"error_message":"string",

"id":"string",

"installed_on":0,

"listing_id":"string",

"listing_name":"string",

"recipient_type":"DELTA_SHARING_RECIPIENT_TYP E_DATABRICKS",

"repo_name":"string",

"repo_path":"string",

"share_name":"string",

"status":"INSTALLED",

"token_detail":{

"bearerToken":"string",

"endpoint":"string",

"expirationTime":"string",

"shareCredentialsVersion":0

},

"tokens":[

{

"activation_url":"string",

"created_at":0,

"created_by":"string",

"expiration_time":0,

"id":"string",

"updated_at":0,

"updated_by":"string"

}

]

},

"rotate_token":true

}

# Response samples

200

{

"installation":{

"catalog_name":"string",

"error_message":"string",

"id":"string",

"installed_on":0,

"listing_id":"string",

"listing_name":"string",

"recipient_type":"DELTA_SHARING_RECIPIENT_TYP E_DATABRICKS",

"repo_name":"string",

"repo_path":"string",

"share_name":"string",

"status":"INSTALLED",

"token_detail":{

"bearerToken":"string",

"endpoint":"string",

"expirationTime":"string",

"shareCredentialsVersion":0

},

"tokens":[

{

"activation_url":"string",

"created_at":0,

"created_by":"string",

"expiration_time":0,

"id":"string",

"updated_at":0,

"updated_by":"string"

}

]

}

}
