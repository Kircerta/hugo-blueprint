+++
title = "Blueprint 示例文章"
date = 2026-05-15T14:30:00-04:00
summary = "Markdown 语法、代码块、文章导航、表格和内置站点页面。"
tags = ["Markdown", "代码", "示例"]
categories = ["示例"]
ShowToc = true
+++

这篇文章展示 Blueprint 内容中常用的元素。

## 标题

### 三级标题

标题会生成文章目录。第一段正文应靠近摘要，便于读者快速进入内容。

## 段落

普通段落使用 Markdown 编写。Blueprint 会保持居中的阅读列，并在文章标题下方显示紧凑元数据。

行内链接、`行内代码`、**粗体** 和 _强调_ 使用 Hugo Goldmark 的 Markdown 语法。

## 列表

1. 确认构建目标。
2. 编写内容。
3. 运行本地预览。
4. 发布静态输出。

- 研究笔记
- 项目日志
- API 参考

## 表格

Blueprint 文章中的表格默认居中。

| 页面 | 用途 |
|---|---|
| 首页 | 最近文章 |
| 归档 | 按时间浏览 |
| 搜索 | 本地 JSON 搜索 |
| 标签 | 主题聚合 |

## 站点控件

页头包含关于、归档、搜索和标签入口。有翻译内容时，语言切换会显示在站点标题旁边。

模式切换按钮固定在页面角落。显示文字来自 `params.blueprint`。

```toml
[params.blueprint]
  homeKicker = "BLUEPRINT BLOG"
  articlePrefix = "ARTICLE"
  entryCta = "READ ARTICLE"
```

## 引用

> Blueprint 是一个带文章卡片、居中内容和本地搜索的技术写作主题。

## 搜索

在站点配置中启用 JSON 输出，并创建使用 `search` layout 的搜索页面。示例站已经包含这两项。

## 代码块

Blueprint 保留 Hugo 的语法高亮支持，并让代码块适配主题配色。

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

在 `[params]` 中设置 `ShowCodeCopyButtons = true` 即可为支持的代码块显示复制按钮。
