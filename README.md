# AIPM Core Skills

AIPM Core Skills 是一套面向 AI 产品经理、AI 体验设计师和 AI Coding 实践者的本地 skill 项目。

这个项目的目标不是做一个“大而全”的提示词库，而是沉淀一组 AI 产品经理日常高频使用的工作能力：看懂 AI 功能、判断产品风险、审查体验质量、复盘失败案例，并把产品需求交接给 AI Coding 工具继续落地。

## 项目背景

这个项目用于把这些实践经验沉淀成可复用的开源 skills，让别人可以感知到 owner 不只是会用 AI 工具，也具备 AI 产品经理的判断、设计和落地能力。

## 首版 Skills

首版只做 5 个核心 skills：

1. `ai-ux-review`：审查 AI 产品体验是否可信、可控、可恢复。
2. `ai-prd-reviewer`：审查 AI PRD 是否覆盖模型边界、失败兜底和验收标准。
3. `agent-fit-analyzer`：判断一个需求是否真的适合做 Agent。
4. `badcase-diagnosis`：分析 AI 产品失败案例，定位问题来源和改进方向。
5. `ai-coding-handoff`：把产品需求整理成适合 Codex、Claude Code、Cursor 等 AI Coding 工具执行的任务说明。

暂不做 RAG。RAG 涉及切片、召回、重排、向量库、权限和评测等深水区，当前阶段先聚焦更贴合 owner 经验的 AI 产品与体验设计能力。

## 适合谁用

- 想从传统产品经理转向 AI 产品经理的人。
- 想把 UI/UX 经验升级为 AI 体验设计能力的人。
- 想用 Codex、Claude Code、Cursor 等工具做 AI Coding 协作的人。
- 想把个人 AI 项目包装成作品集和开源项目的人。

## 项目结构

```text
.
├── AGENTS.md
├── README.md
├── docs/
│   ├── 00-project-brief.md
│   ├── 01-sdd.md
│   ├── 02-skill-roadmap.md
│   ├── 03-progress-log.md
│   ├── 04-decisions.md
│   ├── 05-interview-notes.md
│   ├── 06-competitor-research-ai-ux-review.md
│   ├── 07-competitor-research-ai-prd-reviewer.md
│   ├── 08-competitor-research-agent-fit-analyzer.md
│   ├── 09-competitor-research-badcase-diagnosis.md
│   └── 10-competitor-research-ai-coding-handoff.md
├── examples/
│   ├── agent-fit-analysis-celebrity-council.md
│   ├── ai-coding-handoff-celebrity-council.md
│   ├── ai-prd-review-celebrity-council.md
│   ├── ai-ux-review-celebrity-council.md
│   ├── ai-ux-review-celebrity-council-v2.md
│   ├── badcase-diagnosis-celebrity-council.md
│   └── badcase-diagnosis-celebrity-council-simulated.md
└── skills/
    ├── ai-coding-handoff/SKILL.md
    ├── ai-prd-reviewer/SKILL.md
    ├── ai-ux-review/SKILL.md
    ├── agent-fit-analyzer/SKILL.md
    └── badcase-diagnosis/SKILL.md
```

## 真实案例

项目包含基于真实 AI 项目“名人智囊团”的评审案例，用来展示 skills 的实际工作方式：

- `examples/ai-ux-review-celebrity-council-v2.md`：使用 `ai-ux-review` 评估 AI 产品体验是否成立。
- `examples/ai-prd-review-celebrity-council.md`：使用 `ai-prd-reviewer` 审查真实项目 PRD/SDD 是否清楚、可落地、可评测、可交接。
- `examples/agent-fit-analysis-celebrity-council.md`：使用 `agent-fit-analyzer` 判断真实项目是否适合做 Full Agent、Copilot、workflow 或局部 agentic step。
- `examples/badcase-diagnosis-celebrity-council.md`：使用 `badcase-diagnosis` 诊断真实项目中的高风险建议、角色失真和黄金评测集坏案例。
- `examples/badcase-diagnosis-celebrity-council-simulated.md`：使用 `badcase-diagnosis` 评测一条模拟真实使用场景的名人智囊团 bad case。
- `examples/ai-coding-handoff-celebrity-council.md`：使用 `ai-coding-handoff` 把 PRD 评审和 bad case 诊断转成 AI Coding 可执行任务包。

## 当前状态

当前处于 v0.2 初稿阶段，5 个首版 skills 已完成第一版，并都配套了名人智囊团真实项目案例。

## 开源协议

本项目使用 MIT License。
