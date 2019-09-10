---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "部署Hugo博客到服务器"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2019-09-10T11:12:31+08:00
lastmod: 2019-09-10T11:12:31+08:00
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

# 部署Hugo博客到服务器

## 直接部署到Github

### 新建仓库

```
在自己的GitHub上新建仓库，且必须命名为  账户名.github.io
cd My_Website/
hugo  --theme=academic --baseUrl="https://github.com/账户名/账户名.github.io" --buildDrafts
cd public/
git init
git add -A
git commit -m "我的Hugo博客第一次提交"
git remote add origin https://github.com/账户名/账户名.github.io.git
git push -u origin master
```

> 浏览器输入    账户名.github.io

### 博客更新

```
hugo new post/blog_name.md
git add -A
git commit -m "我的Hugo博客第二次提交"
git push origin master
```

> 浏览器输入    账户名.github.io

## 通过Netlify部署

打开	https://app.netlify.com/start/deploy?repository=https://github.com/sourcethemes/academic-kickstart

### 1、Connect to GitHub.

> Connect Netlify to your GitHub account to create your `academic-kickstart` repository.

### 2、Configure your site.

### 3、配置域名

在管理域名的后台控制器修改解析https://blog.csdn.net/mqdxiaoxiao/article/details/96365253

### 4、Your site is live!

> Just push your changes to GitHub and we’ll automatically deploy them to our global CDN.

