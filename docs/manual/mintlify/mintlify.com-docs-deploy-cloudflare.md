---
url: https://mintlify.com/docs/deploy/cloudflare
canonical: https://www.mintlify.com/docs/deploy/cloudflare
title: "Cloudflare - Mintlify"
description: "Host documentation at a subpath on Cloudflare Workers."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

/docs subpath

Cloudflare

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

To host your documentation at a subpath such as `yoursite.com/docs` using Cloudflare, you must create and configure a Cloudflare Worker.

Before you begin, you need a Cloudflare account and a domain name (can be managed on or off Cloudflare).

##

[​](#set-up-a-cloudflare-worker)

Set up a Cloudflare Worker

Create a Cloudflare Worker by following the [Cloudflare Workers getting started guide](https://developers.cloudflare.com/workers/get-started/dashboard/), if you have not already.

If your DNS provider is Cloudflare, disable proxying for the CNAME record to avoid potential configuration issues.

###

[​](#proxies-with-vercel-deployments)

Proxies with Vercel deployments

If you use Cloudflare as a proxy with Vercel deployments, you must ensure proper configuration to avoid conflicts with Vercel’s domain verification and SSL certificate provisioning. Improper proxy configuration can prevent Vercel from provisioning Let’s Encrypt SSL certificates and cause domain verification failures.

####

[​](#required-path-allowlist)

Required path allowlist

Your Cloudflare Worker must allow traffic to these specific paths without blocking or redirecting:

- `/.well-known/acme-challenge/*` - Required for Let’s Encrypt certificate verification
- `/.well-known/vercel/*` - Required for Vercel domain verification

While Cloudflare automatically handles many verification rules, creating additional custom rules may inadvertently block this critical traffic.

####

[​](#header-forwarding-requirements)

Header forwarding requirements

Ensure that the `HOST` header is correctly forwarded in your Worker configuration. Failure to properly forward headers will cause verification requests to fail.

###

[​](#configure-routing)

Configure routing

In your Cloudflare dashboard, select **Edit Code** and add the following script into your Worker’s code. See the [Cloudflare documentation](https://developers.cloudflare.com/workers-ai/get-started/dashboard/#development) for more information on editing a Worker.

Replace `[SUBDOMAIN]` with your unique subdomain, `[YOUR_DOMAIN]` with your website’s base URL, and `/docs` with your desired subpath if different.
```
addEventListener("fetch", (event) => {
  event.respondWith(handleRequest(event.request));
});

async function handleRequest(request) {
  try {
    const urlObject = new URL(request.url);

    // If the request is to a Vercel verification path, allow it to pass through
    if (urlObject.pathname.startsWith('/.well-known/')) {
      return await fetch(request);
    }

    // If the request is to the docs subpath
    if (/^\/docs/.test(urlObject.pathname)) {
      // Then Proxy to Mintlify
      const DOCS_URL = "[SUBDOMAIN].mintlify.dev";
      const CUSTOM_URL = "[YOUR_DOMAIN]";

      let url = new URL(request.url);
      url.hostname = DOCS_URL;

      let proxyRequest = new Request(url, request);

      proxyRequest.headers.set("Host", DOCS_URL);
      proxyRequest.headers.set("X-Forwarded-Host", CUSTOM_URL);
      proxyRequest.headers.set("X-Forwarded-Proto", "https");
      // If deploying to Vercel, preserve client IP
      proxyRequest.headers.set("CF-Connecting-IP", request.headers.get("CF-Connecting-IP"));

      return await fetch(proxyRequest);
    }
  } catch (error) {
    // If no action found, play the regular request
    return await fetch(request);
  }
}
```
Select **Deploy** and wait for the changes to propagate.

After configuring your DNS, custom subdomains are usually available within a few minutes. DNS propagation can sometimes take 1-4 hours, and in rare cases up to 48 hours. If your subdomain is not immediately available, please wait before troubleshooting.

###

[​](#test-your-worker)

Test your Worker

After your code deploys, test your Worker to ensure it routes to your Mintlify docs.

1.  Test using the Worker’s preview URL: `your-worker.your-subdomain.workers.dev/docs`
2.  Verify the Worker routes to your Mintlify docs and your website.

###

[​](#add-custom-domain)

Add custom domain

1.  In your [Cloudflare dashboard](https://dash.cloudflare.com/), navigate to your Worker.
2.  Go to **Settings > Domains & Routes > Add > Custom Domain**.
3.  Add your domain.

We recommend you add your domain both with and without `www.` prepended.

See [Add a custom domain](https://developers.cloudflare.com/workers/configuration/routing/custom-domains/#add-a-custom-domain) in the Cloudflare documentation for more information.

###

[​](#resolve-dns-conflicts)

Resolve DNS conflicts

If your domain already points to another service, you must remove the existing DNS record. Your Cloudflare Worker must be configured to control all traffic for your domain.

1.  Delete the existing DNS record for your domain. See [Delete DNS records](https://developers.cloudflare.com/dns/manage-dns-records/how-to/create-dns-records/#delete-dns-records) in the Cloudflare documentation for more information.
2.  Return to your Worker and add your custom domain.

##

[​](#webflow-custom-routing)

Webflow custom routing

If you use Webflow to host your main site and want to serve Mintlify docs at `/docs` on the same domain, you’ll need to configure custom routing through Cloudflare Workers to proxy all non-docs traffic to your main site.

Make sure your main site is set up on a landing page before deploying this Worker, or visitors to your main site will see errors.

1.  In Webflow, set up a landing page for your main site like `landing.yoursite.com`. This will be the page that visitors see when they visit your site.
2.  Deploy your main site to the landing page. This ensures that your main site remains accessible while you configure the Worker.
3.  To avoid conflicts, update any absolute URLs in your main site to be relative.
4.  In Cloudflare, select **Edit Code** and add the following script into your Worker’s code.

Replace `[SUBDOMAIN]` with your unique subdomain, `[YOUR_DOMAIN]` with your website’s base URL, `[LANDING_DOMAIN]` with your landing page URL, and `/docs` with your desired subpath if different.
```
addEventListener("fetch", (event) => {
event.respondWith(handleRequest(event.request));
});
async function handleRequest(request) {
try {
  const urlObject = new URL(request.url);

  // If the request is to a Vercel verification path, allow it to pass through
  if (urlObject.pathname.startsWith('/.well-known/')) {
    return await fetch(request);
  }

  // If the request is to the docs subpath
  if (/^\/docs/.test(urlObject.pathname)) {
    // Proxy to Mintlify
    const DOCS_URL = "[SUBDOMAIN].mintlify.dev";
    const CUSTOM_URL = "[YOUR_DOMAIN]";
    let url = new URL(request.url);
    url.hostname = DOCS_URL;
    let proxyRequest = new Request(url, request);
    proxyRequest.headers.set("Host", DOCS_URL);
    proxyRequest.headers.set("X-Forwarded-Host", CUSTOM_URL);
    proxyRequest.headers.set("X-Forwarded-Proto", "https");
    // If deploying to Vercel, preserve client IP
    proxyRequest.headers.set("CF-Connecting-IP", request.headers.get("CF-Connecting-IP"));
    return await fetch(proxyRequest);
  }
  // Route everything else to main site
  const MAIN_SITE_URL = "[LANDING_DOMAIN]";
  if (MAIN_SITE_URL && MAIN_SITE_URL !== "[LANDING_DOMAIN]") {
    let mainSiteUrl = new URL(request.url);
    mainSiteUrl.hostname = MAIN_SITE_URL;
    return await fetch(mainSiteUrl, {
      method: request.method,
      headers: request.headers,
      body: request.body
    });
  }
} catch (error) {
  // If no action found, serve the regular request
  return await fetch(request);
}
}
```
5.  Select **Deploy** and wait for the changes to propagate.

After configuring your DNS, custom subdomains are usually available within a few minutes. DNS propagation can sometimes take 1-4 hours, and in rare cases up to 48 hours. If your subdomain is not immediately available, please wait before troubleshooting.

Was this page helpful?

YesNo

[OverviewPrevious](https://www.mintlify.com/docs/deploy/docs-subpath)[AWS Route 53 and CloudFrontNext](https://www.mintlify.com/docs/deploy/route53-cloudfront)

⌘I
