---
url: https://mintlify.com/docs/create/code
canonical: https://www.mintlify.com/docs/create/code
title: "Format code - Mintlify"
description: "Display and style inline code and code blocks."
generator: Mintlify
type: website
---

[Skip to main content](#content-area)

[Mintlify home page![light logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/light.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b0900d78fd30c5583e438ce3f2591f94)![dark logo](https://mintcdn.com/mintlify/e0-N9JebsJpsinlD/logo/dark.svg?fit=max&auto=format&n=e0-N9JebsJpsinlD&q=85&s=b42419758ebac281070d7ed579c40075)](https://mintlify.com/docs)

[Documentation](https://www.mintlify.com/docs)[Guides](https://www.mintlify.com/docs/guides)[API reference](https://www.mintlify.com/docs/api/introduction)[Changelog](https://www.mintlify.com/docs/changelog)

Search...

Navigation

Create content

Format code

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

[​](#adding-code-samples)

Adding code samples

You can add inline code snippets or code blocks. Code blocks support meta options for syntax highlighting, titles, line highlighting, icons, and more.

###

[​](#inline-code)

Inline code

To denote a `word` or `phrase` as code, enclose it in backticks (\`).
```
To denote a `word` or `phrase` as code, enclose it in backticks (`).
```

###

[​](#code-blocks)

Code blocks

Use [fenced code blocks](https://www.markdownguide.org/extended-syntax/#fenced-code-blocks) by enclosing code in three backticks. Code blocks are copyable, and if you have the assistant enabled, users can ask AI to explain the code. Specify the programming language for syntax highlighting and to enable meta options. Add any meta options, like a title or icon, after the language.

HelloWorld.java example

Format
```
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

##

[​](#code-block-options)

Code block options

Add meta options to your code blocks to customize their appearance.

You must specify a programming language for a code block before adding any other meta options.

###

[​](#option-syntax)

Option syntax

- **String and boolean options**: Wrap with `""`, `''`, or no quotes.
- **Expression options**: Wrap with `{}`, `""`, or `''`.

###

[​](#syntax-highlighting)

Syntax highlighting

Enable syntax highlighting by specifying the programming language after the opening backticks of a code block. We use [Shiki](https://shiki.style/) for syntax highlighting and support all available languages. See the full list of [languages](https://shiki.style/languages) in Shiki’s documentation. Customize code block themes globally using `styling.codeblocks` in your `docs.json` file. Set simple themes like `system` or `dark`, or configure custom [Shiki themes](https://shiki.style/themes) for light and dark modes. See [Settings](https://www.mintlify.com/docs/organize/settings#param-styling) for configuration options.

Syntax highlighting example

Format
```
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
Custom syntax highlighting theme

For custom themes, set your theme in `docs.json` to `"css-variables"` and override syntax highlighting colors using CSS variables with the `--mint-` prefix.The following variables are available:**Basic colors**

- `--mint-color-text`: Default text color
- `--mint-color-background`: Background color

**Token colors**

- `--mint-token-constant`: Constants and literals
- `--mint-token-string`: String values
- `--mint-token-comment`: Comments
- `--mint-token-keyword`: Keywords
- `--mint-token-parameter`: Function parameters
- `--mint-token-function`: Function names
- `--mint-token-string-expression`: String expressions
- `--mint-token-punctuation`: Punctuation marks
- `--mint-token-link`: Links

**ANSI colors**

- `--mint-ansi-black`, `--mint-ansi-black-dim`
- `--mint-ansi-red`, `--mint-ansi-red-dim`
- `--mint-ansi-green`, `--mint-ansi-green-dim`
- `--mint-ansi-yellow`, `--mint-ansi-yellow-dim`
- `--mint-ansi-blue`, `--mint-ansi-blue-dim`
- `--mint-ansi-magenta`, `--mint-ansi-magenta-dim`
- `--mint-ansi-cyan`, `--mint-ansi-cyan-dim`
- `--mint-ansi-white`, `--mint-ansi-white-dim`
- `--mint-ansi-bright-black`, `--mint-ansi-bright-black-dim`
- `--mint-ansi-bright-red`, `--mint-ansi-bright-red-dim`
- `--mint-ansi-bright-green`, `--mint-ansi-bright-green-dim`
- `--mint-ansi-bright-yellow`, `--mint-ansi-bright-yellow-dim`
- `--mint-ansi-bright-blue`, `--mint-ansi-bright-blue-dim`
- `--mint-ansi-bright-magenta`, `--mint-ansi-bright-magenta-dim`
- `--mint-ansi-bright-cyan`, `--mint-ansi-bright-cyan-dim`
- `--mint-ansi-bright-white`, `--mint-ansi-bright-white-dim`

**Custom syntax highlighting**Add syntax highlighting for languages not included in Shiki’s default set by providing custom TextMate grammar files. Create a JSON file following the [TextMate grammar format](https://macromates.com/manual/en/language_grammars), then reference it in your `docs.json`. You can add multiple custom languages by including additional paths in the array.

docs.json
```
{
  "styling": {
    "codeblocks": {
      "languages": {
        "custom": ["/languages/my-custom-language.json"]
      }
    }
  }
}
```

###

[​](#twoslash)

Twoslash

In JavaScript and TypeScript code blocks, use `twoslash` to enable interactive type information. Users can hover over variables, functions, and parameters to see types and errors like in an IDE.

Twoslash example

Format
```
type Pet = "cat" | "dog" | "hamster";

function adoptPet(name: string, type: Pet) {
  return `${name} the ${type} is now adopted!`;
}

// Hover to see the inferred types
const message = adoptPet("Mintie", "cat");
```

###

[​](#title)

Title

Add a title to label your code example. Use `title="Your title"` or a string on a single line.

Title example

Format
```
const hello = "world";
```

###

[​](#icon)

Icon

Add an icon to your code block using the `icon` property. See [Icons](https://www.mintlify.com/docs/components/icons) for all available options.

Icon example

Format
```
const hello = "world";
```

###

[​](#line-highlighting)

Line highlighting

Highlight specific lines in your code blocks using `highlight` with the line numbers or ranges you want to highlight.

Line highlighting example

Format
```
const greeting = "Hello, World!";
function sayHello() {
  console.log(greeting);
}
sayHello();
```

###

[​](#line-focusing)

Line focusing

Focus on specific lines in your code blocks using `focus` with line numbers or ranges.

Line focusing example

Format
```
const greeting = "Hello, World!";
function sayHello() {
  console.log(greeting);
}
sayHello();
```

###

[​](#show-line-numbers)

Show line numbers

Display line numbers on the left side of your code block using `lines`.

Show line numbers example

Format
```
const greeting = "Hello, World!";
function sayHello() {
  console.log(greeting);
}
sayHello();
```

###

[​](#expandable)

Expandable

Allow users to expand and collapse long code blocks using `expandable`.

Expandable example

Format
```
from datetime import datetime, timedelta
from typing import Dict, List, Optional
from dataclasses import dataclass

@dataclass
class Book:
title: str
author: str
isbn: str
checked_out: bool = False
due_date: Optional[datetime] = None

class Library:
    def __init__(self):
        self.books: Dict[str, Book] = {}
        self.checkouts: Dict[str, List[str]] = {} # patron -> list of ISBNs

    def add_book(self, book: Book) -> None:
        if book.isbn in self.books:
            raise ValueError(f"Book with ISBN {book.isbn} already exists")
        self.books[book.isbn] = book

    def checkout_book(self, isbn: str, patron: str, days: int = 14) -> None:
        if patron not in self.checkouts:
            self.checkouts[patron] = []

        book = self.books.get(isbn)
        if not book:
            raise ValueError("Book not found")

        if book.checked_out:
            raise ValueError("Book is already checked out")

        if len(self.checkouts[patron]) >= 3:
            raise ValueError("Patron has reached checkout limit")

        book.checked_out = True
        book.due_date = datetime.now() + timedelta(days=days)
        self.checkouts[patron].append(isbn)

    def return_book(self, isbn: str) -> float:
        book = self.books.get(isbn)
        if not book or not book.checked_out:
            raise ValueError("Book not found or not checked out")

        late_fee = 0.0
        if datetime.now() > book.due_date:
            days_late = (datetime.now() - book.due_date).days
            late_fee = days_late * 0.50

        book.checked_out = False
        book.due_date = None

        # Remove from patron's checkouts
        for patron, books in self.checkouts.items():
            if isbn in books:
                books.remove(isbn)
                break

        return late_fee

    def search(self, query: str) -> List[Book]:
        query = query.lower()
        return [
            book for book in self.books.values()
            if query in book.title.lower() or query in book.author.lower()
        ]

def main():
    library = Library()

    # Add some books
    books = [
        Book("The Hobbit", "J.R.R. Tolkien", "978-0-261-10295-4"),
        Book("1984", "George Orwell", "978-0-452-28423-4"),
    ]

    for book in books:
        library.add_book(book)

    # Checkout and return example
    library.checkout_book("978-0-261-10295-4", "patron123")
    late_fee = library.return_book("978-0-261-10295-4")
    print(f"Late fee: ${late_fee:.2f}")

if __name__ == "__main__":
    main()
```
See all 87 lines

###

[​](#wrap)

Wrap

Enable text wrapping for long lines using `wrap`. This prevents horizontal scrolling and makes long lines easier to read.

Wrap example

Format
```
const greeting =
  "Hello, World! I am a long line of text that will wrap to the next line.";
function sayHello() {
  console.log(greeting);
}
sayHello();
```

###

[​](#diff)

Diff

Show a visual diff of added or removed lines in your code blocks. Added lines are highlighted in green and removed lines are highlighted in red. To create diffs, add these special comments at the end of lines in your code block:

- `// [!code ++]`: Mark a line as added (green highlight).
- `// [!code --]`: Mark a line as removed (red highlight).

For multiple consecutive lines, specify the number of lines after a colon:

- `// [!code ++:3]`: Mark the current line plus the next two lines as added.
- `// [!code --:5]`: Mark the current line plus the next four lines as removed.

The comment syntax must match your programming language (for example, `//` for JavaScript or `#` for Python).

Diff example

Format
```
const greeting = "Hello, World!";
function sayHello() {
  console.log("Hello, World!");
  console.log(greeting);
}
sayHello();
```

##

[​](#codeblock-component)

CodeBlock component

Use the `<CodeBlock>` component in custom React components to programmatically render code blocks with the same styling and features as markdown code blocks.

###

[​](#props)

Props

[​](#param-language)

language

string

The programming language for syntax highlighting.

[​](#param-filename)

filename

string

The filename to display in the code block header.

[​](#param-icon)

icon

string

The icon to display in the code block header. See [Icons](https://www.mintlify.com/docs/components/icons) for available options.

[​](#param-lines)

lines

boolean

Whether to show line numbers.

[​](#param-wrap)

wrap

boolean

Whether to wrap the code block.

[​](#param-expandable)

expandable

boolean

Whether to expand the code block.

[​](#param-highlight)

highlight

string

The lines to highlight. Provide a stringified array of numbers. Example: `"[1,3,4,5]"`.

[​](#param-focus)

focus

string

The lines to focus on. Provide a stringified array of numbers. Example: `"[1,3,4,5]"`.

###

[​](#example)

Example
```
export const CustomCodeBlock = ({
  filename,
  icon,
  language,
  highlight,
  children,
}) => {
  return (
    <CodeBlock
      filename={filename}
      icon={icon}
      language={language}
      lines
      highlight={highlight}
    >
      {children}
    </CodeBlock>
  );
};
```
Was this page helpful?

YesNo

[Format textPrevious](https://www.mintlify.com/docs/create/text)[What is the agent?Next](https://www.mintlify.com/docs/agent)

⌘I
