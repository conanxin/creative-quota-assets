# 图片 Prompt 解释 · stabilityai/stable-video-diffusion-img2vid-xt

这张图为什么这样画：

- **策略**：ai-ecosystem → 模型能力图 / pipeline flow / model card hero，强调「能力输入输出 + 关键指标」
- **目标画面**：model capability diagram
- **风格关键词**：model card visual、Hugging Face inspired、amber to magenta gradient、dark slate background
- **构图提示**：Hero: large model name badge with version. Center: capability flow from input → model → output.
- **负面提示**：低质量、模糊、水印、人物面孔
- **推荐参数**：16:9 · 2K · model card, hero, dark slate, gradient

## 完整中文意图

把 HF 模型包成「模型卡 hero 图」。模型：stabilityai/stable-video-diffusion-img2vid-xt。任务类型：任务类型: image-to-video。底层库：库: diffusers。下载量：下载量: 200,356。点赞数：点赞数: 3,315。核心思路：左中右三段式 — 任务/输入图标 → 模型块（带层次感）→ 输出图标，右侧加 2-3 个指标瓦片

## 完整英文 Prompt

```text
A polished AI model card visual. model name "stabilityai/stable-video-diffusion-img2vid-xt" shown as a large hero badge. central pipeline flow: input (icon) → model block with subtle inner layers → output (icon). task label "image-to-video" near the input. two or three monospaced metric tiles on the right: downloads, likes, library. style: Hugging Face inspired, dark slate background, amber-to-magenta gradient, soft glow. no human faces, no company logos
```

## 适合的使用场景

- X 帖封面 / Open Graph 卡片
- 公众号 / 博客头图
- 内部技术分享视觉

---
本文件是 image-prompt.enriched.md 的人类可读解释版。