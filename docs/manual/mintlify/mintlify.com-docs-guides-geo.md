---
url: https://mintlify.com/docs/guides/geo
canonical: https://www.mintlify.com/docs/guides/geo
title: "GEO guide: Optimize docs for AI search and answer engines - Mintlify"
description: "Optimize your documentation for AI search and answer engines."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

AI

GEO guide: Optimize docs for AI search and answer engines

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

Optimize your documentation for both traditional search engines and AI-powered answer engines like ChatGPT, Perplexity, and Google AI Overviews. Generative Engine Optimization (GEO) focuses on being cited by AI systems through comprehensive content and structured information, while traditional SEO targets search result rankings.

##

[​](#geo-quickstart)

GEO quickstart

###

[​](#initial-setup)

Initial setup

1.  **Make sure your docs are being indexed** in your `docs.json` settings
2.  **Audit current pages** for missing descriptions and titles

###

[​](#content-improvements)

Content improvements

1.  **Add comparison tables** to appropriate pages
2.  **Audit headings** to ensure they answer common questions
3.  **Improve internal linking** between related topics
4.  **Test with AI tools** to verify accuracy

##

[​](#geo-best-practices)

GEO best practices

In general, well written and well structured documentation will have strong GEO. You should still prioritize writing for your users, and if your content is meeting their needs, you will be well on your way to optimizing for AI tools. Creating genuinely helpful content rather than optimizing for optimization’s sake is rewarded by both traditional and AI search engines. Focus on:

- Content aligned to user needs rather than keyword matching
- Structured, scannable information
- Direct answers to questions

###

[​](#format-for-clarity)

Format for clarity

These formatting practices help AI tools parse and understand your content:

- Don’t skip heading levels (H1 → H2 → H3)
- Use specific object names instead of “it” or “this”
- Label code blocks with their programming language
- Give images descriptive alt text
- Link to related concepts to help AI understand relationships

###

[​](#answer-questions-directly)

Answer questions directly

Write content that addresses specific user questions:

- Begin sections with the main takeaway
- Use descriptive headings that match common queries
- Break complex topics into numbered steps

##

[​](#mintlify-configuration)

Mintlify configuration

Use these features to improve GEO.

###

[​](#add-descriptive-page-metadata)

Add descriptive page metadata

Include clear titles and descriptions in your frontmatter:
```
---
title: "API authentication guide"
description: "Complete guide to implementing API authentication with code examples"
---
```

###

[​](#configure-global-indexing-settings)

Configure global indexing settings

Add to your `docs.json`:
```
{
  "seo": {
    "indexing": "all",
    "metatags": {
      "og:type": "website",
      "og:site_name": "Your docs"
    }
  }
}
```

###

[​](#llms-txt)

LLMs.txt

LLMs.txt files help AI systems understand your documentation structure, similar to how sitemaps help search engines. Mintlify automatically generates LLMs.txt files for your docs. No configuration is required.

##

[​](#testing-your-documentation)

Testing your documentation

Test various AI tools with questions about your product and documentation to see how well your docs are being cited. **Ask AI assistants specific questions about your docs:**

- “How do I set up authentication using this API?”
- “Walk me through the installation process step by step”

**Check that tools provide:**

- Correct code samples
- Accurate step-by-step instructions

Was this page helpful?

YesNo

[CursorPrevious](https://www.mintlify.com/docs/guides/cursor)[WindsurfNext](https://www.mintlify.com/docs/guides/windsurf)

⌘I
