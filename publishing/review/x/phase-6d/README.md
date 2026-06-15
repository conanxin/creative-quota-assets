# X Human Review Pack — Phase 6D

**Phase:** 6D (X Shortlist Human Review Pack)  
**Generated:** 2026-06-15T21:15:00+08:00  
**Based on:** Phase 6C X ready shortlist  
**Mode:** READ-ONLY review artefacts for human review

---

## Purpose

This directory contains the **Phase 6D human review pack** for the 5 X posts in Phase 6C's X ready shortlist. The pack is:

- **Read-only** — no automatic publishing.
- **Copy-ready** — each post's text is preserved verbatim from Phase 6C, ready for the human to copy into the X UI.
- **Checklist-driven** — every post has a manual review checklist (factual / tone / image / link / sensitive leak / final approval).
- **Boundary-enforced** — no X API call, no baoyu-post-to-x call, no model call, no media generation, no timer.

---

## Directory Structure

```
publishing/review/x/phase-6d/
├── README.md                       (this file)
├── index.json                      (5-item review pack index)
└── posts/
    ├── flaws-in-the-llm-automation-narrative.md
    ├── stabilityai-stable-video-diffusion-img2vid-xt.md
    ├── samuraigpt-generative-media-skills.md
    ├── river-ai.md
    └── the-penitence-of-saint-jerome.md
```

## Review Items (5/5 unique topics, 5/5 unique source types)

| # | Topic | source_type | id | quality | risk |
|---|-------|-------------|-----|---------|------|
| 1 | Flaws in the LLM Automation Narrative | academic | `Q-6B-X-...-mq8c6kp5-u-flaws-i` | 96 | low |
| 2 | stabilityai/stable-video-diffusion-img2vid-xt | ai-ecosystem | `Q-6B-X-...-mq8c663q-4-stabili` | 94 | low |
| 3 | SamurAIGPT/Generative-Media-Skills | code | `Q-6B-X-...-mq8c6kp4-7-samurai` | 97 | low |
| 4 | River AI | dev-community | `Q-6B-X-...-mq8c663q-v-river-a` | 97 | **medium** (founder-attributed) |
| 5 | The Penitence of Saint Jerome | culture-art | `Q-6B-X-...-mq8c6kp5-r-the-pen` | 96 | **medium** (public-domain artwork) |

All 5:
- `review_status: ready_for_human_review`
- `publish_status: not_published`
- `no_platform_publish: true`
- Have `image_url`, `gallery_url`, `review_url`, `linked_content_pack`

---

## How to Use (Human Review Workflow)

For each of the 5 items:

### Step 1: Open the post's review markdown
Open `posts/<topic-slug>.md` in a markdown viewer.

### Step 2: Read the post text
Confirm the post text is acceptable as-is.

### Step 3: Walk through the manual review checklist
The post markdown has 6 checklist sections:
1. **Factual check** — verify the topic, attribution, hashtags.
2. **Tone check** — confirm the Chinese + English mix is acceptable.
3. **Image relevance check** — confirm the image is appropriate.
4. **Link check** — verify the linked_content_pack URL.
5. **No sensitive leak check** — verify no PII, no proprietary data.
6. **Final human approval** — sign off with name, date, decision (APPROVE / EDIT / REJECT).

### Step 4: For approved posts
1. Open X (twitter.com) in browser.
2. Click "Post" to open the new post composer.
3. Paste the X Post Text block from the post markdown (exactly as shown).
4. Upload the image from `image_url` (download first if needed).
5. Review the preview, then click "Post".
6. **Do NOT call baoyu-post-to-x. Do NOT call X API. Do NOT auto-publish.**

### Step 5: For edited posts
- Save a new file with `-edited.md` suffix.
- Note the change in the human review log.
- Do NOT overwrite the original.

### Step 6: For rejected posts
- Mark in a future review JSON (Phase 6E or later).
- Do NOT auto-substitute with another post.

---

## Boundaries (enforced by Phase 6D)

- ❌ No X API call
- ❌ No baoyu-post-to-x call
- ❌ No model call (LLM, image, video, music)
- ❌ No media generation
- ❌ No collect:* / generate:* / digest:send:* / report:send:*
- ❌ No timer / cron
- ❌ No systemd / gateway modification
- ❌ No commit of .env / .env.telegram.local / .control.local / control-action-audit.jsonl
- ❌ No token print
- ✅ Human review required before any post
- ✅ OpenClaw final reply = 1 sentence

---

## Source References

- Phase 6C shortlist (harvester): `~/.openclaw/workspace/projects/creative-quota-harvester/dashboard/deduped-publishing-shortlist.json`
- Phase 6C shortlist (assets): `~/.openclaw/workspace/projects/creative-quota-assets/publishing/shortlists/x-ready-shortlist.json`
- Phase 6B index (assets): `~/.openclaw/workspace/projects/creative-quota-assets/publishing/x/index.json`
- Phase 6C review (harvester): `~/.openclaw/workspace/projects/creative-quota-harvester/dashboard/publishing-readiness-review.json`
- Phase 6C commits: Harvester `44a0af8` / Assets `9c153aa`

---

## Status Fields

| Field | Value |
|-------|-------|
| total_review_items | 5 |
| reviewed | 0 |
| approved_for_manual_publish | 0 |
| published_externally | 0 |
| no_platform_publish | true |

(After human review and posting, `reviewed`, `approved_for_manual_publish`, and `published_externally` will be updated in a future phase. Phase 6D does NOT update these.)

---

_辛 🔮 — Phase 6D review pack complete. Copy-ready, human-review required, no auto-publish._
