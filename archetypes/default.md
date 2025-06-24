---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
lastmod: {{ .Date }}
draft: true
author: "Sullivan"
tags: []
categories: []
description: ""

# 封面配置
cover:
    image: "" # 图片链接：支持以下几种方式
            # 1. OSS：https://sullivan-blog.oss-cn-beijing.aliyuncs.com/posts/tech/example/cover.png
            # 2. 本地：posts/tech/example/cover.png（将图片放在 static 目录下）
            # 3. 外链：https://example.com/images/cover.png
    caption: "" # 图片底部描述
    alt: "" # 图片替代文本（SEO 友好）
    relative: false # 使用相对路径（本地图片建议设为 true）
    hidden: false # 是否隐藏封面

showToc: true
TocOpen: false
hidemeta: false
comments: true

canonicalURL: "https://sullivan.top/{{ .Name }}"
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
---

## 简介
