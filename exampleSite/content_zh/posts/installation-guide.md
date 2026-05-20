+++
title = "Blueprint 安装指南"
date = 2026-05-16T09:00:00-04:00
summary = "在 Hugo 站点中安装 Blueprint 并启用示例配置。"
tags = ["安装", "Hugo", "主题"]
categories = ["指南"]
ShowToc = true
TocOpen = true
+++

Blueprint 可以作为 Hugo 主题子模块安装，也可以复制到站点的 `themes` 目录。下面使用子模块，便于明确更新。

## 要求

- Hugo extended `0.158.0` 或更新版本
- Git
- 一个 Hugo 站点

安装前检查 Hugo：

```bash
hugo version
```

## 安装

在 Hugo 站点根目录运行：

```bash
git submodule add https://github.com/Kircerta/hugo-blueprint.git themes/hugo-blueprint
```

在 `hugo.toml` 中启用主题：

```toml
theme = "hugo-blueprint"
```

## 配置

Blueprint 使用与 PaperMod 相同的内容模型。下面的配置启用文章列表、搜索索引、目录和主题标签。

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

## 预览

启动本地服务：

```bash
hugo server
```

打开 Hugo 输出的本地地址。编辑 `content/posts` 下的文件后刷新浏览器即可预览。
