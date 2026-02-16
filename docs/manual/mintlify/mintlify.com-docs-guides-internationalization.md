---
url: https://mintlify.com/docs/guides/internationalization
canonical: https://www.mintlify.com/docs/guides/internationalization
title: "Internationalization - Mintlify"
description: "Set up multi-language documentation to reach global audiences."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Best practices

Internationalization

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

Internationalization (i18n) is the process of designing software or content to work for different languages and locales. This guide explains how to structure files, configure navigation, and maintain translations effectively so that you can help users access your documentation in their preferred language and improve global reach.

##

[​](#file-structure)

File structure

Organize translated content in language-specific directories to keep your documentation maintainable and structure your navigation by language. Create a separate directory for each language using [ISO 639-1 language codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes). Place translated files in these directories with the same structure as your default language.

Show supported language codes

- `ar` - Arabic
- `cs` - Czech
- `cn` or `zh-Hans` - Chinese (Simplified)
- `zh-Hant` - Chinese (Traditional)
- `de` - German
- `en` - English
- `es` - Spanish
- `fr` - French
- `he` - Hebrew
- `hi` - Hindi
- `id` - Indonesian
- `it` - Italian
- `jp` - Japanese
- `ko` - Korean
- `lv` - Latvian
- `nl` - Dutch
- `no` - Norwegian
- `pl` - Polish
- `pt` or `pt-BR` - Portuguese
- `ro` - Romanian
- `ru` - Russian
- `sv` - Swedish
- `tr` - Turkish
- `ua` - Ukrainian
- `uz` - Uzbek
- `vi` - Vietnamese

Example file structure
```
docs/
├── index.mdx                    # English (default)
├── quickstart.mdx
├── fr/
│   ├── index.mdx               # French
│   ├── quickstart.mdx
├── es/
│   ├── index.mdx               # Spanish
│   ├── quickstart.mdx
└── zh/
    ├── index.mdx               # Chinese
    └── quickstart.mdx
```
Keep the same file names and directory structure across all languages. This makes it easier to maintain translations and identify missing content.

##

[​](#configure-the-language-switcher)

Configure the language switcher

To add a language switcher to your documentation, configure the `languages` array in your `docs.json` navigation.

docs.json
```
{
  "navigation": {
    "languages": [
      {
        "language": "en",
        "groups": [
          {
            "group": "Getting started",
            "pages": ["index", "quickstart"]
          }
        ]
      },
      {
        "language": "es",
        "groups": [
          {
            "group": "Comenzando",
            "pages": ["es/index", "es/quickstart"]
          }
        ]
      }
    ]
  }
}
```
Each language entry in the `languages` array requires:

- `language`: ISO 639-1 language code
- Full navigation structure
- Paths to translated files

The navigation structure can differ between languages to accommodate language-specific content needs.

###

[​](#set-default-language)

Set default language

The first language in the `languages` array is automatically used as the default. To use a different language as the default, either reorder the array or add the `default` property:

docs.json
```
{
  "navigation": {
    "languages": [
      {
        "language": "es",
        "groups": [...]
      },
      {
        "language": "en",
        "groups": [...]
      }
    ]
  }
}
```
Alternatively, use the `default` property to override the order:

docs.json
```
{
  "navigation": {
    "languages": [
      {
        "language": "en",
        "groups": [...]
      },
      {
        "language": "es",
        "default": true,
        "groups": [...]
      }
    ]
  }
}
```

###

[​](#single-language-documentation)

Single language documentation

If you only want one language available without a language switcher, remove the `languages` field from your navigation configuration. Instead, define your navigation structure directly:

docs.json
```
{
  "navigation": {
    "tabs": [
      {
        "tab": "Documentation",
        "groups": [
          {
            "group": "Getting started",
            "pages": ["index", "quickstart"]
          }
        ]
      }
    ]
  }
}
```
This displays your documentation in a single language without the language switcher UI.

Translate navigation labels like group or tab names to match the language of the content. This creates a fully localized experience for your users.

###

[​](#global-navigation)

Global navigation

To add global navigation elements that appear across all languages, configure the `global` object in your `docs.json` navigation.

docs.json
```
{
  "navigation": {
    "global": {
      "anchors": [
        {
          "anchor": "Documentation",
          "href": "https://example.com/docs"
        },
        {
          "anchor": "Blog",
          "href": "https://example.com/blog"
        }
      ]
    },
    "languages": [
      // Language-specific navigation
    ]
  }
}
```

##

[​](#maintain-translations)

Maintain translations

Keep translations accurate and synchronized with your source content.

###

[​](#translation-workflow)

Translation workflow

1.  Update source content in your primary language.
2.  Identify changed content.
3.  Translate changed content.
4.  Review translations for accuracy.
5.  Update translated files.
6.  Verify navigation and links work.

###

[​](#automated-translations)

Automated translations

For automated translation solutions, [contact the Mintlify sales team](mailto:gtm@mintlify.com).

###

[​](#images-and-media)

Images and media

Store translated images in language-specific directories.
```
images/
├── dashboard.png          # English version
├── fr/
│   └── dashboard.png     # French version
└── es/
    └── dashboard.png     # Spanish version
```
Reference images using relative paths in your translated content.

es/index.mdx
```
![Captura de pantalla del panel de control](/images/es/dashboard.png)
```

##

[​](#seo-for-multi-language-sites)

SEO for multi-language sites

Optimize each language version for search engines.

###

[​](#page-metadata)

Page metadata

Include translated metadata in each file’s frontmatter:

fr/index.mdx
```
---
title: "Commencer"
description: "Apprenez à commencer avec notre produit."
keywords: ["démarrage", "tutoriel", "guide"]
---
```

##

[​](#best-practices)

Best practices

###

[​](#date-and-number-formats)

Date and number formats

Consider locale-specific formatting for dates and numbers.

- Date formats: MM/DD/YYYY vs DD/MM/YYYY
- Number formats: 1,000.00 vs 1.000,00
- Currency symbols: $100.00 vs 100,00€

Include examples in the appropriate format for each language or use universally understood formats.

###

[​](#maintain-consistency)

Maintain consistency

- Maintain content parity across all languages to ensure every user gets the same quality of information.
- Create a translation glossary for technical terms.
- Keep the same content structure across languages.
- Match the tone and style of your source content.
- Use Git branches to manage translation work separately from main content updates.

###

[​](#layout-differences)

Layout differences

Some languages require more or less space than English. Test your translated content on different screen sizes to ensure:

- Navigation fits properly.
- Code blocks don’t overflow.
- Tables and other formatted text remain readable.
- Images scale appropriately.

###

[​](#character-encoding)

Character encoding

Ensure your development environment and deployment pipeline support UTF-8 encoding to properly display all characters in languages with different alphabets and special characters.

Was this page helpful?

YesNo

[Improve your docsPrevious](https://www.mintlify.com/docs/guides/improving-docs)[LinkingNext](https://www.mintlify.com/docs/guides/linking)

⌘I
