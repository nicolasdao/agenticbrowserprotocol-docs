---
url: https://mintlify.com/docs/agent/slack
canonical: https://www.mintlify.com/docs/agent/slack
title: "Add the agent to Slack - Mintlify"
description: "Use the agent in Slack to make documentation updates from conversations and capture team knowledge."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Agent

Add the agent to Slack

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

If your Slack Workspace Owner requires admin approval to install apps, ask them to approve the Mintlify app before you connect it.

##

[​](#connect-your-slack-workspace)

Connect your Slack workspace

1.  Open the agent panel in your dashboard.
2.  Click the **Settings** button.

    ![The settings button in light mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-settings-light.png?fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=ecb555eecfddf7480baaaf7d2fd6bce9)![The settings button in dark mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-settings-dark.png?fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=a3250fa23cac19e8914b7185ac24c6d0)

3.  In the Slack integration section, click **Connect**.
4.  Follow the Slack prompts to add the `mintlify` app to your workspace.
5.  Follow the Slack prompts to link your Mintlify account to your Slack workspace.
6.  Test that the agent is working and responds when you:
    -   Send a direct message to it.
    -   Mention it with `@mintlify` in a channel.

##

[​](#use-the-agent-in-slack)

Use the agent in Slack

Once connected, you can:

- Send direct messages to the agent to use it privately to update your documentation.
- Mention `@mintlify` in a channel to use it publicly and collaboratively.
- Continue conversations in threads to iterate on changes.
- Share pull request links with the agent to update related documentation.

##

[​](#update-documentation)

Update documentation

Use the agent to update your documentation with a new request or in an existing thread.

- **New request**: Send a direct message to the agent or mention `@mintlify` in a channel with instructions on what to update.
- **Existing thread**: Reply in the thread and mention `@mintlify` with instructions on what to update.

The agent reads the context of the request or thread and creates a pull request in your connected repository with the updates.

##

[​](#best-practices)

Best practices

- **Be specific**: Tell the agent exactly what you want documented and where it should go.
- **Add context**: If a thread doesn’t contain all the necessary information, include additional details in your message to the agent.
- **Review carefully**: You should always review pull requests that the agent creates before merging them.

Was this page helpful?

YesNo

[QuickstartPrevious](https://www.mintlify.com/docs/agent/quickstart)[Agent suggestionsNext](https://www.mintlify.com/docs/agent/suggestions)

⌘I

![The settings button in dark mode.](https://mintcdn.com/mintlify/l1-TgESjTbrqcwOU/images/agent/dashboard-settings-dark.png?w=1650&fit=max&auto=format&n=l1-TgESjTbrqcwOU&q=85&s=c1d8e1cd78e6a494852b809cbeb1a695)
