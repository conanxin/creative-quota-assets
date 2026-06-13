# 视频 Prompt 解释 · stabilityai/stable-video-diffusion-img2vid-xt

- **这个视频想表现什么？** 视频方向：model pipeline flow (input image → motion → video)
- **它基于哪些事实？** model: stabilityai/stable-video-diffusion-img2vid-xt；task: 任务类型: image-to-video；library: 库: diffusers
- **适合什么用途？** 短视频（X 帖 / 公众号 / 内部分享 / 模型演示）
- **生成时要注意什么？** 深色板岩背景；琥珀 → 紫红渐变高光；monospaced 指标瓦片；HF 风格；节奏舒缓，无快速剪辑。
- **是否适合后续真实生成？** 是，但当前为 prompt-only，未调用视频模型；推荐参数：8s · 16:9 · hailuo

## 完整创作意图

视频方向：model pipeline flow (input image → motion → video)。模型：stabilityai/stable-video-diffusion-img2vid-xt。任务类型：任务类型: image-to-video。底层库：库: diffusers。下载量：下载量: 200,356。点赞数：点赞数: 3,315。核心思路：8 秒 3 镜头 — 输入 → 模型处理 → 输出；末尾显示关键指标瓦片

## 镜头设计 3 段

- **Shot 1** (3s): a single still image card floats in the lower-left, glowing softly, on dark slate background（static medium / image pulses gently）
- **Shot 2** (3s): frame-by-frame strip emerges to the right, each frame 1/4 step further along the motion timeline, subtle blur indicating motion（slow pan L→R / frames appear in sequence, motion arrows between them）
- **Shot 3** (2s): final frame holds, a monospaced metric tile (downloads/likes) fades in below（static / final frame stabilizes, tile fades in）

## 适合的使用场景

- X 帖短视频（≤8s）
- 公众号 / 博客头图视频化
- 内部技术分享 / 路演开场
- AI 模型能力演示

## 与现有素材的关系

- 原始 video-prompt.md：保留为兜底短语，不被覆盖
- image-prompt.enriched.md：图片视觉可作为首帧参考（本 prompt 不强制图生视频，可独立运行）

---
本文件是 video-prompt.enriched.md 的人类可读解释版。