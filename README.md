# ChatSummary Plugin for XYBotV2

## 简介

`ChatSummary` 插件是一个 XYBotV2 的扩展，用于总结个人聊天和群聊天的聊天记录。 它通过调用 Dify AI 平台的大模型来生成聊天记录的总结报告。

## 功能

*   **聊天记录总结：**  自动或手动触发，总结指定数量的聊天记录。
*   **Dify AI 集成：**  使用 Dify AI 平台的大模型生成高质量的总结报告。
*   **可配置性：**  通过 `config.toml` 文件灵活配置插件的行为。
*   **异步处理：**  使用 asyncio 进行异步处理，避免阻塞主进程。

## 安装

1.  将 `main.py` 文件保存到 `plugins/ChatSummary/` 目录下。
2.  在 `plugins/ChatSummary/` 目录下创建 `config.toml` 文件，并配置相应的参数。
3.  重启 XYBotV2，以便加载新的插件。

## 配置

`config.toml` 文件用于配置插件的行为。 以下是一个示例：

```toml
[ChatSummary]
enable = true
commands = ["总结", "summary"]
default_num_messages = 20
summary_wait_time = 60

  [ChatSummary.Dify]
  enable = true
  api-key = "YOUR_DIFY_API_KEY"
  base-url = "YOUR_DIFY_BASE_URL"
  http-proxy = ""
