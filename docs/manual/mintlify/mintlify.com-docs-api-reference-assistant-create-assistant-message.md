---
url: https://mintlify.com/docs/api-reference/assistant/create-assistant-message
canonical: https://www.mintlify.com/docs/api/assistant/create-assistant-message
title: "Assistant message v1 - Mintlify"
description: "Generates a response message from the assistant for the specified domain. Compatible with AI SDK v4."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Assistant message v1

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

Assistant message v1

cURL
```
curl --request POST \
  --url https://api.mintlify.com/discovery/v1/assistant/{domain}/message \
  --header 'Authorization: Bearer <token>' \
  --header 'Content-Type: application/json' \
  --data '
{
  "fp": "<string>",
  "messages": [
    {
      "id": "foobar",
      "role": "user",
      "content": "how do i get started",
      "parts": [
        {
          "type": "text",
          "text": "How do I get started"
        }
      ]
    }
  ],
  "threadId": null,
  "retrievalPageSize": 5,
  "filter": null
}
'
```
200
```
{}
```
POST

/

v1

/

assistant

/

{domain}

/

message

Try it

Assistant message v1

cURL
```
curl --request POST \
  --url https://api.mintlify.com/discovery/v1/assistant/{domain}/message \
  --header 'Authorization: Bearer <token>' \
  --header 'Content-Type: application/json' \
  --data '
{
  "fp": "<string>",
  "messages": [
    {
      "id": "foobar",
      "role": "user",
      "content": "how do i get started",
      "parts": [
        {
          "type": "text",
          "text": "How do I get started"
        }
      ]
    }
  ],
  "threadId": null,
  "retrievalPageSize": 5,
  "filter": null
}
'
```
200
```
{}
```
Deprecated

The assistant message v1 endpoint is compatible with **AI SDK v4**. If you use AI SDK v5 or later, use the [assistant message v2 endpoint](https://www.mintlify.com/docs/api-reference/assistant/create-assistant-message-v2) instead.

##

[​](#integration-with-usechat)

Integration with `useChat`

The `useChat` hook from Vercel’s AI SDK is the recommended way to integrate the assistant API into your application.

1

[](#)

Install AI SDK v4
```
npm i ai@^4.1.15
```
2

[](#)

Use the hook
```
import { useChat } from 'ai/react';

function MyComponent({ domain }) {
  const { messages, input, handleInputChange, handleSubmit, isLoading } = useChat({
    api: `https://api.mintlify.com/discovery/v1/assistant/${domain}/message`,
    headers: {
      'Authorization': `Bearer ${process.env.PUBLIC_MINTLIFY_ASSISTANT_KEY}`,
    },
    body: {
      fp: 'anonymous',
      retrievalPageSize: 5,
      context: [
        {
          type: 'code',
          value: 'const example = "code snippet";',
          elementId: 'code-block-1',
        },
      ],
    },
    streamProtocol: 'data',
    sendExtraMessageFields: true,
  });

  return (
    <div>
      {messages.map((message) => (
        <div key={message.id}>
          {message.role === 'user' ? 'User: ' : 'Assistant: '}
          {message.content}
        </div>
      ))}
      <form onSubmit={handleSubmit}>
        <input value={input} onChange={handleInputChange} />
        <button type="submit">Send</button>
      </form>
    </div>
  );
}
```
**Required configuration for Mintlify:**

- `streamProtocol: 'data'` - Required for streaming responses.
- `sendExtraMessageFields: true` - Required to send message metadata.
- `body.fp` - Fingerprint identifier (use ‘anonymous’ or a user identifier).
- `body.retrievalPageSize` - Number of search results to use (recommended: 5).

**Optional configuration:**

- `body.context` - Array of contextual information to provide to the assistant. Each context object contains:
    -   `type` - Either `'code'` or `'textSelection'`.
    -   `value` - The code snippet or selected text content.
    -   `elementId` (optional) - Identifier for the UI element containing the context.

See [useChat](https://ai-sdk.dev/docs/reference/ai-sdk-ui/use-chat) in the AI SDK documentation for more details.

##

[​](#rate-limits)

Rate limits

The assistant API has the following limits:

- 10,000 uses per key per month
- 10,000 requests per Mintlify organization per hour
- 10,000 requests per IP per day

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

[​](#body-fp)

fp

string

required

Fingerprint identifier for tracking conversation sessions. Use 'anonymous' for anonymous users or provide a unique user identifier.

[​](#body-messages)

messages

object\[\]

required

Array of messages in the conversation. On the frontend, you will likely want to use the handleSubmit function from the @ai-sdk package's useChat hook to append user messages and handle streaming responses, rather than manually defining the objects in this array as they have so many parameters.

Show child attributes

[​](#body-thread-id)

threadId

string

An optional identifier used to maintain conversation continuity across multiple messages. When provided, it allows the system to associate follow-up messages with the same conversation thread. The threadId is returned in the response as event.threadId when event.type === 'finish'.

[​](#body-retrieval-page-size)

retrievalPageSize

number

default:5

Number of documentation search results to use for generating the response. Higher values provide more context but may increase response time. Recommended: 5.

[​](#body-filter)

filter

object

Optional filter criteria for the search.

Show child attributes

#### Response

200 - application/json

Message generated successfully

Response object with data stream parts formatted with the specified status, headers, and content. For more information, see the AI SDK documentation at [ai-sdk.dev/docs/ai-sdk-ui/streaming-data](https://ai-sdk.dev/docs/ai-sdk-ui/streaming-data). Use the [useChat hook from ai-sdk](https://ai-sdk.dev/docs/reference/ai-sdk-ui/use-chat#usechat) to handle the response stream.

Was this page helpful?

YesNo

⌘I
