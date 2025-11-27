# 部署指南

## 📦 已完成的准备工作

✅ Git仓库已初始化  
✅ 所有文件已提交  
✅ Vercel配置文件已创建  
✅ .gitignore已配置  

## 🚀 部署步骤

### 1. 推送到GitHub

首先，你需要在GitHub上创建一个新仓库：

1. 访问 [GitHub](https://github.com) 并登录
2. 点击右上角的 "+" 号，选择 "New repository"
3. 填写仓库名称（例如：`exhibition-hall-maps`）
4. 选择 Public 或 Private
5. **不要**勾选 "Initialize this repository with a README"
6. 点击 "Create repository"

然后，在终端执行以下命令：

```bash
cd "/Users/changvivian/我去上海站 2"

# 添加远程仓库（将 YOUR_USERNAME 和 REPO_NAME 替换为你的实际值）
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git

# 推送到GitHub
git push -u origin main
```

### 2. 部署到Vercel

#### 方法一：通过Vercel网站（推荐）

1. 访问 [Vercel](https://vercel.com)
2. 使用GitHub账号登录
3. 点击 "Add New..." → "Project"
4. 在 "Import Git Repository" 中选择你刚创建的仓库
5. 点击 "Import"
6. Vercel会自动检测项目配置：
   - Framework Preset: Other
   - Root Directory: `./`
   - Build Command: （留空）
   - Output Directory: （留空）
7. 点击 "Deploy"
8. 等待部署完成（通常1-2分钟）
9. 部署完成后，你会得到一个类似 `https://your-project.vercel.app` 的URL

#### 方法二：使用Vercel CLI

```bash
# 安装Vercel CLI
npm i -g vercel

# 在项目目录下执行
cd "/Users/changvivian/我去上海站 2"
vercel

# 按照提示操作：
# - 登录Vercel账号
# - 选择项目设置（直接回车使用默认值即可）
# - 确认部署
```

### 3. 访问你的网站

部署完成后，你可以通过以下方式访问：

- **生产环境URL**: `https://your-project.vercel.app`
- **预览URL**: 每次推送代码都会生成新的预览URL

## 🔄 更新网站

当你修改了代码后，只需要：

```bash
# 提交更改
git add .
git commit -m "更新描述"

# 推送到GitHub
git push

# Vercel会自动检测到更改并重新部署
```

## 📝 注意事项

1. **入口页面**: 网站根路径 `/` 会自动重定向到 `hall_maps_index.html`
2. **静态资源**: 所有HTML文件都是静态的，可以直接访问
3. **CDN加速**: Vercel会自动为你的网站提供全球CDN加速
4. **HTTPS**: Vercel自动提供SSL证书，网站默认HTTPS访问

## 🐛 常见问题

### Q: 部署后页面显示404？
A: 检查 `vercel.json` 文件是否正确配置了路由重写。

### Q: 如何自定义域名？
A: 在Vercel项目设置中，点击 "Domains"，添加你的自定义域名。

### Q: 如何查看部署日志？
A: 在Vercel项目页面，点击 "Deployments" 标签，选择任意部署记录查看日志。

## 📞 需要帮助？

如果遇到问题，可以：
- 查看 [Vercel文档](https://vercel.com/docs)
- 检查项目中的 `vercel.json` 配置
- 查看浏览器控制台的错误信息

