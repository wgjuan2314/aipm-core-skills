# Competitor Research: ai-prd-reviewer

调研日期：2026-05-26

## 调研目标

为第二个 skill `ai-prd-reviewer` 调研 GitHub 和公开工具中的 PRD / AI PRD / Claude Code PRD 竞品，判断已有项目覆盖了什么，以及我们的差异化机会在哪里。

## 主要竞品

| 项目 | 热度 | 形态 | 主要覆盖 | 对我们的启发 |
| --- | ---: | --- | --- | --- |
| `anombyte93/prd-taskmaster` | 451 stars | Claude Code skill | 面向 Taskmaster 的工程化 PRD 生成 | 高质量 PRD skill 已经存在，但重点是生成和 task breakdown，不是审查 AI PRD 是否成立。 |
| `rohitg00/CreateMVP` | 645 stars | Web app / 开源工具 | 从需求生成 MVP 文档和实现计划 | 说明“想法到 PRD/实现计划”需求强，但它偏生成器。 |
| `dredozubov/prd-generator` | 45 stars | Claude Code plugin | 生成完整 PRD | 证明 Claude Code 生态里 PRD 生成器正在增多。 |
| `fivetaku/show-me-the-prd` | 13 stars | Interview-driven PRD generator | 通过问答生成多份设计文档 | 问答式澄清值得参考，但我们更适合做审查和补缺口。 |
| `feba-capital/prd-generator` | 2 stars | Claude Code / Codex plugin | 将 freeform brief 变成多文档 PRD package，带不确定性标签和质量门 | “质量门”和“不确定性标签”值得借鉴。 |
| `Keeborg PRD Generator` | 商业工具 | AI PRD generator | 生成 AI-ready PRD、用户故事、验收标准、边界情况 | 市场语言强调 AI coding agents 需要清晰验收标准和边界情况。 |
| `PRD Stacks` | 商业工具 | 多 agent PRD generator | PRD、数据库、API、用户流、QA、Cursor/Windsurf super prompt | 说明“PRD 到 AI Coding 交接”是主流方向。 |

## 竞品共性

- 大多数竞品是“PRD 生成器”，从一句想法生成完整文档。
- 很多工具强调给 Claude Code、Cursor、Windsurf、Taskmaster 使用。
- 常见输出包括用户故事、验收标准、技术任务、API、数据模型、测试计划。
- 竞品普遍关注工程交接，但较少系统审查 AI 产品体验是否真的成立。

## 竞品空位

现有竞品较少系统覆盖：

- AI 功能为什么需要 AI，而不是普通规则功能。
- AI 输出质量标准如何定义。
- 模型不确定、跑题、幻觉、过度建议时怎么办。
- 用户如何控制、撤回、重试或纠正 AI。
- PRD 是否能支持 prompt、设计、开发、测试同时执行。
- PRD 是否有 AI 特有验收标准和 bad case。
- 从 AI PM 角度审查“这个需求是否足够成熟”，而不是直接生成长文档。

## 我们的定位

`ai-prd-reviewer` 不做“从零生成 PRD”的红海能力，而是做：

> AI PRD 审查器：判断一份 AI 产品需求是否清楚、可落地、可评测、可交接。

它更适合体现 AI 产品经理能力，因为真正的产品判断不是把文档写长，而是发现：

- 问题是否定义清楚。
- AI 体验是否成立。
- 模型行为是否有边界。
- 输出质量是否可验收。
- 失败和异常是否有兜底。
- 能不能交给设计、开发、prompt、测试和 AI Coding 工具继续推进。

