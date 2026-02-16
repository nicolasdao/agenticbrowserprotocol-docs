---
url: https://mintlify.com/docs/ai/assistant
canonical: https://www.mintlify.com/docs/ai/assistant
title: "Assistant - Mintlify"
description: "Add AI-powered chat to your docs that answers questions, cites sources, and generates code examples."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Optimize

Assistant

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

The assistant is automatically enabled on [Pro and Enterprise plans](https://mintlify.com/pricing?ref=assistant).

##

[​](#about-the-assistant)

About the assistant

The assistant answers questions about your documentation through natural language queries. Users access the assistant on your documentation site, so they can find answers quickly and succeed with your product even if they don’t know where to look. The assistant uses agentic RAG (retrieval-augmented generation) with tool calling. When users ask questions, the assistant:

- **Searches and retrieves** relevant content from your documentation to provide accurate answers.
- **Cites sources** and provides navigable links to take users directly to referenced pages.
- **Generates copyable code examples** to help users implement solutions from your documentation.

You can view assistant usage through your dashboard to understand user behavior and documentation effectiveness. Export and analyze query data to help identify:

- Frequently asked questions that might need better coverage.
- Content gaps where users struggle to find answers.
- Popular topics that could benefit from additional content.

###

[​](#how-indexing-works)

How indexing works

The assistant automatically indexes your published documentation to answer questions accurately. When you publish changes, the assistant immediately indexes new, updated, or deleted content. The assistant does not index draft branches or preview deployments. By default, the assistant does not index hidden pages. To include hidden pages in the assistant’s index, set `seo.indexing: "all"` in your `docs.json`. See [Hidden pages](https://www.mintlify.com/docs/organize/hidden-pages#search-seo-and-ai-indexing) for more information.

###

[​](#how-the-assistant-handles-unknown-questions)

How the assistant handles unknown questions

The assistant only answers questions based on information in your documentation. If it cannot find relevant information after searching, it responds that it doesn’t have enough information to answer. You can [set a deflection email](https://www.mintlify.com/docs/ai/assistant#set-deflection-email) so that the assistant provides your support email to users whose questions it cannot answer. This gives users a path forward, even if the documentation doesn’t address their specific question.

##

[​](#configure-the-assistant)

Configure the assistant

The assistant is active on Pro and Enterprise plans by default. Manage the assistant from the [Assistant Configurations](https://dashboard.mintlify.com/products/assistant/settings) page of your dashboard. Enable or disable the assistant, configure response handling, add default questions, and manage your message allowance.

###

[​](#enable-or-disable-the-assistant)

Enable or disable the assistant

Toggle the assistant status to enable or disable the assistant for your documentation site.

![The assistant status toggle in the dashboard.](https://mintcdn.com/mintlify/qxFvxlkWYrjV0OaV/images/assistant/status-light.png?fit=max&auto=format&n=qxFvxlkWYrjV0OaV&q=85&s=723881f19ac3ad665a774eeb6f3b8652)![The assistant status toggle in the dashboard.](https://mintcdn.com/mintlify/qxFvxlkWYrjV0OaV/images/assistant/status-dark.png?fit=max&auto=format&n=qxFvxlkWYrjV0OaV&q=85&s=8c7ae23c57d3db8f67a649b0f09d45c4)

###

[​](#set-deflection-email)

Set deflection email

In the Response Handling section, enable the assistant to redirect unanswered questions to your support team. Specify an email address for the assistant to give to users if it cannot answer their question. You can also enable a “Contact support” button to appear in the assistant chat panel.

![The assistant deflection panel in the dashboard. Assistant deflection is toggled on and support@mintlify.com is set as the deflection email.](https://mintcdn.com/mintlify/RnZ31raTBKoRr5sX/images/assistant/deflection-light.png?fit=max&auto=format&n=RnZ31raTBKoRr5sX&q=85&s=d63b7b91381f5f2ca86790610fe4337b)![The assistant deflection panel in the dashboard. Assistant deflection is toggled on and support@mintlify.com is set as the deflection email.](https://mintcdn.com/mintlify/RnZ31raTBKoRr5sX/images/assistant/deflection-dark.png?fit=max&auto=format&n=RnZ31raTBKoRr5sX&q=85&s=f422e292dd30a1a3a488048ba176dddd)

###

[​](#search-domains)

Search domains

In the Response Handling section, configure domains that the assistant can use for web search to find additional context when answering questions.

- Domains must be publicly available.
- Domains that require JavaScript to load are not supported.

![The assistant search domains panel enabled in the dashboard. The assistant is configured to search the mintlify.com/pricing domain.](https://mintcdn.com/mintlify/2qBICQFhOKqkes42/images/assistant/search-domains-light.png?fit=max&auto=format&n=2qBICQFhOKqkes42&q=85&s=a15d483e0eee1b9a55a8ff6583a7d331)![The assistant search domains panel enabled in the dashboard. The assistant is configured to search the mintlify.com/pricing domain.](https://mintcdn.com/mintlify/2qBICQFhOKqkes42/images/assistant/search-domains-dark.png?fit=max&auto=format&n=2qBICQFhOKqkes42&q=85&s=ae032b581c467630c044b073b583dded)

For more precise control over what the assistant can search, use filtering syntax.

- **Domain-level filtering**
    -   `example.com`: Search only the `example.com` domain
    -   `docs.example.com`: Search only the `docs.example.com` subdomain
    -   `*.example.com`: Search all subdomains of `example.com`
- **Path-level filtering**
    -   `docs.example.com/api`: Search all pages under the `/api` subpath
- **Multiple patterns**
    -   Add multiple entries to target different sections of sites

###

[​](#add-sample-questions)

Add sample questions

Help your users begin conversations with the assistant by adding starter questions. Add commonly asked questions or questions about topics that you want your users to know about. Click **Ask AI** for recommended questions based on your documentation.

![The search suggestions panel in the dashboard with starter questions enabled and populated with three questions.](https://mintcdn.com/mintlify/2qBICQFhOKqkes42/images/assistant/search-suggestions-light.png?fit=max&auto=format&n=2qBICQFhOKqkes42&q=85&s=f2e40f177d289259f24644e5f1372a7d)![The search suggestions panel in the dashboard with starter questions enabled and populated with three questions.](https://mintcdn.com/mintlify/2qBICQFhOKqkes42/images/assistant/search-suggestions-dark.png?fit=max&auto=format&n=2qBICQFhOKqkes42&q=85&s=6a9bdfcc55dbe36c1fe30c877bcb414d)

##

[​](#manage-billing)

Manage billing

The assistant uses tiered message allowances. A message is any user interaction with the assistant that receives a correct response. If you have unused messages, up to half of your message allowance can carry over to the next billing cycle. For example, if you have a 1,000 message allowance and you use 300 messages, 500 messages carry over to the next billing cycle giving you a total of 1,500 messages for the next billing cycle. By default, the assistant allows overages. You can disable overages to avoid incurring additional costs for usage beyond your tier. If you reach your message allowance with overages disabled, the assistant is unavailable until your message allowance resets. If you allow overages, each message beyond your allowance incurs an overage charge, but occasional overages may be cheaper than upgrading to a higher tier depending on your usage.

###

[​](#change-your-assistant-tier)

Change your assistant tier

Assistant tiers determine your monthly message allowance and pricing. View and change your current tier on the [Billing tab](https://dashboard.mintlify.com/products/assistant/settings/billing) of the assistant page in your dashboard. In the **Spending Controls** section, select your preferred tier from the dropdown menu. **Upgrade your tier:**

- Your new message allowance is available immediately.
- You pay a prorated difference for the current billing cycle.

**Downgrade your tier:**

- Your message allowance updates immediately.
- Pricing changes take effect at the start of your next billing cycle.
- Unused messages from your current tier **do not** carry over.

###

[​](#allow-overages)

Allow overages

If you want to disallow overages, disable them in the **Billing Controls** section of the [Billing tab](https://dashboard.mintlify.com/products/assistant/settings/billing) of the assistant page in your dashboard.

###

[​](#set-usage-alerts)

Set usage alerts

In the Billing Controls section, set usage alerts to receive an email when you reach a certain percentage of your message allowance.

##

[​](#connect-apps)

Connect apps

In the connect apps section, add the assistant to your [Discord](https://www.mintlify.com/docs/ai/discord) server and [Slack](https://www.mintlify.com/docs/ai/slack-bot) workspace to allow users to get answers from your documentation on those platforms.

##

[​](#assistant-insights)

Assistant insights

Use assistant insights to understand how users interact with your documentation and identify improvement opportunities. The [assistant page](https://dashboard.mintlify.com/products/assistant) shows usage trends for the month to date. View more detailed insights on the [analytics](https://www.mintlify.com/docs/optimize/analytics#assistant) page.

##

[​](#make-content-ai-ingestible)

Make content AI ingestible

Structure your documentation to help the assistant provide accurate, relevant answers. Clear organization and comprehensive context benefit both human readers and AI understanding.

## Structure and organization

- Use semantic markup.
- Write descriptive headings for sections.
- Create a logical information hierarchy.
- Use consistent formatting across your docs.
- Include comprehensive metadata in page frontmatter.
- Break up long blocks of text into shorter paragraphs.

## Context

- Define specific terms and acronyms when first introduced.
- Provide sufficient conceptual content about features and procedures.
- Include examples and use cases.
- Cross-reference related topics.
- Add [hidden pages](https://www.mintlify.com/docs/organize/hidden-pages) with additional context that users don’t need, but the assistant can reference.

##

[​](#use-the-assistant)

Use the assistant

Users have multiple ways to start a conversation with the assistant. Each method opens a chat panel on the right side of your docs. Users can ask any question and the assistant searches your documentation for an answer. If the assistant cannot retrieve relevant information, the assistant responds that it cannot answer the question. Add the assistant as a bot to your [Slack workspace](https://www.mintlify.com/docs/ai/slack-bot) or [Discord server](https://www.mintlify.com/docs/ai/discord) so that your community can ask questions without leaving their preferred platform.

###

[​](#ui-placement)

UI placement

The assistant appears in two locations: as a button next to the search bar and as a bar at the bottom of the page.

![Search bar and assistant button in light mode.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/assistant/assistant-button-light.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=716582bc54eaea73cb53d26b36a74fb4)![Search bar and assistant button in dark mode.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/assistant/assistant-button-dark.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=34096a771f492853e59eef654567b081)

Assistant button next to the search bar.

![Assistant bar in light mode.](https://mintcdn.com/mintlify/Gt7y__uLw46fbQ_E/images/assistant/assistant-bar-light.png?fit=max&auto=format&n=Gt7y__uLw46fbQ_E&q=85&s=920b62e97a4a24a5aa7a29d9306b3762)![Assistant bar in dark mode.](https://mintcdn.com/mintlify/Gt7y__uLw46fbQ_E/images/assistant/assistant-bar-dark.png?fit=max&auto=format&n=Gt7y__uLw46fbQ_E&q=85&s=f597be3a1c8a95a8a72aaae4f799981f)

Assistant button at the bottom of the page.

###

[​](#keyboard-shortcut)

Keyboard shortcut

Open the assistant chat panel with the keyboard shortcut Command + I on macOS and Ctrl + I on Windows.

###

[​](#highlight-text)

Highlight text

Highlight text on a page and click the **Add to assistant** pop up button to open the assistant chat panel and add the highlighted text as context. You can add multiple text snippets or code blocks to the assistant’s context.

![The Add to assistant button above highlighted text in light mode.](https://mintcdn.com/mintlify/Gt7y__uLw46fbQ_E/images/assistant/highlight-light.png?fit=max&auto=format&n=Gt7y__uLw46fbQ_E&q=85&s=13c93b72e4f6b21800e31a55f85c3690)![The Add to assistant button above highlighted text in dark mode.](https://mintcdn.com/mintlify/Gt7y__uLw46fbQ_E/images/assistant/highlight-dark.png?fit=max&auto=format&n=Gt7y__uLw46fbQ_E&q=85&s=73ef7699810025a73fce4dc125fea683)

###

[​](#code-blocks)

Code blocks

Click the **Ask AI** button in a code block to open the assistant chat panel and add the code block as context. You can add multiple code blocks or text snippets to the assistant’s context.

![The Ask AI button in a code block in light mode.](https://mintcdn.com/mintlify/Gt7y__uLw46fbQ_E/images/assistant/code-block-light.png?fit=max&auto=format&n=Gt7y__uLw46fbQ_E&q=85&s=d9b3cbecca1416291915ded538315d05)![The Ask AI button in a code block in dark mode.](https://mintcdn.com/mintlify/Gt7y__uLw46fbQ_E/images/assistant/code-block-dark.png?fit=max&auto=format&n=Gt7y__uLw46fbQ_E&q=85&s=1e5ffae5032208ff67d2a725b48fdafd)

###

[​](#urls)

URLs

Open the assistant with a URL query parameter to create deep links that guide users to specific information or share assistant conversations with pre-filled questions.

- **Open the assistant**: Append `?assistant=open` to open the assistant chat panel when the page loads.
    -   Example: [https://mintlify.com/docs?assistant=open](https://mintlify.com/docs?assistant=open)
- **Open with a pre-filled query**: Append `?assistant=YOUR_QUERY` to open the assistant and automatically submit a question.
    -   Example: [https://mintlify.com/docs?assistant=explain webhooks](https://mintlify.com/docs?assistant=explain%20webhooks)

##

[​](#troubleshooting)

Troubleshooting

Assistant chat bar not visible

If the assistant UI is not visible in specific browsers, you may need to submit a false positive report to [EasyList](https://easylist.to). Browsers that use the EasyList Cookies List like Brave and Comet sometimes block the assistant or other UI elements. The EasyList Cookies List includes a domain-specific rule that hides fixed elements on certain domains to block cookie banners. This rule inadvertently affects legitimate UI components.Submit a false positive report to [EasyList](https://github.com/easylist/easylist) to request removal of the rule. This resolves the issue for all users once the filter list updates.

Was this page helpful?

YesNo

[GitLabPrevious](https://www.mintlify.com/docs/deploy/gitlab)[Discord botNext](https://www.mintlify.com/docs/ai/discord)

⌘I

![The assistant status toggle in the dashboard.](https://mintcdn.com/mintlify/qxFvxlkWYrjV0OaV/images/assistant/status-dark.png?w=1650&fit=max&auto=format&n=qxFvxlkWYrjV0OaV&q=85&s=161b1e9ac9cbf2c1b678fa59240d99cb)

![The assistant deflection panel in the dashboard. Assistant deflection is toggled on and support@mintlify.com is set as the deflection email.](https://mintcdn.com/mintlify/RnZ31raTBKoRr5sX/images/assistant/deflection-dark.png?w=1650&fit=max&auto=format&n=RnZ31raTBKoRr5sX&q=85&s=8649f39ec8f1332565c4dc650ebe805d)

![The assistant search domains panel enabled in the dashboard. The assistant is configured to search the mintlify.com/pricing domain.](https://mintcdn.com/mintlify/2qBICQFhOKqkes42/images/assistant/search-domains-dark.png?w=1650&fit=max&auto=format&n=2qBICQFhOKqkes42&q=85&s=1a6a7c6ce03629355444678429d355ed)

![The search suggestions panel in the dashboard with starter questions enabled and populated with three questions.](https://mintcdn.com/mintlify/2qBICQFhOKqkes42/images/assistant/search-suggestions-dark.png?w=1650&fit=max&auto=format&n=2qBICQFhOKqkes42&q=85&s=69e0804fe76e88d7edb0182b052b29da)

![Search bar and assistant button in dark mode.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/assistant/assistant-button-dark.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=0c15a237b868f23fad34f7838bdc3579)

![Assistant bar in dark mode.](https://mintcdn.com/mintlify/Gt7y__uLw46fbQ_E/images/assistant/assistant-bar-dark.png?w=1650&fit=max&auto=format&n=Gt7y__uLw46fbQ_E&q=85&s=cdaa4b744b73ac71837bc70ef9f0a08e)

![The Add to assistant button above highlighted text in dark mode.](https://mintcdn.com/mintlify/Gt7y__uLw46fbQ_E/images/assistant/highlight-dark.png?w=1650&fit=max&auto=format&n=Gt7y__uLw46fbQ_E&q=85&s=5aed16d9f8682b297610e4510486fa2a)

![The Ask AI button in a code block in dark mode.](https://mintcdn.com/mintlify/Gt7y__uLw46fbQ_E/images/assistant/code-block-dark.png?w=1650&fit=max&auto=format&n=Gt7y__uLw46fbQ_E&q=85&s=507ea9c7461f37d047d4b12cb18d7df2)
