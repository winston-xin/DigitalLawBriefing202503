# GitHub Pages 部署指南

## 快速部署

### 方法一：直接上传文件
1. 在GitHub上创建新仓库（仓库名建议：`DigitalLawBriefing202503`）
2. 将本文件夹内所有文件上传到仓库
3. 在仓库设置中启用GitHub Pages：
   - 进入 Settings → Pages
   - Source 选择 "Deploy from a branch"
   - Branch 选择 "main" 或 "master"
   - Folder 选择 "/ (root)"
   - 点击 Save
4. 等待部署完成，访问 `https://[username].github.io/DigitalLawBriefing202503/`

### 方法二：使用GitHub Actions（自动部署）
1. 上传所有文件到GitHub仓库
2. GitHub Actions工作流会自动触发部署
3. 部署完成后，访问 `https://[username].github.io/DigitalLawBriefing202503/`

## 文件结构说明

```
DigitalLawBriefing202503/
├── .nojekyll                 # 告诉GitHub Pages不要使用Jekyll处理
├── .github/
│   └── workflows/
│       └── deploy.yml        # GitHub Actions自动部署配置
├── _config.yml              # Jekyll配置文件
├── index.html               # 主页面
├── 404.html                 # 404错误页面
├── README.md               # 项目说明
├── DEPLOY.md               # 部署说明（本文件）
└── [所有HTML和PDF文件]      # 政策文件和网页版本
```

## 注意事项

1. **文件命名**：避免使用特殊字符，中文文件名在GitHub Pages中可能需要URL编码
2. **文件大小**：单个文件建议不超过100MB
3. **链接路径**：所有链接使用相对路径，确保在不同页面间正常跳转
4. **浏览器兼容性**：项目已优化支持现代浏览器（Chrome、Firefox、Safari、Edge）

## 本地测试

在部署前，可以在本地测试：

```bash
# 使用Python启动本地服务器
python -m http.server 8000

# 使用Node.js
npx serve .

# 然后访问 http://localhost:8000
```

## 故障排除

1. **页面无法加载**：检查GitHub Pages是否已正确启用
2. **文件404错误**：确认文件名和路径正确
3. **样式丢失**：检查CSS路径是否正确
4. **搜索功能失效**：确保JavaScript文件正确加载

## 维护更新

添加新文件时：
1. 确保文件名符合规范
2. 更新`index.html`中的文件列表
3. 提交更改到GitHub，自动触发重新部署

---

© 2025 辽宁省律师协会数字法治与数字经济专业委员会