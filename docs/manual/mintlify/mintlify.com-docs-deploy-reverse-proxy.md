---
url: https://mintlify.com/docs/deploy/reverse-proxy
canonical: https://www.mintlify.com/docs/deploy/reverse-proxy
title: "Reverse proxy - Mintlify"
description: "Configure a custom reverse proxy to serve your documentation."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

/docs subpath

Reverse proxy

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

Reverse proxy configurations are only supported for [Enterprise plans](https://mintlify.com/pricing?ref=reverse-proxy).

To serve your documentation through a custom reverse proxy, you must configure routing rules, caching policies, and header forwarding. When you implement a reverse proxy, monitor for potential issues with domain verification, SSL certificate provisioning, authentication flows, performance, and analytics tracking.

##

[​](#choose-your-deployment-approach)

Choose your deployment approach

Mintlify supports two reverse proxy configurations depending on your subpath requirements.

- **Host at `/docs`**: Use `mintlify.dev` as the proxy target. Enable the **Host at `/docs`** toggle on the [Custom domain setup](https://dashboard.mintlify.com/settings/deployment/custom-domain) page in your dashboard. This is a simpler configuration with fewer routes.
- **Custom subpath**: Use `mintlify.app` as the proxy target. This approach supports any subpath and requires additional routing rules.

##

[​](#host-at-/docs-subpath)

Host at `/docs` subpath

Use this configuration when you want to serve documentation at the `/docs` path on your domain. Before configuring your reverse proxy:

1.  Navigate to [Custom domain setup](https://dashboard.mintlify.com/settings/deployment/custom-domain) in your dashboard.
2.  Enable the **Host at `/docs`** toggle.
3.  Enter your domain and select **Add domain**.

When you enable **Host at `/docs`**, your canonical docs URL becomes `<your-subdomain>.mintlify.dev`. Cache invalidation stops on `mintlify.app`, and you must proxy to `mintlify.dev` for updates to appear.

###

[​](#routing-configuration)

Routing configuration

Proxy these paths to your Mintlify subdomain:

| Path | Destination | Caching |
| --- | --- | --- |
| `/docs` | `<your-subdomain>.mintlify.dev/docs` | No cache |
| `/docs/*` | `<your-subdomain>.mintlify.dev/docs` | No cache |
| `/.well-known/vercel/*` | `<your-subdomain>.mintlify.dev` | No cache |
| `/.well-known/skills/*` (optional) | `<your-subdomain>.mintlify.dev/docs` | No cache |
| `/skill.md` (optional) | `<your-subdomain>.mintlify.dev/docs` | No cache |

The `/.well-known/skills/*` and `/skill.md` routes are optional. Include them only if you want to serve AI skills files at root paths like `your-domain.com/skills.md` instead of under your docs subpath like `your-domain.com/docs/skills.md`.

###

[​](#required-header-configuration)

Required header configuration

Configure your reverse proxy with these header requirements:

- **Origin**: Contains the target subdomain `<your-subdomain>.mintlify.dev`
- **X-Forwarded-For**: Preserves client IP information
- **X-Forwarded-Proto**: Preserves original protocol (http/https)
- **X-Real-IP**: Forwards the real client IP address
- **User-Agent**: Forwards the user agent

Ensure that the `Host` header is not forwarded.

###

[​](#example-nginx-configuration)

Example nginx configuration
```
server {
    listen 80;
    server_name <your-domain>.com;

    # Vercel verification paths
    location ~ ^/\.well-known/vercel/ {
        proxy_pass https://<your-subdomain>.mintlify.dev;
        proxy_set_header Origin <your-subdomain>.mintlify.dev;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        add_header Cache-Control "no-cache, no-store, must-revalidate";
    }

    # AI skills paths
    location ^~ /.well-known/skills/ {
        proxy_pass https://<your-subdomain>.mintlify.dev/docs;
        proxy_set_header Origin <your-subdomain>.mintlify.dev;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        add_header Cache-Control "no-cache, no-store, must-revalidate";
    }

    # Skill manifest (optional)
    location = /skill.md {
        proxy_pass https://<your-subdomain>.mintlify.dev/docs;
        proxy_set_header Origin <your-subdomain>.mintlify.dev;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        add_header Cache-Control "no-cache, no-store, must-revalidate";
    }

    # Documentation root
    location = /docs {
        proxy_pass https://<your-subdomain>.mintlify.dev/docs;
        proxy_set_header Origin <your-subdomain>.mintlify.dev;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        add_header Cache-Control "no-cache, no-store, must-revalidate";
    }

    # All documentation paths
    location /docs/ {
        proxy_pass https://<your-subdomain>.mintlify.dev/docs/;
        proxy_set_header Origin <your-subdomain>.mintlify.dev;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        add_header Cache-Control "no-cache, no-store, must-revalidate";
    }
}
```

##

[​](#custom-subpath)

Custom subpath

When you need a subpath other than `/docs` (such as `/help` or `/resources`), use the following routing configuration. Proxy these paths to your Mintlify subdomain with the specified caching policies:

| Path | Destination | Caching |
| --- | --- | --- |
| `/.well-known/vercel/*` | `<your-subdomain>.mintlify.app` | No cache |
| `/.well-known/skills/*` | `<your-subdomain>.mintlify.app` | No cache |
| `/skill.md` | `<your-subdomain>.mintlify.app` | No cache |
| `/mintlify-assets/_next/static/*` | `<your-subdomain>.mintlify.app` | Cache enabled |
| `/_mintlify/*` | `<your-subdomain>.mintlify.app` | No cache |
| `/*` | `<your-subdomain>.mintlify.app` | No cache |
| `/` | `<your-subdomain>.mintlify.app` | No cache |

###

[​](#required-header-configuration-2)

Required header configuration

Configure your reverse proxy with these header requirements:

- **Origin**: Contains the target subdomain `<your-subdomain>.mintlify.app`
- **X-Forwarded-For**: Preserves client IP information
- **X-Forwarded-Proto**: Preserves original protocol (HTTP/HTTPS)
- **X-Real-IP**: Forwards the real client IP address
- **User-Agent**: Forwards the user agent

Ensure that the `Host` header is not forwarded

###

[​](#example-nginx-configuration-2)

Example nginx configuration
```
server {
    listen 80;
    server_name <your-domain>.com;

    # Vercel verification paths
    location ~ ^/\.well-known/vercel/ {
        proxy_pass https://<your-subdomain>.mintlify.app;
        proxy_set_header Origin <your-subdomain>.mintlify.app;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        # Disable caching for verification paths
        add_header Cache-Control "no-cache, no-store, must-revalidate";
    }

    # AI skills paths
    location ^~ /.well-known/skills/ {
        proxy_pass https://<your-subdomain>.mintlify.app;
        proxy_set_header Origin <your-subdomain>.mintlify.app;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        # Disable caching for verification paths
        add_header Cache-Control "no-cache, no-store, must-revalidate";
    }

    # Skill manifest
    location = /skill.md {
        proxy_pass https://<your-subdomain>.mintlify.app;
        proxy_set_header Origin <your-subdomain>.mintlify.app;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        # Disable caching for skill manifest
        add_header Cache-Control "no-cache, no-store, must-revalidate";
    }

    # Static assets with caching
    location ~ ^/mintlify-assets/_next/static/ {
        proxy_pass https://<your-subdomain>.mintlify.app;
        proxy_set_header Origin <your-subdomain>.mintlify.app;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        # Enable caching for static assets
        add_header Cache-Control "public, max-age=86400";
    }

    # Mintlify-specific paths
    location ~ ^/_mintlify/ {
        proxy_pass https://<your-subdomain>.mintlify.app;
        proxy_set_header Origin <your-subdomain>.mintlify.app;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        # Disable caching for Mintlify paths
        add_header Cache-Control "no-cache, no-store, must-revalidate";
    }

    # Root path
    location = / {
        proxy_pass https://<your-subdomain>.mintlify.app;
        proxy_set_header Origin <your-subdomain>.mintlify.app;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        # Disable caching for dynamic content
        add_header Cache-Control "no-cache, no-store, must-revalidate";
    }

    # All other documentation paths
    location / {
        proxy_pass https://<your-subdomain>.mintlify.app;
        proxy_set_header Origin <your-subdomain>.mintlify.app;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_set_header User-Agent $http_user_agent;

        # Disable caching for dynamic content
        add_header Cache-Control "no-cache, no-store, must-revalidate";
    }
}
```

##

[​](#troubleshooting)

Troubleshooting

###

[​](#changes-not-appearing)

Changes not appearing

**Symptoms**: You publish documentation updates, but the changes don’t appear on your site. **Cause**: You have **Host at `/docs`** enabled in your dashboard but your reverse proxy points to `mintlify.app` instead of `mintlify.dev`. **Solution**: Update your reverse proxy configuration to point to `<your-subdomain>.mintlify.dev` instead of `<your-subdomain>.mintlify.app`.

###

[​](#404-error)

404 error

**Symptoms**: Documentation loads, but features don’t work. API calls fail. **Cause**: The reverse proxy forwards the `Host` header or the `Origin` header is missing. **Solution**:

- Remove `Host` header forwarding
- Set `Origin` header to your Mintlify subdomain (`mintlify.dev` for a `/docs` subpath or `mintlify.app` for a different subpath)

###

[​](#performance-issues)

Performance issues

**Symptoms**: Slow page loads and layout shifts. **Cause**: Incorrect caching configuration. **Solution**: For custom subpath configurations, enable caching only for `/mintlify-assets/_next/static/*` paths. The `/docs` subpath configuration handles caching automatically.

Was this page helpful?

YesNo

[VercelPrevious](https://www.mintlify.com/docs/deploy/vercel)[Content Security Policy (CSP) configurationNext](https://www.mintlify.com/docs/deploy/csp-configuration)

⌘I
