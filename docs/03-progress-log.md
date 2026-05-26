# Progress Log

## 2026-05-26

### 已完成

- 确认项目方向：AIPM Core Skills。
- 确认首版只做 5 个核心 skills。
- 确认暂不做 RAG，避免进入 owner 当前不熟悉的深技术区。
- 创建项目文档系统。
- 创建 `AGENTS.md` 作为项目核心协作文件。
- 创建 `docs/` 目录。
- 创建 `skills/` 目录。
- 创建 5 个 skill 的 `SKILL.md` 占位文件。
- 调研 `ai-ux-review` 相关竞品，包括通用 UI/UX skill、vibe-coded website review、AI UX auditor 和综合 UX toolkit。
- 创建 `docs/06-competitor-research-ai-ux-review.md`。
- 补全 `skills/ai-ux-review/SKILL.md` 初稿，加入 YAML frontmatter、6 维审查框架、输出模板、质量标准和示例。
- 使用名人智囊团项目跑通 `ai-ux-review`，并创建案例报告 `examples/ai-ux-review-celebrity-council.md`。
- 根据 owner 反馈升级 `ai-ux-review` 输出颗粒度：结论必须详拆，建议必须可执行，并补充负责人、落地位置、验收标准和 7 天执行清单。
- 根据 owner 反馈重构 `ai-ux-review` 方法论：从风险审查升级为通用 AI 产品体验评估框架，新增产品类型识别、核心体验承诺和 8 层体验评估。
- 将新版名人智囊团评估结果保存为 `examples/ai-ux-review-celebrity-council-v2.md`，供后续修改项目时参考。
- 调研 `ai-prd-reviewer` 相关竞品，包括 PRD 生成器、Claude Code PRD skill、Taskmaster PRD、AI-ready PRD 商业工具。
- 创建 `docs/07-competitor-research-ai-prd-reviewer.md`。
- 补全 `skills/ai-prd-reviewer/SKILL.md` 初稿，定位为 AI PRD 审查器，而不是 PRD 生成器。
- 使用名人智囊团现有 `CLAUDE.md`、`docs/SDD.md`、`docs/API.md`、`docs/DECISIONS.md` 跑通 `ai-prd-reviewer`，并创建案例报告 `examples/ai-prd-review-celebrity-council.md`。
- 将 `examples/ai-prd-review-celebrity-council.md` 补成可开源发布的真实项目案例说明，用来展示 `ai-prd-reviewer` 的实际审查能力。
- 将 `examples/ai-ux-review-celebrity-council-v2.md` 补成可开源发布的真实项目案例说明，用来展示 `ai-ux-review` 的实际体验评估能力。
- 确认后续第 3、4、5 个 skill 都采用“skill + 真实项目案例”的发布方法论。
- 调研 `agent-fit-analyzer` 相关竞品和公开方法论，包括 Agent vs Workflow、Human-in-the-loop、Agentic UX、Workspace Agents。
- 创建 `docs/08-competitor-research-agent-fit-analyzer.md`。
- 补全 `skills/agent-fit-analyzer/SKILL.md` 初稿，定位为 Agent 适配性判断器，而不是 Agent 编排器。
- 使用名人智囊团跑通 `agent-fit-analyzer`，并创建真实项目案例 `examples/agent-fit-analysis-celebrity-council.md`。
- 根据 owner 反馈调整 `agent-fit-analyzer`：强调先判断产品目标和用户任务，再判断 Agent 必要性；不混入项目级 skill 自检方法论。
- 调研 `badcase-diagnosis` 相关竞品和相邻实践，包括 Langfuse、Opik、OpenAI Evals、DeepEval、OpenEvals、Future AGI、RagaAI Catalyst 和 cane-eval。
- 创建 `docs/09-competitor-research-badcase-diagnosis.md`。
- 补全 `skills/badcase-diagnosis/SKILL.md` 初稿，定位为 AI 产品 bad case 复盘器，而不是工程 eval 平台。
- 使用名人智囊团的 SDD、API 文档、决策记录和黄金评测集跑通 `badcase-diagnosis`，并创建真实项目案例 `examples/badcase-diagnosis-celebrity-council.md`。
- 调研 `ai-coding-handoff` 相关竞品和相邻实践，包括 Claude Task Master、spec-driven development、PRD TaskMaster、AIF handoff、project memory 和 session governance。
- 创建 `docs/10-competitor-research-ai-coding-handoff.md`。
- 补全 `skills/ai-coding-handoff/SKILL.md` 初稿，定位为 AI PM 到 AI Coding 的任务交接器，而不是任务管理系统。
- 基于名人智囊团的 PRD 评审与 bad case 诊断结果，创建真实项目交接案例 `examples/ai-coding-handoff-celebrity-council.md`。
- 根据 owner 反馈，明确名人智囊团当前还没有线上真实 bad case，因此新增一份“模拟真实使用场景”的 bad case 评测报告：`examples/badcase-diagnosis-celebrity-council-simulated.md`。

### 当前状态

项目处于 v0.2 初稿阶段，5 个首版 skills 已完成第一版，其中 5 个都已配套名人智囊团真实项目案例。

### 下一步

整体复查 5 个 skills 的一致性，随后准备开源前 README、案例索引和安装说明。
