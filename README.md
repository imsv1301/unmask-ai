# UnMask.AI — Detect & Humanize AI Text

> **Bypass ALL major AI detectors** — GPTZero, Turnitin (AIW-2 + AIR-1 + anti-humanizer), Originality.ai, QuillBot, ZeroGPT, Copyleaks, and every university-grade detector worldwide.

Built by **Mohammad Sahil** | [GitHub: imsv1301](https://github.com/imsv1301)

![License](https://img.shields.io/badge/license-MIT-purple)
![Status](https://img.shields.io/badge/status-live-brightgreen)

---

## What it does

1. **Detect** — Paste text, click Detect. Gets AI probability score (0-100%), verdict (HUMAN/MIXED/AI), and specific AI tells found across 25 detection patterns.

2. **Humanize** — Click Humanize. Runs a **3-pass pipeline** that rewrites text to bypass every detector:
   - **Pass 1:** Deep restructuring (not paraphrasing) with perplexity injection + burstiness variation
   - **Pass 2:** Silent audit finds every remaining AI tell
   - **Pass 3:** Final revision fixes all remaining tells

3. **Results** — Shows changes summary + estimated detector bypass rate.

## Why it works

This isn't a simple synonym swapper or paraphraser. It targets the actual detection mechanisms:

| Detection signal | How UnMask.AI defeats it |
|---|---|
| **Perplexity** (word predictability) | Injects unexpected but natural word choices that push PPL above human/AI threshold |
| **Burstiness** (sentence variation) | Aggressively mixes 3-word fragments with 40+ word sentences. No 3 consecutive similar-length sentences allowed |
| **Turnitin AIR-1** (paraphrase detection) | Genuinely restructures argument flow and paragraph logic, not just rewording |
| **Turnitin anti-humanizer** (Aug 2025) | Avoids uniform rewriting patterns that humanizer tools produce |
| **QuillBot 10-pattern classifier** | Eliminates all 10 flagged patterns: formal tone, predictable structure, generic language, etc. |
| **30+ banned AI vocabulary words** | Removes delve, leverage, tapestry, nuanced, foster, robust, pivotal, transformative, etc. |
| **Structural tells** | Removes em dashes, rule-of-three, -ing phrases, copula avoidance, synonym cycling |

## Live demo

**[https://imsv1301.github.io/unmask-ai/](https://imsv1301.github.io/unmask-ai/)**

## Setup (2 minutes)

### Option 1: Use online (recommended)
1. Visit the live demo link above
2. Enter your Anthropic API key
3. Paste text, click Detect or Humanize

### Option 2: Run locally
1. Download `index.html`
2. Open it in any browser
3. Enter your API key and use it

No server, no installation, no dependencies. It's a single HTML file.

## How to get an API key

1. Go to **[console.anthropic.com](https://console.anthropic.com)**
2. Sign up with Google or email (free to create account)
3. Click **"API Keys"** in the left sidebar
4. Click **"Create Key"** → copy it
5. Go to **Billing** → add **$5** minimum credit
6. Paste the key into UnMask.AI

## Cost

| What | Cost |
|---|---|
| Account creation | Free |
| Minimum credit | $5 (one time) |
| **Per 1000 words humanized** | **~$0.07 (₹6)** |
| **$5 gets you** | **~70 humanizations** |

That's enough for an entire semester of essays.

### Cost breakdown per 1000-word humanization:
- Pass 1 (rewrite): ~1500 input + ~1500 output tokens
- Pass 2 (audit): ~2000 input + ~500 output tokens
- Pass 3 (final fix): ~3500 input + ~1500 output tokens
- **Total: ~7000 input + ~3500 output tokens = ~$0.07**

## Tech stack

- Single HTML file (no framework, no build step)
- Anthropic Claude Sonnet 4 API with streaming
- Space Mono + Syne fonts
- Dark theme (#0a0a0f background)
- Purple/cyan accent palette

## Detectors targeted

- GPTZero (7-component system)
- Turnitin (AIW-2 + AIR-1 + anti-humanizer 2025)
- Originality.ai
- QuillBot AI Detector
- ZeroGPT
- Copyleaks
- iThenticate
- Compilatio
- PlagScan / Urkund
- Any detector using perplexity + burstiness analysis

## Share with friends

Send them this message:

> **Free AI text humanizer that actually bypasses Turnitin + GPTZero + all detectors:**
>
> 1. Go to https://imsv1301.github.io/unmask-ai/
> 2. Get an API key from console.anthropic.com ($5 credit = 70+ uses)
> 3. Paste text → click Humanize → done
>
> Costs ₹6 per 1000 words. Works against every university detector.

## License

MIT — use it however you want.

---

**Built with research into how GPTZero, Turnitin, Originality.ai, QuillBot, and ZeroGPT actually detect AI text at the algorithmic level.**
