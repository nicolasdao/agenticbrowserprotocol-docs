---
url: https://mintlify.com/docs/api/analytics/feedback
canonical: https://www.mintlify.com/docs/api/analytics/feedback
title: "Get user feedback - Mintlify"
description: "Returns paginated user feedback with optional filtering"
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Analytics

Get user feedback

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

Get user feedback

cURL
```
curl --request GET \
  --url 'https://api.mintlify.com/api/external/v1/analytics/{projectId}/feedback?limit=50' \
  --header 'Authorization: Bearer <token>'
```
200

400

500
```
{
  "feedback": [
    {
      "id": "<string>",
      "path": "<string>",
      "comment": "<string>",
      "createdAt": "<string>",
      "source": "code_snippet",
      "status": "pending"
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

feedback

Try it

Get user feedback

cURL
```
curl --request GET \
  --url 'https://api.mintlify.com/api/external/v1/analytics/{projectId}/feedback?limit=50' \
  --header 'Authorization: Bearer <token>'
```
200

400

500
```
{
  "feedback": [
    {
      "id": "<string>",
      "path": "<string>",
      "comment": "<string>",
      "createdAt": "<string>",
      "source": "code_snippet",
      "status": "pending"
    }
  ],
  "nextCursor": "<string>",
  "hasMore": true
}
```

##

[​](#usage)

Usage

Use this endpoint to export user feedback collected from your documentation. Feedback includes contextual feedback from page ratings and code snippet feedback. Paginate through results using the `cursor` parameter returned in the response. Continue fetching while `hasMore` is `true`.

##

[​](#filtering)

Filtering

Filter feedback by:

- **Date range**: Use `dateFrom` and `dateTo` to limit results to a specific time period
- **Source**: Filter by `code_snippet` or `contextual` feedback types
- **Status**: Filter by status values like `pending`, `in_progress`, `resolved`, or `dismissed`

##

[​](#response-types)

Response types

The response contains different feedback types based on the source:

- **Contextual feedback**: Includes `helpful` boolean and optional `contact` email
- **Code snippet feedback**: Includes `code`, `filename`, and `lang` fields

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

[​](#parameter-source)

source

enum<string>

Filter by feedback source

Available options:

`code_snippet`,

`contextual`

[​](#parameter-status)

status

string

Comma-separated list of statuses to filter by

[​](#parameter-limit)

limit

number

default:50

Max results per page

Required range: `1 <= x <= 100`

[​](#parameter-cursor)

cursor

string

Pagination cursor

#### Response

200

application/json

Feedback data with pagination

[​](#response-feedback)

feedback

object\[\]

required

List of feedback entries.

- Option 1

- Option 2

- Option 3


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

[Search documentationPrevious](https://www.mintlify.com/docs/api/assistant/search)[Get assistant conversationsNext](https://www.mintlify.com/docs/api/analytics/assistant-conversations)

⌘I
