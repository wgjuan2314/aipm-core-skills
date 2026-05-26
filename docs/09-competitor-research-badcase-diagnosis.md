# Competitor Research: badcase-diagnosis

调研日期：2026-05-26

## 目标

为 `badcase-diagnosis` 找到可参考的竞品和相邻实践，判断它应该避开什么、补什么空位。

本 skill 不做大型 LLM eval 平台，也不做 RAG 深水区诊断。它更像 AI 产品经理的 bad case 复盘表：把一次失败输出拆成产品规则、prompt 修改、体验改动和回归测试。

## 参考项目

| 项目 | 当前 star | 定位 | 可借鉴点 | 对本项目的启发 |
| --- | ---: | --- | --- | --- |
| [langfuse/langfuse](https://github.com/langfuse/langfuse) | 27939 | LLM observability、evals、prompt management、datasets | 生产观测、prompt 管理、数据集闭环 | bad case 不能只靠主观感觉，应该沉淀为可复测样本。 |
| [comet-ml/opik](https://github.com/comet-ml/opik) | 19376 | LLM 应用调试、评估、监控 | tracing、自动评估、dashboard | 工程平台会记录链路，本 skill 负责把链路问题翻译成 PM 可执行判断。 |
| [openai/evals](https://github.com/openai/evals) | 18534 | LLM / LLM system evaluation framework | benchmark registry、系统化评测 | 坏案例最终应该进入 golden set，而不是只停留在一次复盘。 |
| [raga-ai-hub/RagaAI-Catalyst](https://github.com/raga-ai-hub/RagaAI-Catalyst) | 16168 | Agent observability、monitoring、evaluation | timeline、execution graph、multi-agent debugging | 多步骤 AI 产品需要定位“哪一步坏了”，不能只看最终答案。 |
| [confident-ai/deepeval](https://github.com/confident-ai/deepeval) | 15701 | LLM evaluation framework | answer relevance、hallucination、task completion 等指标 | 可以借鉴指标思维，但本项目要保持小白友好，不做复杂工程接入。 |
| [langchain-ai/openevals](https://github.com/langchain-ai/openevals) | 1063 | ready-made evaluators for LLM apps | LLM-as-judge、结构化评估器 | 说明通用 evaluator 已经很多，AIPM 的机会在“产品化诊断语言”。 |
| [future-agi/future-agi](https://github.com/future-agi/future-agi) | 1045 | eval、observability、simulation、guardrails | 从 eval 到 guardrail 的闭环 | bad case 诊断应该产出 guardrail/产品规则，而不是只写问题。 |
| [colingfly/cane-eval](https://github.com/colingfly/cane-eval) | 5 | reliability eval、schema validation、failure mining、root cause analysis | failure mining、root cause analysis | 直接证明“失败挖掘 + 根因分析”是一个新兴方向，但多数项目偏工程。 |

## 竞品空位

现有开源项目大多偏工程平台：

- 需要接入 SDK、日志、tracing、dashboard。
- 适合工程团队做持续监控。
- 输出通常是分数、trace、metric、dataset。

但 AI 产品经理常见的问题是：

- 手里只有一个坏输出，不知道怎么拆。
- 不知道这是 prompt 问题、产品规则问题，还是体验流程问题。
- 不知道哪些坏案例值得进 golden set。
- 不知道怎么把坏案例变成 PRD、prompt 或 AI Coding 任务。

`badcase-diagnosis` 的机会就是填这个空位。

## 本 skill 的差异化

`badcase-diagnosis` 不追求做技术平台，而是追求：

- 输入低门槛：一段用户输入 + AI 输出即可开始。
- 输出产品化：直接给 PRD 文本、prompt 修改、体验改动、AI Coding 任务。
- 诊断分层：输入、意图、事实、推理、角色、格式、流程、安全、评测。
- 面试可讲：体现 owner 能把“AI 不好用”拆成系统性产品问题。
- 与前两个 skill 互补：`ai-ux-review` 看整体体验，`ai-prd-reviewer` 看文档完整性，`badcase-diagnosis` 看单个失败案例。

## 对名人智囊团的启发

名人智囊团有天然的 bad case 来源：

- 黄金评测集里已有“盲测未命中”“立场一致性低”“论证路径低”的样本。
- 当前 prompt 存在“直接给观点，不要说免责声明”的约束，高风险决策场景需要重新定义边界。
- 多角色流程里，某一位名人输出弱，会影响后续辩论和主持人汇总。
- 最终汇总如果只是折中复述，而不是提炼真正分歧，核心体验会被削弱。

因此第四个 skill 可以直接拿真实项目跑出一个有说服力的案例。
