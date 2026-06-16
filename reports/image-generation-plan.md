# Phase 6E-B: Controlled Image Generation Plan

> **Phase**: 6E-B  
> **Mode**: controlled_image_generation_plan (PLAN ONLY, no execution)  
> **Generated at**: 2026-06-16T11:38:00+08:00  
> **Strict boundaries**: no_model_call / no_media_generation / no_telegram / no_timer / no_x_publish / no_promote / no_c5n_change / no_6d5_modify / no_secrets  
> **Based on**: Phase 6E-A preflight (20 pending items → 5 diverse selected)  

---

## 1. 任务目标

基于 6E-A preflight 选出的 5 个 pending image items, 设计一个**人类门控**的 image generation execution plan。

**核心原则**:
- Plan-only — 本阶段不调任何 image model, 不生成任何图片
- 5 个 diverse items (5/5 source_type 覆盖)
- 3 个 execution runs (2+2+1), 全部由人类显式批准
- 4 个人类 gate (batch_1/2/3 + model_spend)
- 全部 run 都需等人类回复 Y/N 才会执行

---

## 2. 5 个 Selected Items (首批 5 张图)

| item_id | pack_id | title | source_type | score | risk | aspect | wm | batch | run | order |
|---------|---------|-------|-------------|-------|------|--------|----|-------|------|-------|
| `Q-6E-B-001` | `brief-brief-mq8swsla-f-samuraigpt-generative-media...` | SamurAIGPT/Generative-Media-Skills | code | 0.7025 | low | 16:9 | ✓ | 1 | 1 | 1 |
| `Q-6E-B-002` | `brief-brief-mq8tbqf4-j-flaws-in-the-llm-automation...` | Flaws in the LLM Automation Narrative | academic | 0.6620 | low | 16:9 | ✓ | 1 | 1 | 2 |
| `Q-6E-B-003` | `brief-brief-mq8swsla-m-river-ai...` | River AI | dev-community | 0.5254 | low | 1:1 | ✓ | 1 | 2 | 1 |
| `Q-6E-B-004` | `brief-brief-mq8tbqf4-s-stabilityai-stable-video-di...` | stabilityai/stable-video-diffusion-img2vid-xt | ai-ecosystem | 0.4762 | low | 16:9 | ✓ | 1 | 2 | 2 |
| `Q-6E-B-005` | `brief-brief-mq8tbqf4-8-the-penitence-of-saint-jero...` | The Penitence of Saint Jerome | culture-art | 0.6000 | medium | 16:9 | ✓ | 1 | 3 | 1 |

**Selection criteria**:
- **rule_1_diversity**: one item per source_type (5/5 covered)
- **rule_2_canonical_primary**: all 5 are canonical_primary in gallery-dedup-index.json
- **rule_3_baseline_match**: each aspect_ratio matches the already-generated baseline (16:9 for 4, 1:1 for dev-community)
- **rule_4_score_priority**: run order respects score (high first)
- **rule_5_risk_ladder**: low-risk (Run 1) → low-risk (Run 2) → medium-risk (Run 3, culture-art)

---

## 3. 5 Items 详细字段

### Q-6E-B-001 — SamurAIGPT/Generative-Media-Skills

- **pack_id**: `brief-brief-mq8swsla-f-samuraigpt-generative-media-skills`
- **title**: SamurAIGPT/Generative-Media-Skills
- **source_type**: code
- **risk_level**: low
- **created_at**: 2026-06-11T01:10:39.550Z
- **pack_date**: 2026-06-11
- **final_score**: 0.7025
- **prompt path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8swsla-f-samuraigpt-generative-media-skills/image-prompt.enriched.md`
- **prompt meta path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8swsla-f-samuraigpt-generative-media-skills/image-prompt.meta.json`
- **facts path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8swsla-f-samuraigpt-generative-media-skills/facts.enriched.md`
- **x_post path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8swsla-f-samuraigpt-generative-media-skills/x-post.zh.md`
- **recommended aspect ratio**: 16:9
- **watermark**: True
- **batch number**: 1
- **run number**: 1
- **run order**: 1
- **facts_complete**: True
- **visual_clarity**: high
- **duplicate_overlap_risk**: medium (canonical primary 1/5, 其他 4 version 共享 asset)
- **strategy**: code → 仓库封面 + 工作流/agent 架构图，强调「开发者一眼看懂能力边界」
- **review_required**: False
- **rationale**: Highest score (0.7025), code/developer-ecosystem, low risk, baseline-quality

