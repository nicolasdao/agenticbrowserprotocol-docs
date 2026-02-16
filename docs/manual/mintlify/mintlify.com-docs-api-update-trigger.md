---
url: https://mintlify.com/docs/api/update/trigger
canonical: https://www.mintlify.com/docs/api/update/trigger
title: "Trigger update - Mintlify"
description: "Queue a deployment update for your documentation project. Returns a status ID that can be used to track the update progress. The update is triggered from your configured deployment branch."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Admin

Trigger update

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

Trigger update

cURL
```
curl --request POST \
  --url https://api.mintlify.com/v1/project/update/{projectId} \
  --header 'Authorization: Bearer <token>'
```
202
```
{
  "statusId": "<string>"
}
```
POST

/

project

/

update

/

{projectId}

Try it

Trigger update

cURL
```
curl --request POST \
  --url https://api.mintlify.com/v1/project/update/{projectId} \
  --header 'Authorization: Bearer <token>'
```
202
```
{
  "statusId": "<string>"
}
```

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

202 - application/json

A successful response

[​](#response-status-id)

statusId

string

The status ID of the triggered updated.

Was this page helpful?

YesNo

[IntroductionPrevious](https://www.mintlify.com/docs/api/introduction)[Get update statusNext](https://www.mintlify.com/docs/api/update/status)

⌘I
