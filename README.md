# Agentic Browser Protocol — Documentation

> **Official documentation for the Agentic Browser Protocol (ABP)**
>
> This is a **Mintlify documentation site** that documents the ABP specification and MCP Bridge implementation.

## What is the Agentic Browser Protocol?

The **Agentic Browser Protocol (ABP)** is an open specification that enables web applications and Chrome extensions to expose browser-exclusive capabilities — like PDF rendering, authenticated sessions, GPU-accelerated graphics, and privileged `chrome.*` APIs — to AI agents through direct API calls rather than fragile UI automation.

**Instead of this** (fragile, breaks when UI changes):
```javascript
await page.click('#export-button');
await page.waitForSelector('.success');
```

**ABP provides this** (explicit contract, reliable):
```javascript
const result = await abp.call('export.pdf', {
  html: content,
  options: { pageSize: 'letter' }
});
```

**Main Project Repository:** [github.com/nicholasdao/agenticbrowserprotocol](https://github.com/nicholasdao/agenticbrowserprotocol)

**Live Documentation:** [Link will be added after deployment]

---

## About This Repository

This repository contains the **Mintlify-powered documentation website** for ABP. Mintlify is a modern documentation platform that:
- Generates beautiful, searchable documentation from MDX files
- Provides interactive components (tabs, code groups, callouts)
- Auto-deploys from Git when you push changes
- Offers an AI-powered search assistant

**Technology Stack:**
- **Platform:** Mintlify
- **Content Format:** MDX (Markdown + React components)
- **Deployment:** Auto-deploys from GitHub main branch
- **Local Preview:** `npx mint dev`

### Open Source & Community

This project is **open source** under the **BSD 3-Clause License**. See [LICENSE](LICENSE) for full terms.

**We welcome contributions!** ABP is a community-driven protocol. You can:
- 🐛 Report issues or inaccuracies in the documentation
- ✏️ Fix typos, improve examples, clarify confusing sections
- 💡 Suggest new guides or examples
- 🔧 Help keep docs in sync with protocol changes
- 🌍 Share ABP with the developer community

---

## Documentation Structure & Navigation Guide

The documentation is organized into **3 main tabs with 7 topic groups** covering 26 pages total. Here's what each section contains and when to use it.

### Tab 1: Documentation (Main)

#### Getting Started (3 pages)
Start here if you're new to ABP.

| Page | File | What It Covers | Read This If... |
|------|------|----------------|-----------------|
| **Introduction** | `introduction.mdx` | What ABP is, why it exists, design principles, relationship to MCP, use cases | You're new to ABP and want a high-level overview |
| **Quick Start** | `quickstart.mdx` | Three fast-track paths: using ABP apps, building web apps, building extensions | You want to get started immediately |
| **Glossary** | `glossary.mdx` | Definitions of all ABP terms (manifest, capability, session, elicitation, etc.) | You need to look up ABP terminology |

#### Core Concepts (7 pages)
Deep dives into how ABP works.

| Page | File | What It Covers | Read This If... |
|------|------|----------------|-----------------|
| **Protocol Overview** | `concepts/protocol-overview.mdx` | Simplified protocol introduction, capabilities, sessions, manifest, transport options | You want to understand ABP's core architecture |
| **Architecture** | `concepts/architecture.mdx` | System components, integration model, communication flows, data routing | You need to understand how all the pieces fit together |
| **Discovery** | `concepts/discovery.mdx` | How agents find ABP apps, manifest format, web vs extension discovery | You're building a client or debugging discovery issues |
| **Capabilities** | `concepts/capabilities.mdx` | Standard capability namespaces (export.*, convert.*, ai.*), naming conventions, forbidden patterns | You're designing capabilities for your app |
| **Data Flow** | `concepts/data-flow.mdx` | How the MCP Bridge routes binary data to files, preventing context bloat | You're working with large outputs (PDFs, images) |
| **Elicitation & Progress** | `concepts/elicitation-and-progress.mdx` | Bidirectional communication: apps requesting input, reporting progress | You need user input during capability execution |
| **Security** | `concepts/security.mdx` | Threat model, input validation, rate limiting, CORS, permission model | You're concerned about security implications |

### Tab 2: Guides

#### Building ABP Apps (5 pages)
Implementation guides for web developers.

| Page | File | What It Covers | Read This If... |
|------|------|----------------|-----------------|
| **Building Web Apps** | `guides/building-web-apps.mdx` | Practical quick-start: add manifest link, create manifest, implement `window.abp` | You want to make your web app ABP-compatible (START HERE) |
| **Chrome Extensions** | `guides/chrome-extensions.mdx` | Expose `chrome.tabs`, `chrome.scripting` APIs as ABP capabilities | You're building a Chrome extension with ABP |
| **Implementation Guide** | `guides/implementation-guide.mdx` | Comprehensive process: inventory features, map to capabilities, validate | You need the complete implementation methodology |
| **Common Pitfalls** | `guides/common-pitfalls.mdx` | Critical mistakes: native UI dialogs, status messages vs data, delivery mechanisms | ⚠️ READ BEFORE SHIPPING - prevents silent failures |
| **Examples** | `guides/examples.mdx` | Complete working code: minimal app, markdown converter, PDF generator, canvas renderer | You learn best from code examples |

#### MCP Bridge (3 pages)
For users and developers of the reference client.

| Page | File | What It Covers | Read This If... |
|------|------|----------------|-----------------|
| **MCP Bridge Quick Start** | `guides/mcp-bridge-quickstart.mdx` | Install, configure, connect to apps, use capabilities | You're an agent user wanting to use ABP apps |
| **MCP Bridge Architecture** | `guides/mcp-bridge-architecture.mdx` | How the bridge works internally: browser management, data flow, tool generation | You're studying the reference implementation |
| **Troubleshooting** | `guides/troubleshooting.mdx` | Common issues: connection failures, capability errors, permission problems | Something isn't working and you need help |

### Tab 3: Reference

#### Protocol API (5 pages)
Authoritative API specifications.

| Page | File | What It Covers | Read This If... |
|------|------|----------------|-----------------|
| **API Reference** | `reference/api.mdx` | Complete TypeScript definitions for `window.abp`, all methods, types, schemas | You need the authoritative API specification |
| **Error Handling** | `reference/error-handling.mdx` | Standard error codes, retry strategies, MCP Bridge error patterns | You're implementing error handling |
| **Binary Data** | `reference/binary-data.mdx` | BinaryData format, transport-specific handling, Base64 encoding | You're working with PDFs, images, or file data |
| **Cancellation** | `reference/cancellation.mdx` | How to cancel long operations using AbortSignal | You need to support operation cancellation |
| **Conformance** | `reference/conformance.mdx` | Minimum requirements for ABP-compliant apps and clients | You're verifying your implementation is compliant |

#### Implementation (3 pages)
Advanced implementation guides.

| Page | File | What It Covers | Read This If... |
|------|------|----------------|-----------------|
| **App-Side Implementation** | `reference/app-side.mdx` | Advanced patterns: modular runtime, capability registry, progress, cancellation, testing | You're building a production ABP app |
| **Client-Side Implementation** | `reference/client-side.mdx` | Building ABP clients: discovery, browser management, session lifecycle, data routing | You're building a client (not using the MCP Bridge) |
| **Versioning** | `reference/versioning.mdx` | Three version tracks (protocol, spec, bridge), release workflows, commit conventions | You're contributing to ABP or managing versions |

---

## Finding What You Need

### By User Type

**I'm an AI agent user** (want to use ABP apps):
1. Start: [Quick Start](/quickstart) → [MCP Bridge Quick Start](/guides/mcp-bridge-quickstart)
2. Troubleshooting: [Troubleshooting Guide](/guides/troubleshooting)

**I'm a web developer** (want to make my app ABP-compatible):
1. Start: [Building Web Apps](/guides/building-web-apps)
2. Complete process: [Implementation Guide](/guides/implementation-guide)
3. Before shipping: [Common Pitfalls](/guides/common-pitfalls) ⚠️
4. Verify: [Conformance Requirements](/reference/conformance)

**I'm building a Chrome extension**:
1. Start: [Chrome Extensions Guide](/guides/chrome-extensions)
2. Reference: [Common Pitfalls](/guides/common-pitfalls)

**I'm building an ABP client** (in Python, Rust, etc.):
1. Start: [Protocol Overview](/concepts/protocol-overview)
2. Architecture: [Architecture](/concepts/architecture)
3. Implementation: [Client-Side Implementation](/reference/client-side)
4. Study: [MCP Bridge Architecture](/guides/mcp-bridge-architecture) (reference implementation)

**I'm researching ABP**:
1. Overview: [Introduction](/introduction)
2. Concepts: [Protocol Overview](/concepts/protocol-overview)
3. Design: [Architecture](/concepts/architecture)

### By Topic

| Topic | Where to Find It |
|-------|------------------|
| **What is ABP?** | `introduction.mdx` |
| **How does ABP work?** | `concepts/protocol-overview.mdx`, `concepts/architecture.mdx` |
| **Implementing `window.abp`** | `guides/building-web-apps.mdx` (quick), `guides/implementation-guide.mdx` (comprehensive) |
| **Capability design** | `concepts/capabilities.mdx` (taxonomy), `guides/implementation-guide.mdx` (mapping process) |
| **Binary data (PDFs, images)** | `concepts/data-flow.mdx` (client-side), `reference/binary-data.mdx` (protocol spec) |
| **Error handling** | `reference/error-handling.mdx` |
| **Security** | `concepts/security.mdx` |
| **Testing ABP apps** | `guides/building-web-apps.mdx` (manual testing), `reference/app-side.mdx` (unit/integration tests) |
| **Chrome extensions** | `guides/chrome-extensions.mdx` |
| **MCP Bridge usage** | `guides/mcp-bridge-quickstart.mdx` |
| **MCP Bridge internals** | `guides/mcp-bridge-architecture.mdx` |
| **Discovery mechanism** | `concepts/discovery.mdx` |
| **Progress reporting** | `concepts/elicitation-and-progress.mdx` |
| **Cancellation** | `reference/cancellation.mdx` |
| **API reference** | `reference/api.mdx` |
| **Troubleshooting** | `guides/troubleshooting.mdx` |
| **Versioning** | `reference/versioning.mdx` |

### By Question

| Question | Answer Location |
|----------|----------------|
| How do I make my web app ABP-compatible? | `guides/building-web-apps.mdx` |
| What capabilities can I expose? | `concepts/capabilities.mdx` |
| How do I handle binary data? | `reference/binary-data.mdx` |
| What are the common mistakes? | `guides/common-pitfalls.mdx` |
| How do I test my implementation? | `guides/building-web-apps.mdx` (section: Testing), `reference/conformance.mdx` |
| How does discovery work? | `concepts/discovery.mdx` |
| How do I build a client? | `reference/client-side.mdx` |
| What's the complete API? | `reference/api.mdx` |
| How do I use ABP with my agent? | `guides/mcp-bridge-quickstart.mdx` |
| How does the MCP Bridge work internally? | `guides/mcp-bridge-architecture.mdx` |
| Why isn't my app working? | `guides/troubleshooting.mdx`, `guides/common-pitfalls.mdx` |

---

## File Organization

```
agenticbrowserprotocol-docs/
│
├── README.md                    ← You are here
├── docs.json                    ← Mintlify site configuration
├── .gitignore                   ← Git ignore rules
│
├── introduction.mdx             ← Homepage: What ABP is, why it exists
├── quickstart.mdx               ← Fast paths for different user types
├── glossary.mdx                 ← ABP terminology reference
│
├── concepts/                    ← Core Concepts (7 pages)
│   ├── protocol-overview.mdx    ← How ABP works (simplified)
│   ├── architecture.mdx         ← System architecture (comprehensive)
│   ├── discovery.mdx            ← How agents find ABP apps
│   ├── capabilities.mdx         ← Capability namespaces and conventions
│   ├── data-flow.mdx            ← Binary data routing
│   ├── elicitation-and-progress.mdx  ← Bidirectional communication
│   └── security.mdx             ← Security model and best practices
│
├── guides/                      ← Implementation Guides (8 pages)
│   ├── building-web-apps.mdx    ← Quick start for web developers ⭐
│   ├── chrome-extensions.mdx    ← Chrome extension guide
│   ├── implementation-guide.mdx ← Comprehensive implementation process
│   ├── common-pitfalls.mdx      ← Critical mistakes to avoid ⚠️
│   ├── examples.mdx             ← Working code examples
│   ├── mcp-bridge-quickstart.mdx    ← Using the MCP Bridge
│   ├── mcp-bridge-architecture.mdx  ← How the bridge works
│   └── troubleshooting.mdx      ← Common issues and solutions
│
├── reference/                   ← API Reference & Specs (8 pages)
│   ├── api.mdx                  ← Complete API specification
│   ├── error-handling.mdx       ← Error codes and strategies
│   ├── binary-data.mdx          ← Binary data protocol
│   ├── cancellation.mdx         ← Cancellation protocol
│   ├── conformance.mdx          ← Compliance requirements
│   ├── app-side.mdx             ← Advanced app patterns
│   ├── client-side.mdx          ← Building ABP clients
│   └── versioning.mdx           ← Version management
│
└── docs/                        ← Reference materials
    └── manual/
        └── mintlify/            ← Mintlify documentation (local reference)
```

---

## Content Map: What's Covered Where

### Introduction & Overview
- **What ABP is:** `introduction.mdx`
- **Why ABP exists:** `introduction.mdx` → "Why ABP?" section
- **Quick overview:** `concepts/protocol-overview.mdx`
- **Design principles:** `introduction.mdx` → "Design Principles"
- **Relationship to MCP:** `introduction.mdx` → "Relationship to MCP"

### Getting Started

#### For Web Developers (Making Apps ABP-Compatible)
1. **Quick start:** `guides/building-web-apps.mdx` — Add manifest link, create `window.abp`, test (100-150 lines of code)
2. **Comprehensive guide:** `guides/implementation-guide.mdx` — Full process: inventory features, map to capabilities, implement, validate
3. **Before shipping:** `guides/common-pitfalls.mdx` — Critical mistakes that cause silent failures ⚠️
4. **Examples:** `guides/examples.mdx` — Complete working apps to study
5. **Verification:** `reference/conformance.mdx` — Checklist to ensure compliance

#### For Chrome Extension Developers
1. **Extension guide:** `guides/chrome-extensions.mdx` — Expose `chrome.*` APIs as capabilities
2. **Common pitfalls:** `guides/common-pitfalls.mdx` — Anti-patterns apply to extensions too

#### For Agent Users (Using ABP Apps)
1. **Setup:** `guides/mcp-bridge-quickstart.mdx` — Install and configure the MCP Bridge
2. **Usage:** `guides/mcp-bridge-quickstart.mdx` → "Using ABP Capabilities"
3. **Problems:** `guides/troubleshooting.mdx` — Common issues and solutions

#### For Client Developers (Building ABP Clients)
1. **Protocol:** `concepts/protocol-overview.mdx` — Understand the protocol first
2. **Architecture:** `concepts/architecture.mdx` — See how components interact
3. **Implementation:** `reference/client-side.mdx` — Build a client in Python, Rust, etc.
4. **Reference:** `guides/mcp-bridge-architecture.mdx` — Study the MCP Bridge (reference implementation)

### Core Protocol Concepts

| Concept | Primary Reference | Additional Reading |
|---------|-------------------|-------------------|
| **Sessions** | `concepts/protocol-overview.mdx` → "Sessions" | `concepts/architecture.mdx` → "Session Management" |
| **Capabilities** | `concepts/capabilities.mdx` | `concepts/protocol-overview.mdx` → "Capabilities" |
| **Manifest** | `concepts/discovery.mdx` | `concepts/protocol-overview.mdx` → "Manifest" |
| **Discovery** | `concepts/discovery.mdx` | `concepts/architecture.mdx` → "Initialization Flow" |
| **Transport** | `concepts/protocol-overview.mdx` → "Transport Options" | `concepts/architecture.mdx` → "Communication Flow" |
| **Binary data** | `reference/binary-data.mdx` (protocol spec) | `concepts/data-flow.mdx` (client routing) |
| **Elicitation** | `concepts/elicitation-and-progress.mdx` | `reference/api.mdx` → "Elicitation Methods" |
| **Progress** | `concepts/elicitation-and-progress.mdx` | `reference/app-side.mdx` → "Progress Reporting" |
| **Cancellation** | `reference/cancellation.mdx` | `reference/api.mdx` → "cancel()" |
| **Security** | `concepts/security.mdx` | `reference/conformance.mdx` → security checklist items |

### Implementation Details

| What You're Building | Start Here | Also Read |
|---------------------|------------|-----------|
| **Minimal ABP app** | `guides/building-web-apps.mdx` → "Complete Example" | `guides/examples.mdx` → "Minimal ABP App" |
| **Production ABP app** | `guides/implementation-guide.mdx` | `reference/app-side.mdx` (advanced patterns) |
| **Chrome extension** | `guides/chrome-extensions.mdx` | `guides/common-pitfalls.mdx` |
| **ABP client (Python, etc.)** | `reference/client-side.mdx` | `guides/mcp-bridge-architecture.mdx` |
| **Capability handlers** | `guides/building-web-apps.mdx` → "Common Patterns" | `reference/app-side.mdx` |
| **Progress reporting** | `concepts/elicitation-and-progress.mdx` → "Progress Reporting" | `reference/app-side.mdx` → "Progress Reporting" |
| **Binary output (PDFs)** | `guides/implementation-guide.mdx` → "The PDF/Print Pattern" | `reference/binary-data.mdx` |
| **Error handling** | `reference/error-handling.mdx` | `reference/api.mdx` → "Standard Error Codes" |

### Troubleshooting & Debugging

| Problem | Where to Look |
|---------|---------------|
| **Discovery fails** | `guides/troubleshooting.mdx` → "Discovery Issues" |
| **Connection fails** | `guides/troubleshooting.mdx` → "Connection Issues" |
| **window.abp undefined** | `guides/common-pitfalls.mdx` → framework-specific guidance, `guides/troubleshooting.mdx` |
| **Capabilities return wrong data** | `guides/common-pitfalls.mdx` → "Status Messages Instead of Data" |
| **Native UI dialogs block** | `guides/common-pitfalls.mdx` → "Native Browser UI" |
| **Permission denied** | `guides/troubleshooting.mdx` → "Permission Issues" |
| **Files not saved** | `guides/troubleshooting.mdx` → "Data Flow Issues" |
| **General issues** | `guides/troubleshooting.mdx` (first), then `guides/common-pitfalls.mdx` |

### Advanced Topics

| Topic | Location |
|-------|----------|
| **Modular ABP runtime** | `reference/app-side.mdx` → "Architecture Patterns" |
| **Capability registry pattern** | `reference/app-side.mdx` → "Capability Registry Pattern" |
| **Testing strategies** | `reference/app-side.mdx` → "Testing" |
| **Performance optimization** | `reference/app-side.mdx` → "Performance Optimization" |
| **Rate limiting** | `concepts/security.mdx` → "Rate Limiting" |
| **Browser automation** | `concepts/architecture.mdx` → "Browser Requirements" |
| **Multiple transports** | `concepts/protocol-overview.mdx` → "Transport Options" |
| **Dynamic capabilities** | `guides/examples.mdx` → "Dynamic Capabilities Example" |

---

## Reading Paths for Different Goals

### Path 1: "I want to use an ABP app with my AI agent"
1. `quickstart.mdx` → "Using ABP Apps"
2. `guides/mcp-bridge-quickstart.mdx` (install, configure, connect)
3. `guides/troubleshooting.mdx` (if issues arise)

**Estimated time:** 15-30 minutes

### Path 2: "I want to make my web app ABP-compatible"
1. `introduction.mdx` (understand what ABP is)
2. `guides/building-web-apps.mdx` (implement in ~150 lines)
3. `guides/common-pitfalls.mdx` (avoid critical mistakes) ⚠️
4. `reference/conformance.mdx` (verify compliance)

**Estimated time:** 2-4 hours for initial implementation

### Path 3: "I want to understand ABP deeply"
1. `introduction.mdx` (overview)
2. `concepts/protocol-overview.mdx` (core concepts)
3. `concepts/architecture.mdx` (how it all fits together)
4. `concepts/capabilities.mdx` (capability system)
5. `reference/api.mdx` (complete specification)

**Estimated time:** 1-2 hours of reading

### Path 4: "I want to build an ABP client (not using the bridge)"
1. `concepts/protocol-overview.mdx` (understand the protocol)
2. `concepts/architecture.mdx` (understand client role)
3. `concepts/discovery.mdx` (implement discovery)
4. `reference/client-side.mdx` (implementation checklist)
5. `guides/mcp-bridge-architecture.mdx` (study reference implementation)
6. `reference/api.mdx` (complete API spec)

**Estimated time:** 4-8 hours to build a basic client

### Path 5: "Something isn't working"
1. `guides/troubleshooting.mdx` (common issues)
2. `guides/common-pitfalls.mdx` (if building an app)
3. `reference/conformance.mdx` (verify requirements)

---

## Working with This Documentation

### Local Development

```bash
# Install Mintlify CLI globally (one-time)
npm install -g mintlify

# Preview the site locally
npx mint dev
```

The site will be available at **http://localhost:3000** with hot-reload (changes update automatically).

### Making Changes

#### Small Edits (Typos, Clarifications)
1. Edit the `.mdx` file directly
2. Check locally with `npx mint dev`
3. Commit and push to deploy

#### Adding New Pages
1. Create `.mdx` file in the appropriate directory (`concepts/`, `guides/`, or `reference/`)
2. Add frontmatter:
   ```yaml
   ---
   title: "Page Title"
   description: "Brief description for SEO and navigation"
   icon: "icon-name"  # Optional: Font Awesome icon
   ---
   ```
3. Add to `docs.json` navigation
4. Test locally
5. Commit and push

#### Editing Navigation
Edit `docs.json` to change:
- Tab structure
- Group organization
- Page order
- Topbar links

### Link Conventions

**Always use Mintlify path-based links** (no file extensions):

```markdown
✅ [Protocol Overview](/concepts/protocol-overview)
✅ [API Reference](/reference/api#initialize)
❌ [Protocol Overview](./concepts/protocol-overview.md)
❌ [API Reference](../reference/api.mdx)
```

### Mintlify Components

Use these MDX components for rich formatting:

```mdx
<Note>
Informational callout
</Note>

<Warning>
Critical warning
</Warning>

<Steps>
  <Step title="First">Do this</Step>
  <Step title="Second">Then this</Step>
</Steps>

<CodeGroup>
```js JavaScript
const code = 'here';
```
```python Python
code = "here"
```
</CodeGroup>

<CardGroup cols={2}>
  <Card title="Card 1" icon="rocket" href="/link">
    Card content
  </Card>
</CardGroup>
```

See `docs/manual/mintlify/mintlify.com-docs-components.md` for the complete component library.

---

## Deployment

### Auto-Deployment
Pushes to the **main branch** automatically deploy to the live site via Mintlify.

### Preview Deployments
Pushes to **other branches** create preview deployments (if configured in Mintlify dashboard).

### Manual Deployment
Not needed — Mintlify watches the GitHub repository and deploys automatically.

---

## Source Material

This documentation is migrated from the main ABP project at:
**[github.com/nicholasdao/agenticbrowserprotocol](https://github.com/nicholasdao/agenticbrowserprotocol)**

| Source File | Transformed To | Notes |
|-------------|----------------|-------|
| `README.md` | `introduction.mdx` + `quickstart.mdx` | Split into overview and quick start |
| `VERSIONING.md` | `reference/versioning.mdx` | Complete migration |
| `docs/glossary.md` | `glossary.mdx` | Complete migration |
| `docs/protocol-overview.md` | `concepts/protocol-overview.mdx` | Links transformed |
| `docs/architecture.md` | `concepts/architecture.mdx` | Links transformed |
| `docs/discovery.md` | `concepts/discovery.mdx` | Links transformed |
| `docs/capability-taxonomy.md` | `concepts/capabilities.mdx` | Links transformed |
| `docs/data-flow.md` | `concepts/data-flow.mdx` | Links transformed |
| `docs/elicitation-and-progress.md` | `concepts/elicitation-and-progress.mdx` | Links transformed |
| `docs/security.md` | `concepts/security.mdx` | Links transformed |
| `docs/building-abp-apps.md` | `guides/building-web-apps.mdx` | Links transformed |
| `docs/chrome-extension-guide.md` | `guides/chrome-extensions.mdx` | Links transformed |
| `docs/abp-implementation-guide.md` | `guides/implementation-guide.mdx` | Links transformed |
| `docs/common-pitfalls.md` | `guides/common-pitfalls.mdx` | Links transformed |
| `docs/examples.md` | `guides/examples.mdx` | Links transformed |
| `docs/quick-start-mcp-bridge.md` | `guides/mcp-bridge-quickstart.mdx` | Links transformed |
| `docs/mcp-bridge-architecture.md` | `guides/mcp-bridge-architecture.mdx` | Links transformed |
| `docs/troubleshooting.md` | `guides/troubleshooting.mdx` | Links transformed |
| `docs/api-reference.md` | `reference/api.mdx` | Links transformed |
| `docs/error-handling.md` | `reference/error-handling.mdx` | Links transformed |
| `docs/binary-data-protocol.md` | `reference/binary-data.mdx` | Links transformed |
| `docs/cancellation.md` | `reference/cancellation.mdx` | Links transformed |
| `docs/conformance.md` | `reference/conformance.mdx` | Links transformed |
| `docs/implementation-app-side.md` | `reference/app-side.mdx` | Links transformed |
| `docs/implementation-client-side.md` | `reference/client-side.mdx` | Links transformed |

**All transformations:**
- Internal links converted from `./docs/xxx.md` to `/section/page` format
- Table of Contents sections removed (Mintlify auto-generates)
- Mintlify components added (`<Note>`, `<Warning>`, `<Steps>`, `<Card>`, etc.)
- Frontmatter added to every page

---

## Keeping Docs in Sync

### Source of Truth

The **main ABP repository** at `/Users/nicolasdao/cloudless/agenticbrowserprotocol` (or `github.com/nicholasdao/agenticbrowserprotocol`) is the source of truth for:
- Protocol specification (`docs/*.md`)
- API definitions
- Examples and code samples
- Versioning information

This **docs repository** is a Mintlify-formatted mirror of that content.

### When to Update This Docs Site

Update this documentation when:
- ✅ **Protocol changes** — New capabilities, API changes, breaking changes
- ✅ **Documentation improvements** — Better examples, clearer explanations, new guides
- ✅ **Version bumps** — Update version numbers in relevant pages
- ✅ **Bug fixes** — Correct inaccuracies or outdated information
- ✅ **New features** — MCP Bridge updates, new implementation patterns

### Sync Workflow

#### Manual Sync (Current Process)

When docs change in the main ABP repo:

1. **Identify changed files** in `/Users/nicolasdao/cloudless/agenticbrowserprotocol/docs/`
2. **Find corresponding MDX files** in this repo (use the mapping table above)
3. **Update the MDX files** with the new content:
   - Copy the updated content
   - Transform internal links (`.md` → Mintlify paths)
   - Ensure Mintlify components are used appropriately
   - Preserve frontmatter
4. **Test locally** with `npx mint dev`
5. **Commit and push** to deploy

#### Automated Sync (Future Enhancement)

Potential automation options:
- **GitHub Action** that detects changes in the main repo and creates a PR in the docs repo
- **Script** that reads main repo files and regenerates Mintlify MDX
- **Webhook** that triggers a sync when main repo docs change

### Version Number Updates

When the ABP protocol version changes:

**Files to update:**
- `introduction.mdx` → "Project Status" section
- `reference/versioning.mdx` → Version tables
- Any code examples showing `protocolVersion: '0.1'`

**Search and replace:**
```bash
# Find all references to old version
grep -r "0.1.0-alpha" .

# Update protocol version in examples
grep -r 'protocolVersion: "0.1"' .
```

### Keeping the Mapping Updated

The **Source Material** table above maps source files to MDX files. When you:
- **Add a new doc** in the main repo → Create corresponding MDX file and add to this table
- **Delete a doc** in the main repo → Remove MDX file and update this table
- **Rename a doc** in the main repo → Rename MDX file and update this table

---

## Key Documentation Sections

### Essential Reading (Start Here)

**For everyone:**
- `introduction.mdx` — What ABP is and why it matters

**For app developers:**
- `guides/building-web-apps.mdx` — Your starting point
- `guides/common-pitfalls.mdx` — Read before shipping ⚠️

**For agent users:**
- `guides/mcp-bridge-quickstart.mdx` — Setup and usage

### Deep Dives

**Protocol internals:**
- `concepts/protocol-overview.mdx` — Simplified explanation
- `concepts/architecture.mdx` — Complete system architecture
- `reference/api.mdx` — Authoritative API spec

**Capability system:**
- `concepts/capabilities.mdx` — Naming and taxonomy
- `guides/implementation-guide.mdx` → "Step 2: Map Features to ABP Capabilities"
- `guides/common-pitfalls.mdx` → Capability anti-patterns

**Data handling:**
- `concepts/data-flow.mdx` — Client-side routing strategy
- `reference/binary-data.mdx` — Protocol-level binary format
- `guides/implementation-guide.mdx` → "The PDF/Print Pattern"

**Communication:**
- `concepts/elicitation-and-progress.mdx` — Bidirectional patterns
- `reference/api.mdx` → "Communication Methods"

### Critical Pages (Don't Skip)

1. **`guides/common-pitfalls.mdx`** ⚠️ — Most apps that fail do so because of patterns in this doc
2. **`reference/conformance.mdx`** — Minimum requirements for compliance
3. **`guides/implementation-guide.mdx`** → "The Critical Rule" — The foundational principle

---

## Technology: Why Mintlify?

This documentation uses **Mintlify** as its platform because:

1. **Built for technical docs** — Code blocks, API references, versioning, search
2. **MDX-based** — Write in Markdown with React components for rich formatting
3. **Git-native** — Docs live in version control, use standard Git workflows
4. **Auto-deploy** — Push to GitHub → site updates automatically
5. **AI-powered** — Built-in search assistant that answers questions about ABP
6. **Developer-friendly** — Local preview with `npx mint dev`, hot reload

**Mintlify vs alternatives:**
- **vs static site generators (Hugo, Jekyll):** Mintlify is specialized for technical documentation with built-in API reference generation, search, and versioning
- **vs Docusaurus:** Mintlify requires less configuration and offers better out-of-the-box search and AI features
- **vs GitBook/ReadTheDocs:** Mintlify offers better customization and modern UI components

---

## Mintlify Features Used in This Project

| Feature | Where It's Used |
|---------|-----------------|
| **Tabs** | 3 main tabs: Documentation, Guides, Reference |
| **Groups** | 7 groups organizing 26 pages |
| **Steps component** | Procedural guides (`building-web-apps.mdx`, `conformance.mdx`, etc.) |
| **Code groups** | Multi-language examples (`examples.mdx`) |
| **Callouts** | `<Note>`, `<Warning>`, `<Tip>` throughout all pages |
| **Cards** | Navigation cards in "Next Steps" sections |
| **Accordions** | Collapsible sections (`versioning.mdx` → "Common Scenarios") |
| **Syntax highlighting** | JavaScript, TypeScript, JSON, HTML, Bash, Python |
| **Auto-generated TOC** | Every page has automatic table of contents |
| **Feedback** | Thumbs up/down on every page |

---

## Contributing to This Documentation

### Who Can Contribute

- **ABP project maintainers:** Update docs when the protocol changes
- **Community members:** Fix typos, improve examples, clarify confusing sections
- **Users who found issues:** Report bugs or unclear explanations

### How to Contribute

**Small fixes (typos, clarifications):**
```bash
# Edit directly and commit
git add <file>
git commit -m "docs: fix typo in building-web-apps guide"
git push
```

**Larger changes (new sections, restructuring):**
```bash
# Create a branch
git checkout -b improve-capability-docs

# Make changes, test locally
npx mint dev

# Commit and push
git add .
git commit -m "docs: expand capability taxonomy with more examples"
git push origin improve-capability-docs

# Open a pull request on GitHub
```

### Content Guidelines

1. **Be concise** — Developers scan, they don't read word-for-word
2. **Show code** — Code examples are more valuable than prose
3. **Use components** — `<Warning>` for critical info, `<Steps>` for procedures
4. **Link liberally** — Help readers find related information
5. **Update both places** — If you update the spec in the main repo, update these docs too

---

## Questions & Support

### About the ABP Protocol
- **Issues:** [github.com/nicholasdao/agenticbrowserprotocol/issues](https://github.com/nicholasdao/agenticbrowserprotocol/issues)
- **Discussions:** Use GitHub Discussions on the main repo

### About This Documentation Site
- **Issues:** Open an issue in this repository
- **Mintlify support:** [mintlify.com/docs/contact-support](https://mintlify.com/docs/contact-support)

---

## Additional Resources

### Mintlify Documentation (Local Reference)
We maintain a local copy of Mintlify docs in `docs/manual/mintlify/` for offline reference:
- Component reference
- Configuration options
- Best practices
- Deployment guides

### External Links
- **ABP Main Repository:** [github.com/nicholasdao/agenticbrowserprotocol](https://github.com/nicholasdao/agenticbrowserprotocol)
- **Mintlify Platform:** [mintlify.com](https://mintlify.com)
- **Mintlify Docs:** [mintlify.com/docs](https://mintlify.com/docs)
- **Model Context Protocol:** [modelcontextprotocol.io](https://modelcontextprotocol.io)

---

## Quick Reference

### Most Important Files

| File | Purpose |
|------|---------|
| `docs.json` | Site configuration — navigation, theme, metadata |
| `introduction.mdx` | Homepage — first thing visitors see |
| `guides/building-web-apps.mdx` | Most common entry point for developers |
| `guides/common-pitfalls.mdx` | Critical reading before shipping |
| `reference/api.mdx` | Authoritative API specification |

### Commands

```bash
# Preview locally
npx mint dev

# Find broken links (requires Mintlify CLI)
npx mint broken-links

# Validate all MDX files
npx mint validate
```

---

## License & Community

**License:** BSD 3-Clause License — see [LICENSE](LICENSE) file for full terms.

ABP is an **open source protocol** built for the community. The specification, reference implementation, and documentation are all open and freely available. We encourage:

- **Using ABP** in your projects (commercial or non-commercial)
- **Building ABP apps** and sharing them with the community
- **Contributing** improvements to the protocol and documentation
- **Building clients** in different languages and environments
- **Joining discussions** about protocol design and evolution

This is a community-driven project. Your contributions, feedback, and implementations help shape the future of browser-AI interaction.

---

**Built by [Nic Dao](https://github.com/nicholasdao) • Documentation powered by [Mintlify](https://mintlify.com)**

**License:** BSD 3-Clause • **Status:** Open Source Community Project
