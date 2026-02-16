---
url: https://mintlify.com/docs/guides/knowledge-base
canonical: https://www.mintlify.com/docs/guides/knowledge-base
title: "Create a knowledge base - Mintlify"
description: "Host your internal knowledge base on Mintlify to consolidate information for your team, improve search, and reduce maintenance burden."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Use cases

Create a knowledge base

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

An internal knowledge base helps your team find answers and maintain a source of truth. If your team has information spread across different channels and platforms, people might find inaccurate or no information when they search for answers. A centralized knowledge base solves this by putting answers where everyone can find them and giving your team a specific place to record shared knowledge. Mintlify provides the infrastructure for knowledge bases that your entire team can contribute to.

- **AI-powered search**: The [assistant](https://www.mintlify.com/docs/ai/assistant) answers questions using your knowledge base content, so people find answers without knowing exactly where to look.
- **Slack integrations**: Add the assistant to [Slack](https://www.mintlify.com/docs/ai/slack-bot) so your team can ask questions and use the [agent](https://www.mintlify.com/docs/agent/slack) to capture knowledge from conversations.
- **Low-barrier contributions**: The [web editor](https://www.mintlify.com/docs/editor) and [agent](https://www.mintlify.com/docs/agent/quickstart) let anyone on your team update content without learning Git or Markdown.
- **Authentication built-in**: Control access with [SSO or OAuth](https://www.mintlify.com/docs/deploy/authentication-setup), and use [groups](https://www.mintlify.com/docs/deploy/authentication-setup#control-access-with-groups) to show different content to different teams.

##

[​](#prerequisites)

Prerequisites

If you haven’t created a Mintlify project yet, see the [Quickstart](https://www.mintlify.com/docs/quickstart) to deploy your site.

- An authentication system (SSO or OAuth provider like Okta or Azure AD)
- Control over your domain for hosting
- Admin access to your Mintlify organization

##

[​](#migrate-existing-content)

Migrate existing content

If you’re creating a knowledge base from scratch, skip to [Design the navigation structure](#design-the-navigation-structure).

###

[​](#audit-existing-content)

Audit existing content

Catalog the content you currently have in your existing knowledge base. This helps you understand what content you need to migrate, plan how to organize it in your new knowledge base, identify any gaps in your content, and confirm that you moved all of your content to your new knowledge base.

- **Total number of articles**: Helps estimate migration effort and track completeness.
- **Topics and content**: Informs your navigation structure and content organization.
- **Current organization**: See how your content is currently organized and whether it matches your desired structure.
- **Content types**: Determine any content conversion requirements for text, PDFs, videos, and embedded content.
- **Metadata**: Identify any metadata to preserve like dates, authors, and tags.
- **Access requirements**: Determine the best authentication approach for your knowledge base.

###

[​](#export-your-existing-content)

Export your existing content

Most knowledge base platforms support exporting content in standard formats. The format you choose depends on your current platform and your priorities.

- Export to **Markdown** for the simplest migration to Mintlify. (recommended)
- Export to **HTML** if Markdown isn’t available. You must convert your content to Markdown later.
- Export to **JSON or CSV** if you have structured metadata to preserve.

##

[​](#design-the-navigation-structure)

Design the navigation structure

Your navigation structure determines how people find content in your knowledge base. You can recreate your existing structure or redesign it to better match how your team thinks about the content.

Migrating is a good time to improve your structure. Consider whether your current organization actually works for your team, or if you can reorganize to make information easier to find.

Your `docs.json` file defines the navigation structure of your knowledge base. Create this file at the root of your project repository.
```
{
  "navigation": {
    "groups": [
      {
        "group": "Finance",
        "pages": [
            "finance/overview",
            "finance/budgeting-process",
            "finance/expense-reports",
            "finance/cost-allocation"
        ]
      },
      {
        "group": "HR",
        "pages": [
            "hr/overview",
            "hr/onboarding",
            "hr/benefits",
            "hr/time-off-policy"
        ]
      },
      {
        "group": "Engineering",
        "pages": [
          "engineering/overview",
          "engineering/dev-setup",
          "engineering/deployment",
          "engineering/code-standards"
        ]
      }
    ]
  }
}
```
See [Navigation](https://www.mintlify.com/docs/organize/navigation) for more information on how to structure your knowledge base.

##

[​](#set-up-authentication)

Set up authentication

Determine who needs access to what content in your knowledge base. If everyone should have access to the entire knowledge base, set up only [authentication](https://www.mintlify.com/docs/deploy/authentication-setup). If you need to restrict access to certain content to specific users or groups, set up authentication with [group-based access control](https://www.mintlify.com/docs/deploy/authentication-setup#control-access-with-groups).

##

[​](#migrate-your-content)

Migrate your content

Move your exported content into a folder structure that matches the navigation structure you designed. Convert content to Markdown if needed, add any missing frontmatter, and set up internal links.

1

[](#)

Organize files

Create folders that match your `docs.json` structure. For example, if your `docs.json` has a Finance group, create a `finance/` folder:
```
your-project/
├── docs.json
├── finance/
│   ├── overview.mdx
│   ├── budgeting-process.mdx
│   ├── expense-reports.mdx
│   └── cost-allocation.mdx
├── hr/
│   ├── overview.mdx
│   ├── onboarding.mdx
│   ├── benefits.mdx
│   └── time-off-policy.mdx
└── engineering/
    ├── overview.mdx
    ├── dev-setup.mdx
    ├── deployment.mdx
    └── code-standards.mdx
```
Place each article in its corresponding folder. The file path must match the path in your `docs.json`. For example, if `docs.json` references `"finance/expense-reports"`, the file should be `finance/expense-reports.mdx` in your project repository.

2

[](#)

Add frontmatter to each article

Every `.mdx` file needs frontmatter at the top with metadata. Every page requires a title and description. See [Pages](https://www.mintlify.com/docs/organize/pages) for more information on page metadata.
```
---
title: "Expense Report Process"
description: "How to submit and track expense reports"
---

Your content here...
```
3

[](#)

Set up internal links

Link between pages using paths from your project root.
```
See [Onboarding Guide](/hr/onboarding) for new employee setup.

For questions, contact [HR Benefits Team](/hr/benefits#common-questions).
```
4

[](#)

Convert HTML and other formats to Markdown

If you exported your content as HTML, convert it to Markdown. Some tools that can help include:

- **Pandoc**: Command-line tool that converts between many formats.
- **CloudConvert**: Online converter supporting HTML, DOCX, PDF, and more.
- **VS Code extensions**: Search for “HTML to Markdown” in extensions.

5

[](#)

Handle multiple content formats

If you have PDFs, videos, or other media, decide how to include them in your knowledge base.

- **Embed videos**: Embed videos or link to hosted videos.
- **Link to PDFs**: Add PDFs to your project repository and link to them from relevant pages.
- **Convert PDFs to Markdown**: If you want the content of a PDF to be a page, convert PDFs to Markdown.

##

[​](#set-up-the-assistant)

Set up the assistant

The assistant is automatically enabled for Pro and Enterprise plans. The assistant lets your team ask questions and get answers with cited sources from your knowledge base. Configure the assistant from your [dashboard](https://dashboard.mintlify.com/products/assistant/settings):

- **Sample questions**: Add common questions like “how do I submit an expense report” or “what is the vacation policy” so people can get answers with one click.
- **Search sites**: Include additional sites the assistant can search when answering questions.
- **Deflection email**: Set a support email for questions the assistant can’t answer.

###

[​](#add-the-assistant-to-slack)

Add the assistant to Slack

The [Slack bot](https://www.mintlify.com/docs/ai/slack-bot) lets your team ask the assistant questions without leaving Slack. Create a channel where the bot responds to every message or let people @mention the bot in any channel.

##

[​](#enable-team-contributions)

Enable team contributions

A knowledge base stays accurate when everyone can update it, not just the people who set it up. Mintlify provides three ways for team members to contribute quickly to your knowledge base.

###

[​](#web-editor)

Web editor

The [web editor](https://www.mintlify.com/docs/editor) lets anyone create and edit pages in their browser. Contributors can:

- Edit pages visually or in Markdown.
- Drag and drop to reorganize navigation.
- Upload images and media.
- Create branches and pull requests for review.

This works well for subject matter experts who know the content but aren’t comfortable with code workflows.

###

[​](#agent)

Agent

The [agent](https://www.mintlify.com/docs/agent/quickstart) in your dashboard creates documentation updates from natural language prompts. Describe what you want to change, and the agent creates a pull request with the updates. For example, a team member could prompt “add a section to the expense policy page explaining how to submit receipts for meals over $50” and copy the existing expense policy page into the prompt. The agent would draft the content and open a PR for review.

###

[​](#capture-knowledge-from-slack)

Capture knowledge from Slack

Teams share valuable information in Slack that often never makes it into documentation. The [agent in Slack](https://www.mintlify.com/docs/agent/slack) can capture this knowledge and convert it into structured documentation. When someone shares useful information in a Slack thread, any team member can mention `@mintlify` with instructions to document it. The agent reads the conversation, extracts the relevant information, and creates a pull request. This is useful for capturing technical decisions, troubleshooting solutions, and process explanations while the context is still fresh. For example, if your team discussed how to configure a new integration in a thread, you could reply:

> @mintlify Create a guide for configuring the Acme integration based on this conversation.

The agent uses the thread context to create documentation that captures the key information from the discussion.

###

[​](#locally)

Locally

Anyone with access to your knowledge base repository can work locally in their preferred editor and push changes to your repository.

##

[​](#establish-maintenance-workflows)

Establish maintenance workflows

A knowledge base can decay quickly without maintenance. Set up systems to keep content up to date and help your team contribute to the knowledge base.

1

[](#)

Assign content ownership

Designate an owner or small team for each section. They don’t have to write all the content, but they’re responsible for:

- Reviewing content regularly.
- Flagging outdated information.
- Approving new pages in their section.
- Responding when people report errors.

2

[](#)

Set up review cycles and content verification

Content becomes stale over time. Establish a review schedule.

- **Critical content**: Review every 30 days
- **Standard content**: Review every 90 days
- **Evergreen content**: Review yearly

When reviewing, check:

- Are links still valid?
- Have systems or processes changed?
- Are examples current?
- Is there new information that should be added?

3

[](#)

Create contribution guidelines

Make it easy for anyone to improve the knowledge base. Your guidelines should cover:

- **Format**: Do you have specific templates or format requirements?
- **Process**: How should someone propose and submit changes?
- **Review**: Who reviews submissions? What’s the turnaround time?
- **Scope**: What types of content are in scope?

4

[](#)

Monitor usage metrics

Review how your team uses the knowledge base to prioritize content and identify areas for improvement. Set a regular cadence for reviewing usage metrics—monthly or quarterly are good intervals.

- Which articles get the most views? Invest in keeping these accurate and easy to read.
- Which articles get no views? Consider removing them or improving discoverability.
- What’s the bounce rate? If people leave immediately, the content might not be helpful or navigation could be improved.

##

[​](#next-steps)

Next steps

Your knowledge base is ready to launch. After deploying:

1.  Announce the knowledge base to your team.
2.  Monitor usage and search patterns in your analytics.
3.  Encourage contributions when people find gaps.
4.  Review and update content regularly.

The most successful knowledge bases evolve based on how teams actually use them.

Was this page helpful?

YesNo

[Create developer documentationPrevious](https://www.mintlify.com/docs/guides/developer-documentation)[Create a support centerNext](https://www.mintlify.com/docs/guides/support-center)

⌘I
