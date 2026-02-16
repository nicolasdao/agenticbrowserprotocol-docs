---
url: https://mintlify.com/docs/deploy/csp-configuration
canonical: https://www.mintlify.com/docs/deploy/csp-configuration
title: "Content Security Policy (CSP) configuration - Mintlify"
description: "Configure CSP headers to allow Mintlify resources while maintaining security for reverse proxies, firewalls, and networks that enforce strict security policies."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

/docs subpath

Content Security Policy (CSP) configuration

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

    -   [Overview](https://www.mintlify.com/docs/deploy/docs-subpath)
    -   [Cloudflare](https://www.mintlify.com/docs/deploy/cloudflare)
    -   [AWS](https://www.mintlify.com/docs/deploy/route53-cloudfront)
    -   [Vercel](https://www.mintlify.com/docs/deploy/vercel)
    -   [Reverse proxy](https://www.mintlify.com/docs/deploy/reverse-proxy)
    -   [CSP configuration](https://www.mintlify.com/docs/deploy/csp-configuration)
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

Content Security Policy (CSP) is a security standard that helps prevent cross-site scripting (XSS) attacks by controlling which resources a web page can load. Mintlify serves a default CSP that protects most sites. If you host your documentation behind a reverse proxy or firewall, that overwrites the default CSP, you may need to configure CSP headers for features to function properly.

##

[​](#csp-directives)

CSP directives

The following CSP directives are used to control which resources can be loaded:

- `script-src`: Controls which scripts can be executed
- `style-src`: Controls which stylesheets can be loaded
- `font-src`: Controls which fonts can be loaded
- `img-src`: Controls which images, icons, and logos can be loaded
- `connect-src`: Controls which URLs can be connected to for API calls and WebSocket connections
- `frame-src`: Controls which URLs can be embedded in frames or iframes
- `default-src`: Fallback for other directives when not explicitly set

##

[​](#domain-whitelist)

Domain whitelist

| Domain | Purpose | CSP directive | Required |
| --- | --- | --- | --- |
| `d4tuoctqmanu0.cloudfront.net` | KaTeX CSS, fonts | `style-src`, `font-src` | Required |
| `*.mintlify.dev` | Documentation content | `connect-src`, `frame-src` | Required |
| `*.mintlify.com` | Dashboard, API, analytics proxy | `connect-src` | Required |
| `leaves.mintlify.com` | Assistant API | `connect-src` | Required |
| `d3gk2c5xim1je2.cloudfront.net` | Icons, images, logos | `img-src` | Required |
| `d1ctpt7j8wusba.cloudfront.net` | Mint version and release files | `connect-src` | Required |
| `mintcdn.com` | Images, favicons | `img-src`, `connect-src` | Required |
| `*.mintcdn.com` | Images, favicons | `img-src`, `connect-src` | Required |
| `api.mintlifytrieve.com` | Search API | `connect-src` | Required |
| `cdn.jsdelivr.net` | Emoji assets for OG images | `script-src`, `img-src` | Required |
| `mintlify.s3.us-west-1.amazonaws.com` | S3-hosted images | `img-src` | Required |
| `fonts.googleapis.com` | Google Fonts | `style-src`, `font-src` | Optional |
| `www.googletagmanager.com` | Google Analytics/GTM | `script-src`, `connect-src` | Optional |
| `cdn.segment.com` | Segment analytics | `script-src`, `connect-src` | Optional |
| `plausible.io` | Plausible analytics | `script-src`, `connect-src` | Optional |
| `us.posthog.com` | PostHog analytics | `connect-src` | Optional |
| `tag.clearbitscripts.com` | Clearbit tracking | `script-src` | Optional |
| `cdn.heapanalytics.com` | Heap analytics | `script-src` | Optional |
| `chat.cdn-plain.com` | Plain chat widget | `script-src` | Optional |
| `chat-assets.frontapp.com` | Front chat widget | `script-src` | Optional |
| `browser.sentry-cdn.com` | Sentry error tracking | `script-src`, `connect-src` | Optional |
| `js.sentry-cdn.com` | Sentry JavaScript SDK | `script-src` | Optional |

##

[​](#example-csp-configuration)

Example CSP configuration

Only include domains for services that you use. Remove any analytics domains that you have not configured for your documentation.
```
Content-Security-Policy:
default-src 'self';
script-src 'self' 'unsafe-inline' 'unsafe-eval' cdn.jsdelivr.net www.googletagmanager.com cdn.segment.com plausible.io
us.posthog.com tag.clearbitscripts.com cdn.heapanalytics.com chat.cdn-plain.com chat-assets.frontapp.com
browser.sentry-cdn.com js.sentry-cdn.com;
style-src 'self' 'unsafe-inline' d4tuoctqmanu0.cloudfront.net fonts.googleapis.com;
font-src 'self' d4tuoctqmanu0.cloudfront.net fonts.googleapis.com;
img-src 'self' data: blob: d3gk2c5xim1je2.cloudfront.net mintcdn.com *.mintcdn.com cdn.jsdelivr.net mintlify.s3.us-west-1.amazonaws.com;
connect-src 'self' *.mintlify.dev *.mintlify.com d1ctpt7j8wusba.cloudfront.net mintcdn.com *.mintcdn.com
api.mintlifytrieve.com www.googletagmanager.com cdn.segment.com plausible.io us.posthog.com browser.sentry-cdn.com;
frame-src 'self' *.mintlify.dev;
```

##

[​](#common-configurations-by-proxy-type)

Common configurations by proxy type

Most reverse proxies support adding custom headers.

###

[​](#cloudflare-configuration)

Cloudflare configuration

Create a Response Header Transform Rule:

1.  In your Cloudflare dashboard, go to **Rules > Overview**.
2.  Select **Create rule > Response Header Transform Rule**.
3.  Configure the rule:

- **Modify response header**: Set static
- **Header name**: `Content-Security-Policy`
- **Header value**:

    ```
    default-src 'self'; script-src 'self' 'unsafe-inline' 'unsafe-eval' cdn.jsdelivr.net; style-src 'self' 'unsafe-inline' d4tuoctqmanu0.cloudfront.net fonts.googleapis.com; font-src 'self' d4tuoctqmanu0.cloudfront.net fonts.googleapis.com; img-src 'self' data: blob: d3gk2c5xim1je2.cloudfront.net mintcdn.com *.mintcdn.com cdn.jsdelivr.net mintlify.s3.us-west-1.amazonaws.com; connect-src 'self' *.mintlify.dev *.mintlify.com d1ctpt7j8wusba.cloudfront.net mintcdn.com *.mintcdn.com api.mintlifytrieve.com; frame-src 'self' *.mintlify.dev;
    ```


4.  Deploy your rule.

###

[​](#aws-cloudfront-configuration)

AWS CloudFront configuration

Add a response headers policy in CloudFront:
```
{
"ResponseHeadersPolicy": {
    "Name": "MintlifyCSP",
    "Config": {
    "SecurityHeadersConfig": {
        "ContentSecurityPolicy": {
        "ContentSecurityPolicy": "default-src 'self'; script-src 'self' 'unsafe-inline' 'unsafe-eval' cdn.jsdelivr.net; style-src 'self' 'unsafe-inline' d4tuoctqmanu0.cloudfront.net fonts.googleapis.com; font-src 'self' d4tuoctqmanu0.cloudfront.net fonts.googleapis.com; img-src 'self' data: blob: d3gk2c5xim1je2.cloudfront.net mintcdn.com *.mintcdn.com cdn.jsdelivr.net mintlify.s3.us-west-1.amazonaws.com; connect-src 'self' *.mintlify.dev *.mintlify.com d1ctpt7j8wusba.cloudfront.net mintcdn.com *.mintcdn.com api.mintlifytrieve.com; frame-src 'self' *.mintlify.dev;",
        "Override": true
        }
      }
    }
  }
}
```

###

[​](#vercel-configuration)

Vercel configuration

Add to your `vercel.json`:
```
{
"headers": [
    {
    "source": "/(.*)",
    "headers": [
        {
        "key": "Content-Security-Policy",
        "value": "default-src 'self'; script-src 'self' 'unsafe-inline' 'unsafe-eval' cdn.jsdelivr.net; style-src 'self' 'unsafe-inline' d4tuoctqmanu0.cloudfront.net fonts.googleapis.com; font-src 'self' d4tuoctqmanu0.cloudfront.net fonts.googleapis.com; img-src 'self' data: blob: d3gk2c5xim1je2.cloudfront.net mintcdn.com *.mintcdn.com cdn.jsdelivr.net mintlify.s3.us-west-1.amazonaws.com; connect-src 'self' *.mintlify.dev *.mintlify.com d1ctpt7j8wusba.cloudfront.net mintcdn.com *.mintcdn.com api.mintlifytrieve.com; frame-src 'self' *.mintlify.dev;"
        }
      ]
    }
  ]
}
```

##

[​](#troubleshooting)

Troubleshooting

Identify CSP violations in your browser console:

1.  Open your browser’s Developer Tools.
2.  Go to the **Console** tab.
3.  Look for errors starting with:
    -   `Content Security Policy: The page's settings blocked the loading of a resource`
    -   `Refused to load the script/stylesheet because it violates the following Content Security Policy directive`
    -   `Refused to connect to because it violates the following Content Security Policy directive`

Was this page helpful?

YesNo

[Reverse proxyPrevious](https://www.mintlify.com/docs/deploy/reverse-proxy)[Authentication setupNext](https://www.mintlify.com/docs/deploy/authentication-setup)

⌘I
