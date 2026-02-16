---
url: https://mintlify.com/docs/create/text
canonical: https://www.mintlify.com/docs/create/text
title: "Format text - Mintlify"
description: "Learn how to format text, create headers, and style content."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Create content

Format text

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

##

[​](#headers)

Headers

Headers organize your content and create navigation anchors. They appear in the table of contents and help users scan your documentation.

###

[​](#creating-headers)

Creating headers

Use `#` symbols to create headers of different levels:
```

## Main section header

### Subsection header

#### Sub-subsection header
```
Use descriptive, keyword-rich headers that clearly indicate the content that follows. This improves both user navigation and search engine optimization.

###

[​](#disabling-anchor-links)

Disabling anchor links

By default, headers include clickable anchor links that allow users to link directly to specific sections. You can disable these anchor links using the `noAnchor` prop in HTML or React headers.

HTML header example

React header example
```
<h2 noAnchor>
Header without anchor link
</h2>
```
When `noAnchor` is used, the header will not display the anchor chip and clicking the header text will not copy the anchor link to the clipboard.

##

[​](#text-formatting)

Text formatting

We support most Markdown formatting for emphasizing and styling text.

###

[​](#basic-formatting)

Basic formatting

Apply these formatting styles to your text:

| Style | Syntax | Example | Result |
| --- | --- | --- | --- |
| **Bold** | `**text**` | `**important note**` | **important note** |
| _Italic_ | `_text_` | `_emphasis_` | _emphasis_ |
| Strikethrough | `~text~` | `~deprecated feature~` | deprecated feature |

###

[​](#combining-formats)

Combining formats

You can combine formatting styles:
```
**_bold and italic_**
**~~bold and strikethrough~~**
*~~italic and strikethrough~~*
```
_**bold and italic**_
**bold and strikethrough**
_italic and strikethrough_

###

[​](#superscript-and-subscript)

Superscript and subscript

For mathematical expressions or footnotes, use HTML tags:

| Type | Syntax | Example | Result |
| --- | --- | --- | --- |
| Superscript | `<sup>text</sup>` | `example<sup>2</sup>` | example2 |
| Subscript | `<sub>text</sub>` | `example<sub>n</sub>` | examplen |

##

[​](#links)

Links

Links help users navigate between pages and access external resources. Use descriptive link text to improve accessibility and user experience.

###

[​](#internal-links)

Internal links

Link to other pages in your documentation using root-relative paths:
```
[Quickstart](/quickstart)
[Steps](/components/steps)
```
[Quickstart](https://www.mintlify.com/docs/quickstart)
[Steps](https://www.mintlify.com/docs/components/steps)

###

[​](#external-links)

External links

For external resources, include the full URL:
```
[Markdown Guide](https://www.markdownguide.org/)
```
[Markdown Guide](https://www.markdownguide.org/)

###

[​](#broken-links)

Broken links

You can check for broken links in your documentation using the [CLI](https://www.mintlify.com/docs/installation):
```
mint broken-links
```

##

[​](#blockquotes)

Blockquotes

Blockquotes highlight important information, quotes, or examples within your content.

###

[​](#single-line-blockquotes)

Single line blockquotes

Add `>` before text to create a blockquote:
```
> This is a quote that stands out from the main content.
```
> This is a quote that stands out from the main content.

###

[​](#multi-line-blockquotes)

Multi-line blockquotes

For longer quotes or multiple paragraphs:
```
> This is the first paragraph of a multi-line blockquote.
>
> This is the second paragraph, separated by an empty line with `>`.
```
> This is the first paragraph of a multi-line blockquote. This is the second paragraph, separated by an empty line with `>`.

Use blockquotes sparingly to maintain their visual impact and meaning. Consider using [callouts](https://www.mintlify.com/docs/components/callouts) for notes, warnings, and other information.

##

[​](#mathematical-expressions)

Mathematical expressions

We support LaTeX for rendering mathematical expressions and equations. You can override automated detection by configuring `styles.latex` in your `docs.json` [settings](https://www.mintlify.com/docs/organize/settings#param-latex).

###

[​](#inline-math)

Inline math

Use single dollar signs, `$`, for inline mathematical expressions:
```
The Pythagorean theorem states that $(a^2 + b^2 = c^2)$ in a right triangle.
```
The Pythagorean theorem states that (a2+b2\=c2)(a^2 + b^2 = c^2) in a right triangle.

###

[​](#block-equations)

Block equations

Use double dollar signs, `$$`, for standalone equations:
```
$$
E = mc^2
$$
```
E\=mc2E = mc^2

LaTeX support requires proper mathematical syntax. Refer to the [LaTeX documentation](https://www.latex-project.org/help/documentation/) for comprehensive syntax guidelines.

##

[​](#line-breaks-and-spacing)

Line breaks and spacing

Control spacing and line breaks to improve content readability.

###

[​](#paragraph-breaks)

Paragraph breaks

Separate paragraphs with blank lines:
```
This is the first paragraph.

This is the second paragraph, separated by a blank line.
```
This is the first paragraph. This is the second paragraph, separated by a blank line.

###

[​](#manual-line-breaks)

Manual line breaks

Use HTML `<br />` tags for forced line breaks within paragraphs:
```
This line ends here.<br />
This line starts on a new line.
```
This line ends here.
This line starts on a new line.

In most cases, paragraph breaks with blank lines provide better readability than manual line breaks.

##

[​](#best-practices)

Best practices

###

[​](#content-organization)

Content organization

- Use headers to create clear content hierarchy
- Follow proper header hierarchy (don’t skip from H2 to H4)
- Write descriptive, keyword-rich header text

###

[​](#text-formatting-2)

Text formatting

- Use bold for emphasis, not for entire paragraphs
- Reserve italics for terms, titles, or subtle emphasis
- Avoid over-formatting that distracts from content

###

[​](#links-2)

Links

- Write descriptive link text instead of “click here” or “read more”
- Use root-relative paths for internal links
- Test links regularly to prevent broken references

Was this page helpful?

YesNo

[Install the CLIPrevious](https://www.mintlify.com/docs/installation)[Format codeNext](https://www.mintlify.com/docs/create/code)

⌘I
