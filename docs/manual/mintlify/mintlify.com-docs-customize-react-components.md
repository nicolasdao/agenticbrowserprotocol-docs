---
url: https://mintlify.com/docs/customize/react-components
canonical: https://www.mintlify.com/docs/customize/react-components
title: "React - Mintlify"
description: "Build interactive and reusable elements with React components."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Customize

React

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

[React components](https://react.dev) are a powerful way to create interactive and reusable elements in your documentation.

##

[​](#using-react-components)

Using React components

You can build React components directly in your MDX files using [React hooks](https://react.dev/reference/react/hooks).

###

[​](#example)

Example

This example declares a `Counter` component and then uses it with `<Counter />`.
```
export const Counter = () => {
  const [count, setCount] = useState(0)

  const increment = () => setCount(count + 1)
  const decrement = () => setCount(count - 1)

  return (
  <div className="flex items-center justify-center">
      <div className="flex items-center rounded-xl overflow-hidden border border-zinc-950/20 dark:border-white/20">
        <button
          onClick={decrement}
          className="flex items-center justify-center h-8 w-8 text-zinc-950/80 dark:text-white/80 border-r border-zinc-950/20 dark:border-white/20"
          aria-label="Decrease"
        >
          -
        </button>

        <div className="flex text-sm items-center justify-center h-8 px-6 text-zinc-950/80 dark:text-white/80 font-medium min-w-[4rem] text-center">
          {count}
        </div>

        <button
          onClick={increment}
          className="flex items-center justify-center h-8 w-8 text-zinc-950/80 dark:text-white/80 border-l border-zinc-950/20 dark:border-white/20"
          aria-label="Increase"
        >
          +
        </button>
      </div>
    </div>
  )
}

<Counter />
```
The counter renders as an interactive React component.

\-

0

+ ##

[​](#importing-components)

Importing components

To import React components in your MDX files, the component files must be located in the `/snippets/` folder. Learn more about [reusable snippets](https://www.mintlify.com/docs/create/reusable-snippets).

Nested imports are not supported. If a React component references other components, you must import all components directly into the parent MDX file rather than importing components within component files.

###

[​](#example-2)

Example

This example declares a `ColorGenerator` component that uses multiple React hooks and then uses it in an MDX file. Create `color-generator.jsx` file in the `snippets` folder:

/snippets/color-generator.jsx
```
export const ColorGenerator = () => {
  const [hue, setHue] = useState(180)
  const [saturation, setSaturation] = useState(50)
  const [lightness, setLightness] = useState(50)
  const [colors, setColors] = useState([])

  useEffect(() => {
    const newColors = []
    for (let i = 0; i < 5; i++) {
      const l = Math.max(10, Math.min(90, lightness - 20 + i * 10))
      newColors.push(`hsl(${hue}, ${saturation}%, ${l}%)`)
    }
    setColors(newColors)
  }, [hue, saturation, lightness])

  const copyToClipboard = (color) => {
    navigator.clipboard
      .writeText(color)
      .then(() => {
        console.log(`Copied ${color} to clipboard!`)
      })
      .catch((err) => {
        console.error("Failed to copy: ", err)
      })
  }

  return (
    <div className="p-4 border dark:border-zinc-950/80 rounded-xl not-prose">
      <div className="space-y-4">
        <div className="space-y-2">
          <label className="block text-sm text-zinc-950/70 dark:text-white/70">
            Hue: {hue}°
            <input
              type="range"
              min="0"
              max="360"
              value={hue}
              onChange={(e) => setHue(Number.parseInt(e.target.value))}
              className="w-full h-2 bg-zinc-950/20 rounded-lg appearance-none cursor-pointer dark:bg-white/20 mt-1"
              style={{
                background: `linear-gradient(to right,
                  hsl(0, ${saturation}%, ${lightness}%),
                  hsl(60, ${saturation}%, ${lightness}%),
                  hsl(120, ${saturation}%, ${lightness}%),
                  hsl(180, ${saturation}%, ${lightness}%),
                  hsl(240, ${saturation}%, ${lightness}%),
                  hsl(300, ${saturation}%, ${lightness}%),
                  hsl(360, ${saturation}%, ${lightness}%))`,
              }}
            />
          </label>

          <label className="block text-sm text-zinc-950/70 dark:text-white/70">
            Saturation: {saturation}%
            <input
              type="range"
              min="0"
              max="100"
              value={saturation}
              onChange={(e) => setSaturation(Number.parseInt(e.target.value))}
              className="w-full h-2 bg-zinc-950/20 rounded-lg appearance-none cursor-pointer dark:bg-white/20 mt-1"
              style={{
                background: `linear-gradient(to right,
                  hsl(${hue}, 0%, ${lightness}%),
                  hsl(${hue}, 50%, ${lightness}%),
                  hsl(${hue}, 100%, ${lightness}%))`,
              }}
            />
          </label>

          <label className="block text-sm text-zinc-950/70 dark:text-white/70">
            Lightness: {lightness}%
            <input
              type="range"
              min="0"
              max="100"
              value={lightness}
              onChange={(e) => setLightness(Number.parseInt(e.target.value))}
              className="w-full h-2 bg-zinc-950/20 rounded-lg appearance-none cursor-pointer dark:bg-white/20 mt-1"
              style={{
                background: `linear-gradient(to right,
                  hsl(${hue}, ${saturation}%, 0%),
                  hsl(${hue}, ${saturation}%, 50%),
                  hsl(${hue}, ${saturation}%, 100%))`,
              }}
            />
          </label>
        </div>

        <div className="flex space-x-1">
          {colors.map((color, idx) => (
            <div
              key={idx}
              className="h-16 rounded flex-1 cursor-pointer transition-transform hover:scale-105"
              style={{ backgroundColor: color }}
              title={`Click to copy: ${color}`}
              onClick={() => copyToClipboard(color)}
            />
          ))}
        </div>

        <div className="text-sm font-mono text-zinc-950/70 dark:text-white/70">
          <p>
            Base color: hsl({hue}, {saturation}%, {lightness}%)
          </p>
        </div>
      </div>
    </div>
  )
}
```
See all 110 lines

Import the `ColorGenerator` component and use it in an MDX file:
```
import { ColorGenerator } from "/snippets/color-generator.jsx"

<ColorGenerator />
```
The color generator renders as an interactive React component.

Hue: 165°Saturation: 84%Lightness: 31%

Base color: hsl(165, 84%, 31%)

##

[​](#considerations)

Considerations

Client-side rendering impact

React hook components render on the client-side, which has several implications:

- **SEO**: Search engines might not fully index dynamic content.
- **Initial load**: Visitors may experience a flash of loading content before components render.
- **Accessibility**: Ensure dynamic content changes are announced to screen readers.

Performance best practices

- **Optimize dependency arrays**: Include only necessary dependencies in your `useEffect` dependency arrays.
- **Memoize complex calculations**: Use `useMemo` or `useCallback` for expensive operations.
- **Reduce re-renders**: Break large components into smaller ones to prevent cascading re-renders.
- **Lazy loading**: Consider lazy loading complex components to improve initial page load time.

Was this page helpful?

YesNo

[Custom scriptsPrevious](https://www.mintlify.com/docs/customize/custom-scripts)[Custom 404 pageNext](https://www.mintlify.com/docs/customize/custom-404-page)

⌘I
