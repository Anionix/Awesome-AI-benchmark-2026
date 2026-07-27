# AI 基准测试列表 2026

用于评估 LLM、智能体、工具使用、编码、多模态、长上下文、安全、网络安全与真实任务执行能力的基准列表。

> **Note**  
> 截至 2026 年 6 月的快照。基准的重要性变化很快，尤其是在智能体工作流、编码、浏览器操作和工具使用方面。

## Contents

- [Benchmark list](#benchmark-list)
- [Recommended benchmark bundles by evaluation goal](#按评估目标推荐的基准组合)
- [Data files](#data-files)

## Benchmark list

| 类别 | 基准 | 评估重点 |
| --- | --- | --- |
| 传统 LLM 能力 | [MMLU](https://arxiv.org/abs/2009.03300) | 评估多个学科领域中的广泛学术与专业知识能力。 |
| 传统 LLM 能力 | [MMLU-Pro](https://github.com/TIGER-AI-Lab/MMLU-Pro) | 更高难度的 MMLU 风格基准，增加选项数量并强化推理要求。 |
| 传统 LLM 能力 | [GPQA Diamond](https://epoch.ai/benchmarks/gpqa-diamond) | 使用高难度研究生级科学问题评估专家级科学推理能力。 |
| 传统 LLM 能力 | [HLE / Humanity's Last Exam](https://agi.safe.ai/) | 面向前沿模型的高难度综合基准，覆盖知识、推理与多模态任务。 |
| 传统 LLM 能力 | [LiveBench](https://livebench.ai/) | 持续更新的基准，旨在降低测试集污染并跟踪最新模型能力。 |
| 面向 AGI 的推理 | [ARC-AGI-2](https://arcprize.org/arc-agi/2) | 评估抽象模式发现、规则归纳和少样本泛化能力。 |
| 面向 AGI 的推理 | [ARC-AGI-3](https://arcprize.org/arc-agi/3) | 评估交互式推理、探索、目标发现、世界模型构建与规划能力。 |
| 实用 AI 智能体 | [Agents' Last Exam / ALE](https://arxiv.org/abs/2606.05405) | 评估跨多个领域、具有经济价值的长程真实世界任务执行能力。 |
| 实用 AI 智能体 | [GDPval](https://openai.com/index/gdpval/) | 评估跨职业与行业的真实知识工作交付物。 |
| 实用 AI 智能体 | [APEX-Agents](https://epoch.ai/benchmarks/apex-agents) | 评估金融、咨询、法律、医疗等专业领域的工作流执行能力。 |
| 工具使用与 MCP | [Toolathlon / Tool Decathlon](https://github.com/hkust-nlp/Toolathlon) | 评估在多应用、多工具环境中的长程任务执行能力。 |
| 工具使用与 MCP | [MCP-Atlas](https://labs.scale.com/leaderboard/mcp_atlas) | 评估 MCP 工具发现、参数指定和多工具协调能力。 |
| 工具使用与 MCP | [LiveMCPBench](https://icip-cas.github.io/LiveMCPBench/) | 评估在大规模实时 MCP 服务器环境中的工具选择与使用能力。 |
| 工具使用与 MCP | [BFCL v4](https://gorilla.cs.berkeley.edu/leaderboard.html) | 评估 LLM 与智能体的函数调用和工具调用准确性。 |
| 工具使用与 MCP | [MCP-Bench](https://github.com/Accenture/mcp-bench) | 通过 MCP 服务器评估现实多步骤工具使用任务。 |
| 工具使用与 MCP | [τ-bench](https://github.com/sierra-research/tau-bench) | 评估真实用户、工具与政策约束交互环境中的智能体能力。 |
| 工具使用与 MCP | [τ²-bench](https://sierra.ai/resources/research/tau-squared-bench) | 评估用户与智能体共同控制、共同使用工具并遵守政策约束的能力。 |
| 工具使用与 MCP | [Agent-Diff](https://arxiv.org/abs/2602.11224) | 通过比较最终状态差异评估企业 API 任务执行结果。 |
| CLI 与软件工程 | [Terminal-Bench 2.0 / 3.0](https://www.tbench.ai/) | 评估自动执行 CLI 任务的能力，如编译代码和配置系统。 |
| CLI 与软件工程 | [TerminalWorld](https://github.com/EuniAI/TerminalWorld) | 使用真实终端操作日志派生的任务评估 CLI 能力。 |
| CLI 与软件工程 | [SWE-bench](https://www.swebench.com/) | 评估真实 GitHub 仓库中的 issue 修复能力。 |
| CLI 与软件工程 | [SWE-bench Verified](https://www.swebench.com/verified.html) | SWE-bench 的人工验证子集，用于更高质量的软件工程评估。 |
| CLI 与软件工程 | [SWE-bench Pro](https://labs.scale.com/leaderboard/swe_bench_pro_public) | 评估更长程、更贴近真实的软件工程任务。 |
| CLI 与软件工程 | [ProjDevBench](https://github.com/zsworld6/projdevbench) | 评估根据高层规格构建完整软件仓库的能力。 |
| CLI 与软件工程 | [OmniCode](https://github.com/seal-research/OmniCode) | 覆盖多种编程语言中的广泛软件工程任务。 |
| CLI 与软件工程 | [WebCompass](https://github.com/NJU-LINK/WebCompass) | 评估根据多模态输入生成、编辑和修复网站或 Web 应用的能力。 |
| CLI 与软件工程 | [VISTA](https://arxiv.org/abs/2605.26144) | 评估从截图和设计结构生成 Web 应用的能力。 |
| CLI 与软件工程 | [SecureVibeBench](https://arxiv.org/abs/2509.22097) | 评估编码智能体是否能生成安全代码，尤其是与漏洞相关的任务。 |
| CLI 与软件工程 | [SlopCodeBench](https://github.com/SprocketLab/slop-code-bench) | 评估反复规格变更下代码退化、膨胀和质量下降问题。 |
| CLI 与软件工程 | [CentaurEval](https://arxiv.org/abs/2512.04111) | 评估人在回路中的协作对智能体编码任务的价值。 |
| 数据、办公与研究 | [Data Agent Benchmark / DAB](https://github.com/ucbepic/DataAgentBench) | 评估企业数据智能体工作流，包括数据库、数据转换和分析。 |
| 数据、办公与研究 | [AIDABench](https://github.com/MichaelYang-lyx/AIDABench) | 评估面向异构数据、文档和业务记录的分析型智能体。 |
| 数据、办公与研究 | [DSBench](https://github.com/liqiangjing/dsbench) | 评估数据科学智能体在真实分析与建模任务中的能力。 |
| 数据、办公与研究 | [DataSciBench](https://datascibench.github.io/) | 评估 LLM 智能体的数据科学任务执行能力。 |
| 数据、办公与研究 | [AIRS-Bench](https://github.com/facebookresearch/airs-bench) | 评估 AI 研究科学智能体在研究生命周期中的能力。 |
| 数据、办公与研究 | [DeployBench](https://arxiv.org/abs/2606.05238) | 评估在新环境中部署和复现实验制品的能力。 |
| 数据、办公与研究 | [PaperBench](https://github.com/openai/frontier-evals/tree/main/project/paperbench) | 评估智能体能否复现 AI 研究论文，包括实现与实验。 |
| 数据、办公与研究 | [EduAgentBench](https://arxiv.org/abs/2605.14322) | 评估教育智能体在教学、学习诊断和教育工作流中的能力。 |
| 数据、办公与研究 | [AutoMat](https://arxiv.org/abs/2605.00803) | 评估复现计算材料科学论文中主张的能力。 |
| 数据、办公与研究 | [SpreadsheetBench](https://spreadsheetbench.github.io/) | 评估复杂电子表格操作和商务表格工作流。 |
| Web 与 PC 操作 | [OSWorld](https://os-world.github.io/) | 评估真实计算机环境中的 GUI 与操作系统级任务执行能力。 |
| Web 与 PC 操作 | [WebArena](https://webarena.dev/) | 评估真实 Web 环境中的自主 Web 智能体。 |
| Web 与 PC 操作 | [VisualWebArena](https://github.com/web-arena-x/visualwebarena) | 评估利用网页视觉信息的多模态 Web 智能体。 |
| Web 与 PC 操作 | [BrowserArena](https://github.com/sagnikanupam/browserarena) | 评估实时开放 Web 浏览器任务和偏好式判断。 |
| Web 与 PC 操作 | [BrowseComp](https://openai.com/index/browsecomp/) | 评估困难网页浏览和难以查找信息的检索能力。 |
| Web 与 PC 操作 | [ClawBench](https://claw-bench.com/) | 覆盖144个真实网站的长程浏览器智能体任务，并提供请求级结果检查和执行轨迹。 |
| 多模态、长上下文与视频 | [MMMU-Pro](https://arxiv.org/abs/2409.02813) | 评估包含图像与文本输入的大学级多模态推理能力。 |
| 多模态、长上下文与视频 | [Video-MME v2](https://github.com/MME-Benchmarks/Video-MME-v2) | 评估短视频与长视频中的综合视频理解能力。 |
| 多模态、长上下文与视频 | [LongBench v2](https://longbench2.github.io/) | 评估长上下文中的深层理解与推理能力。 |
| 多模态、长上下文与视频 | [MRCR](https://huggingface.co/datasets/openai/mrcr) | 评估多轮共指检索和长上下文信息追踪能力。 |
| 多模态、长上下文与视频 | [RULER](https://github.com/NVIDIA/RULER) | 通过检索和推理任务评估有效上下文长度。 |
| 多模态、长上下文与视频 | [NeedleBench](https://github.com/open-compass/opencompass/blob/main/opencompass/configs/datasets/needlebench_v2/readme.md) | 评估在超长上下文中检索隐藏关键信息的能力。 |
| 多模态、长上下文与视频 | [VLM-RobustBench](https://arxiv.org/abs/2603.06148) | 评估视觉语言模型在图像扰动和变换下的鲁棒性。 |
| 安全、网络安全与医疗 | [MultiBreak](https://arxiv.org/abs/2605.01687) | 评估 LLM 面对多样化多轮越狱攻击时的安全性。 |
| 安全、网络安全与医疗 | [XL-SafetyBench](https://github.com/AIM-Intelligence/XL-SafetyBench) | 评估多语言、跨文化的安全性与文化敏感性。 |
| 安全、网络安全与医疗 | [TukaBench](https://arxiv.org/abs/2606.01322) | 评估非洲语言中具备文化语境的越狱鲁棒性。 |
| 安全、网络安全与医疗 | [CyberGym-E2E](https://www.cybergym.io/cybergym-e2e/) | 评估漏洞发现、PoC 生成和补丁修复等端到端网络安全任务。 |
| 安全、网络安全与医疗 | [CAIBench](https://arxiv.org/abs/2510.24317) | 覆盖攻击、防御、知识和隐私任务的网络安全 AI 智能体元基准。 |
| 安全、网络安全与医疗 | [HealthBench](https://openai.com/index/healthbench/) | 评估临床推理、医疗安全、不确定性处理和沟通能力。 |

## 按评估目标推荐的基准组合

| 评估目标 | 推荐基准 |
| --- | --- |
| 通用 AI 智能体能力 | ALE, GDPval, APEX-Agents, Toolathlon / Tool Decathlon |
| 面向 AGI 的推理 | ARC-AGI-3, ARC-AGI-2 |
| 工具与 MCP 使用 | MCP-Atlas, LiveMCPBench, MCP-Bench, BFCL v4, τ²-bench |
| PC 与浏览器操作 | OSWorld, BrowserArena, BrowseComp, WebArena, VisualWebArena |
| CLI 与开发环境操作 | Terminal-Bench 2.0 / 3.0, TerminalWorld |
| 实用编码能力 | SWE-bench Pro, SWE-bench Verified, OmniCode, ProjDevBench, WebCompass |
| 研究复现与科学工作 | PaperBench, AIRS-Bench, DeployBench, AutoMat |
| 数据分析与文档工作 | DAB, AIDABench, DSBench, SpreadsheetBench |
| 多模态能力 | MMMU-Pro, Video-MME v2, VLM-RobustBench |
| 长上下文处理 | LongBench v2, RULER / MRCR / NeedleBench family |
| 安全性 | MultiBreak, XL-SafetyBench, TukaBench, CyberGym-E2E, HealthBench |

## Data files

This repository also includes reusable CSV and JSON files:

- [`data/benchmarks.csv`](../data/benchmarks.csv)
- [`data/benchmarks.json`](../data/benchmarks.json)

## Citation and maintenance note

Please treat this list as a living reference. Prefer official pages, GitHub repositories, leaderboards, or paper pages when updating links.
