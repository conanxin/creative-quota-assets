# Run 2 Human Image Scoring Sheet — Phase 6E-K

**Phase:** 6E-K · Run 2 Human Image Scoring Sheet
**Generated:** 2026-06-17T06:46:00+08:00
**Based on:** Phase 6E-J Run 2 Controlled Image Generation
**Assets commit:** `b03580e` · **Harvester commit:** `52a69d6`
**Mode:** READ-ONLY scoring template. Scores must be filled by 爸爸.

---

## Scoring Dimensions

| Dimension | Weight | Score to fill | Description |
|-----------|--------|---------------|-------------|
| `prompt_alignment` | 25% | __/10 | How well does the image realize the prompt? |
| `visual_quality` | 25% | __/10 | Sharpness, lighting, color harmony, no artifacts |
| `usefulness_as_asset` | 20% | __/10 | Works for gallery / blog / X post? |
| `factual_safety` | 15% | __/10 | No fake logos, citations, or real people |
| `brand_text_artifact_risk` | 15% | __/10 | Lower = safer (10 = severe risk) |

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

---

## Image 1 — Q-6E-B-003: River AI

**Path:** `images/2026/06/16/cqa-2026-06-16-run2-001_001.jpg`
**URL:** https://conanxin.github.io/creative-quota-assets/images/2026/06/16/cqa-2026-06-16-run2-001_001.jpg
**Aspect:** 1:1 · 1024×1024 px · 137,300 bytes
**Source:** dev-community · **Risk:** low · **Model:** image-01

**Prompt:** A developer community discussion poster. topic "River AI" as a short hook at the top in rounded sans-serif. central visual: a stylized developer workspace with three monitors showing code, terminal, and chat. bottom one-liner summarizing the pain point in italics. style: editorial flat illustration, pastel pink and slate, soft shadows, minimal. no faces, no company logos

### Scores

| Dimension | Score |
|-----------|-------|
| prompt_alignment | __/10 |
| visual_quality | __/10 |
| usefulness_as_asset | __/10 |
| factual_safety | __/10 |
| brand_text_artifact_risk | __/10 |
| **Overall** | **__/100** |

**Decision:** ⏳ pending (`approve` / `needs_regen` / `reject`)
**Notes:** ________________________________________________

---

## Image 2 — Q-6E-B-004: stabilityai/stable-video-diffusion-img2vid-xt

**Path:** `images/2026/06/16/cqa-2026-06-16-run2-002_001.jpg`
**URL:** https://conanxin.github.io/creative-quota-assets/images/2026/06/16/cqa-2026-06-16-run2-002_001.jpg
**Aspect:** 16:9 · 1280×720 px · 64,917 bytes
**Source:** ai-ecosystem · **Risk:** low · **Model:** image-01

**Prompt:** A polished AI model card visual. model name "stabilityai/stable-video-diffusion-img2vid-xt" shown as a large hero badge. central pipeline flow: input (icon) → model block with subtle inner layers → output (icon). task label "image-to-video" near the input. two or three monospaced metric tiles on the right: downloads, likes, library. style: Hugging Face inspired, dark slate background, amber-to-magenta gradient, soft glow. no human faces, no company logos

### Scores

| Dimension | Score |
|-----------|-------|
| prompt_alignment | __/10 |
| visual_quality | __/10 |
| usefulness_as_asset | __/10 |
| factual_safety | __/10 |
| brand_text_artifact_risk | __/10 |
| **Overall** | **__/100** |

**Decision:** ⏳ pending (`approve` / `needs_regen` / `reject`)
**Notes:** ________________________________________________

---

## Summary

| Metric | Value |
|--------|-------|
| Approved | 0 |
| Needs regen | 0 |
| Rejected | 0 |
| Pending | 2 |
| **Run 2 outcome** | **⏳ pending_human_review** |

**Next:** Fill in scores above, then record your decision per image.
