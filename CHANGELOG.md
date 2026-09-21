# Changelog

This file records user-visible changes in public Keva releases.

## 2026.39.2 — 2026-09-21

- **No more false 15-second timeouts.** A turn whose first reply took longer than 15 seconds — image generation, or the first message after the engine had been idle — could be cut off as "no reply after 180 s". That guard is gone; the timeout message now reports how long you actually waited.
- **Codex reconnects no longer fail the task.** When the Codex stream reconnects mid-task ("Reconnecting… 2/5"), the turn keeps running and shows "Retrying" instead of ending with an error.
- **Pictures and videos, right in the chat.** Images and videos the assistant produces now appear as a photo grid under its reply (up to nine tiles, "+N" beyond that). Tap to open a gallery you can swipe through and pinch-zoom; videos play in the app, with a fallback to your system player.
- **Up to six attachments, picked at once.** The gallery and file pickers accept multiple selections; the limit is six per message.
- **Large photos no longer freeze the send button.** Camera originals are resized by dimension in the background as soon as you pick them, keeping detail instead of squeezing them into a tiny file. HEIC/AVIF images are sent as files for now.
- **Third-party models keep working when your Claude subscription lapses.** An expired Claude sign-in no longer blocks Minimax, DeepSeek, Kimi and other API providers.
- **Staying signed in.** A sign-in that was interrupted mid-refresh (an update, the system killing the app) no longer signs you out on every device. This part is a server change and applies to all versions.
- **Image conversations resume reliably.** Long Codex conversations that include images no longer time out when resumed.

## 2026.38.9 — 2026-09-20

- **"Engine is already running" fix.** After cancelling a Codex sign-in or switching models, every Claude-side model (Kimi, DeepSeek, …) could fail with `E-PROC-?` and "CODEX engine is already running", and swiping the app away did not clear it. Sign-in and account checks now release the engine when they finish, the app reconciles a leftover engine on launch, and a refused start shows `E-ENGINE-BUSY` with a plain explanation instead of a crash code.

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
