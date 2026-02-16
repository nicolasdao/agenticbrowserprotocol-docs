---
url: https://mintlify.com/docs/api-playground/openapi-setup
canonical: https://www.mintlify.com/docs/api-playground/openapi-setup
title: "OpenAPI setup - Mintlify"
description: "Generate API pages from your OpenAPI specification automatically."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Document APIs

OpenAPI setup

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

OpenAPI is a specification for describing APIs. Mintlify supports OpenAPI 3.0 and 3.1 documents to generate interactive API documentation and keep it up to date.

##

[​](#add-an-openapi-specification-file)

Add an OpenAPI specification file

To document your endpoints with OpenAPI, you need one or more valid OpenAPI specifications in either JSON or YAML format that follow the [OpenAPI specification 3.0 or 3.1](https://swagger.io/specification/). Add OpenAPI specifications to your documentation repository or host them online where you can access the specifications by URL. Reference any number of OpenAPI specifications in the navigation element of your `docs.json` to create pages for your API endpoints. Each specification file generates its own set of endpoints.

Single specification

Multiple specifications
```
"navigation": {
  "tabs": [
    {
      "tab": "API Reference",
      "openapi": "openapi.json"
    }
  ]
}
```
Mintlify supports `$ref` for **internal references only** within a single OpenAPI document. External references are not supported.

###

[​](#describe-your-api)

Describe your API

We recommend the following resources to learn about and construct your OpenAPI specification.

- [Swagger’s OpenAPI Guide](https://swagger.io/docs/specification/v3_0/basic-structure/) to learn the OpenAPI syntax.
- [The OpenAPI specification Markdown sources](https://github.com/OAI/OpenAPI-Specification/blob/main/versions/) to reference details of the latest OpenAPI specification.
- [Swagger Editor](https://editor.swagger.io/) to edit, validate, and debug your OpenAPI document.
- [The Mint CLI](https://www.npmjs.com/package/mint) to validate your OpenAPI document with the command: `mint openapi-check <openapiFilenameOrUrl>`.

Swagger’s OpenAPI Guide is for OpenAPI v3.0, but nearly all of the information is applicable to v3.1. For more information on the differences between v3.0 and v3.1, see [Migrating from OpenAPI 3.0 to 3.1.0](https://www.openapis.org/blog/2021/02/16/migrating-from-openapi-3-0-to-3-1-0) in the OpenAPI blog.

###

[​](#specify-the-base-url-for-your-api)

Specify the base URL for your API

To enable the API playground, add a `servers` field to your OpenAPI specification with your API’s base URL.
```
{
  "servers": [
    {
      "url": "https://api.example.com/v1"
    }
  ]
}
```
In an OpenAPI specification, different API endpoints are specified by their paths, like `/users/{id}` or simply `/`. The base URL defines where these paths should be appended. For more information on how to configure the `servers` field, see [API Server and Base Path](https://swagger.io/docs/specification/api-host-and-base-path/) in the OpenAPI documentation. The API playground uses these server URLs to determine where to send requests. If you specify multiple servers, a dropdown allows users to toggle between servers. If you do not specify a server, the API playground uses simple mode since it cannot send requests without a base URL. If your API has endpoints that exist at different URLs, you can [override the `servers` field](https://swagger.io/docs/specification/v3_0/api-host-and-base-path/#overriding-servers) for a given path or operation.

###

[​](#specify-authentication)

Specify authentication

To enable authentication in your API documentation and playground, configure the `securitySchemes` and `security` fields in your OpenAPI specification. The API descriptions and API playground add authentication fields based on the security configurations in your OpenAPI specification.

1

[](#)

Define your authentication method.

Add a `securitySchemes` field to define how users authenticate.This example shows a configuration for bearer authentication.
```
{
  "components": {
    "securitySchemes": {
      "bearerAuth": {
        "type": "http",
        "scheme": "bearer"
      }
    }
  }
}
```
2

[](#)

Apply authentication to your endpoints.

Add a `security` field to require authentication.
```
{
  "security": [
    {
      "bearerAuth": []
    }
  ]
}
```
Common authentication types include:

- [API Keys](https://swagger.io/docs/specification/authentication/api-keys/): For header, query, or cookie-based keys.
- [Bearer](https://swagger.io/docs/specification/authentication/bearer-authentication/): For JWT or OAuth tokens.
- [Basic](https://swagger.io/docs/specification/authentication/basic-authentication/): For username and password.

If different endpoints within your API require different methods of authentication, you can [override the `security` field](https://swagger.io/docs/specification/authentication/#:~:text=you%20can%20apply%20them%20to%20the%20whole%20API%20or%20individual%20operations%20by%20adding%20the%20security%20section%20on%20the%20root%20level%20or%20operation%20level%2C%20respectively.) for a given operation. For more information on defining and applying authentication, see [Authentication](https://swagger.io/docs/specification/authentication/) in the OpenAPI documentation.

##

[​](#customize-your-endpoint-pages)

Customize your endpoint pages

Customize your endpoint pages by adding the `x-mint` extension to your OpenAPI specification. The `x-mint` extension provides additional control over how your API documentation is generated and displayed.

###

[​](#metadata)

Metadata

Override the default metadata for generated API pages by adding `x-mint: metadata` to any operation. You can use any metadata field that would be valid in MDX frontmatter except for `openapi`.
```
{
  "paths": {
    "/users": {
      "get": {
        "summary": "Get users",
        "description": "Retrieve a list of users",
        "x-mint": {
          "metadata": {
            "title": "List all users",
            "description": "Fetch paginated user data with filtering options",
            "og:title": "Display a list of users"
          }
        },
        "parameters": [
          {
            // Parameter configuration
          }
        ]
      }
    }
  }
}
```
You can also control playground display per endpoint using the `playground` and `groups` metadata fields:
```
{
  "paths": {
    "/admin/users": {
      "post": {
        "summary": "Create admin user",
        "x-mint": {
          "metadata": {
            "playground": "auth",
            "groups": ["admin"],
            "public": true
          }
        }
      }
    }
  }
}
```
This configuration makes the page publicly visible while restricting the interactive playground to authenticated users in the `admin` group.

###

[​](#content)

Content

Add content before the auto-generated API documentation using `x-mint: content`. The `x-mint: content` extension supports all Mintlify MDX components and formatting.
```
{
  "paths": {
    "/users": {
      "post": {
        "summary": "Create user",
        "x-mint": {
          "content": "## Prerequisites\n\nThis endpoint requires admin privileges and has rate limiting.\n\n<Note>User emails must be unique across the system.</Note>"
        },
        "parameters": [
          {
            // Parameter configuration
          }
        ]
      }
    }
  }
}
```

###

[​](#href)

Href

Set the URL of the autogenerated endpoint page using `x-mint: href`. When `x-mint: href` is present, the generated API page uses the specified URL instead of the default autogenerated URL.
```
{
  "paths": {
    "/legacy-endpoint": {
      "get": {
        "summary": "Legacy endpoint",
        "x-mint": {
          "href": "/deprecated-endpoints/legacy-endpoint"
        }
      }
    },
    "/documented-elsewhere": {
      "post": {
        "summary": "Special endpoint",
        "x-mint": {
          "href": "/guides/special-endpoint-guide"
        }
      }
    }
  }
}
```

##

[​](#auto-populate-api-pages)

Auto-populate API pages

Add an `openapi` field to any navigation element in your `docs.json` to automatically generate pages for OpenAPI endpoints. You can control where these pages appear in your navigation structure, as dedicated API sections or with other pages. The `openapi` field accepts either a file path in your docs repo or a URL to a hosted OpenAPI document. Generated endpoint pages have these default metadata values:

- `title`: The operation’s `summary` field, if present. If there is no `summary`, the title is generated from the HTTP method and endpoint.
- `description`: The operation’s `description` field, if present.
- `version`: The `version` value from the parent anchor or tab, if present.
- `deprecated`: The operation’s `deprecated` field. If `true`, a deprecated label appears next to the endpoint title in the side navigation and on the endpoint page.

To exclude specific endpoints from your auto-generated API pages, add the [x-hidden](https://www.mintlify.com/docs/api-playground/managing-page-visibility#x-hidden) property to the operation in your OpenAPI spec.

There are two approaches for adding endpoint pages into your documentation:

1.  **Dedicated API sections**: Reference OpenAPI specs in navigation elements for dedicated API sections.
2.  **Selective endpoints**: Reference specific endpoints in your navigation alongside other pages.

###

[​](#dedicated-api-sections)

Dedicated API sections

Generate dedicated API sections by adding an `openapi` field to a navigation element and no other pages. All endpoints in the specification are included.
```
"navigation": {
  "tabs": [
    {
        "tab": "API Reference",
        "openapi": "https://petstore3.swagger.io/api/v3/openapi.json"
    }
  ]
}
```
To organize multiple OpenAPI specifications in separate sections of your documentation, assign each specification to a different group in your navigation hierarchy. Each group can reference its own OpenAPI specification.
```
"navigation": {
  "tabs": [
    {
      "tab": "API Reference",
      "groups": [
        {
          "group": "Users API",
          "openapi": {
            "source": "/path/to/users-openapi.json",
            "directory": "users-api-reference"
          }
        },
        {
          "group": "Admin API",
          "openapi": {
            "source": "/path/to/admin-openapi.json",
            "directory": "admin-api-reference"
          }
        }
      ]
    }
  ]
}
```
The `directory` field is optional and specifies where generated API pages are stored in your docs repo. If not specified, defaults to the `api-reference` directory of your repo.

###

[​](#selective-endpoints)

Selective endpoints

When you want more control over where endpoints appear in your documentation, you can reference specific endpoints in your navigation. This approach allows you to generate pages for API endpoints alongside other content. You can also use this approach to mix endpoints from different OpenAPI specifications.

####

[​](#set-a-default-openapi-spec)

Set a default OpenAPI spec

Configure a default OpenAPI specification for a navigation element. Then reference specific endpoints in the `pages` field.
```
"navigation": {
  "tabs": [
    {
      "tab": "Getting started",
      "pages": [
        "quickstart",
        "installation"
      ]
    },
    {
      "tab": "API reference",
      "openapi": "/path/to/openapi.json",
      "pages": [
        "api-overview",
        "GET /users",
        "POST /users",
        "guides/authentication"
      ]
    }
  ]
}
```
Any page entry matching the format `METHOD /path` generates an API page for that endpoint using the default OpenAPI specification.

####

[​](#openapi-spec-inheritance)

OpenAPI spec inheritance

OpenAPI specifications are inherited down the navigation hierarchy. Child navigation elements inherit their parent’s OpenAPI specification unless they define their own.
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

####

[​](#individual-endpoints)

Individual endpoints

Reference specific endpoints without setting a default OpenAPI specification by including the file path. You can reference endpoints from multiple OpenAPI specifications in the same documentation section.
```
"navigation": {
  "pages": [
    "introduction",
    "user-guides",
    "/path/to/users-openapi.json POST /users",
    "/path/to/orders-openapi.json GET /orders"
  ]
}
```
This approach is useful when you need individual endpoints from different specifications, only want to include select endpoints, or want to include endpoints alongside other types of documentation.

##

[​](#create-mdx-pages-from-your-openapi-specification)

Create MDX pages from your OpenAPI specification

For more granular control over individual endpoint pages, create MDX pages from your OpenAPI specification. This lets you customize page metadata, content, and reorder or exclude pages in your navigation while still using the auto-generated parameters and responses. There are two ways to document your OpenAPI specification with individual MDX pages:

- Document endpoints with the `openapi` field in the frontmatter.
- Document data models with the `openapi-schema` field in the frontmatter.

###

[​](#document-endpoints)

Document endpoints

Create a page for each endpoint and specify which OpenAPI operation to display using the `openapi` field in the frontmatter.

Example

Format
```
---
title: "Get users"
description: "Returns all plants from the system that the user has access to"
openapi: "/path/to/openapi-1.json GET /users"
deprecated: true
version: "1.0"
---
```
The method and path must exactly match your OpenAPI spec. If you have multiple OpenAPI specifications, include the file path in your reference. External OpenAPI URLs can be referenced in `docs.json`.

####

[​](#autogenerate-endpoint-pages)

Autogenerate endpoint pages

To autogenerate MDX files from your OpenAPI specification, use the Mintlify [scraper](https://www.npmjs.com/package/@mintlify/scraping).
```
npx @mintlify/scraping@latest openapi-file <path-to-openapi-file> -o <folder-name>
```
Add the `-o` flag to specify a folder to populate the files into. If a folder is not specified, the files will populate in the working directory.

###

[​](#document-data-models)

Document data models

Create a page for each data structure defined in your OpenAPI specification’s `components.schemas` using the `openapi-schema` field in the frontmatter.

Example

Format
```
---
openapi-schema: OrderItem
---
```
If you have schemas with the same name in multiple files, specify the OpenAPI file:

Example

Format
```
---
openapi-schema: en-schema.json OrderItem
---
```

##

[​](#webhooks)

Webhooks

Webhooks are HTTP callbacks that your API sends to notify external systems when events occur. Webhooks are supported in OpenAPI 3.1+ documents. Add a `webhooks` field to your OpenAPI document alongside the `paths` field. For more information on defining webhooks, see [Webhooks](https://spec.openapis.org/oas/v3.1.0#oasWebhooks) in the OpenAPI documentation. To create an MDX page for a webhook (OpenAPI 3.1+), use `webhook` instead of an HTTP method:
```
---
title: "Order updated webhook"
description: "Triggered when an order is updated"
openapi: "openapi.json webhook orderUpdated"
---
```
The webhook name must exactly match the key in your OpenAPI spec’s `webhooks` field.

Was this page helpful?

YesNo

[PlaygroundPrevious](https://www.mintlify.com/docs/api-playground/overview)[Complex data typesNext](https://www.mintlify.com/docs/api-playground/complex-data-types)

⌘I
