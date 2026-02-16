---
url: https://mintlify.com/docs/guides/linking
canonical: https://www.mintlify.com/docs/guides/linking
title: "Linking - Mintlify"
description: "Learn how to create internal links, reference API endpoints, and maintain link integrity across your documentation."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Best practices

Linking

Search...

⌘K

##### Overview

- [Guides](https://www.mintlify.com/docs/guides)

##### AI

- [Automate documentation updates](https://www.mintlify.com/docs/guides/automate-agent)
- [Build an in-app assistant](https://www.mintlify.com/docs/guides/assistant-embed)
- [Claude Code](https://www.mintlify.com/docs/guides/claude-code)
- [Cursor](https://www.mintlify.com/docs/guides/cursor)
- [GEO](https://www.mintlify.com/docs/guides/geo)
- [Windsurf](https://www.mintlify.com/docs/guides/windsurf)

##### API docs

- [Migrate from MDX to OAS](https://www.mintlify.com/docs/guides/migrating-from-mdx)

##### Best practices

- [Accessibility](https://www.mintlify.com/docs/guides/accessibility)
- [Content types](https://www.mintlify.com/docs/guides/content-types)
- [Content templates](https://www.mintlify.com/docs/guides/content-templates)
- [Improve your docs](https://www.mintlify.com/docs/guides/improving-docs)
- [Internationalization](https://www.mintlify.com/docs/guides/internationalization)
- [Linking](https://www.mintlify.com/docs/guides/linking)
- [Maintenance](https://www.mintlify.com/docs/guides/maintenance)
- [Media](https://www.mintlify.com/docs/guides/media)
- [Organize navigation](https://www.mintlify.com/docs/guides/navigation)
- [SEO](https://www.mintlify.com/docs/guides/seo)
- [Style and tone](https://www.mintlify.com/docs/guides/style-and-tone)
- [Understand your audience](https://www.mintlify.com/docs/guides/understand-your-audience)

##### Git

- [Git concepts for documentation](https://www.mintlify.com/docs/guides/git-concepts)
- [Work with branches](https://www.mintlify.com/docs/guides/branches)

##### Use cases

- [Developer documentation](https://www.mintlify.com/docs/guides/developer-documentation)
- [Knowledge base](https://www.mintlify.com/docs/guides/knowledge-base)
- [Support center](https://www.mintlify.com/docs/guides/support-center)

![US](https://d3gk2c5xim1je2.cloudfront.net/flags/US.svg)

English

Effective linking creates a connected documentation experience that helps users discover related content and navigate efficiently. Too many links or broken links can confuse users and make your documentation less effective. This guide covers how to create and maintain links throughout your documentation.

##

[​](#internal-links)

Internal links

Link to other pages in your documentation using root-relative paths. Root-relative paths start from the root of your documentation directory and work consistently regardless of where the linking page is located.
```
* [Quickstart guide](/quickstart)
* [API overview](/api-playground/overview)
* [Custom components](/customize/react-components)
```
- [Quickstart guide](https://www.mintlify.com/docs/quickstart)
- [API overview](https://www.mintlify.com/docs/api-playground/overview)
- [Custom components](https://www.mintlify.com/docs/customize/react-components)

##

[​](#anchor-links)

Anchor links

Anchor links allow you to link directly to specific sections within a page. Every header automatically generates an anchor link based on its text.

###

[​](#link-to-headers-on-the-same-page)

Link to headers on the same page

Reference headers on the current page using the hash symbol:
```
[Jump to best practices](#best-practices)
```
[Jump to best practices](#best-practices)

###

[​](#link-to-headers-on-other-pages)

Link to headers on other pages

Combine page paths with anchor links.
```
* [Customize your playground](/api-playground/overview#customize-your-playground)
* [Cards properties](/components/cards#properties)
```
- [Customize your playground](https://www.mintlify.com/docs/api-playground/overview#customize-your-playground)
- [Cards properties](https://www.mintlify.com/docs/components/cards#properties)

###

[​](#how-anchor-links-are-generated)

How anchor links are generated

Anchor links are automatically created from header text.

- Convert to lowercase
- Replace spaces with hyphens
- Remove special characters
- Preserve numbers and letters

| Header text | Anchor link |
| --- | --- |
| `## Getting Started` | `#getting-started` |
| `### API Authentication` | `#api-authentication` |
| `#### Step 1: Install` | `#step-1-install` |

Headers with the `noAnchor` prop will not generate anchor links. See [Format text](https://www.mintlify.com/docs/create/text#disabling-anchor-links) for details.

##

[​](#link-to-api-endpoints)

Link to API endpoints

When documenting APIs, you can link to specific endpoints from anywhere in your documentation. Link to API endpoint pages using their path in the navigation.

##

[​](#link-to-external-pages)

Link to external pages

When you link to external resources, make it clear the link goes outside your documentation.
```
Learn more about [Markdown syntax](https://www.markdownguide.org/) (external link).

See the [OpenAPI specification](https://swagger.io/specification/) in the Swagger documentation for details.
```

##

[​](#best-practices)

Best practices

###

[​](#write-descriptive-link-text)

Write descriptive link text

Use clear, descriptive text that indicates what users will find when they click.

Good examples

Avoid
```
See [Hidden pages](/organize/hidden-pages) for more information.
[Configure custom domains](/customize/custom-domain)
```

###

[​](#create-topic-clusters)

Create topic clusters

Link related content together to help users discover relevant information.
```

## Related topics

- [API authentication](/api-playground/overview#authentication)
- [Adding SDK examples](/api-playground/adding-sdk-examples)
- [Managing page visibility](/api-playground/managing-page-visibility)
```

###

[​](#use-contextual-links)

Use contextual links

Add links naturally within content where they provide value.
```
To customize your documentation appearance, configure [themes](/customize/themes)
and [fonts](/customize/fonts) in your settings. You can also add
[custom scripts](/customize/custom-scripts) for advanced functionality.
```

###

[​](#link-to-prerequisites)

Link to prerequisites

Help users prepare by linking to prerequisite content:
```

## Prerequisites

Before deploying your documentation, ensure you have:

- Completed the [quickstart guide](/quickstart)
- Configured your [custom domain](/customize/custom-domain)
- Set up [authentication](/deploy/authentication-setup) if needed
```

###

[​](#avoid-circular-links)

Avoid circular links

Do not create links that send users back and forth between the same pages.

###

[​](#check-for-broken-links)

Check for broken links

Use the Mintlify CLI to identify broken links in your documentation.
```
mint broken-links
```

###

[​](#update-links-when-reorganizing)

Update links when reorganizing

When moving or renaming pages:

1.  Update the page path in your navigation configuration.
2.  Configure redirects for the old path to the new path.
3.  Search your documentation for references to the old path.
4.  Update all internal links to use the new path.
5.  Run `mint broken-links` to verify all links work.

###

[​](#use-redirects-for-moved-content)

Use redirects for moved content

When permanently moving content, add redirects to prevent broken links.
```
{
  "redirects": [
    {
      "source": "/old-path",
      "destination": "/new-path"
    }
  ]
}
```
See [Redirects](https://www.mintlify.com/docs/create/redirects) for more information.

##

[​](#related-resources)

Related resources

- [Format text](https://www.mintlify.com/docs/create/text): Learn about Markdown formatting.
- [Navigation](https://www.mintlify.com/docs/organize/navigation): Configure your documentation structure.
- [Redirects](https://www.mintlify.com/docs/create/redirects): Set up redirects for moved content.

Was this page helpful?

YesNo

[InternationalizationPrevious](https://www.mintlify.com/docs/guides/internationalization)[MaintenanceNext](https://www.mintlify.com/docs/guides/maintenance)

⌘I
