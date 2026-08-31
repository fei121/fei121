<div align="center">

# 你好，我是 Yufei 👋

### AI Agent 工程 · LLM 算法 · 推理优化

[![GitHub](https://img.shields.io/badge/GitHub-fei121-181717?logo=github&logoColor=white)](https://github.com/fei121)
[![Focus](https://img.shields.io/badge/Focus-Agent%20Engineering-6C63FF)](#精选项目)
[![Python](https://img.shields.io/badge/Python-Engineering-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![C++](https://img.shields.io/badge/C%2B%2B-20-00599C?logo=cplusplus&logoColor=white)](https://isocpp.org/)

</div>

## 个人概述

- **Agent开发**：具身型Agent（FangOS，Forklift，[Agent-Tool-Index](https://github.com/fei121/Agent-Tool-Index)），业务型Agent（[ClauseMind](https://github.com/fei121/ClauseMind)、[ClaimDoc](https://github.com/fei121/ClaimDoc)）、研究型Agent（[DeepResearch](https://github.com/fei121/DeepResearch)）
- **LLM量化、推理、评测**：搭建联网搜索评测Pipeline；完成 Qwen3-8B 多量化链路对照与误差归因，vLLM INT8 输出吞吐由 **261 提升至 1,085 tokens/s**。([Qwen3-8B Quantization Lab](https://github.com/fei121/Qwen3-8B-Quantization))
- **LLM部署分析**：在统一负载下评测qwen3.6-35b-a3b-fp8在 RTX PRO 6000 单卡/双卡 vLLM 服务，双卡输出吞吐提升 **38.4%**，P99 TTFT 从 **6.28 s 降至 1.85 s**。([Qwen3.6 × RTX PRO 6000](https://github.com/fei121/Qwen3.6-PRO6000-vLLM-Benchmark))
- **算法研究**：熟悉LLM、NLP、CV算法，以第一作者在 *IEEE Robotics and Automation Letters* 发表视觉算法论文；([Paper](https://doi.org/10.1109/LRA.2026.3707344))
- **工程项目**：为显示芯片做补偿验证，使用 C++精确 Golden Model，并完成 **1,572,864** 组穷举验证。([RefreshTone](https://github.com/fei121/RefreshTone))

## 精选项目

### 🛡️ [ClauseMind](https://github.com/fei121/ClauseMind) · 保险条款智能拆解

将保险条款 PDF 转换为可计算的结构化责任数据，覆盖责任范围、等待期、既往症与责任免除等关键字段。组合 PDF / OCR 解析、FAISS + BM25 混合检索、LangGraph 工作流、字段级置信度，以及 OSS / MySQL / Redis 缓存链路。

`Document AI` `Hybrid Retrieval` `LangGraph` `Confidence Scoring` `FastAPI`

### 🧾 [ClaimDoc](https://github.com/fei121/ClaimDoc) · 理赔文档理解与结构化

面向发票、身份证、银行卡和病历等理赔材料，提供 OCR + LLM 的统一结构化 API。支持 JSON Schema 驱动的通用字段抽取、专用字段校验、病历与发票匹配，以及可插拔 OCR 路由。

`OCR + LLM` `JSON Schema` `Field Validation` `Document Matching` `FastAPI`

### 🔎 [DeepResearch](https://github.com/fei121/DeepResearch) · 深度检索 Agent

面向复杂问题自主完成拆解、搜索规划、网页阅读、证据提取与多源交叉验证。基于 ReAct 构建动态推理循环，并为弱搜索结果、网页访问失败、超时、轮次和上下文预算设计完整降级路径。

`ReAct` `Multi-hop Search` `Evidence Verification` `FastAPI` `SSE`

### 🧰 [Agent-Tool-Index](https://github.com/fei121/Agent-Tool-Index) · Agent 工具检索平台

把多个系统的 OpenAPI 文档构建为统一工具知识库，让 Agent 从“预先加载所有工具”转向“先检索、再按需读取”。支持向量检索 + SQLite FTS5 BM25、跨知识库融合排序、完整文档回查，以及 MCP / HTTP 接入。

`OpenAPI` `Hybrid Retrieval` `MCP` `SQLite FTS5` `Python`



## 更多工程实践

| 项目 | 解决的问题 | 值得看的工程点 |
| --- | --- | --- |
| [Qwen3-8B Quantization Lab](https://github.com/fei121/Qwen3-8B-Quantization) | 对比量化与部署链路并定位精度损失来源 | vLLM / TensorRT-LLM、INT8 / MXFP4、SQNR、模块消融与性能分析 |
| [LLM-SearchEval](https://github.com/fei121/LLM-SearchEval) | 评估模型何时搜索、引用是否可靠、信息是否及时 | 参数扫描、双 LLM Judge、人工复核分流、Pareto 分析、Langfuse |
| [Qwen-Infer](https://github.com/fei121/Qwen-vLLM-Benchmark) | 用vLLM 推理Qwen系列，分析单卡多卡性能 | 统一负载、吞吐/尾延迟分析、扩展效率与 GPU 成本权衡 |
| [RefreshTone](https://github.com/fei121/RefreshTone) | 为刷新率相关 Gamma 补偿提供软件参考实现 | C++20 位精确计算、C API、CMake、跨平台 CI、穷举数值验证 |

## 研究与开源

### 📄 [UniFormer-Based Dual Quaternion Network for Visual Odometry](https://doi.org/10.1109/LRA.2026.3707344)

**Yufei Feng**, Chang Xu, Chenggui Yao, Bailu Si, Changgui Gu, Dongping Yang<br>
*IEEE Robotics and Automation Letters*, 2026

将 UniFormerV2、单位双四元数流形、可微 QCQP 求解器与 Rotation-Guided Transformer 组合，在统一几何表示中联合建模旋转和平移，并在 KITTI、TUM、ZJH-VO、4Seasons 与 EuRoC 上完成验证。

### 🤝 [TencentDB-Agent-Memory](https://github.com/fei121/TencentDB-Agent-Memory)

参与腾讯云开源 Agent Memory 项目；提交的 [PR #174：align config default comments](https://github.com/TencentCloud/TencentDB-Agent-Memory/pull/174) 已合并至上游主分支。

## 技术栈

**Agent / LLM** · ReAct · LangGraph · MCP · RAG · LLM-as-a-Judge · Langfuse<br>
**Serving / Infra** · vLLM · TensorRT-LLM · PyTorch · FastAPI · Docker · Redis · Kafka<br>
**Engineering** · Python · C++20 · Rust · Linux · Git · CMake · SQLite
