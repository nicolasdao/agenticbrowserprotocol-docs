---
url: https://mintlify.com/docs/create/changelogs
canonical: https://www.mintlify.com/docs/create/changelogs
title: "Changelogs - Mintlify"
description: "Create product changelogs with RSS feed support for subscribers."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Create content

Changelogs

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

Create a changelog for your docs by adding [Update components](https://www.mintlify.com/docs/components/update) to a page. Check out the [Mintlify changelog](https://www.mintlify.com/docs/changelog) as an example: you can include links, images, text, and demos of your new features in each update.

##

[​](#setting-up-your-changelog)

Setting up your changelog

1

[](#)

Create a page for your changelog

1.  Create a new page in your docs such as `changelog.mdx` or `updates.mdx`.
2.  Add your changelog page to your navigation scheme in your `docs.json`.

2

[](#)

Add Update components to your changelog

Add an `Update` for each changelog entry.Include relevant information like feature releases, bug fixes, or other announcements.

Example changelog.mdx
```
---
title: "Changelog"
description: "Product updates and announcements"
---
<Update label="March 2025" description="v0.0.10">
  Added a new Wintergreen flavor.

  Released a new version of the Spearmint flavor, now with 10% more mint.
</Update>

<Update label="February 2025" description="v0.0.09">
  Released a new version of the Spearmint flavor.
</Update>
```

##

[​](#customizing-your-changelog)

Customizing your changelog

Control how people navigate your changelog and stay up to date with your product information. Each `label` property for an `Update` automatically creates an entry in the right sidebar’s table of contents. This is the default navigation for your changelog.

![Changelog with table of contents displayed in light mode.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/changelog-toc-light.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=3f3018782389da4ccab476fbecfaa84b)![Changelog with table of contents displayed in dark mode.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/changelog-toc-dark.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=d8e69af3525f597335e5d2dcb6ec8192)

###

[​](#tag-filters)

Tag filters

Add `tags` to your `Update` components to replace the table of contents with tag filters. Users can filter the changelog by selecting one or more tags:

Tag filters example
```
<Update label="March 2025" description="v0.0.10" tags={["Wintergreen", "Spearmint"]}>
  Added a new Wintergreen flavor.

  Released a new version of the Spearmint flavor, now with 10% more mint.
</Update>

<Update label="February 2025" description="v0.0.09" tags={["Spearmint"]}>
  Released a new version of the Spearmint flavor.
</Update>

<Update label="January 2025" description="v0.0.08" tags={["Peppermint", "Spearmint"]}>
  Deprecated the Peppermint flavor.

  Released a new version of the Spearmint flavor.
</Update>
```
![Changelog in light mode with the Peppermint tag filter selected.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/changelog-filters-light.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=1c6e5fc5902e27e520fa217924871589)![Changelog in dark mode with the Peppermint tag filter selected.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/changelog-filters-dark.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=5aad3dbe45acd21db99dfae04b4846f7)

The table of contents and changelog filters are hidden when using `custom`, `center`, or `wide` page modes. Learn more about [page modes](https://www.mintlify.com/docs/organize/pages#page-mode).

###

[​](#subscribable-changelogs)

Subscribable changelogs

RSS feeds are only available on public documentation.

Use `Update` components to create a subscribable RSS feed at your page URL with `/rss.xml` appended. For example, `mintlify.com/docs/changelog/rss.xml`. The RSS feed publishes entries when you add new `Update` components and when modify headings inside of existing `Update` components. RSS feed entries contain pure Markdown only. Components, code, and HTML elements are excluded. Use the `rss` property to provide alternative text descriptions for RSS subscribers when your updates include content that is excluded.

Example RSS feed
```
<?xml version="1.0" encoding="UTF-8"?>
<rss xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:content="http://purl.org/rss/1.0/modules/content/" xmlns:atom="http://www.w3.org/2005/Atom" version="2.0">
  <channel>
    <title><![CDATA[Product updates]]></title>
    <description><![CDATA[New updates and improvements]]></description>
    <link>https://mintlify.com/docs</link>
    <generator>RSS for Node</generator>
    <lastBuildDate>Mon, 21 Jul 2025 21:21:47 GMT</lastBuildDate>
    <atom:link href="https://mintlify.com/docs/changelog/rss.xml" rel="self" type="application/rss+xml"/>
    <copyright><![CDATA[Mintlify]]></copyright>
    <docs>https://mintlify.com/docs</docs>
    <item>
      <title><![CDATA[June 2025]]></title>
      <link>https://mintlify.com/docs/changelog#june-2025</link>
      <guid isPermaLink="true">https://mintlify.com/docs/changelog#june-2025</guid>
      <pubDate>Mon, 23 Jun 2025 16:54:22 GMT</pubDate>
    </item>
  </channel>
</rss>
```
RSS feeds can integrate with Slack, email, or other subscription tools to notify users of product changes. Some options include:

- [Slack](https://slack.com/help/articles/218688467-Add-RSS-feeds-to-Slack)
- [Email](https://zapier.com/apps/email/integrations/rss/1441/send-new-rss-feed-entries-via-email) via Zapier
- Discord bots like [Readybot](https://readybot.io) or [RSS Feeds to Discord Bot](https://rss.app/en/bots/rssfeeds-discord-bot)

To make the RSS feed discoverable, you can display an RSS icon button that links to the feed at the top of the page. Add `rss: true` to the page frontmatter:
```
---
rss: true
---
```
![Changelog page in light mode with RSS feed button enabled.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/changelog-rss-button-light.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=088f41b7cdb5f701909d2c5cea5e52fd)![Changelog page in dark mode with RSS feed button enabled.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/changelog-rss-button-dark.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=67b22fea2a8411fe4c38caf569a8bf5f)

Was this page helpful?

YesNo

[RedirectsPrevious](https://www.mintlify.com/docs/create/redirects)[PlaygroundNext](https://www.mintlify.com/docs/api-playground/overview)

⌘I

![Changelog with table of contents displayed in dark mode.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/changelog-toc-dark.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=6ea107d1ab6df90a20484eb05342205e)

![Changelog in dark mode with the Peppermint tag filter selected.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/changelog-filters-dark.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=6010f30b249bc7ec4535adddb16fda10)

![Changelog page in dark mode with RSS feed button enabled.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/changelog-rss-button-dark.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=18bf3c4cf2489d3eb996c3d6ffb54df7)
