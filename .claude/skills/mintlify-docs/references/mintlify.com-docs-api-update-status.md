---
url: https://mintlify.com/docs/api/update/status
canonical: https://www.mintlify.com/docs/api/update/status
title: "Get update status - Mintlify"
description: "Get the status of an update from the status ID"
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Admin

Get update status

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

Get update status

cURL
```
curl --request GET \
  --url https://api.mintlify.com/v1/project/update-status/{statusId} \
  --header 'Authorization: Bearer <token>'
```
200
```
{
  "_id": "<string>",
  "projectId": "<string>",
  "createdAt": "<string>",
  "endedAt": "<string>",
  "status": "queued",
  "summary": "<string>",
  "logs": [
    "<string>"
  ],
  "subdomain": "<string>",
  "screenshot": "<string>",
  "screenshotLight": "<string>",
  "screenshotDark": "<string>",
  "author": "<string>",
  "commit": {
    "sha": "<string>",
    "ref": "<string>",
    "message": "<string>",
    "filesChanged": {
      "added": [
        "<string>"
      ],
      "modified": [
        "<string>"
      ],
      "removed": [
        "<string>"
      ]
    }
  },
  "source": "internal"
}
```
GET

/

project

/

update-status

/

{statusId}

Try it

Get update status

cURL
```
curl --request GET \
  --url https://api.mintlify.com/v1/project/update-status/{statusId} \
  --header 'Authorization: Bearer <token>'
```
200
```
{
  "_id": "<string>",
  "projectId": "<string>",
  "createdAt": "<string>",
  "endedAt": "<string>",
  "status": "queued",
  "summary": "<string>",
  "logs": [
    "<string>"
  ],
  "subdomain": "<string>",
  "screenshot": "<string>",
  "screenshotLight": "<string>",
  "screenshotDark": "<string>",
  "author": "<string>",
  "commit": {
    "sha": "<string>",
    "ref": "<string>",
    "message": "<string>",
    "filesChanged": {
      "added": [
        "<string>"
      ],
      "modified": [
        "<string>"
      ],
      "removed": [
        "<string>"
      ]
    }
  },
  "source": "internal"
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

[​](#parameter-status-id)

statusId

string

required

The status ID of a triggered update.

#### Response

200 - application/json

A successful response

[​](#response-id)

\_id

string

The status ID of the triggered updated.

[​](#response-project-id)

projectId

string

The documentation project ID.

[​](#response-created-at)

createdAt

string

An ISODate with the specified datetime in UTC

[​](#response-ended-at)

endedAt

string

An ISODate with the specified datetime in UTC

[​](#response-status)

status

enum<string>

The status of the update.

Available options:

`queued`,

`in_progress`,

`success`,

`failure`

[​](#response-summary)

summary

string

Summary of the status of the update

[​](#response-logs)

logs

string\[\]

An array of logs.

[​](#response-subdomain)

subdomain

string

The subdomain of the docs being updated.

[​](#response-screenshot)

screenshot

string

A screenshot of the docs.

[​](#response-screenshot-light)

screenshotLight

string

A screenshot of the docs.

[​](#response-screenshot-dark)

screenshotDark

string

A screenshot of the docs in dark mode.

[​](#response-author)

author

string

The author of the update.

[​](#response-commit)

commit

object

The commit details

Show child attributes

[​](#response-source)

source

enum<string>

The source of the update trigger.

Available options:

`internal`,

`github-app-installation`,

`api`,

`github`,

`dashboard`

Was this page helpful?

YesNo

[Trigger updatePrevious](https://www.mintlify.com/docs/api/update/trigger)[Create agent jobNext](https://www.mintlify.com/docs/api/agent/create-agent-job)

⌘I
