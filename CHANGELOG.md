# Changelog

This file records user-visible changes in public Keva releases.

## 2026.43.6 — 2026-10-24

- **Keva Phone Assistant holds up on heavy screens.** A slow screen read (for example inside a large mini-program page) no longer drops the session. When a read runs out of time, the assistant gets the part of the screen it has already read instead of nothing, and the error no longer claims the command was never sent. In our tests a two-hour task on such a page finished with no dropped session.
- **Back to Keva when the task ends.** When a phone task finishes or you stop it, Keva comes back to the front with the same conversation, including on phones that block apps from bringing themselves forward.
- **See what each step is doing.** The floating capsule shows a short description of the current step, and new notifications follow your tasks: progress while one runs, a heads-up when it needs you, and the result when it ends. You can stop a task from the notification.
- **Errors you can act on.** Failures now show as one card that says whose problem it is (your account, your settings, the network, the model service or Keva itself) and offers the action that helps — switch model, sign in again, compact the conversation or retry. When a Codex usage limit is reached, the card shows when it resets, in your local time; raw error text stays folded under technical details.
- **Stop means stop.** Stopping a task now also stops its checklist, which used to keep spinning.
- **New models.** Kimi K3.1 Pro (1M context) is Kimi's strongest tier and Kimi K3 the balanced one; MiniMax's everyday tiers move to MiniMax M3.1-Flash (1M context).
- **Runtime bumps.** Bundled Claude Code 2.1.308 and Codex 0.163.0. The first launch after updating unpacks the new engines once.

## 2026.41.6 — 2026-10-08

- **20 attachments, and a preview before you send.** Photos and videos have separate pickers, and up to 20 attachments fit in one row of thumbnails. Before sending you can open a preview to play a video, see its resolution, or remove a single item. While the picker is still copying files, the tray shows an importing state and sending waits until it finishes.
- **Bigger media, less copying.** Videos and audio play inline with no size cap. Files the picker already copied are moved into your project instead of copied again, and Keva checks storage space before sending, with a shortcut to clean up storage.
- **Frames from video, on the phone's hardware.** The assistant can extract frames from a video (every keyframe, every N seconds, or at given timestamps) with your phone's hardware video decoder through `keva-media`.
- **Media in the Files tab.** Images and videos open in a swipeable gallery with the rest of the folder's media, a lone video plays in place, and audio files get an in-page player.
- **A new working indicator.** While the assistant works, footprints walk forward step by step; when it finishes, a cinnabar check marks the result. In the video player, the picture is no longer covered by a pause button while playing: tap the video to pause, and the play button comes back when it is paused or ends.
- **Claude Haiku 5.5.** The Claude API's Haiku tier is now Haiku 5.5 (`claude-haiku-5-5`). Claude subscription members get it through the bundled Claude Code, whose `haiku` alias now resolves to Haiku 5.5.
- **Runtime bump.** Bundled Claude Code 2.1.293. The first launch after updating unpacks the new engine once.

## 2026.41.5 — 2026-10-06

- **Make videos on your phone.** The bundled `ffmpeg` and `ffprobe` now work, including CJK fonts for subtitles and on-screen text, so the assistant can cut, mix, subtitle and transcode audio and video right on the device.
- **Hardware video encoding.** The assistant can now encode H.264 with your phone's own hardware video encoder through the new `keva-media` tool. In our tests, encoding a 32-second clip was about 6× faster than software encoding, and the whole job went from 336 s to 131 s. Encodes queue up instead of failing when one is already running, and an encode that is interrupted never leaves a half-written file behind.
- **High-risk commands are approved in place.** When you approve a high-risk command (for example one that deletes files), that same command now runs right away instead of being declined and retried. Once you decide, the approval card folds into a faint one-line record; tap it to see the full command and when you decided.
- **Smoother runtime.** `pip` works out of the box, long renders can run for up to an hour, and the runtime repairs an interrupted or incomplete install on the next launch.
- **Select reply text in one go.** You can now select text continuously across paragraphs, lists, tables and code blocks in the assistant's reply.

## 2026.40.4 — 2026-09-30

- **GPT-6.1 Sol in Codex.** The OpenAI picker's Sol entry is now GPT-6.1 Sol, with reasoning levels low to max (no none/minimal). If you had GPT-6 Sol selected, Keva moves you to GPT-6.1 Sol automatically. Each OpenAI model now only offers, and sends, the reasoning levels it actually supports.
- **Runtime bump.** Bundled Codex 0.159.2. The first launch after updating unpacks the new engine once.
- **A Claude conversation with a lost session recovers.** If a conversation's saved Claude session could no longer be found, every message in it failed at start. Keva now detects this, drops the stale session reference and continues the conversation from its transcript, without an error.
- **Clearer start failures.** When the engine cannot start, Keva shows a specific message with a code instead of a generic "process crashed" error, and only retries when a retry can actually help (for example while the previous session is still shutting down).

## 2026.40.3 — 2026-09-29

- **Claude Sonnet 5.5.** The Claude API's Sonnet tier is now Sonnet 5.5 (`claude-sonnet-5-5`, 1M-token context). Claude subscription members get it through the bundled Claude Code, whose `sonnet` alias now resolves to Sonnet 5.5.
- **Runtime bumps.** Bundled Claude Code 2.1.284 and Codex 0.158.0. The first launch after updating unpacks the new engines once.
- **Claude sign-in works after using another provider.** If you had used a non-Claude model (MiniMax, DeepSeek, …), signing in to your Claude subscription could finish successfully but still be reported as "login info doesn't match", and the usage card showed "can't read usage". Both now work.
- **Signing out of Claude no longer blocks Codex.** Previously, after signing out of Claude while a session was open, Codex sign-in and chats kept failing until you restarted the app.
- **Anonymous install-age range on the update check.** The version check now carries a coarse range of days since install (0, 1–2, 3–6 or 7+) so we can count active installs in aggregate. It still carries no ID and no content; the privacy page is updated to match.

## 2026.39.4 — 2026-09-27

- **No more crash when sending while "Preparing…".** On some devices — notably HarmonyOS phones running Android apps through a compatibility layer — sending a message while the engine was still starting could close the whole app. Keva now waits for that start to finish instead of restarting the engine, and a failing background engine step shows an error in the chat rather than taking the app down.
- **See why Keva closed.** If the app ever closes unexpectedly, the next launch shows a short summary with a "Copy details" button, and Settings › Diagnostics keeps the last report so you can send it to us. The report is built from error types, app steps and device info, and is designed to leave out your conversations.
- **The update page always shows the newest version.** Opening it now checks for the latest release first, instead of showing a result cached from earlier.

## 2026.39.3 — 2026-09-23

- **Claude Opus 5.5.** The Claude API's Opus tier is now Opus 5.5, with its 1M-token context window. Claude subscription members get it through the bundled Claude Code.
- **GPT-6 in Codex.** The OpenAI picker offers GPT-6 Astra, GPT-6 Sol, GPT-5.6 Terra and GPT-6 Luna. If you had GPT-5.6 Sol or Luna selected, Keva moves you to GPT-6 Sol or Luna automatically; the reasoning level for the new model starts at its default.
- **Xiaomi MiMo V2.6.** MiMo now uses V2.6 Pro and V2.6 Flash, both with a 1M-token context window.
- **Runtime bumps.** Bundled Claude Code 2.1.280 and Codex 0.156.0. The first launch after updating unpacks the new engines once.

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
