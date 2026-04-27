# 部署指南

本文档说明如何将 echarts-kb 知识库部署到 GitHub Pages。

## 📋 前置要求

- GitHub 账号
- Git 已安装并配置
- 项目代码已推送到 GitHub 仓库

## 🚀 自动部署（推荐）

本项目已配置 GitHub Actions 自动部署流程，无需手动操作。

### 配置步骤

1. **推送代码到 GitHub**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

2. **启用 GitHub Pages**
   - 进入仓库的 **Settings** → **Pages**
   - 在 **Build and deployment** 部分：
     - Source: 选择 **GitHub Actions**
   - 保存设置

3. **触发自动部署**
   - 每次推送到 `main` 分支会自动触发部署
   - 或手动触发：进入 **Actions** → 选择工作流 → 点击 **Run workflow**

4. **访问站点**
   - 部署完成后，访问：`https://jarodchen.github.io/echarts-kb/`
   - 查看部署状态：**Actions** → **Deploy to GitHub Pages**

### 部署流程说明

```mermaid
graph LR
    A[推送代码到 main] --> B[触发 GitHub Actions]
    B --> C[上传 html 目录]
    C --> D[部署到 GitHub Pages]
    D --> E[站点可访问]
```

## 🔧 本地预览

在部署前，可以在本地预览网站：

### 方法 1: 直接打开
直接在浏览器中打开 `html/index.html` 文件

### 方法 2: 使用 Python
```bash
cd html
python -m http.server 8080
```
访问 `http://localhost:8080`

### 方法 3: 使用 Node.js
```bash
npx serve html
```
访问 `http://localhost:3000`

### 方法 4: 使用 VS Code Live Server
1. 安装 **Live Server** 扩展
2. 右键点击 `html/index.html`
3. 选择 **Open with Live Server**

## 📦 项目结构

```
echarts-kb/
├── html/                    # 静态网站文件（部署到此目录）
│   ├── index.html          # 首页
│   ├── quick-reference.html # 快速参考
│   ├── guide/              # 使用指南
│   ├── modules/            # 核心模块
│   ├── cases/              # 实战案例
│   └── assets/             # 资源文件
├── .github/workflows/      # GitHub Actions 配置
│   └── deploy.yml          # 部署工作流
├── package.json            # 项目配置
├── .gitignore              # Git 忽略规则
└── README.md               # 项目说明
```

## ⚙️ GitHub Actions 配置

部署配置文件：`.github/workflows/deploy.yml`

### 关键配置说明

```yaml
on:
  push:
    branches: [main]        # 监听 main 分支
  workflow_dispatch:         # 支持手动触发

jobs:
  deploy:
    steps:
      - uses: actions/checkout@v4
      - uses: actions/upload-pages-artifact@v3
        with:
          path: html         # 上传 html 目录
      - uses: actions/deploy-pages@v4
```

## 🔍 故障排查

### 部署失败

1. **检查 Actions 日志**
   - 进入 **Actions** 标签页
   - 查看失败的 workflow 运行
   - 阅读错误信息

2. **常见问题**
   - ✅ 确保分支名称是 `main`
   - ✅ 确保 `html/` 目录存在且包含文件
   - ✅ 确保已在 Settings 中启用 GitHub Actions

### 部署成功但页面 404

1. **等待几分钟**：GitHub Pages 需要时间生效
2. **检查 URL**：确保访问地址正确
3. **清除缓存**：尝试硬刷新（Ctrl+Shift+R）
4. **检查自定义域名**：如果使用了自定义域名，检查 DNS 配置

### 样式丢失或资源加载失败

1. **检查 base 路径**：确保所有资源使用正确的相对路径
2. **检查大小写**：GitHub Pages 对文件名大小写敏感
3. **查看浏览器控制台**：检查 404 错误的具体资源

## 📊 部署状态

| 项目 | 状态 |
|------|------|
| 构建类型 | 静态 HTML（无需构建） |
| 部署目标 | GitHub Pages |
| 触发方式 | 推送到 main / 手动触发 |
| 部署路径 | `/echarts-kb/` |
| CDN 加速 | ✅ 由 GitHub 提供 |

## 🔄 更新内容

每次更新内容后：

```bash
git add .
git commit -m "更新: 描述你的更改"
git push origin main
```

GitHub Actions 会自动重新部署，通常 1-2 分钟内完成。

## 💡 最佳实践

1. **提交前预览**：先在本地测试页面显示正常
2. **小步提交**：每次更新一个功能或章节
3. **清晰的提交信息**：说明修改的内容和原因
4. **备份重要更改**：重大修改前先创建分支

## 📞 获取帮助

如遇到部署问题：
- 查看 [GitHub Pages 官方文档](https://docs.github.com/en/pages)
- 查看项目的 Issues 页面
- 查阅 GitHub Actions 的详细日志

---

**最后更新**: 2026-04-27
