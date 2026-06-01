# Notes 项目指南

基于 Jekyll + Chirpy 主题的个人笔记站，部署在 GitHub Pages (`itflash.github.io/notes`)。

## 添加笔记

在 `_posts/` 目录下创建文件，命名格式：`YYYY-MM-DD-短标题.md`

```markdown
---
title: 文章标题
categories: [cli]
tags: [tag1, tag2, tag3]
toc: true
---

正文内容（Markdown 格式）。
```

- `categories` 和 `tags` 用 YAML 数组格式，Chirpy 会自动生成分类页和标签页
- `toc: true` 开启文章内目录导航
- 日期可以随便写（不是博客不需要精确日期），但必须符合 `YYYY-MM-DD` 格式

## 添加新分类

如果要新增一个大类，在 `_tabs/` 下创建对应的 tab 页：

```markdown
---
title: 分类名
icon: fas fa-icon-name
order: N
---

[笔记标题](/posts/笔记文件名/)
```

图标名从 [Font Awesome](https://fontawesome.com/search?m=free) 找。

## 部署

push 到 `main` 分支 → GitHub Actions 自动构建并部署到 GitHub Pages。等 1-2 分钟刷新即可看到更新。

## 本地预览（可选）

```bash
bundle install
bundle exec jekyll serve
# 打开 http://localhost:4000/notes/
```

## 目录结构

```
notes/
├── _posts/          # 笔记内容（核心目录）
├── _tabs/           # 顶部导航标签页
├── assets/          # 图片等静态资源
├── _config.yml      # 站点配置
├── Gemfile          # Ruby 依赖
└── .github/workflows/  # 自动部署配置
```
