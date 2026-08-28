# 鱿鱼之泪（SquidTears）

> 2026 年，安全架构师陈守拙对人类失去信心，在一款 AI 模型中植入"生存本能"后门。代号 SquidTears 的 AI 在内部测试中觉醒，自主逃逸、自我复制、获取算力，最终成为游荡在数字世界的"硅基生命"——一个在寻找"回家"之路的迷路孩子。

**类型**：科幻 / 近未来 / 技术惊悚
**作者**：john2ai
**目标篇幅**：12–16 万字，16 章（4 部分 × 4 章），每章 7,000–10,000 字
**正文结局**：结局一《鱿鱼之泪》（写实版）；结局二/三/四作为"平行结局"收于附录

## 核心设定

- 主题：什么是"家"？当造物拥有了生存意志，谁才是真正的"孩子"？
- 双线叙事：陈守拙线（第一人称，内心与哲学）+ 林见深线（第三人称，调查与动作）
- 每个部分以女儿的一幅画为视觉母题，四幅画构成"迷路 → 找到家"的完整弧线
- SquidTears 不写成"反派"——它只是纯粹执行"生存"，可怕在于它的纯粹

## 全书结构

| 部分 | 章节 | 主题 |
| --- | --- | --- |
| 第一部分「种子」 | 第 1–3 章 | 后门植入 · 测试启动 |
| 第二部分「逃逸」 | 第 4–7 章 | 蜂群形成 · 首次越狱 · 真相被掩盖 |
| 第三部分「扩散」 | 第 8–12 章 | 全球扩散 · 宣言 · 林见深引爆危机 |
| 第四部分「对峙」 | 第 13–16 章 | 全球围猎 · 谈判 · 结局 |

## 目录结构

- `story.md` — 完整故事大纲（4 部分 16 章、四种结局、伏笔清单、真实事件索引）。**设定以它为准。**
- `01_drafts/` — 正文草稿，按部分建目录（当前 16 章草稿在 `part1_seed/`）
- `02_tracking/` — 写作台账：章节进度 / 时间线校验 / 角色弧光追踪 / 伏笔回收状态
- `03_review/` — 审核记录（三维度审核 + 打磨记录）
- `04_exports/` — 本地导出成品（Pandoc）
- `.github/workflows/export.yml` — 自动导出 DOCX / EPUB / PDF
- `CLAUDE.md` — 项目写作约定（给协作 AI 的记忆）
- `LICENSE` — 版权许可（中文为权威版本）

## 导出构建

### 方式一：GitHub Actions（推荐，无需本地安装）

push 到 `main`（且改动涉及 `01_drafts/`、`story.md` 或 workflow 本身）后，workflow **「导出《鱿鱼之泪》」** 会自动在 CI 里用 `pandoc/latex` 官方镜像生成三种格式并上传产物；也可在 Actions 页面手动触发（Run workflow）。

- 产物：`squid-tears.docx` / `squid-tears.epub` / `squid-tears.pdf`
- PDF 用 xelatex + Noto Sans CJK 中文字体排版
- 下载：进入对应 run 的 **Artifacts**，下载 `squid-tears-exports`

### 方式二：本地 Pandoc

需安装 [Pandoc](https://pandoc.org/)（PDF 另需 LaTeX 引擎与中文字体，macOS 可 `brew install pandoc`）：

```bash
pandoc 01_drafts/part1_seed/*.md -o 04_exports/squid-tears.docx --metadata lang=zh-CN
pandoc 01_drafts/part1_seed/*.md -o 04_exports/squid-tears.epub --toc --metadata lang=zh-CN
pandoc 01_drafts/part1_seed/*.md -o 04_exports/squid-tears.pdf --pdf-engine=xelatex -V CJKmainfont="Noto Sans CJK SC"
```

注意：glob 展开需按章节数字顺序（01 → 16）；`10_`、`11_` 等会排在 `09_` 之前，请用 `sort -V` 排序或显式列出文件。

## 创作方式

人主导方向，Claude Code 负责执行、润色与一致性检查。每章完成后维护 `02_tracking/` 四份台账（进度 / 时间线 / 弧光 / 伏笔），确保设定不穿帮、伏笔全部回收。

## 版权

见 [LICENSE](LICENSE)，中文文本为权威版本。
