## Ⓜ️⬇ Markdown `.md` 

**Markdown** is a technology for creating text documents, just like **MS Word**, but there are more differences than similarities between these tools.

### Advantages and specifics of Markdown:

- **Web-oriented**. It converts to **HTML**, but is much simpler and more readable, making it the easiest way to publish content on the web.
- Markdown files are lightweight and don't require specialized software _(any text editor will do)_
- **Open format** - an `.md` file is plain, readable text. No binary junk, no license, no vendor lock-in. You can open it in any editor, in 30 years, on any system.
- **AI collaboration** - plain text means smaller context for the model: cheaper, faster, more accurate. AI understands and generates Markdown natively, documentation, READMEs, specifications come out ready to go.
- **Separation of form and content**:
  - Enforcing a uniform document style across all sections of an organization is standard practice. Even when transferring and integrating documentation between different companies, consistent styling is maintained. The style depends on the rendering engine, which is integrated with editing tools like VSCode, and publishing platforms like GitHub or GitLab.
  - This allows document authors to focus on content, which can minimize errors and improve document quality in terms of substance.
- Plain text files with simple formatting, enabling integration with **GIT version control**, which brings a number of benefits:
  - **Change history** - tracks who made changes and when, allowing you to trace a document's history and identify differences between versions.
  - **Collaboration** - facilitates teamwork, enabling multiple people to work on a document simultaneously.
  - **Autobackup** - allows restoring previous versions if new changes are unwanted.
  - **Branching** - enables simultaneous work on different chapters.
  - **Author attribution** - shows who made specific changes, increasing transparency.

### Advantages and specifics of MS Office:
  
- **Print-oriented**. The best solution for preparing documents for print.
- Low barrier to entry, being a simple and intuitive tool for creating documents.
- High popularity, meaning more people are able to edit these documents.
- **Comments and reviews** - built-in change tracking and commenting mode. Works well for short sessions and one-off reviews, but with long-term collaboration among many people it quickly becomes chaos.
- **Templates** - ready-made templates for corporate documents, contracts and official letters: open and fill in, zero configuration.
- **Form and content combined** - you see exactly what you'll print _(WYSIWYG)_. Precise control over margins, page breaks, headers and footers without any syntax.
  - **Rich editing capabilities** - beyond text formatting, it offers image, chart, table and other visual element editing, all in one place.
- **Spell checker** that catches spelling errors.

### Working with Markdown

#### Editing

