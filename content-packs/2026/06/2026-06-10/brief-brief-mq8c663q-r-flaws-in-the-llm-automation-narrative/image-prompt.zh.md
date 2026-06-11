# 图片 Prompt 解释 · Flaws in the LLM Automation Narrative

这张图为什么这样画：

- **策略**：academic → 论文概念图/学术信息图，强调「研究方法 + 关键数据 + 论文气质」
- **目标画面**：paper concept diagram
- **风格关键词**：academic poster、serif and sans-serif typography、deep blue and gold accents、clean white background
- **构图提示**：Top: paper title in serif. Middle: one large conceptual figure. Bottom: 3-stat row (e.g. accuracy, sample size, year).
- **负面提示**：低质量、模糊、水印、人物面孔
- **推荐参数**：4:3 · 2K · academic poster, data-viz, minimalist

## 完整中文意图

把论文包装成「学术海报」风格的视觉摘要。论文标题：Flaws in the LLM Automation Narrative。核心摘要：Large Language Models (LLMs) are increasingly described as performing at the level of human experts on knowledge economy tasks. These claims are primarily based on how LLMs perform on benchmarking tas。主图：方法论/概念图（不画人物面孔），辅以 3 项关键数据瓦片

## 完整英文 Prompt

```text
An academic poster for a research paper. paper title "Flaws in the LLM Automation Narrative" in elegant serif at the top. central conceptual diagram: abstract geometric shapes forming a flow, suggesting research methodology. three small data tiles at the bottom: key metric, sample size, year. style: deep navy blue, ivory white, gold accents, light dotted grid, Edward Tufte inspired. small badge with primary category "arxiv:cs.AI". no human faces, no logo of journals
```

## 适合的使用场景

- X 帖封面 / Open Graph 卡片
- 公众号 / 博客头图
- 内部技术分享视觉

---
本文件是 image-prompt.enriched.md 的人类可读解释版。