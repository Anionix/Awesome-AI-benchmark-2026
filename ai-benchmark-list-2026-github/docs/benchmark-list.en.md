# AI Benchmark List 2026

A curated benchmark list for evaluating LLMs, agents, tool use, coding, multimodal capability, long-context processing, safety, cybersecurity, and real-world task execution.

> **Note**  
> Snapshot as of June 2026. Benchmark relevance evolves rapidly, especially in agentic workflows, coding, browser operation, and tool use.

## Contents

- [Benchmark list](#benchmark-list)
- [Recommended benchmark bundles by evaluation goal](#recommended-benchmark-bundles-by-evaluation-goal)
- [Data files](#data-files)

## Benchmark list

| Category | Benchmark | Evaluation focus |
| --- | --- | --- |
| Traditional LLM capability | [MMLU](https://arxiv.org/abs/2009.03300) | Broad academic and professional knowledge across many subjects. |
| Traditional LLM capability | [MMLU-Pro](https://github.com/TIGER-AI-Lab/MMLU-Pro) | A harder MMLU-style benchmark with more choices and stronger reasoning demand. |
| Traditional LLM capability | [GPQA Diamond](https://epoch.ai/benchmarks/gpqa-diamond) | Expert-level scientific reasoning using difficult graduate-level questions. |
| Traditional LLM capability | [HLE / Humanity's Last Exam](https://agi.safe.ai/) | A frontier benchmark for broad knowledge, reasoning, and multimodal tasks. |
| Traditional LLM capability | [LiveBench](https://livebench.ai/) | A frequently updated benchmark designed to reduce contamination and track current capability. |
| AGI-oriented reasoning | [ARC-AGI-2](https://arcprize.org/arc-agi/2) | Abstract pattern discovery, rule induction, and few-shot generalization. |
| AGI-oriented reasoning | [ARC-AGI-3](https://arcprize.org/arc-agi/3) | Interactive reasoning, exploration, goal discovery, world modeling, and planning. |
| Practical AI agents | [Agents' Last Exam / ALE](https://arxiv.org/abs/2606.05405) | Long-horizon, economically valuable real-world tasks across many fields. |
| Practical AI agents | [GDPval](https://openai.com/index/gdpval/) | Real-world work deliverables across occupations and industries. |
| Practical AI agents | [APEX-Agents](https://epoch.ai/benchmarks/apex-agents) | Professional workflows in finance, consulting, law, medicine, and related domains. |
| Tool use and MCP | [Toolathlon / Tool Decathlon](https://github.com/hkust-nlp/Toolathlon) | Long-horizon task execution with many applications and tools. |
| Tool use and MCP | [MCP-Atlas](https://labs.scale.com/leaderboard/mcp_atlas) | MCP tool discovery, parameter specification, and multi-tool coordination. |
| Tool use and MCP | [LiveMCPBench](https://icip-cas.github.io/LiveMCPBench/) | Tool selection and use across large live MCP server environments. |
| Tool use and MCP | [BFCL v4](https://gorilla.cs.berkeley.edu/leaderboard.html) | Function calling and tool calling accuracy for LLMs and agents. |
| Tool use and MCP | [MCP-Bench](https://github.com/Accenture/mcp-bench) | Realistic multi-step tool-using tasks through MCP servers. |
| Tool use and MCP | [τ-bench](https://github.com/sierra-research/tau-bench) | Realistic user, tool, and policy interaction settings. |
| Tool use and MCP | [τ²-bench](https://sierra.ai/resources/research/tau-squared-bench) | Dual-control user-agent collaboration with tools and policy constraints. |
| Tool use and MCP | [Agent-Diff](https://arxiv.org/abs/2602.11224) | Enterprise API tasks evaluated by final-state differences. |
| CLI and software engineering | [Terminal-Bench 2.0 / 3.0](https://www.tbench.ai/) | Autonomous CLI tasks such as compiling code and configuring systems. |
| CLI and software engineering | [TerminalWorld](https://github.com/EuniAI/TerminalWorld) | Terminal tasks derived from real terminal operation logs. |
| CLI and software engineering | [SWE-bench](https://www.swebench.com/) | Issue fixing in real GitHub repositories. |
| CLI and software engineering | [SWE-bench Verified](https://www.swebench.com/verified.html) | A human-validated SWE-bench subset for higher-quality software engineering evaluation. |
| CLI and software engineering | [SWE-bench Pro](https://labs.scale.com/leaderboard/swe_bench_pro_public) | Longer-horizon and more realistic software engineering tasks. |
| CLI and software engineering | [ProjDevBench](https://github.com/zsworld6/projdevbench) | Building complete software repositories from high-level specifications. |
| CLI and software engineering | [OmniCode](https://github.com/seal-research/OmniCode) | Broad software engineering tasks across multiple programming languages. |
| CLI and software engineering | [WebCompass](https://github.com/NJU-LINK/WebCompass) | Generating, editing, and repairing websites or web apps from multimodal inputs. |
| CLI and software engineering | [VISTA](https://arxiv.org/abs/2605.26144) | Visual-spec-to-web-app coding from screenshots and design structures. |
| CLI and software engineering | [SecureVibeBench](https://arxiv.org/abs/2509.22097) | Secure coding by AI agents, especially for vulnerability-related tasks. |
| CLI and software engineering | [SlopCodeBench](https://github.com/SprocketLab/slop-code-bench) | Code erosion, bloat, and degradation under iterative specification changes. |
| CLI and software engineering | [CentaurEval](https://arxiv.org/abs/2512.04111) | Human-in-the-loop collaboration in agentic coding. |
| Data, office work, and research | [Data Agent Benchmark / DAB](https://github.com/ucbepic/DataAgentBench) | Enterprise data-agent workflows including databases, transformations, and analysis. |
| Data, office work, and research | [AIDABench](https://github.com/MichaelYang-lyx/AIDABench) | Analytical agents over heterogeneous data, documents, and business records. |
| Data, office work, and research | [DSBench](https://github.com/liqiangjing/dsbench) | Data science agents on realistic analysis and modeling tasks. |
| Data, office work, and research | [DataSciBench](https://datascibench.github.io/) | Data science task execution by LLM agents. |
| Data, office work, and research | [AIRS-Bench](https://github.com/facebookresearch/airs-bench) | AI research-science agents across the research lifecycle. |
| Data, office work, and research | [DeployBench](https://arxiv.org/abs/2606.05238) | Deploying and reproducing research artifacts in new environments. |
| Data, office work, and research | [PaperBench](https://github.com/openai/frontier-evals/tree/main/project/paperbench) | Replicating AI research papers, including implementation and experiments. |
| Data, office work, and research | [EduAgentBench](https://arxiv.org/abs/2605.14322) | Educational agents in teaching, diagnosis, and learning workflows. |
| Data, office work, and research | [AutoMat](https://arxiv.org/abs/2605.00803) | Reproducing claims from computational materials science papers. |
| Data, office work, and research | [SpreadsheetBench](https://spreadsheetbench.github.io/) | Complex spreadsheet manipulation and business spreadsheet workflows. |
| Web and PC operation | [OSWorld](https://os-world.github.io/) | GUI and OS-level operation in real computer environments. |
| Web and PC operation | [WebArena](https://webarena.dev/) | Autonomous web agents in realistic web environments. |
| Web and PC operation | [VisualWebArena](https://github.com/web-arena-x/visualwebarena) | Multimodal web agents using visual page information. |
| Web and PC operation | [BrowserArena](https://github.com/sagnikanupam/browserarena) | Live open-web browser tasks and preference-style judgments. |
| Web and PC operation | [BrowseComp](https://openai.com/index/browsecomp/) | Difficult web browsing and hard-to-find information retrieval. |
| Multimodal, long-context, and video | [MMMU-Pro](https://arxiv.org/abs/2409.02813) | University-level multimodal reasoning with image and text inputs. |
| Multimodal, long-context, and video | [Video-MME v2](https://github.com/MME-Benchmarks/Video-MME-v2) | Comprehensive video understanding across short and long videos. |
| Multimodal, long-context, and video | [LongBench v2](https://longbench2.github.io/) | Deep understanding and reasoning over long contexts. |
| Multimodal, long-context, and video | [MRCR](https://huggingface.co/datasets/openai/mrcr) | Multi-round coreference retrieval and long-context information tracking. |
| Multimodal, long-context, and video | [RULER](https://github.com/NVIDIA/RULER) | Effective context length with retrieval and reasoning tasks. |
| Multimodal, long-context, and video | [NeedleBench](https://github.com/open-compass/opencompass/blob/main/opencompass/configs/datasets/needlebench_v2/readme.md) | Retrieval of relevant information hidden in very long contexts. |
| Multimodal, long-context, and video | [VLM-RobustBench](https://arxiv.org/abs/2603.06148) | Robustness of vision-language models under image corruptions and transformations. |
| Safety, cybersecurity, and healthcare | [MultiBreak](https://arxiv.org/abs/2605.01687) | LLM safety against diverse multi-turn jailbreak attacks. |
| Safety, cybersecurity, and healthcare | [XL-SafetyBench](https://github.com/AIM-Intelligence/XL-SafetyBench) | Multilingual and cross-cultural safety and sensitivity. |
| Safety, cybersecurity, and healthcare | [TukaBench](https://arxiv.org/abs/2606.01322) | Culturally grounded jailbreak robustness for African languages. |
| Safety, cybersecurity, and healthcare | [CyberGym-E2E](https://www.cybergym.io/cybergym-e2e/) | End-to-end cybersecurity tasks such as vulnerability discovery, PoC creation, and patching. |
| Safety, cybersecurity, and healthcare | [CAIBench](https://arxiv.org/abs/2510.24317) | A meta-benchmark for cybersecurity AI agents across attack, defense, knowledge, and privacy tasks. |
| Safety, cybersecurity, and healthcare | [HealthBench](https://openai.com/index/healthbench/) | Clinical reasoning, medical safety, uncertainty handling, and communication. |

## Recommended benchmark bundles by evaluation goal

| Evaluation goal | Recommended benchmarks |
| --- | --- |
| General AI agent capability | ALE, GDPval, APEX-Agents, Toolathlon / Tool Decathlon |
| AGI-oriented reasoning | ARC-AGI-3, ARC-AGI-2 |
| Tool and MCP use | MCP-Atlas, LiveMCPBench, MCP-Bench, BFCL v4, τ²-bench |
| PC and browser operation | OSWorld, BrowserArena, BrowseComp, WebArena, VisualWebArena |
| CLI and development-environment operation | Terminal-Bench 2.0 / 3.0, TerminalWorld |
| Practical coding ability | SWE-bench Pro, SWE-bench Verified, OmniCode, ProjDevBench, WebCompass |
| Research replication and scientific work | PaperBench, AIRS-Bench, DeployBench, AutoMat |
| Data analysis and document work | DAB, AIDABench, DSBench, SpreadsheetBench |
| Multimodal capability | MMMU-Pro, Video-MME v2, VLM-RobustBench |
| Long-context processing | LongBench v2, RULER / MRCR / NeedleBench family |
| Safety | MultiBreak, XL-SafetyBench, TukaBench, CyberGym-E2E, HealthBench |

## Data files

This repository also includes reusable CSV and JSON files:

- [`data/benchmarks.csv`](../data/benchmarks.csv)
- [`data/benchmarks.json`](../data/benchmarks.json)

## Citation and maintenance note

Please treat this list as a living reference. Prefer official pages, GitHub repositories, leaderboards, or paper pages when updating links.
