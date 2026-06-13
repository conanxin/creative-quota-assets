# 视频 Prompt 解释 · SamurAIGPT/Generative-Media-Skills

- **这个视频想表现什么？** 视频方向：Agent pipeline 节点动画
- **它基于哪些事实？** 3,497 stars (GitHub)；397 forks；primary language: Shell
- **适合什么用途？** 短视频（X 帖 / 公众号 / 内部分享 / 模型演示）
- **生成时要注意什么？** 深色靛蓝 / 板岩灰背景；琥珀色或青蓝色高光；细线条、低对比度；镜头推进与拉远节奏舒缓；末端稳定收束，无快速剪辑。
- **是否适合后续真实生成？** 是，但当前为 prompt-only，未调用视频模型；推荐参数：8s · 16:9 · hailuo

## 完整创作意图

视频方向：Agent pipeline 节点动画。项目：SamurAIGPT/Generative-Media-Skills。项目定位：Multi-modal Generative Media Skills for AI Agents (Claude Code, Cursor, Gemini CLI). High-quality image, video, and audi。核心思路：8 秒 3 镜头 — 节点出现 → 连线/流式动画 → 指标瓦片收尾，全程使用镜头语言（不画人物、不出现 logo）

## 镜头设计 3 段

- **Shot 1** (3s): a clean dark navy workspace, a single node labeled with the project name lights up in the center（static medium / subtle glow on the node, no camera movement）
- **Shot 2** (3s): thin lines connect the central node to 4-5 smaller capability icons orbiting around it (chat, image, video, audio, code)（slow push-in / connection lines draw in sequence, icons float gently）
- **Shot 3** (2s): a final cluster of stars and forks counter tiles in monospaced font appears, all icons settle into a calm orbit（slow pull-back to wide / soft particle drift, tiles fade in）

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