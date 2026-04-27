# ECharts 知识库

Apache ECharts 系统化学习与实践指南。

## 在线访问

https://jarodchen.github.io/echarts-kb/

## 知识体系

### 核心模块
- **基础图表**: 折线图、柱状图、饼图、散点图等
- **高级可视化**: 地图、关系图、树图、热力图
- **交互功能**: 数据缩放、提示框、图例、动画
- **组件系统**: 坐标系、视觉映射、数据区域

### 配置与样式
- 主题定制与切换
- 响应式布局设计
- 颜色方案与调色板
- 字体与标签优化

### 性能优化
- 大数据量渲染策略
- Canvas vs SVG 选择
- 增量渲染与流式加载
- 内存管理与清理

### 实战案例
- 商业仪表板设计
- 实时监控可视化
- 地理信息系统
- 网络关系分析

## 本地预览

```bash
# 方法 1: 直接打开 html/index.html

# 方法 2: Python HTTP 服务器
cd html
python -m http.server 8080

# 方法 3: Node.js
npx serve html
```

访问 http://localhost:8080

## 项目结构

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

## 技术栈

- **可视化库**: Apache ECharts 5.x
- **构建工具**: VitePress
- **部署**: GitHub Pages + GitHub Actions

## 适用人群

- 前端开发者学习数据可视化
- 数据分析师需要图表展示
- 产品经理设计数据仪表板
- 学生和研究人员进行数据呈现

## 特色

- 系统化学习路径，从基础到高级
- 每个概念都有可运行的代码示例
- 大数据渲染优化章节
- 覆盖商业场景的真实应用案例
- 跟随 ECharts 最新版本更新

## 许可证

MIT License
