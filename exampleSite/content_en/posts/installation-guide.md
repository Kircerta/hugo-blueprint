+++
title = "Blueprint Installation Guide"
date = 2026-05-16T09:00:00-04:00
summary = "Install Blueprint in a Hugo site and enable the demo configuration."
tags = ["installation", "hugo", "theme"]
categories = ["Guide"]
ShowToc = true
TocOpen = true
+++

Blueprint can be installed as a Hugo theme submodule or copied into a site's `themes` directory. The example below uses a submodule so updates stay explicit.

## Requirements

- Hugo extended `0.158.0` or newer
- Git
- A Hugo site

Check Hugo before installing:

```bash
hugo version
```

## Install

From the root of a Hugo site:

```bash
git submodule add https://github.com/Kircerta/hugo-blueprint.git themes/hugo-blueprint
```

Set the theme in `hugo.toml`:

```toml
theme = "hugo-blueprint"
```

## Configure

Blueprint works with the same content model as PaperMod. These settings enable the main writing surface, search index, table of contents, and theme labels.

```toml
title = "Blueprint"
theme = "hugo-blueprint"
defaultTheme = "dark"
disableThemeToggle = true

[outputs]
  home = ["HTML", "RSS", "JSON"]

[params]
  mainSections = ["posts"]
  ShowReadingTime = true
  ShowToc = true
  TocOpen = false

  [params.blueprint]
    homeKicker = "BLUEPRINT BLOG"
    articlePrefix = "ARTICLE"
    entryCta = "READ ARTICLE"
    documentLabel = "ARTICLE"
```

## Preview

Run the local server:

```bash
hugo server
```

Open the local URL printed by Hugo. Edit files under `content/posts` and refresh the browser to preview changes.
