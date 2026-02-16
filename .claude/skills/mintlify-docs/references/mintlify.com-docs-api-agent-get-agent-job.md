---
url: https://mintlify.com/docs/api/agent/get-agent-job
canonical: https://www.mintlify.com/docs/api/agent/get-agent-job
alternate_urls:
  - https://mintlify.com/docs/api/agent/get-agent-job
  - https://mintlify.com/docs/api-reference/agent/get-agent-job
title: "Get agent job by ID - Mintlify"
description: "Retrieves the details and status of a specific agent job by its ID."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Agent

Get agent job by ID

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

Get agent job by ID

cURL
```
curl --request GET \
  --url https://api.mintlify.com/v1/agent/{projectId}/job/{id} \
  --header 'Authorization: Bearer <token>'
```
200
```
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
```
GET

/

agent

/

{projectId}

/

job

/

{id}

Try it

Get agent job by ID

cURL
```
curl --request GET \
  --url https://api.mintlify.com/v1/agent/{projectId}/job/{id} \
  --header 'Authorization: Bearer <token>'
```
200
```
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
```

##

[​](#usage)

Usage

This endpoint retrieves the details and status of a specific agent job by its unique identifier. Use this to check the progress, status, and results of a previously created agent job.

##

[​](#job-details)

Job details

The response includes information such as:

- Job execution status and completion state
- Branch information and pull request details
- Session metadata and timestamps

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

[​](#parameter-id)

id

string

required

The unique identifier of the agent job to retrieve.

#### Response

200 - application/json

Agent job details retrieved successfully

[​](#response-session-id)

sessionId

string

The subdomain this session belongs to.

[​](#response-subdomain)

subdomain

string

The subdomain this session belongs to.

[​](#response-branch-one-of-0)

branch

string | null

Git branch name where changes were made.

[​](#response-haulted)

haulted

boolean

Whether the session execution was halted.

[​](#response-hault-reason)

haultReason

enum<string>

Reason for session halt.

Available options:

`completed`,

`github_missconfigured`,

`error`

[​](#response-pull-request-link)

pullRequestLink

string

Link to the created pull request.

[​](#response-message-to-user)

messageToUser

string

Message for the user about the session outcome.

[​](#response-todos)

todos

object\[\]

List of todo items from the session.

Show child attributes

[​](#response-created-at)

createdAt

string<date-time>

Timestamp when the session was created.

Was this page helpful?

YesNo

[Create agent jobPrevious](https://www.mintlify.com/docs/api/agent/create-agent-job)[Get all agent jobsNext](https://www.mintlify.com/docs/api/agent/get-all-jobs)

⌘I
