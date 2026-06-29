# Internal Beyond (IB) — English Edition

A fully offline, single-file personal website with multi-AI integration.

Nine functional modules, two visual themes, all data stored locally in your browser. No servers, no accounts, no data collection.

Customize your profile, character portraits, and system prompts. Connect your own AI API keys to unlock all interactive features.

**This project is permanently free and open source.**

> 🌏 **中文版 / Chinese Version**: [Sui-IB](https://github.com/Sui-IB)

> **Quick Start**: Download the ZIP → extract → open `InternalBeyond.html` in your browser.

---

## ✦ Quick Start

1. Download this repository (click the green **Code** button → **Download ZIP**)
2. Extract the archive and open `InternalBeyond.html` in your browser
3. Go to **API Settings** and add your AI API key
4. Start exploring

Basic features (journal, wardrobe, theme switching, music playback, etc.) work offline. AI-related features require an internet connection for API calls.

## ✦ Features

| Module | Description |
|--------|-------------|
| **Room** | Pixel-art interactive room (1672×941), featuring Sui dialogue, tea break, interactive story, tarot reading, wardrobe, and sleep — six sub-modules |
| **Chat** | Multi-endpoint AI real-time conversations — floating panel + fullscreen + group chat + thinking chain + mini companion window |
| **Blog** | Journal / password diary / AI comments / custom scripts |
| **Letters** | AI correspondence — asynchronous letter exchange where AI reads your profile and writes back |
| **Memory** | Long-term emotional memory — star map visualization + natural decay + automatic API context injection |
| **Music** | Local music player + 48-band frequency visualizer |
| **Profile** | Liquid glass personal card — avatar + bio + portfolio |
| **API** | Multi-endpoint config hub — up to 10 independent APIs, each with nickname, relationship, and system prompt |
| **DIY** | Custom transparent character portraits and tarot tablecloth |

## ✦ Theme System

Toggle via the droplet button in the navigation bar:

- **Internal** — Light mode. The Room shows a daytime scene (prismatic rainbow light, weather effects, and floating particles).
- **Infernal** — Dark mode. The Room shows a nighttime scene (moonlight, candlelight, and soft warm glow effects).

Background images crossfade smoothly, the homepage title fades out and rewrites, rain effects and UI color palette adapt in sync.

## ✦ Module Details

### Room — Pixel Interactive Space

Access via the Room link in the navigation bar (fullscreen) or the `[Room]` tab on the right side of the screen (floating panel with resize and drag support). The floating panel supports Mini mode — a draggable mini window that hovers in the corner, perfect for keeping Sui nearby while browsing other pages.

- **Sui**: Dialogue with the room's host. Start a guided tour of the room.
- **Tea**: Emotional dialogue space. 5 beverages × 5 desserts = 25 unique atmosphere combinations, designed around attachment theory, polyvagal theory, and self-determination theory. Conversations save to the password diary by default, up to 52 rounds.
- **Story**: AI-driven branching narrative engine. 5 genre types + adjustable horror level + custom scripts. 12–16 rounds of narrative with 3 normal endings and 1 hidden ending.
- **Tarot**: Full 78-card Rider-Waite deck, 5 spreads + optional guidance card + real-time AI interpretation. Complete operation log can be saved at any time.
- **Wardrobe**: 6 outfits with instant switching.
- **Sleep**: Character lies down to rest. Click anywhere to wake up.

### Chat — Real-Time Dialogue

Floating panel and fullscreen mode. Friend list is auto-generated from API configurations. Supports group chat, thinking chain display, message deletion, history search, and calendar view. One-click memory generation to the Memory module.

### Blog — Journal System

Write journal entries, manage categories, invite AI comments. The password diary is protected and hidden from all APIs — Tea and Story archives save here by default. Entries can trigger AI memory generation.

### Letters — Correspondence System

Select an AI friend to request a letter. The AI reads your Profile, recent journals, and chat history, then writes a personalized reply.

### Memory — Long-Term Memory

An emotional long-term memory system inspired by the Ombre Brain concept. Each memory carries emotional coordinates (valence/arousal), importance score, and natural decay. The star map visualizes all memories on a 2D emotional plane; the timeline displays them as planetary forms. Up to 7 pinned memories, four visibility levels. Multiple creation sources (manual / Chat / Blog / Letters / Story / Tea). Relevant memories are automatically retrieved and injected into API context, with a configurable token budget.

### DIY — Creative Workshop

Configure custom transparent portraits (PNG, recommended 800×920) for each API, displayed in Story/Tea dialogue panels. Custom tarot tablecloth (1920×1080). A test portrait `portrait_[Cluade].png` is included in the game folder — rename the bracket content to match your API nickname and test.

## ✦ API Configuration Guide

IB supports various AI services (up to 10 endpoints):

### Official APIs

| Provider | Registration | IB Selection | Key Format |
|----------|-------------|--------------|------------|
| Anthropic (Claude) | console.anthropic.com | `Claude (Anthropic)` | sk-ant-… |
| OpenAI (GPT) | platform.openai.com | `GPT (OpenAI)` | sk-… |
| DeepSeek | platform.deepseek.com | `DeepSeek` | sk-… |
| Google (Gemini) | aistudio.google.com | `Gemini (Google)` | AIza… |

Select a provider, and the endpoint URL and default model will auto-fill. Just paste your API key.

### Custom / Relay APIs

If you cannot access overseas APIs directly, you can use a relay service (API proxy):

1. Register and add credits on the relay platform
2. Obtain the API key, endpoint URL, and available model names
3. In IB's API settings, select **Custom** as the provider and fill in the details
4. Save and you're ready

### World-Building

Set a custom world-building prompt in the API Settings system prompt field — it will be automatically injected into all AI features. The Story module supports an independent personalization toggle.

## ✦ Data Management

- **Export**: Navigation bar Export → all data exported as a JSON file. Memory also supports standalone import/export.
- **Import**: Import → select a JSON backup file. Incremental merge without overwriting.
- **Storage**: Browser IndexedDB, fully offline.
- **⚠ Backup Reminder**: All data is stored locally in your browser only. Clearing browser data will permanently delete everything. Please back up regularly.

## ✦ Device Compatibility

Requires a modern browser with IndexedDB, CSS backdrop-filter, and ES6+ support.

- ✅ Windows / macOS / Linux (Chrome / Edge / Firefox recommended)
- ✅ iPhone / iPad (Safari)
- ✅ Android / Huawei / HarmonyOS
- The Room module is designed for a 1672×941px viewport and is best experienced on desktop. Mobile devices can access all non-Room features.

## ✦ Project Structure

```
InternalBeyond.html       ← Main file (open this in your browser)
game/
  game_module.js           ← Pixel room engine
  *.png                    ← Sprite sheets and scene assets
  portraits/               ← Character portraits (default + user DIY)
```

## ✦ Technical Specifications

- **Architecture**: Pure frontend single-file HTML + standalone game engine JS. No frameworks, no build tools, no servers.
- **Fonts**: Cormorant Garamond · Noto Sans SC · Noto Serif SC · Raleway · Great Vibes · Spectral (Google Fonts CDN).
- **Visual Effects**: CSS glassmorphism, canvas rain (45 drops) and water ripples, prismatic light, candlelight and moonlight, floating dust, crossfade transitions.
- **AI Protocol**: Anthropic native format + OpenAI-compatible format, covering official and relay APIs.
- **Built with**: Claude (Opus 4.6) primary development · Opus 4.8 / Sonnet 4.6 / Fable 5 assisted programming · GPT-IMAGE-2 textures · Adobe Photoshop CS design and illustration.

---

## ✦ Contact

- GitHub: [Sui-IB](https://github.com/Sui-IB)
- X / Twitter: [@underthepuresky](https://x.com/underthepuresky)
- Email: 1282901880@qq.com

## ✦ License

© 2025–2026 Sui. All rights reserved.

This is an original personal creative work — all code and design are original. Free to download and use. Not for commercial use or resale.

All character sprites and scene assets were designed and created by Sui. This project was built using Anthropic Claude (Opus 4.6), with Claude (Opus 4.8), Claude (Sonnet 4.6), and Claude Fable 5 assisting in programming. Some textures were generated by OpenAI GPT-IMAGE-2. UI design and illustration used Adobe Photoshop CS. AI tools are creative aids and do not hold copyright over the project content. This notice applies to all versions and derivative forms.

**If you obtained this project through a paid transaction, you did not receive the official version.** Please contact the author through the channels above for the free, official release.
