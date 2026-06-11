# AI 创意素材库 / Creative Quota Assets

**公开素材库** — 从真实世界信号自动生成的 Creative Brief、Prompt 与内容包。

[查看在线 Gallery](https://conanxin.github.io/creative-quota-assets/gallery/)

---

## 📁 内容结构

| 目录 | 说明 |
|------|------|
| `content-packs/` | Creative Brief 内容包（含 metadata + prompts） |
| `gallery/` | 公开浏览页面（纯静态 HTML/CSS/JS） |
| `images/` | 已生成的图片素材 |
| `metadata/` | 索引数据（asset-index.json, generated-assets.json） |

---

## 🖼️ 已生成图片

目前已通过 MiniMax Token Plan 生成 **3 张**图片：

| 文件 | 来源 | 模型 | 日期 |
|------|------|------|------|
| `cqa-2026-06-11-canary-001_001.jpg` | Flaws in the LLM Automation Narrative | image-01 | 2026-06-11 |
| `cqa-2026-06-11-gen-002_001.jpg` | SamurAIGPT/Generative-Media-Skills | image-01 | 2026-06-11 |
| `cqa-2026-06-11-gen-003_001.jpg` | The Penitence of Saint Jerome | image-01 | 2026-06-11 |

音乐 / 视频尚未启用（Phase 3C quota guard 已就位）。

---

## 🎯 信号来源

| 来源 | 类型 | 数量 |
|------|------|------|
| GitHub Open Source Radar | 开源项目 | 持续更新 |
| arXiv AI | 学术研究 | 持续更新 |
| Hugging Face Hub | AI 模型生态 | 持续更新 |
| Hacker News | 开发者社区 | 持续更新 |
| The Met Collection | 文化艺术 | 持续更新 |
| 其他 | 日期与天气等 | 持续更新 |

---

## 🔗 链接

| 资源 | URL |
|------|-----|
| **Gallery 在线浏览** | https://conanxin.github.io/creative-quota-assets/gallery/ |
| GitHub 仓库 | https://github.com/conanxin/creative-quota-assets |
| Harvester 项目 | https://github.com/conanxin/creative-quota-harvester |
| Harvester Roadmap | https://github.com/conanxin/creative-quota-harvester/blob/main/docs/ROADMAP.md |

---

## ⚖️ 协议

| 内容 | 协议 |
|------|------|
| Creative Brief 与 Prompt 文本 | [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| 元数据（JSON、YAML） | [MIT](https://opensource.org/licenses/MIT) |
| 生成的图片 / 音乐 / 视频 | [CC-BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) |

---

## 🛠️ 技术说明

- **纯静态页面** — 无后端，可通过 GitHub Pages 免费托管
- **零依赖** — 不需要 npm / Node.js / 数据库即可浏览
- **信号采集** — Creative Quota Harvester 自动从多个公开 API 采集信号
- **Quota Guard** — 所有真实 MiniMax 生成需要显式确认（Phase 3C）

---

_Creative Quota Assets — AI 创意素材库_

---

## 📦 Content Pack 详情

每个 Content Pack 现在包含：

| 文件 | 说明 |
|------|------|
| `manifest.json` | 元数据（标题、来源类型、评分、标签） |
| `detail.json` | 结构化详情（一句话介绍、背景、推荐用途） |
| `content-summary.zh.md` | 中文内容摘要 |
| `brief.md` | Creative Brief |
| `facts.md` | 事实依据 |
| `x-post.zh.md` | X 帖草稿 |
| `image-prompt.md` | 图片生成 Prompt |
| `video-prompt.md` | 视频 Prompt |
| `music-prompt.md` | 音乐 Prompt |
| `webpage-outline.md` | 网页大纲 |

Gallery 页面可直接查看每个 Pack 的**一句话介绍**和**推荐用途**。

---

## 📄 Content Pack 详情页

每个 Content Pack 现在都有**人类可读的详情页**（index.html），从 Gallery 或每日归档中点击"详情"即可打开：

| 入口 | 内容 |
|------|------|
| **详情页** (`index.html`) | 人类可读的可视化页面：标题、来源、一句话介绍、背景、为什么值得关注、推荐用途、已有素材、Prompt 预览、开发者文件 |
| **摘要原文** (`content-summary.zh.md`) | Markdown 格式中文摘要 |
| **原始数据** (`detail.json`) | 机器可读的结构化数据 |

**示例详情页：**
https://conanxin.github.io/creative-quota-assets/content-packs/2026/06/2026-06-11/brief-brief-mq8swsla-f-samuraigpt-generative-media-skills/index.html

---

## 🖼️ 已生成图片说明

`metadata/generated-image-descriptions.json` 包含每张图片的中文描述：

| 图片 | 内容描述 |
|------|---------|
| cqa-2026-06-11-canary-001_001.jpg | 基于学术论文"Flaws in the LLM Automation Narrative"主题生成，呈现古典手稿与神经网络视觉融合 |
| cqa-2026-06-11-gen-002_001.jpg | 基于 SamurAIGPT/Generative-Media-Skills 项目主题生成 |
| cqa-2026-06-11-gen-003_001.jpg | 基于 The Penitence of Saint Jerome 艺术作品主题生成 |


---

## 📅 每日归档

按日期浏览每日采集的信号、Content Packs 和已生成内容：

- **日历首页:** https://conanxin.github.io/creative-quota-assets/daily/
- 按日期查看每天的 Content Packs、来源类型和已生成图片

**归档日期说明：**
- **Content Pack 日期**：内容包创建日期（manifest.json 的 created_at）
- **生成图片日期**：实际图片生成日期（metadata/generated-assets.json 的 generated_at）

同一内容包的图片可能在后续日期生成。例如：Content Pack 于 2026-06-10 创建，图片于 2026-06-11 生成，图片会归档到 2026-06-11。

当前归档日期：**2 天**
- 2026-06-11：10 Content Packs + 3 生成图片
- 2026-06-10：15 Content Packs

