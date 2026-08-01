---
layout: default
title: "Horizon Summary: 2026-08-01 (ZH)"
date: 2026-08-01
lang: zh
---

> 从 36 条内容中筛选出 5 条重要资讯。

---

1. [无状态 MCP 2.0 规范重新点燃兴趣并催生新工具](#item-1) ⭐️ 9.0/10
2. [华为开源 505B 参数 MoE 大模型 openPangu-2.0-Pro](#item-2) ⭐️ 9.0/10
3. [DeepSeek V4 Flash 0731：每百万输出 tokens 仅 0.28 美元的前沿级模型](#item-3) ⭐️ 8.0/10
4. [MiniMax 将于 8 月 3 日开源多模态视频模型 H3](#item-4) ⭐️ 8.0/10
5. [德国法院裁定 AI 音乐公司 Suno 侵犯版权](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [无状态 MCP 2.0 规范重新点燃兴趣并催生新工具](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 9.0/10

2026-07-28 发布的 Model Context Protocol 规范（MCP 2.0）使协议变为无状态，用单个 HTTP 请求取代了原来的两次握手建会话流程。Simon Willison 本周构建了三个实现，包括开源的 mcp-explorer 命令行工具和 datasette-mcp。 这是 MCP 自推出以来最重大的变化，大幅降低了实现复杂度，并且让工具比基于 shell 的智能体更易于审计和控制。这可能会扩大 MCP 在 AI 智能体工具领域的采用，尤其有利于在笔记本电脑上运行的较小模型。 旧版 MCP 需要两次 HTTP 请求：一次 initialize 调用返回 Mcp-Session-Id，随后再带该头部调用 tools/call。新的无状态版本只用一个 POST 请求，通过 MCP-Protocol-Version、Mcp-Method 和 Mcp-Name 头部完成，不再需要服务端会话状态和会话感知路由。

rss · Simon Willison · 7月31日 23:13

**背景**: MCP 是 Anthropic 于 2024 年 11 月推出的开放标准，旨在通过标准化接口将 AI 助手连接到外部工具和数据源。它在 2025 年人气飙升，但部分被主要教导模型如何使用工具的 Claude Skills 所掩盖；这次无状态更新解决了关键的扩展性和复杂度痛点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>
<li><a href="https://www.arcade.dev/blog/mcp-going-stateless/">MCP Is Going Stateless. Here&#x27;s What That Means - Arcade.dev</a></li>

</ul>
</details>

**标签**: `#MCP`, `#AI agents`, `#protocol`, `#LLM tools`, `#specification`

---

<a id="item-2"></a>
## [华为开源 505B 参数 MoE 大模型 openPangu-2.0-Pro](https://huggingface.co/openpangu/openPangu-2.0-Pro) ⭐️ 9.0/10

华为在 Hugging Face 上开源了 openPangu-2.0-Pro，这是一个基于昇腾 NPU 训练的 505B 参数混合专家（MoE）语言模型，使用了约 34T tokens 的训练数据，并支持 512k 上下文窗口。其“Thinking”版本在 AIME 2026 数学基准上得分为 95.4，在 GPQA-Diamond 上得分为 87.9。 此次开源是全球科技巨头在开源领域的一个重要里程碑，展示了华为在 NPU 硬件、训练基础设施和模型开发方面的全栈 AI 能力。它提供了一个先进的 MoE 替代方案，可能加速基于昇腾的 AI 生态系统的采用，并进一步推动开放权重大模型的竞争。 该架构结合了多头潜在注意力（MLA）与 DSA（DeepSeek 稀疏注意力）和 SWA（滑动窗口注意力）的混合分层设计，并配有 3 头多 token 预测（MTP）自投机解码模块。后训练阶段完成了快慢合一微调与多专项强化学习，每个 token 激活的参数量约为 18B。

telegram · zaihuapd · 7月31日 06:50

**背景**: MoE（混合专家）模型每个 token 只激活总参数中的一小部分，从而在推理成本可控的情况下实现超大规模模型。MLA（多头潜在注意力）通过压缩潜在表示来减少键值缓存内存，而 SWA（滑动窗口注意力）将注意力限制在局部窗口内，DSA（稀疏注意力）则采用稀疏注意力模式以提高效率。MTP（多 token 预测）允许模型同时预测多个未来 token，可用于投机解码以加速生成。华为的昇腾 NPU 是中国在大规模 AI 训练方面对 Nvidia GPU 的一种替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/google-cloud/attention-evolved-how-multi-head-latent-attention-works-427a922dd6a1">Attention Evolved: How Multi - Head Latent Attention Works | Medium</a></li>
<li><a href="https://www.emergentmind.com/topics/sliding-window-attention-fbe25958-222c-4175-aa0e-3ec07d794708">Sliding Window Attention</a></li>
<li><a href="https://www.mox.es/2026/05/10/multi-token-prediction-mtp-how-llms-learn-to-look-ahead/">Multi - Token Prediction ( MTP ): How LLMs Learn to Look Ahead...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#MoE`, `#Huawei`, `#open-source`, `#AI`

---

<a id="item-3"></a>
## [DeepSeek V4 Flash 0731：每百万输出 tokens 仅 0.28 美元的前沿级模型](https://artificialanalysis.ai/models/deepseek-v4-flash) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek-V4-Flash-0731 的官方公开测试版本，此前的额外后训练提升了代理、编程和工具调用能力。据报道，该模型以每百万输出 tokens 0.28 美元的价格实现了接近前沿水平的智能。 该发布将接近前沿水平的基准测试表现与极低的 API 定价相结合，可能改变人们对大模型定价的预期，并给竞争对手带来压力。对于关注 token 成本的开发者和高频 API 用户来说尤其重要。 DeepSeek-V4-Flash 是一个专家混合（MoE）模型，总参数量为 284B，激活参数量为 13B，上下文窗口为 1M tokens。0731 版本是于 2026 年 7 月 31 日发布的官方公开测试版，社区用户还指出无损 Q8 量化版本约 162GB，适合本地部署。

hackernews · theanonymousone · 7月31日 07:59 · [社区讨论](https://news.ycombinator.com/item?id=49120299)

**背景**: 前沿 AI 模型通常指在特定时间最先进的通用人工智能模型。LLM API 通常分别对输入 tokens 和输出 tokens 计费，其中输出 tokens 的价格通常是输入的 2-5 倍。DeepSeek-V4-Flash 是一款为高效推理设计的专家混合（MoE）模型，每次处理 token 时只激活一部分参数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ollama.com/library/deepseek-v4-flash">deepseek-v4-flash - ollama.com</a></li>
<li><a href="https://www.orcarouter.ai/blog/deepseek-v4-flash-official-release">DeepSeek V4 Flash: Official Release, Explained - orcarouter.ai</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work | NVIDIA Glossary</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体非常积极：有用户称该模型是“极好的”日常驱动模型，并指出它以每百万输出 tokens 仅 0.28 美元的价格提供了约 GLM 5.2/Gemini 3.6 级别的智能，还有可用于本地部署的 162GB Q8 版本。也有用户猜测即将推出的 V4 Pro 可能媲美或超越 Opus 5，还有人质疑 Hugging Face 托管的经济性，并询问 DeepSeek 是否会发布优化的编程 agent harness。

**标签**: `#AI/ML`, `#DeepSeek`, `#Model Release`, `#Performance`, `#Pricing`

---

<a id="item-4"></a>
## [MiniMax 将于 8 月 3 日开源多模态视频模型 H3](https://modelscope.cn/models/MiniMax/MiniMax-H3) ⭐️ 8.0/10

MiniMax 宣布其全模态视频模型 H3 将于 8 月 3 日在魔搭社区开源。H3 原生支持文本、图像、音频和视频的理解与生成，可生成最高 2K 分辨率、15 秒并带有原生立体声的视频。 开源最先进的多模态视频模型将降低开发者与创作者的使用门槛，有望加速影视、广告、电商和游戏领域的 AI 视频制作。此举还增强了开源 AI 生态，并与专有视频生成模型形成竞争。 该模型面向商业内容创作，具备多维度精准编辑控制能力，可将多种参考素材融合为连贯输出，生成字幕、品牌信息、特效、产品展示及 UI 动效等内容。它被描述为开放权重模型，但具体许可证条款尚未完全公布。

telegram · zaihuapd · 7月31日 12:37

**背景**: 魔搭（ModelScope）是阿里巴巴旗下的一站式模型社区，用于模型的探索、部署与训练。H3 是一种全模态（omni-modal）生成模型，可在单一模型中联合理解文本、图像、视频和音频等模态，从而实现如带同步音频的视频生成等任务，而这些任务通常需要多个独立模型完成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H 3 : An Open Model Breaking the Boundaries Between Tasks...</a></li>
<li><a href="https://fal.ai/minimax-h3">MiniMax H 3 - Open-Weights General-Purpose Multimodal Video Model</a></li>
<li><a href="https://modelscope.ai/">ModelScope</a></li>

</ul>
</details>

**标签**: `#multimodal`, `#video generation`, `#open source`, `#MiniMax`, `#AI model`

---

<a id="item-5"></a>
## [德国法院裁定 AI 音乐公司 Suno 侵犯版权](https://www.dw.com/en/german-court-rules-that-ai-music-firm-suno-violated-copyrights/a-78152227) ⭐️ 8.0/10

慕尼黑地区法院裁定，AI 音乐公司 Suno 未经许可使用受版权保护的音乐训练模型，侵犯了版权，须披露非法所得并支付数额待定的赔偿。Suno 表示不认同判决，将评估包括上诉在内的所有选项。 这是全球首批专门针对 AI 音乐生成的重大司法裁决之一，可能为版权法如何适用于 AI 训练数据树立全球先例。此案由德国集体管理组织 GEMA 提起，可能重塑生成式 AI 公司与音乐权利人之间的许可谈判格局。 GEMA 于 2025 年 1 月提起诉讼，并在庭审中演示了用 Suno 生成的歌曲与原作品高度相似。GEMA 代表德国逾 9.5 万名音乐人及全球超 200 万名权利持有人。

telegram · zaihuapd · 7月31日 13:11

**背景**: Suno 是一个生成式 AI 音乐平台，于 2023 年 12 月推出网页应用并与微软合作成为 Copilot 插件后广泛可用。生成式 AI 模型通常通过分析大量现有作品的数据集进行学习，由此引发了关于此类训练行为是否构成版权侵权或合理使用的争议。GEMA 是德国一家由政府授权的集体管理组织和表演权组织，为作曲家、词作者和音乐出版商管理并维护音乐版权。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Suno_AI">Suno AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/GEMA_%28German_organization%29">GEMA (German organization) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI`, `#copyright`, `#legal`, `#music`, `#Suno`

---