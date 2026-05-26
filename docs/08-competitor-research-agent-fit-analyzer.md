# Competitor Research: agent-fit-analyzer

调研日期：2026-05-26

## 调研目标

为第三个 skill `agent-fit-analyzer` 调研 GitHub 和公开资料中的 Agent / Workflow / Human-in-the-loop / Agentic UX 相关竞品与方法论，判断已有项目覆盖了什么，以及我们的差异化机会在哪里。

## 主要发现

GitHub 上直接叫 `agent-fit-analyzer` 或专门面向 AI PM 的 Agent 适配性判断 skill 很少。现有内容更多集中在：

- Agent 框架。
- 多 Agent 编排。
- Agentic workflow demo。
- Agent vs Workflow 方法论文章。
- Human-in-the-loop 设计模式。
- Agentic UX pattern library。

## 主要参考

| 来源 | 形态 | 主要观点 | 对我们的启发 |
| --- | --- | --- | --- |
| OpenAI Workspace Agents | 官方文章 | Agent 支持依赖共享系统、标准交接、稳定输出和真实业务约束的重复工作流。 | Agent 不是聊天壳子，而是围绕真实工作流推进任务。 |
| Retool AI workflows vs agents | 方法论文章 | Copilot、workflow、agent 的边界在于实时适应、工具调用和流程自动化程度。 | 需要帮助 PM 判断应该做 Copilot、workflow 还是 Agent。 |
| Agentic UX Patterns | pattern library | Agent 体验要重视信任、记忆、个性化、数据使用和控制感。 | Agent 适配不只是技术，也要看用户是否能理解和控制。 |
| Multi-Agent Wiki: Human-in-the-loop | 设计模式 | 高风险操作需要人工确认、权限边界和可审计。 | 判断 Agent 是否成立时必须检查人工确认点。 |
| Agents vs Workflows 相关文章 | 方法论文章 | 如果步骤可预定义，workflow 往往比 agent 更稳定；agent 适合动态决策和未知路径。 | 我们的 skill 应该反过来防止过度 agent 化。 |
| Agentic AI 风险文章 | 行业分析 | Agent 一旦作用于真实业务流程，错误成本和治理要求显著升高。 | 产品经理必须评估失败成本、权限、日志、回滚和数据基础。 |

## 竞品共性

- 大量项目在教人如何构建 Agent，但很少教人判断“是否应该做 Agent”。
- 公开文章普遍强调 agent 与 workflow 的区别，但面向产品经理的可执行框架较少。
- 很多 Agent demo 忽略权限、失败成本、人工确认、日志和回滚。
- Human-in-the-loop 经常被简化成最后一个“批准”按钮，但真正的 Agent 产品需要多个关键确认点。

## 竞品空位

现有竞品较少系统覆盖：

- 一个需求到底适合普通 AI、Copilot、workflow、agentic step，还是 full agent。
- 如何从产品价值角度判断 Agent 是否有必要。
- 如何防止“为了热点而 Agent 化”。
- 如何评估任务不确定性、动态决策需求、自主执行价值。
- 如何评估写入、删除、支付、发布、部署等真实动作的风险。
- 如何输出可直接补进 PRD 的 Agent 形态建议。

## 我们的定位

`agent-fit-analyzer` 不做 Agent 编排器，也不写工具调用代码，而是做：

> Agent 适配性判断器：帮助 AI 产品经理判断一个需求是否真的需要 Agent，以及更轻量、更安全的产品形态是什么。

它更适合体现 AI PM 能力，因为真正的产品判断不是把所有需求包装成 Agent，而是知道什么时候该用：

- 普通 AI 功能。
- AI 助手 / Copilot。
- 确定性工作流。
- 工作流 + agentic step。
- Human-in-the-loop Agent。
- Full Agent。

