---
url: https://mintlify.com/docs/deploy/authentication-setup
canonical: https://www.mintlify.com/docs/deploy/authentication-setup
title: "Authentication setup - Mintlify"
description: "Control access to your documentation by authenticating users."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Deploy

Authentication setup

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

[Pro plans](https://mintlify.com/pricing?ref=authentication) include password authentication.[Enterprise plans](https://mintlify.com/pricing?ref=authentication) include all authentication methods.

Authentication requires users to log in before accessing your documentation. When you enable authentication, users must log in to access any content. You can configure specific pages or groups as public while keeping other pages protected.

##

[​](#configure-authentication)

Configure authentication

Select the handshake method that you want to configure.

- Password

- Mintlify dashboard

- OAuth 2.0

- JWT


Password authentication provides access control only and does **not** support user-specific features like group-based access control or API playground pre-filling.

###

[​](#prerequisites)

Prerequisites

- Your security requirements allow sharing passwords among users.

###

[​](#set-up)

Set up

1

[](#)

Create a password.

1.  In your dashboard, go to [Authentication](https://dashboard.mintlify.com/products/authentication).
2.  Enable authentication.
3.  In the **Password Protection** section, enter a secure password

After you enter a password, your site redeploys. When it finishes deploying, anyone who visits your site must enter the password to access your content.

2

[](#)

Distribute access.

Securely share the password and documentation URL with authorized users.

###

[​](#example)

Example

You host your documentation at `docs.foo.com` and you need basic access control without tracking individual users. You want to prevent public access while keeping setup simple.**Create a strong password** in your dashboard. **Share credentials** with authorized users. That’s it!

###

[​](#prerequisites-2)

Prerequisites

- Everyone who needs to access your documentation must be a member of your Mintlify organization.

###

[​](#set-up-2)

Set up

1

[](#)

Enable Mintlify dashboard authentication.

1.  In your dashboard, go to [Authentication](https://dashboard.mintlify.com/products/authentication).
2.  Enable authentication.
3.  In the **Custom Authentication** section, click **Mintlify Auth**.
4.  Click **Enable Mintlify Auth**.

After you enable Mintlify authentication, your site redeploys. When it finishes deploying, anyone who visits your site must log in to your Mintlify organization to access your content.

2

[](#)

Add authorized users.

1.  In your dashboard, go to [Members](https://dashboard.mintlify.com/settings/organization/members).
2.  Add each person who should have access to your documentation.
3.  Assign appropriate roles based on their editing permissions.

###

[​](#example-2)

Example

You host your documentation at `docs.foo.com` and your entire team has access to your dashboard. You want to restrict access to team members only.**Enable Mintlify authentication** in your dashboard settings.**Verify team access** by checking that all team members are active in your organization.

###

[​](#prerequisites-3)

Prerequisites

- An OAuth or OIDC server that supports the Authorization Code Flow.
- Ability to create an API endpoint accessible by OAuth access tokens (optional, to enable group-based access control).

###

[​](#set-up-3)

Set up

1

[](#)

Configure your OAuth settings.

1.  In your dashboard, go to [Authentication](https://dashboard.mintlify.com/products/authentication).
2.  Enable authentication.
3.  In the **Custom Authentication** section, click **OAuth**.
4.  Configure these fields:

- **Authorization URL**: Your OAuth endpoint.
- **Client ID**: Your OAuth 2.0 client identifier.
- **Client Secret**: Your OAuth 2.0 client secret.
- **Scopes** (optional): Permissions to request. Copy the **entire** scope string (for example, for a scope like `provider.users.docs`, copy the complete `provider.users.docs`). Use multiple scopes if you need different access levels.
- **Additional authorization parameters** (optional): Additional query parameters to add to the initial authorization request.
- **Token URL**: Your OAuth token exchange endpoint.
- **Info API URL** (optional): Endpoint on your server that Mintlify calls to retrieve user info. Required for group-based access control. If omitted, the OAuth flow only verifies identity.
- **Logout URL** (optional): The native logout URL for your OAuth provider. When users log out, Mintlify validates the logout redirect against this configured URL for security. The redirect only succeeds if it exactly matches the configured `logoutUrl`. If you do not configure a logout URL, users redirect to `/login`. Mintlify redirects users with a `GET` request and does not append query parameters, so include any parameters (for example, `returnTo`) directly in the URL.
- **Redirect URL** (optional): The URL to redirect users to after authentication.

5.  Click **Save changes**.

After you configure your OAuth settings, your site redeploys. When it finishes deploying, anyone who visits your site must log in to your OAuth provider to access your content.

2

[](#)

Configure your OAuth server.

1.  Copy the **Redirect URL** from your [authentication settings](https://dashboard.mintlify.com/products/authentication).
2.  Add the redirect URL as an authorized redirect URL for your OAuth server.

3

[](#)

Create your user info endpoint (optional).

To enable group-based access control, create an API endpoint that:

- Responds to `GET` requests.
- Accepts an `Authorization: Bearer <access_token>` header for authentication.
- Returns user data in the `User` format. See [User data format](#user-data-format) for more information.

Mintlify calls this endpoint with the OAuth access token to retrieve user information. No additional query parameters are sent.Add this endpoint URL to the **Info API URL** field in your [authentication settings](https://dashboard.mintlify.com/products/authentication).

###

[​](#example-3)

Example

You host your documentation at `foo.com/docs` and you have an existing OAuth server at `auth.foo.com` that supports the Authorization Code Flow.**Configure your OAuth server details** in your dashboard:

- **Authorization URL**: `https://auth.foo.com/authorization`
- **Client ID**: `ydybo4SD8PR73vzWWd6S0ObH`
- **Scopes**: `['provider.users.docs']`
- **Token URL**: `https://auth.foo.com/exchange`
- **Info API URL**: `https://api.foo.com/docs/user-info`
- **Logout URL**: `https://auth.foo.com/logout?returnTo=https%3A%2F%2Ffoo.com%2Fdocs`

**Create a user info endpoint** at `api.foo.com/docs/user-info`, which requires an OAuth access token with the `provider.users.docs` scope, and returns:
```
{
  "groups": ["engineering", "admin"],
  "expiresAt": 1735689600,
  "apiPlaygroundInputs": {
    "header": {
      "Authorization": "Bearer user_abc123"
    }
  }
}
```
Control session length with the `expiresAt` field in your user info response. This is a Unix timestamp (seconds since epoch) indicating when the session should expire. See [User data format](#user-data-format) for more details.

**Configure your OAuth server to allow redirects** to your callback URL.

###

[​](#prerequisites-4)

Prerequisites

- An authentication system that can generate and sign JWTs.
- A backend service that can create redirect URLs.

###

[​](#set-up-4)

Set up

1

[](#)

Generate a private key.

1.  In your dashboard, go to [Authentication](https://dashboard.mintlify.com/products/authentication).
2.  Enable authentication.
3.  In the **Custom Authentication** section, click **JWT**.
4.  Enter the URL of your existing login flow.
5.  Click **Save changes**.
6.  Click **Generate new key**.
7.  Store your key securely where it can be accessed by your backend.

After you generate a private key, your site redeploys. When it finishes deploying, anyone who visits your site must log in to your JWT authentication system to access your content.

2

[](#)

Integrate Mintlify authentication into your login flow.

Modify your existing login flow to include these steps after user authentication:

- Create a JWT containing the authenticated user’s info in the `User` format. See [User data format](#user-data-format) for more information.
- Sign the JWT with your secret key, using the EdDSA algorithm.
- Create a redirect URL back to the `/login/jwt-callback` path of your docs, including the JWT as the hash.

###

[​](#example-4)

Example

You host your documentation at `docs.foo.com` with an existing authentication system at `foo.com`. You want to extend your login flow to grant access to the docs while keeping your docs separate from your dashboard (or you don’t have a dashboard).Create a login endpoint at `https://foo.com/docs-login` that extends your existing authentication.After verifying user credentials:

- Generate a JWT with user data in Mintlify’s format.
- Sign the JWT and redirect to `https://docs.foo.com/login/jwt-callback#{SIGNED_JWT}`.

TypeScript

Python
```
import * as jose from 'jose';
import { Request, Response } from 'express';

const TWO_WEEKS_IN_MS = 1000 * 60 * 60 * 24 * 7 * 2;

const signingKey = await jose.importPKCS8(process.env.MINTLIFY_PRIVATE_KEY, 'EdDSA');

export async function handleRequest(req: Request, res: Response) {
  const user = {
    expiresAt: Math.floor((Date.now() + TWO_WEEKS_IN_MS) / 1000), // 2 week session expiration
    groups: res.locals.user.groups,
    apiPlaygroundInputs: {
      header: {
        "Authorization": `Bearer ${res.locals.user.apiKey}`,
      },
    },
  };

  const jwt = await new jose.SignJWT(user)
    .setProtectedHeader({ alg: 'EdDSA' })
    .setExpirationTime('10 s') // 10 second JWT expiration
    .sign(signingKey);

  return res.redirect(`https://docs.foo.com/login/jwt-callback#${jwt}`);
}
```

###

[​](#redirect-unauthenticated-users)

Redirect unauthenticated users

When an unauthenticated user tries to access a protected page, the redirect to your login URL preserves the user’s intended destination.

1.  User attempts to visit a protected page: `https://docs.foo.com/quickstart`.
2.  Redirect to your login URL with a redirect query parameter: `https://foo.com/docs-login?redirect=%2Fquickstart`.
3.  After authentication, redirect to `https://docs.foo.com/login/jwt-callback?redirect=%2Fquickstart#{SIGNED_JWT}`.
4.  User lands in their original destination.

##

[​](#make-pages-public)

Make pages public

When using authentication, all pages require authentication to access by default. You can make specific pages viewable without authentication at the page or group level with the `public` property.

###

[​](#individual-pages)

Individual pages

To make a page public, add `public: true` to the page’s frontmatter.

Public page example
```
---
title: "Public page"
public: true
---
```

###

[​](#groups-of-pages)

Groups of pages

To make all pages in a group public, add `"public": true` beneath the group’s name in the `navigation` object of your `docs.json`.

Public group example
```
{
  "navigation": {
    "groups": [
      {
        "group": "Public group",
        "public": true,
        "icon": "play",
        "pages": [
          "quickstart",
          "installation",
          "settings"
        ]
      },
      {
        "group": "Private group",
        "icon": "pause",
        "pages": [
          "private-information",
          "secret-settings"
        ]
      }
    ]
  }
}
```

##

[​](#control-access-with-groups)

Control access with groups

When you use OAuth or JWT authentication, you can restrict specific pages to certain user groups. This is useful when you want different users to see different content based on their role or attributes. Manage groups through user data passed during authentication. See [User data format](#user-data-format) for details.

Example user info
```
{
  "groups": ["admin", "beta-users"],
  "expiresAt": 1735689600
}
```
Specify which groups can access specific pages using the `groups` property in frontmatter.

Example page restricted to the admin group
```
---
title: "Admin dashboard"
groups: ["admin"]
---
```
Users must belong to at least one of the listed groups to access the page. If a user tries to access a page without the required group, they’ll receive a 404 error.

###

[​](#how-groups-interact-with-public-pages)

How groups interact with public pages

- All pages require authentication by default.
- Pages with a `groups` property are only accessible to authenticated users in those groups.
- Pages without a `groups` property are accessible to all authenticated users.
- Pages with `public: true` and no `groups` property are accessible to everyone.

Public page

Protected page

Protected page with groups
```
---
title: "Public guide"
public: true
---
```

##

[​](#user-data-format)

User data format

When using OAuth or JWT authentication, your system returns user data that controls session length, group membership, and [content personalization](https://www.mintlify.com/docs/create/personalization).

Format

Example
```
type User = {
  expiresAt?: number;
  groups?: string[];
  content?: Record<string, any>;
  apiPlaygroundInputs?: {
    server?: Record<string, string>;
    header?: Record<string, unknown>;
    query?: Record<string, unknown>;
    cookie?: Record<string, unknown>;
    path?: Record<string, unknown>;
  };
};
```
[​](#param-expires-at)

expiresAt

number

Session expiration time in seconds since epoch. When the current time passes this value, the user must re-authenticate.

**For JWT:** This differs from the JWT’s `exp` claim, which determines when a JWT is considered invalid. Set the JWT `exp` claim to a short duration (10 seconds or less) for security. Use `expiresAt` for the actual session length (hours to weeks).

[​](#param-groups)

groups

string\[\]

List of groups the user belongs to. Pages with matching `groups` in their frontmatter are accessible to this user.**Example**: A user with `groups: ["admin", "engineering"]` can access pages tagged with either the `admin` or `engineering` groups.

[​](#param-content)

content

Record<string, any>

Custom data accessible in MDX pages via the `user` variable for [personalized content](https://www.mintlify.com/docs/create/personalization#dynamic-mdx-content).

[​](#param-api-playground-inputs)

apiPlaygroundInputs

object

Pre-fills API playground fields with user-specific values. When a user authenticates, these values populate the corresponding input fields in the API playground. Users can override pre-filled values, and their overrides persist in local storage.Only values that match the current endpoint’s security scheme are applied.

Show properties

[​](#param-header)

header

Record<string, unknown>

Header values to pre-fill, keyed by header name.

[​](#param-query)

query

Record<string, unknown>

Query parameter values to pre-fill, keyed by parameter name.

[​](#param-cookie)

cookie

Record<string, unknown>

Cookie values to pre-fill, keyed by cookie name.

[​](#param-server)

server

Record<string, string>

Server variable values to pre-fill, keyed by variable name.

[​](#param-path)

path

Record<string, unknown>

Path parameter values to pre-fill, keyed by parameter name.

Was this page helpful?

YesNo

[Content Security Policy (CSP) configurationPrevious](https://www.mintlify.com/docs/deploy/csp-configuration)[Single sign-on (SSO)Next](https://www.mintlify.com/docs/dashboard/sso)

⌘I
