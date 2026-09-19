# Changelog

This file records user-visible changes in public Keva releases.

## 2026.38.8 — 2026-09-19

- **Sign-in behind VPN proxies.** Codex sign-in no longer needs an app restart when the proxy came up after the app did; the app re-checks the proxy on every explicit sign-in tap.
- **Strict battery restrictions.** On phones that restrict the app's background activity, Keva no longer crashes about half a minute after launch; Settings explains the restriction instead.
- **Settings fixes.** The status bar stays readable in the light theme; the account row shows the real device count right after launch.
- **Cleaner update screens.** One headline, one line of details.

## 2026.38.5 — 2026-09-17 · First public release

Download: https://keva.chat/download/ (APK with SHA-256 checksum).

- **Automatic update checks.** Keva now looks for new versions on its own. Optional updates show up in Settings and on the chat page; required updates open a full-screen download guide. Installing an update keeps your data.
- **"Version & updates" in Settings.** Current version, last check time, one-tap check, and a dot on the Settings tab when an update is waiting.
- **Task checklists in Claude mode.** Multi-step jobs start with a checklist and tick items off as they go.
- **Task checklists in Codex mode.** The same checklist card now appears when Codex plans a task.
- **Accurate sub-task counter.** "Running N of M" counts down correctly for parallel sub-tasks, and each turn keeps its own checklist instead of overwriting the previous one.
- **Cleaner worklog.** Codex sub-task operations (wait, message, close) read as plain language instead of raw identifiers.
- **Better behind VPNs and proxies.** The app's own requests (update checks, model discovery) use the same proxy settings as the built-in CLIs.
- **Faster sending.** Messages no longer wait on a location fix; connections are reused, with fewer false "network error" reports.
- **Redesigned new-chat page.** Clearer welcome copy and four scene cards: documents, files, search, code.
- **Copy polish and runtime bumps.** Hundreds of strings revised in English and Chinese; DeepSeek defaults to deepseek-v4.1-flash; bundled Claude Code 2.1.259 and Codex 0.153.4.

Earlier, unreleased builds added the complete Claude Code and OpenAI Codex runtimes, Codex sign-in with a ChatGPT subscription or OpenAI API key, and conversation context that survives switching between Claude and Codex.
