---
layout: default
title: "Horizon Summary: 2026-09-01 (ZH)"
date: 2026-09-01
lang: zh
---

> 从 37 条内容中筛选出 7 条重要资讯。

---

1. [库克卸任苹果 CEO，特努斯接棒主攻 AI](#item-1) ⭐️ 9.0/10
2. [谷歌从 Chrome 网上应用店移除 Manifest V2 扩展，含 uBlock Origin](#item-2) ⭐️ 8.0/10
3. [NAT：推动互联网走向中心化的“原罪”](#item-3) ⭐️ 8.0/10
4. [滑动窗口注意力在长上下文推理上胜过线性注意力](#item-4) ⭐️ 8.0/10
5. [SynthFin-AML 数据集揭示 GNN 反洗钱模型中的时间泄漏问题](#item-5) ⭐️ 8.0/10
6. [OpenClaw 2.0 发布史上最大更新，汇集逾 1.6 万个拉取请求](#item-6) ⭐️ 8.0/10
7. [DeepSeek 发布实验性多模态模型 V4-Flash-Vision-Exp](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [库克卸任苹果 CEO，特努斯接棒主攻 AI](https://www.bloomberg.com/news/articles/2026-08-30/apple-s-new-ceo-john-ternus-takes-reins-from-tim-cook-focusing-on-ai) ⭐️ 9.0/10

8 月 31 日是库克担任苹果 CEO 的最后一天，9 月 1 日起 51 岁的硬件工程老将约翰·特努斯接任 CEO，库克留任执行主席。特努斯的首要任务是推动 AI 落地，补齐 Siri 升级延期等短板，9 月 9 日发布会预计亮相首款折叠屏 iPhone。 苹果 CEO 更替极为罕见，且影响全球科技行业格局，因为苹果是全球最具影响力的科技公司之一。新任 CEO 明确将战略重心转向 AI，并推出折叠屏 iPhone，这将对智能手机和 AI 产业产生广泛影响。 据称首款折叠屏 iPhone 将配备 12GB 内存，并深度植入 Siri AI，可结合屏幕、日历与相机理解现实场景。库克并未完全离开苹果，而是留任执行主席。

telegram · zaihuapd · 8月31日 10:21

**背景**: 蒂姆·库克自 2011 年起接替史蒂夫·乔布斯担任苹果 CEO，任职超过十年。Apple Intelligence 是苹果 2024 年推出的 AI 功能套件，结合端侧与服务器处理，提供写作辅助、通知摘要、照片处理以及 ChatGPT 集成等功能；Siri 则是苹果的语音助手，目前正通过这些 AI 能力进行升级。新 CEO 出身硬件工程，预示苹果将重点推进搭载 AI 能力的设备。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence</a></li>
<li><a href="https://www.apple.com/apple-intelligence/">Apple Intelligence and Siri - Apple</a></li>

</ul>
</details>

**标签**: `#Apple`, `#CEO transition`, `#AI`, `#Tim Cook`, `#John Ternus`

---

<a id="item-2"></a>
## [谷歌从 Chrome 网上应用店移除 Manifest V2 扩展，含 uBlock Origin](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

谷歌已从 Chrome 网上应用店移除所有剩余的 Manifest V2（MV2）扩展，包括广受欢迎的广告拦截器 uBlock Origin。此举发生在 Chrome 151 最终弃用 MV2 支持、并从浏览器源码树中删除最后 MV2 代码之后。 这一变化影响了数百万依靠 uBlock Origin 进行广告拦截和隐私保护的用户。它也引发了更广泛的担忧：一家公司对浏览器扩展和网络标准拥有单方面控制权，促使许多用户考虑转向 Firefox。 Manifest V3 被谷歌宣称可提升安全性、隐私性和性能，但它通过以 declarativeNetRequest 取代 webRequest API 来限制广告拦截扩展，从而减少了过滤规则集。Firefox 仍支持 uBlock Origin 的完整功能，其开发者指出该扩展在 Firefox 上表现最佳。

hackernews · twapi · 8月31日 21:10 · [社区讨论](https://news.ycombinator.com/item?id=49514878)

**背景**: Manifest V2 和 Manifest V3 是 manifest（manifest.json）文件的版本，该文件定义了浏览器扩展的功能和权限。谷歌自该规范公布后一直在将 Chrome 迁移到 MV3，声称这可通过阻止扩展执行远程托管的代码来提升安全性。弃用时间表分批次从 Chrome 网上应用店移除 MV2 扩展，到 2026 年 8 月 31 日所有剩余扩展均被移除。uBlock Origin 是一款免费开源的广告拦截扩展，以高效、易用著称，可在 Firefox 和基于 Chromium 的浏览器上使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline">Manifest V 2 support timeline | Chrome for Developers</a></li>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3">Extensions / Manifest V3 | Chrome for Developers</a></li>
<li><a href="https://en.wikipedia.org/wiki/UBlock_Origin">uBlock Origin - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了强烈担忧，认为广告拦截现在对不太懂技术的用户而言是一个安全问题，同时指出谷歌等公司未能自行过滤恶意广告。许多用户表示已改用 Firefox，一位评论者提到 uBlock Origin 在 Firefox 上表现最佳，这反映出对 Chrome 单方面控制的不信任情绪。

**标签**: `#Chrome`, `#Manifest V3`, `#privacy`, `#ad-blocking`, `#browser extensions`

---

<a id="item-3"></a>
## [NAT：推动互联网走向中心化的“原罪”](https://dreamstation.systems/personal/ntppost.html) ⭐️ 8.0/10

一篇文章提出，网络地址转换（NAT）是导致互联网中心化的最早推手之一，并引发了社区的热烈讨论，其中包括 Linux 当前 NAT 系统实现者 Rusty Russell 的反思性评论。文章将 NAT 为了节省地址所做的权衡视为历史转折点，使普通用户的自建服务器和直接点对点连接变得更加困难。 这一讨论之所以重要，是因为 NAT 的设计选择塑造了现代互联网：它加速了客户端—服务器模式，让“设备必须连接云端而不是彼此直连”的观念成为常态，并催生了 NAT 穿透和云中转服务的市场。围绕 IPv6 普及、运营商级 NAT（CGNAT）以及将端到端连接还给用户的提议，这场争论仍在继续。 Linux NAT 实现者 Rusty Russell 表示，他当年选择不做端口预留，而是尽可能在一个 IP 上塞入更多连接，只要远端地址不同就能区分；但这也意味着来自其他地址的入站流量无法路由，用户因此失去公网端点——成了“穷人防火墙”。评论者还区分了普通家庭 NAT（可通过端口转发/UPnP 解决）和运营商级 NAT，后者被真正视为限制自由的罪魁祸首。

hackernews · robinpie · 8月31日 02:23 · [社区讨论](https://news.ycombinator.com/item?id=49504905)

**背景**: 网络地址转换（NAT）允许多台私有网络设备通过改写数据包中的 IP 地址和端口，共用一个公网 IP 上网。NAT 最初是为了缓解 IPv4 地址枯竭，同时也通过隐藏内部主机提供了基本的防护。由于 NAT 打破了互联网原有的端到端模型，人们发明了 STUN、TURN、ICE 等技术，让应用可以发现并穿透 NAT 映射，实现点对点连接。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.geeksforgeeks.org/computer-networks/network-address-translation-nat/">Network Address Translation ( NAT ) - GeeksforGeeks</a></li>
<li><a href="https://en.wikipedia.org/wiki/NAT_traversal">NAT traversal - Wikipedia</a></li>
<li><a href="https://liveapi.com/blog/nat-traversal/">What Is NAT Traversal ? STUN , TURN , ICE Explained - LiveAPI Blog</a></li>

</ul>
</details>

**社区讨论**: 评论区观点多样：Rusty Russell 坦诚地为当年的实现选择道歉；solatic 哀叹开放互联网的消逝，认为 NAT 让所有人觉得客户端—服务器模式是理所当然；elric 反驳说普通 NAT 没问题，只有运营商级 NAT 才真正限制自由；miki123211 则认为是把现实世界的肉身边界规范套用到了网络空间，才是根本性错误。

**标签**: `#NAT`, `#networking`, `#Internet history`, `#centralization`, `#infrastructure`

---

<a id="item-4"></a>
## [滑动窗口注意力在长上下文推理上胜过线性注意力](https://www.reddit.com/r/MachineLearning/comments/1w3j1vw/slidingwindow_attention_beats_linear_on/) ⭐️ 8.0/10

一篇新的 arXiv 预印本（2608.28444）报告称，带 sinks 的滑动窗口注意力在 Needle-in-a-Haystack 和 BABILong 长上下文推理基准上，性能比后训练线性注意力变体高出 2 到 10 倍。作者建议改用 SWA，而不是对线性模型进行后训练。 这挑战了高效注意力研究的主要方向，表明更简单且已有的基线被低估了。如果得到验证，它可能会改变 LLM 架构的选择，并节省大量后训练算力。 论文称，带 sinks 的滑动窗口注意力不需要后训练，运行速度快，且内存占用低。在两个选定任务上报告的差距很大，但该发现仅来自单一预印本，需要独立验证。

reddit · r/MachineLearning · /u/Justgototheeffinmoon · 8月31日 16:35

**背景**: 标准 Transformer 注意力在序列长度上呈二次方开销，使得长上下文非常昂贵。线性注意力旨在将其降至线性扩展，但通常需要后训练才能达到同等质量。滑动窗口注意力（SWA）限制每个 token 只关注固定窗口内的邻近 token，从而降低成本；加入“sinks”（吸收额外注意力的特殊 token）有助于保留全局信息。BABILong 是一个长上下文推理基准，通过长文档上的多跳问答等任务来测试模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.28444">[2608.28444] Sliding-window beats linear attention</a></li>
<li><a href="https://www.digitalocean.com/community/tutorials/sliding-window-attention-efficient-long-context-models">Sliding Window Attention: Efficient Long-Context Modeling | DigitalOcean</a></li>
<li><a href="https://github.com/booydar/babilong">GitHub - booydar/ babilong : BABILong is a benchmark for LLM...</a></li>

</ul>
</details>

**标签**: `#attention mechanisms`, `#long-context reasoning`, `#linear attention`, `#LLMs`, `#efficiency`

---

<a id="item-5"></a>
## [SynthFin-AML 数据集揭示 GNN 反洗钱模型中的时间泄漏问题](https://www.reddit.com/r/MachineLearning/comments/1w3imxy/your_gnn_is_probably_just_an_overcomplicated_mlp/) ⭐️ 8.0/10

该帖子介绍了 SynthFin-AML v10.0，一个包含 10 万个节点和 120 万条边的合成金融图数据集，通过严格的 3 快照因果划分来防止 GNN 训练中的时间泄漏。作者将调优后的 LightGBM 与 GraphSAGE 进行基准测试，在严格时间划分下报告 PR-AUC 分别为 0.848 和 0.881。 这一工作意义重大，因为它揭示了一个关键的评估缺陷：许多动态图上的 GNN 模型可能只是过度复杂的 MLP，在训练时通过看到未来的边而作弊。通过提供一个具体的数据集和评估标准，它推动图机器学习社区走向更可靠的基准测试，尤其是在反洗钱和其他对时间敏感的应用中。 该数据集强制执行严格的 3 快照时间点划分：训练图使用截至第 7 天的边，验证图使用截至第 8 天的边，测试图使用截至第 10 天的边，通过物理上分离时间窗口来限制 GNN 的感受野。它还通过让欺诈和零售交易金额共享相同的对数正态分布（μ=8.517，σ=0.8）来消除表格泄漏。作者已将基准测试提交至 PyTorch Geometric，即 PR \#10774。

reddit · r/MachineLearning · /u/Glabmayt2075 · 8月31日 16:21

**背景**: 图神经网络中的时间泄漏是指在动态图的静态快照上训练 GNN 时，模型在训练过程中能够看到未来的边、特征或事件，从而导致性能虚高。标准的随机转导划分在金融交易网络上根本行不通，因为这类划分违背了时间箭头。动态图基准测试需要采用时间感知的评估方法（如因果划分），以确保模型学习到真正的模式，而不是记住未来信息。SynthFin-AML 建立在先前合成反洗钱数据集的基础上，这些数据集用于在保护隐私的同时对统计和机器学习方法进行基准测试。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kumo.ai/pyg/concepts/data-leakage/">Data Leakage in Graph ML: When Future Information Contaminates Training | Kumo.ai | Kumo.ai</a></li>
<li><a href="https://kumo.ai/pyg/concepts/temporal-graph/">Temporal Graphs in PyG: Time-Evolving Graph Neural Networks | Kumo.ai | Kumo.ai</a></li>

</ul>
</details>

**标签**: `#graph neural networks`, `#temporal leakage`, `#dataset`, `#anti-money laundering`, `#evaluation methodology`

---

<a id="item-6"></a>
## [OpenClaw 2.0 发布史上最大更新，汇集逾 1.6 万个拉取请求](https://openclaw.ai/blog/openclaw-2-accidentally) ⭐️ 8.0/10

OpenClaw 于 8 月 30 日发布其史上最大更新 2.0，汇集了来自 933 名贡献者（含 569 名首次参与者）的逾 1.6 万个拉取请求。本次更新全面改造了安装、消息、记忆、技能、模型、浏览器、插件与安全，并新增共享云端会话以支持多人协作。 此次发布标志着开源 AI 助手生态系统的一个重要里程碑，展示了规模空前的社区驱动开发。全方位的更新可能显著改善易用性，并吸引更广泛的用户群体。 团队为此刻意将近七周未发布新版本，以准备此次更新。新版本简化了安装流程，重建了浏览器端体验，并引入了支持多人协作的共享云端会话。

telegram · zaihuapd · 8月31日 04:38

**背景**: OpenClaw 是一个免费开源的自主任 AI 代理，通过大语言模型执行任务，并以消息平台作为其主要用户界面。该项目吸引了庞大而活跃的社区；本次更新的 1.6 万个拉取请求约占项目迄今全部拉取请求的一半。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openclaw.ai/">OpenClaw — Open -Source AI Assistant</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenClaw">OpenClaw</a></li>

</ul>
</details>

**标签**: `#open-source`, `#software-release`, `#AI-assistant`, `#development`, `#community`

---

<a id="item-7"></a>
## [DeepSeek 发布实验性多模态模型 V4-Flash-Vision-Exp](https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-Vision-Exp) ⭐️ 8.0/10

DeepSeek 发布了 V4 系列首款实验性多模态模型 DeepSeek-V4-Flash-Vision-Exp，在 V4-Flash 架构上加入视觉模块并继续训练。该版本大幅提升了多模态 agent 能力，ApexBench 从 26.2 升至 36.5，文本 agent 任务表现基本持平。 此次发布标志着 DeepSeek 在多模态 agent 能力和开放权重研究方面的推进，为社区提供了可用于实验的强视觉-语言模型。它在 agent 相关基准上的显著提升也表明，随着 AI 系统从聊天机器人扩展到工具调用和自主工作流，这类能力正变得越来越重要。 该模型为实验性版本，基于 V4-Flash 架构，可能不代表最终 V4 稳定版的全部能力。其基准提升主要集中在多模态 agent 任务上：ApexBench（Pass@1）从 26.2 升至 36.5，而纯文本 agent 性能基本持平，表明视觉模块是主要差异点。

telegram · zaihuapd · 8月31日 11:41

**背景**: 开放权重（open weights）意味着模型的训练参数公开可下载，任何人都能运行它，但不一定包含完整的训练代码和数据。多模态 agent 是集成视觉、音频和文本的 AI 系统，能理解并作用于丰富的真实世界输入，代表了超越纯文本界面的演进方向。ApexBench 是一个多模态 agent 基准，使用 Pass@1 分数评估模型在结合视觉与文本信息时完成 agent 任务的能力。DeepSeek 是一家以开放权重发布高能力模型而闻名的 AI 实验室，本次实验性视觉模型是其 V4 系列的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.datalearner.com/en/benchmarks/apexbench">ApexBench : Multimodal Agent Benchmark and... | DataLearnerAI</a></li>
<li><a href="https://www.ai21.com/glossary/foundational-llm/open-weights-model/">What is an Open - Weights Model ? | AI21</a></li>
<li><a href="https://fast.io/resources/ai-agent-multimodal-processing/">AI Agent Multimodal Processing: The 2026 Guide | Fastio</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#multimodal`, `#AI model release`, `#open weights`, `#agent`

---