---
url: https://mintlify.com/docs/guides/windsurf
canonical: https://www.mintlify.com/docs/guides/windsurf
title: "Windsurf - Mintlify"
description: "Configure Windsurf to be your writing assistant."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

AI

Windsurf

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

Transform Windsurf into a documentation expert that understands your style guide, components, and project context through workspace rules and memories.

##

[​](#use-windsurf-with-mintlify)

Use Windsurf with Mintlify

Windsurf’s Cascade AI assistant can be tuned to write documentation according to your standards using Mintlify components. Workspace rules and memories provide persistent context about your project, ensuring more consistent suggestions from Cascade.

- **Workspace rules** are stored in your documentation repository and shared with your team.
- **Memories** provide individual context that builds up over time.

We recommend setting up workspace rules for shared documentation standards. You can develop memories as you work, but since they are not shared, they will not be consistent across team members. Create workspace rules in the `.windsurf/rules` directory of your docs repo. See [Memories & Rules](https://docs.windsurf.com/windsurf/cascade/memories) in the Windsurf documentation for more information.

##

[​](#example-workspace-rule)

Example workspace rule

This rule provides Cascade with context about Mintlify components and general technical writing best practices. You can use this example rule as-is or customize it for your documentation:

- **Writing standards**: Update language guidelines to match your style guide.
- **Component patterns**: Add project-specific components or modify existing examples.
- **Code examples**: Replace generic examples with real API calls and responses for your product.
- **Style and tone preferences**: Adjust terminology, formatting, and other rules.

Save your rule as a `.md` file in the `.windsurf/rules` directory of your docs repo.
````

# Mintlify technical writing rule

## Project context

- This is a documentation project on the Mintlify platform
- We use MDX files with YAML frontmatter
- Navigation is configured in `docs.json`
- We follow technical writing best practices

## Writing standards

- Use second person ("you") for instructions
- Write in active voice and present tense
- Start procedures with prerequisites
- Include expected outcomes for major steps
- Use descriptive, keyword-rich headings
- Keep sentences concise but informative

## Required page structure

Every page must start with frontmatter:
```yaml
---
title: "Clear, specific title"
description: "Concise description for SEO and navigation"
---
```

## Mintlify components

### docs.json

- Refer to the [docs.json schema](https://mintlify.com/docs.json) when building the docs.json file and site navigation

### Callouts

- `<Note>` for helpful supplementary information
- `<Warning>` for important cautions and breaking changes
- `<Tip>` for best practices and expert advice
- `<Info>` for neutral contextual information
- `<Check>` for success confirmations

### Code examples

- When appropriate, include complete, runnable examples
- Use `<CodeGroup>` for multiple language examples
- Specify language tags on all code blocks
- Include realistic data, not placeholders
- Use `<RequestExample>` and `<ResponseExample>` for API docs

### Procedures

- Use `<Steps>` component for sequential instructions
- Include verification steps with `<Check>` components when relevant
- Break complex procedures into smaller steps

### Content organization

- Use `<Tabs>` for platform-specific content
- Use `<Accordion>` for progressive disclosure
- Use `<Card>` and `<CardGroup>` for highlighting content
- Wrap images in `<Frame>` components with descriptive alt text

## API documentation requirements

- Document all parameters with `<ParamField>`
- Show response structure with `<ResponseField>`
- Include both success and error examples
- Use `<Expandable>` for nested object properties
- Always include authentication examples

## Quality standards

- Test all code examples before publishing
- Use relative paths for internal links
- Include alt text for all images
- Ensure proper heading hierarchy (start with h2)
- Check existing patterns for consistency
````

##

[​](#working-with-cascade)

Working with Cascade

Once your rules are set up, you can use Cascade to assist with various documentation tasks. See [Cascade](https://docs.windsurf.com/windsurf/cascade) in the Windsurf documentation for more information.

###

[​](#example-prompts)

Example prompts

**Writing new content**:
```
Create a new page explaining how to authenticate with our API. Include code examples in JavaScript, Python, and cURL.
```
**Improving existing content**:
```
Review this page and suggest improvements for clarity and component usage. Focus on making the steps easier to follow.
```
**Creating code examples**:
```
Generate a complete code example showing error handling for this API endpoint. Use realistic data and include expected responses.
```
**Maintaining consistency**:
```
Check if this new page follows our documentation standards and suggest any needed changes.
```

##

[​](#enhance-with-mcp-server)

Enhance with MCP server

Connect the Mintlify MCP server to Windsurf to give Cascade access to search the Mintlify documentation while helping you write. When you connect the MCP server, Cascade searches the up to date Mintlify documentation for context so you don’t have to leave your IDE to reference documentation. See [Model Context Protocol](https://www.mintlify.com/docs/ai/model-context-protocol#example%3A-connect-to-the-mintlify-mcp-server) for complete setup instructions.

Was this page helpful?

YesNo

[GEO guide: Optimize docs for AI search and answer enginesPrevious](https://www.mintlify.com/docs/guides/geo)[Migrating MDX API pages to OpenAPI navigationNext](https://www.mintlify.com/docs/guides/migrating-from-mdx)

⌘I
