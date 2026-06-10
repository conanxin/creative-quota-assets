# Creative Quota Assets

**Open source AI generation asset library — prompts, briefs, and metadata for creative AI workflows.**

> Powered by [creative-quota-harvester](https://github.com/conanxin/creative-quota-harvester). Assets are sourced from real-world signals (academic papers, open source projects, cultural collections) and transformed into reusable generation prompts.

---

## Project Status

| Phase | Status | Description |
|-------|--------|-------------|
| Phase 0A | ✅ Complete | Mock pipeline, dry-run |
| Phase 1 | ✅ Complete | Real signal collection, SQLite storage |
| Phase 1R | ✅ Complete | Source reliability + fallback chains |
| Phase 2A | ✅ Complete | Signal → Creative Brief → Content Pack |
| **Phase 2B** | **✅ Complete** | **Asset gallery polish + open source prep** |
| Phase 2C | ⬜ Next | GitHub open-source publish prep |
| Phase 3A | ⬜ Planned | MiniMax quota-aware generation |
| Phase 3B | ⬜ Planned | Telegram daily report |
| Phase 4 | ⬜ Planned | Scheduled automation |

**Current note:** Phase 2B is complete. This repo contains prompt/metadata assets only — no real generated images, music, or video yet. MiniMax generation is Phase 3A.

---

## Project Structure

```
creative-quota-assets/
├── content-packs/           ← Self-contained brief + prompt bundles
│   └── YYYY/MM/YYYY-MM-DD/  ← Date-organized content packs
│       ├── index.json       ← Batch manifest
│       └── brief-*/ ← One pack per creative brief
│           ├── manifest.json     # Pack metadata
│           ├── source.json # Source signal references
│           ├── signal.json       # Original signal data
│           ├── brief.md          # Creative brief (human readable)
│           ├── facts.md          # Factual basis + source links
│           ├── x-post.zh.md      # Chinese X (Twitter) post draft
│           ├── image-prompt.md # Image generation prompt
│           ├── video-prompt.md   # Video generation prompt
│           ├── music-prompt.md   # Music generation prompt
│           ├── webpage-outline.md
│           └── asset-plan.json   # Full asset plan
├── gallery/
│   ├── index.html           ← Web gallery (static HTML/JS, no build)
│   └── assets.json          ← Gallery asset index
├── metadata/
│   ├── asset-index.json     # All assets master index
│   ├── source-index.json # Assets grouped by source type
│   └── daily-index.json     # Assets grouped by date
├── images/                  # Generated images (Phase 3A+)
├── music/                   # Generated music (Phase 3A+)
├── videos/                  # Generated video (Phase 3A+)
└── prompts/                 # Standalone prompt files
```

---

## Content Pack Format

Each `content-pack/` is a **self-contained directory** — no build step, no database. Open `brief.md` for the full creative brief, or use individual prompt files directly in your generation pipeline.

### Minimal Example

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
| `image-prompt.md` | Text prompt for image generation (e.g. Midjourney, DALL-E) |
| `video-prompt.md` | Text prompt for video generation |
| `music-prompt.md` | Text prompt for music generation |
| `webpage-outline.md` | Webpage structure based on the brief |
| `asset-plan.json` | Full asset plan with priorities and outputs |

---

## How to Browse the Gallery

**Open in browser:** `gallery/index.html`

- Pure static HTML + CSS + JS — no build step, no server required
- Reads `gallery/assets.json` directly in-browser
- Filter by source type, tags, or date
- Click through to content pack files

**Via GitHub Pages (after publish):**
```
https://conanxin.github.io/creative-quota-assets/gallery/
```

---

## How to Reuse Prompts

Prompts in `content-packs/*/image-prompt.md` are **prompt-engineering artifacts** — they encode the creative angle, target audience, and factual basis from real signals. Use them directly as input to:

- Image: Midjourney, DALL-E, Stable Diffusion, Flux
- Video: Kling, Runway, Sora
- Music: Suno, Udio
- Text: Claude, GPT, MiniMax

No attribution required for using prompts alone (see License below).

---

## Metadata

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

- **Not a build artifact** — it is a publication target, independently useful
- **Not dependent on the harvester** — content packs can be consumed standalone
- **No real generated media yet** — Phase 2B contains prompts only; media generation is Phase 3A

---

## Related

- [creative-quota-harvester](https://github.com/conanxin/creative-quota-harvester) — Program that produces these assets
- [creative-quota-harvester/docs/ROADMAP.md](https://github.com/conanxin/creative-quota-harvester/blob/main/docs/ROADMAP.md) — Full project roadmap