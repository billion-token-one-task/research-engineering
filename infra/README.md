# infra/

基础设施类代码。

## 放什么
- CI / CD 配置
- 部署脚本（Modal / RunPod / Docker）
- wandb / mlflow 等实验追踪集成
- 日志、监控、报警
- 开发环境配置（devcontainer、pre-commit 等）

## 不放什么
- 业务逻辑代码（benchmark 逻辑、实验逻辑）
- 一次性任务脚本 → `experiments/`

## 典型任务示例
- 统一 wandb logging wrapper
- GPU 任务调度脚本
- 自动化的 token 成本追踪
