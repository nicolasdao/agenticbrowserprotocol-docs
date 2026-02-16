---
url: https://mintlify.com/docs/guides/assistant-embed
canonical: https://www.mintlify.com/docs/guides/assistant-embed
title: "Tutorial: Build an in-app documentation assistant - Mintlify"
description: "Embed the assistant in your application to answer questions with information from your documentation."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

AI

Tutorial: Build an in-app documentation assistant

Search...

⌘K

##### Overview

- [Guides](https://www.mintlify.com/docs/guides)

##### AI

- [Automate documentation updates](https://www.mintlify.com/docs/guides/automate-agent)
- [Build an in-app assistant](https://www.mintlify.com/docs/guides/assistant-embed)
- [Claude Code](https://www.mintlify.com/docs/guides/claude-code)
- [Cursor](https://www.mintlify.com/docs/guides/cursor)
- [GEO](https://www.mintlify.com/docs/guides/geo)
- [Windsurf](https://www.mintlify.com/docs/guides/windsurf)

##### API docs

- [Migrate from MDX to OAS](https://www.mintlify.com/docs/guides/migrating-from-mdx)

##### Best practices

- [Accessibility](https://www.mintlify.com/docs/guides/accessibility)
- [Content types](https://www.mintlify.com/docs/guides/content-types)
- [Content templates](https://www.mintlify.com/docs/guides/content-templates)
- [Improve your docs](https://www.mintlify.com/docs/guides/improving-docs)
- [Internationalization](https://www.mintlify.com/docs/guides/internationalization)
- [Linking](https://www.mintlify.com/docs/guides/linking)
- [Maintenance](https://www.mintlify.com/docs/guides/maintenance)
- [Media](https://www.mintlify.com/docs/guides/media)
- [Organize navigation](https://www.mintlify.com/docs/guides/navigation)
- [SEO](https://www.mintlify.com/docs/guides/seo)
- [Style and tone](https://www.mintlify.com/docs/guides/style-and-tone)
- [Understand your audience](https://www.mintlify.com/docs/guides/understand-your-audience)

##### Git

- [Git concepts for documentation](https://www.mintlify.com/docs/guides/git-concepts)
- [Work with branches](https://www.mintlify.com/docs/guides/branches)

##### Use cases

- [Developer documentation](https://www.mintlify.com/docs/guides/developer-documentation)
- [Knowledge base](https://www.mintlify.com/docs/guides/knowledge-base)
- [Support center](https://www.mintlify.com/docs/guides/support-center)

![US](https://d3gk2c5xim1je2.cloudfront.net/flags/US.svg)

English

##

[​](#what-you-will-build)

What you will build

A reusable widget that embeds the [assistant](https://www.mintlify.com/docs/ai/assistant) directly in your application. The widget provides:

- A floating button that opens a chat panel when clicked
- Real-time streaming responses based on information from your documentation
- Message rendering with Markdown support

Users can use the widget to get help with your product without leaving your application.

![Demo of the assistant widget being opened and the user typing in How do I get started? Then the assistant responds.](https://mintcdn.com/mintlify/14gofcrk-ET1sjS3/images/assistant/assistant-embed-demo.gif?s=140b5b5da46b72b54045372b8a2759fc)

##

[​](#prerequisites)

Prerequisites

- [Mintlify Pro or Enterprise plan](https://mintlify.com/pricing)
- Your domain name, which appears at the end of your dashboard URL. For example, if your dashboard URL is `https://dashboard.mintlify.com/org-name/domain-name`, your domain name is `domain-name`
- An [assistant API key](https://dashboard.mintlify.com/settings/organization/api-keys)
- Node.js v18 or higher and npm installed
- Basic React knowledge

###

[​](#get-your-assistant-api-key)

Get your assistant API key

1.  Navigate to the [API keys](https://dashboard.mintlify.com/settings/organization/api-keys) page in your dashboard.
2.  Click **Create Assistant API Key**.
3.  Copy the assistant API key (starts with `mint_dsc_`) and save it securely.

The assistant API key is a public token that you can use in frontend code. Calls using this token count toward your plan’s message allowance and can incur overages.

##

[​](#set-up-the-example)

Set up the example

Clone the [example repository](https://github.com/mintlify/assistant-embed-example) and customize it for your needs.

1

[](#)

Clone the repository
```
git clone https://github.com/mintlify/assistant-embed-example.git
cd assistant-embed-example
```
2

[](#)

Choose your development tool

The repository includes Next.js and Vite examples. Choose the tool you prefer to use.

Next.js

Vite
```
cd nextjs
npm install
```
3

[](#)

Configure your project

Open `src/config.js` and update with your Mintlify project details.

src/config.js
```
export const ASSISTANT_CONFIG = {
  domain: 'your-domain',
  docsURL: 'https://yourdocs.mintlify.app',
};
```
Replace:

- `your-domain` with your Mintlify project domain found at the end of your dashboard URL.
- `https://yourdocs.mintlify.app` with your actual documentation URL.

4

[](#)

Add your API token

Create a `.env` file in the project root.

.env
```
VITE_MINTLIFY_TOKEN=mint_dsc_your_token_here
```
Replace `mint_dsc_your_token_here` with your assistant API key.

5

[](#)

Start the development server
```
npm run dev
```
Open your application in a browser and click the **Ask** button to open the assistant widget.

##

[​](#customization-ideas)

Customization ideas

###

[​](#source-citations)

Source citations

Extract and display sources from assistant responses:
```
const extractSources = (parts) => {
  return parts
    ?.filter(p => p.type === 'tool-invocation' && p.toolInvocation?.toolName === 'search')
    .flatMap(p => p.toolInvocation?.result || [])
    .map(source => ({
      url: source.url || source.path,
      title: source.metadata?.title || source.path,
    })) || [];
};

// In your message rendering:
{messages.map((message) => {
  const sources = message.role === 'assistant' ? extractSources(message.parts) : [];
  return (
    <div key={message.id}>
      {/* message content */}
      {sources.length > 0 && (
        <div className="mt-2 text-xs">
          <p className="font-semibold">Sources:</p>
          {sources.map((s, i) => (
            <a key={i} href={s.url} target="_blank" rel="noopener noreferrer" className="text-blue-600">
              {s.title}
            </a>
          ))}
        </div>
      )}
    </div>
  );
})}
```

###

[​](#track-conversation-thread-ids)

Track conversation thread IDs

Store thread IDs to maintain conversation history across sessions:
```
import { useState, useEffect } from 'react';

export function AssistantWidget({ domain, docsURL }) {
  const [threadId, setThreadId] = useState(null);

  useEffect(() => {
    // Retrieve saved thread ID from localStorage
    const saved = localStorage.getItem('assistant-thread-id');
    if (saved) {
      setThreadId(saved);
    }
  }, []);

  const { messages, input, handleInputChange, handleSubmit, isLoading } = useChat({
    api: `https://api.mintlify.com/discovery/v1/assistant/${domain}/message`,
    headers: {
      'Authorization': `Bearer ${import.meta.env.VITE_MINTLIFY_TOKEN}`,
    },
    body: {
      fp: 'anonymous',
      retrievalPageSize: 5,
      ...(threadId && { threadId }), // Include thread ID if available
    },
    streamProtocol: 'data',
    sendExtraMessageFields: true,
    fetch: async (url, options) => {
      const response = await fetch(url, options);
      const newThreadId = response.headers.get('x-thread-id');
      if (newThreadId) {
        setThreadId(newThreadId);
        localStorage.setItem('assistant-thread-id', newThreadId);
      }
      return response;
    },
  });

  // ... rest of component
}
```

###

[​](#add-keyboard-shortcuts)

Add keyboard shortcuts

Allow users to open the widget and submit messages with keyboard shortcuts:
```
useEffect(() => {
  const handleKeyDown = (e) => {
    // Cmd/Ctrl + Shift + I to toggle widget
    if ((e.metaKey || e.ctrlKey) && e.shiftKey && e.key === 'I') {
      e.preventDefault();
      setIsOpen((prev) => !prev);
    }

    // Enter (when widget is focused) to submit
    if (e.key === 'Enter' && !e.shiftKey && document.activeElement.id === 'assistant-input') {
      e.preventDefault();
      handleSubmit();
    }
  };

  window.addEventListener('keydown', handleKeyDown);
  return () => window.removeEventListener('keydown', handleKeyDown);
}, [handleSubmit]);
```
Was this page helpful?

YesNo

[Tutorial: Auto-update documentation when code is changedPrevious](https://www.mintlify.com/docs/guides/automate-agent)[Claude CodeNext](https://www.mintlify.com/docs/guides/claude-code)

⌘I

![Demo of the assistant widget being opened and the user typing in How do I get started? Then the assistant responds.](https://mintcdn.com/mintlify/14gofcrk-ET1sjS3/images/assistant/assistant-embed-demo.gif?s=140b5b5da46b72b54045372b8a2759fc)
