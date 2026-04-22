# research-engineering

研究团队的工程协作仓库。研究者在这里提需求，工程贡献者以 PR 形式交付。

## 这个仓库是什么

我们是一个研究团队，主要方向是 long-horizon agent / token scheduling / agent runtime。日常工作中经常遇到**"研究者擅长实验和理论，但需要工程支援把想法跑起来"**的情况。

这个仓库就是为了这件事：

- **研究者**：把你卡住的工程问题开成 issue
- **工程贡献者**：看到合适的 issue，评论认领，以 PR 形式完成

异步协作，互相专注各自擅长的事。

## 快速开始

### 研究者（提需求）

1. 点 [New Issue](../../issues/new/choose)，选 "研究工程任务" 模板
2. 按模板填完发出来
3. 如果 72 小时没人认领，在 issue 里 @维护者

### 工程贡献者（领任务 + 交付）

完整工作流：

```
1. 浏览 Issues,看到合适的 → 评论 "我来做这个"
2. Fork 本仓库到你自己账号
3. clone 你的 fork,建分支:
     git checkout -b feat/42-short-description   # 42 替换成 issue 号
4. 在对应子目录里写代码(见下面「代码组织」)
5. commit 并 push 到你的 fork
6. 在 GitHub 上发起 PR:你的 fork:feat/42-xxx  →  本仓库:main
7. PR 描述第一行写 "Closes #42"  ← 这会自动关联并在合并时关闭 issue
8. 维护者 review 合并
```

**分支命名**：`feat/<issue号>-<短描述>` 或 `fix/<issue号>-<短描述>`
**PR 关联 issue**：在 PR 描述里写 `Closes #42` / `Fixes #42` / `Resolves #42` 三者任一

## 代码组织

所有代码都提到 `main` 分支（通过 PR）。根据任务类型放到对应子目录：

| 目录 | 放什么 |
|---|---|
| [`benchmarks/`](./benchmarks) | 测评/跑分/性能对比脚本 |
| [`infra/`](./infra) | 基础设施：CI、部署、wandb 集成、监控 |
| [`tools/`](./tools) | CLI / 可视化 / dashboard / 数据工具 |
| [`experiments/`](./experiments) | 一次性实验脚本（不长期维护） |
| [`shared/`](./shared) | 跨任务共享的工具库（配置/日志/常用 utils） |

不确定放哪个目录？在 issue 里问维护者或任意标注，review 时会告诉你。

## 任务难度标签

- `good first issue` · 清晰范围，< 1 天工作量，适合第一次贡献
- `medium` · 需要 2-5 天，可能需要一点研究背景
- `hard` · 需要较深的工程经验或跨多个模块
- `research-blocker` · 研究正在等这个，优先级高

## 贡献者激励

这个仓库的维护团队会：

- **每月公布 Top 贡献者**（仅名字/GitHub ID，不涉及其他）
- **持续贡献者邀请加入内部 Reading Group**（讨论前沿研究方向）
- **高质量贡献者有机会进入更深度的合作**（具体一人一议）

## 联系维护者

- 紧急问题：在 issue 里 @ 维护者
- 非公开讨论：见 [CONTRIBUTING.md](./CONTRIBUTING.md) 里的联系方式

## License

代码采用 MIT License（见 [LICENSE](./LICENSE)）。

---

*本仓库隶属 billion-token-one-task research group。相关研究仓库：[latent-communication](https://github.com/billion-token-one-task/latent-communication) · [Deepgraph](https://github.com/billion-token-one-task/Deepgraph)*
