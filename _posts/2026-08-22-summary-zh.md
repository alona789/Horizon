---
layout: default
title: "Horizon Summary: 2026-08-22 (ZH)"
date: 2026-08-22
lang: zh
---

> 从 30 条内容中筛选出 5 条重要资讯。

---

1. [SGLang v0.5.18 发布：新增多款模型并加速启动](#item-1) ⭐️ 8.0/10
2. [MCP 路线图：远程服务器标准化为 HTTP，并统一智能体身份认证](#item-2) ⭐️ 8.0/10
3. [250M 参数量化 LLM 从零训练，60MB 部署](#item-3) ⭐️ 8.0/10
4. [开源 Roguelike 游戏 DelveRL：专为训练 AI 智能体打造](#item-4) ⭐️ 8.0/10
5. [SemiAnalysis：开源模型追平闭源时间每代减半](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SGLang v0.5.18 发布：新增多款模型并加速启动](https://github.com/sgl-project/sglang/releases/tag/v0.5.18) ⭐️ 8.0/10

SGLang v0.5.18 正式发布，合并了 212 位贡献者提交的 710 个拉取请求。该版本新增了对新模型的支持，包括 Meta 的 Muse Glimmer、SANA-Video、LTX-2.5 和 Cosmos3 Edge，并引入了重叠检查点暂存和 TP LMHead All-to-All 等优化。 SGLang 是一款广泛使用的 LLM 推理引擎，此次更新显著扩展了模型覆盖范围，加入了对扩散模型和 Muse Glimmer 等智能体模型的支持。性能优化减少了启动时间并降低了延迟，有利于 AI/ML 服务基础设施的发展。 该版本新增了重叠检查点暂存功能，使 Qwen3-32B 在 H100 上的启动速度最高提升 2.38 倍；TP LMHead 全对全通信使 DeepSeek-V4-Pro 的 LMHead 时间从 320 微秒降至 169 微秒。FlashInfer MNNVL 纯全规约模式在 Blackwell 上带来最高 +6.9% 的解码性能提升。依赖项更新至 torch 2.13.0、flashinfer 0.6.17 和 sgl-kernel 0.4.6.post1。

github · Fridge003 · 8月22日 00:09

**背景**: SGLang 是一个开源的推理引擎，专为服务于大型语言模型及其他生成式模型而设计，注重高吞吐量和低延迟。此次发布延续了项目从纯 LLM 服务向图像与视频扩散模型扩展的趋势，反映了不同生成式 AI 工作负载的融合。项目提供了 cookbook，包含每个支持模型的部署方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.meta.ai/blog/introducing-muse-glimmer-open-agentic-model">Introducing Muse Glimmer: An Open Agentic Model That Runs on Your Device | Meta AI Research</a></li>
<li><a href="https://huggingface.co/Efficient-Large-Model/SANA-Video_2B_480p">Efficient-Large- Model / SANA - Video _2B_480p · Hugging Face</a></li>
<li><a href="https://ltx.io/model/ltx-2-5">LTX - 2 . 5 : LTX&#x27;s Latest AI Open-Source Foundation Model | LTX</a></li>

</ul>
</details>

**标签**: `#sglang`, `#LLM inference`, `#release`, `#AI/ML`, `#model serving`

---

<a id="item-2"></a>
## [MCP 路线图：远程服务器标准化为 HTTP，并统一智能体身份认证](https://blog.modelcontextprotocol.io/posts/mcp-roadmap/) ⭐️ 8.0/10

MCP 团队发布了新路线图：自 2026-07-28 版本起，远程 MCP 服务器将被视为与任何其他 HTTP 工作负载无异。路线图还计划标准化 MCP 服务器如何识别并信任代表用户行事的智能体身份。 这直接回应了社区的两大批评：MCP 自定义协议过于复杂，以及其以浏览器为中心的授权模式不适合拥有自身身份的云上智能体。将智能体身份标准化并把远程 MCP 视为普通 HTTP，可降低采用门槛，并提升智能体 AI 工作负载的安全性。 路线图指出，目前 MCP 授权仍需要用户在浏览器中批准访问，而越来越多的调用方是以云工作负载运行的智能体：它们拥有自己的身份、代表不在场的用户行事，或将更小范围的权限委托给子智能体。这些改进建立在现有身份体系和基于 OAuth 的授权基础之上，而非另造一套专有标准。

hackernews · pentagrama · 8月22日 13:31 · [社区讨论](https://news.ycombinator.com/item?id=49399591)

**背景**: 模型上下文协议（MCP）是 Anthropic 于 2024 年 11 月推出的开放标准，旨在统一 AI 系统连接外部数据和工具的方式，此后 OpenAI 和 Google DeepMind 也相继采用。远程 MCP 服务器以往依赖 OAuth 和浏览器中的用户同意等交互式流程，这并不适合智能体之间或云工作负载，因此路线图推动标准化 HTTP 部署与智能体身份。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol</a></li>
<li><a href="https://modelcontextprotocol.io/docs/2026-07-28/getting-started/intro">What is the Model Context Protocol (MCP)? - Model Context Protocol</a></li>
<li><a href="https://www.redhat.com/en/blog/mcp-security-implementing-robust-authentication-and-authorization">MCP security: Implementing robust authentication and authorization</a></li>

</ul>
</details>

**社区讨论**: 评论区对转向普通 HTTP 表示赞同，有人说当初推出自定义新协议是“愚蠢的做法”。也有人持怀疑态度：他们质疑有多少服务器会完整实现路线图，MCP 端点是否真的比 REST 加 skills.md 文件更好用，并提到 MCP 多次转向、功能占用上下文等问题是自己放弃它的原因；还有人开玩笑说看到“MCP”仍会想到“主控程序”（Master Control Program）。

**标签**: `#MCP`, `#AI`, `#protocol`, `#roadmap`, `#agent authentication`

---

<a id="item-3"></a>
## [250M 参数量化 LLM 从零训练，60MB 部署](https://www.reddit.com/r/MachineLearning/comments/1vv2nkh/i_developed_my_own_quantized_llm_from_scratch/) ⭐️ 8.0/10

一位开发者使用 FineWeb 数据集的 300 亿个 token 从零训练了一个 2.5 亿参数的 LLM，并将权重量化到 2 比特以下，最终以 60 MB 的大小部署，在笔记本电脑 CPU 上以约 400 token/秒的速度运行，仅需约 80 MB 内存。该模型的长上下文系统会将 2048 token 之前的旧 token 压缩为 1 比特并存储到磁盘，支持从最多 1 亿 token 的历史中检索信息。 这说明从零构建超紧凑的量化模型并在资源受限设备上高效运行是可行的，同时通过磁盘卸载仍能利用长上下文。这可能推动隐私敏感或低成本场景下的边缘 AI 应用，也挑战了“有用的大语言模型必须拥有数十亿参数和大型 GPU”的传统观念。 该模型没有使用经过训练的嵌入表，而是为 131k 个 token 中的每一个分配了固定的 512 位代码（共 8.4 MB），在 WordSim-353 上的 Spearman 相关系数为 0.619，而随机编码仅为 0.029。磁盘缓存以每 token 约 320 字节（100 万 token 约 320 MB）存储旧 token，模型被训练为从最多 1 亿 token 的磁盘历史中检索答案，但不在这些 token 间进行推理。

reddit · r/MachineLearning · /u/Final-Data-1410 · 8月22日 04:39

**背景**: 量化会将模型权重的精度从 FP16 等较高精度降低到 1–2 比特，从而缩小内存占用并加快推理速度，但会带来一定精度损失。在文本生成时，LLM 会维护一个 KV 缓存来保存过去键值对，以避免重复计算注意力；对于长上下文，这个缓存会变得非常大，因此需要使用压缩、卸载到 CPU 或磁盘等技术。FineWeb 是 Hugging Face 整理的大规模英文网页文本数据集，常用于预训练各种规模的模型。该开发者的方案结合了亚 2 比特量化、带 1 比特压缩的磁盘 KV 缓存和从零训练的小型模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2511.11907v1">KVSwap: Disk-aware KV Cache Offloading for Long-Context On-device Inference</a></li>
<li><a href="https://lzwjava.github.io/fineweb-overview-usage-en">FineWeb Dataset Overview and Usage</a></li>
<li><a href="https://github.com/pprp/Awesome-LLM-Quantization">GitHub - pprp/Awesome-LLM- Quantization : Awesome list for LLM...</a></li>

</ul>
</details>

**社区讨论**: Reddit 上的讨论非常积极；作者表示自己原本担心会被“毒舌”批评，但收到的评论都充满好奇和帮助。用户们深入探讨了技术细节，GitHub 仓库在发布后不久就获得了 7 颗星。

**标签**: `#LLM`, `#quantization`, `#efficient inference`, `#long context`, `#edge AI`

---

<a id="item-4"></a>
## [开源 Roguelike 游戏 DelveRL：专为训练 AI 智能体打造](https://www.reddit.com/r/MachineLearning/comments/1vvii1j/i_built_an_opensource_roguelike_specifically_for/) ⭐️ 8.0/10

一位开发者发布了 DelveRL——一个开源、可人类游玩的 Roguelike 游戏，专为强化学习环境而设计。它具备结构化 API、确定性模拟、程序化关卡、部分可观测性，并附带循环 PPO 训练器，基线结果中位层数达到 18 层，延长运行可达 33 层。 这填补了强化学习研究中的一个空白：既能让人类游玩，又能轻松集成到智能体训练框架中。它降低了研究者和爱好者在丰富策略环境中进行 RL 实验的门槛，类似于 NetHack 但更易上手。 游戏完全本地运行，支持批处理式无渲染环境，并包含基于 LSTM 的循环 PPO 基线。所有代码、训练脚本、模型检查点、桥接文档和原始基准均开源。

reddit · r/MachineLearning · /u/SnyderConsulting · 8月22日 17:32

**背景**: Roguelike 是一种程序化生成关卡、带有永久死亡机制的游戏类型，玩家需要逐层探索、战斗并管理资源。强化学习（RL）通过奖励机制训练智能体做出序列决策，PPO（近端策略优化）是常用算法，而循环 PPO 则利用 LSTM 网络处理部分可观测性问题——即智能体只能看到环境的局部信息，需要记忆来推断隐藏状态。DelveRL 提供结构化 API 和确定性模拟，正是为了简化这类 RL 智能体的集成过程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sb3-contrib.readthedocs.io/en/master/modules/ppo_recurrent.html">Recurrent PPO — Stable Baselines3 - Contrib 2.9.0 documentation</a></li>
<li><a href="https://arxiv.org/abs/2204.08967">[2204.08967] When Is Partially Observable Reinforcement Learning Not Scary?</a></li>

</ul>
</details>

**标签**: `#reinforcement learning`, `#game environment`, `#open-source`, `#AI training`, `#procedural generation`

---

<a id="item-5"></a>
## [SemiAnalysis：开源模型追平闭源时间每代减半](https://newsletter.semianalysis.com/p/are-open-models-catching-up) ⭐️ 8.0/10

SemiAnalysis 发布报告，将大模型历史划分为早期扩展、推理和智能体三个时代，发现开源模型每代追平闭源前沿模型的时间都在减半。在智能体时代，Kimi K2.6 用 4.8 个月超越 Opus 4.5，GLM-5.2 用 6 个月超过 GPT-5.2。 这种加速追赶意味着模型层正在商品化，威胁到 Anthropic 等闭源实验室的定价权——后者部分年化收入超过 650 亿美元，依赖编程和智能体能力。对企业和开发者而言，强大的开源替代方案可能削弱专有前沿模型的溢价。 文章指出 GLM 5.3、Kimi K3 等开源模型已能胜任许多曾支撑 Anthropic 收入的编程与智能体任务，但提醒基准测试并非全部，Anthropic 的产品化能力仍是其优势。这种追平是在特定任务上的能力对齐，并非完整功能或体验的等同。

telegram · zaihuapd · 8月22日 08:26

**背景**: 大语言模型经历了几个不同阶段：早期预训练扩展、以推理为核心的推理时代，以及当前让 AI 系统自主感知、推理和行动的智能体时代。Kimi K2.6（1 万亿参数的 MoE 模型）和 GLM-5.2（744B 参数、100 万上下文窗口）等开源模型在长程编程和智能体任务上取得了接近最先进的成绩。SemiAnalysis 的分析量化了这些开源模型在各个时代追赶专有前沿模型的速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/moonshotai/Kimi-K2.6">moonshotai/Kimi-K2.6 · Hugging Face</a></li>
<li><a href="https://huggingface.co/zai-org/GLM-5.2">zai-org/GLM-5.2 · Hugging Face</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained | MIT Sloan</a></li>

</ul>
</details>

**标签**: `#AI`, `#open-source`, `#large-language-models`, `#industry-analysis`, `#model-competition`

---