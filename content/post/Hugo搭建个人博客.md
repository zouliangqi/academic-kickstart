---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Hugo搭建个人博客"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2019-09-10T10:43:37+08:00
lastmod: 2019-09-10T10:43:37+08:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

[TOC]

# Hugo搭建个人博客

## 下载

### 在Ubuntu16.04

```
wget https://github.com/gohugoio/hugo/releases/download/v0.58.1/hugo_extended_0.58.1_Linux-64bit.deb
```

### 在Windows

> 直接在https://github.com/gohugoio/hugo/releases/上下载最新的extended版本

> 或者用 git clone 下载

## 安装（解压）

### 在Ubuntu16.04

```
sudo dpkg -i hugo_extended_0.58.1_Linux-64bit.deb
```

### 在Windows

> 直接右键解压放到新建的目录的bin里，然后将路径添加到path环境变量

## 测试

```
hugo --help
```

## 新建站点

```
hugo new site website_name
```

## 新建博客

```
hugo new post/blog_name.md
```

## 运行

```
hugo server
```

## 查看网页

> 打开浏览器输入localhost:1313

## 运用主题(academic)

```
mkdir My_Website  ##新建网页项目根目录
git clone https://github.com/<USERNAME>/academic-kickstart.git My_Website
cd My_Website
git submodule update --init --recursive
```

```
hugo server --theme=academic-kickstart --buildDrafts
打开浏览器输入localhost:1313
```

