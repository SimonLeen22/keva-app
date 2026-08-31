# Keva（可行）— Android 手机上的 AI 智能体

**只要你说，就可行。**

[官网](https://keva.chat/) · [安卓版下载](https://keva.chat/download/) · [English](README.md) · [开发手记](docs/why-i-built-keva.zh-CN.md) · [常见问题](docs/FAQ.zh-CN.md) · [更新日志](CHANGELOG.md)

> **把真正能干活的 AI 智能体装进 Android 手机，不需要电脑。**

Keva 是一款本地优先的 Android AI 智能体。它把完整的 **Claude Code** 和 **OpenAI Codex** 运行时带到手机上：读写文件、运行代码和工具、联网检索、管理 Git 仓库，都不需要 PC 或云端桌面。

**首个公开 Android 版本即将开放。** 关注本仓库可获取版本动态、公开文档和上线消息。

## Keva 有什么不同

| | 这意味着什么 |
|---|---|
| **不止聊天，能把事做完** | 读写文件、运行命令、写代码、调用工具、联网查证，并把任务推进到结果。 |
| **两套完整运行时** | 可选择 Claude Code 或 OpenAI Codex；Codex 支持 ChatGPT 订阅或 OpenAI API Key。 |
| **为手机而生** | 原生 Android 无需 root、无需电脑、无需云端桌面；文件、项目数据和密钥留在你的设备上。 |

## 适合谁

- **开发者**：离开电脑时仍想写代码、查看仓库、处理文件。
- **研究和运营人员**：把一个需求变成有出处的报告或可交付成果。
- **AI 重度用户**：希望自己选择服务商、API Key 或订阅，不被锁定在单一模型里。

## 手机上的真实案例

Keva 面向的是有明确结果的任务，而不只是一次对话。目前公开演示包括：

1. 在原生 Android 上从零做出一个可运行的俄罗斯方块；
2. 通过 Codex 调研一周 AI 动态，并交付一份 HTML 行业周报。

可在 [Keva 官网案例区](https://keva.chat/#cases) 查看演示。

## 运行时与接入方式

- **Claude Code**：使用你配置的服务商或 Claude 方案。
- **OpenAI Codex**：使用 ChatGPT 订阅登录，或填写 OpenAI API Key。
- **其他服务商**：Keva 的服务商配置支持 DeepSeek、GLM、MiniMax、Kimi 和 Qwen。

Claude 与 Codex 之间切换时，当前对话上下文会被保留，不必从头交代工作。

## 公开发布

APK 暂未开放。首个公开 Android 版本上线后，官方 APK 和 SHA-256 校验值将发布在 [keva.chat/download](https://keva.chat/download/)。请只从 Keva 官方地址下载，并核对校验值。

## 反馈与安全

- 查看 [常见问题](docs/FAQ.zh-CN.md)。
- 使用 Issue 模板提交可复现的问题或功能建议。
- 提交公开反馈前请阅读 [CONTRIBUTING.md](CONTRIBUTING.md)。
- 安全漏洞请遵循 [SECURITY.md](SECURITY.md)，不要公开提交 Issue。

## 本仓库的边界

Keva 是**闭源产品**。本公开仓库用于发布产品动态、公开文档、收集反馈和提供安全披露说明；不包含 Keva 的专有 App 源码、签名密钥、内部工具或发布产物。
