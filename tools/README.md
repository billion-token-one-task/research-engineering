# tools/

CLI 工具、可视化、dashboard、数据处理等辅助工具。

## 放什么
- CLI 命令行工具
- 可视化 dashboard (Streamlit / Gradio / 前端页面)
- 数据清洗 / 转换脚本
- 日常开发辅助小工具

## 不放什么
- 评测跑分 → `benchmarks/`
- 基础设施 → `infra/`

## 组织方式

按工具名建子目录，每个工具独立：

```
tools/
├── token-budget-viz/       # token 预算可视化
│   ├── README.md
│   └── app.py
└── pr-stats/
    └── ...
```
