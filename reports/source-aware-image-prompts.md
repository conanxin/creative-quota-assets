# Source-Aware Image Prompts — Enhancement Report

**Phase:** 4G
**Generated:** 2026-06-11
**Packs:** 25/25
**Strategy:** Rule-based, 0 LLM calls

---

## Strategy Summary

| Source Type | Visual Goal | Style | Aspect | Guidance |
|-------------|-------------|-------|--------|----------|
| code | Repository cover + agent workflow | Tech editorial, isometric | 16:9 | 7.5 |
| academic | Paper concept diagram | Academic poster, Tufte | 4:3 | 6.5 |
| ai-ecosystem | Model card hero + pipeline | HF-inspired, amber-magenta | 16:9 | 7.0 |
| dev-community | Developer pain point poster | Editorial flat, pastel | 1:1 | 6.5 |
| culture-art | Museum lighting + art reinterpretation | Classical, warm wood | 4:5 | 7.5 |
| context | Mood board | Soft pastel, paper texture | 3:4 | 6.0 |

---

## Per-Pack Output Files

Each content pack now has:
- `image-prompt.enriched.md` — Chinese intent + English prompt + negative + params + strategy metadata
- `image-prompt.zh.md` — Human-readable Chinese explanation
- `image-prompt.meta.json` — Machine-readable metadata with strategy, style_tags, visual_subjects

---

## Validation

```
508/508 checks passed
25/25 enriched.md
25/25 zh.md
25/25 meta.json
```

---

## Example Prompts

### code (SamurAIGPT/Generative-Media-Skills)
> A modern GitHub repository cover banner for an open-source AI toolkit. repository name "SamurAIGPT/Generative-Media-Skills" displayed as the central hero title. isometric 3/4 perspective developer workspace with floating capability tiles...

### academic (Flaws in the LLM Automation Narrative)
> An academic poster for a research paper. paper title "Flaws in the LLM Automation Narrative" in elegant serif at the top. central conceptual diagram: abstract geometric shapes forming a flow, suggesting research methodology...

### ai-ecosystem (stabilityai/stable-video-diffusion-img2vid-xt)
> A polished AI model card visual. model name "stabilityai/stable-video-diffusion-img2vid-xt" shown as a large hero badge. central pipeline flow: input (icon) → model block with subtle inner layers → output (icon)...

### dev-community (River AI)
> A developer community discussion poster. topic "River AI" as a short hook at the top in rounded sans-serif. central visual: a stylized developer workspace with three monitors showing code, terminal, and chat...

### culture-art (The Penitence of Saint Jerome)
> A museum-style photograph of a classical artwork reinterpretation. subject: "The Penitence of Saint Jerome" by Joachim Patinir. period: ca. 1515. medium hint: Oil on wood. museum lighting: warm spotlight from the upper-left...

---

## Gallery Badge

Gallery now shows "✨ Enhanced Prompt" badge on all 5 unique topic cards.

Detail pages show enhanced prompt card with collapsible English Prompt / Negative Prompt sections, plus links to enriched.md, zh.md, and meta.json.

---

## Files

- `image-prompt.enriched.md` — 25 files
- `image-prompt.zh.md` — 25 files
- `image-prompt.meta.json` — 25 files
- `index.html` (updated) — 25 files
- `gallery/index.html` (updated)