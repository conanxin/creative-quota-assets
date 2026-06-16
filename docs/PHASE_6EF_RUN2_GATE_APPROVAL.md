# Phase 6E-F: Approve Run 2 Image Generation Gate

**Phase:** 6E-F
**Mode:** run2_gate_approval_only
**Date:** 2026-06-16
**Status:** COMPLETE
**Strict boundary:** No model call, no media generation, no X publish, no timer/digest/promote/C5N

---

## 1. Purpose

Phase 6E-F records the **human gate decision** for **Run 2** of the 5-image Phase 6E-B controlled image generation plan. This phase:

- Records the Run 2 gate decision only
- Updates the dashboard JSON files
- Adds the validator script (`validate:image-generation-run2-gates`)
- Does **NOT** execute image generation
- Does **NOT** call any image / video / music model
- Does **NOT** consume quota
- Does **NOT** approve Run 3
- Does **NOT** reopen Run 1
- Does **NOT** modify Run 1 final closeout (Phase 6E-I, message_id 50787)
- Does **NOT** touch the 6D-5 closeout

Run 2 image generation is blocked on a separate explicit command: `Phase 6E-J Run 2 Controlled Image Generation`.

---

## 2. Background

Phase 6E-B produced a controlled image generation plan covering 5 selected content packs (one per source_type), distributed across 3 execution runs:

| Run | Items | Risk Ladder | Status before 6E-F |
|-----|-------|-------------|--------------------|
| Run 1 | 2 items (code + academic) | Low risk | **closed (Phase 6E-I)** |
| Run 2 | 2 items (dev-community + ai-ecosystem) | Low risk | **approved (Phase 6E-F, this phase)** |
| Run 3 | 1 item (culture-art) | Medium risk | pending |

Run 1 final closeout (Phase 6E-I, message_id 50787, assets_commit=208671b, harvester_commit=943d74b) is **frozen at 2/2 usable images** (`approved_after_regen`). Phase 6E-F does not reopen Run 1.

---

## 3. Human Gate Decision

**Decision text:** `HUMAN_APPROVES_RUN_2_AND_LIMITED_SPEND_2_IMAGES`

**Decider:** 爸爸 (Xin Conan, chat_id 1540208324, message_id 50791)
**Decided at:** 2026-06-16T20:15:09+08:00

### 3.1 Approval scope

| Field | Value |
|-------|-------|
| `approve_batch_2` | **true** |
| `approve_model_spend_run2` | **approved_limited_run2_only** |
| `approved_run` | **run_2** |
| `approved_image_count_limit_run2` | **2** |
| `run_1_decision` | **closed** (from 6E-I, not modified) |
| `run_3_decision` | **pending** (not approved) |
| `total_5_image_plan_approval` | **partial** (Run 1 + Run 2, 4 of 5 images) |

### 3.2 Run 2 approved items

| item_id | title | source_type | aspect_ratio | risk_level |
|---------|-------|-------------|--------------|------------|
| `Q-6E-B-003` | River AI | dev-community | 1:1 | low |
| `Q-6E-B-004` | stabilityai/stable-video-diffusion-img2vid-xt | ai-ecosystem | 16:9 | low |

> **Note:** `risk_level` values are taken from `dashboard/image-generation-plan.json` (existing). Phase 6E-F does not rewrite them.

---

## 4. Gate Updates

### 4.1 `gate_2_approve_batch_2`

| Field | Before 6E-F | After 6E-F |
|-------|-------------|------------|
| decision | pending | **approved** |
| approved_run | null | **run_2** |
| approved_image_count_limit | null | **2** |
| approved_items | [] | **Q-6E-B-003, Q-6E-B-004** |
| decision_owner | 爸爸 | 爸爸 (no change) |
| decided_at | null | 2026-06-16T20:15:09+08:00 |
| decision_message_id | n/a | **50791** |

### 4.2 `gate_4_approve_model_spend`

| Field | Before 6E-F | After 6E-F |
|-------|-------------|------------|
| decision | approved_limited_run1_only | **approved_limited_run2_only** |
| approved_scope | Run 1 only (2 images maximum) | **Run 2 only (2 images maximum)** |
| approved_image_count_limit | 2 | 2 |
| run_1_budget_approval | true | **closed** (executed in 6E-D) |
| run_2_budget_approval | false | **true** |
| run_3_budget_approval | false | **false** |

### 4.3 `run_status.run_2`

| Field | After 6E-F |
|-------|------------|
| status | **approved_pending_generation** |
| approved | **true** |
| gate_approved_in_phase | **6E-F** |
| gate_decision_message_id | **50791** |
| generation_status | **not_started** |
| model_call_made | **false** |
| media_generated | **false** |
| next_required_action | separate human command required (Phase 6E-J Run 2 Controlled Image Generation) |

