---
name: ai-coding-handoff
description: Use this skill to convert a product idea, PRD gap, UX review finding, bad case diagnosis, or feature request into a task packet that Codex, Claude Code, Cursor, Copilot coding agent, or another AI coding tool can implement safely. It produces scoped implementation tasks, relevant files, constraints, acceptance criteria, test plan, non-goals, and human decisions required before coding.
---

# ai-coding-handoff

## 使用场景

当你已经有产品想法、PRD、UX 评审结论、bad case 诊断或功能描述，希望交给 Codex、Claude Code、Cursor 等 AI Coding 工具执行时，使用这个 skill。

它的目标不是直接写代码，而是把“产品语言”翻译成 AI Coding 不容易跑偏的任务包。

适合处理：

- 把 PRD 缺口拆成开发任务。
- 把 UX 评审建议拆成前端/交互任务。
- 把 bad case 修复拆成 prompt、规则、测试任务。
- 把 backlog 改写成 AI Coding 可执行 issue。
- 判断一个需求是否太大，需要拆成多轮。
- 明确哪些东西 AI 可以做，哪些必须 owner 决策。

## 输入材料

尽量提供：

- 产品目标。
- 用户场景。
- 要改的功能或问题。
- 当前表现和期望表现。
- 相关 PRD、SDD、设计稿、截图或代码路径。
- 技术栈和运行方式。
- 涉及页面、组件、接口、prompt 或数据文件。
- 必须保留的现有行为。
- 不希望 AI 改动的范围。
- 验收标准。
- 时间优先还是质量优先。

## 工作流程

### Step 1: 先判断任务是否适合交给 AI Coding

按三类判断：

- **可直接交给 AI Coding**：范围明确、涉及文件可定位、验收标准清楚。
- **需要先拆清楚**：目标明确，但缺少交互、数据、边界或验收标准。
- **不建议直接交给 AI Coding**：需求很大、产品方向未定、涉及高风险业务判断、需要真实用户研究或复杂架构决策。

### Step 2: 收敛任务范围

每个任务包只做一件事。

如果需求包含多个目标，要拆成：

- P0 必做任务。
- P1 可选增强。
- 暂不做事项。

### Step 3: 标出代码/文档落点

尽量写清楚：

- 可能涉及哪些文件。
- 需要先阅读哪些文档。
- 可能要新增哪些状态、字段、函数或 prompt 规则。
- 哪些文件只能读，不能乱改。

如果不知道文件路径，写“需要 AI 先搜索定位”，不要编造路径。

### Step 4: 写清实现约束

必须说明：

- 保留哪些现有行为。
- 不要重构哪些无关部分。
- 不要引入哪些复杂依赖。
- 是否允许改数据结构。
- 是否需要兼容历史记录。
- 是否需要小白可理解的注释或文档更新。

### Step 5: 写验收标准和测试计划

验收标准要能判断“做完没有”，不要只写“体验更好”。

推荐包含：

- 正常路径。
- 空状态。
- 错误状态。
- 边界输入。
- 回归场景。
- 人工检查点。

### Step 6: 输出任务包

任务包要能被复制到 Codex、Claude Code、Cursor、GitHub issue 或项目文档中。

## 输出格式

```markdown
# AI Coding Handoff

## 1. 交接结论

- 是否可直接交给 AI Coding：
- 建议执行方式：单任务 / 多任务 / 先澄清
- 风险等级：
- 一句话说明：

## 2. 背景与目标

- 产品背景：
- 用户问题：
- 本次目标：
- 不做什么：

## 3. 任务拆解

| 优先级 | 任务 | 目标 | 是否可直接执行 |
| --- | --- | --- | --- |

## 4. 推荐交给 AI Coding 的任务包

### Task 1: 任务名称

**目标**

**建议先阅读**

**可能涉及文件**

**实现要求**

**不要改动**

**验收标准**

**测试计划**

**完成后需要更新的文档**

## 5. 需要 owner 先确认的问题

## 6. 可直接复制给 AI Coding 工具的 Prompt
```

## 质量标准

好的输出应该：

- 先判断任务是否适合交给 AI Coding。
- 把大需求拆成小任务，而不是一次性交给 AI 写完整项目。
- 写清楚背景、范围、文件、约束、验收标准和测试计划。
- 明确“不做什么”，减少 AI 乱发挥。
- 能保护现有代码和用户已有改动。
- 能把产品判断翻译成开发语言。
- 能标出需要 owner 决策的地方。

差的输出通常表现为：

- 只写“请优化体验”。
- 任务过大，一次性要求改很多模块。
- 没有验收标准。
- 没有不做事项。
- 没有说明涉及文件和保留行为。
- 把产品方向决策交给 AI 自己拍脑袋。

## 示例：名人智囊团高风险问题兜底

输入：

> PRD 评审发现名人智囊团在“我要不要辞职创业”这类问题上缺少高风险边界，旧 prompt 里还有“直接给观点，不要说免责声明”。

输出应拆成：

- Task 1：增加高风险问题识别函数。
- Task 2：高风险问题下修改名人回答 prompt 附加规则。
- Task 3：修改主持人汇总 prompt，输出“关键变量、可选路径、小步验证”。
- Task 4：新增 golden set 测试样本。

每个 task 都要写清涉及文件、不要改动、验收标准和测试方式。

## 不适用场景

不适合用来：

- 替代完整架构设计。
- 自动决定产品方向。
- 自动选择全新技术栈。
- 一次性交接超大项目。
- 处理没有任何目标、输入、范围的模糊愿望。
- 绕过安全、隐私、合规或支付相关审查。
