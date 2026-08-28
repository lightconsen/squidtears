# 构建与项目说明（Build）

> 本文件负责项目的**工程侧**内容：目录结构、导出构建、创作方式。[README.md](README.md) 是读者向的书籍首页（封面、在线阅读与下载链接）。

## 目录结构

- `story.md` — 完整故事大纲（4 部分 16 章、四种结局、伏笔清单、真实事件索引）。**设定以它为准。**
- `01_drafts/` — 正文草稿，按部分建目录（当前 16 章草稿在 `part1_seed/`）
- `02_tracking/` — 写作台账：章节进度 / 时间线校验 / 角色弧光追踪 / 伏笔回收状态
- `03_review/` — 审核记录（三维度审核 + 打磨记录）
- `04_exports/` — 导出成品（HTML / DOCX / EPUB / PDF），由 GitHub Actions 自动生成并提交回仓库
- `assets/` — 封面等资源（`cover.jpg`）
- `.github/workflows/export.yml` — 自动导出 workflow
- `CLAUDE.md` — 项目写作约定（给协作 AI 的记忆）
- `LICENSE` — 版权许可（中文为权威版本）

## 导出构建

### 方式一：GitHub Actions（推荐，无需本地安装）

push 到 `main`（且改动涉及 `01_drafts/`、`story.md` 或 workflow 本身）后，workflow **「导出《鱿鱼之泪》」** 会自动：

1. 用 `pandoc/latex` 官方镜像生成 **HTML / DOCX / EPUB / PDF** 四种格式；
2. **提交回 `04_exports/` 目录**——README 里的下载链接因此始终有效；
3. 同时上传 artifact `squid-tears-exports` 作为备份。

也可在 Actions 页面手动触发（Run workflow）。

- 产物：`squid-tears.html` / `squid-tears.docx` / `squid-tears.epub` / `squid-tears.pdf`
- PDF 用 xelatex + Noto Sans CJK 中文字体排版（边距 2.5cm、带目录）
- HTML 为自包含单文件（CSS 内嵌、带目录），可直接在浏览器打开

### 方式二：本地 Pandoc

需安装 [Pandoc](https://pandoc.org/)（PDF 另需 LaTeX 引擎与中文字体，macOS 可 `brew install pandoc`）：

```bash
# HTML（在线阅读）
pandoc 01_drafts/part1_seed/*.md -o 04_exports/squid-tears.html \
  -s --embed-resources --toc \
  --metadata title="鱿鱼之泪" --metadata author="john2ai" --metadata lang=zh-CN

# DOCX
pandoc 01_drafts/part1_seed/*.md -o 04_exports/squid-tears.docx \
  --metadata title="鱿鱼之泪" --metadata author="john2ai" --metadata lang=zh-CN

# EPUB
pandoc 01_drafts/part1_seed/*.md -o 04_exports/squid-tears.epub \
  --toc --metadata title="鱿鱼之泪" --metadata author="john2ai" --metadata lang=zh-CN

# PDF
pandoc 01_drafts/part1_seed/*.md -o 04_exports/squid-tears.pdf \
  --pdf-engine=xelatex --toc -V geometry:margin=2.5cm \
  -V mainfont="Noto Sans CJK SC" -V CJKmainfont="Noto Sans CJK SC" \
  --metadata title="鱿鱼之泪" --metadata author="john2ai"
```

注意：glob 展开需按章节数字顺序（01 → 16）；`10_`、`11_` 等会排在 `09_` 之前，请用 `sort -V` 排序或显式列出文件。

## 创作方式

人主导方向，Claude Code 负责执行、润色与一致性检查。每章完成后维护 `02_tracking/` 四份台账（进度 / 时间线 / 弧光 / 伏笔），确保设定不穿帮、伏笔全部回收。
