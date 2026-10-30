# AI Agent 岗位 7 天学习路线

## 目标
在 7 天内，快速建立 AI Agent 相关知识框架，补足面试和项目需要的核心能力，重点是：
- LLM / Agent 基础
- RAG
- Tool Calling
- Agent 编排
- Memory / State
- Eval / Observability
- 项目表达能力

这个路线适合：
- Java 后端工程师
- 有 AI 使用经验，但没有系统化 AI Agent 实战经验
- 想尽快准备 AI Agent 岗位面试

---

## Day 1：LLM 与 Agent 基础认知

### 学习重点
- LLM 是什么
- Transformer 的核心思想
- Prompt 是什么
- Hallucination 是什么
- Agent 与聊天机器人区别
- ReAct / Plan-Act / Tool Use
- Agent 的典型架构

### 学习任务
1. 读 2 篇 AI Agent 入门文章
2. 了解什么是：
   - Prompt
   - Context
   - Temperature
   - Top-p
   - Hallucination
3. 记住这几个概念：
   - Agent = 可规划 + 可调用工具 + 可执行任务
   - Chatbot = 任务式问答
   - Agent = 任务执行系统

### 输出要求
写一篇 300-500 字的笔记，回答：
- 什么是 Agent？
- 它和普通聊天机器人有什么区别？
- 为什么复杂任务不能只靠一次模型回答？

### 面试准备
准备 3 个高频问题：
- 什么是 Agent？
- Agent 和聊天机器人有什么区别？
- 为什么 Agent 需要工具？

---

## Day 2：RAG 与知识库基础

### 学习重点
- RAG 是什么
- 检索与生成的关系
- Embedding
- 向量数据库
- Chunking
- 检索召回
- 重排
- 文档知识库问答

### 学习任务
1. 学会理解 RAG 流程：
   - 文档入库
   - 分块
   - embedding
   - 向量检索
   - 重排
   - 生成回答
2. 熟悉常用组件：
   - Qdrant
   - pgvector
   - Milvus（了解即可）
3. 写一个最简单的 RAG 流程说明图

### 输出要求
绘制一张流程图：
- 用户提问
- 检索
- 召回
- LLM 生成
- 输出答案

### 面试准备
准备 3 个问题：
- 什么是 RAG？
- RAG 与微调的区别是什么？
- 你如何看待向量数据库在知识库中的作用？

---

## Day 3：Tool Calling 与 Agent 编排

### 学习重点
- Tool Calling / Function Calling
- Agent 调工具的模式
- 任务规划
- 多步骤执行
- 状态管理
- LangGraph / AutoGen / CrewAI 的概念

### 学习任务
1. 学一个 Agent 框架：
   - 优先推荐 LangGraph
   - 了解 AutoGen / CrewAI 也可以
2. 试着写一个最小 Agent：
   - 用户输入问题
   - 调用一个工具（例如搜索、查询、文档获取）
   - 再生成回答
3. 理解“多步任务”与“状态机”概念

### 输出要求
写一段说明：
- 一个 Agent 为什么要调用工具？
- 什么时候需要规划？
- 为什么复杂任务不能一次性回答？

### 面试准备
准备 3 个问题：
- 什么是 Tool Calling？
- Agent 为什么需要状态？
- 什么是多步任务编排？

---

## Day 4：Memory 与 Session Management

### 学习重点
- Short-term memory
- Long-term memory
- 会话状态
- 用户偏好记忆
- 工作流状态
- Agent 的“任务状态”管理

### 学习任务
1. 理解会话状态管理的重要性
2. 学习通过：
   - session 表
   - memory store
   - vector memory
   - task state
   来管理状态
3. 做一个简单的状态图

### 输出要求
做一个状态流图：
- NEW
- PLANNING
- TOOL_CALLING
- EVALUATING
- NEED_CONFIRMATION
- DONE

### 面试准备
准备 3 个问题：
- Agent 为什么需要 Memory？
- 短期记忆和长期记忆有什么区别？
- 复杂任务如何维持状态？

---

## Day 5：评估（Evaluation）与观测性（Observability）

### 学习重点
- Agent 评估标准
- 回答准确性
- 任务完成率
- Tool 调用成功率
- 成本控制
- 延迟
- Hallucination rate
- Trace / Logging / Monitoring

### 学习任务
1. 理解 Agent 的评估维度
2. 掌握这几个指标：
   - correctness
   - tool success rate
   - latency
   - cost
   - task completion rate
3. 学习 trace 思路：
   - 每一步调用日志
   - 用户输入
   - 模型输出
   - 工具结果
   - 错误和重试

