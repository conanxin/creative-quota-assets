# 音乐 Prompt 解释 · stabilityai/stable-video-diffusion-img2vid-xt

- **这段音乐想表现什么？** 音乐方向：futuristic model flow (light pulse + soft synth)
- **基于哪些事实？** model: stabilityai/stable-video-diffusion-img2vid-xt；task: 任务类型: image-to-video；下载量: 200,356
- **适合什么用途？** 背景音乐、模型演示、短视频、产品卡片
- **推荐节奏 / 乐器 / 情绪**：90-110 BPM, gentle forward motion · soft analog synth pads, gentle pulse bass, sparse high-end plucks · clean, modern, slightly forward-looking
- **是否适合后续真实生成？** 是，但当前为 prompt-only，未调用音乐模型；推荐参数：60-90s · minimax-music · instrumental=true

## 完整创作意图

音乐方向：futuristic model flow (light pulse + soft synth)。模型：stabilityai/stable-video-diffusion-img2vid-xt。任务类型：任务类型: image-to-video。核心思路：60-90 秒干净现代的合成器背景，节奏轻盈；适合模型能力演示视频

## 音乐属性

- **mood**: clean, modern, slightly forward-looking
- **genre**: light electronic pulse
- **tempo**: 90-110 BPM, gentle forward motion
- **instrumentation**: soft analog synth pads, gentle pulse bass, sparse high-end plucks
- **texture**: clean, polished, slight sidechain pumping
- **energy**: medium-low, supportive, never dominates
- **loopability**: 4-bar motif loop, gentle transitions

## 适合的使用场景

- 背景音乐
- 模型演示
- 短视频
- 产品卡片

## 与现有素材的关系

- 原始 music-prompt.md：保留为兑底短语，不被覆盖
- video-prompt.enriched.md：音乐可作为视频背景音，节奏与镜头长度匹配（默认 60-90s vs 8s 视频，可以拼接循环）
- image-prompt.enriched.md：图片与音乐气质可同源（同一 source_type 策略）

---
本文件是 music-prompt.enriched.md 的人类可读解释版。