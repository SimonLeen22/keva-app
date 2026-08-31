# Keva

**A full AI agent for Android, built to do work on your phone.**

Keva brings complete Claude Code and OpenAI Codex runtimes to Android. It can work with files, run code and tools, search the web, and manage Git repositories — without requiring a computer or a cloud desktop.

> The first public Android release is coming soon.

## What this repository is for

Keva is a **closed-source product**. This public repository is the home for:

- release notes and known issues;
- public product documentation;
- bug reports and feature requests;
- security-disclosure instructions.

It does not contain Keva's proprietary application source code, signing keys, internal tooling, or release artifacts.

## Two complete runtimes

- **Claude Code** — use your configured provider or Claude plan.
- **OpenAI Codex** — sign in with a ChatGPT subscription or use an OpenAI API key.

You can switch between the two without starting your work from scratch: Keva carries the current conversation context across the runtime change.

## Public release

The Android APK is not available yet. When it opens, the official download and SHA-256 checksum will be published at [keva.chat/download](https://keva.chat/download/).

## Help and feedback

- Read the [FAQ](docs/FAQ.md).
- Report a reproducible problem using the bug-report template.
- Suggest a product improvement using the feature-request template.
- For security issues, read [SECURITY.md](SECURITY.md) and do not open a public issue.

## Repository map

```text
.
├── README.md                # Product overview and public-release status
├── CHANGELOG.md             # User-facing release notes
├── CONTRIBUTING.md          # Feedback and issue-reporting guidance
├── SECURITY.md              # Private vulnerability disclosure policy
├── docs/
│   └── FAQ.md               # Product and release questions
└── .github/ISSUE_TEMPLATE/  # Bug-report and feature-request forms
```

## License

No source-code license is granted by this repository. The Keva application and its proprietary components are not open source.
