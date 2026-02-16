---
url: https://mintlify.com/docs/deploy/preview-deployments
canonical: https://www.mintlify.com/docs/deploy/preview-deployments
title: "Preview deployments - Mintlify"
description: "Get unique preview URLs for pull requests to review changes before merging."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Deploy

Preview deployments

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

Preview deployments are available on [Pro and Enterprise plans](https://mintlify.com/pricing?ref=preview-deployments).

Preview deployments let you see how changes to your docs will look before merging to production. Each preview creates a shareable URL that updates automatically as you push new changes. Preview URLs are publicly viewable by default. Share a preview link with anyone who needs to review your changes.

##

[​](#create-preview-deployments)

Create preview deployments

Preview deployments are created automatically through pull requests or manually from your dashboard.

###

[​](#automatic-previews)

Automatic previews

Automatic previews are only created for pull requests targeting your [deployment branch](https://www.mintlify.com/docs/guides/git-concepts#deployment-branch).

When you create a pull request, the Mintlify bot automatically adds a link to view the preview deployment in your pull request. The preview updates each time you push new commits to the branch.

![Link to view deployment in the pull request timeline](https://mintcdn.com/mintlify/f7fo9pnTEtzBD70_/images/previews/preview-deployment-light.png?fit=max&auto=format&n=f7fo9pnTEtzBD70_&q=85&s=4cbf574001b521afbd8c9f6717ed907f)![Link to view deployment in the pull request timeline](https://mintcdn.com/mintlify/f7fo9pnTEtzBD70_/images/previews/preview-deployment-dark.png?fit=max&auto=format&n=f7fo9pnTEtzBD70_&q=85&s=9fbb5054761316d1bbb8168646ed51bf)

###

[​](#manual-previews)

Manual previews

You can manually create a preview for any branch.

1.  Go to your [dashboard](https://dashboard.mintlify.com/).
2.  Select **Previews**.
3.  Select **Create custom preview**.
4.  Enter the name of the branch you want to preview.
5.  Select **Create deployment**.

##

[​](#redeploy-a-preview)

Redeploy a preview

Redeploy a preview to refresh content or retry after a failed deployment.

1.  Select the preview from your [dashboard](https://dashboard.mintlify.com/).
2.  Select **Redeploy**.

![The Previews menu with the deploy button emphasized by an orange rectangle.](https://mintcdn.com/mintlify/f7fo9pnTEtzBD70_/images/previews/redeploy-preview-light.png?fit=max&auto=format&n=f7fo9pnTEtzBD70_&q=85&s=eaa1711b0c580931036f1d1f4685312e)![The Previews menu with the deploy button emphasized by an orange rectangle.](https://mintcdn.com/mintlify/f7fo9pnTEtzBD70_/images/previews/redeploy-preview-dark.png?fit=max&auto=format&n=f7fo9pnTEtzBD70_&q=85&s=086e0340522fc6a620e47e3e35703ae2)

##

[​](#preview-widget)

Preview widget

The preview widget appears on preview deployments to help you navigate and review updated pages. The widget is a floating button in the bottom-right corner of your preview deployment.

![Preview widget expanded to show list of changed files.](https://mintcdn.com/mintlify/AjqaLQO45zsoo98J/images/previews/widget-light.png?fit=max&auto=format&n=AjqaLQO45zsoo98J&q=85&s=c6928d2ead75217426f1cc703fef5271)![Preview widget expanded to show list of changed files.](https://mintcdn.com/mintlify/AjqaLQO45zsoo98J/images/previews/widget-dark.png?fit=max&auto=format&n=AjqaLQO45zsoo98J&q=85&s=cdeb39bd833e56e69563ff226a106708)

1.  Click the widget to show all added, modified, or removed files in the preview.
2.  Click a file to view the changes on the corresponding page.
3.  Use the search bar to filter the list of changed files.

The widget only appears on preview deployments, not on your live site or local previews.

##

[​](#restrict-access-to-preview-deployments)

Restrict access to preview deployments

By default, preview deployments are publicly accessible to anyone with the URL. You can restrict access to authenticated members of your Mintlify organization.

1.  Navigate to the **Previews** section in the [Add-ons](https://dashboard.mintlify.com/products/addons) page of your dashboard.
2.  Click the **Preview authentication** toggle to enable or disable preview authentication.

![The preview authentication toggle in the Add-ons page](https://mintcdn.com/mintlify/JpjPdD_YybFKEYPk/images/previews/preview-auth-light.png?fit=max&auto=format&n=JpjPdD_YybFKEYPk&q=85&s=efbbd50e1a18d29953f17fb8a9d7138b)![The preview authentication toggle in the Add-ons page](https://mintcdn.com/mintlify/JpjPdD_YybFKEYPk/images/previews/preview-auth-dark.png?fit=max&auto=format&n=JpjPdD_YybFKEYPk&q=85&s=b5d877ae3918afcd852a8047eab98233)

##

[​](#troubleshooting-preview-deployments)

Troubleshooting preview deployments

If your preview deployment fails, try these troubleshooting steps.

- **View the build logs**: In your [dashboard](https://dashboard.mintlify.com/), go to **Previews** and click the failed preview. The deployment logs show errors that caused failures.
- **Check your configuration**:
    -   Invalid `docs.json` syntax
    -   Missing or incorrect file paths referenced in your navigation
    -   Invalid frontmatter in MDX files
    -   Broken image links or missing image files
- **Validate locally**: Run `mint dev` locally to catch build errors before pushing to the repository.
- **Check recent changes**: Review the most recent commits in your branch to identify what changes caused the build to fail.

Was this page helpful?

YesNo

[DeploymentsPrevious](https://www.mintlify.com/docs/deploy/deployments)[OverviewNext](https://www.mintlify.com/docs/deploy/docs-subpath)

⌘I

![Link to view deployment in the pull request timeline](https://mintcdn.com/mintlify/f7fo9pnTEtzBD70_/images/previews/preview-deployment-dark.png?w=1650&fit=max&auto=format&n=f7fo9pnTEtzBD70_&q=85&s=fc090479eb70d57448ad26bf279f8b3a)

![The Previews menu with the deploy button emphasized by an orange rectangle.](https://mintcdn.com/mintlify/f7fo9pnTEtzBD70_/images/previews/redeploy-preview-dark.png?w=1650&fit=max&auto=format&n=f7fo9pnTEtzBD70_&q=85&s=d05748dbe4b8008f53fcc2da6ec3cde7)

![Preview widget expanded to show list of changed files.](https://mintcdn.com/mintlify/AjqaLQO45zsoo98J/images/previews/widget-dark.png?w=1650&fit=max&auto=format&n=AjqaLQO45zsoo98J&q=85&s=48db60828829ae3c145ddd0910a1b06e)

![The preview authentication toggle in the Add-ons page](https://mintcdn.com/mintlify/JpjPdD_YybFKEYPk/images/previews/preview-auth-dark.png?w=1650&fit=max&auto=format&n=JpjPdD_YybFKEYPk&q=85&s=0ce6ee48959b1002fdba61540d24cf0e)
