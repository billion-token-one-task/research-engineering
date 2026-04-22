# benchmarks/

测评、跑分、性能对比类代码放这里。

## 放什么
- 模型/方法的 benchmark runner
- 性能基准测试脚本
- 跨版本/跨配置的对比工具
- 可复现的评测 harness

## 不放什么
- 一次性的探索实验 → 去 `experiments/`
- 可视化/报表 → 去 `tools/`

## 添加新 benchmark 时

在本目录下新建子目录，每个 benchmark 一个子目录：

```
benchmarks/
├── gsm8k-latent/
│   ├── README.md        # 这个 benchmark 是什么、怎么跑、期望输出
│   ├── run.py
│   └── ...
└── token-budget-ladder/
    └── ...
```

每个子目录的 README 至少包含：怎么装依赖、怎么跑、期望输出格式。
