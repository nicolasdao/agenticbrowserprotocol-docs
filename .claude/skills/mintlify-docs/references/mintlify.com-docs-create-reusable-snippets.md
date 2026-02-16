---
url: https://mintlify.com/docs/create/reusable-snippets
canonical: https://www.mintlify.com/docs/create/reusable-snippets
title: "Reusable snippets - Mintlify"
description: "Create reusable snippets to maintain consistency across pages."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Create content

Reusable snippets

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

One of the core principles of software development is DRY (Don’t Repeat Yourself), which applies to documentation too. If you find yourself repeating the same content in multiple places, create a custom snippet for that content. Snippets contain content that you can import into other files to reuse. You control where the snippet appears on a page. If you ever need to update the content, you only need to edit the snippet rather than every file where the snippet is used.

##

[​](#how-snippets-work)

How snippets work

Snippets are any `.mdx`, `.md`, or `.jsx` files imported into another file. You can place snippet files anywhere in your project. When you import a snippet into another file, the snippet only appears where you import it and does not render as a standalone page. Any file in the `/snippets/` folder is always a snippet even if it is not imported into another file.

##

[​](#create-snippets)

Create snippets

Create a file with the content you want to reuse. Snippets can contain all content types supported by Mintlify and they can import other snippets.

##

[​](#import-snippets-into-pages)

Import snippets into pages

Import snippets into pages using either an absolute or relative path.

- **Absolute imports**: Start with `/` for imports from the root of your project.
- **Relative imports**: Use `./` or `../` to import snippets relative to the current file’s location.

Relative imports enable IDE navigation. Press CMD and click a snippet name in your editor to jump directly to the snippet definition.

###

[​](#import-text)

Import text

1.  Add content to your snippet file that you want to reuse.

    shared/my-snippet.mdx

    ```
    Hello world! This is my content I want to reuse across pages.
    ```

2.  Import the snippet into your destination file using either an absolute or relative path.

    Absolute import

    Relative import

    ```
    ---
    title: "An example page"
    description: "This is an example page that imports a snippet."
    ---

    import MySnippet from "/shared/my-snippet.mdx";

    The snippet content displays beneath this sentence.

    <MySnippet />
    ```


###

[​](#import-variables)

Import variables

Reference variables from a snippet in a page.

1.  Export variables from a snippet file.

    shared/custom-variables.mdx

    ```
    export const myName = "Ronan";

    export const myObject = { fruit: "strawberries" };

    ;
    ```

2.  Import the snippet from your destination file and use the variable.

    destination-file.mdx

    ```
    ---
    title: "An example page"
    description: "This is an example page that imports a snippet with variables."
    ---

    import { myName, myObject } from "/shared/custom-variables.mdx";

    Hello, my name is {myName} and I like {myObject.fruit}.
    ```


###

[​](#import-snippets-with-variables)

Import snippets with variables

Use variables to pass data to a snippet when you import it.

1.  Add variables to your snippet and pass in properties when you import it. In this example, the variable is `{word}`.

    shared/my-snippet.mdx

    ```
    My keyword of the day is {word}.
    ```

2.  Import the snippet into your destination file with the variable. The passed property replaces the variable in the snippet definition.

    destination-file.mdx

    ```
    ---
    title: "An example page"
    description: "This is an example page that imports a snippet with a variable."
    ---

    import MySnippet from "/shared/my-snippet.mdx";

    <MySnippet word="bananas" />
    ```


###

[​](#import-react-components)

Import React components

1.  Create a snippet with a JSX component. See [React components](https://www.mintlify.com/docs/customize/react-components) for more information.

    components/my-jsx-snippet.jsx

    ```
    export const MyJSXSnippet = () => {
      return (
        <div>
          <h1>Hello, world!</h1>
        </div>
      );
    };
    ```


When creating JSX snippets, use arrow function syntax (`=>`) rather than function declarations. The `function` keyword is not supported in snippets.

2.  Import the snippet.

    destination-file.mdx

    ```
    ---
    title: "An example page"
    description: "This is an example page that imports a snippet with a React component."
    ---

    import { MyJSXSnippet } from "/components/my-jsx-snippet.jsx";

    <MyJSXSnippet />
    ```


Was this page helpful?

YesNo

[Lists and tablesPrevious](https://www.mintlify.com/docs/create/list-table)[Personalized contentNext](https://www.mintlify.com/docs/create/personalization)

⌘I
