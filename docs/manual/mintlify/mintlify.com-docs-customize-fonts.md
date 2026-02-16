---
url: https://mintlify.com/docs/customize/fonts
canonical: https://www.mintlify.com/docs/customize/fonts
title: "Fonts - Mintlify"
description: "Customize typography with Google Fonts or self-hosted fonts."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Customize

Fonts

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

Set a custom font for your entire site or separately for headings and body text. Use Google Fonts, local font files, or externally hosted fonts. The default font varies by theme. Fonts are controlled by the [fonts property](https://www.mintlify.com/docs/organize/settings#param-fonts) in your `docs.json`.

##

[​](#google-fonts)

Google Fonts

Mintlify automatically loads [Google Fonts](https://fonts.google.com) when you specify a font family name in your `docs.json`.

docs.json
```
"fonts": {
  "family": "Inter"
}
```

##

[​](#local-fonts)

Local fonts

To use local fonts, place your font files in your project directory and reference them in your `docs.json` configuration.

###

[​](#setting-up-local-fonts)

Setting up local fonts

1

[](#)

Add font files to your project

For example, create a `fonts` directory and add your font files:
```
your-project/
├── fonts/
│   ├── InterDisplay-Regular.woff2
│   └── InterDisplay-Bold.woff2
├── docs.json
└── ...
```
2

[](#)

Configure fonts in docs.json

Reference your local fonts using relative paths from your project root:

docs.json
```
{
  "fonts": {
    "family": "InterDisplay",
    "source": "/fonts/InterDisplay-Regular.woff2",
    "format": "woff2",
    "weight": 400
  }
}
```

###

[​](#local-fonts-for-headings-and-body)

Local fonts for headings and body

Configure separate local fonts for headings and body text in your `docs.json`:

docs.json
```
{
  "fonts": {
    "heading": {
      "family": "InterDisplay",
      "source": "/fonts/InterDisplay-Bold.woff2",
      "format": "woff2",
      "weight": 700
    },
    "body": {
      "family": "InterDisplay",
      "source": "/fonts/InterDisplay-Regular.woff2",
      "format": "woff2",
      "weight": 400
    }
  }
}
```

##

[​](#externally-hosted-fonts)

Externally hosted fonts

Use externally hosted fonts by referencing a font source URL in your `docs.json`:

docs.json
```
{
  "fonts": {
    "family": "Hubot Sans",
    "source": "https://mintlify-assets.b-cdn.net/fonts/Hubot-Sans.woff2",
    "format": "woff2",
    "weight": 400
  }
}
```

##

[​](#font-configuration-reference)

Font configuration reference

[​](#param-fonts)

fonts

object

Font configuration for your documentation.

Show Fonts

[​](#param-family)

family

string

required

Font family name, such as “Inter” or “Playfair Display”.

[​](#param-weight)

weight

number

Font weight, such as 400 or 700. Variable fonts support precise weights such as 550.

[​](#param-source)

source

string (uri)

URL to your font source, such as `https://mintlify-assets.b-cdn.net/fonts/Hubot-Sans.woff2`, or path to your local font file, such as `/assets/fonts/InterDisplay.woff2`. Google Fonts are loaded automatically when you specify a Google Font `family` name, so no source URL is needed.

[​](#param-format)

format

'woff' | 'woff2'

Font file format. Required when using the `source` field.

[​](#param-heading)

heading

object

Override font settings specifically for headings.

Show Heading

[​](#param-family-1)

family

string

required

Font family name for headings.

[​](#param-weight-1)

weight

number

Font weight for headings.

[​](#param-source-1)

source

string (uri)

URL to your font source, such as `https://mintlify-assets.b-cdn.net/fonts/Hubot-Sans.woff2`, or path to your local font file for headings. Google Fonts are loaded automatically when you specify a Google Font `family` name, so no source URL is needed.

[​](#param-format-1)

format

'woff' | 'woff2'

Font file format for headings. Required when using the `source` field.

[​](#param-body)

body

object

Override font settings specifically for body text.

Show Body

[​](#param-family-2)

family

string

required

Font family name for body text.

[​](#param-weight-2)

weight

number

Font weight for body text.

[​](#param-source-2)

source

string (uri)

URL to your font source, such as `https://mintlify-assets.b-cdn.net/fonts/Hubot-Sans.woff2`, or path to your local font file for body text. Google Fonts are loaded automatically when you specify a Google Font `family` name, so no source URL is needed.

[​](#param-format-2)

format

'woff' | 'woff2'

Font file format for body text. Required when using the `source` field.

Was this page helpful?

YesNo

[ThemesPrevious](https://www.mintlify.com/docs/customize/themes)[Custom scriptsNext](https://www.mintlify.com/docs/customize/custom-scripts)

⌘I