---

## 5. Boundaries enforced

| Boundary | Status |
|----------|--------|
| No image model call | ✅ `no_model_call=true` |
| No video model call | ✅ `no_video_generation=true` |
| No music model call | ✅ `no_music_generation=true` |
| No media generation | ✅ `no_media_generation=true` |
| No quota consumption | ✅ `no_run_2_generation_executed=true` |
| No Run 2 generation in 6E-F | ✅ generation_status=not_started |
| No Run 3 approval | ✅ `run_3.approved=false` |
| No Run 1 reopen | ✅ `run_1.closed=true`, `not_reopened_in_6ef=true` |
| No Run 1 final closeout modification | ✅ `run1_final_closeout_record.not_modified_in_6ef=true` |
| No 6D-5 modification | ✅ `no_6d5_modify=true` |
| No X publish | ✅ `no_x_publish=true` |
| No timer | ✅ `no_timer=true` |
| No digest | ✅ `no_digest=true` |
| No promote | ✅ `no_promote=true` |
| No C5N change | ✅ `no_c5n_change=true` |
| No secrets committed | ✅ `no_secrets=true` |

---

## 6. Counters (unchanged)

| Counter | Value | Source |
|---------|-------|--------|
| `total_generated_image_files` | **8** | (5 baseline + 2 from 6E-D + 1 from 6E-G regen) |
| `pending_images` | **18** | (unchanged from 6E-G) |
| `usable_run1_images` | **2 / 2** | (from 6E-I final closeout) |

Phase 6E-F does **NOT** add to these counters. Run 2 generation will only happen in Phase 6E-J (separate command).

---

## 7. Files written

### assets-repo
- `dashboard/image-generation-gates.json` (updated, Run 2 gate approval recorded)
- `docs/PHASE_6EF_RUN2_GATE_APPROVAL.md` (new, this file)
- `reports/image-generation-run2-gate-approval.md` (new)

### harvester-repo
- `dashboard/image-generation-gates.json` (updated, mirror)
- `dashboard/image-generation-plan.json` (updated, run_2 status block)
- `dashboard/mainline-production-queue.json` (updated, current_phase=6E-F, run2_gate_approval block)
- `dashboard/index.html` (updated, new 6E-F card)
- `scripts/validate-image-generation-run2-gates.ts` (new)
- `package.json` (new script `validate:image-generation-run2-gates`)
- `reports/phase-6ef-run2-gate-approval.md` (new)
- `reports/telegram-phase-6ef-run2-gate-approval.txt` (new)

---

## 8. Validators

- `validate:image-generation-run2-gates` (new)
- `validate:image-generation-run1-final`
- `validate:image-generation-regen-review-decision`
- `validate:image-generation-run1-regen`
- `validate:image-generation-run1-review-decisions`
- `validate:image-generation-run1-review`
- `validate:image-generation-run1`
- `validate:image-generation-gates`
- `validate:image-generation-plan`
- `validate:image-generation-preflight`
- `validate:x-manual-publishing-closeout`
- `validate:mainline-recovery`
- `validate:dashboard-control-safety`
- `dashboard:control:validate`
- `validate:telegram-sanitizer`
- `validate:project-report-send`

---

## 9. Next phase

> Run 2 generation is **NOT** auto-triggered. The next phase requires a separate explicit human command.

### Option · Phase 6E-J · Run 2 Controlled Image Generation
- Target: generate 2 approved Run 2 images (Q-6E-B-003 + Q-6E-B-004) within approved budget (2 images)
- Requires: separate explicit human command
- Hard limit #15: quota check required (general interval ≥ 50%)
- Auto-trigger: **false**

### Option · Idle · Stop here
- No further action
- Run 1 closed (2/2)
- Run 2 gate approved but generation not executed
- Run 3 still pending

---

## 10. Audit trail (Phase 6E series)

1. **6E-A:** Preflight validation (25 packs, 20 pending)
2. **6E-B:** Controlled image generation plan (3 runs, 5 items)
3. **6E-C:** Run 1 gate approval
4. **6E-D:** Run 1 generation (2 images, cum 5 → 7)
5. **6E-E:** Run 1 human review (1 approve, 1 needs_regen)
6. **6E-G:** Regen Q-6E-B-002 (1 image, cum 7 → 8)
7. **6E-H:** Regen human review (approve 76.6)
8. **6E-I:** Run 1 final closeout (closed, 2/2 usable, message_id 50787)
9. **6E-F (now):** Run 2 gate approval — generation NOT executed

---

_Phase 6E-F · Run 2 gate approval · ✅ COMPLETE · 2 Run 2 items approved · generation NOT executed · awaiting Phase 6E-J._