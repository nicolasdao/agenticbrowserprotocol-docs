---
url: https://mintlify.com/docs/api-playground/mdx-setup
canonical: https://www.mintlify.com/docs/api-playground/mdx-setup
title: "Create manual API pages - Mintlify"
description: "Document API endpoints manually with MDX files."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Document APIs

Create manual API pages

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

You can manually define API endpoints in individual MDX pages. This approach is useful for small APIs or prototyping.

##

[​](#setup)

Setup

1

[](#)

Configure your API settings

In your `docs.json` file, define your base URL and authentication method.

Example docs.json
```
"api": {
  "mdx": {
    "server": "https://api.acme.com/",
    "auth": {
      "method": "key",
      "name": "x-api-key"
    }
  }
}
```
If you want to hide the API playground, set the `display` field to `none`. You don’t need to include an authentication method if you hide the playground.
```
"api": {
  "playground": {
    "display": "none"
  }
}
```
Find a full list of API configurations in [Settings](https://www.mintlify.com/docs/organize/settings#api-configurations).

2

[](#)

Create your endpoint pages

Create an MDX file for each endpoint. Define the `title` and `api` in the frontmatter:
```
---
title: 'Create new user'
api: 'POST /v1/users'
---
```
The `api` frontmatter field accepts either a full URL or a relative path:

- **Full URL** like `POST https://api.acme.com/v1/users`. The `server` field in `docs.json` is ignored for that endpoint.
- **Relative path** like `POST /v1/users`. Requires a `server` field in `docs.json`. The server URL is prepended to the path.

Specify path parameters by wrapping them in `{}`:
```
https://api.example.com/v1/endpoint/{userId}
```
To override the global playground display mode for a specific page, add `playground` to the frontmatter:
```
---
title: 'Create new user'
api: 'POST https://api.mintlify.com/user'
playground: 'none'
---
```
Options:

- `playground: 'interactive'` - Display the interactive playground (default)
- `playground: 'simple'` - Display a copyable endpoint with no playground
- `playground: 'none'` - Hide the playground entirely

3

[](#)

Add parameters and responses

Use [parameter and response fields](https://www.mintlify.com/docs/components/fields) to document your endpoint’s parameters and return values.
```
<ParamField path="userId" type="string" required>
  Unique identifier for the user
</ParamField>

<ParamField body="email" type="string" required>
  User's email address
</ParamField>

<ResponseField name="id" type="string" required>
  Unique identifier for the newly created user
</ResponseField>

<ResponseField name="email" type="string" required>
  User's email address
</ResponseField>
```
4

[](#)

Add your endpoints to your docs

Add your endpoint pages to the navigation by updating the `pages` field in your `docs.json`:

docs.json
```
"navigation": {
  "tabs": [
    {
      "tab": "API Reference",
      "groups": [
        {
          "group": "Users",
          "pages": [
            "api-reference/users/create-user",
            "api-reference/users/get-user",
            "api-reference/users/update-user"
          ]
        },
        {
          "group": "Orders",
          "pages": [
            "api-reference/orders/create-order",
            "api-reference/orders/list-orders"
          ]
        }
      ]
    }
  ]
}
```
Each page path corresponds to an MDX file in your docs repository. For example, `api-reference/users/create-user.mdx`. Learn more about structuring your docs in [Navigation](https://www.mintlify.com/docs/organize/navigation).

###

[​](#using-openapi-endpoints-in-navigation)

Using OpenAPI endpoints in navigation

If you have an OpenAPI specification, you can reference endpoints directly in your navigation without creating individual MDX files. Reference specific endpoints by including the OpenAPI file path and the endpoint:

docs.json
```
"navigation": {
  "pages": [
    "introduction",
    "/path/to/users-openapi.json POST /users",
    "/path/to/orders-openapi.json GET /orders"
  ]
}
```
You can also set a default OpenAPI spec for a navigation group and reference endpoints by method and path:

docs.json
```
{
  "group": "API reference",
  "openapi": "/path/to/openapi-v1.json",
  "pages": [
    "overview",
    "authentication",
    "GET /users",
    "POST /users",
    {
      "group": "Orders",
      "openapi": "/path/to/openapi-v2.json",
      "pages": [
        "GET /orders",
        "POST /orders"
      ]
    }
  ]
}
```
For more details on OpenAPI integration, see [OpenAPI setup](https://www.mintlify.com/docs/api-playground/openapi-setup).

##

[​](#enable-authentication)

Enable authentication

You can set authentication globally in `docs.json` or override it on individual pages using the `authMethod` field in frontmatter. A page-specific method overrides the global setting.

###

[​](#bearer-token)

Bearer token

docs.json

Page Metadata
```
"api": {
  "mdx": {
    "auth": {
      "method": "bearer"
    }
  }
}
```

###

[​](#basic-authentication)

Basic authentication

docs.json

Page Metadata
```
"api": {
  "mdx": {
    "auth": {
      "method": "basic"
    }
  }
}
```

###

[​](#api-key)

API key

docs.json

Page Metadata
```
"api": {
  "mdx": {
    "auth": {
      "method": "key",
      "name": "x-api-key"
    }
  }
}
```

###

[​](#none)

None

To disable authentication on a specific page, set `authMethod` to `none`:

Page Metadata
```
---
title: "Your page title"
authMethod: "none"
---
```
Was this page helpful?

YesNo

[Multiple responsesPrevious](https://www.mintlify.com/docs/api-playground/multiple-responses)[AsyncAPI setupNext](https://www.mintlify.com/docs/api-playground/asyncapi-setup)

⌘I
