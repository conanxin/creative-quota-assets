# Run 2 Human Image Review Pack — Phase 6E-K

**Phase:** 6E-K · Run 2 Human Image Review Pack
**Generated:** 2026-06-17T06:46:00+08:00
**Based on:** Phase 6E-J Run 2 Controlled Image Generation
**Assets commit:** `b03580e` · **Harvester commit:** `52a69d6`
**Mode:** READ-ONLY review artefacts. No model call, no media generation.

---

## Purpose

This directory contains the **Phase 6E-K Run 2 human image review pack** for the 2 images generated in Phase 6E-J Run 2. The pack is:

- **Read-only** — no model call, no media generation.
- **No auto-decision** — every `decision` starts as `pending` and must be filled by 爸爸.
- **No side effects** — no X publish, no timer, no digest, no promote, no C5N.
- **No 6D-5 modification** — `x-manual-post-log.json` `final_status="closed"` is preserved.
- **No Run 1 re-open** — Run 1 final closeout (`approved_after_regen`, `usable_images=2/2`) is preserved.
- **No Run 3 approval** — Run 3 (Q-6E-B-005 Penitence) remains `pending`.
- **No Run 2 image overwrite** — the 2 generated images are not touched.

---

## Directory Structure

```
publishing/review/image/phase-6e/run2/
├── README.md           (this file)
├── review-board.json   (2-item review board; machine-readable)
├── review-board.md     (human-readable review board)
├── scoring-sheet.json  (5-dimension scoring sheet; machine-readable)
└── scoring-sheet.md    (human-readable scoring sheet)
```

---

## What this pack contains

### 1. `review-board.json` / `review-board.md`

The 2 Run 2 images with their current review state:

| # | item_id | asset_id | title | source_type | review_status | decision |
|---|---------|----------|-------|-------------|---------------|----------|
| 1 | `Q-6E-B-003` | `cqa-2026-06-16-run2-001` | River AI | dev-community | pending_human_review | pending |
| 2 | `Q-6E-B-004` | `cqa-2026-06-16-run2-002` | stabilityai/stable-video-diffusion-img2vid-xt | ai-ecosystem | pending_human_review | pending |

### 2. `scoring-sheet.json` / `scoring-sheet.md`

5 scoring dimensions per image (see scoring-sheet for weights):

1. `prompt_alignment` (0–10) — how well the image matches the prompt
2. `visual_quality` (0–10) — sharpness, lighting, no artifacts
3. `usefulness_as_asset` (0–10) — works for gallery / blog / X
4. `factual_safety` (0–10) — no fake citations, fake names, hallucinated logos
5. `brand_text_artifact_risk` (0–10, lower is better) — garbled text, fake brand confusion

**Overall score (0–100):** weighted combination (25/25/20/15/15%, with risk reversed).

**Decision (3 options):** `approve` / `needs_regen` / `reject`.

---

## Run Status Snapshot

| Run | Status | Detail |
|-----|--------|--------|
| Run 1 | closed | `final_status=closed`, `outcome=approved_after_regen`, `usable_images=2/2` |
| Run 2 | pending_human_review | 2 of 2 generated, awaiting scores + decisions |
| Run 3 | pending | `Q-6E-B-005 Penitence` — NOT approved, NOT triggered |

`total_generated_image_files=10` · `pending_images=16`.

---

## Next Phase (NOT auto-triggered)

| Outcome | Next Phase |
|---------|-----------|
| Both approved | Phase 6E-L: Run 2 Final Closeout → Run 2 frozen, cumulative updated, pending decremented |
| Any needs_regen | Phase 6E-K-regen: Run 2 Regeneration (separate human command) |
| Any rejected | Phase 6E-L-rejected: Run 2 Rejection Record |
| Idle | Wait for Run 3 (Penitence) decision |

**Requires explicit human command to proceed.**