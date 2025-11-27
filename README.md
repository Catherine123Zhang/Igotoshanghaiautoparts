# 展会客户展位标注工具

这是一个用于在展会平面图上标注客户位置的Web应用。

## 功能特性

- 📊 13个展厅的客户展位标注
- 🎨 可视化标注（大/中/小客户颜色区分）
- ⭐ 优先客户标记
- 📱 响应式设计，支持移动端
- 🖼️ 支持上传平面图并导出标注后的图片

## 技术栈

- HTML5 + CSS3
- JavaScript (Vanilla)
- Fabric.js (Canvas操作)

## 部署

本项目已配置为可直接部署到 Vercel。

### 部署步骤

1. **初始化Git仓库**（如果还没有）
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   ```

2. **推送到GitHub**
   ```bash
   git remote add origin <your-repo-url>
   git branch -M main
   git push -u origin main
   ```

3. **部署到Vercel**
   - 访问 [Vercel](https://vercel.com)
   - 点击 "New Project"
   - 导入你的GitHub仓库
   - Vercel会自动检测并部署

或者使用Vercel CLI：
```bash
npm i -g vercel
vercel
```

## 本地开发

直接在浏览器中打开 `hall_maps_index.html` 即可。

## 文件结构

```
.
├── hall_maps_index.html      # 入口页面（展厅索引）
├── hall_X_X_map.html         # 各展厅标注页面
├── HALL_MAPS_README.md       # 使用说明
├── vercel.json               # Vercel配置
└── README.md                 # 项目说明
```

## 使用说明

详细使用说明请参考 [HALL_MAPS_README.md](./HALL_MAPS_README.md)

