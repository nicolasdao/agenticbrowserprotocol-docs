---
url: https://mintlify.com/docs/guides
canonical: https://www.mintlify.com/docs/organize/pages
alternate_urls:
  - https://mintlify.com/docs/guides
  - https://mintlify.com/docs/api/introduction
  - https://mintlify.com/docs/changelog
  - https://mintlify.com/docs/quickstart
  - https://mintlify.com/docs/ai-native
  - https://mintlify.com/docs/migration
  - https://mintlify.com/docs/organize/settings
  - https://mintlify.com/docs/organize/navigation
  - https://mintlify.com/docs/organize/pages
title: "Pages - Mintlify"
description: "Configure page metadata, titles, and frontmatter properties."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Organize

Pages

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

Each page is a Markdown file. You can use either `.mdx` or `.md` file types for your pages. We recommend MDX, which combines Markdown with React components for rich, interactive documentation. Plain Markdown (`.md`) can expedite migration from other platforms, but switching to MDX enables more features.

##

[​](#page-metadata)

Page metadata

Every page begins with frontmatter, the YAML metadata enclosed by `---` at the top of a file. This metadata controls how your page appears and behaves. Use frontmatter to control:

- Page titles and descriptions
- Sidebar titles, icons, and tags
- Page layouts
- SEO meta tags
- Custom metadata

[​](#param-title)

title

string

required

The title of your page that appears in navigation and browser tabs.

[​](#param-description)

description

string

A brief description of what this page covers. Displays under the title and improves SEO.

[​](#param-sidebar-title)

sidebarTitle

string

A short title that displays in the sidebar navigation.

[​](#param-icon)

icon

string

The icon to display.Options:

- [Font Awesome icon](https://fontawesome.com/icons) name
- [Lucide icon](https://lucide.dev/icons) name
- [Tabler icon](https://tabler.io/icons) name
- URL to an externally hosted icon
- Path to an icon file in your project

[​](#param-icon-type)

iconType

string

For [Font Awesome](https://fontawesome.com/icons) icons only. The style of the icon.Options: `regular`, `solid`, `light`, `thin`, `sharp-solid`, `duotone`, `brands`.

[​](#param-tag)

tag

string

A tag that appears next to your page title in the sidebar.

[​](#param-hidden)

hidden

boolean

Set to `true` to remove the page from the sidebar navigation. Users can still access the page via its URL, but search engines do not index it. See [Hidden pages](https://www.mintlify.com/docs/organize/hidden-pages) for details.

[​](#param-noindex)

noindex

boolean

Set to `true` to prevent search engines from indexing the page. See [Disable indexing](https://www.mintlify.com/docs/optimize/seo#disable-indexing) for details. All pages with `hidden: true` in their frontmatter receive `noindex: true` automatically.

[​](#param-custom)

<custom>

string

Any valid YAML frontmatter. For example, `product: "API"` or `version: "1.0.0"`.

Example YAML frontmatter
```
---
title: "About frontmatter"
description: "Frontmatter is the metadata that controls how your page appears and behaves"
sidebarTitle: "Frontmatter"
icon: "book"
tag: "NEW"
---
```

##

[​](#page-mode)

Page mode

Control your page’s layout with the `mode` setting.

###

[​](#default)

Default

If you do not define a mode, the page uses a standard layout with sidebar navigation and table of contents.
```
---
title: "Default page title"
---
```

###

[​](#wide)

Wide

Wide mode hides the table of contents. Use this mode for pages without headings or if you want extra horizontal space. Every theme supports wide mode.
```
---
title: "Wide page title"
mode: "wide"
---
```

###

[​](#custom)

Custom

Custom mode provides a minimalist layout and removes all elements except for the top navbar. Treat custom mode as a blank canvas to build landing pages or unique layouts with minimal navigation. All themes support custom mode.
```
---
title: "Custom page title"
mode: "custom"
---
```
The `style` property on custom mode pages may cause a layout shift on page load. Prefer [Tailwind CSS or custom CSS](https://www.mintlify.com/docs/customize/custom-scripts) to avoid this issue.

###

[​](#frame)

Frame

Frame mode provides a layout similar to custom mode but keeps the sidebar navigation. Use this mode to include custom HTML and components while preserving the default navigation experience. Only Aspen and Almond themes support frame mode.
```
---
title: "Frame page title"
mode: "frame"
---
```

###

[​](#center)

Center

Center mode removes the sidebar and table of contents, and centers the content. Use center mode for changelogs or other pages where you want to place focus on the content. Mint and Linden themes support center mode.
```
---
title: "Center page title"
mode: "center"
---
```

##

[​](#api-pages)

API pages

To create an interactive API playground, add an API specification to your frontmatter by setting `api` or `openapi`.
```
---
openapi: "GET /endpoint"
---
```
Learn more about building [API documentation](https://www.mintlify.com/docs/api-playground/overview).

##

[​](#external-links)

External links

Link to external sites directly from your navigation with the `url` metadata.
```
---
title: "npm Package"
url: "https://www.npmjs.com/package/mint"
---
```

##

[​](#search-engine-optimization)

Search engine optimization

Mintlify automatically generates most SEO meta tags. You can set SEO meta tags manually to customize your approach to SEO, social sharing, and browser compatibility.

Always wrap meta tags with colons in quotes.
```
---
"twitter:image": "/images/social-preview.jpg"
---
```
See [SEO](https://www.mintlify.com/docs/optimize/seo) for the full list of SEO metadata options.

##

[​](#internal-search-keywords)

Internal search keywords

Help users discover a specific page in search results by providing `keywords` in your metadata. These keywords don’t appear in page content. If users search for the keywords, the page appears in the search results.
```
---
keywords: ['configuration', 'setup', 'getting started']
---
```

##

[​](#last-modified-timestamp)

Last modified timestamp

Show a “Last modified on \[date\]” timestamp on all pages by enabling `metadata.timestamp` in your [global settings](https://www.mintlify.com/docs/organize/settings#metadata).

docs.json
```
"metadata": {
  "timestamp": true
}
```
To override the global timestamp setting for an individual page, use the `timestamp` frontmatter field. Use this field to show or hide timestamps on specific pages.
```
---
title: "Page title"
timestamp: false
---
```
If you set `timestamp: true`, the page always shows the timestamp even if the global setting is `false`. If you set `timestamp: false`, the page hides the timestamp even if the global setting is `true`.

Was this page helpful?

YesNo

[NavigationPrevious](https://www.mintlify.com/docs/organize/navigation)[Hidden pagesNext](https://www.mintlify.com/docs/organize/hidden-pages)

⌘I
