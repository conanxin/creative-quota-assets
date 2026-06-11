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
