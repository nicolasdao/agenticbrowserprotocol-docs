---
url: https://mintlify.com/docs/api-playground/complex-data-types
canonical: https://www.mintlify.com/docs/api-playground/complex-data-types
title: "Complex data types - Mintlify"
description: "Describe APIs with flexible schemas, optional properties, and multiple data formats using oneOf, anyOf, and allOf keywords."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Document APIs

Complex data types

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

When your API accepts multiple data formats, has conditional fields, or uses inheritance patterns, OpenAPI’s schema composition keywords help you document these flexible structures. Using `oneOf`, `anyOf`, and `allOf`, you can describe APIs that handle different input types or combine multiple schemas into comprehensive data models.

##

[​](#oneof-anyof-allof-keywords)

`oneOf`, `anyOf`, `allOf` keywords

For complex data types, OpenAPI provides keywords for combining schemas:

- `allOf`: Combines multiple schemas (like merging objects or extending a base schema). Functions like an `and` operator.
- `anyOf`: Accepts data matching any of the provided schemas. Functions like an `or` operator.
- `oneOf`: Accepts data matching exactly one of the provided schemas. Functions like an `exclusive-or` operator.

Mintlify treats `oneOf` and `anyOf` identically since the practical difference rarely affects using the API.

For detailed specifications of these keywords see the [OpenAPI documentation](https://swagger.io/docs/specification/data-models/oneof-anyof-allof-not/).

The `not` keyword is currently unsupported.

###

[​](#combining-schemas-with-allof)

Combining schemas with `allOf`

When you use `allOf`, Mintlify performs some preprocessing on your OpenAPI document to display complex combinations in a readable way. For example, when you combine two object schemas with `allOf`, Mintlify combines the properties of both into a single object. This becomes especially useful when leveraging OpenAPI’s reusable [components](https://swagger.io/docs/specification/components/).
```
org_with_users:
  allOf:
    - $ref: '#/components/schemas/Org'
    - type: object
      properties:
        users:
          type: array
          description: An array containing all users in the organization

# ...
components:
  schemas:
    Org:
      type: object
      properties:
        id:
          type: string
          description: The ID of the organization
```
[​](#param-org-with-users)

org\_with\_users

object

Show child attributes

[​](#param-id)

id

string

The ID of the organization

[​](#param-users)

users

object\[\]

An array containing all users in the organization

###

[​](#providing-options-with-oneof-and-anyof)

Providing options with `oneOf` and `anyOf`

When you use `oneOf` or `anyOf`, the options are displayed in a tabbed container. Specify a `title` field in each subschema to give your options names. For example, here’s how you might display two different types of delivery addresses:
```
delivery_address:
  oneOf:
    - title: StreetAddress
      type: object
      properties:
        address_line_1:
          type: string
          description: The street address of the recipient
        # ...
    - title: POBox
      type: object
      properties:
        box_number:
          type: string
          description: The number of the PO Box
        # ...
```
[​](#param-delivery-address)

delivery\_address

object

- StreetAddress

- POBox


[​](#param-address-line-1)

address\_line\_1

string

The street address of the residence

[​](#param-box-number)

box\_number

string

The number of the PO Box

Was this page helpful?

YesNo

[OpenAPI setupPrevious](https://www.mintlify.com/docs/api-playground/openapi-setup)[Add SDK examplesNext](https://www.mintlify.com/docs/api-playground/adding-sdk-examples)

⌘I
