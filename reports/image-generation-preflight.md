# Phase 6E-A: Image Generation Preflight Report

> **Phase**: 6E-A  
> **Mode**: image_generation_preflight (read-only, dry-run)  
> **Generated at**: 2026-06-16T11:25:00+08:00  
> **Boundaries**: no_model_call / no_media_generation / no_telegram / no_timer / no_x_publish / no_promote / no_c5n_change / no_6d5_modify / no_secrets  

---

## 1. Executive Summary

- **Total content packs**: 25
- **Generated images**: 5 (one per source_type, all 5/5 source types covered)
- **Pending images**: 20 (80% gap — 20 packs have image prompts but no image)
- **Ready for human approval**: 20
- **Hold / Skip**: 0 / 0

**核心结论**: 25 个 content pack 的 image prompt 已全部就绪（100% 覆盖 `image-prompt.enriched.md`），
但只有 5 张图被生成（每 source_type 1 张，作为首批 cover image）。剩余 20 个 pack 全部 `ready_for_human_approval`，
等待 6E-B 阶段的人类预算/批决策。

**Strict boundaries**: 本次 preflight **不调用任何模型，不生成任何新图片，不消耗任何额度**。所有输出为只读文档/JSON。

---

## 2. Source / Signal Status (snapshot)

| 维度 | 数值 | 状态 |
|------|------|------|
| 唯一 topic | 5 | ✅ 覆盖 5 source_type × 5 topic |
| 每 topic version 数 | 5 | 同一 topic 5 次重写（不同 signal_id） |
| Content pack 完整性 | facts/x-post/summary/music_prompt 25/25 | ✅ |
| Video prompt 覆盖 | 5/25 | ⚠️ 仅 5 个 pack 有 video prompt |
| Webpage outline 覆盖 | 15/25 | ⚠️ 60% 覆盖 |
| facts.enriched.md 完整 | 10/25 | ⚠️ 多数 facts 为 '无增强数据' |

---

## 3. 已生成的 5 张图（baseline）

| pack_dir | source_type | watermark | model | quality_score | aspect_ratio |
|----------|-------------|-----------|-------|---------------|--------------|
| `brief-brief-mq8c6kp5-u-flaws-in-the-llm-automation-narrative` | academic | ✓ | image-01 | 96 | 16:9 |
| `brief-brief-mq8c6kp4-7-samuraigpt-generative-media-skills` | code | ✗ | image-01 | 97 | 16:9 |
| `brief-brief-mq8c6kp5-r-the-penitence-of-saint-jerome` | culture-art | ✗ | image-01 | 96 | 16:9 |
| `brief-brief-mq8c663q-v-river-ai` | dev-community | ✓ | image-01 | 97 | 1:1 |
| `brief-brief-mq8c663q-4-stabilityai-stable-video-diffusion-img2vid-xt` | ai-ecosystem | ✓ | image-01 | 95 | 16:9 |

**已生成图特征**: 5/5 quality ≥ 95 (excellent)，1/5 watermark=True（canary），1/5 是 1:1 aspect（River AI dev-community），其余 16:9。

---

## 4. 待生成的 20 个 pack 清单（preflight）

