---
url: https://mintlify.com/docs/organize/hidden-pages
canonical: https://www.mintlify.com/docs/organize/hidden-pages
title: "Hidden pages - Mintlify"
description: "Hide pages from your navigation while keeping them accessible."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Organize

Hidden pages

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

Hidden pages don’t appear in your site’s navigation, but anyone who knows the URL can still access them. For example, if you create a hidden page like `guides/hidden-page.mdx`, visitors can reach it at `docs.yoursite.com/guides/hidden-page`. Use hidden pages for content you want users to access or reference as context for AI tools, but don’t want listed in the navigation. If your content requires strict access control, you must configure [authentication](https://www.mintlify.com/docs/deploy/authentication-setup). To restrict pages to specific user groups, set up [group-based access control](https://www.mintlify.com/docs/deploy/authentication-setup#control-access-with-groups). See an [example of a hidden page](https://www.mintlify.com/docs/organize/hidden-page-example).

Some navigation elements like sidebars, dropdowns, and tabs may appear empty or shift layout on hidden pages.

##

[​](#hide-a-page)

Hide a page

To hide a page, set `hidden: true` in the page’s [frontmatter](https://www.mintlify.com/docs/organize/pages) or remove it from your `docs.json` navigation.

###

[​](#set-hidden-true-in-frontmatter)

Set `hidden: true` in frontmatter

Add `hidden: true` to a page’s frontmatter to remove it from the rendered navigation while still including it in your `docs.json` configuration.
```
---
title: "My hidden page"
hidden: true
---
```
Search engines cannot index pages with `hidden: true`. See [Disable indexing](https://www.mintlify.com/docs/optimize/seo#disabling-indexing) for more information.

###

[​](#remove-the-page-from-navigation)

Remove the page from navigation

If you don’t include a page in your `docs.json` navigation, you hide it. This method works well for pages that you don’t want to appear in navigation at all.

##

[​](#hide-a-group-of-pages)

Hide a group of pages

To hide a group of pages, set the `hidden` property to `true` for the group in your `docs.json` file:
```
"groups": [
  {
    "group": "Getting started",
    "hidden": true,
    "pages": [
      "index",
      "quickstart"
    ]
  },
  {
    "group": "Guides",
    "pages": [
      "guides/hidden-page.mdx",
      "guides/hidden-groups.mdx"
    ]
  }
]
```
In this example, the `Getting started` group is hidden and the `Guides` group is visible.

###

[​](#hide-a-tab)

Hide a tab

To hide a tab, add the `hidden` property for the tab in your `docs.json` file:
```
"tabs": [
  {
    "tab": "Home",
    "hidden": true,
    "pages": [
      "index",
      "quickstart"
    ]
  }
]
```

##

[​](#search-seo-and-ai-indexing)

Search, SEO, and AI indexing

By default, hidden pages don’t appear in indexing for search engines, documentation site search, or as AI assistant context. To include hidden pages in search results and assistant context, add the `seo` property to your `docs.json`:
```
"seo": {
    "indexing": "all"
}
```
To exclude a specific page, add `noindex: true` to its frontmatter.

Was this page helpful?

YesNo

[PagesPrevious](https://www.mintlify.com/docs/organize/pages)[Exclude files from publishingNext](https://www.mintlify.com/docs/organize/mintignore)

⌘I
