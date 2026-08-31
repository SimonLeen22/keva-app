# Keva — AI agent for Android

[Website](https://keva.chat/) · [Download for Android](https://keva.chat/download/) · [中文说明](README.zh-CN.md) · [FAQ](docs/FAQ.md) · [Changelog](CHANGELOG.md)

> **Run a real AI agent on your Android phone — no PC required.**

Keva is a local-first AI agent for Android. It brings complete **Claude Code** and **OpenAI Codex** runtimes to your phone, so you can work with files, run code and tools, search the web, and manage Git repositories without a computer or a cloud desktop.

**The first public Android release is coming soon.** Follow this repository for release notes, public documentation, and launch updates.

## Why Keva

| | What it means |
|---|---|
| **A real agent, not just chat** | Keva can read and write files, run commands, write code, use tools, search the web, and carry work through to a result. |
| **Two complete runtimes** | Choose Claude Code or OpenAI Codex. Codex supports a ChatGPT subscription or an OpenAI API key. |
| **Built for the phone you already have** | Run on stock Android without root, a PC, or a cloud desktop. Your files, project data, and keys stay on your device. |

## Who it is for

- **Developers** who want to code, inspect repositories, or work with files away from a computer.
- **Researchers and operators** who want an agent to turn a request into a sourced report or a working deliverable.
- **AI power users** who want to choose their own provider, API key, or subscription instead of being locked into one model.

## Real work on a phone

Keva is built for tasks with an outcome, not just a reply. Current public demos show it:

1. building a working Tetris game from scratch on stock Android;
2. using Codex to research a week of AI developments and deliver an HTML industry report.

Watch the demos on the [Keva website](https://keva.chat/#cases).

## Runtimes and access

- **Claude Code:** use your configured provider or Claude plan.
- **OpenAI Codex:** sign in with a ChatGPT subscription or use an OpenAI API key.
- **Additional providers:** DeepSeek, GLM, MiniMax, Kimi, and Qwen are supported through Keva's provider setup.

Switching between Claude and Codex keeps the current conversation context, so you do not need to start the work over.

## Public release

The Android APK is not available yet. When it opens, the official APK and SHA-256 checksum will be published at [keva.chat/download](https://keva.chat/download/). Only download Keva from an official Keva address and verify the checksum.

## Help, feedback, and security

- Read the [FAQ](docs/FAQ.md).
- Open a reproducible bug report or feature request using the issue templates.
- Read [CONTRIBUTING.md](CONTRIBUTING.md) before posting public feedback.
- For vulnerabilities, follow [SECURITY.md](SECURITY.md). Do not open a public security issue.

## About this repository

Keva is a **closed-source product**. This public repository is for product updates, public documentation, feedback, and security-disclosure instructions. It does not contain Keva's proprietary application source code, signing keys, internal tooling, or release artifacts.

```text
.
├── README.md                # English product overview
├── README.zh-CN.md          # 中文产品说明
├── llms.txt                 # Machine-readable product facts
├── CHANGELOG.md             # User-facing release notes
├── CONTRIBUTING.md          # Feedback and issue-reporting guidance
├── SECURITY.md              # Private vulnerability disclosure policy
├── docs/
│   ├── FAQ.md               # English product and release questions
│   └── FAQ.zh-CN.md         # 中文常见问题
└── .github/ISSUE_TEMPLATE/  # Bug-report and feature-request forms
```

## License

No source-code license is granted by this repository. The Keva application and its proprietary components are not open source.
