---
url: https://mintlify.com/docs/ai/contextual-menu
canonical: https://www.mintlify.com/docs/ai/contextual-menu
title: "Contextual menu - Mintlify"
description: "Add one-click AI integrations to your docs."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Optimize

Contextual menu

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

The contextual menu provides quick access to AI-optimized content and direct integrations with popular AI tools. When users select the contextual menu on any page, they can copy content as context for AI tools or open conversations in ChatGPT, Claude, Perplexity, or a custom tool of your choice with your documentation already loaded as context.

##

[​](#menu-options)

Menu options

The contextual menu includes several pre-built options that you can enable by adding their identifier to your configuration.

| Option | Identifier | Description |
| --- | --- | --- |
| **Copy page** | `copy` | Copies the current page as Markdown for pasting as context into AI tools |
| **View as Markdown** | `view` | Opens the current page as Markdown |
| **Open in ChatGPT** | `chatgpt` | Creates a ChatGPT conversation with the current page as context |
| **Open in Claude** | `claude` | Creates a Claude conversation with the current page as context |
| **Open in Perplexity** | `perplexity` | Creates a Perplexity conversation with the current page as context |
| **Open in Grok** | `grok` | Creates a Grok conversation with the current page as context |
| **Copy MCP server URL** | `mcp` | Copies your MCP server URL to the clipboard |
| **Copy MCP install command** | `add-mcp` | Copies the `npx add-mcp` command to install the MCP server |
| **Connect to Cursor** | `cursor` | Installs your hosted MCP server in Cursor |
| **Connect to VS Code** | `vscode` | Installs your hosted MCP server in VS Code |
| **Custom options** | Object | Add custom options to the contextual menu |

![The expanded contextual menu showing the Copy page, View as Markdown, Open in ChatGPT, and Open in Claude menu items.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/contextual-menu/contextual-menu.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=b37c2bfffdc0db86422a7f7e692adaf7)

##

[​](#enabling-the-contextual-menu)

Enabling the contextual menu

Add the `contextual` field to your `docs.json` file and specify which options you want to include.
```
{
 "contextual": {
   "options": [
     "copy",
     "view",
     "chatgpt",
     "claude",
     "perplexity",
     "grok",
     "mcp",
     "cursor",
     "vscode"
   ]
 }
}
```

##

[​](#adding-custom-options)

Adding custom options

Create custom options in the contextual menu by adding an object to the `options` array. Each custom option requires these properties:

[​](#param-title)

title

string

required

The title of the option.

[​](#param-description)

description

string

required

The description of the option. Displayed beneath the title when the contextual menu is expanded.

[​](#param-icon)

icon

string

required

The icon to display.Options:

- [Font Awesome icon](https://fontawesome.com/icons) name, if you have the `icons.library` [property](https://www.mintlify.com/docs/organize/settings#param-icons) set to `fontawesome` in your `docs.json`
- [Lucide icon](https://lucide.dev/icons) name, if you have the `icons.library` [property](https://www.mintlify.com/docs/organize/settings#param-icons) set to `lucide` in your `docs.json`
- [Tabler icon](https://tabler.io/icons) name, if you have the `icons.library` [property](https://www.mintlify.com/docs/organize/settings#param-icons) set to `tabler` in your `docs.json`
- URL to an externally hosted icon
- Path to an icon file in your project

[​](#param-icon-type)

iconType

string

The [Font Awesome](https://fontawesome.com/icons) icon style. Only used with Font Awesome icons.Options: `regular`, `solid`, `light`, `thin`, `sharp-solid`, `duotone`, `brands`.

[​](#param-href)

href

string | object

required

The href of the option. Use a string for simple links or an object for dynamic links with query parameters.

Show href object

[​](#param-base)

base

string

required

The base URL for the option.

[​](#param-query)

query

object

required

The query parameters for the option.

Show query object

[​](#param-key)

key

string

required

The query parameter key.

[​](#param-value)

value

string

required

The query parameter value. We will replace the following placeholders with the corresponding values:

- Use `$page` to insert the current page content in Markdown.
- Use `$path` to insert the current page path.
- Use `$mcp` to insert the hosted MCP server URL.

Example custom option:
```
{
    "contextual": {
        "options": [
            "copy",
            "view",
            "chatgpt",
            "claude",
            "perplexity",
            {
                "title": "Request a feature",
                "description": "Join the discussion on GitHub to request a new feature",
                "icon": "plus",
                "href": "https://github.com/orgs/mintlify/discussions/categories/feature-requests"
            }
        ]
    }
}
```

###

[​](#custom-option-examples)

Custom option examples

Simple link
```
{
  "title": "Request a feature",
  "description": "Join the discussion on GitHub",
  "icon": "plus",
  "href": "https://github.com/orgs/mintlify/discussions/categories/feature-requests"
}
```
Dynamic link with page content
```
{
  "title": "Share on X",
  "description": "Share this page on X",
  "icon": "x",
  "href": {
    "base": "https://x.com/intent/tweet",
    "query": [
      {
      "key": "text",
      "value": "Check out this documentation: $page"
      }
    ]
  }
}
```
Was this page helpful?

YesNo

[Slack botPrevious](https://www.mintlify.com/docs/ai/slack-bot)[AnalyticsNext](https://www.mintlify.com/docs/optimize/analytics)

⌘I

![The expanded contextual menu showing the Copy page, View as Markdown, Open in ChatGPT, and Open in Claude menu items.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/contextual-menu/contextual-menu.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=e1a176c05eda0b2ebcba63d57631a57e)
