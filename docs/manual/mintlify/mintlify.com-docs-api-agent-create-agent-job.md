---
url: https://mintlify.com/docs/api/agent/create-agent-job
canonical: https://www.mintlify.com/docs/api/agent/create-agent-job
alternate_urls:
  - https://mintlify.com/docs/api/agent/create-agent-job
  - https://mintlify.com/docs/api-reference/agent/create-agent-job
title: "Create agent job - Mintlify"
description: "Creates a new agent job that can generate and edit documentation based on provided messages and branch information."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Agent

Create agent job

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

Create agent job

cURL
```
curl --request POST \
  --url https://api.mintlify.com/v1/agent/{projectId}/job \
  --header 'Authorization: Bearer <token>' \
  --header 'Content-Type: application/json' \
  --data '
{
  "branch": "<string>",
  "messages": [
    {
      "role": "system",
      "content": "<string>"
    }
  ],
  "asDraft": true,
  "model": "sonnet"
}
'
```
200
```
"<string>"
```
POST

/

agent

/

{projectId}

/

job

Try it

Create agent job

cURL
```
curl --request POST \
  --url https://api.mintlify.com/v1/agent/{projectId}/job \
  --header 'Authorization: Bearer <token>' \
  --header 'Content-Type: application/json' \
  --data '
{
  "branch": "<string>",
  "messages": [
    {
      "role": "system",
      "content": "<string>"
    }
  ],
  "asDraft": true,
  "model": "sonnet"
}
'
```
200
```
"<string>"
```
This endpoint creates an agent job based on provided messages and branch information. The job executes asynchronously and returns a streaming response with the execution details and results. If a branch doesn’t exist, the agent creates one. If files are edited successfully, a pull request is automatically created at the end of the job.

##

[​](#rate-limits)

Rate limits

The agent API has the following limits:

- 100 uses per Mintlify project per hour

##

[​](#suggested-usage)

Suggested usage

For best results, use the [useChat hook from ai-sdk](https://ai-sdk.dev/docs/reference/ai-sdk-ui/use-chat#usechat) to send requests and handle responses.

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

#### Body

application/json

[​](#body-branch)

branch

string

required

The name of the Git branch that the agent should work on, will be automatically created if it doesn't exist

[​](#body-messages)

messages

object\[\]

required

A list of messages to provide to the agent. A default system prompt is always prepended automatically, so you typically only need to include user messages.

Show child attributes

[​](#body-as-draft)

asDraft

boolean

default:true

Control whether the pull request is created in draft or non-draft mode. When true, creates a draft pull request. When false, creates a regular (non-draft) pull request ready for review.

[​](#body-model)

model

enum<string>

default:sonnet

The AI model to use for the agent job. Use `sonnet` for faster, cost-effective processing. Use `opus` for more capable, but slower processing.

Available options:

`sonnet`,

`opus`

#### Response

200 - text/plain

Agent job created successfully (streaming response). X-Session-Id Header is sent back in the response

Streaming response containing the agent job execution details and results.

Was this page helpful?

YesNo

[Get update statusPrevious](https://www.mintlify.com/docs/api/update/status)[Get agent job by IDNext](https://www.mintlify.com/docs/api/agent/get-agent-job)

⌘I
