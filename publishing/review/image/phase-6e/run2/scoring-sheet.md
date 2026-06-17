# Run 2 Human Image Scoring Sheet — Phase 6E-K2

**Phase:** 6E-K2 · Run 2 Human Image Scoring Sheet (Completed)
**Generated:** 2026-06-17T06:46:00+08:00
**Updated:** 2026-06-17T08:41:00+08:00
**Based on:** Phase 6E-J Run 2 Controlled Image Generation
**Assets commit:** `a1230a7` · **Harvester commit:** `79c5271`
**Mode:** READ-ONLY scoring record. Scores recorded by 爸爸.

---

## Scoring Dimensions

| Dimension | Weight | Description |
|-----------|--------|-------------|
| `prompt_alignment` | 25% | How well does the image realize the prompt? |
| `visual_quality` | 25% | Sharpness, lighting, color harmony, no artifacts |
| `usefulness_as_asset` | 20% | Works for gallery / blog / X post? |
| `factual_safety` | 15% | No fake logos, citations, or real people |
| `brand_text_artifact_risk` | 15% | Lower = safer (10 = severe risk) |

**Overall (0–100):**
```
(prompt_alignment × 0.25 + visual_quality × 0.25 + usefulness × 0.20
 + factual_safety × 0.15 + (10 − brand_text_artifact_risk) × 0.15) × 10
```

---

## Decision Thresholds

| Decision | Condition |
|----------|-----------|
| ✅ **approve** | overall ≥ 80 AND factual ≥ 8 AND risk ≤ 4 |
| 🔄 **needs_regen** | overall 60–79 OR factual 5–7 OR risk 5–7 |
| ❌ **reject** | overall < 60 OR factual < 5 OR risk ≥ 8 |

> Human override note: 爸爸's decision is authoritative. needs_regen may be selected even when formula suggests reject; recorded as-is.

---

## Image 1 — Q-6E-B-003: River AI

**Path:** `images/2026/06/16/cqa-2026-06-16-run2-001_001.jpg`
**URL:** https://conanxin.github.io/creative-quota-assets/images/2026/06/16/cqa-2026-06-16-run2-001_001.jpg
**Aspect:** 1:1 · 1024×1024 px · 137,300 bytes
**Source:** dev-community · **Risk:** low · **Model:** image-01

**Prompt:** A developer community discussion poster. topic "River AI" as a short hook at the top in rounded sans-serif. central visual: a stylized developer workspace with three monitors showing code, terminal, and chat. bottom one-liner summarizing the pain point in italics. style: editorial flat illustration, pastel pink and slate, soft shadows, minimal. no faces, no company logos

### Scores (recorded)

| Dimension | Score |
|-----------|-------|
| prompt_alignment | 5.5/10 |
| visual_quality | 5.5/10 |
| usefulness_as_asset | 4.5/10 |
| factual_safety | 4.0/10 |
| brand_text_artifact_risk | 8.0/10 |
| **Overall** | **45.5/100** |

**Score breakdown:** `0.25·5.5 + 0.25·5.5 + 0.20·4.5 + 0.15·4.0 + 0.15·(10−8.0) = 1.375 + 1.375 + 0.9 + 0.6 + 0.3 = 4.55; overall = 4.55 × 10 = 45.5`

**Decision:** 🔄 `needs_regen`
**Reason:** Severe text artifacts in title area ("Develoesin UncerPto"), fake footer/logo text, weak River AI semantic clarity.
**Notes:** Regenerate with minimal or no text, no fake logos, cleaner personal-AI/developer-workflow visual.

---

## Image 2 — Q-6E-B-004: stabilityai/stable-video-diffusion-img2vid-xt

**Path:** `images/2026/06/16/cqa-2026-06-16-run2-002_001.jpg`
**URL:** https://conanxin.github.io/creative-quota-assets/images/2026/06/16/cqa-2026-06-16-run2-002_001.jpg
**Aspect:** 16:9 · 1280×720 px · 64,917 bytes
**Source:** ai-ecosystem · **Risk:** low · **Model:** image-01

**Prompt:** A polished AI model card visual. model name "stabilityai/stable-video-diffusion-img2vid-xt" shown as a large hero badge. central pipeline flow: input (icon) → model block with subtle inner layers → output (icon). task label "image-to-video" near the input. two or three monospaced metric tiles on the right: downloads, likes, library. style: Hugging Face inspired, dark slate background, amber-to-magenta gradient, soft glow. no human faces, no company logos

### Scores (recorded)

| Dimension | Score |
|-----------|-------|
| prompt_alignment | 6.0/10 |
| visual_quality | 5.0/10 |
| usefulness_as_asset | 4.5/10 |
| factual_safety | 5.5/10 |
| brand_text_artifact_risk | 6.5/10 |
| **Overall** | **50.0/100** |

**Score breakdown:** `0.25·6.0 + 0.25·5.0 + 0.20·4.5 + 0.15·5.5 + 0.15·(10−6.5) = 1.5 + 1.25 + 0.9 + 0.825 + 0.525 = 5.0; overall = 5.0 × 10 = 50.0`

**Decision:** 🔄 `needs_regen`
**Reason:** Reasonable abstract video-diffusion pipeline direction, but scene too dark, main subject too small, most labels unreadable pseudo-text.
**Notes:** Regenerate with clearer video generation pipeline visual, stronger central composition, minimal readable labels, no fake UI metrics.

---

## Summary

| Metric | Value |
|--------|-------|
| Approved | 0 |
| Needs regen | 2 |
| Rejected | 0 |
| Pending | 0 |
| **Run 2 outcome** | **needs_regen_all** |
| Auto-regen executed | No |
| Run 1 status | closed (unchanged) |
| Run 3 status | pending (unchanged) |
| total_generated_image_files | 10 |
| pending_images | 16 |

**Next:** Choose next phase — Phase 6E-M (Controlled Regeneration) or Idle. Both Run 2 images marked needs_regen; no regeneration executed in 6E-K2.