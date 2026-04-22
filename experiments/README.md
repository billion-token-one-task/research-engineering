# experiments/

一次性实验脚本。做完就做完，不保证长期维护。

## 放什么
- 研究探索的一次性脚本
- "我想看看 X 是不是 Y" 这种验证代码
- 各种 ablation study

## 不放什么
- 长期维护的工具 → `tools/`
- 可复现的评测 → `benchmarks/`

## 组织方式

按日期 + 简短主题：

```
experiments/
├── 2026-04-ablation-context-compression/
│   ├── README.md         # 结论 + 怎么跑 + 用了什么数据
│   └── run.py
└── 2026-05-token-budget-sweep/
    └── ...
```

**要求**：即使是一次性脚本，子目录必须有 README 说明：做了什么、结论是什么、怎么复现。其他人（包括未来的你）才能看懂。
