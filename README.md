<div align="center">

# 你好，我是 Yufei 👋

### AI Agent 工程 · Agent 基础设施 · LLM 评测与推理部署

[![GitHub](https://img.shields.io/badge/GitHub-fei121-181717?logo=github&logoColor=white)](https://github.com/fei121)
[![Focus](https://img.shields.io/badge/Focus-AI%20Agent-6C63FF)](https://github.com/fei121)
[![Python](https://img.shields.io/badge/Python-工程实践-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![C++](https://img.shields.io/badge/C%2B%2B-20-00599C?logo=cplusplus&logoColor=white)](https://isocpp.org/)

</div>

## 关于我

我主要关注 **AI Agent 的工程化落地**：从 ReAct 推理循环、工具发现与检索，到领域文档理解、质量评测、上下文管理和服务化部署。

除了 Agent 应用，我也持续实践支撑 Agent 落地的 **LLM 评测与 AI Infra**，包括联网搜索评测、模型量化、vLLM 推理部署与性能分析。我的项目强调可运行、可评测、可观测和可复现，而不只停留在 Demo。

## 能力地图

| 方向 | 工程实践 |
| --- | --- |
| **Agent 系统** | ReAct、多跳检索、工具调用、证据验证、运行时降级与上下文保护 |
| **Agent 基础设施** | OpenAPI 工具知识库、MCP、混合检索、长期记忆与上下文压缩 |
| **领域智能服务** | PDF / OCR 文档理解、Schema 驱动抽取、保险条款与理赔材料结构化 |
| **评测与可观测性** | 参数扫描、规则评测、LLM-as-a-Judge、Pareto 分析、Langfuse |
| **AI Infra** | 后训练量化、vLLM / TensorRT-LLM 部署、吞吐与尾延迟分析 |
| **系统工程** | C++20、位精确计算、CMake、跨平台 CI 与穷举验证 |

## Agent 应用

### [DeepResearch](https://github.com/fei121/DeepResearch) — 深度检索 Agent

- 基于 ReAct 循环完成问题拆解、搜索规划、网页阅读、证据提取与多源交叉验证。
- 支持中英文双搜索源路由、弱结果自动降级、SSE 心跳，以及超时、轮次和上下文预算保护。

### [ClauseMind](https://github.com/fei121/ClauseMind) — 保险条款智能拆解

- 将保险条款 PDF 转换为可计算的结构化责任数据，覆盖责任范围、等待期、既往症和责任免除等字段。
- 组合 PDF 解析、Markdown 结构化、FAISS / BM25 混合检索、LangGraph 工作流、字段级置信度与缓存机制。

### [ClaimDoc](https://github.com/fei121/ClaimDoc) — 理赔文档理解与结构化

- 面向发票、身份证、银行卡和病历等理赔材料，提供 OCR + LLM 的统一结构化 API。
- 支持 JSON Schema 驱动的通用字段抽取、专用字段校验、病历与发票匹配，以及可插拔 OCR 路由。

## Agent 基础设施

### [Agent-Tool-Index](https://github.com/fei121/Agent-Tool-Index) — Agent 工具发现中间服务

- 将多个系统的 OpenAPI 文档构建为统一工具知识库，让 Agent 先搜索候选 API，再按需获取完整文档。
- 提供向量检索、SQLite FTS5 BM25、跨知识库融合排序、证据片段回查，以及 MCP / HTTP 接口。
- 服务边界止于“发现工具并返回文档”，实际业务 API 仍由 Agent 调用。

## Agent 评测

### [LLM-SearchEval](https://github.com/fei121/LLM-SearchEval) — LLM 联网搜索评测框架

- 评估模型是否正确触发搜索、引用是否可追溯、信息是否具备时效性，并记录延迟、Token 和搜索次数。
- 支持参数扫描、规则指标、双 LLM Judge、人工复核分流、Pareto 权衡分析和科研风格可视化。

## 开源贡献

### [TencentDB-Agent-Memory](https://github.com/fei121/TencentDB-Agent-Memory)

- 参与腾讯云开源 Agent Memory 项目，关注本地长期记忆、符号化短期记忆与分层信息组织。
- 提交的 [PR #174：align config default comments](https://github.com/TencentCloud/TencentDB-Agent-Memory/pull/174) 已合并至上游主分支。

## AI Infra 实验

### [Qwen3-8B-Quantization](https://github.com/fei121/Qwen3-8B-Quantization) — 后训练量化与误差归因

- 对比 vLLM + LLM Compressor、AutoRound + vLLM、TensorRT-LLM + ModelOpt 三条量化与部署链路。
- 在统一 GSM8K / C-Eval 口径下评测 BF16、INT8 与 MXFP4，并通过 hidden-state cosine、SQNR 和模块消融定位量化误差。
- vLLM INT8 W8A8 输出吞吐从 **261 tokens/s** 提升至 **1,085 tokens/s**，同时保持接近 BF16 的评测精度。

### [Qwen3.6-PRO6000-vLLM-Benchmark](https://github.com/fei121/Qwen3.6-PRO6000-vLLM-Benchmark) — vLLM 部署实验

- 在相同 300 请求、20 并发、4K 输入 / 1K 输出负载下，对比 RTX PRO 6000 单卡与双卡部署。
- 双卡输出吞吐提升 **38.4%**、P99 TTFT 从 **6.28 s** 降至 **1.85 s**，并分析扩展效率与 GPU 成本权衡。

## C++ / 系统工程

### [GammaVRR](https://github.com/fei121/GammaVRR) — 位精确 C++ Golden Model

- 使用 C++20 实现刷新率等级相关 Gamma 补偿的软件参考模型，覆盖定点插值、舍入、饱和与旁路语义。
- 提供 C / C++ 接口、CMake 构建、跨平台 CI，并对 **1,572,864** 种像素、等级和通道组合进行独立数值验证。

## 技术栈

<p align="left">
  <img src="https://skillicons.dev/icons?i=py,cpp,pytorch,fastapi,docker,sqlite,linux,git,cmake" alt="Python, C++, PyTorch, FastAPI, Docker, SQLite, Linux, Git, CMake" />
</p>

<p>
  <img src="https://img.shields.io/badge/LangGraph-Agent%20Workflow-1C3C3C" alt="LangGraph" />
  <img src="https://img.shields.io/badge/MCP-Agent%20Tools-7357FF" alt="MCP" />
  <img src="https://img.shields.io/badge/vLLM-推理部署-00A67E" alt="vLLM" />
  <img src="https://img.shields.io/badge/TensorRT--LLM-推理加速-76B900?logo=nvidia&logoColor=white" alt="TensorRT-LLM" />
  <img src="https://img.shields.io/badge/Langfuse-可观测性-F7B955" alt="Langfuse" />
</p>

## 当前关注

- 构建可靠、可评测、可观测的 AI Agent 系统。
- 优化 Agent 的工具发现、知识检索、记忆与上下文使用效率。
- 将模型能力沉淀为可复现、可部署的工程服务。

## 联系方式

欢迎通过 [GitHub @fei121](https://github.com/fei121) 交流 AI Agent、LLM 评测、推理部署与开源工程实践。
