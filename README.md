# Keva — AI agent for Android

**Say the word. It's done.**

[Website](https://keva.chat/) · [Download for Android](https://keva.chat/download/) · [中文说明](README.zh-CN.md) · [Why I built Keva](docs/why-i-built-keva.md) · [FAQ](docs/FAQ.md) · [Changelog](CHANGELOG.md) · [Paper](docs/paper/Keva_Paper_v1.1_EN.md)

> **Your Android phone, now the AI agent's computer.**

Keva puts the official **Claude Code** and **OpenAI Codex** CLIs on your phone, with the model you choose. The agent works with your files, the phone's GPS and video hardware, and — with your permission — your other apps. No PC, no root, no cloud desktop.

**The current Android release is 2026.43.7** — download it at [keva.chat/download](https://keva.chat/download/). It fixes Phone Assistant setup getting stuck on step 6 when Android stops accepting Keva's saved pairing. The 2026.43.6 release before it made Keva Phone Assistant hold up on heavy screens and return to Keva when a task ends, added a step-by-step capsule and task notifications, showed errors as one clear card with the action that helps, and added Kimi K3.1 Pro and MiniMax M3.1-Flash. See the [Changelog](CHANGELOG.md) for every release, and follow this repository for release notes and public documentation.

## Why a phone can do this

| | What it means |
|---|---|
| **The phone is the computer** | Keva puts a shell, files, Git, Python, Node and ffmpeg on your phone, so the agent has a real place to work. It doesn't run desktop apps; it gives the agent what it needs. |
| **A full agent, with the model you pick** | The official Claude Code and Codex CLIs are built in. The agent runs on the phone; the model runs at your provider, and requests go straight there, never through Keva. |
| **Your phone's GPS and video hardware** | With your permission, maps tasks can use where you are; coordinates are never logged. Video is decoded and encoded on the phone's own hardware, so a 1080p film is made right on the phone. |
| **Your other apps, with you in control** | Pair Android's Wireless debugging with Keva once, on the same phone. Then it reads the screen and taps, swipes and types in your other apps. A floating capsule shows each step; take over or stop any time. |

## What you can get done

- **Documents** — reports, contracts, spreadsheets, written and polished, ready to send. *"Turn this week's notes into a three-paragraph report."*
- **Code** — build a small tool, or fix one that won't run. *"Make me a small web page that tracks my spending by month."*
- **Edit video** — turn your clips into a short, ready to post. *"Cut these clips into 30 seconds with gentle music."*
- **Phone Use** — with your permission, it gets tasks done in your other apps. *"Find the cheapest flight from New York to Tokyo next Wednesday."*

## See it work

1. **Build a Tetris game from one request** — it writes the code, reviews and fixes it, then you play it in the phone's browser.
2. **Turn travel clips into a short film** — it looks through the footage, cuts to your pace, adds music and captions, and saves the film.
3. **Check flight prices in Expedia** — say where and when; it opens the app, taps through to the flight list and shows you the prices. You can take over or stop it at any time.

Watch the films on the [Keva website](https://keva.chat/#watch).

## Models and access

- **Claude Code:** sign in with a Claude plan, or use an API key or provider.
- **OpenAI Codex:** sign in with a ChatGPT subscription, or use an OpenAI API key.
- **More providers:** DeepSeek, GLM, Kimi, LongCat, MiniMax, Qwen and Xiaomi MiMo, plus one slot for your own Anthropic-compatible endpoint.

Switching between Claude and Codex keeps the current conversation context, so you do not need to start the work over.

## Your files stay on your phone

Files, chat history and model API keys stay on your device. What you send and the files a task uses go straight to the model provider you choose — never to Keva. While Phone Use is working, screen content goes to that provider too. Keva's own service sees only an anonymous version check and, when you sign in or buy, the account, license, payment and device data needed to activate; Paddle handles card data. No trackers, no analytics SDKs.

## Pricing

Every feature is unlocked for a 7-day trial. After that, a one-time license covers two devices: founder price US$19.90 (¥98) for the first 100 orders, then US$39.90 (¥198). Model usage is billed separately by your provider. See [keva.chat/pricing](https://keva.chat/pricing/).

## Public release

Download the official APK and its SHA-256 checksum from [keva.chat/download](https://keva.chat/download/). Only download Keva from an official Keva address and verify the checksum before installing.

## Help, feedback, and security

- Read the [FAQ](docs/FAQ.md).
- Open a reproducible bug report or feature request using the issue templates.
- If Keva closed unexpectedly, the next launch offers a crash summary: tap **Copy details** (or open **Settings › Runtime diagnostics**, which keeps the last report) and paste it into your bug report. It is built from error types, app steps, and device info, and is designed to leave out your conversations.
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
│   ├── FAQ.zh-CN.md         # 中文常见问题
│   ├── why-i-built-keva.md  # Founder's note before the first release
│   └── why-i-built-keva.zh-CN.md  # 开发手记（中文）
└── .github/ISSUE_TEMPLATE/  # Bug-report and feature-request forms
```

## License

No source-code license is granted by this repository. The Keva application and its proprietary components are not open source.
