# Hugo Blueprint

Hugo [Blueprint](https://www.zixiangzhang.com/design/UndertideAtelier) is [Zixiang Zhang](https://zixiangzhang.com)'s personal design language for Hugo, originated from his [personal website](https://zixiangzhang.com). It is a PaperMod-derived theme for dense technical blogs, project logs, and research notes.

Author: [Zixiang Zhang](https://zixiangzhang.com). Personal Hugo blog: [kircerta.com](https://www.kircerta.com).

## Preview

![Blueprint dark preview](https://raw.githubusercontent.com/Kircerta/hugo-blueprint/main/images/screenshot-dark.png)

![Blueprint light preview](https://raw.githubusercontent.com/Kircerta/hugo-blueprint/main/images/screenshot-light.png)

## Theme Surface

- Article-card home and list pages with compact metadata.
- Blueprint dark and light visual modes with a fixed mode switch.
- Collapsible table of contents support for long technical posts.
- Styled archives, search, tags, pagination, tables, and code blocks.
- Multilingual example site and theme labels under `params.blueprint`.

## Install

Add the theme to a Hugo site:

```bash
git submodule add https://github.com/Kircerta/hugo-blueprint.git themes/hugo-blueprint
```

Set the theme:

```toml
theme = "hugo-blueprint"
```

## Configuration

```toml
baseURL = "https://example.com/"
title = "Blueprint"
theme = "hugo-blueprint"
defaultTheme = "dark"
disableThemeToggle = true
enableRobotsTXT = true

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
    darkLabel = "BLUEPRINT DARK"
    lightLabel = "BLUEPRINT LIGHT"
```

## Example Site

Demo: <https://kircerta.github.io/hugo-blueprint/>

Build the included example site:

```bash
hugo --source exampleSite --themesDir ../.. --theme hugo-blueprint --destination /tmp/hugo-blueprint-example --cleanDestinationDir --gc --minify
```

## Attribution

Blueprint is derived from [hugo-PaperMod](https://github.com/adityatelange/hugo-PaperMod) by [Aditya Telange](https://github.com/adityatelange). Thanks to [Hugo](https://gohugo.io/) and the [Hugo authors](https://github.com/gohugoio/hugo/graphs/contributors). PaperMod and Blueprint are distributed under the MIT License.

## License

MIT. See [LICENSE](LICENSE).
