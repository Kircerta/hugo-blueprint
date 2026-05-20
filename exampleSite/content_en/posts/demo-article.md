+++
title = "Blueprint Demo Article"
date = 2026-05-15T14:30:00-04:00
summary = "Markdown syntax, code blocks, article navigation, tables, and built-in site surfaces."
tags = ["markdown", "code", "demo"]
categories = ["Examples"]
ShowToc = true
+++

This article shows the common elements used in Blueprint content.

## Headings

### A Third-Level Heading

Use headings to build the table of contents. Keep the first visible section close to the article summary.

## Paragraphs

Write normal Markdown paragraphs. Blueprint keeps the reading column centered and uses compact metadata above the article.

Inline links, `inline code`, **bold text**, and _emphasis_ use the same Markdown syntax as Hugo's default Goldmark renderer.

## Lists

1. Define the build target.
2. Write the content.
3. Run the local preview.
4. Publish the static output.

- Research note
- Project log
- API reference

## Tables

Tables are centered by default in Blueprint articles.

| Surface | Use |
|---|---|
| Home | Recent articles |
| Archives | Chronological lookup |
| Search | Local JSON search |
| Tags | Topic grouping |

## Site Controls

The header links to About, Archives, Search, and Tags. The language switch appears next to the site title when translations exist.

The mode switch stays fixed in the lower corner. Its labels come from `params.blueprint`.

```toml
[params.blueprint]
  homeKicker = "BLUEPRINT BLOG"
  articlePrefix = "ARTICLE"
  entryCta = "READ ARTICLE"
```

## Quote

> Blueprint is a technical writing theme with article cards, centered content, and local search.

## Search

Enable the JSON output in the site config, then create a search page using the `search` layout. The included example site already has both.

## Code Blocks

Blueprint keeps Hugo's syntax highlighting support and styles code blocks for the theme palette.

```text
hugo server --buildDrafts
```

```toml
baseURL = "https://example.com/"
title = "Blueprint"
theme = "hugo-blueprint"

[outputs]
  home = ["HTML", "RSS", "JSON"]
```

```go {linenos=table,hl_lines=[3,"6-7"]}
package main

import "fmt"

func main() {
    name := "Blueprint"
    fmt.Println(name)
}
```

Set `ShowCodeCopyButtons = true` in `[params]` to show copy controls on supported code blocks.
