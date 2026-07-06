# freeyoutubetranscribe.com

**Paste a YouTube link, read the video.** Free forever, no signup, no limits.

**Try it: [freeyoutubetranscribe.com](https://freeyoutubetranscribe.com)**

[freeyoutubetranscribe.com](https://freeyoutubetranscribe.com) turns any YouTube video into a clean, searchable transcript in seconds: clickable timestamps, chapters, every caption language the video has, and one-click export to TXT, SRT, VTT, or an AI-ready prompt format.

> This is the project's public page. The source code lives in a private repository; all rights reserved. If you want to talk about the project, [get in touch](https://freeyoutubetranscribe.com/contact).

## Why build this

Video is where most of the world's knowledge lands first, but video is a slow and inaccessible format for a lot of people:

- **Deaf and hard-of-hearing users** get a full text alternative to any video.
- **Language learners** can read at their own pace, switch caption languages, and jump to the exact moment a phrase is spoken.
- **People on slow or expensive connections** can read a 40-minute lecture in a few hundred kilobytes instead of streaming hundreds of megabytes.
- **Students, journalists, and researchers** can search, quote, and cite video the way they would a document.
- **Anyone using AI tools** can copy a transcript formatted for pasting straight into a chat assistant.

There is no paywall, no account, no rate limit, and no ads. The service is built so that the marginal cost of one more user is effectively zero, which is what "free forever" requires to actually stay true.

## What makes it unusual

### It works where server-based transcript tools break

YouTube aggressively blocks transcript requests coming from datacenter and cloud IPs, which is why so many transcript sites are slow, broken, or hide behind paywalls that fund proxy fleets. This site takes a different route: the transcript is fetched by **your own browser, directly from YouTube**, the same way it would be if you were watching the video. No scraping servers, no proxies, no per-request cost, nothing to block. A server-side fallback covers unusual networks.

### Every reader makes the library bigger

Each transcript anyone views is cached at the edge and becomes a permanent, search-indexable public page. The sitemap grows automatically from the cache. The public library is literally built by the people who use the tool, one video at a time, at no extra cost to anyone.

### Machine learning that runs on your device

Auto-generated captions arrive as an unpunctuated stream of lowercase words. An opt-in "Fix punctuation" feature runs a real transformer model **inside your browser**: it restores punctuation and capitalization between the words that are already there, and by construction it cannot rewrite, paraphrase, or invent text. The transcript never leaves your device, and because inference runs on the reader's hardware, it stays free at any scale.

### A genuinely zero-budget architecture

The entire stack runs on free-tier edge infrastructure. Fonts are self-hosted, there are no paid APIs anywhere, and the heaviest computation is distributed to the browsers that request it. This is not a free trial subsidized by investors; it is a system designed so that running it costs nothing.

## The details people notice

- Play-sync: open the video and the transcript highlights the line being spoken.
- Chapters parsed from the video and rendered as a table of contents.
- Keyboard shortcuts for search, copy, and navigation.
- Dark mode with no flash on load.
- Copy formats tuned for humans, subtitles, and AI assistants.

## Built with

Astro, Cloudflare Workers and KV, Tailwind CSS, and an on-device transformer via ONNX. Designed and built in 2026.

---

**[freeyoutubetranscribe.com](https://freeyoutubetranscribe.com)** — paste a link, read the video.
