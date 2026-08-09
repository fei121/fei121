<div align="center">

# 你好，我是 Yufei 👋

### LLM 推理优化 · AI Agent 工程 · 多模态智能

上海理工大学

[![GitHub](https://img.shields.io/badge/GitHub-fei121-181717?logo=github&logoColor=white)](https://github.com/fei121)
[![Python](https://img.shields.io/badge/Python-工程实践-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Focus](https://img.shields.io/badge/Focus-LLM%20%7C%20Agent%20%7C%20Multimodal-6C63FF)](https://github.com/fei121)

</div>

## 关于我

我关注如何将模型能力转化为可复现、可评测、可部署的工程系统。当前的实践重点包括大语言模型量化与推理性能分析、AI Agent 的工具与检索能力，以及多模态时空感知。

我尤其重视从实验结果出发定位问题根因，并将结论沉淀为可复核的数据、脚本与文档。

## 技术方向

| 方向 | 实践重点 |
| --- | --- |
| **LLM 推理优化** | 后训练量化、精度评测、吞吐与时延分析、异常归因 |
| **AI Agent 工程** | 工具发现、检索增强、上下文与知识库能力 |
| **多模态智能** | RGB 与伪深度融合、时空特征建模、视觉里程计 |
| **工程方法** | 可复现实验、模块消融、结果可视化、技术文档化 |

## 代表项目

### [Qwen3-8B Quantization Lab](https://github.com/fei121/Qwen3-8B-Quantization)

面向 Qwen3-8B 的后训练量化、推理性能评测与精度损失归因项目。

- 对比 **vLLM + LLM Compressor**、**AutoRound + vLLM**、**TensorRT-LLM + ModelOpt** 三条量化与部署链路。
- 在统一的 GSM8K / C-Eval 评测口径下，比较 BF16、INT8 与 MXFP4 的精度和性能。
- 通过 hidden-state cosine、SQNR、P99 误差、模块跳过与累计消融，将特定 INT8 异常的主要误差定位到 `mlp.down_proj`。
- 在 vLLM INT8 W8A8 链路中，输出吞吐由 BF16 的 **261 tokens/s** 提升至 **1,085 tokens/s**，同时保持接近 BF16 的评测精度。

### [DeepResearch](https://github.com/fei121/DeepResearch)

面向复杂问题的深度检索 Agent。基于 ReAct 循环完成问题拆解、搜索路径规划、网页阅读、证据提取与多源交叉验证，并包含搜索源降级、SSE 心跳、超时和上下文预算保护。

### [LLM-SearchEval](https://github.com/fei121/LLM-SearchEval)

面向大语言模型联网搜索能力的实验、评估与可观测分析框架。覆盖参数扫描、搜索触发与引用追踪、规则评估、LLM-as-a-Judge、Pareto 权衡分析和科研风格可视化。

### [Tool Index](https://github.com/fei121/tool_index)

面向 AI Agent 的 OpenAPI 文档知识库与混合检索服务。将分散的 API 文档结构化为可搜索、可回查的工具目录，通过 MCP 和 HTTP 提供向量检索、BM25 与跨知识库候选融合能力。

### [保险条款拆解服务](https://github.com/fei121/agents-disassemble)

面向保险条款 PDF 的文档理解与结构化责任拆解服务。结合 PDF 解析、Markdown 结构化、FAISS / BM25 混合检索、LLM 工作流与字段级置信度评估，输出责任范围、等待期、既往症与责任免除等信息。

### [理赔文档结构化服务](https://github.com/fei121/agents-claim-doc-consolidation)

面向理赔流程的 OCR + LLM 文档理解服务。支持发票、身份证、银行卡、自定义 JSON Schema 抽取，以及病历与发票匹配；通过 FastAPI 对外提供统一的结构化 API。

### [TencentDB Agent Memory](https://github.com/fei121/TencentDB-Agent-Memory)

**开源项目学习与实践（Fork）**。关注 Agent 的本地化长期记忆、符号化短期记忆和分层信息组织，探索如何降低长任务中的上下文负担并提升信息可追溯性。

## 技术栈

<p align="left">
  <img src="https://skillicons.dev/icons?i=py,pytorch,fastapi,sqlite,linux,git" alt="Python, PyTorch, FastAPI, SQLite, Linux, Git" />
  <img src="https://cdn.simpleicons.org/huggingface" alt="Hugging Face" height="48" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" alt="NumPy" height="48" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" alt="Pandas" height="48" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/matplotlib/matplotlib-original.svg" alt="Matplotlib" height="48" />
</p>

<p>
  <img src="https://img.shields.io/badge/vLLM-推理部署-00A67E" alt="vLLM" />
  <img src="https://img.shields.io/badge/TensorRT--LLM-推理加速-76B900?logo=nvidia&logoColor=white" alt="TensorRT-LLM" />
  <img src="https://img.shields.io/badge/Hugging%20Face-模型生态-FFD21E?logo=huggingface&logoColor=black" alt="Hugging Face" />
  <img src="https://img.shields.io/badge/SQLite-本地知识库-003B57?logo=sqlite&logoColor=white" alt="SQLite" />
</p>

## 正在探索

- 大模型量化的精度—性能权衡与可解释性分析。
- 面向 AI Agent 的工具检索、结构化 API 知识库与上下文优化。
- 将研究型实验打磨为可复现、可部署的工程成果。

## 联系方式

欢迎通过 [GitHub @fei121](https://github.com/fei121) 交流 LLM 推理优化、AI Agent 与开源工程实践。
