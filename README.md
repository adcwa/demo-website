# 极简私人博客

一个采用Hugo构建的极简风格私人博客，设计灵感来自苹果官网的简洁美学。

## ✨ 特点

- **极简设计**：苹果风格，黑白灰主色调，充足留白
- **响应式布局**：完美适配桌面端和移动端设备  
- **隐私保护**：禁止搜索引擎收录，保护个人隐私
- **Markdown支持**：支持完整的Markdown语法和代码高亮
- **快速加载**：静态网站，加载速度极快
- **易于维护**：本地Markdown文件管理，简单高效

## 🚀 快速开始

### 环境要求

- Hugo (>= v0.121.0)
- Git

### 本地预览

```bash
# 克隆仓库
git clone <your-repo-url>
cd demo-website

# 启动开发服务器
hugo server --buildDrafts

# 访问 http://localhost:1313
```

### 构建网站

```bash
# 构建静态文件
hugo

# 生成的文件在 public/ 目录
```

## 📝 内容管理

### 创建新文章

1. 在 `content/posts/` 目录下创建新的 `.md` 文件
2. 使用以下格式的Front Matter：

```yaml
---
title: "文章标题"
date: 2024-01-14T10:00:00+08:00
draft: false
tags: ["标签1", "标签2"]
---

这里是文章内容...
```

### 文章管理

- **发布文章**：设置 `draft: false`
- **草稿文章**：设置 `draft: true`  
- **文章标签**：在 `tags` 数组中添加标签
- **文章日期**：修改 `date` 字段

## 🛠️ 配置说明

主要配置文件：`hugo.toml`

```toml
baseURL = "https://your-domain.com"  # 修改为你的域名
title = "私人博客"                    # 网站标题
author = "博主"                      # 作者名称

# 隐私设置已预配置，禁止搜索引擎收录
enableRobotsTXT = true
disableKinds = ["rss", "sitemap"]
```

## 🎨 主题定制

主题文件位于 `layouts/` 目录：

- `layouts/_default/baseof.html` - 基础模板
- `layouts/_default/list.html` - 首页模板  
- `layouts/_default/single.html` - 文章页模板

样式采用内联CSS，遵循苹果设计系统的色彩和字体规范。

## 🔒 隐私保护

本博客默认启用以下隐私保护措施：

- `robots.txt` 禁止所有爬虫
- 所有页面添加 `noindex, nofollow` meta标签
- 禁用RSS和sitemap生成
- 禁用所有第三方跟踪服务

## 📱 响应式设计

设计采用移动端优先策略：

- **桌面端**：最大宽度800px，充足留白
- **平板端**：768px断点，适配中等屏幕
- **手机端**：480px断点，优化触摸操作

## 🚀 部署建议

### Vercel (推荐)

1. 推送代码到GitHub
2. 在Vercel中连接仓库
3. 构建命令：`hugo --buildDrafts`
4. 发布目录：`public`

### Netlify

1. 推送代码到Git仓库
2. 在Netlify中连接仓库  
3. 构建设置：
   - 构建命令：`hugo --buildDrafts`
   - 发布目录：`public`

### 其他静态托管

支持任何静态文件托管服务，只需上传 `public/` 目录的内容。

## 📄 许可证

本项目为个人使用，请根据需要选择合适的许可证。

## 🤝 贡献

这是一个私人博客项目，如有建议或问题，欢迎通过Issues讨论。

---

**注意**：此博客已配置为禁止搜索引擎收录，适合私人使用。如需公开博客，请修改相关隐私设置。 