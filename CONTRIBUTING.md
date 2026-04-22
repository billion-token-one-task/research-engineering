# 贡献指南

## 工作流总览

```
issue(研究者开) → 认领 → fork → 开分支 → 写代码 → 提 PR → review → 合并 → issue 自动关闭
```

## 1. 认领 issue

在 issue 下评论 "我来做这个" 或 `/claim`。

**同时只认领 1-2 个 issue**，避免堵队。如果认领后 7 天没开 PR，维护者会询问进度，必要时释放给其他人。

## 2. Fork + 建分支

```bash
# 1. GitHub 页面点 "Fork" 到你自己账号
# 2. clone 你的 fork
git clone git@github.com:<你的用户名>/research-engineering.git
cd research-engineering

# 3. 加主仓库为 upstream(方便之后同步)
git remote add upstream git@github.com:billion-token-one-task/research-engineering.git

# 4. 开分支(分支名必须带 issue 号)
git checkout -b feat/42-benchmark-runner
```

**分支命名规则**：
- 新功能：`feat/<issue号>-<短描述>`
- 修 bug：`fix/<issue号>-<短描述>`
- 文档：`docs/<issue号>-<短描述>`

## 3. 写代码

- 代码放到对应子目录（见 [README 代码组织](./README.md#代码组织)）
- 不确定放哪个目录 → 在 issue 里问
- 遵循 issue 里的验收标准
- 如果发现 issue 描述不清，直接在 issue 下问，不要猜

## 4. 提 PR

```bash
git push origin feat/42-benchmark-runner
```

然后在 GitHub 上发 PR：你的 fork 的 `feat/42-xxx` 分支 → 主仓库的 `main` 分支。

**PR 描述第一行必须写** `Closes #42`（把 42 替换成实际 issue 号）。这会：
- 自动把 PR 和 issue 互相关联
- PR 合并时自动关闭 issue

一个 PR 可以同时关闭多个 issue：`Closes #42, closes #43`。

按 PR 模板填完其他内容：做了什么、验收项对照、如何验证、代码位置。

## 5. Review

- 研究者或维护者 review
- 技术无异议后合并
- 一般 72 小时内会有首次反馈
- 如果 review 要求改动，直接在本地分支改完 push，PR 会自动更新

## 6. 合并后

- 主仓库的 main 已有你的代码 ✓
- 对应 issue 已自动关闭 ✓
- 你可以删除 fork 里的 feature 分支

同步主仓库最新代码到你的 fork：

```bash
git checkout main
git fetch upstream
git merge upstream/main
git push origin main
```

## 代码规范（极简）

- 语言/框架按 issue 里指定
- 代码要能跑（测试通过 / 有示例脚本）
- 不要大改既有代码风格，除非有理由
- 所有提交的子目录/模块要有 README.md

## 联系方式

- 日常沟通：在 issue / PR 里 @ 维护者
- 加入贡献者群（Discord / 飞书）：在 issue 里留言或邮件 `jim [at] diwenbao.co`

## 行为准则

技术讨论对事不对人。保持专业和尊重。
