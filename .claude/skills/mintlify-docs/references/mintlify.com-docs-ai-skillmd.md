---
url: https://mintlify.com/docs/ai/skillmd
canonical: https://www.mintlify.com/docs/ai/skillmd
title: "skill.md - Mintlify"
description: "Make your docs agent-ready with a structured capability file."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Optimize

skill.md

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

Mintlify hosts a `skill.md` file at the root of your project that describes what AI agents can do with your product. The [skill.md specification](https://agentskills.io/specification) is a structured, machine-readable format that makes capabilities, required inputs, and constraints for products explicit so that agents can use them more reliably. Mintlify automatically generates a `skill.md` file for your project by analyzing your documentation with an agentic loop. This file stays up to date as you make updates to your documentation and requires no maintenance. You can optionally add a custom `skill.md` file to the root of your project that overrides the automatically generated one. View your `skill.md` by appending `/skill.md` to your documentation site’s URL. Mintlify only generates `skill.md` files for documentation sites that are public.

Both `llms.txt` and `skill.md` files help agents work with your documentation, but they serve different purposes.

- `llms.txt` is a directory. It lists all your documentation pages with descriptions so agents know where to find information.
- `skill.md` is a capability summary. It tells agents what they can accomplish with your product, what inputs they need, and what constraints apply.

##

[​](#use-skill-md-files-with-agents)

Use `skill.md` files with agents

If you use a [reverse proxy](https://www.mintlify.com/docs/deploy/reverse-proxy), configure it to forward `/skill.md` and `/.well-known/skills/*` paths (with caching disabled) to your Mintlify subdomain.

Agents can process your `skill.md` with the [skills CLI](https://www.npmjs.com/package/skills).
```
npx skills add https://your-docs-domain.com
```
This adds your product’s capabilities to the agent’s context so it can take actions on behalf of users.

Teach your users how to use `skill.md` files with agents so that they have better results using your product with their AI tools.

##

[​](#skill-md-structure)

`skill.md` structure

Mintlify generates a `skill.md` file following the [agentskills.io specification](https://agentskills.io/specification). The generated file includes:

- **Metadata**: Project name, description, and version.
- **Capabilities**: What agents can accomplish with your product.
- **Skills**: Specific actions organized by category.
- **Workflows**: Step-by-step procedures for common tasks.
- **Integration**: Supported tools and services.
- **Context**: Background on your product’s architecture.

##

[​](#custom-skill-md-files)

Custom `skill.md` files

Add a `skill.md` file to the root of your project to override the automatically generated file. If you delete a custom file, Mintlify generates a new `skill.md` file. Write a custom file when you want precise control over how agents interact with your product. Follow the [agentskills.io specification](https://agentskills.io/specification) to ensure compatibility with agent tooling.

###

[​](#frontmatter-fields)

Frontmatter fields

Custom `skill.md` files must start with YAML frontmatter.

| Field | Type | Description |
| --- | --- | --- |
| `name` | string | The name of your skill. |
| `description` | string | A brief description of what your skill does. |
| `license` | string | The license for your skill (for example, `MIT` or `Apache-2.0`). |
| `compatibility` | string | Requirements or compatibility notes (for example, runtime dependencies). |
| `metadata` | object | Additional metadata as string key-value pairs (for example, `author` or `version`). |
| `allowed-tools` | string | Space-delimited list of pre-approved tools the skill may use (experimental). |

Example frontmatter
```
---
name: mintlify
description: Build and maintain documentation sites with Mintlify. Use when creating docs pages, configuring navigation, adding components, or setting up API references.
license: MIT
compatibility: Requires Node.js for CLI. Works with any Git-based workflow.
metadata:
  author: mintlify
  version: "1.0"
---
```
Was this page helpful?

YesNo

[llms.txtPrevious](https://www.mintlify.com/docs/ai/llmstxt)[Model Context ProtocolNext](https://www.mintlify.com/docs/ai/model-context-protocol)

⌘I
