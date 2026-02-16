---
url: https://mintlify.com/docs/deploy/vercel
canonical: https://www.mintlify.com/docs/deploy/vercel
title: "Vercel - Mintlify"
description: "Deploy documentation to a subpath on Vercel."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

/docs subpath

Vercel

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

Configure your `vercel.json` file to proxy requests from your main domain to your documentation at a subpath.

##

[​](#vercel-json-file)

vercel.json file

The `vercel.json` file configures how your project builds and deploys. It sits in your project’s root directory and controls various aspects of your deployment, including routing, redirects, headers, and build settings. We use the `rewrites` configuration in your `vercel.json` file to proxy requests from your main domain to your documentation. Rewrites map incoming requests to different destinations without changing the URL in the browser. When someone visits `yoursite.com/docs`, Vercel internally fetches content from `your-subdomain.mintlify.dev/docs`, but the user still sees `yoursite.com/docs` in their browser. This is different from redirects, which send users to another URL entirely.

##

[​](#configuration)

Configuration

###

[​](#host-at-/docs-subpath)

Host at `/docs` subpath

1.  Navigate to [Custom domain setup](https://dashboard.mintlify.com/settings/deployment/custom-domain) in your dashboard.
2.  Click the **Host at `/docs`** toggle to the on position.

    ![Screenshot of the Custom domain setup page. The Host at `/docs` toggle is on and highlighted by an orange rectangle.](https://mintcdn.com/mintlify/y0I2fgo5Rzv873ju/images/subpath/toggle-light.png?fit=max&auto=format&n=y0I2fgo5Rzv873ju&q=85&s=7e32943b9dd517e21030678381a60b40)![Screenshot of the Custom domain setup page. The Host at `/docs` toggle is on and highlighted by an orange rectangle.](https://mintcdn.com/mintlify/y0I2fgo5Rzv873ju/images/subpath/toggle-dark.png?fit=max&auto=format&n=y0I2fgo5Rzv873ju&q=85&s=9e0fd7047a7937d5a6d9cfc2c55acb09)

3.  Enter your domain.
4.  Select **Add domain**.
5.  Add the following rewrites to your `vercel.json` file. Replace `[subdomain]` with your subdomain, which is found at the end of your dashboard URL. For example, `dashboard.mintlify.com/your-organization/your-subdomain` has a domain identifier of `your-subdomain`.

    ```
    {
      "rewrites": [
        {
          "source": "/docs",
          "destination": "https://[subdomain].mintlify.dev/docs"
        },
        {
          "source": "/docs/:match*",
          "destination": "https://[subdomain].mintlify.dev/docs/:match*"
        }
      ]
    }
    ```


The `rewrites` configuration maps the `/docs` subpath on your domain to the `/docs` subpath on your documentation.

- **`source`**: The path pattern on your domain that triggers the rewrite.
- **`destination`**: Where the request should be proxied to.
- **`:match*`**: A wildcard that captures any path segments after your subpath.

For more information, see [Configuring projects with vercel.json: Rewrites](https://vercel.com/docs/projects/project-configuration#rewrites) in the Vercel documentation.

###

[​](#host-at-custom-subpath)

Host at custom subpath

To use a custom subpath (any path other than `/docs`), you must organize your documentation files within your repository to match your subpath structure. For example, if your documentation is hosted at `yoursite.com/help`, your documentation files must be in a `help/` directory. Use the generator below to create your rewrites configuration. Add the rewrites to your `vercel.json` file.

Subdomain

Subpath

Copy
```
{
  "rewrites": [
    {
      "source": "/_mintlify/:path*",
      "destination": "https://[SUBDOMAIN].mintlify.app/_mintlify/:path*"
    },
    {
      "source": "/api/request",
      "destination": "https://[SUBDOMAIN].mintlify.app/_mintlify/api/request"
    },
    {
      "source": "/[SUBPATH]",
      "destination": "https://[SUBDOMAIN].mintlify.app/[SUBPATH]"
    },
    {
      "source": "/[SUBPATH]/llms.txt",
      "destination": "https://[SUBDOMAIN].mintlify.app/llms.txt"
    },
    {
      "source": "/[SUBPATH]/llms-full.txt",
      "destination": "https://[SUBDOMAIN].mintlify.app/llms-full.txt"
    },
    {
      "source": "/[SUBPATH]/sitemap.xml",
      "destination": "https://[SUBDOMAIN].mintlify.app/sitemap.xml"
    },
    {
      "source": "/[SUBPATH]/robots.txt",
      "destination": "https://[SUBDOMAIN].mintlify.app/robots.txt"
    },
    {
      "source": "/[SUBPATH]/mcp",
      "destination": "https://[SUBDOMAIN].mintlify.app/mcp"
    },
    {
      "source": "/[SUBPATH]/:path*",
      "destination": "https://[SUBDOMAIN].mintlify.app/[SUBPATH]/:path*"
    },
    {
      "source": "/mintlify-assets/:path+",
      "destination": "https://[SUBDOMAIN].mintlify.app/mintlify-assets/:path+"
    }
  ]
}
```
Was this page helpful?

YesNo

[AWS Route 53 and CloudFrontPrevious](https://www.mintlify.com/docs/deploy/route53-cloudfront)[Reverse proxyNext](https://www.mintlify.com/docs/deploy/reverse-proxy)

⌘I

![Screenshot of the Custom domain setup page. The Host at `/docs` toggle is on and highlighted by an orange rectangle.](https://mintcdn.com/mintlify/y0I2fgo5Rzv873ju/images/subpath/toggle-dark.png?w=1650&fit=max&auto=format&n=y0I2fgo5Rzv873ju&q=85&s=f2b3176eb3af0ac276f8255973ae57ab)