### Q-6E-B-002 — Flaws in the LLM Automation Narrative

- **pack_id**: `brief-brief-mq8tbqf4-j-flaws-in-the-llm-automation-narrative`
- **title**: Flaws in the LLM Automation Narrative
- **source_type**: academic
- **risk_level**: low
- **created_at**: 2026-06-11T01:22:16.576Z
- **pack_date**: 2026-06-11
- **final_score**: 0.6620
- **prompt path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-j-flaws-in-the-llm-automation-narrative/image-prompt.enriched.md`
- **prompt meta path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-j-flaws-in-the-llm-automation-narrative/image-prompt.meta.json`
- **facts path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-j-flaws-in-the-llm-automation-narrative/facts.enriched.md`
- **x_post path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-j-flaws-in-the-llm-automation-narrative/x-post.zh.md`
- **recommended aspect ratio**: 16:9
- **watermark**: True
- **batch number**: 1
- **run number**: 1
- **run order**: 2
- **facts_complete**: False
- **visual_clarity**: high
- **duplicate_overlap_risk**: medium (canonical primary 1/5, 其他 4 version 共享 asset)
- **strategy**: academic → 论文概念图/学术信息图，强调「研究方法 + 关键数据 + 论文气质」
- **review_required**: False
- **rationale**: Academic / arxiv concept image, low risk, matches already-generated canary (96 score)

### Q-6E-B-003 — River AI

- **pack_id**: `brief-brief-mq8swsla-m-river-ai`
- **title**: River AI
- **source_type**: dev-community
- **risk_level**: low
- **created_at**: 2026-06-11T01:10:39.550Z
- **pack_date**: 2026-06-11
- **final_score**: 0.5254
- **prompt path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8swsla-m-river-ai/image-prompt.enriched.md`
- **prompt meta path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8swsla-m-river-ai/image-prompt.meta.json`
- **facts path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8swsla-m-river-ai/facts.enriched.md`
- **x_post path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8swsla-m-river-ai/x-post.zh.md`
- **recommended aspect ratio**: 1:1
- **watermark**: True
- **batch number**: 1
- **run number**: 2
- **run order**: 1
- **facts_complete**: False
- **visual_clarity**: high
- **duplicate_overlap_risk**: medium (canonical primary 1/5, 其他 4 version 共享 asset)
- **strategy**: dev-community → 开发者痛点海报 / 讨论信息图，强调「开发者一眼共情」
- **review_required**: False
- **rationale**: dev-community, 1:1 square aspect (dev poster), matches already-generated gen-004 baseline (97 score, 1:1)

### Q-6E-B-004 — stabilityai/stable-video-diffusion-img2vid-xt

- **pack_id**: `brief-brief-mq8tbqf4-s-stabilityai-stable-video-diffusion-img2vid-xt`
- **title**: stabilityai/stable-video-diffusion-img2vid-xt
- **source_type**: ai-ecosystem
- **risk_level**: low
- **created_at**: 2026-06-11T01:22:16.576Z
- **pack_date**: 2026-06-11
- **final_score**: 0.4762
- **prompt path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-s-stabilityai-stable-video-diffusion-img2vid-xt/image-prompt.enriched.md`
- **prompt meta path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-s-stabilityai-stable-video-diffusion-img2vid-xt/image-prompt.meta.json`
- **facts path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-s-stabilityai-stable-video-diffusion-img2vid-xt/facts.enriched.md`
- **x_post path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-s-stabilityai-stable-video-diffusion-img2vid-xt/x-post.zh.md`
- **recommended aspect ratio**: 16:9
- **watermark**: True
- **batch number**: 1
- **run number**: 2
- **run order**: 2
- **facts_complete**: False
- **visual_clarity**: high
- **duplicate_overlap_risk**: medium (canonical primary 1/5, 其他 4 version 共享 asset)
- **strategy**: ai-ecosystem → 模型能力图 / pipeline flow / model card hero，强调「能力输入输出 + 关键指标」
- **review_required**: False
- **rationale**: ai-ecosystem model card hero, matches already-generated gen-005 baseline (95 score)

