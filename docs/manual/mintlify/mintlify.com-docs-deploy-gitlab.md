---
url: https://mintlify.com/docs/deploy/gitlab
canonical: https://www.mintlify.com/docs/deploy/gitlab
title: "GitLab - Mintlify"
description: "Connect to a GitLab repository for automated deployments and preview builds."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Deploy

GitLab

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

We use access tokens and webhooks to authenticate and sync changes between GitLab and Mintlify.

- Mintlify uses access tokens to pull information from GitLab.
- GitLab uses webhooks to notify Mintlify when changes are made, enabling preview deployments for merge requests.

##

[​](#set-up-the-connection)

Set up the connection

**HTTPS cloning required**: Your GitLab project must have HTTPS cloning enabled for Mintlify to access your repository. You can verify this in GitLab by going to your project’s **Settings** > **General** > **Visibility and access controls** section.

1

[](#)

Find your project ID

In your GitLab project, navigate to **Settings** > **General** and locate your **Project ID**.

![The General Settings page in the GitLab dashboard. The Project ID is highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gitlab/gitlab-project-id.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=4aae3ff6adbb509b607a63a4998992d0)

2

[](#)

Generate an access token

Navigate to **Settings** > **Access Tokens** and select **Add new token**.Configure the token with these settings:

- **Name**: Mintlify
- **Role**: Maintainer (required for private repos)
- **Scopes**: `api` and `read_api`

Click **Create project access token** and copy the token.

If Project Access Tokens are not available, you can use a Personal Access Token instead. Note that Personal Access Tokens expire and must be updated.

![The Access tokens page in the GitLab dashboard. The settings to configure for Mintlify are highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gitlab/gitlab-project-access-token.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=59ef23c54d88cdd723632086bced658b)

3

[](#)

Set up the connection

In the [Mintlify dashboard](https://dashboard.mintlify.com/settings/deployment/git-settings):

1.  Enter your project ID and access token.
2.  Complete any other required configurations.
3.  Click **Save Changes**.

![The GitLab configuration panel in the Git Settings page of the Mintlify dashboard.](https://mintcdn.com/mintlify/TMkAdDUtcJGNvRU5/images/gitlab/gitlab-config-light.png?fit=max&auto=format&n=TMkAdDUtcJGNvRU5&q=85&s=98809a957ecd59f3d2f2bd747086c5a2)![The GitLab configuration panel in the Git Settings page of the Mintlify dashboard.](https://mintcdn.com/mintlify/TMkAdDUtcJGNvRU5/images/gitlab/gitlab-config-dark.png?fit=max&auto=format&n=TMkAdDUtcJGNvRU5&q=85&s=b4834ea4d6ebf771b7af095589a194ac)

##

[​](#create-the-webhook)

Create the webhook

Webhooks allow us to receive events when changes are made so that we can automatically trigger deployments.

1

[](#)

Add new webhook

1.  In GitLab, navigate to **Settings** > **Webhooks**.
2.  Click **Add new webhook**.

![Screenshot of the Webhooks page in the GitLab dashboard.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gitlab/gitlab-webhook.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=760e8faa2437ecf8ff2739c4dfa0bdc4)

2

[](#)

Set up URL and webhook

Name the webhook **Mintlify**.In the **URL** field, enter the endpoint `https://leaves.mintlify.com/gitlab-webhook`.

3

[](#)

Get webtoken

In your Mintlify dashboard, click **Show Webtoken**. Copy the webtoken.

![Screenshot of the GitLab connection in the Mintlify dashboard.](https://mintcdn.com/mintlify/iZZGgKQ6swbDUuUa/images/gitlab/show-webtoken-light.png?fit=max&auto=format&n=iZZGgKQ6swbDUuUa&q=85&s=50d2acef9a5f88b607128f7c5292743c)![Screenshot of the GitLab connection in the Mintlify dashboard.](https://mintcdn.com/mintlify/iZZGgKQ6swbDUuUa/images/gitlab/show-webtoken-dark.png?fit=max&auto=format&n=iZZGgKQ6swbDUuUa&q=85&s=9fa9732011ac61c1250ebae004de87be)

4

[](#)

Paste webtoken

In GitLab, paste the webtoken from your Mintlify dashboard in the **Secret token** field.

5

[](#)

Select events

Select the following events to trigger the webhook:

- **Push events** (All branches)
- **Merge requests events**

6

[](#)

Verify the webhook

You should see the following settings after configuring the webhook:

- **Name**: Mintlify
- **URL**: `https://leaves.mintlify.com/gitlab-webhook`
- **Secret token**: The webtoken from your Mintlify dashboard
- **Events**: **Push events** (All branches) and **Merge requests events**

Add the webhook.

![The Webhook page in the GitLab dashboard. The settings to configure for Mintlify are highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gitlab/gitlab-project-webtoken.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=00c0ce70ce9e8dbc2712f71aaeef3362)

7

[](#)

Test the webhook

After you create the webhook, click the **Test** dropdown. Click **Push events** to send a sample payload. If the test returns `Hook executed successfully: HTTP 200`, your webhook is configured correctly.

![Screenshot of the GitLab Webhooks page. The 'Push events' menu item is highlighted in the 'Test' menu.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gitlab/gitlab-project-webtoken-test.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=3ad52f7ac39124a4c03944256d0b79d3)

Was this page helpful?

YesNo

[GitHub Enterprise ServerPrevious](https://www.mintlify.com/docs/deploy/ghes)[AssistantNext](https://www.mintlify.com/docs/ai/assistant)

⌘I

![The General Settings page in the GitLab dashboard. The Project ID is highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gitlab/gitlab-project-id.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=c18b327b668e3111c2c365bd28804d4f)

![The Access tokens page in the GitLab dashboard. The settings to configure for Mintlify are highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gitlab/gitlab-project-access-token.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=0b593dfe4be4578274123931ec3fd9a8)

![The GitLab configuration panel in the Git Settings page of the Mintlify dashboard.](https://mintcdn.com/mintlify/TMkAdDUtcJGNvRU5/images/gitlab/gitlab-config-dark.png?w=1650&fit=max&auto=format&n=TMkAdDUtcJGNvRU5&q=85&s=32f2f35d16704fa661ccf963a7d47635)

![Screenshot of the Webhooks page in the GitLab dashboard.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gitlab/gitlab-webhook.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=99c65eb0a83da2b793c1608ea3a47cbc)

![Screenshot of the GitLab connection in the Mintlify dashboard.](https://mintcdn.com/mintlify/iZZGgKQ6swbDUuUa/images/gitlab/show-webtoken-dark.png?w=1650&fit=max&auto=format&n=iZZGgKQ6swbDUuUa&q=85&s=fe78cb48d5c090f0a931c477e425d678)

![The Webhook page in the GitLab dashboard. The settings to configure for Mintlify are highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gitlab/gitlab-project-webtoken.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=24770ed142d0cf9b7bfb0dc307c13449)

![Screenshot of the GitLab Webhooks page. The 'Push events' menu item is highlighted in the 'Test' menu.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gitlab/gitlab-project-webtoken-test.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=ebd368461ffa4880d63a3ecbda59d84e)