Markdown is best edited in the same editor you already work in: [**VSCode**](https://code.visualstudio.com/), [Sublime Text](https://www.sublimetext.com/), [Vim](https://www.vim.org/), [Notepad++](https://notepad-plus-plus.org/). You don't need a separate application, a preview plugin is enough. For VSCode, [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one) works great, providing live preview, keyboard shortcuts and automatic list formatting. Open preview with `Ctrl+Shift+V` or `Ctrl+K V` _(side-by-side)_.

#### Preview and publishing

On Windows without an editor, [**mdview**](https://github.com/c3er/mdview/releases) works as a lightweight `.md` file viewer. Platforms like [**GitHub**](https://github.com) and [GitLab](https://gitlab.com) automatically render `.md` files. The `readme.md` file in a repository directory displays as the project's main page, making it the most common way to publish documentation, guides, and articles.

#### Conversion

[**Pandoc**](https://pandoc.org/installing.html) is a command-line tool for converting between document formats. It lets you generate a ready `.docx` or `.pdf` from an `.md` file with a single command.
```sh
# Convert to Word
pandoc document.md -o document.docx
# Convert to PDF (requires LaTeX or wkhtmltopdf installed)
pandoc document.md -o document.pdf
```

Useful when you need to hand off documentation as `.docx` to a client who doesn't know Markdown.

# Syntax

Below you'll find Markdown **markers**, i.e. syntax elements, both more and less useful ones.

## Headings

To create a heading, place `#` at the beginning of a new line. The number of `#` characters corresponds to the heading level.

```md
# Title
## Chapter
### Subchapter
#### Section
##### Subsection
```

To strongly separate sections of text without adding a heading, you can insert a horizontal rule:

```
---
```

---

## Text emphasis

You can emphasize important parts of text in several ways

```md
**Bold text**
_Italic text_
`Text as code`
~~Strikethrough text~~
==Highlighted text==
> Text as blockquote
```

**Bold text**

_Italic text_

`Text as code`

~~Strikethrough text~~

==Highlighted text==

> Text as blockquote

### Subscript and superscript

```md
Subscript: H~2~O
Superscript: x^2^
```

Subscript: H~2~O
Superscript: x^2^

## Lists

#### Bullet list

```md
- Saltpeter 74.64%
- Charcoal 13.51%
- Sulfur 11.85%
```

- Saltpeter 74.64%
- Charcoal 13.51%
- Sulfur 11.85%

#### Numbered list

```md
1. Collect $25000
2. Invest in Bitcoin
3. Be broke again
```

1. Collect $25000
2. Invest in Bitcoin
3. Be broke again

#### Multi-level list

You can create multi-level lists and mix list types

```md
1. **Python** programming course
  - Environment setup
  - Learning basics
    - Variables and basic operations
    - Conditional statements `if`...`else`
    - Loops `while` and `for`
  - QUIZ project with custom questions
2. **Markdown** document training
  1. Learning syntax elements
  2. Creating your own blog, course or cookbook
```

1. **Python** programming course
  - Environment setup
  - Learning basics
    - Variables and basic operations
    - Conditional statements `if`...`else`
    - Loops `while` and `for`
  - QUIZ project with custom questions
2. **Markdown** document training
  1. Learning syntax elements
  2. Creating your own blog, course or cookbook

### Task list

```
- [x] Go hang out with friends
- [ ] Study for the exam
- [ ] Prepare the project for grading
```

- [x] Go hang out with friends
- [ ] Study for the exam
- [ ] Prepare the project for grading

## Definitions

A special syntax was developed for explaining terms and formulating definitions.

```
Noob
: A colloquial term, especially common in gaming and internet culture, referring to a newcomer or someone who did something foolish. The term is versatile and carries various connotations. Its popularity has been growing steadily since the early 2000s.
```

Noob
: A colloquial term, especially common in gaming and internet culture, referring to a newcomer or someone who did something foolish. The term is versatile and carries various connotations. Its popularity has been growing steadily since the early 2000s.

## Footnotes

When you want to reference terms and phrases in the text that will be explained at the bottom of the document, you can use the `[^x]` syntax, where `x` is the footnote number.

```
**The C language** saw the light of day in 1972 and despite its advanced age is still widely used.
There are of course many other languages on the market, usually easier for programmers,
but C still has no equal in many applications [^1].

[^1]: _C Programming Absolute Beginner's Guide_, Greg Perry, Dean Miller, 2013
```

**The C language** saw the light of day in 1972 and despite its advanced age is still widely used.
There are of course many other languages on the market, usually easier for programmers,
but C still has no equal in many applications [^1].

[^1]: _C Programming Absolute Beginner's Guide_, Greg Perry, Dean Miller, 2013

## Links

To navigate to another document/file, you need to create a **hyperlink**. It can point to documents or other files located locally in the document's folder, as well as to content available on the internet. The syntax is the same for both, only the address/path differs.

```
[Link to a local file](./path/to/file.md)
[Link to an internet file](https://some-website.com)
[Link to a heading in this file](#some-header)
```

[Link to a local file](./xaeian.png)

[Link to an internet file](https://google.com)

[Link to a heading in this file](#headings)

If you want the content of a document or file to appear in this document _(be copied into it)_, just place `!` before the link

```
![Local file content](./aux-file.md)
![Internet file link](https://google.com)
```

### Images

Embedding content from a given path is a great way to display graphics. Just like links, images can be placed locally in the document's folder or fetched from the internet.

```
![Image with PNG extension](./path/to/image.png)
```

![Xaeian Logo](./xaeian.png)

### Tables

A characteristic of Markdown is that the source code itself should resemble the original document as closely as possible, so even without a converter that renders it nicely, the document is relatively readable. This becomes especially apparent when creating tables, which are built using `|`, `-` and `:` characters, where the last one indicates alignment.

```
|  No   | Country              |         Area |     Population |
| :---: | :------------------- | -----------: | -------------: |
|   1   | Russia               |   17 098 242 |    146 238 185 |
|   2   | Canada               |    9 984 670 |     37 943 231 |
|   3   | China                |    9 596 960 |    332 403 650 |
|   4   | United States        |    9 525 067 |  1 411 778 724 |
|   5   | Brazil               |    8 515 767 |    217 240 060 |
```

Largest countries in the world:

|  No   | Country              |         Area |     Population |
| :---: | :------------------- | -----------: | -------------: |
|   1   | Russia               |   17 098 242 |    146 238 185 |
|   2   | Canada               |    9 984 670 |     37 943 231 |
|   3   | China                |    9 596 960 |    332 403 650 |
|   4   | United States        |    9 525 067 |  1 411 778 724 |
|   5   | Brazil               |    8 515 767 |    217 240 060 |

## Code block

Markdown was originally created as a tool for writing programmer documentation, so it's no surprise that it supports embedding code blocks with syntax highlighting for many languages. Place the code between ` ``` ` tags and optionally specify the language.

#### Code block in Python

````md
```py
a = "5"
b = 10
c = a + str(b) # string concatenation
print(c)
d = b + int(a) # int addition
print(d)
```
````

```py
a = "5"
b = 10
c = a + str(b) # string concatenation
print(c)
d = b + int(a) # int addition
print(d)
```

## Emoji

You can copy emoticons _(e.g. [from here](https://emojidb.org/))_ and place them directly in the document, or use their codes.

```
👍 + :heart:
```

👍 + :heart:


## Math formulas

Markdown supports math formulas in **LaTeX** notation. Inline formulas go between `$...$`, block formulas between `$$...$$`. Supported by GitHub, Obsidian, Jupyter Notebook.

```md
Inline formula: $E = mc^2$, square root: $\sqrt{a^2 + b^2}$

$$
\sum_{i=1}^{n} x_i = x_1 + x_2 + \cdots + x_n
$$
```

Inline formula: $E = mc^2$, square root: $\sqrt{a^2 + b^2}$

$$
\sum_{i=1}^{n} x_i = x_1 + x_2 + \cdots + x_n
$$

## Diagrams

**Mermaid** is a syntax for creating diagrams directly in Markdown: `flowchart`s, `sequenceDiagram`s, `gantt` and more. Supported by GitHub, GitLab and Obsidian.

````md
```mermaid
flowchart LR
  A([🌅 Wake up]) --> B{Got coffee?}
  B -->|Yes| C[Drink it]
  B -->|No| D[Buy some]
  D --> C
  C --> E([💻 Code])
```
````

```mermaid
flowchart LR
  A([🌅 Wake up]) --> B{Got coffee?}
  B -->|Yes| C[Drink it]
  B -->|No| D[Buy some]
  D --> C
  C --> E([💻 Code])
```

## Callouts

Highlighted blocks to catch the reader's attention. Warnings and important information that can't be missed.

```md
> [!NOTE]
> `readme.md` is automatically displayed as the repository page.

> [!WARNING]
> Don't commit passwords and API keys to the repository.
```

> [!NOTE]
> `readme.md` is automatically displayed as the repository page.

> [!WARNING]
> Don't commit passwords and API keys to the repository.

## Escaping

To disable Markdown syntax and display a character literally, precede it with a backslash `\`.

```md
\*this text won't be italic\*
\# this is not a heading
\`this is not code\`
```

\*this text won't be italic\*

\# this is not a heading

\`this is not code\`

## Markdown and HTML

Markdown is a shorthand for HTML, every syntax element has its counterpart:

| Markdown          | HTML                            | Result         |
| :---------------- | :------------------------------ | :------------- |
| `# Heading`       | `<h1>`Heading`</h1>`            | **big title**  |
| `**bold**`        | `<strong>`bold`</strong>`       | **bold**       |
| `_italic_`        | `<em>`italic`</em>`             | _italic_       |
| `[link](url)`     | `<a href="url">`link`</a>`      | [link](url)    |
| `![img](img.png)` | `<img src="img.png" />`         | 🖼️              |

An intermediate format, Markdown leverages existing technology instead of reinventing the wheel. Every new renderer _(VSCode, GitHub, MkDocs, Pandoc)_ automatically supports your old `.md` files.

# Project

The project involves creating your own document/project in **Markdown**, which will be one of:

- A **tutorial** covering a chosen topic, consisting of a title page and at least three lessons.
- A **cookbook** with a title page about cooking and nutrition with three recipes.
- A **travel guide** for a chosen city or location, with a general description and three most interesting spots.
- A **blog** consisting of a title page about yourself or a fictional character, with three posts.

Minimum project requirements:

- [ ] Every project/document must consist of a **main file** `readme.md` and at least **three additional** `.md` files.
- [ ] [Text emphasis](#text-emphasis) must be used consistently throughout the text.
- [ ] Every page/file must contain at least **one graphic**/image _(graphics must be stored locally in the project)_.
- [ ] The project as a whole must contain at least **two lists** (bullet/numbered).
- [ ] The project must contain at least **one table**.
- [ ] The project must contain at least **one external link**.