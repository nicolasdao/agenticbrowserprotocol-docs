---
url: https://mintlify.com/docs/deploy/route53-cloudfront
canonical: https://www.mintlify.com/docs/deploy/route53-cloudfront
title: "AWS Route 53 and CloudFront - Mintlify"
description: "Deploy documentation at a subpath on AWS with Route 53 DNS and CloudFront CDN."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

/docs subpath

AWS Route 53 and CloudFront

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

To host your documentation at a subpath such as `yoursite.com/docs` using AWS Route 53 and CloudFront, you must configure your DNS provider to point to your CloudFront distribution.

##

[​](#overview)

Overview

Route traffic to these paths with a Cache Policy of **CachingDisabled**:

- `/.well-known/acme-challenge/*` - Required for Let’s Encrypt certificate verification
- `/.well-known/vercel/*` - Required for domain verification
- `/docs/*` - Required for subpath routing
- `/docs/` - Required for subpath routing

Route traffic to this path with a Cache Policy of **CachingEnabled**:

- `/mintlify-assets/_next/static/*`
- `Default (*)` - Your website’s landing page

All Behaviors must have the an **origin request policy** of `AllViewerExceptHostHeader`. ![CloudFront "Behaviors" page with 4 behaviors: /docs/*, /docs, Default, and /.well-known/*.](https://mintcdn.com/mintlify/in3v2q9tGvWcAFWD/images/cloudfront/all-behaviors.png?fit=max&auto=format&n=in3v2q9tGvWcAFWD&q=85&s=666a7c785bcc7f6b2aa23424f8c1c668)

##

[​](#create-cloudfront-distribution)

Create CloudFront distribution

1.  Navigate to [CloudFront](https://aws.amazon.com/cloudfront) inside the AWS console.
2.  Select **Create distribution**.

![CloudFront Distributions page with the "Create distribution" button emphasized.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/create-distribution.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=cd402e36a077943e5de51319a2fba9c3)

3.  For the Origin domain, input `[SUBDOMAIN].mintlify.dev` where `[SUBDOMAIN]` is your project’s unique subdomain.

![CloudFront "Create distribution" page showing "acme.mintlify.dev" as the origin domain.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/origin-name.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=3bccb966a96cba7ec83364dabf5ba788)

4.  For “Web Application Firewall (WAF),” enable security protections.

![Web Application Firewall (WAF) options with "Enable security protections" selected.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/enable-security-protections.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=73a02de58bfbce884656443bb5d1ec42)

5.  The remaining settings should be default.
6.  Select **Create distribution**.

##

[​](#add-default-origin)

Add default origin

1.  After creating the distribution, navigate to the “Origins” tab.

![A CloudFront distribution with the "Origins" tab highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/cloudfront/origins.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=bbf7cd128d5fa29b2d957e224757d90c)

2.  Find your staging URL that mirrors the main domain. This is highly variant depending on how your landing page is hosted. For example, the Mintlify staging URL is [mintlify-landing-page.vercel.app](https://mintlify-landing-page.vercel.app).

If your landing page is hosted on Webflow, use Webflow’s staging URL. It would look like `.webflow.io`.If you use Vercel, use the `.vercel.app` domain available for every project.

3.  Create a new Origin and add your staging URL as the “Origin domain.”

![CloudFront "Create origin" page with a "Origin domain" input field highlighted.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/default-origin.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=c67257bc20e907ea4da1a8719fae0543)

By this point, you should have two Origins: one with `[SUBDOMAIN].mintlify.app` and another with your staging URL.

![CloudFront "Origins" page with two origins: One for mintlify and another for mintlify-landing-page.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/final-origins.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=c1fdd6d6e346e0e7b3a669daba284fba)

##

[​](#set-behaviors)

Set behaviors

Behaviors in CloudFront enable control over the subpath logic. At a high level, we’re looking to create the following logic:

- **If a user lands on your custom subpath**, go to `[SUBDOMAIN].mintlify.dev`.
- **If a user lands on any other page**, go the current landing page.

1.  Navigate to the “Behaviors” tab of your CloudFront distribution.

![CloudFront "Behaviors" tab highlighted.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/behaviors.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=6ab02a43a5427d2d1306dfd6d313bc49)

2.  Select the **Create behavior** button and create the following behaviors.

###

[​](#/-well-known/)

`/.well-known/*`

Create behaviors for Vercel domain verification paths with a **Path pattern** of `/.well-known/*` and set **Origin and origin groups** to your docs URL. For “Cache policy,” select **CachingDisabled** to ensure these verification requests pass through without caching.

![CloudFront "Create behavior" page with a "Path pattern" of "/.well-known/*" and "Origin and origin groups" pointing to the staging URL.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/cloudfront/well-known-policy.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=374fd2e53349cc9796515cda82a9b165)

If `.well-known/*` is too generic, it can be narrowed down to 2 behaviors at a minimum for Vercel:

- `/.well-known/vercel/*` - Required for Vercel domain verification
- `/.well-known/acme-challenge/*` - Required for Let’s Encrypt certificate verification

###

[​](#your-subpath)

Your subpath

Create a behavior with a **Path pattern** of your chosen subpath, for example `/docs`, with **Origin and origin groups** pointing to the `.mintlify.dev` URL (in our case `acme.mintlify.dev`).

- Set “Cache policy” to **CachingOptimized**.
- Set “Origin request policy” to **AllViewerExceptHostHeader**.
- Set Viewer Protocol Policy to **Redirect HTTP to HTTPS**

![CloudFront "Create behavior" page with a "Path pattern" of "/docs/*" and "Origin and origin groups" pointing to the acme.mintlify.dev URL.](https://mintcdn.com/mintlify/in3v2q9tGvWcAFWD/images/cloudfront/behavior-1.png?fit=max&auto=format&n=in3v2q9tGvWcAFWD&q=85&s=0ce9e6db0d16c0c095abf1bc44e68833)

###

[​](#your-subpath-with-wildcard)

Your subpath with wildcard

Create a behavior with a **Path pattern** of your chosen subpath followed by `/*`, for example `/docs/*`, and **Origin and origin groups** pointing to the same `.mintlify.dev` URL. These settings should exactly match your base subpath behavior. With the exception of the **Path pattern**.

- Set “Cache policy” to **CachingOptimized**.
- Set “Origin request policy” to **AllViewerExceptHostHeader**.
- Set “Viewer protocol policy” to **Redirect HTTP to HTTPS**

###

[​](#/mintlify-assets/_next/static/)

`/mintlify-assets/_next/static/*`

- Set “Cache policy” to **CachingOptimized**
- Set “Origin request policy” to **AllViewerExceptHostHeader**
- Set “Viewer protocol policy” to **Redirect HTTP to HTTPS**

###

[​](#default)

`Default (*)`

Lastly, we’re going to edit the `Default (*)` behavior.

![A CloudFront distribution with the "Default (*)" behavior selected and the Edit button emphasized.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/default-behavior-1.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=d1404011b4a312d88c7e523bbcf94316)

1.  Change the default behavior’s **Origin and origin groups** to the staging URL (in our case `mintlify-landing-page.vercel.app`).

![CloudFront "Edit behavior" page with the "Origin and origin groups" input field highlighted.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/default-behavior-2.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=3c81d60889bc1157954524865a0bde14)

2.  Select **Save changes**.

###

[​](#check-behaviors-are-set-up-correctly)

Check behaviors are set up correctly

If you follow the above steps, your behaviors should look like this:

![CloudFront "Behaviors" page with 4 behaviors: /docs/*, /docs, Default, and /.well-known/*.](https://mintcdn.com/mintlify/in3v2q9tGvWcAFWD/images/cloudfront/all-behaviors.png?fit=max&auto=format&n=in3v2q9tGvWcAFWD&q=85&s=666a7c785bcc7f6b2aa23424f8c1c668)

##

[​](#preview-distribution)

Preview distribution

You can now test if your distribution is set up properly by going to the “General” tab and visiting the **Distribution domain name** URL.

![CloudFront "General" tab with the "Distribution domain name" URL highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/cloudfront/preview-distribution.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=b7f0582640bb6650054c7b40ee9bdd57)

All pages should be directing to your main landing page, but if you append your chosen subpath, for example `/docs`, to the URL, you should see it going to your Mintlify documentation instance.

##

[​](#connect-with-route53)

Connect with Route53

Now, we’re going to bring the functionality of the CloudFront distribution into your primary domain.

For this section, you can also refer to AWS’s official guide on [Configuring Amazon Route 53 to route traffic to a CloudFront distribution](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-to-cloudfront-distribution.html#routing-to-cloudfront-distribution-config)

1.  Navigate to [Route53](https://aws.amazon.com/route53) inside the AWS console.
2.  Navigate to the “Hosted zone” for your primary domain.
3.  Select **Create record**.

![Route 53 "Records" page with the "Create record" button emphasized.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/cloudfront/route53-create-record.png?fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=27a00457e2401c2d55262291dda15579)

4.  Toggle `Alias` and then **Route traffic to** the `Alias to CloudFront distribution` option.

![Route 53 "Create record" page with the "Alias" toggle and the "Route traffic to" menu highlighted.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/create-record-alias.png?fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=cb7dbe0320f3f73233ed6452ac3b0372)

5.  Select **Create records**.

You may need to remove the existing A record if one currently exists.

Your documentation is now live at your chosen subpath for your primary domain.

After configuring your DNS, custom subdomains are usually available within a few minutes. DNS propagation can sometimes take 1-4 hours, and in rare cases up to 48 hours. If your subdomain is not immediately available, please wait before troubleshooting.

Was this page helpful?

YesNo

[CloudflarePrevious](https://www.mintlify.com/docs/deploy/cloudflare)[VercelNext](https://www.mintlify.com/docs/deploy/vercel)

⌘I

![CloudFront "Behaviors" page with 4 behaviors: /docs/*, /docs, Default, and /.well-known/*.](https://mintcdn.com/mintlify/in3v2q9tGvWcAFWD/images/cloudfront/all-behaviors.png?w=1650&fit=max&auto=format&n=in3v2q9tGvWcAFWD&q=85&s=c4a30fd51baf478014221afc66c7ac2a)

![CloudFront Distributions page with the "Create distribution" button emphasized.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/create-distribution.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=77d0f33cd3538e0945e392e3a7347aa3)

![CloudFront "Create distribution" page showing "acme.mintlify.dev" as the origin domain.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/origin-name.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=e1c482ddd1688c0b7b35f08a05ad8801)

![Web Application Firewall (WAF) options with "Enable security protections" selected.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/enable-security-protections.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=f859c34c5c459da088e65cf9d41fda5f)

![A CloudFront distribution with the "Origins" tab highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/cloudfront/origins.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=b3949751be07019ea134de611921bf8e)

![CloudFront "Create origin" page with a "Origin domain" input field highlighted.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/default-origin.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=8edb7f1a41443eda7cf820cabd9d9eb1)

![CloudFront "Origins" page with two origins: One for mintlify and another for mintlify-landing-page.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/final-origins.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=bf9804c4703342bc0de775f27ff55494)

![CloudFront "Behaviors" tab highlighted.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/behaviors.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=7ad8b32781d0e8cdb8c7d2fc7b7b6691)

![CloudFront "Create behavior" page with a "Path pattern" of "/.well-known/*" and "Origin and origin groups" pointing to the staging URL.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/cloudfront/well-known-policy.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=3659464f1ce1e75c49c2add0cc7c91ef)

![CloudFront "Create behavior" page with a "Path pattern" of "/docs/*" and "Origin and origin groups" pointing to the acme.mintlify.dev URL.](https://mintcdn.com/mintlify/in3v2q9tGvWcAFWD/images/cloudfront/behavior-1.png?w=1650&fit=max&auto=format&n=in3v2q9tGvWcAFWD&q=85&s=17211bee07269e1ca4e013a7e8414b8c)

![A CloudFront distribution with the "Default (*)" behavior selected and the Edit button emphasized.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/default-behavior-1.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=e049af02765251c8dc70f75871ce8646)

![CloudFront "Edit behavior" page with the "Origin and origin groups" input field highlighted.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/default-behavior-2.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=2b75a3d1bd5e7f728e6fc98dec394abd)

![CloudFront "Behaviors" page with 4 behaviors: /docs/*, /docs, Default, and /.well-known/*.](https://mintcdn.com/mintlify/in3v2q9tGvWcAFWD/images/cloudfront/all-behaviors.png?w=1650&fit=max&auto=format&n=in3v2q9tGvWcAFWD&q=85&s=c4a30fd51baf478014221afc66c7ac2a)

![CloudFront "General" tab with the "Distribution domain name" URL highlighted.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/cloudfront/preview-distribution.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=c0e9bf74112262191fd0c053f3a42a74)

![Route 53 "Records" page with the "Create record" button emphasized.](https://mintcdn.com/mintlify/GiucHIlvP3i5L17o/images/cloudfront/route53-create-record.png?w=1650&fit=max&auto=format&n=GiucHIlvP3i5L17o&q=85&s=7257b0f07303f69ad65e2af26ae20937)

![Route 53 "Create record" page with the "Alias" toggle and the "Route traffic to" menu highlighted.](https://mintcdn.com/mintlify/WXXCCJWDplNJgTwZ/images/cloudfront/create-record-alias.png?w=1650&fit=max&auto=format&n=WXXCCJWDplNJgTwZ&q=85&s=233ca4593b197c489cada291613333a3)
