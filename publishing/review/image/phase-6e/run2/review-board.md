# Run 2 Human Image Review Board — Phase 6E-K

**Phase:** 6E-K · Run 2 Human Image Review Pack
**Generated:** 2026-06-17T06:46:00+08:00
**Based on:** Phase 6E-J Run 2 Controlled Image Generation
**Assets commit:** `b03580e` · **Harvester commit:** `52a69d6`
**Mode:** READ-ONLY review artefacts. No model call, no media generation.
**Run 1 status:** `final_status=closed`, `outcome=approved_after_regen`, `usable_images=2/2` — NOT modified.
**Run 3 status:** `pending` — NOT approved.

---

## Run 2 Images — Pending Human Review

| # | item_id | title | source_type | risk | aspect | decision |
|---|---------|-------|-------------|------|--------|----------|
| 1 | `Q-6E-B-003` | River AI | dev-community | low | 1:1 | ⏳ pending |
| 2 | `Q-6E-B-004` | stabilityai/stable-video-diffusion-img2vid-xt | ai-ecosystem | low | 16:9 | ⏳ pending |

---

## Image 1 — Q-6E-B-003: River AI

**Path:** `images/2026/06/16/cqa-2026-06-16-run2-001_001.jpg`
**URL:** https://conanxin.github.io/creative-quota-assets/images/2026/06/16/cqa-2026-06-16-run2-001_001.jpg
**Dimensions:** 1024×1024 px | **Size:** 137,300 bytes | **Aspect:** 1:1
**Model:** image-01 | **Watermark:** ✅ | **AIGC watermark:** ✅
**Prompt hash:** `713fa2351907` | **Output hash:** `0fa9609b9aff`
**Generated:** 2026-06-16T20:59:22+08:00
**Review status:** `pending_human_review` | **Human score:** `null`
**Decision:** ⏳ pending

**Prompt:**
> A developer community discussion poster. topic "River AI" as a short hook at the top in rounded sans-serif. central visual: a stylized developer workspace with three monitors showing code, terminal, and chat. bottom one-liner summarizing the pain point in italics. style: editorial flat illustration, pastel pink and slate, soft shadows, minimal. no faces, no company logos

---

## Image 2 — Q-6E-B-004: stabilityai/stable-video-diffusion-img2vid-xt

**Path:** `images/2026/06/16/cqa-2026-06-16-run2-002_001.jpg`
**URL:** https://conanxin.github.io/creative-quota-assets/images/2026/06/16/cqa-2026-06-16-run2-002_001.jpg
**Dimensions:** 1280×720 px | **Size:** 64,917 bytes | **Aspect:** 16:9
**Model:** image-01 | **Watermark:** ✅ | **AIGC watermark:** ✅
**Prompt hash:** `5b76a00ddcb7` | **Output hash:** `200ad2cff498`
**Generated:** 2026-06-16T20:59:41+08:00
**Review status:** `pending_human_review` | **Human score:** `null`
**Decision:** ⏳ pending

**Prompt:**
> A polished AI model card visual. model name "stabilityai/stable-video-diffusion-img2vid-xt" shown as a large hero badge. central pipeline flow: input (icon) → model block with subtle inner layers → output (icon). task label "image-to-video" near the input. two or three monospaced metric tiles on the right: downloads, likes, library. style: Hugging Face inspired, dark slate background, amber-to-magenta gradient, soft glow. no human faces, no company logos

---

## Scoring Dimensions

Each image requires scoring on 5 dimensions (0–10):

| Dimension | Weight | Description |
|-----------|--------|-------------|
| `prompt_alignment` | 25% | How well does the image realize the prompt? |
| `visual_quality` | 25% | Sharpness, lighting, color harmony, no artifacts |
| `usefulness_as_asset` | 20% | Works for gallery / blog / X post? |
| `factual_safety` | 15% | No fake logos, citations, or real people |
| `brand_text_artifact_risk` | 15% | Lower = safer. 10 = severe brand confusion |

**Overall (0–100):** `(prompt×0.25 + visual×0.25 + useful×0.20 + factual×0.15 + (10−risk)×0.15) × 10`

**Decision thresholds:**
- `approve`: overall ≥ 80 AND factual ≥ 8 AND risk ≤ 4
- `needs_regen`: overall 60–79 OR factual 5–7 OR risk 5–7
- `reject`: overall < 60 OR factual < 5 OR risk ≥ 8

---

## Decision Options

| Decision | Meaning |
|----------|---------|
| `approve` | Image is usable. Run 2 closeout can proceed. |
| `needs_regen` | Regenerate this image only. Other images unaffected. |
| `reject` | Image is unusable. Run 2 cannot proceed. |

---

## Next Phase (NOT auto-triggered)

| Outcome | Next Phase |
|---------|-----------|
| Both approved | Phase 6E-L: Run 2 Final Closeout |
| Any needs_regen | Phase 6E-K-regen: Run 2 Regeneration (separate command) |
| Any rejected | Phase 6E-L-rejected: Run 2 Rejection Record |
| Idle | Wait for Run 3 (Penitence) decision |

**Requires explicit human command to proceed.**
