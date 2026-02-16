---
url: https://mintlify.com/docs/api-playground/managing-page-visibility
canonical: https://www.mintlify.com/docs/api-playground/managing-page-visibility
title: "Manage page visibility - Mintlify"
description: "Control which API endpoints appear in your documentation navigation."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Document APIs

Manage page visibility

Search...

⌘K

##### Get started

- [Introduction](https://www.mintlify.com/docs)
- [Quickstart](https://www.mintlify.com/docs/quickstart)
- [AI-native](https://www.mintlify.com/docs/ai-native)
- [Migration guide](https://www.mintlify.com/docs/migration)

##### Organize

- [Global settings](https://www.mintlify.com/docs/organize/settings)
- [Navigation](https://www.mintlify.com/docs/organize/navigation)
- [Pages](https://www.mintlify.com/docs/organize/pages)
- [Hidden pages](https://www.mintlify.com/docs/organize/hidden-pages)
- [Exclude files](https://www.mintlify.com/docs/organize/mintignore)

##### Customize

- [Custom domain](https://www.mintlify.com/docs/customize/custom-domain)
- [Themes](https://www.mintlify.com/docs/customize/themes)
- [Fonts](https://www.mintlify.com/docs/customize/fonts)
- [Custom scripts](https://www.mintlify.com/docs/customize/custom-scripts)
- [React](https://www.mintlify.com/docs/customize/react-components)
- [Custom 404 page](https://www.mintlify.com/docs/customize/custom-404-page)

##### Create content

- Web editor

- [Install the CLI](https://www.mintlify.com/docs/installation)
- [Format text](https://www.mintlify.com/docs/create/text)
- [Format code](https://www.mintlify.com/docs/create/code)
- Agent

- Components

- [Images and embeds](https://www.mintlify.com/docs/create/image-embeds)
- [Files](https://www.mintlify.com/docs/create/files)
- [Lists and tables](https://www.mintlify.com/docs/create/list-table)
- [Reusable snippets](https://www.mintlify.com/docs/create/reusable-snippets)
- [Personalized content](https://www.mintlify.com/docs/create/personalization)
- [Redirects](https://www.mintlify.com/docs/create/redirects)
- [Changelogs](https://www.mintlify.com/docs/create/changelogs)

##### Document APIs

- [Playground](https://www.mintlify.com/docs/api-playground/overview)
- [OpenAPI setup](https://www.mintlify.com/docs/api-playground/openapi-setup)
- [Complex data types](https://www.mintlify.com/docs/api-playground/complex-data-types)
- [Add SDK examples](https://www.mintlify.com/docs/api-playground/adding-sdk-examples)
- [Manage page visibility](https://www.mintlify.com/docs/api-playground/managing-page-visibility)
- [Multiple responses](https://www.mintlify.com/docs/api-playground/multiple-responses)
- [Create manual API pages](https://www.mintlify.com/docs/api-playground/mdx-setup)
- [AsyncAPI setup](https://www.mintlify.com/docs/api-playground/asyncapi-setup)
- [Troubleshooting](https://www.mintlify.com/docs/api-playground/troubleshooting)

##### Deploy

- [Deployments](https://www.mintlify.com/docs/deploy/deployments)
- [Preview deployments](https://www.mintlify.com/docs/deploy/preview-deployments)
- /docs subpath

- [Authentication setup](https://www.mintlify.com/docs/deploy/authentication-setup)
- Dashboard access

- [Monorepo setup](https://www.mintlify.com/docs/deploy/monorepo)
- [External proxies with Vercel](https://www.mintlify.com/docs/deploy/vercel-external-proxies)
- [CI checks](https://www.mintlify.com/docs/deploy/ci)
- [GitHub](https://www.mintlify.com/docs/deploy/github)
- [GitHub Enterprise Server](https://www.mintlify.com/docs/deploy/ghes)
- [GitLab](https://www.mintlify.com/docs/deploy/gitlab)

##### Optimize

- [Assistant](https://www.mintlify.com/docs/ai/assistant)
- [Discord bot](https://www.mintlify.com/docs/ai/discord)
- [Slack bot](https://www.mintlify.com/docs/ai/slack-bot)
- [Contextual menu](https://www.mintlify.com/docs/ai/contextual-menu)
- [Analytics](https://www.mintlify.com/docs/optimize/analytics)
- [Feedback](https://www.mintlify.com/docs/optimize/feedback)
- [llms.txt](https://www.mintlify.com/docs/ai/llmstxt)
- [skill.md](https://www.mintlify.com/docs/ai/skillmd)
- [Model Context Protocol](https://www.mintlify.com/docs/ai/model-context-protocol)
- [SEO](https://www.mintlify.com/docs/optimize/seo)
- [Markdown export](https://www.mintlify.com/docs/ai/markdown-export)
- [PDF exports](https://www.mintlify.com/docs/optimize/pdf-exports)
- Integrations


![US](https://d3gk2c5xim1je2.cloudfront.net/flags/US.svg)

English

For internal-only endpoints, deprecated operations, beta features, or endpoints that should be accessible via direct URL but not discoverable through site navigation, you can control which OpenAPI operations get published as documentation pages and their visibility in navigation. If your pages are autogenerated from an OpenAPI document, manage page visibility with the `x-hidden` and `x-excluded` extensions.

##

[​](#x-hidden)

`x-hidden`

The `x-hidden` extension creates a page for an endpoint, but hides it from navigation. The page is only accessible by navigating directly to its URL. Common use cases for `x-hidden` are:

- Endpoints you want to document, but not promote.
- Pages that you will link to from other content.
- Endpoints for specific users.

##

[​](#x-excluded)

`x-excluded`

The `x-excluded` extension completely excludes an endpoint from your documentation. Common use cases for `x-excluded` are:

- Internal-only endpoints.
- Deprecated endpoints that you don’t want to document.
- Beta features that are not ready for public documentation.

##

[​](#implementation)

Implementation

Add the `x-hidden` or `x-excluded` extension under the HTTP method in your OpenAPI specification. Here are examples of how to use each property in an OpenAPI schema document for an endpoint and a webhook path.

Endpoint example
```
"paths": {
  "/plants": {
    "get": {
      "description": "Returns all plants from the store",
      "parameters": { /*...*/ },
      "responses": { /*...*/ }
    }
  },
  "/hidden_plants": {
    "get": {
      "x-hidden": true,
      "description": "Returns all somewhat secret plants from the store",
      "parameters": { /*...*/ },
      "responses": { /*...*/ }
    }
  },
  "/secret_plants": {
    "get": {
      "x-excluded": true,
      "description": "Returns all top secret plants from the store (do not publish this endpoint!)",
      "parameters": { /*...*/ },
      "responses": { /*...*/ }
    }
  }
},
```
Webhook example
```
"webhooks": {
  "/plants_hook": {
    "post": {
      "description": "Webhook for information about a new plant added to the store",
    }
  },
  "/hidden_plants_hook": {
    "post": {
      "x-hidden": true,
      "description": "Webhook for somewhat secret information about a new plant added to the store"
    }
  },
  "/secret_plants_hook": {
    "post": {
      "x-excluded": true,
      "description": "Webhook for top secret information about a new plant added to the store (do not publish this endpoint!)"
    }
  }
}
```
Was this page helpful?

YesNo

[Add SDK examplesPrevious](https://www.mintlify.com/docs/api-playground/adding-sdk-examples)[Multiple responsesNext](https://www.mintlify.com/docs/api-playground/multiple-responses)

⌘I
