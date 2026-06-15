# Manual Post Log Entry Template

**Use this template to record one manual X post.**

---

## Item Reference

- **item_id:** `<paste from approved/posts/<slug>.md frontmatter>`
- **title:** `<paste from approved/posts/<slug>.md frontmatter>`
- **topic_slug:** `<paste from approved/posts/<slug>.md frontmatter>`
- **source_type:** `<academic | ai-ecosystem | code | dev-community | culture-art>`
- **risk_level:** `<low | medium>`

---

## Manual Post Record

- **x_post_url:** `<full URL of the manually-posted tweet, e.g. https://x.com/yourhandle/status/1234567890>`
- **posted_at:** `<ISO 8601 timestamp, e.g. 2026-06-15T23:30:00+08:00>`
- **posted_by:** `<human account handle, e.g. @yourhandle>`
- **notes:** `<optional human note, e.g. "Posted via X web UI, no edits.">`

---

## State Transition

After recording, the item should be updated to:

- `manual_post_status: posted_manually`
- `posted_manually: true`
- `publish_status: posted_manually` (or stay `not_published` per system policy)
- `x_post_url: <URL>`
- `posted_at: <ISO timestamp>`
- `posted_by: <handle>`
- `notes: <note>`

---

## DO NOT

- ❌ Do NOT call X API to verify the post
- ❌ Do NOT call baoyu-post-to-x
- ❌ Do NOT mark `posted_manually=true` unless you actually posted manually
- ❌ Do NOT mark `x_post_url` with a placeholder or fake URL
- ❌ Do NOT mark `posted_at` with a future timestamp

---

## Notes on Phase Boundary

This template is for **Phase 6D-4B** (Record Manual X Post URLs) — only used after the human has manually posted via X UI and provided real post URLs.

Phase 6D-4A created the **scaffold** for this template. The 5 approved items have NOT been posted yet, so all entries currently have `x_post_url=null`, `posted_at=null`, `posted_by=null`.

---

_辛 🔮 — Template for Phase 6D-4B manual post log entry._
