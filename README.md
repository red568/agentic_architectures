# All Agentic Architectures（中文笔记）

本仓库包含 **17+ 种前沿 Agentic 架构** 的详细实现，基于 LangChain 与 LangGraph 构建。它旨在作为一本“活的教材”，弥合理论概念与可落地生产代码之间的差距。

## 📖 为什么要做这个仓库？

AI 智能体领域发展非常快，但许多资料仍偏抽象与理论化。这个项目的目标，是为开发者、研究者和 AI 爱好者提供一条结构化、可实践、强调教学深度的学习路径，真正掌握构建智能系统的方法。

- **从理论到可运行代码：** 每个架构不仅讲原理，而且都以可运行的 Jupyter Notebook 端到端实现。
- **循序渐进的学习路径：** Notebook 按难度编排，从基础模式逐步过渡到高级多智能体与自反系统。
- **重视评估：** 不只“搭建”智能体，也“量化”智能体。大多数 Notebook 引入 `LLM-as-a-Judge`，用于客观评估性能，这是走向生产级 AI 的关键能力。
- **贴近真实场景：** 示例覆盖金融分析、代码生成、社媒管理、医疗分诊等，概念可直接迁移到现实任务。
- **统一现代框架：** 以 `LangGraph` 为核心编排器，学习状态化、循环式的智能体工作流，这正逐渐成为行业主流。

---

## 🏛️ 架构总览

本仓库覆盖现代 Agentic 设计的完整光谱：从单智能体增强到复杂协作与自我改进系统。

| # | 架构 | 核心概念 / TL;DR | 典型场景 | Notebook |
|:---:|---|---|---|:---:|
| **01** | **Reflection** | 通过自我批评与迭代优化，把一次性生成器升级为多步推理者。 | 高质量代码生成、复杂总结 | [01_reflection_zh.ipynb](./01_reflection_zh.ipynb) |
| **02** | **Tool Use** | 通过调用外部 API/函数，突破知识截止并与真实世界交互。 | 实时研究助手、企业机器人 | [02_tool_use_zh.ipynb](./02_tool_use_zh.ipynb) |
| **03** | **ReAct** | 在循环中动态交替“思考（Thought）”与“行动（Tool Use）”。 | 多跳问答、网页导航与检索 | [03_ReAct_zh.ipynb](./03_ReAct_zh.ipynb) |
| **04** | **Planning** | 执行前先把复杂任务拆解为可追踪的分步计划。 | 可预测报告生成、项目管理 | [04_planning_zh.ipynb](./04_planning_zh.ipynb) |
| **05** | **Multi-Agent Systems** | 多个专长智能体协作分工，提升输出深度与质量。 | 软件开发流水线、创意头脑风暴 | [05_multi_agent_zh.ipynb](./05_multi_agent_zh.ipynb) |
| **06** | **PEV (Plan, Execute, Verify)** | 每步执行后由验证器检查结果并触发纠错恢复。 | 高风险自动化、金融、不稳定工具链 | [06_PEV_zh.ipynb](./06_PEV_zh.ipynb) |
| **07** | **Blackboard Systems** | 智能体通过共享黑板记忆机会式协作，由控制器动态调度。 | 复杂诊断、动态问题求解 | [07_blackboard_zh.ipynb](./07_blackboard_zh.ipynb) |
| **08** | **Episodic + Semantic Memory** | 向量记忆（情景）+ 图谱记忆（语义）结合，实现长期个性化。 | 长期助理、个性化导师 | [08_episodic_with_semantic_zh.ipynb](./08_episodic_with_semantic_zh.ipynb) |
| **09** | **Tree of Thoughts (ToT)** | 以树状结构探索多条推理路径并剪枝，系统寻找更优解。 | 逻辑谜题、约束规划 | [09_tree_of_thoughts_zh.ipynb](./09_tree_of_thoughts_zh.ipynb) |
| **10** | **Mental Loop (Simulator)** | 在内部模拟器中预演行动结果，评估风险后再执行。 | 机器人、量化交易、安全关键系统 | [10_mental_loop_zh.ipynb](./10_mental_loop_zh.ipynb) |
| **11** | **Meta-Controller** | 元控制器分析任务并路由到最合适的专家子智能体。 | 多服务 AI 平台、自适应助理 | [11_meta_controller_zh.ipynb](./11_meta_controller_zh.ipynb) |
| **12** | **Graph (World-Model Memory)** | 把知识表示为实体关系图，支持复杂多跳推理。 | 企业情报、高级研究 | [12_graph_zh.ipynb](./12_graph_zh.ipynb) |
| **13** | **Ensemble** | 多个独立智能体并行分析，再由聚合器综合输出。 | 高风险决策支持、事实核查 | [13_ensemble_zh.ipynb](./13_ensemble_zh.ipynb) |
| **14** | **Dry-Run Harness** | 高安全模式：先沙箱演练，再由人/检查器批准后执行。 | 生产级部署、调试验证 | [14_dry_run_zh.ipynb](./14_dry_run_zh.ipynb) |
| **15** | **RLHF (Self-Improvement)** | 由“编辑器智能体”给反馈并迭代修订，优质结果沉淀复用。 | 高质量内容生成、持续学习 | [15_RLHF_zh.ipynb](./15_RLHF_zh.ipynb) |
| **16** | **Cellular Automata** | 局部简单规则驱动全局涌现行为（如路径优化）。 | 空间推理、物流、复杂系统模拟 | [16_cellular_automata_zh.ipynb](./16_cellular_automata_zh.ipynb) |
| **17** | **Reflexive Metacognitive** | 具备“自我模型”，可评估能力边界并选择升级到人类。 | 医疗/法律/金融等高风险咨询 | [17_reflexive_metacognitive_zh.ipynb](./17_reflexive_metacognitive_zh.ipynb) |

