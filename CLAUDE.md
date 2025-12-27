# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 常用命令（开发相关）

- 本仓库为纯 Markdown 内容库，未检测到构建、Lint、测试脚本。
- 构建：无（N/A）。
- Lint：无（N/A）。
- 测试：无（N/A，亦无单测框架与“运行单个测试”的命令）。
- 预览：使用本地编辑器/查看器的 Markdown 预览功能；仓库未内置预览命令。

## 高层架构与结构

- 仓库定位：内容型笔记库（不包含可执行应用代码）。
- 主要目录：
  - `notes/` — 存放 Markdown 文章与笔记。
- 文件特征：
  - Markdown 文件顶部使用 front matter（YAML 风格）记录元数据，示例键：`tags`（数组）、`title`（字符串）、`created`（ISO 8601 字符串）、`modified`（ISO 8601 字符串）。
  - 文件名与标题可使用中文与空格；请在路径引用时注意正确转义/引用。
- 规则与说明：
  - 未发现 `.cursor/`、`.cursorrules`、`.github/copilot-instructions.md` 等规则文件。
  - 未发现 `README.md` 或构建/运行相关文档。

## 在本仓库使用 Claude Code 的工作要点

- 任务定位：以内容维护为主（新增/编辑 Markdown、统一 front matter、修正格式或内部链接）。
- 修改策略：
  - 仅在必要时新增文件（遵循“优先编辑现有文件”的原则）。
  - 保持 front matter 键名与格式一致（尤其是 `created`/`modified` 的 ISO 8601 字符串）。
- 工具使用建议：
  - 发现性操作：使用 Explore 子代理了解整体结构；针对于特定文件用 Read 精读。
  - 编辑：使用 Edit 精准替换；避免一次性重写整篇文档（便于审阅差异）。
  - 引用片段：在讨论中使用 `file_path:line_number` 形式定位（例：`notes/程序员的AI开发第一课.md:8`）。
  - 任务管理：使用 TodoWrite 跟踪内容编辑任务，逐项完成并及时标记完成。

## 约定与建议（非通用实践，仅基于现状）

- Front matter：保持上述键集合与类型一致；新增键前请在对话中说明用途以利后续一致性。
- 时间戳：`created`/`modified` 使用 ISO 8601 字符串（示例：`2024-12-25T14:55:24.715Z`）。
- 内容链接：若添加跨文档引用，尽量使用相对路径并在提交前通过 Read 验证目标存在。
