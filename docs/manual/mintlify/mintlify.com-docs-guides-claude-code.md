---
url: https://mintlify.com/docs/guides/claude-code
canonical: https://www.mintlify.com/docs/guides/claude-code
title: "Claude Code - Mintlify"
description: "Configure Claude Code to write, review, and update your documentation."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

AI

Claude Code

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

Claude Code is an agentic command line tool that can help you maintain your documentation. It can write new content, review existing pages, and keep docs up to date. You can train Claude Code to understand your documentation standards and workflows by adding a `CLAUDE.md` file to your project and refining it over time.

##

[​](#getting-started)

Getting started

**Prerequisites:**

- Active Claude subscription (Pro, Max, or API access)

**Setup:**

1.  Install Claude Code:
```
npm install -g @anthropic-ai/claude-code
```
2.  Navigate to your docs directory.
3.  (Optional) Add the `CLAUDE.md` file below to your project.
4.  Run `claude` to start.

##

[​](#claude-md-template)

CLAUDE.md template

Save a `CLAUDE.md` file at the root of your docs directory to help Claude Code understand your project. This file trains Claude Code on your documentation standards, preferences, and workflows. See [Manage Claude’s memory](https://docs.anthropic.com/en/docs/claude-code/memory) in the Anthropic docs for more information. Copy this example template or make changes for your docs specifications:
```

# Mintlify documentation

## Working relationship
- You can push back on ideas-this can lead to better documentation. Cite sources and explain your reasoning when you do so
- ALWAYS ask for clarification rather than making assumptions
- NEVER lie, guess, or make up anything

## Project context
- Format: MDX files with YAML frontmatter
- Config: docs.json for navigation, theme, settings
- Components: Mintlify components

## Content strategy
- Document just enough for user success - not too much, not too little
- Prioritize accuracy and usability
- Make content evergreen when possible
- Search for existing content before adding anything new. Avoid duplication unless it is done for a strategic reason
- Check existing patterns for consistency
- Start by making the smallest reasonable changes

## docs.json

- Refer to the [docs.json schema](https://mintlify.com/docs.json) when building the docs.json file and site navigation

## Frontmatter requirements for pages
- title: Clear, descriptive page title
- description: Concise summary for SEO/navigation

## Writing standards
- Second-person voice ("you")
- Prerequisites at start of procedural content
- Test all code examples before publishing
- Match style and formatting of existing pages
- Include both basic and advanced use cases
- Language tags on all code blocks
- Alt text on all images
- Relative paths for internal links

## Git workflow
- NEVER use --no-verify when committing
- Ask how to handle uncommitted changes before starting
- Create a new branch when no clear branch exists for changes
- Commit frequently throughout development
- NEVER skip or disable pre-commit hooks

## Do not
- Skip frontmatter on any MDX file
- Use absolute URLs for internal links
- Include untested code examples
- Make assumptions - always ask for clarification
```

##

[​](#sample-prompts)

Sample prompts

Once you have Claude Code set up, try these prompts to see how it can help with common documentation tasks. You can copy and paste these examples directly, or adapt them for your specific needs.

###

[​](#convert-notes-to-polished-docs)

Convert notes to polished docs

Turn rough drafts into proper Markdown pages with components and frontmatter. **Example prompt:**
```
Convert this text into a properly formatted MDX page: [paste your text here]
```

###

[​](#review-docs-for-consistency)

Review docs for consistency

Get suggestions to improve style, formatting, and component usage. **Example prompt:**
```
Review the files in docs/ and suggest improvements for consistency and clarity
```

###

[​](#update-docs-when-features-change)

Update docs when features change

Keep documentation current when your product evolves. **Example prompt:**
```
Our API now requires a version parameter. Update our docs to include version=2024-01 in all examples
```

###

[​](#generate-comprehensive-code-examples)

Generate comprehensive code examples

Create multi-language examples with error handling. **Example prompt:**
```
Create code examples for [your API endpoint] in JavaScript, Python, and cURL with error handling
```

##

[​](#extending-claude-code)

Extending Claude Code

Beyond manually prompting Claude Code, you can integrate it with your existing workflows.

###

[​](#automation-with-github-actions)

Automation with GitHub Actions

Run Claude Code automatically when code changes to keep docs up to date. You can trigger documentation reviews on pull requests or update examples when API changes are detected.

###

[​](#multi-instance-workflows)

Multi-instance workflows

Use separate Claude Code sessions for different tasks - one for writing new content and another for reviewing and quality assurance. This helps maintain consistency and catch issues that a single session might miss.

###

[​](#team-collaboration)

Team collaboration

Share your refined `CLAUDE.md` file with your team to ensure consistent documentation standards across all contributors. Teams often develop project-specific prompts and workflows that become part of their documentation process.

###

[​](#custom-commands)

Custom commands

Create reusable slash commands in `.claude/commands/` for frequently used documentation tasks specific to your project or team.

Was this page helpful?

YesNo

[Tutorial: Build an in-app documentation assistantPrevious](https://www.mintlify.com/docs/guides/assistant-embed)[CursorNext](https://www.mintlify.com/docs/guides/cursor)

⌘I
