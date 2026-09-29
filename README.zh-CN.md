# Keva（可行）— Android 手机上的 AI 智能体

**只要你说，就可行。**

[官网](https://keva.chat/) · [安卓版下载](https://keva.chat/download/) · [English](README.md) · [开发手记](docs/why-i-built-keva.zh-CN.md) · [常见问题](docs/FAQ.zh-CN.md) · [更新日志](CHANGELOG.md) · [论文](docs/paper/Keva_Paper_v1.1_ZH.md)

> **把真正能干活的 AI 智能体装进 Android 手机，不需要电脑。**

Keva 是一款本地优先的 Android AI 智能体。它把完整的 **Claude Code** 和 **OpenAI Codex** 运行时带到手机上：读写文件、运行代码和工具、联网检索、管理 Git 仓库，都不需要 PC 或云端桌面。

**当前 Android 版本为 2026.40.3**，可从 [keva.chat/download](https://keva.chat/download/) 下载。本版新增 Claude Sonnet 5.5，并升级内置的 Claude Code（2.1.284）与 Codex（0.158.0）；修复了用过其他模型后 Claude 会员登录与用量卡片误报失败，以及退出 Claude 登录后 Codex 无法使用的问题。历次版本见[更新日志](CHANGELOG.md)，关注本仓库可获取版本动态和公开文档。

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
- **其他服务商**：Keva 的服务商配置支持 DeepSeek、GLM、Kimi、LongCat、MiniMax、Qwen 和小米 MiMo。

Claude 与 Codex 之间切换时，当前对话上下文会被保留，不必从头交代工作。

## 公开发布

请从 [keva.chat/download](https://keva.chat/download/) 获取官方 APK 与 SHA-256 校验值。只从 Keva 官方地址下载，安装前核对校验值。

## 反馈与安全

- 查看 [常见问题](docs/FAQ.zh-CN.md)。
- 使用 Issue 模板提交可复现的问题或功能建议。
- 如果 Keva 意外退出，下次打开会弹出崩溃摘要：点「**复制详情**」（或在「**设置 › 运行诊断**」里查看保留的上次报告），粘贴到问题反馈里即可。报告由错误类型、App 操作步骤和设备信息组成，设计上不包含你的对话内容。
- 提交公开反馈前请阅读 [CONTRIBUTING.md](CONTRIBUTING.md)。
- 安全漏洞请遵循 [SECURITY.md](SECURITY.md)，不要公开提交 Issue。

## 本仓库的边界

Keva 是**闭源产品**。本公开仓库用于发布产品动态、公开文档、收集反馈和提供安全披露说明；不包含 Keva 的专有 App 源码、签名密钥、内部工具或发布产物。
