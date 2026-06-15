# Publishing Shortlists — Creative Quota Assets

**Phase:** 6C (Publishing Readiness Review & Deduped Shortlist)  
**Generated:** 2026-06-15T20:55:00+08:00  
**Mode:** read-only shortlist artefacts for human review

---

## Purpose

This directory holds the **Phase 6C deduped shortlists** — the result of reviewing Phase 6B's publishing pack and applying a 7-rule dedup policy (see harvester's `dashboard/publishing-readiness-policy.json`).

These shortlists exist to:
1. **Fix the topic-flooding risk** in Phase 6B (top 5 priority were all the same topic).
2. **Maximize topic diversity** in the first publish round (5/5 unique topics in each shortlist).
3. **Preserve the no-platform-publish boundary** — all items here are for human review, not auto-publish.
4. **Mirror shortlist state from the harvester repo** so assets repo and harvester repo stay in sync.

---

## Files

| File | Items | Purpose |
|------|-------|---------|
| `x-ready-shortlist.json` | 5 | First-round X posts (one per topic) — has post text + image, ready for human review |
| `blog-shortlist.json` | 5 | First-round blog drafts (one per topic) — outlines ready, body needs human writing |
| `image-generation-candidates.json` | 5 | Topics that still need an image before X-publishing (one per topic) — **model NOT called in Phase 6C** |
| `README.md` | — | This file |

---

## Topic Coverage (5/5 unique topics, 5/5 unique source types)

| # | Topic | Source type | In X | In Blog | In Image-gen |
|---|-------|-------------|------|---------|--------------|
| 1 | Flaws in the LLM Automation Narrative | academic | ✅ | ✅ | ✅ |
| 2 | stabilityai/stable-video-diffusion-img2vid-xt | ai-ecosystem | ✅ | ✅ | ✅ |
| 3 | SamurAIGPT/Generative-Media-Skills | code | ✅ | ✅ | ✅ |
| 4 | River AI | dev-community | ✅ | ✅ | ✅ |
| 5 | The Penitence of Saint Jerome | culture-art | ✅ | ✅ | ✅ |

---

## What Phase 6C did to these files

- Created the 3 shortlist JSON files and this README.
- **Did NOT modify** any `x-post.zh.md` or `blog/drafts/*.md` body. All `post_text` and `one_sentence_summary` fields are verbatim copies.
- **Did NOT generate** any image. All `image_url` fields are verbatim copies of Phase 6B's `linked_image_url`.
- **Did NOT call** any model. `image-generation-candidates.json` items all have `model_call_status: not_called`.

## What Phase 6C did NOT do

- Did NOT publish to X / Twitter / any platform.
- Did NOT call X API.
- Did NOT call any image / video / music / LLM model.
- Did NOT send Telegram digest.
- Did NOT start any timer or cron.
- Did NOT modify systemd, gateway, or .env files.

---

## How to use (human review only)

1. Open `x-ready-shortlist.json` — review each of the 5 items.
2. For each item, decide: **approve** / **edit** / **reject**.
3. If approved, post manually via baoyu-post-to-x or direct Twitter UI.
4. If rejected, mark in a future review JSON; do not auto-substitute.
5. Image generation is a separate, human-approved, separately-budgeted future phase.

---

## Source references

- Harvester repo: `~/.openclaw/workspace/projects/creative-quota-harvester/`
- Assets repo: `~/.openclaw/workspace/projects/creative-quota-assets/`
- Policy: `harvester/dashboard/publishing-readiness-policy.json`
- Full review: `harvester/dashboard/publishing-readiness-review.json`
- Consolidated shortlist: `harvester/dashboard/deduped-publishing-shortlist.json`
- Markdown reports: `harvester/reports/publishing-readiness-review.md` and `harvester/reports/deduped-publishing-shortlist.md`
- Validator: `harvester/scripts/validate-publishing-readiness.ts` (run via `npm run validate:publishing-readiness` in harvester)

---

_辛 🔮 — Phase 6C shortlists complete. No publish, no model call, no media generation, no timer. Review-ready._
