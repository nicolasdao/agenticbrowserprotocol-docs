---
url: https://mintlify.com/docs/ai/slack-bot
canonical: https://www.mintlify.com/docs/ai/slack-bot
title: "Slack bot - Mintlify"
description: "Add a bot to your Slack workspace that answers questions based on your documentation."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Optimize

Slack bot

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

The Slack app is available for [Pro and Custom plans](https://mintlify.com/pricing?ref=slack-app) with access to the assistant.

The Slack app adds a bot to your workspace that supports your community with real-time answers. The bot uses the Mintlify assistant to search your docs and provide accurate, cited responses, so it is always up-to-date. The bot can only see messages in channels you specifically add it to. It does not have global read access to your workspace. The bot responds to `@` mentions or to all messages in a specific channel that you configure. Each message sent by the bot counts toward your assistant message usage.

##

[​](#set-up-the-slack-app)

Set up the Slack app

You can only install the Slack app once per workspace. If you have multiple Mintlify deployments, you can only connect one deployment at a time to a workspace. You must disconnect the app from one deployment before connecting it to another.

If your Slack Workspace Owner requires admin approval to install apps, ask them to approve the Mintlify Slack app before you add it.

1.  Navigate to the [Assistant](https://dashboard.mintlify.com/products/assistant) page in your dashboard.
2.  In the Slack card, click **Configure**. This opens Slack.

    ![The connected apps section of the assistant page.](https://mintcdn.com/mintlify/iWC1DRgIiF7skzGL/images/assistant/connected-apps-light.png?fit=max&auto=format&n=iWC1DRgIiF7skzGL&q=85&s=647b6ec148afcbb3177e536cba7f858e)![The connected apps section of the assistant page.](https://mintcdn.com/mintlify/iWC1DRgIiF7skzGL/images/assistant/connected-apps-dark.png?fit=max&auto=format&n=iWC1DRgIiF7skzGL&q=85&s=cc2ef191b665b1042d1130d28b9346f2)

3.  Follow the Slack prompts to add the app to your workspace.
4.  Mention the bot to add it to a channel. The bot’s default name is `@mintlify-assistant`.

##

[​](#create-an-#ask-ai-channel)

Create an `#ask-ai` channel

To help your users quickly get answers to their questions, the bot can reply to every message in a channel that you choose. By default, the bot replies to every message in channels named `#ask-ai`. Create an `#ask-ai` channel and let your users know that the bot replies to messages in that channel. See [Create a channel](https://slack.com/help/articles/201402297-Create-a-channel) in the Slack Help Center for more information. If you want the bot to reply to messages in a different channel, select a channel in the Slack bot [configuration menu](https://dashboard.mintlify.com/products/assistant/settings/integrations).

![The Slack configuration panel in light mode.](https://mintcdn.com/mintlify/Cua8vliIsZB_FwDG/images/assistant/slack-configure-light.png?fit=max&auto=format&n=Cua8vliIsZB_FwDG&q=85&s=52112c0ed2e0d0767ef9ce9529e31b5b)![The Slack configuration panel in dark mode.](https://mintcdn.com/mintlify/Cua8vliIsZB_FwDG/images/assistant/slack-configure-dark.png?fit=max&auto=format&n=Cua8vliIsZB_FwDG&q=85&s=ac31230309042ad15238b57518038bf9)

##

[​](#manage-the-slack-app)

Manage the Slack app

After you add the app to your workspace, you can manage or remove the app from the [Integrations](https://dashboard.mintlify.com/products/assistant/settings/integrations) tab. In the Slack bot configuration menu, customize the bot by changing its avatar or name, and choose which channel it automatically replies to all messages in.

Was this page helpful?

YesNo

[Discord botPrevious](https://www.mintlify.com/docs/ai/discord)[Contextual menuNext](https://www.mintlify.com/docs/ai/contextual-menu)

⌘I

![The connected apps section of the assistant page.](https://mintcdn.com/mintlify/iWC1DRgIiF7skzGL/images/assistant/connected-apps-dark.png?w=1650&fit=max&auto=format&n=iWC1DRgIiF7skzGL&q=85&s=7faabc681aefdb7d0a3f72cdf11fc9cc)

![The Slack configuration panel in dark mode.](https://mintcdn.com/mintlify/Cua8vliIsZB_FwDG/images/assistant/slack-configure-dark.png?w=1650&fit=max&auto=format&n=Cua8vliIsZB_FwDG&q=85&s=41b01ef125a4f9d14c4b6854b5007810)
