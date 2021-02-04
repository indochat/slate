---
title: SID9 API

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='#'>Powered by IndoChat</a>

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the SID9 API! You can use our API to access SID9 API endpoints, which can create SID9 Code.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: Basic api_key"
```

> Make sure to replace `api_key` with your API key(base64(account:pw)).

`Authorization: Basic api_key`

<aside class="notice">
You must replace <code>api_key</code> with your personal API key.
</aside>

# SID9

## Create SID9

### HTTP Request

`GET http://example.com/v1/SID9`

### Body Data

Parameter | Required | Description
---------- | ------- | -----------
content | true | SID9 code content (what you want in it)

```shell
curl --location --request POST 'https://example.com/v1/SID9' \
--header 'Content-Type: application/json' \
--header 'Authorization: Basic api_key' \
--data-raw '{
	"content":"test data"
}'
```

> The above command returns JSON structured like this:

```json
{
    "sid9_code": "some base64 code...",
    "quota": 49
}
```

This endpoint create SID9 code.