### Q-6E-B-005 — The Penitence of Saint Jerome

- **pack_id**: `brief-brief-mq8tbqf4-8-the-penitence-of-saint-jerome`
- **title**: The Penitence of Saint Jerome
- **source_type**: culture-art
- **risk_level**: medium
- **created_at**: 2026-06-11T01:22:16.576Z
- **pack_date**: 2026-06-11
- **final_score**: 0.6000
- **prompt path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-8-the-penitence-of-saint-jerome/image-prompt.enriched.md`
- **prompt meta path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-8-the-penitence-of-saint-jerome/image-prompt.meta.json`
- **facts path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-8-the-penitence-of-saint-jerome/facts.enriched.md`
- **x_post path**: `creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8tbqf4-8-the-penitence-of-saint-jerome/x-post.zh.md`
- **recommended aspect ratio**: 16:9
- **watermark**: True
- **batch number**: 1
- **run number**: 3
- **run order**: 1
- **facts_complete**: True
- **visual_clarity**: high
- **duplicate_overlap_risk**: medium (canonical primary 1/5, 其他 4 version 共享 asset)
- **strategy**: culture-art → 艺术启发的视觉 / 博物馆灯光 / 风格重绎，强调「原作气质的当代重绎」
- **review_required**: True
- **rationale**: culture-art / classical painting re-interpretation, medium risk (human review required), matches already-generated gen-003 baseline (96 score)

---

## 4. Run Schedule (3 Runs, 5 Images)

### Run 1 — run_6eb_1

- **Description**: First execution run — 2 low-risk items, highest score (code + academic)
- **Items**: Q-6E-B-001, Q-6E-B-002
- **Estimated images**: 2
- **Budget tier**: tier_1_minimal
- **Human gate**: approve_batch_1
- **Estimated wall-clock**: ~8 min
- **Preconditions**:
  - approve_batch_1 from 爸爸
  - image model spend cap configured
  - asset_id pattern validated
- **Expected outputs**:
  - images/2026/06/<asset_id>_001.jpg (2 files)
  - metadata/generated-assets.json (appended)
  - dashboard/asset-quality-scores.json (after 3E review)

### Run 2 — run_6eb_2

- **Description**: Second execution run — 2 low-risk items (dev-community 1:1 + ai-ecosystem 16:9)
- **Items**: Q-6E-B-003, Q-6E-B-004
- **Estimated images**: 2
- **Budget tier**: tier_1_minimal
- **Human gate**: approve_batch_2
- **Estimated wall-clock**: ~8 min
- **Preconditions**:
  - approve_batch_2 from 爸爸
  - Run 1 quality review complete (avg score >= 90)
- **Expected outputs**:
  - images/2026/06/<asset_id>_001.jpg (2 files)
  - metadata/generated-assets.json (appended)

### Run 3 — run_6eb_3

- **Description**: Third execution run — 1 medium-risk item (culture-art / classical painting re-interpretation)
- **Items**: Q-6E-B-005
- **Estimated images**: 1
- **Budget tier**: tier_1_minimal
- **Human gate**: approve_batch_3
- **Estimated wall-clock**: ~5 min
- **Preconditions**:
  - approve_batch_3 from 爸爸
  - Run 1+2 quality review complete
  - culture-art human review path ready (since risk=medium)
- **Expected outputs**:
  - images/2026/06/<asset_id>_001.jpg (1 file)
  - metadata/generated-assets.json (appended)
  - Phase 6E-B culture-art review report (if human flags any issue)

---

## 5. 4 个人类 Gate (Required Confirmations)

| gate_id | 描述 | owner | 触发时机 | 决策路径 | 默认 | 阻塞影响 |
|---------|------|-------|----------|----------|------|----------|
| `gate_1_approve_batch_1` | Approve Run 1 (2 images: code + academic) | 爸爸 | run 前 | Telegram reply or dashboard/approval-6eb-batch-1.json (human-set) | pending | image model will not be called |
| `gate_2_approve_batch_2` | Approve Run 2 (2 images: dev-community + ai-ecosystem) | 爸爸 | run 前 | Telegram reply or dashboard/approval-6eb-batch-2.json (human-set) | pending | Run 2 will not start |
| `gate_3_approve_batch_3` | Approve Run 3 (1 image: culture-art / Penitence, medium risk) | 爸爸 | run 前 | Telegram reply or dashboard/approval-6eb-batch-3.json (human-set) | pending | Run 3 will not start |
| `gate_4_approve_model_spend` | Approve total budget cap for 5 image generations | 爸爸 | run 前 | Telegram reply or dashboard/approval-6eb-spend.json (human-set) | pending | No image generation runs will execute |

**决策触发**: Telegram reply Y/N 或 dashboard/approval-6eb-*.json (人类手写)

---

## 6. Safety Strategy

- **watermark_default**: True
- **watermark_rationale**: Watermark all 5 first-batch images (pre-publish safety); human can choose to regenerate without watermark after first review
- **image_review_required_per_item**: True
- **human_review_path_for_medium_risk**: culture-art: human review post-generation, can request regenerate
- **auto_publish_disabled**: True
- **baoyu_post_to_x_disabled**: True
- **x_api_disabled**: True

---

## 7. Out of Scope (本 plan 不做)

- **video_generation**: not in 6E-B; separate phase 6J
- **music_generation**: not in 6E-B; separate phase 6K
- **republishing_to_x**: not in 6E-B; Phase 6F (X performance review) is separate
- **blog_drafts**: not in 6E-B; 6G-blog separate
- **changing_6d5_closeout**: not allowed; 6D-5 final_status=closed must remain

---

## 8. Validator 验证 (auto)

预生成 `scripts/validate-image-generation-plan.ts` 验证以下结构:

- ✅ Phase = 6E-B / Mode = controlled_image_generation_plan
- ✅ 5 items selected (1 per source_type, 5/5 覆盖)
- ✅ 3 runs planned (2+2+1)
- ✅ 4 human gates defined (batch_1/2/3 + spend)
- ✅ 全部 selected items 标记 `decision: pending_human_approval`
- ✅ Watermark 默认 True, aspect_ratio 匹配 baseline
- ✅ boundaries 全 locked: no_model_call / no_media_generation / etc.
- ✅ 6D-5 closeout 仍 `final_status=closed`

---

## 9. 6E-B Plan Closeout

**Status**: ready  
**Phase**: 6E-B  
**Mode**: controlled_image_generation_plan (PLAN ONLY)  
**Recommended next phase**: 6E-B-execution (gated on human approval)  

**Output files**:
- `creative-quota-assets/dashboard/image-generation-plan.json`
- `creative-quota-harvester/dashboard/image-generation-plan.json`
- `creative-quota-assets/reports/image-generation-plan.md` (this file)
- `creative-quota-assets/docs/PHASE_6EB_CONTROLLED_IMAGE_GENERATION_PLAN.md`
- `creative-quota-harvester/scripts/validate-image-generation-plan.ts`

**Strict boundaries preserved**: 6D-5 closeout 未被修改; C5N freeze 未被修改; control plane 未被修改. **No image model called, no media generated.**
