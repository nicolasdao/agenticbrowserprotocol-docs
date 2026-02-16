---
url: https://mintlify.com/docs/api/analytics/assistant-conversations
canonical: https://www.mintlify.com/docs/api/analytics/assistant-conversations
title: "Get assistant conversations - Mintlify"
description: "Returns paginated AI assistant conversation history"
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Analytics

Get assistant conversations

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

Get assistant conversations

cURL
```
curl --request GET \
  --url 'https://api.mintlify.com/api/external/v1/analytics/{projectId}/assistant?limit=100' \
  --header 'Authorization: Bearer <token>'
```
200

400

500
```
{
  "conversations": [
    {
      "id": "<string>",
      "timestamp": "<string>",
      "query": "<string>",
      "response": "<string>",
      "sources": [
        {
          "title": "<string>",
          "url": "<string>"
        }
      ],
      "queryCategory": "<string>"
    }
  ],
  "nextCursor": "<string>",
  "hasMore": true
}
```
GET

/

api

/

external

/

v1

/

analytics

/

{projectId}

/

assistant

Try it

Get assistant conversations

cURL
```
curl --request GET \
  --url 'https://api.mintlify.com/api/external/v1/analytics/{projectId}/assistant?limit=100' \
  --header 'Authorization: Bearer <token>'
```
200

400

500
```
{
  "conversations": [
    {
      "id": "<string>",
      "timestamp": "<string>",
      "query": "<string>",
      "response": "<string>",
      "sources": [
        {
          "title": "<string>",
          "url": "<string>"
        }
      ],
      "queryCategory": "<string>"
    }
  ],
  "nextCursor": "<string>",
  "hasMore": true
}
```

##

[​](#usage)

Usage

Use this endpoint to export AI assistant conversation history from your documentation. Each conversation includes the user query, assistant response, sources cited, and query category. Paginate through results using the `cursor` parameter returned in the response. Continue fetching while `hasMore` is `true`.

##

[​](#filtering)

Filtering

Filter conversations by date range using `dateFrom` and `dateTo` parameters.

##

[​](#conversation-data)

Conversation data

Each conversation includes:

- **query**: The user’s question
- **response**: The assistant’s answer
- **sources**: Pages referenced in the response, with title and URL
- **queryCategory**: Classification of the query type (if available)

#### Authorizations

[​](#authorization-authorization)

Authorization

string

header

required

The Authorization header expects a Bearer token. Use an admin API key (prefixed with `mint_`). This is a server-side secret key. Generate one on the [API keys page](https://dashboard.mintlify.com/settings/organization/api-keys) in your dashboard.

#### Path Parameters

[​](#parameter-project-id)

projectId

string

required

Your project ID. Can be copied from the [API keys](https://dashboard.mintlify.com/settings/organization/api-keys) page in your dashboard.

#### Query Parameters

[​](#parameter-date-from)

dateFrom

string

Date in ISO 8601 or YYYY-MM-DD format

Example:

`"2024-01-01"`

[​](#parameter-date-to)

dateTo

string

Date in ISO 8601 or YYYY-MM-DD format. `dateTo` is an exclusive upper limit. Results include dates before, but not on, the specified date.

Example:

`"2024-01-01"`

[​](#parameter-limit)

limit

number

default:100

Max results per page

Required range: `1 <= x <= 1000`

[​](#parameter-cursor)

cursor

string<ulid>

Pagination cursor (ULID format)

#### Response

200

application/json

Conversation data with pagination

[​](#response-conversations)

conversations

object\[\]

required

List of assistant conversations.

Show child attributes

[​](#response-next-cursor-one-of-0)

nextCursor

string | null

required

Cursor to retrieve the next page of results. Null if no more results.

[​](#response-has-more)

hasMore

boolean

required

Whether additional results are available beyond this page.

Was this page helpful?

YesNo

[Get user feedbackPrevious](https://www.mintlify.com/docs/api/analytics/feedback)

⌘I
