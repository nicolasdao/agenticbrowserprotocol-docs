---
url: https://mintlify.com/docs/integrations/sdks/stainless
canonical: https://www.mintlify.com/docs/integrations/sdks/stainless
title: "Stainless - Mintlify"
description: "Automate SDK code samples in your API playground."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

SDKs

Stainless

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

    -   Analytics

    -   SDKs

        -   [Speakeasy](https://www.mintlify.com/docs/integrations/sdks/speakeasy)
        -   [Stainless](https://www.mintlify.com/docs/integrations/sdks/stainless)
    -   Support

    -   Privacy


![US](https://d3gk2c5xim1je2.cloudfront.net/flags/US.svg)

English

##

[​](#prerequisites)

Prerequisites

- Have a [Stainless](https://app.stainless.com) account.

##

[​](#integrate-with-stainless)

Integrate with Stainless

1

[](#)

Set up OpenAPI decoration in Stainless.

In your `stainless.yml` config file, add `openapi.code_samples: 'mintlify'`. See the [Stainless documentation](https://app.stainless.com/docs/guides/integrate-docs) for more information.

2

[](#)

Publish the URL to your OpenAPI spec.

In your Stainless project:

1.  Select the **Release** tab.
2.  Select **Setup OpenAPI publishing**.
3.  Copy the URL to your publicly accessible OpenAPI spec.

![Stainless release page with the OpenAPI spec URL highlighted with a green box.](https://mintcdn.com/mintlify/f7fo9pnTEtzBD70_/images/stainless-public-OpenAPI-spec.png?fit=max&auto=format&n=f7fo9pnTEtzBD70_&q=85&s=74e968242d6e3c42818a57f2523ecdfe)

3

[](#)

Add your OpenAPI spec URL to your `docs.json`.

In your `docs.json` file, add the URL from Stainless to the `openapi` field. See [OpenAPI Setup](https://www.mintlify.com/docs/api-playground/openapi-setup) for more information.

Was this page helpful?

YesNo

[SpeakeasyPrevious](https://www.mintlify.com/docs/integrations/sdks/speakeasy)[Support integrationsNext](https://www.mintlify.com/docs/integrations/support/overview)

⌘I

![Stainless release page with the OpenAPI spec URL highlighted with a green box.](https://mintcdn.com/mintlify/f7fo9pnTEtzBD70_/images/stainless-public-OpenAPI-spec.png?w=1650&fit=max&auto=format&n=f7fo9pnTEtzBD70_&q=85&s=cc11946cfa1f54a50b72c4058548f2b3)
