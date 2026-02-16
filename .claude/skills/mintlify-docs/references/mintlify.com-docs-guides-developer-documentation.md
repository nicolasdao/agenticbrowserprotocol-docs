---
url: https://mintlify.com/docs/guides/developer-documentation
canonical: https://www.mintlify.com/docs/guides/developer-documentation
title: "Create developer documentation - Mintlify"
description: "Build documentation that helps developers integrate with your APIs, SDKs, and tools."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Use cases

Create developer documentation

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

Developer documentation helps people understand and integrate with your product. Good documentation helps people do more with your product, reduces support burden, speeds up adoption, and improves developer experience. Mintlify provides infrastructure built for developer documentation.

- **API reference generation**: Generate interactive [API references](https://www.mintlify.com/docs/api-playground/overview) from OpenAPI specifications that let developers test endpoints in your documentation.
- **Code blocks with explanations**: The [assistant](https://www.mintlify.com/docs/ai/assistant) explains code examples in context, helping developers understand implementation details.
- **Git sync**: Keep documentation in sync with your codebase using [GitHub](https://www.mintlify.com/docs/deploy/github) or [GitLab](https://www.mintlify.com/docs/deploy/gitlab).
- **Versioning**: Maintain documentation for multiple [versions](https://www.mintlify.com/docs/organize/navigation#versions) so developers on older versions can still find accurate information.

##

[​](#prerequisites)

Prerequisites

If you haven’t created a Mintlify project yet, see the [Quickstart](https://www.mintlify.com/docs/quickstart) to deploy your site.

- Your API specification in OpenAPI format (if documenting an API)
- A Git repository for your documentation
- Admin access to your Mintlify organization

##

[​](#migrate-existing-documentation)

Migrate existing documentation

If you’re creating documentation from scratch, skip to [Plan your documentation structure](#plan-your-documentation-structure).

###

[​](#audit-existing-content)

Audit existing content

Review your current documentation to understand what you have and what you need to migrate.

- **API reference**: Is it generated from a spec or hand-written? What endpoints do you document?
- **Guides and tutorials**: What integration guides exist? Are they current?
- **Code examples**: What languages and frameworks do you use?
- **SDK documentation**: Do you have separate documentation for each SDK?
- **Changelog**: Do you maintain a changelog or release notes?
- **Metadata**: Do you have metadata for your content like dates, authors, and tags?

###

[​](#export-your-existing-content)

Export your existing content

- Export to **Markdown** for the simplest migration to Mintlify.
- Export **OpenAPI specs** for API reference content.
- Export to **HTML** if Markdown isn’t available, then convert to Markdown.

##

[​](#plan-your-documentation-structure)

Plan your documentation structure

Developer documentation typically includes several content types. Structure your navigation around how your users understand your product.

docs.json example
```
{
  "navigation": {
    "groups": [
      {
        "group": "Get Started",
        "pages": [
          "introduction",
          "quickstart",
          "authentication"
        ]
      },
      {
        "group": "Guides",
        "pages": [
          "guides/webhooks",
          "guides/error-handling",
          "guides/rate-limits",
          "guides/pagination"
        ]
      },
      {
        "group": "API Reference",
        "pages": [
          "api-reference/overview",
          "api-reference/users",
          "api-reference/orders",
          "api-reference/products"
        ]
      },
      {
        "group": "SDKs",
        "pages": [
          "sdks/javascript",
          "sdks/python",
          "sdks/go"
        ]
      }
    ]
  }
}
```
See [Navigation](https://www.mintlify.com/docs/organize/navigation) for more configuration options.

##

[​](#set-up-your-api-reference)

Set up your API reference

If you have an API, generate an interactive reference from your OpenAPI specification.

1

[](#)

Add your OpenAPI spec

Add your OpenAPI specification file to your project. You can use YAML or JSON format.
```
your-project/
├── docs.json
├── openapi.yaml
└── api-reference/
    └── overview.mdx
```
2

[](#)

Configure the spec in docs.json

Reference your OpenAPI file in your `docs.json` configuration.

Configuration example
```
{
  "openapi": "openapi.yaml"
}
```
3

[](#)

Add endpoints to navigation

Add the endpoints to your `docs.json` navigation. See [OpenAPI setup](https://www.mintlify.com/docs/api-playground/openapi-setup) for configuration options.

Navigation example
```
{
  "group": "API Reference",
  "pages": [
    "api-reference/overview",
    "api-reference/users/list-users",
    "api-reference/users/get-user",
    "api-reference/users/create-user"
  ]
}
```

##

[​](#set-up-the-assistant)

Set up the assistant

The assistant helps developers find answers and understand code examples. Configure it from your [dashboard](https://dashboard.mintlify.com/products/assistant/settings).

- **Sample questions**: Add developer-focused questions like “How do I authenticate API requests?” or “Show me how to handle webhooks.”
- **Code explanations**: The assistant can explain code blocks in context when developers ask questions about specific examples.

##

[​](#set-up-versioning)

Set up versioning

If you maintain multiple API versions, configure versioning so developers find documentation for their version.

Versioning example
```
{
  "versions": ["v2", "v1"],
  "navigation": {
    "groups": [
      {
        "group": "API Reference",
        "version": "v2",
        "pages": ["v2/api-reference/users"]
      },
      {
        "group": "API Reference",
        "version": "v1",
        "pages": ["v1/api-reference/users"]
      }
    ]
  }
}
```
See [Versions](https://www.mintlify.com/docs/organize/navigation#versions) for more information.

##

[​](#connect-to-your-repository)

Connect to your repository

Install the Mintlify [GitHub App](https://www.mintlify.com/docs/deploy/github) to keep documentation in sync with your codebase and enable contributions.

1

[](#)

Connect your repository

Link your GitHub repository in the [dashboard](https://dashboard.mintlify.com). This enables automatic deployments when you push changes.

2

[](#)

Configure branch settings

Set your production branch and enable preview deployments for pull requests. This lets you review documentation changes before they go live.

If you use GitLab, see [GitLab](https://www.mintlify.com/docs/deploy/gitlab) for configuration instructions.

##

[​](#maintain-your-documentation)

Maintain your documentation

Developer documentation needs regular updates so that information is accurate and usable.

1

[](#)

Keep the API reference current

Update your OpenAPI specification whenever you release changes. If your specification is generated from code, automate this in your release process.

2

[](#)

Update code examples

Review code examples when you release new SDK versions or product updates. Outdated examples cause integration failures and support requests.

3

[](#)

Maintain a changelog

Document breaking changes, new features, and deprecations. Developers rely on changelogs to understand what changed between versions. See [Changelogs](https://www.mintlify.com/docs/create/changelogs) for more information.

4

[](#)

Monitor feedback

Review assistant conversations and search analytics to identify gaps in your documentation. If developers repeatedly ask about the same topic, improve that section. See [Maintenance](https://www.mintlify.com/docs/guides/maintenance) for more information.

##

[​](#next-steps)

Next steps

Your developer documentation is ready to launch. After deploying:

1.  Announce the documentation to your developer community.
2.  Monitor search patterns and assistant conversations for gaps.
3.  Set up a process to update docs with each API release.
4.  Gather feedback from developers to improve content over time.

Was this page helpful?

YesNo

[Work with branchesPrevious](https://www.mintlify.com/docs/guides/branches)[Create a knowledge baseNext](https://www.mintlify.com/docs/guides/knowledge-base)

⌘I
