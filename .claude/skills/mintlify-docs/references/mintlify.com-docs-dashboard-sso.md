---
url: https://mintlify.com/docs/dashboard/sso
canonical: https://www.mintlify.com/docs/dashboard/sso
title: "Single sign-on (SSO) - Mintlify"
description: "Set up SAML or OIDC with identity providers for team authentication."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Dashboard access

Single sign-on (SSO)

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

    -   [Single sign-on (SSO)](https://www.mintlify.com/docs/dashboard/sso)
    -   [Deployment permissions](https://www.mintlify.com/docs/dashboard/permissions)
    -   [Roles](https://www.mintlify.com/docs/dashboard/roles)
    -   [Audit logs](https://www.mintlify.com/docs/dashboard/audit-logs)
    -   [Security contact](https://www.mintlify.com/docs/dashboard/security-contact)
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

SSO is available on [Enterprise plans](https://mintlify.com/pricing?ref=sso).

Enterprise admins can configure SAML SSO for Okta or Microsoft Entra directly from the Mintlify dashboard. For other providers like Google Workspace or Okta OIDC, [contact us](mailto:support@mintlify.com) to set up SSO.

##

[​](#set-up-sso)

Set up SSO

###

[​](#okta)

Okta

1

[](#)

Configure Okta SSO in your Mintlify dashboard

1.  In your Mintlify dashboard, navigate to the [Single Sign-On](https://dashboard.mintlify.com/settings/organization/sso) page.
2.  Click **Configure**.
3.  Select **Okta SAML**.
4.  Copy the **Single sign on URL** and **Audience URI**.

2

[](#)

Create a SAML app in Okta

1.  In Okta, under **Applications**, create a new app integration using SAML 2.0.
2.  Enter the following from Mintlify:
    -   **Single sign on URL**: the URL you copied from your Mintlify dashboard
    -   **Audience URI**: the URI you copied from your Mintlify dashboard
    -   **Name ID Format**: `EmailAddress`
3.  Add these attribute statements:

    | Name | Name format | Value |
    | --- | --- | --- |
    | `firstName` | Basic | `user.firstName` |
    | `lastName` | Basic | `user.lastName` |


3

[](#)

Copy the Okta metadata URL

In Okta, go to the **Sign On** tab of your application and copy the metadata URL.

4

[](#)

Save in Mintlify

Back in the Mintlify dashboard, paste the metadata URL and click **Save changes**.

###

[​](#microsoft-entra)

Microsoft Entra

1

[](#)

Configure Microsoft Entra SSO in your Mintlify dashboard

1.  In your Mintlify dashboard, navigate to the [Single Sign-On](https://dashboard.mintlify.com/settings/organization/sso) page.
2.  Click **Configure**.
3.  Select **Microsoft Entra ID SAML**.
4.  Copy the **Single sign on URL** and **Audience URI**.

2

[](#)

Create an enterprise application in Microsoft Entra

1.  In Microsoft Entra, navigate to **Enterprise applications**.
2.  Select **New application**.
3.  Select **Create your own application**.
4.  Select “Integrate any other application you don’t find in the gallery (Non-gallery).”

3

[](#)

Configure SAML in Microsoft Entra

1.  In Microsoft Entra, navigate to **Single Sign-On**.
2.  Select **SAML**.
3.  Under **Basic SAML Configuration**, enter the following:
    -   **Identifier (Entity ID)**: the Audience URI from Mintlify
    -   **Reply URL (Assertion Consumer Service URL)**: the Single sign on URL from Mintlify

Leave the other values blank and select **Save**.

4

[](#)

Configure Attributes & Claims in Microsoft Entra

1.  In Microsoft Entra, navigate to **Attributes & Claims**.
2.  Select **Unique User Identifier (Name ID)** under “Required Claim.”
3.  Change the Source attribute to `user.primaryauthoritativeemail`.
4.  Under **Additional claims**, create the following:

    | Name | Value |
    | --- | --- |
    | `firstName` | `user.givenname` |
    | `lastName` | `user.surname` |


5

[](#)

Copy the Microsoft Entra metadata URL

Under **SAML Certificates**, copy the **App Federation Metadata URL**.

6

[](#)

Save in Mintlify

Back in the Mintlify dashboard, paste the metadata URL and click **Save changes**.

7

[](#)

Assign users

In Microsoft Entra, navigate to **Users and groups**. Assign the users who should have access to your Mintlify dashboard.

##

[​](#jit-provisioning)

JIT provisioning

When you enable JIT (just-in-time) provisioning, users who sign in through your identity provider are automatically added to your Mintlify organization. To enable JIT provisioning, you must have SSO enabled. Navigate to the [Single Sign-On](https://dashboard.mintlify.com/settings/organization/sso) page in your dashboard, set up SSO, and then enable JIT provisioning.

##

[​](#change-or-remove-sso-provider)

Change or remove SSO provider

1.  Navigate to the [Single Sign-On](https://dashboard.mintlify.com/settings/organization/sso) page in your dashboard.
2.  Click **Configure**.
3.  Select your preferred SSO provider or no SSO.

If you remove SSO, users must authenticate with a password, magic link, or Google OAuth instead.

##

[​](#other-providers)

Other providers

For providers other than Microsoft Entra or Okta SAML, [contact us](mailto:support@mintlify.com) to configure SSO.

###

[​](#google-workspace-saml)

Google Workspace (SAML)

1

[](#)

Create an application

1.  In Google Workspace, navigate to **Web and mobile apps**.
2.  Select **Add custom SAML app** from the **Add app** dropdown.

![Screenshot of the Google Workspace SAML application creation page with the "Add custom SAML app" menu item highlighted](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gsuite-add-custom-saml-app.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=2c06c394d98ccd65df92aefceaeb75bd)

2

[](#)

Send us your IdP information

Copy the provided SSO URL, Entity ID, and x509 certificate and send it to the Mintlify team.

![Screenshot of the Google Workspace SAML application page with the SSO URL, Entity ID, and x509 certificate highlighted. The specific values for each of these are blurred out.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gsuite-saml-metadata.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=e9e47998599205dc051e9402cba63756)

3

[](#)

Configure integration

On the Service provider details page, enter the following:

- ACS URL (provided by Mintlify)
- Entity ID (provided by Mintlify)
- Name ID format: `EMAIL`
- Name ID: `Basic Information > Primary email`

![Screenshot of the Service provider details page with the ACS URL and Entity ID input fields highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gsuite-sp-details.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=a410a25f000fe2bc4d735a6ebe7754da)

On the next page, enter the following attribute statements:

| Google Directory Attribute | App Attribute |
| --- | --- |
| `First name` | `firstName` |
| `Last name` | `lastName` |

Once this step is complete and users are assigned to the application, let our team know and we’ll enable SSO for your account.

###

[​](#okta-oidc)

Okta (OIDC)

1

[](#)

Create an application

In Okta, under **Applications**, create a new app integration using OIDC. Choose the **Web Application** application type.

2

[](#)

Configure integration

Select the authorization code grant type and enter the Redirect URI provided by Mintlify.

3

[](#)

Send us your IdP information

Navigate to the **General** tab and locate the client ID and client secret. Securely provide these to us along with your Okta instance URL (for example, `<your-tenant-name>.okta.com`). You can send these via a service like 1Password or SendSafely.

Was this page helpful?

YesNo

[Authentication setupPrevious](https://www.mintlify.com/docs/deploy/authentication-setup)[Deployment permissionsNext](https://www.mintlify.com/docs/dashboard/permissions)

⌘I

![Screenshot of the Google Workspace SAML application creation page with the "Add custom SAML app" menu item highlighted](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gsuite-add-custom-saml-app.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=370f4a956ba1cdc9a68462b30dcafbe4)

![Screenshot of the Google Workspace SAML application page with the SSO URL, Entity ID, and x509 certificate highlighted. The specific values for each of these are blurred out.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gsuite-saml-metadata.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=5b4eb469d04332f194a0c7f36a17c81e)

![Screenshot of the Service provider details page with the ACS URL and Entity ID input fields highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/gsuite-sp-details.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=1f97959e4cad04acfb8741400a701694)
