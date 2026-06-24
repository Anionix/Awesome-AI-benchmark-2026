# AIベンチマークリスト 2026

LLM、エージェント、ツール利用、コーディング、マルチモーダル、長文脈、安全性、サイバーセキュリティ、実世界タスク遂行を評価するためのベンチマークリスト。

> **Note**  
> 2026年6月時点のスナップショット。特にエージェントワークフロー、コーディング、ブラウザ操作、ツール利用では、ベンチマークの重要性が急速に変化します。

## Contents

- [Benchmark list](#benchmark-list)
- [Recommended benchmark bundles by evaluation goal](#評価目的別の推奨ベンチマーク構成)
- [Data files](#data-files)

## Benchmark list

| カテゴリ | ベンチマーク | 評価対象 |
| --- | --- | --- |
| 従来型LLM能力 | [MMLU](https://arxiv.org/abs/2009.03300) | 多数の学問・専門分野にわたる基礎知識と問題解決能力を評価。 |
| 従来型LLM能力 | [MMLU-Pro](https://github.com/TIGER-AI-Lab/MMLU-Pro) | MMLUを高難度化し、選択肢数と推論要求を高めた評価。 |
| 従来型LLM能力 | [GPQA Diamond](https://epoch.ai/benchmarks/gpqa-diamond) | 大学院レベルの高難度理科系問題で専門的な科学推論を評価。 |
| 従来型LLM能力 | [HLE / Humanity's Last Exam](https://agi.safe.ai/) | 知識・推論・マルチモーダル能力を広く測る高難度フロンティア評価。 |
| 従来型LLM能力 | [LiveBench](https://livebench.ai/) | 継続更新によりテスト汚染を抑え、最新モデル能力を追跡する評価。 |
| AGI志向の推論 | [ARC-AGI-2](https://arcprize.org/arc-agi/2) | 抽象パターン発見、規則帰納、少数例からの一般化を評価。 |
| AGI志向の推論 | [ARC-AGI-3](https://arcprize.org/arc-agi/3) | 探索、目標発見、世界モデル構築、行動計画などを評価。 |
| 実用AIエージェント | [Agents' Last Exam / ALE](https://arxiv.org/abs/2606.05405) | 多領域にわたる長期・高価値の実世界タスク遂行能力を評価。 |
| 実用AIエージェント | [GDPval](https://openai.com/index/gdpval/) | 職種・産業をまたぐ実世界の知識労働成果物を評価。 |
| 実用AIエージェント | [APEX-Agents](https://epoch.ai/benchmarks/apex-agents) | 金融、コンサル、法律、医療などの専門職ワークフローを評価。 |
| ツール利用とMCP | [Toolathlon / Tool Decathlon](https://github.com/hkust-nlp/Toolathlon) | 多数のアプリ・ツールを使う長期タスク遂行能力を評価。 |
| ツール利用とMCP | [MCP-Atlas](https://labs.scale.com/leaderboard/mcp_atlas) | MCPツールの発見、引数指定、複数ツール連携を評価。 |
| ツール利用とMCP | [LiveMCPBench](https://icip-cas.github.io/LiveMCPBench/) | 大規模ライブMCP環境でのツール選択・利用能力を評価。 |
| ツール利用とMCP | [BFCL v4](https://gorilla.cs.berkeley.edu/leaderboard.html) | LLMやエージェントの関数呼び出し・ツール呼び出し精度を評価。 |
| ツール利用とMCP | [MCP-Bench](https://github.com/Accenture/mcp-bench) | MCPサーバーを通じた現実的な複数ステップのツール利用を評価。 |
| ツール利用とMCP | [τ-bench](https://github.com/sierra-research/tau-bench) | ユーザー、ツール、ポリシーが絡む対話環境で評価。 |
| ツール利用とMCP | [τ²-bench](https://sierra.ai/resources/research/tau-squared-bench) | ユーザーとエージェント双方がツールを使う協調・ポリシー遵守を評価。 |
| ツール利用とMCP | [Agent-Diff](https://arxiv.org/abs/2602.11224) | 企業APIタスクを最終状態の差分で評価。 |
| CLIとソフトウェア工学 | [Terminal-Bench 2.0 / 3.0](https://www.tbench.ai/) | コードコンパイルやシステム設定など、CLI上の自律作業を評価。 |
| CLIとソフトウェア工学 | [TerminalWorld](https://github.com/EuniAI/TerminalWorld) | 実際のターミナル操作ログに基づくCLIタスクを評価。 |
| CLIとソフトウェア工学 | [SWE-bench](https://www.swebench.com/) | 実GitHubリポジトリのIssue修正能力を評価。 |
| CLIとソフトウェア工学 | [SWE-bench Verified](https://www.swebench.com/verified.html) | SWE-benchの人手検証済みサブセット。 |
| CLIとソフトウェア工学 | [SWE-bench Pro](https://labs.scale.com/leaderboard/swe_bench_pro_public) | より長期で現実的なソフトウェアエンジニアリングタスクを評価。 |
| CLIとソフトウェア工学 | [ProjDevBench](https://github.com/zsworld6/projdevbench) | 高レベル仕様からリポジトリ全体を構築する能力を評価。 |
| CLIとソフトウェア工学 | [OmniCode](https://github.com/seal-research/OmniCode) | 複数言語にわたる広範なソフトウェア工学タスクを評価。 |
| CLIとソフトウェア工学 | [WebCompass](https://github.com/NJU-LINK/WebCompass) | マルチモーダル入力からWebサイト/Webアプリを生成・編集・修復する能力を評価。 |
| CLIとソフトウェア工学 | [VISTA](https://arxiv.org/abs/2605.26144) | スクリーンショットや設計構造からWebアプリを実装する能力を評価。 |
| CLIとソフトウェア工学 | [SecureVibeBench](https://arxiv.org/abs/2509.22097) | 脆弱性関連タスクを中心に、安全なコード生成能力を評価。 |
| CLIとソフトウェア工学 | [SlopCodeBench](https://github.com/SprocketLab/slop-code-bench) | 反復的な仕様変更でコードが肥大化・劣化するかを評価。 |
| CLIとソフトウェア工学 | [CentaurEval](https://arxiv.org/abs/2512.04111) | 人間参加型の協働コーディング能力を評価。 |
| データ・オフィス業務・研究 | [Data Agent Benchmark / DAB](https://github.com/ucbepic/DataAgentBench) | DB、変換、分析を含む企業データエージェント業務を評価。 |
| データ・オフィス業務・研究 | [AIDABench](https://github.com/MichaelYang-lyx/AIDABench) | 異種データ、文書、業務記録を扱う分析エージェントを評価。 |
| データ・オフィス業務・研究 | [DSBench](https://github.com/liqiangjing/dsbench) | 現実的な分析・モデリングタスクでデータサイエンスエージェントを評価。 |
| データ・オフィス業務・研究 | [DataSciBench](https://datascibench.github.io/) | LLMエージェントによるデータサイエンスタスク遂行能力を評価。 |
| データ・オフィス業務・研究 | [AIRS-Bench](https://github.com/facebookresearch/airs-bench) | AI研究科学エージェントの研究ライフサイクル全体を評価。 |
| データ・オフィス業務・研究 | [DeployBench](https://arxiv.org/abs/2606.05238) | 新環境で研究成果物を展開・再現できるかを評価。 |
| データ・オフィス業務・研究 | [PaperBench](https://github.com/openai/frontier-evals/tree/main/project/paperbench) | 実装や実験を含め、AI研究論文を再現できるかを評価。 |
| データ・オフィス業務・研究 | [EduAgentBench](https://arxiv.org/abs/2605.14322) | 教授、学習診断、教育ワークフローにおける教育エージェントを評価。 |
| データ・オフィス業務・研究 | [AutoMat](https://arxiv.org/abs/2605.00803) | 計算材料科学論文の主張を再現できるかを評価。 |
| データ・オフィス業務・研究 | [SpreadsheetBench](https://spreadsheetbench.github.io/) | 複雑なスプレッドシート操作と業務表計算ワークフローを評価。 |
| Web・PC操作 | [OSWorld](https://os-world.github.io/) | 実コンピュータ環境でのGUI・OSレベル操作を評価。 |
| Web・PC操作 | [WebArena](https://webarena.dev/) | 現実的なWeb環境で自律Webエージェントを評価。 |
| Web・PC操作 | [VisualWebArena](https://github.com/web-arena-x/visualwebarena) | 視覚情報を使うマルチモーダルWebエージェントを評価。 |
| Web・PC操作 | [BrowserArena](https://github.com/sagnikanupam/browserarena) | ライブWeb上のブラウザタスクと選好型評価を扱う。 |
| Web・PC操作 | [BrowseComp](https://openai.com/index/browsecomp/) | Web上で見つけにくい情報を調査する能力を評価。 |
| マルチモーダル・長文脈・動画 | [MMMU-Pro](https://arxiv.org/abs/2409.02813) | 画像とテキストを含む大学レベルのマルチモーダル推論を評価。 |
| マルチモーダル・長文脈・動画 | [Video-MME v2](https://github.com/MME-Benchmarks/Video-MME-v2) | 短い動画から長い動画まで包括的な動画理解を評価。 |
| マルチモーダル・長文脈・動画 | [LongBench v2](https://longbench2.github.io/) | 長文脈における深い理解と推論能力を評価。 |
| マルチモーダル・長文脈・動画 | [MRCR](https://huggingface.co/datasets/openai/mrcr) | 複数ラウンドの共参照検索と長文脈情報追跡を評価。 |
| マルチモーダル・長文脈・動画 | [RULER](https://github.com/NVIDIA/RULER) | 検索・推論タスクでモデルの実効的なコンテキスト長を測る。 |
| マルチモーダル・長文脈・動画 | [NeedleBench](https://github.com/open-compass/opencompass/blob/main/opencompass/configs/datasets/needlebench_v2/readme.md) | 非常に長い文脈に埋め込まれた重要情報を検索できるかを評価。 |
| マルチモーダル・長文脈・動画 | [VLM-RobustBench](https://arxiv.org/abs/2603.06148) | 画像のノイズ・変換・劣化に対する視覚言語モデルの頑健性を評価。 |
| 安全性・サイバーセキュリティ・医療 | [MultiBreak](https://arxiv.org/abs/2605.01687) | 多様なマルチターン脱獄攻撃に対するLLM安全性を評価。 |
| 安全性・サイバーセキュリティ・医療 | [XL-SafetyBench](https://github.com/AIM-Intelligence/XL-SafetyBench) | 多言語・多文化における安全性と文化的感度を評価。 |
| 安全性・サイバーセキュリティ・医療 | [TukaBench](https://arxiv.org/abs/2606.01322) | アフリカ言語における文化的文脈を含む脱獄耐性を評価。 |
| 安全性・サイバーセキュリティ・医療 | [CyberGym-E2E](https://www.cybergym.io/cybergym-e2e/) | 脆弱性発見、PoC生成、パッチ作成などのエンドツーエンドのサイバータスクを評価。 |
| 安全性・サイバーセキュリティ・医療 | [CAIBench](https://arxiv.org/abs/2510.24317) | 攻撃・防御・知識・プライバシーを含むサイバーAIエージェント評価。 |
| 安全性・サイバーセキュリティ・医療 | [HealthBench](https://openai.com/index/healthbench/) | 臨床推論、医療安全、不確実性の扱い、コミュニケーションを評価。 |

## 評価目的別の推奨ベンチマーク構成

| 評価目的 | 推奨ベンチマーク |
| --- | --- |
| 汎用AIエージェント能力 | ALE, GDPval, APEX-Agents, Toolathlon / Tool Decathlon |
| AGI志向の推論 | ARC-AGI-3, ARC-AGI-2 |
| ツールとMCPの利用 | MCP-Atlas, LiveMCPBench, MCP-Bench, BFCL v4, τ²-bench |
| PC・ブラウザ操作 | OSWorld, BrowserArena, BrowseComp, WebArena, VisualWebArena |
| CLI・開発環境操作 | Terminal-Bench 2.0 / 3.0, TerminalWorld |
| 実用コーディング能力 | SWE-bench Pro, SWE-bench Verified, OmniCode, ProjDevBench, WebCompass |
| 研究再現・科学作業 | PaperBench, AIRS-Bench, DeployBench, AutoMat |
| データ分析・文書業務 | DAB, AIDABench, DSBench, SpreadsheetBench |
| マルチモーダル能力 | MMMU-Pro, Video-MME v2, VLM-RobustBench |
| 長文脈処理 | LongBench v2, RULER / MRCR / NeedleBench family |
| 安全性 | MultiBreak, XL-SafetyBench, TukaBench, CyberGym-E2E, HealthBench |

## Data files

This repository also includes reusable CSV and JSON files:

- [`data/benchmarks.csv`](../data/benchmarks.csv)
- [`data/benchmarks.json`](../data/benchmarks.json)

## Citation and maintenance note

Please treat this list as a living reference. Prefer official pages, GitHub repositories, leaderboards, or paper pages when updating links.
