---
url: https://mintlify.com/docs/create/image-embeds
canonical: https://www.mintlify.com/docs/create/image-embeds
title: "Images and embeds - Mintlify"
description: "Add images, videos, and iframes."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Create content

Images and embeds

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

Add images, embed videos, and include interactive content with iframes to your documentation.

![Photograph of a scenic landscape with purple flowers in the foreground, mountains in the background, and a blue sky with scattered clouds.](https://mintlify-assets.b-cdn.net/bigbend.jpg)

##

[​](#images)

Images

Add images to provide visual context, examples, or decoration to your documentation.

###

[​](#basic-image-syntax)

Basic image syntax

Use [Markdown syntax](https://www.markdownguide.org/basic-syntax/#images) to add images to your documentation:
```
![Alt text describing the image](/path/to/image.png)
```
Always include descriptive alt text to improve accessibility and SEO. The alt text should clearly describe what the image shows.

Image files must be less than 20 MB. For larger files, host them on a CDN service like [Amazon S3](https://aws.amazon.com/s3) or [Cloudinary](https://cloudinary.com).

###

[​](#html-image-embeds)

HTML image embeds

For more control over image display, use HTML `<img>` tags:
```
<img
  src="/images/dashboard.png"
  alt="Main dashboard interface"
  style={{height: "300px", width: "400px"}}
  className="rounded-lg"
/>
```

####

[​](#resize-images-with-inline-styles)

Resize images with inline styles

Use JSX inline styles with the `style` attribute to resize images:
```
<img
  src="/images/architecture.png"
  style={{width: "450px", height: "auto"}}
  alt="Diagram showing the architecture of the system"
/>
```

####

[​](#disable-image-zoom)

Disable image zoom

To disable the default zoom on click for images, add the `noZoom` property:
```
<img
  src="/images/screenshot.png"
  alt="Descriptive alt text"
  noZoom
/>
```

####

[​](#link-images)

Link images

To make an image a clickable link, wrap the image in an anchor tag and add the `noZoom` property:
```
<a href="https://mintlify.com" target="_blank">
  <img
    src="/images/logo.png"
    alt="Mintlify logo"
    noZoom
  />
</a>
```
Images within anchor tags automatically display a pointer cursor to indicate they are clickable.

####

[​](#light-and-dark-mode-images)

Light and dark mode images

To display different images for light and dark themes, use Tailwind CSS classes:
```
<!-- Light mode image -->
<img
  className="block dark:hidden"
  src="/images/light-mode.png"
  alt="Light mode interface"
/>

<!-- Dark mode image -->
<img
  className="hidden dark:block"
  src="/images/dark-mode.png"
  alt="Dark mode interface"
/>
```

###

[​](#svg-images)

SVG images

SVG files that use `foreignObject` elements render differently in production than in local development. Mintlify’s image CDN strips `foreignObject` from SVGs as a security measure, which can truncate or hide text and other embedded HTML content. This commonly affects SVGs exported from tools like [draw.io](https://www.drawio.com) that have HTML text formatting or word wrap turned on. To fix this, disable **Formatted Text** and **Word Wrap** on all labels in your diagram before exporting to SVG. See the [draw.io documentation](https://www.drawio.com/doc/faq/svg-export-text-problems) for more information on SVG exports.

##

[​](#videos)

Videos

Mintlify supports [HTML tags in Markdown](https://www.markdownguide.org/basic-syntax/#html), giving you flexibility to create rich content.

Always include fallback text content within video elements for browsers that don’t support video playback.

###

[​](#youtube-embeds)

YouTube embeds

Embed YouTube videos using iframe elements:
```
<iframe
  className="w-full aspect-video rounded-xl"
  src="https://www.youtube.com/embed/4KzFe50RQkQ"
  title="YouTube video player"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowFullScreen
></iframe>
```

###

[​](#self-hosted-videos)

Self-hosted videos

Use the HTML `<video>` element for self-hosted video content:
```
<video
  controls
  className="w-full aspect-video rounded-xl"
  src="link-to-your-video.com"
></video>
```

###

[​](#autoplay-videos)

Autoplay videos

To autoplay a video, use:
```
<video
  autoPlay
  muted
  loop
  playsInline
  className="w-full aspect-video rounded-xl"
  src="/videos/demo.mp4"
></video>
```
When using JSX syntax, write double-word attributes in camelCase: `autoPlay`, `playsInline`, `allowFullScreen`.

##

[​](#iframes)

iframes

Embed external content using iframe elements:
```
<iframe
  src="https://example.com/embed"
  title="Embedded content"
  className="w-full h-96 rounded-xl"
></iframe>
```

##

[​](#related-resources)

Related resources

[Frame component referenceLearn how to use the Frame component for presenting images.](https://www.mintlify.com/docs/components/frames)

Was this page helpful?

YesNo

[ViewPrevious](https://www.mintlify.com/docs/components/view)[FilesNext](https://www.mintlify.com/docs/create/files)

⌘I

![Photograph of a scenic landscape with purple flowers in the foreground, mountains in the background, and a blue sky with scattered clouds.](https://mintlify-assets.b-cdn.net/bigbend.jpg)
