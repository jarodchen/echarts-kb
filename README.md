# ECharts 知识库

Apache ECharts 系统化学习与实践指南，涵盖从基础图表到高级可视化的完整知识体系。

## 🌐 在线访问

**[https://jarodchen.github.io/echarts-kb/](https://jarodchen.github.io/echarts-kb/)**

## 📚 知识体系

### 📊 核心模块
- **基础图表**: 折线图、柱状图、饼图、散点图等
- **高级可视化**: 地图、关系图、树图、热力图
- **交互功能**: 数据缩放、提示框、图例、动画
- **组件系统**: 坐标系、视觉映射、数据区域

### 🎨 配置与样式
- 主题定制与切换
- 响应式布局设计
- 颜色方案与调色板
- 字体与标签优化

### ⚡ 性能优化
- 大数据量渲染策略
- Canvas vs SVG 选择
- 增量渲染与流式加载
- 内存管理与清理

### 🔧 实战案例
- 商业仪表板设计
- 实时监控可视化
- 地理信息系统
- 网络关系分析

## 🚀 本地开发

如需离线访问或本地预览：

```bash
# 方法 1: 直接打开
# 直接在浏览器中打开 html/index.html 文件

# 方法 2: 使用 Python HTTP 服务器
cd html
python -m http.server 8080

# 方法 3: 使用 Node.js
npx serve html

# 方法 4: 使用 VS Code Live Server
# 安装 Live Server 扩展，右键 index.html 选择 "Open with Live Server"
```

访问 `http://localhost:8080`

## 📁 项目结构

```
echarts-kb/
├── html/                    # 静态网站文件
│   ├── index.html          # 首页
│   ├── quick-reference.html # 快速参考手册
│   ├── guide/              # 使用指南
│   ├── modules/            # 核心模块文档
│   ├── cases/              # 实战案例
│   └── assets/             # CSS、JS、图片资源
├── .github/workflows/      # GitHub Actions 配置
└── README.md
```

## 🔧 技术栈

- **可视化库**: Apache ECharts 5.x
- **构建工具**: VitePress (文档生成)
- **部署**: GitHub Pages + GitHub Actions
- **支持格式**: HTML, SVG, Canvas

## 📖 适用人群

- 前端开发者学习数据可视化
- 数据分析师需要图表展示
- 产品经理设计数据仪表板
- 学生和研究人员进行数据呈现

## 💡 特色亮点

- **系统化**: 从基础到高级，循序渐进的学习路径
- **实战导向**: 每个概念都有可运行的代码示例
- **性能关注**: 专门的大数据渲染优化章节
- **案例丰富**: 覆盖商业场景的真实应用案例
- **持续更新**: 跟随 ECharts 最新版本特性

## 🎯 学习建议

1. **初学者**: 从基础图表开始，掌握配置项语法
2. **进阶者**: 深入学习交互组件和自定义系列
3. **专家级**: 研究源码架构和性能优化技巧
4. **实战派**: 直接查看案例模块，按需查阅文档

## 🤝 贡献

欢迎提出建议和反馈！如有内容补充或错误修正，请提交 Issue 或 Pull Request。

## 📄 许可证

MIT License

---

⭐ 如果这个项目对您有帮助，请给个 Star！
