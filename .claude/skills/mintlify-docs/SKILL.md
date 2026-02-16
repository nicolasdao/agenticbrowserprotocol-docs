---
name: mintlify-docs
description: "Mintlify documentation platform. Covers agent automation, AI features (assistant, MCP, llms.txt, skill.md, contextual menu, Slack/Discord bots), API playground (OpenAPI, AsyncAPI, MDX, SDK examples, WebSocket), API reference (agent jobs, assistant messages, search, analytics, updates), MDX components (accordions, cards, tabs, steps, callouts, code groups, expandables, fields, badges, tooltips, mermaid), content creation (text, code, images, changelogs, snippets, personalization, redirects), customization (themes, fonts, CSS/JS, React components, 404 page, custom domain), deployment (GitHub, GitLab, Vercel, Cloudflare, AWS Route53/CloudFront, reverse proxy, CSP, monorepo, CI, authentication, preview deployments), web editor (pages, navigation, media, collaboration, keyboard shortcuts, live preview, publish), dashboard (roles, permissions, SSO, audit logs), integrations (analytics: GA4, GTM, Amplitude, Mixpanel, PostHog, Segment, Hotjar, Heap, Fathom, Plausible, Pirsch, LogRocket, Clearbit, Clarity, Hightouch; privacy: Osano; SDKs: Speakeasy, Stainless; support: Front/Intercom), optimization (analytics, SEO, feedback, PDF exports), organization (hidden pages, mintignore), guides (accessibility, internationalization, content templates, content types, style and tone, navigation, linking, media, SEO, GEO, branches, git concepts, migration, developer docs, knowledge base, support center, Claude Code, Cursor, Windsurf). ALSO: AGENTS.md configuration, docs.json settings, frontmatter properties, docs-as-code workflow, llms-full.txt complete reference."
allowed-tools: Read, Grep, Glob
---

# Mintlify Documentation Navigator

Documentation location: `.claude/skills/mintlify-docs/references/`

All files are scraped web pages with YAML frontmatter containing `url`, `title`, and `description` fields. Content starts after the navigation boilerplate (typically after line ~70-80 in each file).

---

## File Naming Convention

**Pattern:** `mintlify.com-docs-<section>-<subsection>-<topic>.md`

The filename mirrors the URL path with hyphens replacing slashes.

**Examples:**
- `mintlify.com-docs-agent-customize.md` -> `/docs/agent/customize`
- `mintlify.com-docs-components-cards.md` -> `/docs/components/cards`
- `mintlify.com-docs-deploy-vercel.md` -> `/docs/deploy/vercel`

---

## Non-Standard Documentation

### LLM-Optimized Files

| File | Description | Key Topics |
|------|-------------|------------|
| `mintlify.com-docs-llms-full.txt.md` | Complete Mintlify docs in LLM-readable format | All topics consolidated, plain text, no navigation chrome |
| `mintlify.com-docs-llms.txt.md` | Index of all Mintlify doc pages with descriptions | Page listing with links and summaries |

### Tutorials

| File | Description | Key Topics |
|------|-------------|------------|
| `mintlify.com-docs-guides-assistant-embed.md` | Build an in-app documentation assistant | Embed assistant, API integration, in-app help |
| `mintlify.com-docs-guides-automate-agent.md` | Auto-update docs when code changes | Agent API, automation, CI/CD integration |

### Migration Guides

| File | Description | Key Topics |
|------|-------------|------------|
| `mintlify.com-docs-guides-migrating-from-mdx.md` | Migrate MDX API pages to OpenAPI navigation | MDX to OpenAPI, API page migration |

### Standalone Pages

| File | Description | Key Topics |
|------|-------------|------------|
| `mintlify.com-docs.md` | Introduction to Mintlify | Getting started, platform overview |
| `mintlify.com-docs-installation.md` | Install the CLI | CLI setup, local preview, mintlify dev |
| `mintlify.com-docs-contact-support.md` | Contact support | Help, support channels |
| `mintlify.com-docs-status.md` | Status page | Service status, incidents |

---

## Quick Reference

| Domain | Prefix | Files | Description |
|--------|--------|-------|-------------|
| Agent | `*-agent-*` | 7 | Documentation automation agent |
| AI Features | `*-ai-*` | 9 | Assistant, MCP, llms.txt, skill.md, bots |
| API Playground | `*-api-playground-*` | 10 | Interactive API testing in docs |
| API Reference | `*-api-agent-*`, `*-api-analytics-*`, `*-api-assistant-*`, `*-api-update-*`, `*-api-reference-*` | 10 | Mintlify REST API endpoints |
| Components | `*-components-*` | 21 | MDX component library |
| Create Content | `*-create-*` | 9 | Text, code, images, changelogs, snippets |
| Customize | `*-customize-*` | 6 | Themes, fonts, scripts, React, domain |
| Dashboard | `*-dashboard-*` | 5 | Roles, permissions, SSO, audit logs |
| Deploy | `*-deploy-*` | 15 | GitHub, GitLab, Vercel, Cloudflare, AWS, proxy |
| Editor | `*-editor-*` | 9 | Web-based documentation editor |
| Guides | `*-guides-*` | 24 | Best practices, tutorials, AI tools |
| Integrations | `*-integrations-*` | 20 | Analytics, privacy, SDKs, support tools |
| Optimize | `*-optimize-*` | 4 | Analytics, SEO, feedback, PDF exports |
| Organize | `*-organize-*` | 3 | Hidden pages, mintignore |

---

## How to Find Files

### 1. By domain pattern
```
Glob pattern=".claude/skills/mintlify-docs/references/mintlify.com-docs-<domain>-*.md"
```

### 2. By keyword search
```
Grep pattern="<keyword>" path=".claude/skills/mintlify-docs/references/" output_mode="files_with_matches"
```

### 3. By title/description in frontmatter
```
Grep pattern="<topic>" path=".claude/skills/mintlify-docs/references/" glob="*.md" output_mode="content" -A 2
```

### 4. From full index
```
Read file_path=".claude/skills/mintlify-docs/file-index.md"
```

### 5. Use the LLM-optimized file for broad questions
```
Read file_path=".claude/skills/mintlify-docs/references/mintlify.com-docs-llms-full.txt.md"
```
This file contains ALL Mintlify docs in a clean, consolidated format.

---

## Reading Tips

- **Skip boilerplate**: Each file has ~70 lines of navigation chrome at the top. Use `Grep` to find section markers, then `Read` with `offset` to jump to content.
- **Use frontmatter**: The `title` and `description` fields in YAML frontmatter give a quick summary.
- **Section markers**: Content sections use `## ` headings. Search with `Grep pattern="^## " path="<file>"` to get the outline.

---

## Protocol

1. **Identify the domain** from the user's question (agent, components, deploy, etc.)
2. **Use Glob** to find matching files: `Glob pattern="*-<domain>-*.md"`
3. **Check frontmatter** to confirm the right file: `Read file_path="<file>" limit=10`
4. **Find the relevant section**: `Grep pattern="<heading>" path="<file>" output_mode="content" -n`
5. **Read surgically**: `Read file_path="<file>" offset=<line> limit=50`
6. For broad questions, use `mintlify.com-docs-llms-full.txt.md` which has all docs consolidated

---

## Constraints

- Maximum read: 50-100 lines at a time
- Always use offset/limit parameters
- Search for section markers before reading
- Skip navigation boilerplate (first ~70 lines)
- Check file-index.md when unsure which file to consult
