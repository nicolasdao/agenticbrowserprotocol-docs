---
url: https://mintlify.com/docs/api/agent/get-all-jobs
canonical: https://www.mintlify.com/docs/api/agent/get-all-jobs
alternate_urls:
  - https://mintlify.com/docs/api/agent/get-all-jobs
  - https://mintlify.com/docs/api-reference/agent/get-all-jobs
title: "Get all agent jobs - Mintlify"
description: "Retrieves all agent jobs for the specified domain, including their status and details."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Agent

Get all agent jobs

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

Get all agent jobs

cURL
```
curl --request GET \
  --url https://api.mintlify.com/v1/agent/{projectId}/jobs \
  --header 'Authorization: Bearer <token>'
```
200
```
{
  "allSessions": [
    {
      "sessionId": "<string>",
      "subdomain": "<string>",
      "branch": "<string>",
      "haulted": true,
      "haultReason": "completed",
      "pullRequestLink": "<string>",
      "messageToUser": "<string>",
      "todos": [
        {
          "content": "<string>",
          "status": "pending",
          "priority": "high",
          "id": "<string>"
        }
      ],
      "createdAt": "2023-11-07T05:31:56Z"
    }
  ]
}
```
GET

/

agent

/

{projectId}

/

jobs

Try it

Get all agent jobs

cURL
```
curl --request GET \
  --url https://api.mintlify.com/v1/agent/{projectId}/jobs \
  --header 'Authorization: Bearer <token>'
```
200
```
{
  "allSessions": [
    {
      "sessionId": "<string>",
      "subdomain": "<string>",
      "branch": "<string>",
      "haulted": true,
      "haultReason": "completed",
      "pullRequestLink": "<string>",
      "messageToUser": "<string>",
      "todos": [
        {
          "content": "<string>",
          "status": "pending",
          "priority": "high",
          "id": "<string>"
        }
      ],
      "createdAt": "2023-11-07T05:31:56Z"
    }
  ]
}
```

##

[​](#usage)

Usage

This endpoint retrieves all agent jobs for the specified domain, providing an overview of all agent activities and their current status. This is useful for monitoring and managing multiple concurrent or historical agent jobs.

##

[​](#response)

Response

Use this endpoint to get a comprehensive view of all previous agent sessions.

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

#### Response

200 - application/json

All agent jobs retrieved successfully

[​](#response-all-sessions)

allSessions

object\[\]

Array of all agent sessions for the domain.

Show child attributes

Was this page helpful?

YesNo

[Get agent job by IDPrevious](https://www.mintlify.com/docs/api/agent/get-agent-job)[Assistant messageNext](https://www.mintlify.com/docs/api/assistant/create-assistant-message-v2)

⌘I
