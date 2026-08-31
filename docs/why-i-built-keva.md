# Why I built Keva

*A note written before the first public release. — Simon, August 31, 2026*

[中文版](why-i-built-keva.zh-CN.md)

![A hand holding a phone in a dark room; the light from its screen spills forward and becomes a full workbench of lamp, drafting sheets and tools.](https://keva.chat/assets/img/story-01-workbench.jpg)

---

It started in February, just before Chinese New Year, when OpenClaw was released.

I deployed it to my MacBook first. But a laptop can't stay awake around the clock, so I moved it onto a cloud VPS and started talking to it every day through Telegram. The model behind it went from MiniMax-M2.5 to M2.7 to M3. Until then I had never used an AI agent product, and I had never paid for a single model API key.

I was electrified. I believed a new era for individual productivity had arrived.

Over the holiday I started building something for my colleagues on top of OpenClaw — an internal assistant called Dragon Assistant, a web interface that let anyone at the company talk to a cloud OpenClaw instance directly. I reworked it from a multi-instance multi-tenant architecture into the single-instance multi-tenant design it uses today. To forward OpenClaw's WebSocket protocol out to the public internet, I read its source code very carefully. It was the first time in my life I had worked inside a TypeScript codebase.

When MiniMax-M2.7 rendered that first chat page, I was overjoyed. The bad news arrived quickly. M2.7 simply wasn't capable enough, and the first version never fully came together. I hadn't written a line of code since 2009, the year I left engineering to become a product manager.

So I paid for Claude. On February 25, with Claude's help, the first version finally ran end to end.

On March 1, it fell apart. OpenClaw had upgraded its security model, and the code I had just gotten working stopped working. Eighteen more days went into it. On March 18 I finally delivered the first version to my colleagues. Nothing remarkable — a multi-tenant web build of OpenClaw, with the company knowledge base loaded in. A week later I delivered an AI-driven quoting system. My colleagues didn't take to it. I ran a survey; most of them opened it once and decided it wasn't much use.

Instead of inventing a need, I went looking for a real one. The company had no CRM, and the colleague responsible for the customer database was under real pressure. She asked me for a customer visit and reporting system, and I decided to build it.

April was a long month. CRM business flows turned out to be more complex than anything I had built in my entire internet career. On April 20, a CRM whose architecture was designed and whose code was written 100% by AI, on an AI backend, went into my colleagues' hands.

In the first week after it launched, the requests came flooding in. One day I was out with no laptop and an urgent bug needed fixing. I ran the Claude Code CLI inside Termux on my Android phone and fixed it right there. It worked. I kept working that way for a few days — and an interactive CLI on a small screen is a miserable experience. That was the first time I thought about building a phone client. At the very least it would make my own work faster and my own days happier. It turned out to be even better than I imagined: I can now fix a bug and push to production anywhere, at any moment.

![A person standing alone on a city street at night, absorbed in the phone in their hands, its screen the brightest thing in the frame.](https://keva.chat/assets/img/story-02-street.jpg)

My instinct was pointing the right way. China is a mobile-first country. Most of us don't have the habit of carrying a laptop out the door, and plenty of people don't own one at all. Does creating with AI really have to require a computer? I picked up nearly two decades of product experience and got to work.

The project began in earnest in early June, and the build was finished by mid-July. I have used it every day since. Soon we will hand it to you — Keva, an AI agent that runs natively on an Android phone, with no cloud sandbox behind it and all your data kept local.

In early June I talked to Opus 4.7, the most capable model in the world at that moment. I said I wanted to wrap the Claude Code CLI into a chat app. Opus told me it wasn't possible. I asked why. It said power management and keeping the process alive couldn't be solved — Android would kill it. I said: no. Difficulty is exactly the reason to try. Termux can run it, so this can be solved. Let's start.

I was worried that one model's verdict wasn't reliable enough, so I brought in GPT-5.5, the best model available at the time, to argue it through with Opus 4.7. The two most powerful models in the world. As I remember it, the technical verification ran for fifty hours and drained my subscription quota round after round after round. GPT-5.5 found a way, and that became the first Claude Code runtime. That was the first token furnace — in that stretch, there was simply never enough quota. The method depends on an old Android API. I'm grateful Google never retired it. It's the reason this thing exists at all.

![A vast wall of identical closed doors. A single blade of red light escapes from beneath one of them, and the floor carries the overlapping tracks of a long search.](https://keva.chat/assets/img/story-03-doors.jpg)

The second technical verification came in early August. Codex was at its peak, resetting almost every day, and its subscriber count had climbed past ten million. The moment had come to support both runtimes. The single-runtime version had been finished for two weeks. On a PC or a Mac, hot-switching process management between one runtime and two is easy; inside the SELinux environment of a phone, it is hell. So Claude, Codex and GLM subscriptions all went in at full power. The verification was supposed to take two days. On a road nobody had walked before, it took ten. The day it ended, the token counter on my computer told me I had burned 11 billion tokens in a single week. The actual development work took two days. Then came another two weeks of running it on real devices, using it and hardening it almost every single day.

Underneath Keva's Flutter layer sits a complete Ubuntu userland, running within Android's SELinux constraints. Inside that Linux we install the full Claude Code CLI and Codex CLI, along with dozens of everyday Linux tools including Git, SSH and Python. On the Android side, a great deal of work went into power management and keep-alive watchdogs. Keva supports both native API access and subscription sign-in for Claude and Codex. It also supports DeepSeek, GLM, Kimi, LongCat, MiniMax, Qwen and Xiaomi MiMo, plus a custom provider slot for models or API aggregators that aren't on the list. All of these run on top of Claude Code, primarily over the Anthropic protocol.

The first version that actually ran was born in mid-July. From then until now, I have maintained every work repository I own from inside Keva, and I've built myself a handful of personal agent CLI projects, including one for managing my own health. I believe the CLI will eventually replace every utility app, because the expert models live inside the agent. My personal health agent keeps track of my weight, body fat percentage, calories and exercise data — one agent replacing at least three apps on my home screen. That, I think, is where mobile agents are going.

Keva is heavy. The runtime takes up a lot of room: 3–4 GB of storage on your phone, most of it a complete Linux operating system and its runtimes. If that space makes your work and your life substantially easier, it's worth it. And a ¥1,200 (about US$170) Redmi Android phone runs Keva smoothly.

Here is what I hope for Keva.

If you are an engineer or a one-person company, I hope you can work efficiently with AI from your phone, anywhere, at any time — instead of having to carry a laptop every day of your life.

If you are a student, and there is no computer at home, and you have no time for a computer lab or an internet café, I hope a small amount of spending on tokens is enough to let you feel what it is to create alongside AI. I hope it opens your imagination. Learn to create with AI early, from the phone in your hand — you will be a native of this technology. Spending a little pocket money on tokens is worth it. You will find yourself more creative than anyone your age.

![A young person sitting on the floor of a small bare room; the light from their phone rises and opens into the outline of an enormous, half-built city.](https://keva.chat/assets/img/story-04-room.jpg)

Or whoever you are: when a good idea arrives, wherever you happen to be, open Keva on your phone and start making the thing that belongs to you. You shouldn't have to wait until you're home and in front of a computer.

And in places where not everyone can afford a computer, I hope Keva brings a measure of equality to learning and to personal creation. AI will give humanity more equal opportunities to create.

We would also like to call on more model providers to offer free token support to children who are still in school.

A few practical notes. Claude subscriptions, Codex subscriptions and DeepSeek all come with native web search. For other models you'll need to configure a search API yourself, which isn't complicated. We've built in a location toggle as well; you'll need to configure a map service API for it, which also isn't complicated. You might say Gemini is more efficient for this — maybe so. But everyone's creativity is different, and someone may well build something unexpected with it. If you do, I hope you'll share it. That feature came from a request by a European user in our closed beta.

**Why "Keva"? (可行)**

I've spent ten years studying brand advertising, and the positioning I wrote for this project is: *Say the word. It's done.* Yes — there is nothing you can't finish on a phone. That is the magic of the mobile agent. Knowing and doing as one thing. Think of it, say it, go do it. You will get a result.

![A single gesture read left to right: breath gathers into a brush stroke, and the brush stroke resolves into a built structure.](https://keva.chat/assets/img/story-05-word.jpg)

If you have a good case study, a good piece of work, a problem, or any feedback at all, please get in touch. I'll do my best to respond quickly.

- Website: <https://keva.chat/>
- GitHub: <https://github.com/SimonLeen22/keva-app>
- My X: <https://x.com/simonlin>
- Email: <hello@keva.chat>
