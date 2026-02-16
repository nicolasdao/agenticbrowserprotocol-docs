---
url: https://mintlify.com/docs/api-playground/troubleshooting
canonical: https://www.mintlify.com/docs/api-playground/troubleshooting
title: "Troubleshooting - Mintlify"
description: "Resolve common issues with API page configuration."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Document APIs

Troubleshooting

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

If your API pages aren’t displaying correctly, check these common configuration issues.

All of my OpenAPI pages are completely blank

In this scenario, it’s likely that either Mintlify cannot find your OpenAPI document, or your OpenAPI document is invalid.Running `mint dev` locally should reveal some of these issues.To verify your OpenAPI document will pass validation:

1.  Visit [this validator](https://editor.swagger.io/)
2.  Switch to the “Validate text” tab
3.  Paste in your OpenAPI document
4.  Click “Validate it!”

If the text box that appears below has a green border, your document has passed validation. This is the exact validation package Mintlify uses to validate OpenAPI documents, so if your document passes validation here, there’s a great chance the problem is elsewhere.Additionally, Mintlify does not support OpenAPI 2.0. If your document uses this version of the specification, you could encounter this issue. You can convert your document at [editor.swagger.io](https://editor.swagger.io/) (under Edit > Convert to OpenAPI 3):

![Screenshot of the Swagger Editor with the Edit menu expanded and the "Convert to OpenAPI 3" menu item highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/convert-oas-3.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=3a45e89b8847e632d20b0ae9b3b5d689)

One of my OpenAPI pages is completely blank

This is usually caused by a misspelled `openapi` field in the page metadata. Make sure the HTTP method and path match the HTTP method and path in the OpenAPI document exactly.Here’s an example of how things might go wrong:

get-user.mdx
```
---
openapi: "GET /users/{id}/"
---
```
openapi.yaml
```
paths:
  "/users/{id}":
    get: ...
```
Notice that the path in the `openapi` field has a trailing slash, whereas the path in the OpenAPI document does not.Another common issue is a misspelled filename. If you are specifying a particular OpenAPI document in the `openapi` field, ensure the filename is correct. For example, if you have two OpenAPI documents `openapi/v1.json` and `openapi/v2.json`, your metadata might look like this:

api-reference/v1/users/get-user.mdx
```
---
openapi: "v1 GET /users/{id}"
---
```
Requests from the API Playground don't work

If you have a custom domain configured, this could be an issue with your reverse proxy. By default, requests made via the API Playground start with a `POST` request to the `/_mintlify/api/request` path on the docs site. If your reverse proxy is configured to only allow `GET` requests, then all of these requests will fail. To fix this, configure your reverse proxy to allow `POST` requests to the `/_mintlify/api/request` path.Alternatively, if your reverse proxy prevents you from accepting `POST` requests, you can configure Mintlify to send requests directly to your backend with the `api.playground.proxy` setting in the `docs.json`, as described in the [settings documentation](https://www.mintlify.com/docs/organize/settings#param-proxy). When using this configuration, you will need to configure CORS on your server since requests will come directly from users’ browsers rather than through your proxy.

OpenAPI navigation entries are not generating pages

If you are using an OpenAPI navigation configuration, but the pages aren’t generating, check these common issues:

1.  **Missing default OpenAPI spec**: Ensure you have an `openapi` field set for the navigation element:
```
"navigation": {
  "groups": [
    {
      "group": "API reference",
      "openapi": "/path/to/openapi.json",
      "pages": [
        "GET /users",
        "POST /users"
      ]
    }
  ]
}
```
2.  **OpenAPI spec inheritance**: If using nested navigation, ensure child groups inherit the correct OpenAPI spec or specify their own.
3.  **Validation issues**: Use `mint openapi-check <path-to-openapi-file>` to verify your OpenAPI document is valid.

Some OpenAPI operations appear in navigation but others don't

1.  **Hidden operations**: Operations marked with `x-hidden: true` in your OpenAPI spec won’t appear in auto-generated navigation.
2.  **Invalid operations**: Operations with validation errors in the OpenAPI spec may be skipped. Check your OpenAPI document for syntax errors.
3.  **Manual vs automatic inclusion**: If you reference any endpoints from an OpenAPI spec, only the explicitly referenced operations will appear in navigation. No other pages will be automatically added. This includes operations that are referenced in child navigation elements.

Mixed navigation (OpenAPI and MDX pages) not working correctly

When combining OpenAPI operations with regular documentation pages in navigation:

1.  **File conflicts**: You cannot have both an `MDX` file and a navigation entry for the same operation. For example, if you have `get-users.mdx`, do not also include `"GET /users"` in your navigation. If you need to have a file that shares a name with an operation, use the `x-mint` extension for the endpoint to have the href point to a different location.
2.  **Path resolution**: Navigation entries that don’t match OpenAPI operations will be treated as file paths. Ensure your `MDX` files exist at the expected locations.
3.  **Case sensitivity**: OpenAPI operation matching is case-sensitive. Ensure HTTP methods are uppercase in navigation entries.

Was this page helpful?

YesNo

[AsyncAPI setupPrevious](https://www.mintlify.com/docs/api-playground/asyncapi-setup)[DeploymentsNext](https://www.mintlify.com/docs/deploy/deployments)

⌘I

![Screenshot of the Swagger Editor with the Edit menu expanded and the "Convert to OpenAPI 3" menu item highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/convert-oas-3.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=1560b49e5d0197e873181f13c920486a)
