---
url: https://mintlify.com/docs/deploy/ci
canonical: https://www.mintlify.com/docs/deploy/ci
title: "CI checks - Mintlify"
description: "Automate broken link checks, linting, and grammar validation in CI/CD."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Deploy

CI checks

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

[Pro and Enterprise plans](https://mintlify.com/pricing?ref=docs-ci) include CI checks for GitHub repositories.

Use CI checks to lint your docs for errors and provide warnings before you deploy. Mintlify CI checks run on pull requests against a configured deployment branch.

##

[​](#installation)

Installation

To begin, follow the steps on the [GitHub](https://www.mintlify.com/docs/deploy/github) page.

Only access to the repository where your documentation content exists is required, so it is highly recommended to only grant access to that repository.

##

[​](#configuration)

Configuration

Configure the CI checks enabled for a deployment by navigating to the [Add-ons](https://dashboard.mintlify.com/products/addons) page of your dashboard. Enable the checks that you want to run. When enabling checks, you can choose to run them at a `Warning` or `Blocking` level.

- A `Warning` level check will never provide a failure status, even if there is an error or suggestions.
- A `Blocking` level check will provide a failure status if there is an error or suggestions.

##

[​](#available-ci-checks)

Available CI checks

###

[​](#broken-links)

Broken links

Similar to how the [CLI link checker](https://www.mintlify.com/docs/installation#find-broken-links) works on your local machine, the broken link CI check automatically searches your documentation content for broken internal links. To see the results of this check, visit GitHub’s check results page for a specific commit.

###

[​](#vale)

Vale

[Vale](https://vale.sh/) is an open source rule-based prose linter which supports a range of document types, including Markdown and MDX. Use Vale to check for consistency of style and tone in your documentation. Mintlify supports automatically running Vale in a CI check and displaying the results as a check status.

####

[​](#configuration-2)

Configuration

If you have a `.vale.ini` file in the root content directory of your deployment, the Vale CI check uses that configuration file and any configuration files in your specified `stylesPath`. If you don’t have a Vale config file, the default configuration automatically loads.

Default vale.ini configuration
```

# Top level styles
StylesPath = /app/styles
MinAlertLevel = suggestion

# Inline HTML tags to ignore (code/tt for code snippets, img/url for links/images, a for anchor tags)
IgnoredScopes = code, tt, img, url, a
SkippedScopes = script, style, pre, figure

# Vocabularies
Vocab = Mintlify

# Packages
Packages = MDX

# Only match MDX
[*.mdx]
BasedOnStyles = Vale
Vale.Terms = NO # Enforces really harsh capitalization rules, keep off

# Ignore JSX/MDX-specific syntax patterns

# `import ...`, `export ...`

# `<Component ... />`

# `<Component>...</Component>`

# `{ ... }`
TokenIgnores = (?sm)((?:import|export) .+?$), \
(?<!`)(<\w+ ?.+ ?\/>)(?!`), \
(<[A-Z]\w+>.+?<\/[A-Z]\w+>)

# Exclude multiline JSX and curly braces

# `<Component \n ... />`
BlockIgnores = (?sm)^(<\w+\n .*\s\/>)$, \
(?sm)^({.+.*})
```
See all 31 lines

The default Vale vocabulary includes the following words.

Default Vale vocabulary
```
Mintlify
mintlify
VSCode
openapi
OpenAPI
GitHub
APIs

repo
npm
dev

Lorem
ipsum
impsum
amet

const
myName
myObject
bearerAuth
favicon
topbar
url
borderRadius
args
modeToggle
ModeToggle
isHidden
autoplay

_italic_
Strikethrough
Blockquotes
Blockquote
Singleline
Multiline

onboarding

async
await
boolean
enum
func
impl
init
instanceof
typeof
params
stdin
stdout
stderr
stdout
stdin
var
const
let
null
undefined
struct
bool

cors
csrf
env
xhr
xhr2
jwt
oauth
websocket
localhost
middleware
runtime
webhook
stdin
stdout

json
yaml
yml
md
txt
tsx
jsx
css
scss
html
png
jpg
svg

cdn
cli
css
dom
dto
env
git
gui
http
https
ide
jvm
mvc
orm
rpc
sdk
sql
ssh
ssl
tcp
tls
uri
url
ux
ui

nodejs
npm
yarn
pnpm
eslint
pytest
golang
rustc
kubectl
mongo
postgres
redis

JavaScript
TypeScript
Python
Ruby
Rust
Go
Golang
Java
Kotlin
Swift
Node.js
NodeJS
Deno

React
Vue
Angular
Next.js
Nuxt
Express
Django
Flask
Spring
Laravel
Redux
Vuex
TensorFlow
PostgreSQL
MongoDB
Redis
PNPM

Docker
Kubernetes
AWS
Azure
GCP
Terraform
Jenkins
CircleCI
GitLab
Heroku

Git
git
GitHub
GitLab
Bitbucket
VSCode
Visual Studio Code
IntelliJ
WebStorm
ESLint
eslint
Prettier
prettier
Webpack
webpack
Vite
vite
Babel
babel
Jest
jest
Mocha
Cypress
Postman

HTTP
HTTPS
OAuth
JWT
GraphQL
REST
WebSocket
TCP/IP

NPM
Yarn
PNPM
Pip
PIP
Cargo
RubyGems

Swagger
OpenAPI
Markdown
MDX
Storybook
TypeDoc
JSDoc

MySQL
PostgreSQL
MongoDB
Redis
Elasticsearch
DynamoDB

Linux
Unix
macOS
iOS

Firefox
Chromium
WebKit

config
ctx
desc
dir
elem
err
len
msg
num
obj
prev
proc
ptr
req
res
str
tmp
val
vars

todo
href
lang
nav
prev
next
toc
```
See all 268 lines

To add your own vocabulary for the default configuration, create a `styles/config/vocabularies/Mintlify` directory with `accept.txt` and `reject.txt` files.

- `accept.txt`: Words that should be ignored by the Vale linter. For example, product names or uncommon terms.
- `reject.txt`: Words that should be flagged as errors. For example, jargon or words that are not appropriate for the tone of your documentation.

Example Vale file structure
```
/your-project
  |- docs.json
  |- .vale.ini
  |- styles/
    |- config/
      |- vocabularies/
        |- Mintlify/
          |- accept.txt
          |- reject.txt
  |- example-page.mdx
```
Example monorepo Vale file structure
```
/your-monorepo
  |- main.ts
  |- docs/
    |- docs.json
    |- .vale.ini
    |- styles/
      |- config/
      |- vocabularies/
        |- Mintlify/
          |- accept.txt
          |- reject.txt
    |- example-page.mdx
  |- test/
```
For security reasons, absolute `stylesPath`, or `stylesPath` which include `..` values aren’t supported.Use relative paths and include the `stylesPath` in your repository.

####

[​](#packages)

Packages

Vale supports a range of [packages](https://vale.sh/docs/keys/packages), which can be used to check for spelling and style errors. Any packages you include in your repository under the correct `stylesPath` are automatically installed and used in your Vale configuration. For packages not included in your repository, you may specify any packages from the [Vale package registry](https://vale.sh/explorer), and they’re automatically downloaded and used in your Vale configuration.

For security reasons, automatically downloading packages that aren’t from the [Vale package registry](https://vale.sh/explorer) is **not** supported.

####

[​](#vale-with-mdx)

Vale with `MDX`

MDX native support requires Vale 3.10.0 or later. Check your Vale version with `vale --version`.

To use Vale’s in-document comments in MDX files, use MDX-style comments `{/* ... */}`:
```
{/* vale off */}

This text is ignored by Vale

{/* vale on */}
```
Vale automatically recognizes and respects these comments in MDX files without additional configuration. Use comments to skip lines or sections that should be ignored by the linter.

Was this page helpful?

YesNo

[External proxies with VercelPrevious](https://www.mintlify.com/docs/deploy/vercel-external-proxies)[GitHubNext](https://www.mintlify.com/docs/deploy/github)

⌘I
