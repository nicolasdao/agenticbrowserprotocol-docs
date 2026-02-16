---
url: https://mintlify.com/docs/api/assistant/search
canonical: https://www.mintlify.com/docs/api/assistant/search
title: "Search documentation - Mintlify"
description: "Perform semantic and keyword searches across your documentation with configurable filtering and pagination."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Assistant

Search documentation

Search...

⌘K

##### API reference

- [Introduction](https://www.mintlify.com/docs/api/introduction)

##### Admin

- [POSTTrigger update](https://www.mintlify.com/docs/api/update/trigger)
- [GETGet update status](https://www.mintlify.com/docs/api/update/status)

##### Agent

- [POSTCreate agent job](https://www.mintlify.com/docs/api/agent/create-agent-job)
- [GETGet agent job by ID](https://www.mintlify.com/docs/api/agent/get-agent-job)
- [GETGet all agent jobs](https://www.mintlify.com/docs/api/agent/get-all-jobs)

##### Assistant

- [POSTAssistant message](https://www.mintlify.com/docs/api/assistant/create-assistant-message-v2)
- [POSTSearch documentation](https://www.mintlify.com/docs/api/assistant/search)

##### Analytics

- [GETGet user feedback](https://www.mintlify.com/docs/api/analytics/feedback)
- [GETGet assistant conversations](https://www.mintlify.com/docs/api/analytics/assistant-conversations)

![US](https://d3gk2c5xim1je2.cloudfront.net/flags/US.svg)

English

Search documentation

cURL
```
curl --request POST \
  --url https://api.mintlify.com/discovery/v1/search/{domain} \
  --header 'Authorization: Bearer <token>' \
  --header 'Content-Type: application/json' \
  --data '
{
  "query": "<string>",
  "pageSize": 10,
  "filter": {
    "version": "<string>",
    "language": "<string>"
  }
}
'
```
200
```
[
  {
    "content": "<string>",
    "path": "<string>",
    "metadata": {}
  }
]
```
POST

/

v1

/

search

/

{domain}

Try it

Search documentation

cURL
```
curl --request POST \
  --url https://api.mintlify.com/discovery/v1/search/{domain} \
  --header 'Authorization: Bearer <token>' \
  --header 'Content-Type: application/json' \
  --data '
{
  "query": "<string>",
  "pageSize": 10,
  "filter": {
    "version": "<string>",
    "language": "<string>"
  }
}
'
```
200
```
[
  {
    "content": "<string>",
    "path": "<string>",
    "metadata": {}
  }
]
```

#### Authorizations

[​](#authorization-authorization)

Authorization

string

header

required

The Authorization header expects a Bearer token. Use an assistant API key (prefixed with `mint_dsc_`). This is a public key safe for use in client-side code. Generate one on the [API keys page](https://dashboard.mintlify.com/settings/organization/api-keys) in your dashboard.

#### Path Parameters

[​](#parameter-domain)

domain

string

required

The domain identifier from your `domain.mintlify.app` URL. Can be found at the end of your dashboard URL. For example, `dashboard.mintlify.com/organization/domain` has a domain identifier of `domain`.

#### Body

application/json

[​](#body-query)

query

string

required

The search query to execute against your documentation content.

[​](#body-page-size)

pageSize

number

default:10

Number of search results to return. Defaults to 10 if not specified.

[​](#body-filter)

filter

object

Optional filtering parameters to narrow search results.

Show child attributes

#### Response

200 - application/json

Search results

[​](#response-items-content)

content

string

The matching content from your documentation.

[​](#response-items-path)

path

string

The path or URL to the source document.

[​](#response-items-metadata)

metadata

object

Additional metadata about the search result.

Was this page helpful?

YesNo

[Assistant messagePrevious](https://www.mintlify.com/docs/api/assistant/create-assistant-message-v2)[Get user feedbackNext](https://www.mintlify.com/docs/api/analytics/feedback)

⌘I
