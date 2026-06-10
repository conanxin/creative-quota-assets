# Creative Quota Assets

**Open source AI generation asset library — prompts, briefs, and metadata for creative AI workflows.**

> Powered by [creative-quota-harvester](https://github.com/conanxin/creative-quota-harvester). Assets are sourced from real-world signals (academic papers, open source projects, cultural collections) and transformed into reusable generation prompts.

[![CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-blue.svg)](https://creativecommons.org/licenses/by/4.0/)
[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/conanxin/creative-quota-assets/blob/main/LICENSE)

## Live Gallery

**Browse the asset gallery:**
```
https://conanxin.github.io/creative-quota-assets/gallery/
```

Or open `gallery/index.html` directly — no build required.

---

## Project Status

| Phase | Status | Description |
|-------|--------|-------------|
| Phase 0A–2B | ✅ Complete | Signal collection through asset gallery |
| **Phase 2C** | **✅ Complete** | **GitHub open source publish + GitHub Pages** |
| Phase 3A | ⬜ Planned | MiniMax quota-aware generation |
| Phase 3B | ⬜ Planned | Telegram daily report |
| Phase 4 | ⬜ Planned | Scheduled automation |

**Note:** This repo contains prompts and metadata only — no real generated images, music, or video yet. Media generation is Phase 3A.

---

## Project Structure

```
creative-quota-assets/
├── content-packs/           ← Self-contained brief + prompt bundles
│   └── YYYY/MM/YYYY-MM-DD/  ← Date-organized content packs
│       └── brief-*/         ← One pack per creative brief
│           ├── manifest.json       # Pack metadata
│           ├── source.json         # Source signal references
│           ├── signal.json         # Original signal data
│           ├── brief.md            # Creative brief (human readable)
│           ├── facts.md            # Factual basis + source links
│           ├── x-post.zh.md        # Chinese X (Twitter) post draft
│           ├── image-prompt.md     # Image generation prompt
│           ├── video-prompt.md     # (conditional) video prompt
│           ├── music-prompt.md     # (conditional) music prompt
│           ├── webpage-outline.md # Webpage structure
│           └── asset-plan.json     # Full asset plan
├── gallery/
│   ├── index.html          ← Web gallery (static HTML/JS, no build)
│   └── assets.json         ← Gallery asset index
├── metadata/
│   ├── asset-index.json     # All assets master index
│   ├── source-index.json   # Assets grouped by source type
│   └── daily-index.json    # Assets grouped by date
├── images/                 # Generated images (Phase 3A+)
├── music/                   # Generated music (Phase 3A+)
├── videos/                  # Generated video (Phase 3A+)
└── prompts/                 # Standalone prompt files
```

---

## Content Pack Format

Each `content-pack/` is a **self-contained directory** — no build step, no database. Open `brief.md` for the full creative brief, or use individual prompt files directly.

```bash
# Read a brief
cat content-packs/2026/06/2026-06-10/brief-*/brief.md

# Use an image prompt
cat content-packs/2026/06/2026-06-10/brief-*/image-prompt.md

# Read the Chinese X post draft
cat content-packs/2026/06/2026-06-10/brief-*/x-post.zh.md
```

### Content Pack Fields

| File | Purpose |
|------|---------|
| `manifest.json` | Pack metadata (id, score, tags, recommended assets) |
| `source.json` | Source signal references (types, titles, URLs) |
| `signal.json` | Original signal data |
| `brief.md` | Full creative brief — why_it_matters, content_angle, audience |
| `facts.md` | Factual basis with linked sources |
| `x-post.zh.md` | Chinese social post draft, ready to post |
| `image-prompt.md` | Text prompt for image generation |
| `video-prompt.md` | Text prompt for video generation (conditional) |
| `music-prompt.md` | Text prompt for music generation (conditional) |
| `webpage-outline.md` | Webpage structure based on the brief |
| `asset-plan.json` | Full asset plan with priorities and outputs |

---

## How to Reuse Prompts

Prompts in `content-packs/*/image-prompt.md` are **prompt-engineering artifacts** — they encode the creative angle, target audience, and factual basis from real signals. Use them directly as input to:

- **Image:** Midjourney, DALL-E, Stable Diffusion, Flux
- **Video:** Kling, Runway, Sora
- **Music:** Suno, Udio
- **Text:** Claude, GPT, MiniMax

No attribution required for using prompts alone (see License below).

---

## Metadata Indexes

| File | What it contains |
|------|-----------------|
| `metadata/asset-index.json` | All content packs, sorted by score |
| `metadata/source-index.json` | Content packs grouped by source type |
| `metadata/daily-index.json` | Content packs grouped by export date |
| `gallery/assets.json` | Gallery-specific subset (used by `gallery/index.html`) |

---

## License

| Content | License | Commercial use |
|---------|---------|----------------|
| Source code / metadata JSON | **MIT** | ✅ Yes |
| Prompts + briefs (text content) | **CC-BY 4.0** | ✅ Yes, with attribution |
| Generated media (images/music/video) | **CC-BY-NC 4.0** | ❌ Non-commercial only |
| Assets metadata | **CC01.0** | ✅ Yes, public domain |

See [LICENSE](./LICENSE) and [LICENSE-ASSETS](./LICENSE-ASSETS) for details.

---

## What This Repo Is NOT

- **Not a build artifact** — independently useful without the harvester
- **Not dependent on the harvester** — content packs can be consumed standalone
- **No real generated media yet** — Phase 2B contains prompts only; media generation is Phase 3A

---

## Related

- [creative-quota-harvester](https://github.com/conanxin/creative-quota-harvester) — Program that produces these assets
- [Harvester Roadmap](https://github.com/conanxin/creative-quota-harvester/blob/main/ROADMAP.md) — Full project roadmap
- [Assets Gallery](https://conanxin.github.io/creative-quota-assets/gallery/) — Live gallery (GitHub Pages)
