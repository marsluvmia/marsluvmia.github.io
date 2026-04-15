# 快速开始指南

## 🎉 恭喜！你的博客已经创建成功！

你的 Hexo 博客已经搭建完成，现在需要完成以下几个步骤来部署到 GitHub Pages。

## 📋 部署清单

### 1. 配置 GitHub 仓库

1. 在 GitHub 上创建一个新仓库，命名为 `你的用户名.github.io`
   - 例如：如果你的用户名是 `johndoe`，仓库名应该是 `johndoe.github.io`
   - 仓库设置为 Public（公开）

2. 克隆仓库到本地：
```bash
git clone https://github.com/你的用户名/你的用户名.github.io.git
cd 你的用户名.github.io
```

### 2. 更新配置文件

编辑 `_config.yml` 文件，修改以下内容：

```yaml
# 网站信息
title: 你的博客标题
subtitle: 副标题
description: 博客描述
author: 你的名字
language: zh-CN

# URL 设置
url: https://你的用户名.github.io

# 部署配置
deploy:
  type: git
  repo: https://github.com/你的用户名/你的用户名.github.io.git
  branch: gh-pages
```

### 3. 初始化 Git 仓库并推送

```bash
# 初始化 Git 仓库
git init

# 添加所有文件
git add .

# 创建第一次提交
git commit -m "初始化博客项目"

# 添加远程仓库
git remote add origin https://github.com/你的用户名/你的用户名.github.io.git

# 推送到 GitHub（强制推送首次）
git push -u origin +main
```

**注意**：如果 GitHub 默认分支是 `master`，将 `main` 改为 `master`

### 4. 启用 GitHub Pages

1. 进入你的 GitHub 仓库页面
2. 点击 **Settings** 标签
3. 在左侧菜单中找到 **Pages**
4. 在 **Build and deployment** 下：
   - **Source** 选择：`GitHub Actions`
5. 保存设置

**重要提示**：GitHub Pages 会自动为你提供免费域名 `https://你的用户名.github.io`，**无需任何 DNS 配置**，也无需购买域名。GitHub 会自动配置 HTTPS 证书。

### 5. 等待部署完成

1. 点击 **Actions** 标签
2. 等待工作流运行完成（通常需要 1-3 分钟）
3. 部署成功后，访问 `https://你的用户名.github.io`

## 🌐 关于域名

### 默认域名（推荐）

- **地址**：`https://你的用户名.github.io`
- **费用**：完全免费
- **配置**：无需任何 DNS 设置，GitHub 自动配置
- **SSL 证书**：GitHub 自动提供 HTTPS
- **适用场景**：个人博客、项目展示

### 自定义域名（可选）

如果你想使用自己的域名（如 `www.yourdomain.com`）：

1. 购买域名（每年约 ¥50-100）
2. 在域名注册商处配置 DNS 解析
3. 在 GitHub 仓库设置中添加自定义域名
4. 等待 DNS 生效（通常 24 小时内）

**注意**：95% 的个人博客使用默认域名就足够了，自定义域名需要额外成本和配置。

## 🚀 本地开发

### 启动本地服务器

```bash
npm run server
```

访问 `http://localhost:4000` 查看博客

### 创建新文章

```bash
hexo new "文章标题"
```

### 本地构建预览

```bash
npm run build
```

## 📝 常用命令

```bash
# 启动本地服务器
npm run server

# 生成静态文件
npm run build

# 清理缓存和生成的文件
npm run clean

# 部署到 GitHub Pages（如果配置了手动部署）
npm run deploy
```

## 🎨 自定义配置

### 修改博客信息

编辑 `_config.yml` 文件：

```yaml
title: 博客标题
subtitle: 副标题
description: 描述
author: 作者名
language: zh-CN
```

### 切换主题

1. 在 [Hexo 主题官网](https://hexo.io/themes/) 选择一个主题
2. 克隆主题到 `themes/` 目录：
```bash
git clone https://github.com/主题作者/主题名称.git themes/主题名称
```
3. 修改 `_config.yml`：
```yaml
theme: 主题名称
```

## 🔧 故障排除

### 端口被占用

如果 4000 端口被占用，可以使用其他端口：

```bash
hexo server -p 4001
```

### 构建失败

```bash
# 清理缓存
npm run clean

# 重新安装依赖
rm -rf node_modules
npm install

# 重新构建
npm run build
```

### GitHub Pages 部署失败

1. 检查 GitHub Actions 日志
2. 确认仓库权限设置正确
3. 确认 `_config.yml` 中的配置正确

## 📚 学习资源

- [Hexo 官方文档](https://hexo.io/docs/)
- [Markdown 语法指南](https://www.markdownguide.org/)
- [GitHub Pages 文档](https://docs.github.com/en/pages)

## 🎯 下一步

- [ ] 完成 GitHub 仓库配置
- [ ] 修改博客基本信息
- [ ] 写几篇测试文章
- [ ] 尝试更换主题
- [ ] 添加评论功能
- [ ] 集成 Google Analytics

祝你写作愉快！🎉