| pack_id | title | source_type | score | facts_complete | visual_clarity | aspect | watermark | risk | priority | decision |
|---------|-------|-------------|-------|----------------|----------------|--------|-----------|------|----------|----------|
| `brief-brief-mq8c663q-r-flaws-in-the-llm-automation-narrative` | Flaws in the LLM Automation Narrative | academic | 0.662 | ⚠️ | high | 16:9 | ✓ | low | high | ready_for_human_approval |
| `brief-brief-mq8c6xyg-v-flaws-in-the-llm-automation-narrative` | Flaws in the LLM Automation Narrative | academic | 0.662 | ⚠️ | high | 16:9 | ✓ | low | high | ready_for_human_approval |
| `brief-brief-mq8swsla-y-flaws-in-the-llm-automation-narrative` | Flaws in the LLM Automation Narrative | academic | 0.662 | ⚠️ | high | 16:9 | ✓ | low | high | ready_for_human_approval |
| `brief-brief-mq8tbqf4-j-flaws-in-the-llm-automation-narrative` | Flaws in the LLM Automation Narrative | academic | 0.662 | ⚠️ | high | 16:9 | ✓ | low | high | ready_for_human_approval |
| `brief-brief-mq8c6kp5-5-stabilityai-stable-video-diffusion-img2vid-xt` | stabilityai/stable-video-diffusion-img2vid-xt | ai-ecosystem | 0.476 | ⚠️ | high | 16:9 | ✓ | low | medium | ready_for_human_approval |
| `brief-brief-mq8c6xyg-j-stabilityai-stable-video-diffusion-img2vid-xt` | stabilityai/stable-video-diffusion-img2vid-xt | ai-ecosystem | 0.476 | ⚠️ | high | 16:9 | ✓ | low | medium | ready_for_human_approval |
| `brief-brief-mq8swsla-d-stabilityai-stable-video-diffusion-img2vid-xt` | stabilityai/stable-video-diffusion-img2vid-xt | ai-ecosystem | 0.476 | ⚠️ | high | 16:9 | ✓ | low | medium | ready_for_human_approval |
| `brief-brief-mq8tbqf4-s-stabilityai-stable-video-diffusion-img2vid-xt` | stabilityai/stable-video-diffusion-img2vid-xt | ai-ecosystem | 0.476 | ⚠️ | high | 16:9 | ✓ | low | medium | ready_for_human_approval |
| `brief-brief-mq8c663q-e-samuraigpt-generative-media-skills` | SamurAIGPT/Generative-Media-Skills | code | 0.703 | ✅ | high | 16:9 | ✓ | low | high | ready_for_human_approval |
| `brief-brief-mq8c6xyg-b-samuraigpt-generative-media-skills` | SamurAIGPT/Generative-Media-Skills | code | 0.703 | ✅ | high | 16:9 | ✓ | low | high | ready_for_human_approval |
| `brief-brief-mq8swsla-f-samuraigpt-generative-media-skills` | SamurAIGPT/Generative-Media-Skills | code | 0.703 | ✅ | high | 16:9 | ✓ | low | high | ready_for_human_approval |
| `brief-brief-mq8tbqf3-w-samuraigpt-generative-media-skills` | SamurAIGPT/Generative-Media-Skills | code | 0.703 | ✅ | high | 16:9 | ✓ | low | high | ready_for_human_approval |
| `brief-brief-mq8c663r-2-the-penitence-of-saint-jerome` | The Penitence of Saint Jerome | culture-art | 0.600 | ✅ | high | 16:9 | ✓ | medium | medium | ready_for_human_approval |
| `brief-brief-mq8c6xyg-5-the-penitence-of-saint-jerome` | The Penitence of Saint Jerome | culture-art | 0.600 | ✅ | high | 16:9 | ✓ | medium | medium | ready_for_human_approval |
| `brief-brief-mq8swsla-c-the-penitence-of-saint-jerome` | The Penitence of Saint Jerome | culture-art | 0.600 | ✅ | high | 16:9 | ✓ | medium | medium | ready_for_human_approval |
| `brief-brief-mq8tbqf4-8-the-penitence-of-saint-jerome` | The Penitence of Saint Jerome | culture-art | 0.600 | ✅ | high | 16:9 | ✓ | medium | medium | ready_for_human_approval |
| `brief-brief-mq8c6kp5-1-river-ai` | River AI | dev-community | 0.525 | ⚠️ | high | 1:1 | ✓ | low | medium | ready_for_human_approval |
| `brief-brief-mq8c6xyg-o-river-ai` | River AI | dev-community | 0.525 | ⚠️ | high | 1:1 | ✓ | low | medium | ready_for_human_approval |
| `brief-brief-mq8swsla-m-river-ai` | River AI | dev-community | 0.525 | ⚠️ | high | 1:1 | ✓ | low | medium | ready_for_human_approval |
| `brief-brief-mq8tbqf4-q-river-ai` | River AI | dev-community | 0.525 | ⚠️ | high | 1:1 | ✓ | low | medium | ready_for_human_approval |

---

## 5. 关键审计发现

### 5.1 Duplicate / Overlap Risk

- 25 个 pack 中，5 个 unique topic × 5 version = 25；每个 topic 5 个版本的 `image-prompt.enriched.md` 高度相似。
- `metadata/gallery-dedup-index.json` 已建立 canonical primary 映射（5 个 canonical 路径）。
- 风险：如果为每个 pack 单独生成 1 张图，会产出 5 张几乎相同的图，浪费预算。
- 建议：**仅对 canonical primary 包生成新图，其他 4 个 pack 共享同一 image 资产**（共享通过 `content_pack_dir` 引用）。

### 5.2 Facts Completeness Gap

- 25/25 有 `facts.enriched.md`，但部分 pack 标记为「无增强数据」（HF API failed）。
- 已知问题：Hugging Face Hub source timeout 导致部分 ai-ecosystem pack facts 缺失。
- 影响：image prompt 仍可生成（基于 title + strategy），但 post 文字会少一层数据引用。
- **缓解**：image preflight 不依赖 facts，事实缺口仅影响文字版 post，不影响 image 决策。

