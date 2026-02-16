---
url: https://mintlify.com/docs/guides/accessibility
canonical: https://www.mintlify.com/docs/guides/accessibility
title: "Accessibility - Mintlify"
description: "Create documentation that as many people as possible can use with WCAG compliance."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Best practices

Accessibility

Search...

⌘K

##### Overview

- [Guides](https://www.mintlify.com/docs/guides)

##### AI

- [Automate documentation updates](https://www.mintlify.com/docs/guides/automate-agent)
- [Build an in-app assistant](https://www.mintlify.com/docs/guides/assistant-embed)
- [Claude Code](https://www.mintlify.com/docs/guides/claude-code)
- [Cursor](https://www.mintlify.com/docs/guides/cursor)
- [GEO](https://www.mintlify.com/docs/guides/geo)
- [Windsurf](https://www.mintlify.com/docs/guides/windsurf)

##### API docs

- [Migrate from MDX to OAS](https://www.mintlify.com/docs/guides/migrating-from-mdx)

##### Best practices

- [Accessibility](https://www.mintlify.com/docs/guides/accessibility)
- [Content types](https://www.mintlify.com/docs/guides/content-types)
- [Content templates](https://www.mintlify.com/docs/guides/content-templates)
- [Improve your docs](https://www.mintlify.com/docs/guides/improving-docs)
- [Internationalization](https://www.mintlify.com/docs/guides/internationalization)
- [Linking](https://www.mintlify.com/docs/guides/linking)
- [Maintenance](https://www.mintlify.com/docs/guides/maintenance)
- [Media](https://www.mintlify.com/docs/guides/media)
- [Organize navigation](https://www.mintlify.com/docs/guides/navigation)
- [SEO](https://www.mintlify.com/docs/guides/seo)
- [Style and tone](https://www.mintlify.com/docs/guides/style-and-tone)
- [Understand your audience](https://www.mintlify.com/docs/guides/understand-your-audience)

##### Git

- [Git concepts for documentation](https://www.mintlify.com/docs/guides/git-concepts)
- [Work with branches](https://www.mintlify.com/docs/guides/branches)

##### Use cases

- [Developer documentation](https://www.mintlify.com/docs/guides/developer-documentation)
- [Knowledge base](https://www.mintlify.com/docs/guides/knowledge-base)
- [Support center](https://www.mintlify.com/docs/guides/support-center)

![US](https://d3gk2c5xim1je2.cloudfront.net/flags/US.svg)

English

When you create accessible documentation, you prioritize content design that makes your documentation usable by as many people as possible regardless of how they access and interact with your documentation. Accessible documentation improves the user experience for everyone. Your content is more clear, better structured, and easier to navigate. This guide offers some best practices for creating accessible documentation, but it is not exhaustive. You should consider accessibility an ongoing process. Technologies and standards change over time, which introduce new opportunities to improve documentation.

##

[​](#what-is-accessibility)

What is accessibility?

Accessibility (sometimes abbreviated as a11y for the number of letters between the first and last letters of “accessibility”) is intentionally designing and building websites and tools that as many people as possible can use. People with temporary or permanent disabilities should have the same level of access to digital technologies. And designing for accessibility benefits everyone, including people who access your website on mobile devices or slow networks. Accessible documentation follows web accessibility standards, primarily the [Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/WAI/WCAG22/quickref/). These guidelines help ensure your content is perceivable, operable, understandable, and robust.

##

[​](#getting-started-with-accessibility)

Getting started with accessibility

Making your documentation accessible is a process. You don’t have to fix everything all at once and you can’t do it only once. If you’re just beginning to implement accessibility practices for your documentation, consider a phased approach where you start with high-impact changes and build from there.

###

[​](#first-steps)

First steps

Here are three things you can do right now to improve the accessibility of your documentation:

1.  **Run `mint a11y`** to identify accessibility issues in your content.
2.  **Add alt text** to all images.
3.  **Check your heading hierarchy** to ensure one H1 per page and headings follow sequential order.

###

[​](#plan-your-accessibility-work)

Plan your accessibility work

The best workflow is the one that works for your team. Here is one way that you can approach accessibility work: **Phase 1: Images and structure**

- Review all images for descriptive alt text.
- Audit link text and replace generic phrases like “click here.”
- Fix heading hierarchy issues across your documentation.

**Phase 2: Navigation and media**

- Test keyboard navigation on your documentation.
- Test screen reader support.
- Add captions and transcripts to embedded videos.
- Review color contrast.

**Phase 3: Build it into your workflow**

- Run `mint a11y` before publishing new content.
- Include accessibility checks in your content review process.
- Test keyboard navigation when adding interactive features.
- Verify new external links and embeds include proper titles and descriptions.

Starting small and building accessibility into your regular workflow makes it sustainable. Each improvement helps more users access your documentation successfully.

##

[​](#structure-your-content)

Structure your content

Well-structured content is easier to navigate and understand, especially for screen reader users who rely on headings to move through pages and people who use keyboard navigation.

###

[​](#use-proper-heading-hierarchy)

Use proper heading hierarchy

Each page should have a single H1 heading, which is defined by the `title:` property in a page’s frontmatter. Use additional headings in order without skipping. For example, don’t skip from H2 to H4.
```
<!-- Good -->

# Page title (H1)

## Main section (H2)

### Subsection (H3)

### Another subsection (H3)

## Another main section (H2)

<!-- Bad -->

# Page title (H1)

## Main section (H2)

#### Subsection (H4)

### Another subsection (H3)
```
Headings at the same level should have unique names.
```
<!-- Good -->

## Accessibility tips (H2)

### Write effective alt text (H3)

### Use proper color contrast (H3)

<!-- Bad -->

## Accessibility tips (H2)

### Tip (H3)

### Tip (H3)
```

###

[​](#write-descriptive-link-text)

Write descriptive link text

Link text should be meaningful and connected to the destination. Avoid vague phrases like “click here” or “read more.”
```
<!-- Good -->
Learn how to [configure your navigation](/organize/navigation).

<!-- Unclear relation between link text and destination -->
[Learn more](/organize/navigation).
```

###

[​](#keep-content-scannable)

Keep content scannable

- Break up long paragraphs.
- Use lists for steps and options.
- Highlight information with callouts.

###

[​](#use-proper-table-structure)

Use proper table structure

Use tables sparingly and only for tabular data that has meaning inherited from the column and row headers. When using tables, include headers so screen readers can associate data with the correct column:
```
| Feature | Status |
| ------- | ------ |
| Search  | Active |
| Analytics | Active |
```

##

[​](#write-descriptive-alt-text)

Write descriptive alt text

Alt text makes images accessible to screen reader users and appears when images fail to load. Images in your documentation should have alt text that describes the image and makes it clear why the image is included. Even with alt text, you should not rely on images alone to convey information. Make sure your content describes what the image communicates.

###

[​](#write-effective-alt-text)

Write effective alt text

- **Be specific**: Describe what the image shows, not just that it’s an image.
- **Be concise**: Aim for one to two sentences.
- **Avoid redundancy**: Don’t start with “Image of” because screen readers will already know that the alt text is associated with an image. However, you should include descriptions like “Screenshot of” or “Diagram of” if that context is important to the image.
```
<!-- Good -->
![Screenshot of the dashboard showing three active projects and two pending invitations](/images/dashboard.png)

<!-- Not helpful -->
![Dashboard screenshot](/images/dashboard.png)
```

###

[​](#add-alt-text-to-images)

Add alt text to images

For Markdown images, include alt text in the square brackets:
```
![Description of the image](/path/to/image.png)
```
For HTML images, use the `alt` attribute:
```
<img
  src="/images/screenshot.png"
  alt="Settings panel with accessibility options enabled. The options are emphasized with an orange rectangle."
/>
```

###

[​](#add-titles-to-embedded-content)

Add titles to embedded content

Iframes and video embeds require descriptive titles:
```
<iframe
  src="https://www.youtube.com/embed/example"
  title="Tutorial: Setting up your first documentation site"
></iframe>
```

##

[​](#design-for-readability)

Design for readability

Visual design choices affect how accessible your documentation is to users with low vision, color blindness, or other visual disabilities.

###

[​](#ensure-sufficient-color-contrast)

Ensure sufficient color contrast

If you customize your theme colors, verify the contrast ratios meet WCAG requirements:

- Body text: minimum 4.5:1 contrast ratio
- Large text: minimum 3:1 contrast ratio
- Interactive elements: minimum 3:1 contrast ratio

Test both light and dark mode. The `mint a11y` command checks for color contrast.

###

[​](#don’t-rely-on-color-alone)

Don’t rely on color alone

If you use color to convey information, include a text label or icon as well. For example, don’t mark errors only with red text. Include an error icon or the word “Error.”

###

[​](#use-clear-concise-language)

Use clear, concise language

- Write in plain language.
- Define technical terms when first used.
- Avoid run-on sentences.
- Use active voice.

##

[​](#make-code-examples-accessible)

Make code examples accessible

Code blocks are a core part of technical documentation, but they require specific accessibility considerations to ensure screen reader users can understand them. In general, follow these guidelines:

- Break long code examples into smaller, logical chunks.
- Comment complex logic within the code.
- Consider providing a text description for complex algorithms.
- When showing file structure, use actual code blocks with language labels rather than ASCII art.

###

[​](#specify-the-programming-language)

Specify the programming language

Always declare the language for syntax highlighting. This helps screen readers announce the code context to users:
````
```javascript
function getUserData(id) {
  return fetch(`/api/users/${id}`);
}
```
````

###

[​](#provide-context-around-code)

Provide context around code

Provide clear context for code blocks:
````
The following function fetches user data from the API:
```javascript
function getUserData(id) {
  return fetch(`/api/users/${id}`);
}
```
This returns a promise that resolves to the user object.
````

##

[​](#video-and-multimedia-accessibility)

Video and multimedia accessibility

Videos, animations, and other multimedia content need text alternatives so all users can access the information they contain.

###

[​](#add-captions-to-videos)

Add captions to videos

Captions make video content accessible to users who are deaf or hard of hearing. They also help users in sound-sensitive environments and non-native speakers:

- Use captions for all spoken content in videos.
- Include relevant sound effects in captions.
- Ensure captions are synchronized with the audio.
- Use proper punctuation and speaker identification when multiple people speak.

Most video hosting platforms support adding captions. Upload caption files or use auto-generated captions as a starting point, then review for accuracy.

###

[​](#provide-transcripts)

Provide transcripts

Transcripts offer an alternative way to access video content. They’re searchable, easier to reference, and accessible to screen readers:
```
<iframe
  src="https://www.youtube.com/embed/example"
  title="Tutorial: Setting up authentication"
></iframe>

<Accordion title="Video transcript">
In this tutorial, we'll walk through setting up authentication...
</Accordion>
```
Place transcripts near the video or provide a clear link to access them.

###

[​](#consider-alternatives-to-video-only-content)

Consider alternatives to video-only content

If critical information only appears in a video:

- Provide the same information in text form.
- Include key screenshots with descriptive alt text.
- Create a written tutorial that covers the same material.

This ensures users who can’t access video content can still complete their task.

##

[​](#test-your-documentation)

Test your documentation

Regular testing helps you catch accessibility issues before users encounter them.

###

[​](#check-for-accessibility-issues-with-mint-a11y)

Check for accessibility issues with `mint a11y`

Use the `mint a11y` CLI command to automatically scan your documentation for common accessibility issues:
```
mint a11y
```
The command checks for:

- Missing alt text on images and videos.
- Insufficient color contrast.

When the scan completes, review the reported issues and fix them in your content. Run the command again to verify your fixes. Use flags to check for specific accessibility issues.
```

# Check only for missing alt text
mint a11y --skip-contrast

# Check only for color contrast issues
mint a11y --skip-alt-text
```

###

[​](#basic-keyboard-navigation-test)

Basic keyboard navigation test

Navigate through your documentation using only your keyboard:

1.  Press Tab to move forward through interactive elements.
2.  Press Shift + Tab to move backward.
3.  Press Enter to activate links and buttons.
4.  Verify all interactive elements are reachable and have visible focus indicators.

###

[​](#go-deeper-with-accessibility-testing)

Go deeper with accessibility testing

For more comprehensive testing:

- **Screen readers**: Test with [NVDA (Windows)](https://www.nvaccess.org/) or [VoiceOver (Mac)](https://www.apple.com/accessibility/voiceover/).
- **Browser extensions**: Install [axe DevTools](https://www.deque.com/axe/browser-extensions/) or [WAVE](https://wave.webaim.org/extension/) to scan pages for issues.
- **WCAG guidelines**: Review the [Web Content Accessibility Guidelines](https://www.w3.org/WAI/WCAG22/quickref/) for detailed standards.

##

[​](#additional-resources)

Additional resources

Continue learning about accessibility with these trusted resources:

- **[WebAIM](https://webaim.org/)**: Practical articles and tutorials on web accessibility
- **[The A11y Project](https://www.a11yproject.com/)**: Community-driven accessibility resources and checklist
- **[W3C Web Accessibility Initiative (WAI)](https://www.w3.org/WAI/)**: Official accessibility standards and guidance

Was this page helpful?

YesNo

[Migrating MDX API pages to OpenAPI navigationPrevious](https://www.mintlify.com/docs/guides/migrating-from-mdx)[Content typesNext](https://www.mintlify.com/docs/guides/content-types)

⌘I