### 输出要求
写一份 Agent 评估清单，包括：
- 正确率
- 完成率
- 成本
- 延迟
- 安全性

### 面试准备
准备 3 个问题：
- 你如何评估 Agent 的效果？
- 如何追踪一次 Agent 请求的每一步？
- Agent 怎样做失败定位？

---

## Day 6：一个最小可用 Agent 项目

### 目标
做一个“最小可用”的 Agent 项目，作为面试展示

### 推荐项目
企业知识库问答 Agent
- 用户输入问题
- Agent 检索文档
- 检索到答案
- 输出答案 + 来源
- 记录 trace
- 支持多轮对话

### 技术栈建议
- Python
- FastAPI
- LangGraph
- Postgres
- Qdrant
- Redis
- Docker

### 任务
1. 完成一个最小 demo
2. 文档入库
3. 接入向量检索
4. 做一次工具调用
5. 增加日志 trace
6. 准备 5 分钟项目介绍

### 输出要求
准备一份项目介绍文档，结构如下：
- 背景
- 目标
- 架构
- 技术栈
- 关键流程
- 难点
- 优化方向

---

## Day 7：面试刷题 + 项目讲解准备

### 学习重点
- 高频面试题回答
- 项目讲解
- 系统设计表达
- 自我定位

### 学习任务
1. 复习 Day 1-5 的知识点
2. 练习 10 个高频面试题
3. 准备项目讲解稿，时长 5-8 分钟
4. 准备自我介绍语：
   - 你现在的背景
   - 你为什么转向 AI Agent
   - 你做过什么
   - 你想学什么

### 输出要求
准备以下内容：
- 1 份高频题答案清单
- 1 份项目讲解稿
- 1 份 1 分钟自我介绍

### 面试准备
核心问题：
- 你为什么会做 AI Agent？
- 你做过哪些 AI 相关工作？
- 你最擅长什么？
- 你最弱的地方是什么？
- 你怎么把 Java 业务经验转成 AI Agent 能力？

---

## 7 天学习结果目标

### 你应该具备的能力
- 能解释 Agent 与聊天机器人区别
- 能说明 RAG 的核心流程
- 能说明 Tool Calling 的意义
- 能解释 Memory / State 管理
- 能说出 Agent 评估维度
- 能讲一个最小可用的 Agent 项目
- 能回答 AI Agent 高频面试题

### 你应该形成的思维方式
- 把 AI 当工程系统，而不是黑盒模型
- 把工具、状态、评测和安全当作核心
- 把模型能力与工程约束统一考虑

---

## 7 天建议学习资源

### 必看
- LangGraph 官方文档
- LangChain 官方文档
- OpenAI Function Calling 文档
- Anthropic Claude Tools 文档
- RAG 入门教程（快速看）
- AI Agent 设计相关文章

### 必做
- 做一个最小的 RAG demo
- 做一个最小的 Tool Calling Agent
- 做一个最小的知识库问答 Agent
- 学会讲清楚架构和设计决策

---

## 7 天重点提醒

### 先学“工程”，再学“炫技”
不要只停留在：
- 写 prompt
- 调 API
- 看大模型 demo

你真正需要的是：
- 架构
- 工程
- 状态
- 日志
- 评估
- 安全
- 业务落地

---

## 最终目标
7 天后，你至少应该像一个“具备 AI 工程思维的 Java 工程师”，而不是“只会调模型的人”。

如果你能在面试中说出：
- Agent 是什么
- Tool 调用是什么
- RAG 怎么做
- 为什么需要状态管理
- 如何评估 Agent
- 你做过一个真实项目

那你已经具备非常强的竞争力。

---

## 你可以直接执行的 7 天任务清单

### Day 1
- 读 1 篇 Agent 入门
- 写 1 篇 Agent 笔记

### Day 2
- 看 1 篇 RAG 文章
- 写 1 份 RAG 流程图

### Day 3
- 学 LangGraph
- 写一个最小 Agent demo

### Day 4
- 理解 Memory 和 状态机
- 画状态图

### Day 5
- 学评估与 trace
- 写评估清单

### Day 6
- 做最小项目
- 写项目说明

### Day 7
- 练习面试题
- 练习 5-8 分钟项目介绍
- 练习自我介绍

---

如果你愿意，我下一步可以继续给你：
- “AI Agent 面试回答模板（5 分钟版本）”
- “AI Agent 项目脚手架代码（Python + LangGraph）”
- “AI Agent 学习资源清单（按优先级）”

你只要回复其中一个关键词即可。