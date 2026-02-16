---
url: https://mintlify.com/docs/installation
canonical: https://www.mintlify.com/docs/installation
title: "Install the CLI - Mintlify"
description: "Use the CLI to preview docs locally, test changes in real-time, and catch issues before deploying your documentation site."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Create content

Install the CLI

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

![Decorative graphic representing the CLI.](https://mintcdn.com/mintlify/Y6rP0BmbzgwHuEoU/images/installation/local-development-light.png?fit=max&auto=format&n=Y6rP0BmbzgwHuEoU&q=85&s=ffd8bc88d87fc00fe1919a33a292fa01) ![Decorative graphic representing the CLI.](https://mintcdn.com/mintlify/Y6rP0BmbzgwHuEoU/images/installation/local-development-dark.png?fit=max&auto=format&n=Y6rP0BmbzgwHuEoU&q=85&s=ef0bb527eb258f8d720180d106ea6625) Use the [CLI](https://www.npmjs.com/package/mint) to preview your documentation locally as you write and edit. View changes in real-time before deploying, test your documentation site’s appearance and functionality, and catch issues like broken links or accessibility problems. The CLI also has utilities for maintaining your documentation, including commands to rename files, validate OpenAPI specifications, and migrate content between formats.

##

[​](#prerequisites)

Prerequisites

- [Node.js](https://nodejs.org/en) v20.17.0+ (LTS versions recommended) installed
- [Git](https://git-scm.com/downloads) installed
- Your documentation repository cloned locally

###

[​](#clone-your-repository)

Clone your repository

1

[](#)

Locate your repository

1.  Go to the [Git settings](https://dashboard.mintlify.com/settings/deployment/git-settings) page of your dashboard.
2.  Note your repository location. It is one of these formats:

- `mintlify-community/docs-{org-name}-{id}` (Mintlify-hosted repository)
- `your-org/your-repo` (your own GitHub repository)

2

[](#)

Clone your repository

- Your own repository

- Mintlify-hosted repository


Replace `your-org/your-repo` with your actual repository details from [Git settings](https://dashboard.mintlify.com/settings/deployment/git-settings).
```
git clone https://github.com/your-org/your-repo
cd your-repo
```
**GitHub App required.** To enable automatic deployments when you push changes, you must install the GitHub app. See [GitHub](https://www.mintlify.com/docs/deploy/github) for more information.

You can clone your repository as a private or public repository. Public repositories are visible to anyone who navigates to the repository URL. Private repositories are only visible to people in your organization.On the [Git settings](https://dashboard.mintlify.com/settings/deployment/git-settings) page of your dashboard, select **Clone as private** or **Clone as public**.

##

[​](#install-the-cli)

Install the CLI

Run the following command to install the CLI:

npm

pnpm
```
npm i -g mint
```

##

[​](#preview-locally)

Preview locally

Navigate to your documentation directory containing your `docs.json` file and run:
```
mint dev
```
A local preview of your documentation is available at `http://localhost:3000`. Alternatively, if you do not want to install the CLI globally, you can run a one-time script:
```
npx mint dev
```

###

[​](#custom-ports)

Custom ports

By default, the CLI uses port 3000. You can customize the port using the `--port` flag. To run the CLI on port 3333, for instance, use this command:
```
mint dev --port 3333
```
If you attempt to run on a port that is already in use, the CLI uses the next available port:
```
Port 3000 is already in use. Trying 3001 instead.
```

##

[​](#skip-openapi-processing)

Skip OpenAPI processing

If you have many OpenAPI files, skip OpenAPI file processing during local development to improve performance by using the `--disable-openapi` flag:
```
mint dev --disable-openapi
```

###

[​](#preview-as-a-specific-group)

Preview as a specific group

If you use group-based access control to restrict access to your documentation, you can preview as a specific authentication group by using the `--groups [groupname]` flag. For example, if you have a group named `admin`, you can preview as a member of that group with the command:
```
mint dev --groups admin
```

##

[​](#create-a-new-project)

Create a new project

To create a new documentation project, run the following command:
```
mint new [directory]
```
This command clones the [starter kit](https://github.com/mintlify/starter) into a specified directory. If you do not specify a directory, the CLI tool prompts you to create a new subdirectory or overwrite the current directory.

Overwriting the current directory deletes any existing files.

The CLI tool prompts you for a project name and [theme](https://www.mintlify.com/docs/customize/themes) to finish setting up your project.

###

[​](#flags)

Flags

| Flag | Description | Required |
| --- | --- | --- |
| `--name` | Set the name of the new project. | Yes |
| `--theme` | Set the [theme](https://www.mintlify.com/docs/customize/themes) of the new project. | Yes |
| `--force` | Overwrite the current directory without prompting, even if it contains existing files. | No |

When running `mint new` in non-interactive environments like CI/CD pipelines or with AI coding agents, you must provide all required flags (`--name` and `--theme`).

The CLI automatically detects non-interactive environments. If required flags are missing, it outputs usage instructions instead of hanging on prompts.

##

[​](#update-the-cli)

Update the CLI

If your local preview is out of sync with what you see on the web in the production version, update your local CLI:
```
mint update
```
If this `mint update` command is not available on your local version, re-install the CLI with the latest version:

npm

pnpm
```
npm i -g mint@latest
```

##

[​](#additional-commands)

Additional commands

###

[​](#find-broken-links)

Find broken links

Identify any broken internal links with the following command:
```
mint broken-links
```
The command ignores files matching [.mintignore](https://www.mintlify.com/docs/organize/mintignore) patterns. Links that point to ignored files are reported as broken.

###

[​](#find-accessibility-issues)

Find accessibility issues

Test the color contrast ratios and search for missing alt text on images and videos in your documentation with the following command:
```
mint a11y
```
Use flags to check for specific accessibility issues.
```

# Check only for missing alt text
mint a11y --skip-contrast

# Check only for color contrast issues
mint a11y --skip-alt-text
```

###

[​](#validate-documentation-build)

Validate documentation build

Validate your documentation build in strict mode, which exits with an error if there are any warnings or errors. Use this command for CI/CD pipelines to prevent broken documentation deployments.
```
mint validate
```
Use flags to configure the validation command.

- `--groups [groupname]`: Mock user groups for validation (useful when testing group-based access control)
- `--disable-openapi`: Disable OpenAPI file generation during validation

###

[​](#check-openapi-spec)

Check OpenAPI spec

Check your OpenAPI file for errors with the following command:
```
mint openapi-check <OpenAPI filename or URL>
```
Pass a filename (for example, `./openapi.yaml`) or a URL (for example, `https://petstore3.swagger.io/api/v3/openapi.json`).

###

[​](#rename-files)

Rename files

Rename and update all references to files with the following command:
```
mint rename <path/to/old-filename> <path/to/new-filename>
```

###

[​](#migrate-mdx-endpoint-pages)

Migrate MDX endpoint pages

Migrate MDX endpoint pages to autogenerated pages from your OpenAPI specification with the following command:
```
mint migrate-mdx
```
This command converts individual MDX endpoint pages to autogenerated pages defined in your `docs.json`, moves MDX content to the `x-mint` extension in your OpenAPI specification, and updates your navigation. See [Migrating from MDX](https://www.mintlify.com/docs/guides/migrating-from-mdx) for detailed information.

##

[​](#formatting)

Formatting

While developing locally, we recommend using extensions in your IDE to recognize and format MDX files. If you use Cursor, Windsurf, or VS Code, we recommend the [MDX VS Code extension](https://marketplace.visualstudio.com/items?itemName=unifiedjs.vscode-mdx) for syntax highlighting, and [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) for code formatting. If you use JetBrains, we recommend the [MDX IntelliJ IDEA plugin](https://plugins.jetbrains.com/plugin/14944-mdx) for syntax highlighting, and setting up [Prettier](https://prettier.io/docs/webstorm) for code formatting.

##

[​](#troubleshooting)

Troubleshooting

Error: Could not load the "sharp" module using the darwin-arm64 runtime

This may be due to an outdated version of Node.js. Try the following:

1.  Remove the currently-installed version of the mint CLI: `npm uninstall -g mint`
2.  Upgrade to Node.js v20.17.0+.
3.  Reinstall the mint CLI: `npm install -g mint`

Issue: Encountering an unknown error

**Solution**: Go to the root of your device and delete the `~/.mintlify` folder. Afterwards, run `mint dev` again.

Error: permission denied

This is due to not having the required permissions to globally install node packages.**Solution**: Try running `sudo npm i -g mint`. You will be prompted for your password, which is the one you use to unlock your computer.

The local preview doesn't look the same as my docs do on the web

This is likely due to an outdated version of the CLI.**Solution:** Run `mint update` to get the latest changes.

mintlify vs. mint package

If you have any problems with the CLI package, you should first run `npm ls -g`. This command shows what packages are globally installed on your machine.If you don’t use npm or don’t see it in the -g list, try `which mint` to locate the installation.If you have a package named `mint` and a package named `mintlify` installed, you should uninstall `mintlify`.

1.  Uninstall the old package:
```
  npm uninstall -g mintlify
```
2.  Clear your npm cache:
```
  npm cache clean --force
```
3.  Reinstall the new package:
```
npm i -g mint
```
Client version shows 'none' after installation

If you run `mint version` and the client version displays as `none`, the CLI may be unable to download the client application due to a corporate firewall or VPN blocking the download.**Solution:** Ask your IT administrator to whitelist `releases.mintlify.com` to enable local development with the CLI.

Was this page helpful?

YesNo

[Keyboard shortcutsPrevious](https://www.mintlify.com/docs/editor/keyboard-shortcuts)[Format textNext](https://www.mintlify.com/docs/create/text)

⌘I

![Decorative graphic representing the CLI.](https://mintcdn.com/mintlify/Y6rP0BmbzgwHuEoU/images/installation/local-development-dark.png?w=1650&fit=max&auto=format&n=Y6rP0BmbzgwHuEoU&q=85&s=9b79a51b960489e0d41ffd61b9d7120d)
