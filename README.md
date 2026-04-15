# 我的博客

这是一个使用 Hexo 构建的静态博客网站，部署在 GitHub Pages 上。

## 功能特点

- 🚀 基于 Hexo 框架，快速轻量
- 📝 支持 Markdown 语法编写文章
- 🎨 使用默认的 Landscape 主题
- 🔄 通过 GitHub Actions 自动部署
- 📱 响应式设计，支持移动端

## 快速开始

### 本地开发

1. 安装依赖：
```bash
npm install
```

2. 启动本地服务器：
```bash
npm run server
```

3. 在浏览器中访问 `http://localhost:4000`

### 创建新文章

```bash
hexo new "文章标题"
```

这会在 `source/_posts/` 目录下创建一个新的 Markdown 文件。

### 生成静态文件

```bash
npm run build
```

生成的静态文件会保存在 `public/` 目录中。

## 部署到 GitHub Pages

### 自动部署（推荐）

当你将代码推送到 `main` 分支时，GitHub Actions 会自动构建并部署到 GitHub Pages。

**注意**：GitHub Pages 提供免费默认域名，无需任何 DNS 配置：
- 用户页面：`https://你的用户名.github.io`
- 自动启用 HTTPS 证书

### 手动部署

1. 首先修改 `_config.yml` 中的配置：
   - 将 `url` 改为你的 GitHub Pages 地址（如 `https://你的用户名.github.io`）
   - 将 `deploy.repo` 改为你的仓库地址
   - 将 `deploy.branch` 改为 `gh-pages`

2. 运行部署命令：
```bash
npm run deploy
```

## 配置说明

### 基本配置

编辑 `_config.yml` 文件来配置你的博客：

```yaml
# 网站信息
title: 我的博客
subtitle: 技术分享与思考
description: 分享技术见解、学习心得和有趣的想法
author: 你的名字
language: zh-CN
```

### 主题配置

Hexo 默认使用 Landscape 主题。你可以通过编辑 `_config.landscape.yml` 来自定义主题。

## 目录结构

```
.
├── _config.yml          # 主配置文件
├── _config.landscape.yml # 主题配置文件
├── package.json         # 项目依赖和脚本
├── source/              # 源文件目录
│   ├── _posts/         # 博客文章目录
│   └── _drafts/        # 草稿目录
├── themes/             # 主题目录
├── scaffolds/          # 模板目录
└── public/             # 生成的静态文件（.gitignore）
```

## 常用命令

```bash
# 创建新文章
hexo new "文章标题"

# 创建新页面
hexo new page "页面名称"

# 启动本地服务器
hexo server

# 生成静态文件
hexo generate

# 部署到远程服务器
hexo deploy

# 清除缓存和生成的文件
hexo clean
```

## 资源链接

- [Hexo 官方文档](https://hexo.io/docs/)
- [Hexo 主题](https://hexo.io/themes/)
- [Markdown 语法指南](https://www.markdownguide.org/)

## 许可证

MIT License
