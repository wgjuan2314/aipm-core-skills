# AGENTS.md

这是 AIPM Core Skills 项目的核心协作文件，作用类似 Claude Code 项目里的 `CLAUDE.md`。

任何后续进入本项目的 AI 助手，都应该先阅读本文件，再开始工作。

## 项目定位

AIPM Core Skills 是一套面向 AI 产品经理、AI 体验设计师和 AI Coding 实践者的开源 skills。

项目重点不是做通用提示词库，而是把 AI 产品经理的高频判断沉淀成可复用工作流，帮助使用者完成：

- AI 产品体验审查。
- AI PRD 审查。
- Agent 适用性判断。
- AI 失败案例复盘。
- AI Coding 任务交接。

## 当前阶段

当前阶段：v0.2 首版 skills 初稿完成。

本阶段目标：

- 复查 5 个首版 skills 的一致性。
- 优化 README、案例索引和安装说明。
- 准备 GitHub 开源展示。

## 首版范围

首版只做 5 个 skills：

1. `ai-ux-review`
2. `ai-prd-reviewer`
3. `agent-fit-analyzer`
4. `badcase-diagnosis`
5. `ai-coding-handoff`

暂不做：

- RAG 相关 skill。
- `agent-workflow-designer`。
- `ai-eval-set-builder`。
- 复杂代码工程、npm 包、自动化发布。

## 分工

项目 owner 负责：

- 提供真实项目素材。
- 判断 skill 是否符合真实 AI 产品经理工作场景。
- 决定项目定位、命名和个人品牌表达。
- 亲自运行 skill，并保留截图、录屏或使用记录。
- 在面试或作品集中讲述项目价值。

Codex 负责：

- 设计项目结构。
- 起草文档和 skill 初稿。
- 整理案例、示例和使用方式。
- 帮助把项目包装成 GitHub 可读的开源项目。
- 帮助准备面试讲法和作品集表达。

## 工作原则

- 中文为主，小白友好。
- 先做少而精，不追求大而全。
- 所有 skill 都要能解释清楚：解决什么问题、什么时候用、输入什么、输出什么、怎么判断好坏。
- 避免进入 owner 当前不熟悉的深技术区，尤其是 RAG。
- 文档要服务于后续持续推进，不写空泛口号。
- 面试可讲性优先，开源展示性其次，工程复杂度最后。

## Skill 文件规范

每个 `SKILL.md` 必须包含以下部分：

1. Skill 名称
2. 使用场景
3. 输入材料
4. 工作流程
5. 输出格式
6. 质量标准
7. 示例
8. 不适用场景

如果新增 skill，必须先更新：

- `docs/02-skill-roadmap.md`
- `docs/04-decisions.md`

## 后续协作提醒

每次开始新任务时，先查看：

1. `docs/03-progress-log.md`
2. `docs/02-skill-roadmap.md`
3. 当前要修改的 skill 文件

每次完成阶段性工作后，更新：

1. `docs/03-progress-log.md`
2. 必要时更新 `docs/04-decisions.md`
3. 必要时更新 `README.md`

## 当前成果

截至 2026-05-26，5 个首版 skills 均已完成第一版，并都配套了名人智囊团真实项目案例：

- `ai-ux-review`
- `ai-prd-reviewer`
- `agent-fit-analyzer`
- `badcase-diagnosis`
- `ai-coding-handoff`
