---
url: https://mintlify.com/docs/customize/custom-scripts
canonical: https://www.mintlify.com/docs/customize/custom-scripts
title: "Custom scripts - Mintlify"
description: "Add custom JavaScript and CSS to fully customize the look and feel of your documentation."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Customize

Custom scripts

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

Use CSS to style HTML elements or add custom CSS and JavaScript to fully customize the look and feel of your documentation.

##

[​](#styling-with-tailwind-css)

Styling with Tailwind CSS

Use Tailwind CSS v3 to style HTML elements. You can control layout, spacing, colors, and other visual properties. Some common classes are:

- `w-full` - Full width
- `aspect-video` - 16:9 aspect ratio
- `rounded-xl` - Large rounded corners
- `block`, `hidden` - Display control
- `dark:hidden`, `dark:block` - Dark mode visibility

Tailwind CSS arbitrary values are not supported. For custom values, use the `style` prop instead.
```
<img style={{ width: '350px', margin: '12px auto' }} src="/path/image.jpg" />
```
Using the `style` prop can cause a layout shift on page load, especially on custom mode pages. Use Tailwind CSS classes or custom CSS files instead to avoid shifts or flickering.

##

[​](#custom-css)

Custom CSS

Add CSS files to your repository and their defined class names will be applied and available in all of your MDX files.

###

[​](#adding-style-css)

Adding `style.css`

For example, you can add the following `style.css` file to customize the styling of the navbar and footer.
```
#navbar {
  background: #fffff2;
  padding: 1rem;
}

footer {
  margin-top: 2rem;
}
```

###

[​](#using-identifiers-and-selectors)

Using identifiers and selectors

Mintlify has a set of common identifiers and selectors to help you tag important elements of the UI.

Use inspect element to find references to elements you’re looking to customize.

Identifiers

- APIPlaygroundInput: `api-playground-input`
- AssistantEntry: `assistant-entry`
- AssistantEntryMobile: `assistant-entry-mobile`
- Banner: `banner`
- BodyContent: `body-content`
- ChangelogFilters: `changelog-filters`
- ChangelogFiltersContent: `changelog-filters-content`
- ChatAssistantSheet: `chat-assistant-sheet`
- ChatAssistantTextArea: `chat-assistant-textarea`
- ContentArea: `content-area`
- ContentContainer: `content-container`
- ContentSideLayout: `content-side-layout`
- FeedbackForm: `feedback-form`
- FeedbackFormCancel: `feedback-form-cancel`
- FeedbackFormInput: `feedback-form-input`
- FeedbackFormSubmit: `feedback-form-submit`
- FeedbackThumbsDown: `feedback-thumbs-down`
- FeedbackThumbsUp: `feedback-thumbs-up`
- Footer: `footer`
- Header: `header`
- NavBarTransition: `navbar-transition`
- NavigationItems: `navigation-items`
- Navbar: `navbar`
- PageContextMenu: `page-context-menu`
- PageContextMenuButton: `page-context-menu-button`
- PageTitle: `page-title`
- Pagination: `pagination`
- Panel: `panel`
- RequestExample: `request-example`
- ResponseExample: `response-example`
- SearchBarEntry: `search-bar-entry`
- SearchBarEntryMobile: `search-bar-entry-mobile`
- SearchInput: `search-input`
- Sidebar: `sidebar`
- SidebarContent: `sidebar-content`
- TableOfContents: `table-of-contents`
- TableOfContentsContent: `table-of-contents-content`
- TableOfContentsLayout: `table-of-contents-layout`
- TopbarCtaButton: `topbar-cta-button`

Selectors

- Accordion: `accordion`
- AccordionGroup: `accordion-group`
- AlmondLayout: `almond-layout`
- AlmondNavBottomSection: `almond-nav-bottom-section`
- AlmondNavBottomSectionDivider: `almond-nav-bottom-section-divider`
- Anchor: `nav-anchor`
- Anchors: `nav-anchors`
- APISection: `api-section`
- APISectionHeading: `api-section-heading`
- APISectionHeadingSubtitle: `api-section-heading-subtitle`
- APISectionHeadingTitle: `api-section-heading-title`
- Callout: `callout`
- Card: `card`
- CardGroup: `card-group`
- ChatAssistantSheet: `chat-assistant-sheet`
- ChatAssistantSheetHeader: `chat-assistant-sheet-header`
- ChatAssistantSheetContent: `chat-assistant-sheet-content`
- ChatAssistantInput: `chat-assistant-input`
- ChatAssistantSendButton: `chat-assistant-send-button`
- CodeBlock: `code-block`
- CodeGroup: `code-group`
- Content: `mdx-content`
- DropdownTrigger: `nav-dropdown-trigger`
- DropdownContent: `nav-dropdown-content`
- DropdownItem: `nav-dropdown-item`
- DropdownItemTextContainer: `nav-dropdown-item-text-container`
- DropdownItemTitle: `nav-dropdown-item-title`
- DropdownItemDescription: `nav-dropdown-item-description`
- DropdownItemIcon: `nav-dropdown-item-icon`
- Expandable: `expandable`
- Eyebrow: `eyebrow`
- FeedbackToolbar: `feedback-toolbar`
- Field: `field`
- Frame: `frame`
- Icon: `icon`
- Link: `link`
- LoginLink: `login-link`
- Logo: `nav-logo`
- Mermaid: `mermaid`
- MethodNavPill: `method-nav-pill`
- MethodPill: `method-pill`
- NavBarLink: `navbar-link`
- NavTagPill: `nav-tag-pill`
- NavTagPillText: `nav-tag-pill-text`
- OptionDropdown: `option-dropdown`
- PaginationNext: `pagination-next`
- PaginationPrev: `pagination-prev`
- PaginationTitle: `pagination-title`
- Panel: `panel`
- SidebarGroup: `sidebar-group`
- SidebarGroupIcon: `sidebar-group-icon`
- SidebarGroupHeader: `sidebar-group-header`
- SidebarNavGroupDivider: `sidebar-nav-group-divider`
- SidebarTitle: `sidebar-title`
- Step: `step`
- Steps: `steps`
- Tab: `tab`
- Tabs: `tabs`
- TabsBar: `nav-tabs`
- TabsBarItem: `nav-tabs-item`
- TableOfContents: `toc`
- TableOfContentsItem: `toc-item`
- Tooltip: `tooltip`
- TopbarRightContainer: `topbar-right-container`
- TryitButton: `tryit-button`
- Update: `update`

References and the styling of common elements are subject to change as the platform evolves. Please use custom styling with caution.

##

[​](#custom-javascript)

Custom JavaScript

Custom JS allows you to add custom executable code globally. It is the equivalent of adding a `<script>` tag with JS code into every page.

###

[​](#adding-custom-javascript)

Adding custom JavaScript

Any `.js` file inside the content directory of your docs will be included in every documentation page. For example, you can add the following `ga.js` file to enable [Google Analytics](https://marketingplatform.google.com/about/analytics) across the entire documentation.
```
window.dataLayer = window.dataLayer || [];
function gtag() {
  dataLayer.push(arguments);
}
gtag('js', new Date());

gtag('config', 'TAG_ID');
```
Please use with caution to not introduce security vulnerabilities.

Was this page helpful?

YesNo

[FontsPrevious](https://www.mintlify.com/docs/customize/fonts)[ReactNext](https://www.mintlify.com/docs/customize/react-components)

⌘I
