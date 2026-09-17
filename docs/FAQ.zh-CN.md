# 常见问题

## Keva 开源吗？

不开源。Keva 是闭源产品；本仓库是产品动态、公开文档和用户反馈的公开入口。

## 在哪里下载？

首个公开 Android 版本（2026.38.5）已在 [keva.chat/download](https://keva.chat/download/) 开放下载，并附 SHA-256 校验值。请只从 Keva 官方地址下载。

## 安装时 Google Play 保护机制提示「已屏蔽不安全的应用」，有问题吗？

没有。可行在手机里跑一整套 Linux 运行环境（和 Termux 一样），这类应用只能面向 Android 9 的接口级别构建，所以新版 Android 会提示「此应用是针对旧版 Android 开发的」。点「仍要安装」即可（有些手机要先点「详细了解」再选「仍要安装」）。请只从 keva.chat 下载，安装前核对下载页上的 SHA-256。

## 需要 root 或电脑吗？

不需要。Keva 作为普通 Android 应用运行在原生设备上，不需要 root 或另一台电脑。

## 包含哪些 AI 运行时？

Keva 内置 Claude Code 与 OpenAI Codex。Codex 可使用 ChatGPT 订阅或 OpenAI API Key；同时支持 DeepSeek、GLM、MiniMax、Kimi 和 Qwen 等服务商。

## 我的数据会去哪里？

文件、项目数据和密钥留在设备上；消息会发送给你选择的模型服务商。Keva 不运行数据分析，仅使用极简匿名版本检查来交付必要更新。
