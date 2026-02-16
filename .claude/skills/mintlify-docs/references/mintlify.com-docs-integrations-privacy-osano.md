---
url: https://mintlify.com/docs/integrations/privacy/osano
canonical: https://www.mintlify.com/docs/integrations/privacy/osano
title: "Osano - Mintlify"
description: "Manage cookie consent with Osano privacy platform."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Privacy

Osano

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

    -   Support

    -   Privacy

        -   [Privacy integrations](https://www.mintlify.com/docs/integrations/privacy/overview)
        -   [Osano](https://www.mintlify.com/docs/integrations/privacy/osano)

![US](https://d3gk2c5xim1je2.cloudfront.net/flags/US.svg)

English

Add [Osano](https://www.osano.com/) cookie consent to your docs with a [custom JavaScript file](https://www.mintlify.com/docs/customize/custom-scripts#custom-javascript) in your repository.

##

[​](#setup)

Setup

Create an `osano.js` file in your docs repository with the following content:

Format

Example
```
var script = document.createElement("script");
script.src = "OSANO_SCRIPT_URL";
document.head.appendChild(script);
```
Replace `OSANO_SCRIPT_URL` with your Osano script URL. Your script URL is the `src` value in the code snippet that Osano generates. Your script URL always starts with `https://cmp.osano.com/` and ends with `/osano.js`.

##

[​](#troubleshooting)

Troubleshooting

Pages not loading with Strict compliance mode

If your documentation pages aren’t loading properly when using Osano’s **Strict** compliance mode, you’ll need to whitelist Mintlify’s domain to allow images and other assets to load.

1

[](#)

Navigate to Managed Rules

In your Osano dashboard, go to **Scripts** → **Managed Rules**.

2

[](#)

Add Mintlify domain

Add `.mintlify.app/` as a managed rule.

![Osano managed rule](https://mintcdn.com/mintlify/Y6rP0BmbzgwHuEoU/images/integrations/osano-managed-rule.png?fit=max&auto=format&n=Y6rP0BmbzgwHuEoU&q=85&s=66a71862fce8aa19564959a171927597)

This ensures that all Mintlify-served assets (including images, stylesheets, and other documentation resources) are treated as essential and will load even when Osano blocks uncategorized third-party content.

Was this page helpful?

YesNo

[Privacy integrationsPrevious](https://www.mintlify.com/docs/integrations/privacy/overview)

⌘I

![Osano managed rule](https://mintcdn.com/mintlify/Y6rP0BmbzgwHuEoU/images/integrations/osano-managed-rule.png?w=1650&fit=max&auto=format&n=Y6rP0BmbzgwHuEoU&q=85&s=059d9d98c9e7c5b3159e36a04dd5a67b)
