# Blog Publishing Pack

**Phase:** 6B  
**Generated:** 2026-06-15T09:18:44.454Z  
**no_platform_publish:** true

---

## Overview

**25 blog draft skeletons** built from existing content pack materials.
Drafts are `outline_only` or `draft_ready` — no long-form writing was performed.
No blog platform has been published to.

## Files

- `index.json` — machine-readable index of all blog drafts
- `drafts/<slug>.md` — 25 draft markdown files

## Status Summary

| Status | Count |
|--------|-------|
| draft_ready (has webpage-outline + content-summary) | 15 |
| outline_only (no webpage-outline) | 0 |
| blocked | 10 |
| Needs expansion | 10 |

## Source Type Distribution

| Source Type | Count |
|-------------|-------|
| culture-art | 5 |
| dev-community | 5 |
| academic | 5 |
| ai-ecosystem | 5 |
| code | 5 |

## Manual Expansion Workflow

1. Open `index.json` to see all draft IDs and statuses.
2. Read each `drafts/<slug>.md` file.
3. For `draft_ready` drafts, the structure is already in place — add 2-3 paragraphs per section.
4. For `outline_only` drafts, the `webpage-outline.md` is missing — copy from the content pack or use `content-summary.zh.md`.
5. Expand manually using your preferred writing tool.
6. Do not auto-publish to any blog platform.
7. Do not call models to expand — preserve the verbatim facts from the content pack.
