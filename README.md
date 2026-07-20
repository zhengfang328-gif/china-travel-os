# China Travel OS 🇨🇳

> **The operating system for first-time travelers to China.**
> Remove uncertainty. Get answers that actually work.

A mobile-first, English-language guide site built by someone who lives in China — honest, firsthand knowledge about China's digital ecosystem, transport, and daily life. No SEO fluff, no outdated forum posts, no "Amazing China" propaganda.

## Brand

**Honest / Insider / Warm**

- **Honest**: doesn't sugarcoat. Tells you the 3% foreign card fee exists before you find out yourself.
- **Insider**: written by a Hangzhou local who has watched friends struggle through these exact situations.
- **Warm**: approachable, human, occasionally funny. Like a friend who's been there.

**Tagline:** *China, made simple.*

**Audience:** English-speaking first-time travelers — pre-trip researchers (2–4 weeks before departure) and on-the-ground reference (already in China, solving a specific problem on mobile).

## What's Covered

Each guide solves one problem completely — real screenshots, real edge cases, real mistakes.

| Category | Guides |
|---|---|
| **Payments** | [Alipay](guide/alipay.html), [WeChat Pay](guide/wechat-pay.html) |
| **Internet** | [VPN Setup](guide/vpn.html), [eSIM/Data](guide/esim.html) |
| **Apps** | [8 Essential Apps](guide/apps.html) |
| **Intercity Travel** | [High-Speed Trains](guide/trains.html) |
| **City Transport** | [Metro & Bus](guide/metro.html), [Bike Sharing](guide/bike.html), [Ride-Hailing (DiDi)](guide/ride-hailing.html) |
| **Safety** | [Safety Guide](guide/safety.html) (street safety, scams, emergency numbers, healthcare) |
| **Daily Life** | [Daily Life](guide/daily-life.html), [Local Routines](guide/daily-routines.html), [Common Misunderstandings](guide/misunderstand.html) |
| **Checklist** | [First-Time China Checklist](guide/checklist.html) (21 interactive items with localStorage) |

## Design System

**Creative North Star:** *The Field Notebook* — honest, lived-in, organized with care.

- **Typography:** [Literata](https://fonts.google.com/specimen/Literata) (serif headings) + [Work Sans](https://fonts.google.com/specimen/Work+Sans) (sans body)
- **Primary color:** `#D94838` (committed — carries 30–60% of visible surface)
- **Background:** `#FAFAFA` (chroma-zero off-white)
- **Depth:** Border-based (no shadows except on city card hover)
- **Motion:** Targeted properties only, `cubic-bezier(0.4, 0, 0, 1)`, respects `prefers-reduced-motion`
- **Rejects:** Frosted glass, gradient text, eyebrow labels, `transition: all`, Chinese cultural motifs, SaaS landing-page clichés

Full token reference: [DESIGN.md](DESIGN.md) · Brand principles: [PRODUCT.md](PRODUCT.md)

## Tech Stack

- **Static HTML/CSS** — no framework, no build step, no dependencies
- **Google Fonts** — Literata + Work Sans
- **localStorage** — checklist persistence
- **Mobile-first responsive** — 375px+ viewports

## Preview Locally

```bash
# Clone the repo
git clone https://github.com/zhengfang328-gif/china-travel-os.git
cd china-travel-os

# Open the homepage (no server needed)
open index.html        # macOS
start index.html       # Windows
```

Double-click `index.html` in any browser — it's all static files.

## Deploy

Drag the entire `china-travel-os/` folder to:

- [Netlify](https://netlify.com) (drag-and-drop deploy)
- [Vercel](https://vercel.com) (drag-and-drop deploy)
- Any static host (GitHub Pages, Cloudflare Pages, etc.)

No build step required.

## Project Structure

```
china-travel-os/
├── index.html              ← Homepage (Hero + Anxiety + Guide Hub + Cities + Newsletter)
├── guide/                  ← 14 guide pages
│   ├── alipay.html         ← Alipay tutorial
│   ├── wechat-pay.html     ← WeChat Pay tutorial
│   ├── apps.html           ← Essential apps
│   ├── vpn.html            ← VPN setup
│   ├── esim.html           ← eSIM/Data guide
│   ├── trains.html         ← High-speed rail
│   ├── checklist.html      ← Interactive checklist
│   ├── metro.html          ← Metro & Bus
│   ├── bike.html           ← Bike sharing
│   ├── ride-hailing.html   ← DiDi ride-hailing
│   ├── safety.html         ← Safety guide
│   ├── daily-life.html     ← Daily life in China
│   ├── daily-routines.html ← Local routines
│   ├── misunderstand.html  ← Common misunderstandings
│   └── images/             ← Screenshots by subdirectory
├── city/                   ← Hangzhou city guide
├── docs/                   ← Project documentation (Chinese)
├── RULES.md                ← AI agent rules & project conventions
├── DESIGN.md               ← CSS token reference
├── PRODUCT.md              ← Brand & product principles
├── 项目笔记.md              ← Project notes (Chinese)
└── .gitignore
```

## License

© China Travel OS — project documentation and brand materials.
