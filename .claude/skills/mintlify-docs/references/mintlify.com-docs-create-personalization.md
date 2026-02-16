---
url: https://mintlify.com/docs/create/personalization
canonical: https://www.mintlify.com/docs/create/personalization
title: "Personalized content - Mintlify"
description: "Show custom content based on user data and authentication."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Create content

Personalized content

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

Personalization requires [authentication](https://www.mintlify.com/docs/deploy/authentication-setup) configured with OAuth or JWT.

Customize content for your users when they log in to your documentation site. You can prefill API keys, show content specific to a user’s plan or role, and filter API reference content based on group membership.

##

[​](#api-key-prefilling)

API key prefilling

Automatically populate API playground fields with user-specific values by returning matching field names in your user data. Include the values in the `apiPlaygroundInputs` field of your [user data](https://www.mintlify.com/docs/deploy/authentication-setup#user-data-format).
```
{
  "apiPlaygroundInputs": {
    "header": { "X-API-Key": "user_api_key_123" },
    "server": { "subdomain": "acme" }
  }
}
```
The field names must match the names defined in your OpenAPI specification. Only values that match the current endpoint’s security scheme are applied.

##

[​](#dynamic-mdx-content)

Dynamic MDX content

Display content based on user information like name, plan, or organization with the `user` variable in your MDX pages. Include custom data in the `content` field of your [user data](https://www.mintlify.com/docs/deploy/authentication-setup#user-data-format).
```
{
  "content": {
    "firstName": "Jane",
    "company": "Acme Corp",
    "plan": "Enterprise"
  }
}
```
Reference these values in your MDX.
```
Welcome back, {user.firstName}! Your {user.plan} plan includes 100 seats for members in your {user.company} organization.
```
For conditional rendering based on user data, use the `user` variable in JSX components.
```
{
  user.plan === 'enterprise'
    ? <>Contact your admin to enable this feature.</>
    : <>See <a href="https://yoursite.com/pricing">pricing</a> for information about upgrading.</>
}
```
The `user` variable is an empty object for logged-out users. Use optional chaining on all `user` fields to prevent errors. For example, `{user.org?.plan}` instead of `{user.org.plan}`.

##

[​](#page-visibility)

Page visibility

Restrict pages to specific user groups by adding `groups` to page frontmatter. Users must belong to at least one listed group to access the page.
```
---
title: "Admin settings"
groups: ["admin"]
---
```
For more details on how groups interact with public pages, see [Control access with groups](https://www.mintlify.com/docs/deploy/authentication-setup#control-access-with-groups).

##

[​](#openapi-content-filtering)

OpenAPI content filtering

Filter API reference content based on user groups with the `x-mint` extension in your OpenAPI specification. You can filter entire endpoints, individual schema properties, `oneOf` variants, and enum values.

###

[​](#filter-endpoints)

Filter endpoints

Add `x-mint.groups` to an operation or path to restrict the endpoint page to specific user groups. Users not in the listed groups won’t see the endpoint in navigation or be able to access its page.

Restricted operation

Restricted path
```
{
  "paths": {
    "/billing": {
      "get": {
        "summary": "Get billing details",
        "x-mint": {
          "groups": ["admin", "billing"]
        },
        "responses": {
          "200": {
            "description": "Billing details"
          }
        }
      }
    }
  }
}
```

###

[​](#filter-schema-properties)

Filter schema properties

Add `x-mint.groups` to individual properties within request bodies, parameters, or responses. Properties without `x-mint.groups` remain visible to all users.

Restricted property
```
{
  "components": {
    "schemas": {
      "User": {
        "type": "object",
        "properties": {
          "name": {
            "type": "string"
          },
          "internal_id": {
            "type": "string",
            "x-mint": {
              "groups": ["admin"]
            }
          }
        }
      }
    }
  }
}
```
In this example, all users see the `name` property. Only users in the `admin` group see the `internal_id` property.

###

[​](#filter-oneof-variants)

Filter oneOf variants

Add `x-mint.groups` to individual `oneOf` options to restrict which schema variants a user can see.

Restricted oneOf variant
```
{
  "schema": {
    "oneOf": [
      {
        "title": "Enterprise config",
        "type": "object",
        "x-mint": {
          "groups": ["enterprise"]
        },
        "properties": {
          "sso_enabled": { "type": "boolean" }
        }
      },
      {
        "title": "Standard config",
        "type": "object",
        "properties": {
          "notifications": { "type": "boolean" }
        }
      }
    ]
  }
}
```

###

[​](#filter-enum-values)

Filter enum values

Use the `x-mint-enum` extension to restrict individual enum values by group. List each restricted value as a key, with its allowed groups as the value. Enum values not listed in `x-mint-enum` are visible to all users.

Restricted enum values
```
{
  "type": "string",
  "enum": ["free", "pro", "enterprise"],
  "x-mint-enum": {
    "pro": ["pro", "enterprise"],
    "enterprise": ["enterprise"]
  }
}
```
In this example, all users see `free`. Users in the `pro` or `enterprise` groups see `pro`. Only users in the `enterprise` group see `enterprise`.

`x-mint-enum` is a separate top-level extension on the schema object, not nested under `x-mint`.

##

[​](#user-data-format)

User data format

Your authentication system returns user data that controls personalization. The `groups`, `content`, and `apiPlaygroundInputs` fields described on this page are all part of the user data object. For the full user data format and field reference, see [User data format](https://www.mintlify.com/docs/deploy/authentication-setup#user-data-format).

##

[​](#logout-behavior)

Logout behavior

Logout occurs on the client side. When users click the logout button, Mintlify clears their stored session data in the browser. To limit how long personalization data persists, set the `expiresAt` field in your user data.

Was this page helpful?

YesNo

[Reusable snippetsPrevious](https://www.mintlify.com/docs/create/reusable-snippets)[RedirectsNext](https://www.mintlify.com/docs/create/redirects)

⌘I
