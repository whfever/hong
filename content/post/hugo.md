---
title: "Hugo"
date : "2022-10-15"
draft: false
tags: ["工具",]
categories: ["工具"]

---

##  Install Hugo
Download the appropriate version for your platform from Hugo Releases. Once downloaded, the binary can be run from anywhere. Ideally, you should install it somewhere in your PATH for easy use. /usr/local/bin is the most probable location.

## Create a New Site
hugo new site myBlog
The above will create a new Hugo site in a folder named myBlog.
## Use Theme
```
cd myBlog
git clone https://github.com/xianmin/hugo-theme-jane.git --depth=1 themes/jane

```
Copy the example site content:
```
cp -r themes/jane/exampleSite/content ./
Copy the default site config:

cp themes/jane/exampleSite/config.toml ./

```
Take a look at the example site:
## start
```
hugo server
```
Open http://localhost:1313/ , you will see your site running with the example content.

## hightlight code

```
    <link href="https://cdn.bootcss.com/highlight.js/10.0.1/styles/monokai.min.css" rel="stylesheet">
    <script src="https://cdn.bootcss.com/highlight.js/10.0.1/highlight.min.js"></script>
    <script>hljs.initHighlightingOnLoad();</script>
```
## 图片

```
![hugo](/image/example.jpg)
```
## shortcode
 bilibili
```
`{{< md BV1464y187dL >}}`
```
## goldmark
***config.toml***
```
[markup]
  defaultMarkdownHandler = "goldmark"
  [markup.goldmark]
    [markup.goldmark.renderer]
      unsafe = true

```
