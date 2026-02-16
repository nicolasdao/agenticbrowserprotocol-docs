---
url: https://mintlify.com/docs/ai/model-context-protocol
canonical: https://www.mintlify.com/docs/ai/model-context-protocol
title: "Model Context Protocol - Mintlify"
description: "Connect your documentation and API endpoints to AI tools with a hosted MCP server."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Optimize

Model Context Protocol

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

##

[​](#about-mcp-servers)

About MCP servers

The Model Context Protocol (MCP) is an open protocol that creates standardized connections between AI applications and external services, like documentation. Mintlify generates an MCP server from your documentation, preparing your content for the broader AI ecosystem where any MCP client like Claude, Cursor, Goose, ChatGPT, and others can connect to your documentation. Your MCP server exposes a search tool for AI applications to query your documentation. Your users must connect your MCP server to their tools.

###

[​](#how-mcp-servers-work)

How MCP servers work

When an AI application connects to your documentation MCP server, it can search your documentation directly instead of making a generic web search in response to a user’s prompt. Your MCP server provides access to all indexed content on your documentation site.

- The AI application can proactively search your documentation while generating a response, not just when explicitly asked.
- The AI application determines when to use the search tool based on the context of the conversation and the relevance of your documentation.
- Each search (tool call) happens during the generation process, so the AI application searches up-to-date information from your documentation to generate its response.

Some AI tools like Claude support both MCP and Skills. MCP gives the AI access to your documentation content, while Skills instruct the AI how to use that content effectively. They’re complementary. MCP provides the data and Skills provide the instructions.

###

[​](#search-filtering-parameters)

Search filtering parameters

The MCP search tool supports optional filtering parameters that AI applications can use to narrow search results.

- **`version`**: Filter results to a specific documentation version. For example, `'v0.7'`. Only returns content tagged with the specified version or content available across all versions.
- **`language`**: Filter results to a specific language code. For example, `'en'`, `'zh'`, or `'es'`. Only returns content in the specified language or content available across all languages.

AI applications determine when to apply these filters based on the context of the user’s query. For example, if a user asks about a specific API version, the AI application may automatically apply the appropriate filter to provide more relevant results.

###

[​](#mcp-compared-to-web-search)

MCP compared to web search

AI tools can search the web, but MCP provides distinct advantages for documentation.

- **Direct source access**: Web search depends on what search engines have indexed, which may be stale or incomplete. MCP searches your current indexed documentation directly.
- **Integrated workflow**: MCP allows the AI to search during response generation rather than performing a separate web search.
- **No search noise**: SEO and ranking algorithms influence web search results. MCP goes straight to your documentation content.

##

[​](#access-your-mcp-server)

Access your MCP server

MCP servers are only available for public documentation. Documentation behind end-user authentication cannot generate an MCP server.

Mintlify automatically generates an MCP server for your documentation and hosts it at your documentation URL with the `/mcp` path. For example, Mintlify’s MCP server is available at `https://mintlify.com/docs/mcp`. View and copy your MCP server URL on the [MCP server page](https://dashboard.mintlify.com/products/mcp) in your dashboard.

![MCP server page in the dashboard.](https://mintcdn.com/mintlify/l_uyIoyoCoduAB2a/images/mcp/mcp-server-page-light.png?fit=max&auto=format&n=l_uyIoyoCoduAB2a&q=85&s=fe99ba970692e913694abeda27db201f)![MCP server page in the dashboard.](https://mintcdn.com/mintlify/l_uyIoyoCoduAB2a/images/mcp/mcp-server-page-dark.png?fit=max&auto=format&n=l_uyIoyoCoduAB2a&q=85&s=81739348dcafa3573ecc588a8ca38fbe)

Hosted MCP servers use the `/mcp` path in their URLs. Other navigation elements cannot use the `/mcp` path.

###

[​](#rate-limits)

Rate limits

To protect availability, Mintlify applies rate limits to MCP servers.

| Scope | Limit | Description |
| --- | --- | --- |
| Per user (IP address) | 200 requests per hour | Limits how frequently a single user can search your documentation. |
| Per documentation site (domain) | 1,000 requests per hour | Limits total searches across all users of your MCP server. |

##

[​](#content-filtering-and-indexing)

Content filtering and indexing

Your MCP server searches content that Mintlify indexes from your documentation repository. File processing and search indexing control what content is available through your MCP server.

###

[​](#file-processing-with-mintignore)

File processing with `.mintignore`

If files match [.mintignore](https://www.mintlify.com/docs/organize/mintignore) patterns, Mintlify does not process or index them. These files are not available through your MCP server.

###

[​](#search-indexing-with-docs-json)

Search indexing with `docs.json`

By default, Mintlify only indexes pages included in your `docs.json` navigation for search through your MCP server. Mintlify excludes [hidden pages](https://www.mintlify.com/docs/organize/hidden-pages) (pages not in your navigation) from the search index unless you choose to index all pages. To include hidden pages in your MCP server’s search results, add the `seo.indexing` property to your `docs.json`.
```
"seo": {
    "indexing": "all"
}
```
To exclude a specific page from search indexing, add `noindex: true` to its frontmatter.
```
---
title: "Hidden page"
description: "This page is not in the navigation and is not available through search."
noindex: true
---
```

##

[​](#use-your-mcp-server)

Use your MCP server

Your users must connect your MCP server to their preferred AI tools.

1.  Make your MCP server URL publicly available.
2.  Users copy your MCP server URL and add it to their tools.
3.  Users access your documentation through their tools.

These are some of the ways you can help your users connect to your MCP server:

- Contextual menu

- Claude

- Claude Code

- Cursor

- VS Code


Add options in the [contextual menu](https://www.mintlify.com/docs/ai/contextual-menu) for your users to connect to your MCP server from any page of your documentation.

| Option | Identifier | Description |
| --- | --- | --- |
| **Copy MCP server URL** | `mcp` | Copies your MCP server URL to the user’s clipboard. |
| **Copy MCP install command** | `add-mcp` | Copies the `npx add-mcp` command to install the MCP server. |
| **Connect to Cursor** | `cursor` | Installs your MCP server in Cursor. |
| **Connect to VS Code** | `vscode` | Installs your MCP server in VS Code. |

1

[](#)

Get your MCP server URL.

Navigate to your [dashboard](https://dashboard.mintlify.com/products/mcp) and find your MCP server URL.

2

[](#)

Publish your MCP server URL for your users.

Create a guide for your users that includes your MCP server URL and the steps to connect it to Claude.

1.  Navigate to the [Connectors](https://claude.ai/settings/connectors) page in the Claude settings.
2.  Select **Add custom connector**.
3.  Add your MCP server name and URL.
4.  Select **Add**.
5.  When using Claude, select the attachments button (the plus icon).
6.  Select your MCP server.

See the [Model Context Protocol documentation](https://modelcontextprotocol.io/docs/tutorials/use-remote-mcp-server#connecting-to-a-remote-mcp-server) for more details.

1

[](#)

Get your MCP server URL.

Navigate to your [dashboard](https://dashboard.mintlify.com/products/mcp) and find your MCP server URL.

2

[](#)

Publish your MCP server URL for your users.

Create a guide for your users that includes your MCP server URL and the command to connect it to Claude Code.
```
claude mcp add --transport http <name> <url>
```
See the [Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code/mcp#installing-mcp-servers) for more details.

1

[](#)

Get your MCP server URL.

Navigate to your [dashboard](https://dashboard.mintlify.com/products/mcp) and find your MCP server URL.

2

[](#)

Publish your MCP server URL for your users.

Create a guide for your users that includes your MCP server URL and the steps to connect it to Cursor.

1.  Use Command + Shift + P (Ctrl + Shift + P on Windows) to open the command palette.
2.  Search for “Open MCP settings”.
3.  Select **Add custom MCP**. This opens the `mcp.json` file.
4.  In `mcp.json`, configure your server:
```
{
  "mcpServers": {
    "<your-mcp-server-name>": {
      "url": "<your-mcp-server-url>"
    }
  }
}
```
See the [Cursor documentation](https://docs.cursor.com/en/context/mcp#installing-mcp-servers) for more details.

1

[](#)

Get your MCP server URL.

Navigate to your [dashboard](https://dashboard.mintlify.com/products/mcp) and find your MCP server URL.

2

[](#)

Publish your MCP server URL for your users.

Create a guide for your users that includes your MCP server URL and the steps to connect it to VS Code.

1.  Create a `.vscode/mcp.json` file.
2.  In `mcp.json`, configure your server:
```
{
  "servers": {
    "<your-mcp-server-name>": {
      "type": "http",
      "url": "<your-mcp-server-url>"
    }
  }
}
```
See the [VS Code documentation](https://code.visualstudio.com/docs/copilot/chat/mcp-servers) for more details.

###

[​](#example-connect-to-the-mintlify-mcp-server)

Example: Connect to the Mintlify MCP server

Connect to the Mintlify MCP server to search this documentation site within your preferred AI tool. This gives you more accurate answers about how to use Mintlify in your local environment and demonstrates how you can help your users connect to your MCP server.

- Contextual menu

- Claude

- Claude Code

- Cursor

- VS Code


At the top of this page, select the contextual menu and choose **Connect to Cursor** or **Connect to VS Code** to connect the Mintlify MCP server to the IDE of your choice.

To use the Mintlify MCP server with Claude:

1

[](#)

Add the Mintlify MCP server to Claude

1.  Navigate to the [Connectors](https://claude.ai/settings/connectors) page in the Claude settings.
2.  Select **Add custom connector**.
3.  Add the Mintlify MCP server:

- Name: `Mintlify`
- URL: `https://mintlify.com/docs/mcp`

4.  Select **Add**.

2

[](#)

Access the MCP server in your chat

1.  When using Claude, select the attachments button (the plus icon).
2.  Select the Mintlify MCP server.
3.  Ask Claude a question about Mintlify.

See the [Model Context Protocol documentation](https://modelcontextprotocol.io/docs/tutorials/use-remote-mcp-server#connecting-to-a-remote-mcp-server) for more details.

To use the Mintlify MCP server with Claude Code, run the following command:
```
claude mcp add --transport http Mintlify https://mintlify.com/docs/mcp
```
Test the connection by running:
```
claude mcp list
```
See the [Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code/mcp#installing-mcp-servers) for more details.

[Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=mintlify&config=eyJ1cmwiOiJodHRwczovL21pbnRsaWZ5LmNvbS9kb2NzL21jcCJ9)To connect the Mintlify MCP server to Cursor, click the **Install in Cursor** button. Or to manually connect the MCP server, follow these steps:

1

[](#)

Open MCP settings

1.  Use Command + Shift + P (Ctrl + Shift + P on Windows) to open the command palette.
2.  Search for “Open MCP settings”.
3.  Select **Add custom MCP**. This opens the `mcp.json` file.

2

[](#)

Configure the Mintlify MCP server

In `mcp.json`, add:
```
{
  "mcpServers": {
    "Mintlify": {
      "url": "https://mintlify.com/docs/mcp"
    }
  }
}
```
3

[](#)

Test the connection

In Cursor’s chat, ask “What tools do you have available?” Cursor should show the Mintlify MCP server as an available tool.

See [Installing MCP servers](https://docs.cursor.com/en/context/mcp#installing-mcp-servers) in the Cursor documentation for more details.

[Install in VS Code](https://vscode.dev/redirect/mcp/install?name=mintlify&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fmintlify.com%2Fdocs%2Fmcp%22%7D)To connect the Mintlify MCP server to VS Code, click the **Install in VS Code** button. Or to manually connect the MCP server, create a `.vscode/mcp.json` file and add:
```
{
  "servers": {
    "Mintlify": {
      "type": "http",
      "url": "https://mintlify.com/docs/mcp"
    }
  }
}
```
See the [VS Code documentation](https://code.visualstudio.com/docs/copilot/chat/mcp-servers) for more details.

###

[​](#using-multiple-mcp-servers)

Using multiple MCP servers

Users can connect multiple MCP servers to their AI tools. Connected MCP servers do not consume context until the AI calls a search tool. The AI decides when to search based on query relevance, so it doesn’t search every connected server for every question. When the AI searches, each query returns multiple results that add to the conversation’s context. If the AI searches several servers for a single question, this can use up significant context. Best practices for using multiple MCP servers:

- Connect only the MCP servers relevant to your current work.
- Be specific in your prompts so the AI searches the most relevant server.
- Disconnect servers you’re not actively using to reduce potential context usage.

Was this page helpful?

YesNo

[skill.mdPrevious](https://www.mintlify.com/docs/ai/skillmd)[SEONext](https://www.mintlify.com/docs/optimize/seo)

⌘I

![MCP server page in the dashboard.](https://mintcdn.com/mintlify/l_uyIoyoCoduAB2a/images/mcp/mcp-server-page-dark.png?w=1650&fit=max&auto=format&n=l_uyIoyoCoduAB2a&q=85&s=20bf80ca67cc899ffabeeee7bb21112f)
