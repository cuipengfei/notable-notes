# Repository Guidelines

## 项目结构与模块组织
- 根目录含 `CLAUDE.md`（说明/草案）。
- 笔记位于 `notes/` 下的 Markdown 文件（`.md`）。
- 资源放在 `notes/attachments/`（图片等），思维导图在 `notes/mindmap/`（如 `tea.smm`）。
- 示例：`notes/程序员的AI开发第一课.md`、`notes/attachments/icon.png`。

## 构建、测试与开发命令
- 本仓库为纯笔记集合，无需构建或发布流程。
- 快速浏览文件：`rg --files notes`。
- 查看所有标题（用于索引）：`rg -n '^# ' notes`。
- 检查附件引用：`rg -n '\(attachments/' notes`。

## 代码/内容风格与命名约定
- 文件名与一级标题（`#`）尽量一致，中文标题优先；英文用 `kebab-case`（如 `export-geek-time-notes.md`）。
- 图片统一使用相对路径：`![描述](attachments/icon.png)`；资源仅存放于 `notes/attachments/`。
- Markdown 列表用 `- `，代码块使用三引号围栏；统一 UTF-8、LF。

## 测试与质量检查
- 无自动化测试；提交前自检：
  - 所有附件路径可用且指向 `notes/attachments/`。
  - 文档一级标题存在且与文件名匹配（尽量）。
  - 链接有效、无死链（可用编辑器或 `rg` 粗检）。

## Commit 与 Pull Request 规范
- Commit 信息使用动词开头和简短主题，例如：
  - `Create: 程序员的AI开发第一课.md`
  - `Update: 业务开发算法50讲.md`
  - 可使用简短标签（如 `tea`, `10x`）体现主题。
- PR 需包含：变更摘要、影响范围、示例截图（若更新附件）、关联 issue/背景；按小步可审原则拆分。

## 资产与导图管理
- 大图请提供小图/预览（如 `icon_small.png`）；保持资源体积可控。
- 思维导图（`.smm`）可同时保存源文件与导出图（如 PNG），便于查看与对比。
