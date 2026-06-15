# Publishing Pack — Creative Quota Assets

**Phase:** 6B (X / Blog Publishing Pack)  
**Generated:** 2026-06-15T09:18:44.445Z  
**no_platform_publish:** true

---

## Overview

This directory contains **ready-to-publish drafts** for X and blog platforms.
All items are `draft_ready` and require **human review** before any external posting.

**Important:**
- No items have been auto-published.
- No X API has been called.
- All X post text is **verbatim** from the content pack's `x-post.zh.md`.
- All blog drafts are skeletons built from existing `webpage-outline.md` and `content-summary.zh.md`.

## Directory Structure

```
publishing/
├── README.md           (this file)
├── x/
│   ├── README.md       (X pack documentation)
│   ├── index.json      (X post index)
│   └── posts/          (25 X post markdown files)
└── blog/
    ├── README.md       (Blog pack documentation)
    ├── index.json      (Blog draft index)
    └── drafts/         (25 blog draft skeletons)
```

## Status

| Metric | Value |
|--------|-------|
| Total X posts | 25 |
| X posts ready (post + image) | 5 |
| X posts needs asset | 20 |
| Total blog drafts | 25 |
| Blog drafts draft_ready | 15 |
| Blog drafts outline_only | 0 |

## How to Use

1. **Human review** — Read through `x/posts/*.md` and `blog/drafts/*.md`.
2. **Manual posting** — Use existing tools (baoyu-post-to-x, etc.) to post manually.
3. **No automation** — Do not set up timers or cron jobs for posting.
4. **Track outcomes** — When manually posted, update `no_platform_publish` in any validator JSON if needed.

## Boundaries

- ❌ No X API calls
- ❌ No platform auto-publish
- ❌ No model calls (drafts built from existing text only)
- ❌ No media generation
- ✅ Human review required before any post
- ✅ All text is verbatim from existing content packs