---

## 🗺️ 学习路径建议

仓库按“由浅入深”组织：从单智能体增强，逐步走向多智能体协作、长期记忆、可靠性与自我改进。

- **Part 1（1-4）：基础模式**  
  Reflection、Tool Use、ReAct、Planning。
- **Part 2（5/7/11/13）：多智能体协作**  
  专家分工、路由调度、黑板协作、并行集成。
- **Part 3（8/9/12）：记忆与深度推理**  
  情景+语义记忆、图推理、ToT 搜索。
- **Part 4（6/10/14/17）：安全与可靠性**  
  验证闭环、模拟预演、干跑审批、自我边界认知。
- **Part 5（15/16）：学习与适应**  
  反馈驱动自我优化、涌现式群体行为。

---

## 🛠️ 技术栈与环境

| 组件 | 用途 |
|---|---|
| **Python 3.10+** | 项目核心编程语言 |
| **LangChain** | LLM 与工具交互的基础抽象 |
| **LangGraph** | 构建状态化、循环式工作流的核心框架 |
| **Nebius AI Models** | 负责推理的高性能大模型 |
| **Jupyter Notebooks** | 交互式开发与分步讲解 |
| **Pydantic** | 结构化输出与数据约束 |
| **Tavily Search** | 检索类智能体搜索工具 |
| **Neo4j** | 图数据库（语义/世界模型记忆） |
| **FAISS** | 向量检索（情景记忆） |

## 🚀 快速开始

### 1) 克隆仓库

```bash
git clone https://github.com/red568/agentic_architectures.git
cd agentic-architectures
```

### 2) 创建虚拟环境

```bash
# Unix/macOS
python3 -m venv venv
source venv/bin/activate

# Windows
python -m venv venv
.\venv\Scripts\activate
```

### 3) 安装依赖

本仓库当前未包含 `requirements.txt`。如需运行 Notebook，请按各 Notebook 中实际使用的库自行安装，通常至少需要：

```bash
pip install jupyter langchain langgraph python-dotenv pydantic
```

### 4) 配置环境变量

在项目根目录创建 `.env`，示例：

```python
# .env file

# Nebius AI API Key (for LLM access)
NEBIUS_API_KEY="your_nebius_api_key_here"

# LangSmith API Key (for tracing and debugging)
LANGCHAIN_API_KEY="your_langsmith_api_key_here"
LANGCHAIN_TRACING_V2="true"
LANGCHAIN_PROJECT="All-Agentic-Architectures" # Optional: Set a project name

# Tavily Search API Key (for the Research agent's tool)
TAVILY_API_KEY="your_tavily_api_key_here"

# Neo4j Credentials (for Graph and Memory architectures)
# You must have a Neo4j instance running (e.g., via Docker or Neo4j Desktop)
NEO4J_URI="bolt://localhost:7687"
NEO4J_USERNAME="neo4j"
NEO4J_PASSWORD="your_neo4j_password_here"
```

### 5) 启动 Notebook

```bash
jupyter notebook
```

## 🤝 贡献指南

欢迎贡献！你可以：

1. Fork 仓库  
2. 新建分支（特性或修复）  
3. 提交修改（请保证代码注释与 Notebook 讲解清晰）  
4. 发起 PR 并说明变更原因

也欢迎提交 Issue：报告 bug、建议改进、或提议新增架构。

## 📄 说明

当前仓库为中文整理版本，保留的 Notebook 文件均使用 `_zh.ipynb` 命名。
