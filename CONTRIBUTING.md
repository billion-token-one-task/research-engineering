# 贡献指南

## 工作流程

### 1. 认领 issue

在 issue 下评论 "我来做这个" 或 `/claim`。

**同时只认领 1-2 个 issue**，避免堵队。如果认领后 7 天没开 PR，维护者会询问进度，必要时释放给其他人。

### 2. 开发

- fork 仓库 → 新建分支 `feat/issue-123-short-description` 或 `fix/issue-123-xxx`
- 遵循 issue 里的验收标准
- 如果发现 issue 描述不清，直接在 issue 下问，不要猜

### 3. 提 PR

PR 描述里必须包含：

```
Closes #issue_number

## 做了什么
(1-3 句话)

## 验收项对照
- [x] acceptance item 1
- [x] acceptance item 2

## 如何验证
(具体命令 / 测试 / 截图)
```

### 4. Review

- 研究者或维护者 review
- 技术无异议后合并
- 一般 72 小时内会有首次反馈

## 代码规范（极简）

- 语言/框架按 issue 里指定
- 代码要能跑（测试通过 / 有示例脚本）
- 不要大改既有代码风格，除非有理由

## 联系方式

- 日常沟通：在 issue / PR 里 @ 维护者
- 加入贡献者群（Discord / 飞书）：在 issue 里留言或邮件 `jim [at] diwenbao.co`

## 行为准则

技术讨论对事不对人。保持专业和尊重。
