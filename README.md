# Stock AI Context

这是一个股票观察 AI 上下文只读仓库，统一入口为 [`latest.json`](latest.json)。

ChatGPT 使用步骤：

1. 读取 `latest.json`，检查 `batch.status`，只有 `ready` 才继续。
2. 确认 `batch_time` 是当天最新批次，再读取 `global_rules`。
3. 逐只检查 `plan.status`；只有 `approved` 才允许按计划判断。
4. 根据 `screenshot.image_url` 查看最新分时截图。

本仓库不应包含 Token、Cookie、密码、登录数据或本机隐私信息。
