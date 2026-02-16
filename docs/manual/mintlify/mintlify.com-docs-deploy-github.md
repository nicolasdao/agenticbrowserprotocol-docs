---
url: https://mintlify.com/docs/deploy/github
canonical: https://www.mintlify.com/docs/deploy/github
title: "GitHub - Mintlify"
description: "Connect to a GitHub repository for automated deployments, pull request previews, and continuous synchronization."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Deploy

GitHub

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

Mintlify uses a GitHub App to automatically sync your documentation with your GitHub repository.

**Do you need the GitHub App?**

- **Mintlify-hosted repository** in the `mintlify-community` organization: No. The GitHub App is already configured.
- **Your own repository**: Yes. Install the GitHub App to enable automatic deployments when you push changes.

See your repository in the [Git Settings](https://dashboard.mintlify.com/settings/deployment/git-settings) page of your dashboard.

If your repository is in a private repository owned by the Mintlify organization, the GitHub App is automatically configured and managed by Mintlify. You can use the web editor to make changes to your documentation. If you want to work on your documentation locally, clone the repository to your own organization and update your Git settings to use your own repository.

##

[​](#clone-to-your-own-repository)

Clone to your own repository

If you skipped connecting your own Git repository during onboarding, your documentation lives in a private repository owned by the Mintlify organization. To move it to your own account or organization:

1.  Go to [Git Settings](https://dashboard.mintlify.com/settings/deployment/git-settings) in your dashboard.
2.  Download your documentation as a zip file.
3.  Create a new repository on GitHub or GitLab.
4.  Extract the zip contents and push them to your new repository.
5.  Return to [Git Settings](https://dashboard.mintlify.com/settings/deployment/git-settings) and connect your new repository to Mintlify.
6.  Install the GitHub App by following the steps in [Install the GitHub App](#install-the-github-app) below.

##

[​](#install-the-github-app)

Install the GitHub App

You must have organization ownership or administrator permissions in a repository to install the app. If you lack the necessary permissions, the repository owner must approve the installation request.

Install the Mintlify GitHub App through your [dashboard](https://dashboard.mintlify.com/settings/organization/github-app).

We recommend only granting access to your documentation repository.

![Mintlify GitHub App installation page with the 'Only select repositories' option selected.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/github/select-repos.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=35cc7fc3564471ccef7a54029ef18cd4)

##

[​](#permissions)

Permissions

When you install the GitHub App, grant the following permissions. Read permissions:

- `metadata`: Basic repository information

Read and write permissions:

- `checks`: Create status checks on pull requests
- `code`: Read file changes when you commit to your docs branch
- `deployments`: Generate preview deployments for pull requests
- `pull requests`: Create branches and pull requests from the web editor

The app only accesses repositories that you explicitly grant it access to. If you have branch protection rules enabled, the app can’t push directly to protected branches.

##

[​](#manage-repository-access)

Manage repository access

When installing the GitHub App, you can grant access to all of your repositories or specific ones. We recommend only granting access to your documentation repository and any repositories that you want to provide as context for the agent. You can modify this selection anytime in your [GitHub App settings](https://github.com/apps/mintlify/installations/new).

##

[​](#configure-docs-source)

Configure docs source

Change the organization, repository, or branch that your documentation builds from in the [Git Settings](https://dashboard.mintlify.com/settings/deployment/git-settings) section of your dashboard.

##

[​](#github-enterprise-with-ip-allowlists)

GitHub Enterprise with IP allowlists

If your GitHub Enterprise Cloud organization has an IP allowlist enabled, you need to add Mintlify’s egress IP address (`54.242.90.151`) to your allowlist for the GitHub App to function properly. Follow [GitHub’s documentation](https://docs.github.com/en/enterprise-cloud@latest/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/managing-allowed-ip-addresses-for-your-organization) to configure your IP allowlist.

##

[​](#troubleshooting)

Troubleshooting

###

[​](#deployment-not-triggering-automatically)

Deployment not triggering automatically

If pushes to your repository don’t trigger deployments, check the following possible problems.

Verify GitHub App installation

Check that the correct repository has the app installed.

1.  Go to [GitHub App settings](https://dashboard.mintlify.com/settings/organization/github-app) in your dashboard.
2.  Check that your repository is on the active app installations list.

Check deployment branch

Ensure that you’re pushing to the correct branch.

1.  Go to [Git Settings](https://dashboard.mintlify.com/settings/deployment/git-settings)
2.  Verify the branch in your dashboard matches the branch that you’re pushing to.

###

[​](#github-app-connection-issues)

GitHub App connection issues

If you encounter problems with the GitHub app, resetting the connection can solve most problems.

1

[](#)

Uninstall the Mintlify app through GitHub.

1.  In GitHub, go to [installations](https://github.com/settings/installations) and select **Configure** next to the Mintlify app. Scroll down and select **Uninstall**.
2.  Go to [Authorized GitHub Apps](https://github.com/settings/apps/authorizations) and select **Revoke** next to the Mintlify app.

2

[](#)

Reinstall the Mintlify app.

1.  In your Mintlify dashboard, go to [Git Settings](https://dashboard.mintlify.com/settings/deployment/git-settings) and install the GitHub app.
2.  Authorize your account in the [My Profile](https://dashboard.mintlify.com/settings/account) section of your dashboard.

###

[​](#feedback-add-ons-are-unavailable)

Feedback add-ons are unavailable

The edit suggestions and raise issues feedback features are only available for public GitHub repositories. If these options are disabled in your dashboard, check your repository visibility. If your repository is public and you cannot enable the edit suggestions or raise issues options in your dashboard, revalidate your Git settings.

1

[](#)

Navigate to Git Settings

Go to [Git Settings](https://dashboard.mintlify.com/settings/deployment/git-settings) in your dashboard.

2

[](#)

Revalidate your settings

Click the green check mark in the corner of the Git settings box to revalidate your repository settings. This forces an update to your repository settings to reflect whether your repository is public or private.

![The Git Settings page in the Mintlify dashboard. An orange arrow points to the green check mark that revalidates the repository settings.](https://mintcdn.com/mintlify/0GhkFxoI6iPIzBkf/images/github/revalidate-settings-light.png?fit=max&auto=format&n=0GhkFxoI6iPIzBkf&q=85&s=b3c7c421876bb4a2921ece22fc4b4777)![The Git Settings page in the Mintlify dashboard. An orange arrow points to the green check mark that revalidates the repository settings.](https://mintcdn.com/mintlify/0GhkFxoI6iPIzBkf/images/github/revalidate-settings-dark.png?fit=max&auto=format&n=0GhkFxoI6iPIzBkf&q=85&s=9d2462cd3e07c9e7cf0835b3c50e3020)

Was this page helpful?

YesNo

[CI checksPrevious](https://www.mintlify.com/docs/deploy/ci)[GitHub Enterprise ServerNext](https://www.mintlify.com/docs/deploy/ghes)

⌘I

![Mintlify GitHub App installation page with the 'Only select repositories' option selected.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/github/select-repos.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=799d62da575693367a5fa9c787064968)

![The Git Settings page in the Mintlify dashboard. An orange arrow points to the green check mark that revalidates the repository settings.](https://mintcdn.com/mintlify/0GhkFxoI6iPIzBkf/images/github/revalidate-settings-dark.png?w=1650&fit=max&auto=format&n=0GhkFxoI6iPIzBkf&q=85&s=4bc8a85bfc148c6864423611db134c29)
