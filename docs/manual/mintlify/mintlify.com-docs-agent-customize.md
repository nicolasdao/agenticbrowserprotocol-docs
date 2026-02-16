---
url: https://mintlify.com/docs/agent/customize
canonical: https://www.mintlify.com/docs/agent/customize
title: "Customize agent behavior - Mintlify"
description: "Configure how the agent handles documentation tasks with AGENTS.md."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Agent

Customize agent behavior

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

    -   [What is the agent?](https://www.mintlify.com/docs/agent)
    -   [Quickstart](https://www.mintlify.com/docs/agent/quickstart)
    -   [Add the agent to Slack](https://www.mintlify.com/docs/agent/slack)
    -   [Agent suggestions](https://www.mintlify.com/docs/agent/suggestions)
    -   [Customize agent behavior](https://www.mintlify.com/docs/agent/customize)
    -   [Write effective prompts](https://www.mintlify.com/docs/agent/effective-prompts)
    -   [Workflows](https://www.mintlify.com/docs/agent/workflows)
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

Create an `AGENTS.md` file in your repository to customize the agent’s behavior (`Agents.md` is also accepted). The agent reads this file and follows any instructions you provide. The agent searches for `AGENTS.md` files in two locations. It first checks the documentation directory, then the repository root. If you have `AGENTS.md` files in both locations, the agent uses the file in your documentation directory. Add any instructions that you want the agent to follow. The agent appends these instructions to its system prompt, so the instructions apply to all tasks, whether you use the agent in your dashboard, on Slack, or via the API.

##

[​](#what-to-include-in-agents-md)

What to include in AGENTS.md

Consider adding instructions for:

- **Style preferences**: Voice, tone, formatting, and terminology specific to your documentation.
- **Code standards**: Programming languages, frameworks, and coding conventions to use in examples.
- **Content requirements**: What sections or information to include for different types of pages.
- **Project context**: Specific details about your product, architecture, or user base that inform documentation decisions.

##

[​](#example-agents-md-file)

Example AGENTS.md file

AGENTS.md
```

# Documentation agent instructions

## Code examples
- Use TypeScript for all code examples. Our users are primarily TypeScript developers.
- Always include error handling in API call examples.
- Show both success and error response examples for all endpoints.
- Include import statements at the top of code examples.

## API documentation standards
- Every endpoint must document: authentication requirements, rate limits, and common error codes.
- Use real-world parameter values in examples (not foo/bar placeholders).
- Include a complete request/response cycle for each endpoint.

## Style and formatting
- Write for developers with 2-5 years of experience. Don't oversimplify, but explain non-obvious concepts.
- Use active voice and second person ("you").
- Date format: ISO 8601 (YYYY-MM-DD).
- When referencing UI elements, use bold: **Settings** button.

## What to include
- Add prerequisite sections to guides when users need API keys, environment setup, or dependencies.
- Include "Next steps" sections linking to related documentation.
- Add troubleshooting sections for common issues we see in support tickets.
```
Was this page helpful?

YesNo

[Agent suggestionsPrevious](https://www.mintlify.com/docs/agent/suggestions)[Write effective promptsNext](https://www.mintlify.com/docs/agent/effective-prompts)

⌘I
