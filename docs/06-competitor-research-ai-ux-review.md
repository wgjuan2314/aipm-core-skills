# Competitor Research: ai-ux-review

调研日期：2026-05-26

## 调研目标

为首个 skill `ai-ux-review` 寻找 GitHub 和 skill 市场中的相近竞品，判断已有项目覆盖了什么，以及我们的差异化机会在哪里。

## 主要竞品

| 项目 | 热度 | 形态 | 主要覆盖 | 对我们的启发 |
| --- | ---: | --- | --- | --- |
| `nextlevelbuilder/ui-ux-pro-max-skill` | 82k+ stars | 跨平台 UI/UX skill | UI 风格、设计系统、颜色、字体、技术栈、UX guideline | 高星项目证明 UI/UX skill 有需求，但它更偏通用界面设计，不专门解决 AI 产品信任和失败兜底。 |
| `zuocharles/vibe-coded-website-review` | 0 stars | Claude skill | 识别 AI 生成网站常见视觉反模式 | 结构值得参考：清晰 frontmatter、核心反模式、快速 checklist。我们的方向应从“网站看起来像 AI 做的”升级到“AI 功能用起来是否可信”。 |
| `Acrobatux/ai-ux-auditor` | 0 stars | Python audit toolkit | 高风险系统的可访问性、可用性、安全关键流程、标准映射 | 证明高风险 UX audit 有价值，但它偏工程化和标准合规。我们的版本要更轻、更适合 AI PM 使用。 |
| `cwp-x/ai-ux-auditor` | 0 stars | 网站审计系统 | 性能、可访问性、PageSpeed、优化建议 | 更像网页质量审计，不是 AI 产品交互审查。 |
| `ux-toolkit` | 163 stars | 综合 UX evaluation skill | UX audit、可访问性、用户流、响应式测试、交互评估 | 适合参考“多维度审查”的表达，但它仍偏通用 UX。我们的切口要聚焦 AI 输出、控制、透明和恢复。 |

## 竞品共性

- 通用 UI/UX 项目更容易获得关注，因为使用场景广。
- 高质量 skill 通常会有清晰的 frontmatter，告诉 AI 什么时候触发。
- 好的审查类 skill 往往包含 checklist、反模式、优先级和可操作建议。
- 现有竞品大多关注界面视觉、可访问性、响应式、组件质量或网页性能。

## 竞品空位

现有竞品较少系统覆盖以下 AI 产品体验问题：

- 用户是否知道 AI 能做什么、不能做什么。
- AI 输出是否表达不确定性。
- 用户能否撤回、确认、编辑或跳过 AI 建议。
- AI 失败时是否有空状态、低置信度状态、人工介入或兜底路径。
- 高风险场景中是否避免诊断式、绝对化、误导性措辞。
- AI Agent 或 AI Coding 工具执行动作前是否需要用户确认。

## 我们的定位

`ai-ux-review` 不和通用 UI/UX skill 拼风格库、组件库和技术栈覆盖，而是聚焦：

> AI 功能进入真实产品后，用户是否能理解、信任、控制和恢复。

这更贴合项目 owner 的 10 年体验设计背景，也更适合在面试中讲清楚 AI 产品经理能力。

