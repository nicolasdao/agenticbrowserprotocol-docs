---
url: https://mintlify.com/docs/ai/llmstxt
canonical: https://www.mintlify.com/docs/ai/llmstxt
title: "llms.txt - Mintlify"
description: "Optimize your docs for LLMs to read and index."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Optimize

llms.txt

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

The [llms.txt file](https://llmstxt.org) is an industry standard that helps LLMs index content more efficiently, similar to how a sitemap helps search engines. AI tools can use this file to understand your documentation structure and find content relevant to user queries. Mintlify automatically hosts an `llms.txt` file at the root of your project that lists all available pages in your documentation. This file is always up to date and requires zero maintenance. You can optionally add a custom `llms.txt` file to the root of your project.

If your site requires authentication to access your documentation, your `llms.txt` and `llms-full.txt` files are not available to LLMs and AI tools. LLMs and AI tools can only index publicly available content.

View your `llms.txt` by appending `/llms.txt` to your documentation site’s URL. [Open the llms.txt for this site.](https://mintlify.com/docs/llms.txt)

##

[​](#llms-txt-structure)

llms.txt structure

An `llms.txt` file is a plain Markdown file that contains:

- **Site title** as an H1 heading.
- **Structured content sections** with links and a description of each page in your documentation.

Pages are listed alphabetically in the order they appear in your repository, starting from the root directory. Each page’s description comes from the `description` field in its frontmatter. Pages without a `description` field appear in the `llms.txt` file without a description.

Example llms.txt
```

# Site title

## Docs

- [API](https://example.com/docs/api): Endpoint list and usage
- [Install](https://example.com/docs/install): Setup steps
- [Getting started](https://example.com/docs/start): Intro guide
```
This structured approach allows LLMs to efficiently process your documentation at a high level and locate relevant content for user queries, improving the accuracy and speed of AI-assisted documentation searches.

##

[​](#llms-full-txt)

llms-full.txt

The `llms-full.txt` file combines your entire documentation site into a single file as context for AI tools and is indexed by LLM traffic. Mintlify automatically hosts an `llms-full.txt` file at the root of your project. View your `llms-full.txt` by appending `/llms-full.txt` to your documentation site’s URL. [Open the llms-full.txt for this site.](https://mintlify.com/docs/llms-full.txt)

##

[​](#custom-files)

Custom files

To add a custom `llms.txt` or `llms-full.txt` file, create an `llms.txt` or `llms-full.txt` file at the root of your project. Adding a custom file will override the automatically generated file of the same name. If you delete a custom file, the default file will be used again. Your custom `llms.txt` or `llms-full.txt` file must have a site title as an H1 heading. Other content is optional. See [Format](https://llmstxt.org/#format) in the `llms.txt` specification for more information on optional sections and best practices.

Was this page helpful?

YesNo

[FeedbackPrevious](https://www.mintlify.com/docs/optimize/feedback)[skill.mdNext](https://www.mintlify.com/docs/ai/skillmd)

⌘I
