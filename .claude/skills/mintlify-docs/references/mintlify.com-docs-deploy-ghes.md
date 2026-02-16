---
url: https://mintlify.com/docs/deploy/ghes
canonical: https://www.mintlify.com/docs/deploy/ghes
title: "GitHub Enterprise Server - Mintlify"
description: "Set up the GitHub App on your GitHub Enterprise Server installation."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Deploy

GitHub Enterprise Server

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

This guide walks you through setting up the Mintlify GitHub App on your GitHub Enterprise Server (GHES) installation. To connect a GHES instance to Mintlify, you must create a local version of our app within your self-hosted environment that communicates with our remote server. If you use a cloud-hosted GitHub instance, see the [GitHub](https://www.mintlify.com/docs/deploy/github) page for setup instructions.

##

[​](#prerequisites)

Prerequisites

- Admin privileges on your GitHub Enterprise Server organization where you want to install the app
- Access to your organization’s repositories where you want to install the app
- Network connectivity to communicate with our external services (see [Network requirements](#network-requirements) section below)

###

[​](#network-requirements)

Network requirements

####

[​](#outbound-connectivity)

Outbound connectivity

Your GitHub Enterprise Server must be able to reach:

- Mintlify’s API endpoints ([https://leaves.mintlify.com](https://leaves.mintlify.com))
- Webhook receivers (port 443)

####

[​](#firewall-configuration)

Firewall configuration

The following outbound connections must be allowed:

- Connections from Mintlify’s static IP: `54.242.90.151`
- HTTPS (port 443) to Mintlify’s service domains
- DNS resolution for Mintlify’s service domains

##

[​](#step-1-register-the-github-app)

Step 1: Register the GitHub App

See [Registering a GitHub App](https://docs.github.com/en/enterprise-server@3.18/apps/creating-github-apps/registering-a-github-app/registering-a-github-app) in the GitHub documentation for detailed instructions.

1

[](#)

Navigate to your organization settings

1.  In the upper-right corner of any page on GitHub, click your profile picture.
2.  Click **Your organizations**.
3.  Click **Settings** next to the organization that you want to create the app for.

2

[](#)

Create a new GitHub App

1.  In the left sidebar, click **Developer settings**.
2.  Click **GitHub Apps**.
3.  Click **New GitHub App**.

3

[](#)

Configure basic app information

Set the following:

- **GitHub App name:** `Mintlify`
- **Description:** `Integration with Mintlify services`
- **Homepage URL:** `https://mintlify.com`
- **User authorization callback URL:** `https://your-github-server.com/` (replace with your actual GHES domain)

##

[​](#step-2-configure-app-permissions)

Step 2: Configure app permissions

1

[](#)

Set repository permissions

Set the following permissions for the app. No Organization, Account, or Enterprise permissions are required:

- **Checks:** Read and write
- **Contents:** Read and write
- **Deployments:** Read and write
- **Metadata:** Read-only
- **Pull Requests:** Read and write

2

[](#)

Subscribe to Events

Select the following webhook events:

- Installation
- Installation Target
- Create
- Delete
- Public
- Pull Request
- Push
- Repository

##

[​](#step-3-generate-and-secure-credentials)

Step 3: Generate and secure credentials

1

[](#)

Create the app

Click **Create GitHub App**.You’ll be redirected to the app’s settings page.

2

[](#)

Generate private key

1.  Scroll down to the **Private keys** section.
2.  Click **Generate a private key**.
3.  Download the `.pem` file and securely store it.

3

[](#)

Note app credentials

Record the following:

- **App ID** (visible at the top of the settings page)
- **Client ID** (in the “About” section)
- **Client Secret** (generate and record it securely)

##

[​](#step-4-install-the-app)

Step 4: Install the app

1

[](#)

Navigate to app installation

1.  From the app settings page, click **Install App** in the left sidebar.
2.  Select your organization from the list.

2

[](#)

Choose installation scope

Select either:

- **All repositories** (for organization-wide access)
- **Only select repositories** (choose specific repositories)

We recommend selecting “Only select repositories” and limiting the app to only the repositories where your documentation is located.

3

[](#)

Complete the installation

1.  Click **Install**.
```
https://your-github-server.com/settings/installations/12345
```

##

[​](#step-5-configure-webhook-url)

Step 5: Configure webhook URL

1

[](#)

Return to app settings

1.  Go back to your app’s settings page.
2.  Scroll to the **Webhook** section.

2

[](#)

Set webhook URL

Configure the following:

- **Webhook URL:** `https://leaves.mintlify.com/github-enterprise/:subdomain` (replace `:subdomain` with the URL that we provide you with)
- **Webhook secret:** Generate a random string (32+ characters) and record it securely. Mintlify can also generate this and provide it to you.

##

[​](#share-credentials-with-us)

Share credentials with us

Please share the following information with our team using your secure information transfer method of choice.

###

[​](#required-credentials)

Required credentials

- GitHub Enterprise Server base URL: [https://your-github-server.com](https://your-github-server.com)
- App ID: (from step 3)
- App client ID: (from step 3)
- App client secret: (from step 3)
- Installation ID: (from step 4)
- Private key: The entire contents of the `.pem` file (should be shared via secure file transfer)
- Webhook secret: (from step 5)

###

[​](#optional-credentials-for-troubleshooting)

Optional credentials for troubleshooting

- Organization name: Your GitHub organization name
- Repository names: Specific repositories where the app is installed
- GitHub Enterprise Server version: Found in your site admin dashboard

##

[​](#mintlify-connection)

Mintlify connection

We take the credentials you provide us and store them, encrypted, in a secure location. Then we work with you to either:

- Integrate your GHES environment with an existing Mintlify deployment.
- Integrate your GHES environment with a new Mintlify deployment that we provision for you.

After your GHES environment is integrated with a Mintlify deployment, you are ready to enable webhooks for your GitHub App.

The webhook URL may change based on our configuration. We test the integration and provide you with the new URL.

##

[​](#test-the-integration)

Test the integration

1

[](#)

Verify webhook delivery

1.  Go to your GitHub App settings.
2.  Click the **Advanced** tab.
3.  Check “Recent Deliveries” for successful webhook deliveries.
4.  Look for HTTP 200 responses.

2

[](#)

Test repository access

1.  Create a test issue or pull request in an installed repository.
2.  Verify that Mintlify responds appropriately.

##

[​](#faq-and-troubleshooting)

FAQ and Troubleshooting

The app installation is failing with permission errors.

Ensure you have:

- Site admin privileges for app creation
- Organization owner or admin rights for app installation.
- Proper repository permissions if installing on specific repositories.

Webhooks aren't being delivered

- Verify the webhook URL is correct and accessible.
- Ensure your firewall allows outbound HTTPS connections.
- Check the webhook secret matches what was configured.
- Review webhook delivery logs in the “Advanced” tab of your GitHub App settings.

I'm getting SSL/TLS certificate errors

Your GHES might use self-signed certificates. Our services cannot verify your server’s certificate.**Solution:** Ensure your GHES has a valid SSL certificate.

The app installs, but doesn't respond to events.

- Ensure webhooks are being delivered and acknowledged by our server with response code 200.
- Required permissions were granted during installation.

Can I limit which repositories the app accesses?

Yes, during installation you can select “Only select repositories” and choose specific ones. You can modify this later in your organization’s installed apps settings. This is the recommended form of installation.

How do I update app permissions later?

- Go to the app settings as a site admin.
- Modify permissions as needed.
- The app will need to be re-approved by organization owners.
- Notify us of any permission changes as they may affect functionality.

Our GHES is behind a corporate firewall, nginx proxy, or similar setup.

You must:

- Whitelist our service domains in your firewall.
- Ensure outbound HTTPS (port 443) connectivity.
- If direct internet access is not allowed, set up a proxy.

Can this work with GHES in air-gapped environments?

No, your GHES must be able to communicate with our cloud-hosted server.

Who should I contact if I need help?

Please reach out to your customer success representative who you’ve spoken to at Mintlify, or our support team at [](mailto:support@mintlify.com)[support@mintlify.com](mailto:support@mintlify.com) with:

- Your GitHub Enterprise Server version.
- Specific error messages.
- Screenshots of any issues.
- Network/firewall configuration details (if relevant).

Was this page helpful?

YesNo

[GitHubPrevious](https://www.mintlify.com/docs/deploy/github)[GitLabNext](https://www.mintlify.com/docs/deploy/gitlab)

⌘I
