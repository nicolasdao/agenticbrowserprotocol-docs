---
url: https://mintlify.com/docs/customize/custom-domain
canonical: https://www.mintlify.com/docs/customize/custom-domain
title: "Custom domain - Mintlify"
description: "Host your documentation on a custom domain."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Customize

Custom domain

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

To host your documentation on a custom domain:

1.  Add your domain in your dashboard.
2.  Configure DNS settings on your domain provider.
3.  Allow time for DNS to propagate and TLS certificates to be automatically provisioned.

Looking to set up a subpath like `example.com/docs`? See [/docs subpath](https://www.mintlify.com/docs/deploy/docs-subpath).

##

[​](#add-your-custom-domain)

Add your custom domain

1.  Navigate to the [Custom domain setup](https://dashboard.mintlify.com/settings/deployment/custom-domain) page in your dashboard.
2.  Enter your domain name. For example, `docs.example.com` or `www.example.com`.
3.  Click **Add domain**.

![The Custom domain setup page showing the field to enter your custom domain URL.](https://mintcdn.com/mintlify/Br3zUjMmXXI3_HaI/images/domain/add-custom-domain-light.png?fit=max&auto=format&n=Br3zUjMmXXI3_HaI&q=85&s=d8c8e3f4b035a6714614e52b173bf3f6)![The Custom domain setup page showing the field to enter your custom domain URL.](https://mintcdn.com/mintlify/Br3zUjMmXXI3_HaI/images/domain/add-custom-domain-dark.png?fit=max&auto=format&n=Br3zUjMmXXI3_HaI&q=85&s=d6b5b7f57c57ff72142613135e77cc98)

##

[​](#configure-your-dns)

Configure your DNS

1.  On your domain provider’s website, navigate to your domain’s DNS settings.
2.  Create a new DNS record with the following values:
```
CNAME | docs | cname.mintlify-dns.com.
```
Each domain provider has different ways to add DNS records. Refer to your domain provider’s documentation for specific instructions.

###

[​](#dns-propagation)

DNS propagation

DNS changes typically take 1-24 hours to propagate globally, though it can take up to 48 hours in some cases. You can verify your DNS is configured correctly using [DNSChecker](https://dnschecker.org). Once your DNS records are active, your documentation is first accessible via HTTP. HTTPS is available after Vercel provisions your TLS certificate.

###

[​](#automatic-tls-provisioning)

Automatic TLS provisioning

Once your DNS records propagate and resolve correctly, Vercel automatically provisions a free SSL/TLS certificate for your domain using Let’s Encrypt. This typically completes within a few hours of DNS propagation, though it can take up to 24 hours in rare cases. Certificates are automatically renewed before expiration.

###

[​](#caa-records)

CAA records

If your domain uses CAA (Certification Authority Authorization) records, you must authorize Let’s Encrypt to issue certificates for your domain. Add the following CAA record to your DNS settings:
```
0 issue "letsencrypt.org"
```

###

[​](#reserved-paths)

Reserved paths

The `/.well-known/acme-challenge` path is reserved for certificate validation and cannot be redirected or rewritten. If you have configured redirects or rewrites for this path, certificate provisioning will fail.

###

[​](#provider-specific-settings)

Provider-specific settings

Vercel verification

If Vercel is your domain provider, you must add a verification `TXT` record. This information appears on your dashboard after submitting your custom domain, and is emailed to you.

Cloudflare encryption mode

If Cloudflare is your DNS provider, you must enable the “Full (strict)” mode for the SSL/TLS encryption setting. Additionally, disable “Always Use HTTPS” in your Edge Certificates settings. Cloudflare’s HTTPS redirect will block Let’s Encrypt from validating your domain during certificate provisioning.

##

[​](#set-a-canonical-url)

Set a canonical URL

After configuring your DNS, set a canonical URL to ensure search engines index your preferred domain. A canonical URL tells search engines which version of your documentation is the primary one. This improves SEO when your documentation is accessible from multiple URLs and prevents issues with duplicate content. Add the `canonical` meta tag to your `docs.json`:
```
"seo": {
    "metatags": {
        "canonical": "https://www.your-custom-domain-here.com"
    }
}
```
Replace `https://www.your-custom-domain-here.com` with your actual custom domain. For example, if your custom domain is `docs.mintlify.com`, you would use:
```
"seo": {
    "metatags": {
        "canonical": "https://docs.mintlify.com"
    }
}
```
Was this page helpful?

YesNo

[Exclude files from publishingPrevious](https://www.mintlify.com/docs/organize/mintignore)[ThemesNext](https://www.mintlify.com/docs/customize/themes)

⌘I

![The Custom domain setup page showing the field to enter your custom domain URL.](https://mintcdn.com/mintlify/Br3zUjMmXXI3_HaI/images/domain/add-custom-domain-dark.png?w=1650&fit=max&auto=format&n=Br3zUjMmXXI3_HaI&q=85&s=11c3173d0becd05b6fceb19faa52940d)