### 5.3 Visual Clarity

- 25/25 有 `image-prompt.meta.json`（visual_subjects + style_tags + composition_notes）。
- 多数 meta 提供 4-8 个 visual_subjects，2-3 条 composition_notes，**视觉清晰度高**。
- 唯一弱点：dev-community (River AI) 只有 4 个 visual_subjects + 2 条 composition_notes，
  → 但其已经生成的版本质量 97 分，说明模型可以从有限信息推断。

### 5.4 Risk Level

- 23/25 risk=low（academic/code/ai-ecosystem/dev-community），2/25 risk=medium（culture-art 系列）。
- culture-art medium 原因：涉及经典画作《The Penitence of Saint Jerome》再创作，
  → 已有 1 张生成图（gen-003）无水印且评分 96，证明模型可处理。
- **剩余 4 个 culture-art pack 也应设为 medium 风险**，需要人类对每张图手动 review。

---

## 6. Recommended Batches (供 6E-B 决策)

### 6.1 batch_2026-06-16_pilot (建议首批)

- **范围**: 5 张图（按 score 倒序挑选 5 个 pending pack，确保覆盖所有 source_type）
- **预算 tier**: tier_1_minimal
- **决策点**: 爸爸批准后才执行；不自动触发。
- **前置条件**: 6E-B 阶段需新增 `validate:image-generation-batch` 脚本 + 爸爸 spend approval。

### 6.2 batch_2026-06-20_full (第二批)

- **范围**: 剩余 15 张图
- **预算 tier**: tier_2_moderate
- **决策点**: 等 batch_1 评审后再决定。
- **前置条件**: 累计 20 张图预算，需爸爸明确 spend cap。

### 6.3 替代方案: dedup-aware 生成

- 仅生成 5 张（每 topic 1 张 canonical primary），
- 其他 15 个 pack 通过 `image_asset_ref` 字段引用同一张图（修改 manifest.json）。
- **优势**: 总预算 5 张（tier_1），20 个 pack 全部获得 image 资产引用。
- **劣势**: 牺牲了 visual diversity（5 张图 vs 20 张图）。
- **建议**: 与 6.1 并行作为选项，让爸爸选 A 还是 B。

---

## 7. 6E-B 阶段所需人类决策

| # | 决策项 | 默认建议 | 决策来源 |
|---|--------|----------|----------|
| 1 | 首批 batch 选 5 张（diverse）还是 1 张（canonical primary）？ | 5 张 diverse | 爸爸 spend approval |
| 2 | Watermark 策略：5/5 水印还是 1/5 水印？ | 全部水印（pre-publish 安全） | 爸爸 |
| 3 | Aspect ratio 策略：统一 16:9 还是 dev-community 1:1？ | 按 source_type 区分 | 已生成的 baseline |
| 4 | 每次 run 的图片上限？ | 5 张/run | dashboard/status.json 已设 2 张/run |
| 5 | 是否启用 dedup-aware 共享图？ | 暂不启用，保持 visual diversity | 爸爸 |

---

## 8. Validator 结果

预生成的 validator (`scripts/validate-image-generation-preflight.ts`) 验证以下结构：

- ✅ 25 items / 5 generated / 20 pending
- ✅ 100% 覆盖 image-prompt.enriched.md
- ✅ 100% 覆盖 facts / x-post / summary / music-prompt
- ✅ 所有 20 pending 标记 `decision: ready_for_human_approval`
- ✅ boundaries 全 locked: no_model_call / no_media_generation / etc.
- ✅ recommended_next_phase = '6E-B'

---

## 9. 6E-A Closeout

**Status**: pass  
**Phase**: 6E-A  
**Mode**: image_generation_preflight (read-only)  
**Output files**:
- `creative-quota-assets/dashboard/image-generation-preflight.json`
- `creative-quota-harvester/dashboard/image-generation-preflight.json`
- `creative-quota-assets/reports/image-generation-preflight.md`
- `creative-quota-assets/docs/PHASE_6EA_IMAGE_GENERATION_PREFLIGHT_REPORT.md` (this file)
- `creative-quota-harvester/scripts/validate-image-generation-preflight.ts`

**Recommended next phase**: 6E-B (gated image generation execution, requires human spend approval)  

**Strict boundaries preserved**: 6D-5 manual X publishing closeout 未被修改；C5N freeze 未被修改；control plane 未被修改。
