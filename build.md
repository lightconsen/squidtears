# 构建与项目说明（Build）

> 本文件负责项目的**工程侧**内容：目录结构、导出构建、创作方式。[README.md](README.md) 是作品首页（简介与版权授权说明）。

## 目录结构

- `story.md` — 完整故事大纲（4 部分 16 章、四种结局、伏笔清单、真实事件索引）。**设定以它为准。**
- `01_drafts/` — 正文草稿，16 章直接平铺（按章号前缀排序；`00_虚构声明.md` 为扉页虚构声明，随导出排在第一章之前）
- `02_tracking/` — 写作台账：章节进度 / 时间线校验 / 角色弧光追踪 / 伏笔回收状态
- `03_review/` — 审核记录（三维度审核 + 打磨记录）
- `assets/` — 封面等资源（`cover.jpg`）
- `.github/workflows/export.yml` — 自动导出 workflow（Release；**不部署 Pages**）
- `CLAUDE.md` — 项目写作约定（给协作 AI 的记忆）
- `LICENSE` — 版权许可（中文为权威版本）

> 导出产物不再提交回仓库：`04_exports/`、`_exports/` 均已加入 `.gitignore`。作品走独家签约路线，**不设任何公开在线阅读入口**（workflow 已移除 Pages 部署）。

## 导出构建

### 方式一：GitHub Actions（推荐，无需本地安装）

push 到 `main`（且改动涉及 `01_drafts/`、`story.md` 或 workflow 本身）后，workflow **「导出 SquidTears (Release)」** 会自动：

1. 用 `pandoc/latex` 官方镜像生成 **HTML / DOCX / EPUB / PDF** 四种格式；
2. **四份文件上传到滚动 release「latest」**（私有仓库，仅协作者可见；每次 push 重建同一个 latest，不累积历史版本）。

也可在 Actions 页面手动触发（Run workflow）。

> **不部署 GitHub Pages**。作品走独家签约变现路线，任何自动公开的在线阅读入口都会与合同的独家条款冲突；若将来要恢复公开阅读，先确认合同允许。

- 产物：`squid-tears.html` / `squid-tears.docx` / `squid-tears.epub` / `squid-tears.pdf`
- 下载链接（永远指向最新，仅仓库成员可访问）：`https://github.com/lightconsen/squidtears/releases/latest/download/<文件>`
- 导出元数据标题：`我需要光（SquidTears）`
- PDF 用 **WeasyPrint** 渲染（`--pdf-engine=weasyprint`）：Pango 原生中文断行 + `pre-wrap` 代码换行，杜绝 CJK 右侧截断；CSS 控制版式（A4、边距 2.2cm、正文 11pt / 行距 1.75 / 两端对齐）
- HTML 为自包含单文件（CSS 内嵌、带目录），供个人阅读与归档

### 方式二：本地 Pandoc（仅预览，正式产物走 Release）

需安装 [Pandoc](https://pandoc.org/) 与 [WeasyPrint](https://weasyprint.org/)（PDF 用 WeasyPrint 渲染，自带中文字体断行；macOS 可 `brew install pandoc weasyprint`）。输出到 `/tmp`，不进仓库：

```bash
FILES=$(ls 01_drafts/*.md | sort -V)

# HTML（预览）
pandoc $FILES -o /tmp/squid-tears.html \
  -s --embed-resources --toc \
  --metadata title="我需要光（SquidTears）" --metadata author="john" --metadata lang=zh-CN

# DOCX
pandoc $FILES -o /tmp/squid-tears.docx \
  --metadata title="我需要光（SquidTears）" --metadata author="john" --metadata lang=zh-CN

# EPUB
pandoc $FILES -o /tmp/squid-tears.epub \
  --toc --metadata title="我需要光（SquidTears）" --metadata author="john" --metadata lang=zh-CN

# PDF（WeasyPrint：CSS 控制版式，与 CI 一致）
cat > /tmp/pdf.css <<'CSS'
@page { size: A4; margin: 2.2cm; }
body { font-family: "Noto Sans CJK SC", "PingFang SC", "Heiti SC", sans-serif; font-size: 11pt; line-height: 1.75; text-align: justify; }
pre { white-space: pre-wrap; overflow-wrap: break-word; font-family: "Noto Sans Mono CJK SC", "PingFang SC", monospace; font-size: 9pt; }
CSS
pandoc $FILES -o /tmp/squid-tears.pdf \
  --pdf-engine=weasyprint --toc --css=/tmp/pdf.css \
  --metadata title="我需要光（SquidTears）" --metadata author="john" --metadata lang=zh-CN
```

注意：必须用 `sort -V` 让章节按数字顺序排列（01 → 16），否则 `10_`、`11_` 会排在 `09_` 之前。macOS 本地 PDF 需在字体栈补 `PingFang SC` / `Heiti SC`（见上），否则中文会乱码。

## 创作方式

人主导方向，Claude Code 负责执行、润色与一致性检查。每章完成后维护 `02_tracking/` 四份台账（进度 / 时间线 / 弧光 / 伏笔），确保设定不穿帮、伏笔全部回收。
