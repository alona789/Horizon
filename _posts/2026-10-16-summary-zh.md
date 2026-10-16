---
layout: default
title: "Horizon Summary: 2026-10-16 (ZH)"
date: 2026-10-16
lang: zh
---

> 从 42 条内容中筛选出 6 条重要资讯。

---

1. [Meta 发布 Muse Spark Open：面向本地部署的 816B 开放权重模型](#item-1) ⭐️ 8.0/10
2. [Goodfire 的 Nick Cammarata 主张神经网络其实是「干净的」](#item-2) ⭐️ 8.0/10
3. [Citizen Lab：以色列公司 Discover Tech 将定向广告变成零点击间谍软件投放渠道](#item-3) ⭐️ 8.0/10
4. [Libreboot 26.10 “Ominous Olive” 发布，新增 UEFI/EDK2 与 Chromebook 支持](#item-4) ⭐️ 8.0/10
5. [Anthropic 在 IPO 前向投资者披露季度收入增长近 50%，达 168 亿美元](#item-5) ⭐️ 8.0/10
6. [MIT 与 PNAS 研究：随机连接的神经元单元可自组装出学习回路](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Meta 发布 Muse Spark Open：面向本地部署的 816B 开放权重模型](https://research.meta.ai/blog/muse-spark-open) ⭐️ 8.0/10

Meta 在 Hugging Face 上以 meta-models/Muse-Spark-Open-816B-A42B 仓库发布了 Muse Spark Open，这是一个总参数量 816B、激活参数量 42B 的大型开放权重模型。官方表示该版本针对本地部署做了优化，并提供了覆盖 Unsloth、MLX 等推理运行器的部署文档，甚至可在 Mac Studio 上运行。 这是 Meta 又一次重量级开放权重发布，使其在本地部署赛道上直接与 Qwen、GLM 展开对比。由于许可证对商业化的模型服务加以限制，这次发布也重新点燃了业界对“开放权重”真正含义及其实际自由度的争论。 该许可证允许一般性使用，但禁止“模型即服务”（Model as a Service）行为，即通过 API 或类似接口向第三方提供模型输出——只要使用方及其关联公司合计总收入超过 2000 万美元便受此限制。早期第三方评测显示，Muse Spark Open 的成绩落后于 Qwen3.8 Flash Next 和 GLM 5.3 Flash，而后者据称可在单张 B300 上运行。

hackernews · bigwheels · 10月15日 17:47 · [社区讨论](https://news.ycombinator.com/item?id=50107379)

**背景**: 开放权重模型会公开可供下载的训练数值参数，但与开源软件不同，它们通常附带自定义许可证，可能限制商业用途，因此“开放权重”并不等于经 OSI 认证的开源。Muse Spark Open 采用混合专家（MoE）架构，每个 token 只经过少数几个专家子网络：816B 的总参数量决定了加载模型所需的显存/内存大小，而 42B 的激活参数量决定了每个 token 的计算量与速度。MLX、Unsloth 等本地部署工具链让用户可以在自己的硬件上运行这类模型，而不必按 token 支付 API 费用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vettedconsumer.com/mixture-of-experts-moe-explained-why-active-parameters-decide-what-runs-on-your-machine/">Mixture - of - Experts (MoE), Explained: Why “ Active Parameters ”...</a></li>
<li><a href="https://github.com/Open-Weights/Definition">GitHub - Open-Weights/Definition: Definition for Open Weights ... Open-Weight AI Model Licenses: Commercial Use Rules Explained Open-Weight License Landscape 2026 - Presenc AI Open Weight License Explorer - a Hugging Face Space by open ... Open Weight Definition (OWD)</a></li>
<li><a href="https://www.layer3labs.io/open-weights/best-open-weights-ai-models">Open-Weight AI Models List: Best for Business (2026)</a></li>

</ul>
</details>

**社区讨论**: 评论区观点分化：有人认为该许可证意味着它并非真正的开放权重，有用户直接引用了超过 2000 万美元收入即禁止以 API 方式提供“模型即服务”的条款；也有人称赞 Meta 让模型几乎能在从 Unsloth 到 MLX 的所有运行器上跑起来。关注评测的人指出其性能落后于 Qwen3.8 Flash Next 和 GLM 5.3 Flash，还有用户因为本地机器扛不住这个体量而改经 OpenRouter 调用。一个反复出现的战略观点是：Meta 正试图通过免费分发让自家模型成为标准，从而构建生态护城河。

**标签**: `#AI`, `#open-weight models`, `#Meta`, `#LLM`, `#licensing`

---

<a id="item-2"></a>
## [Goodfire 的 Nick Cammarata 主张神经网络其实是「干净的」](https://already-clean.goodfire.com/) ⭐️ 8.0/10

曾在 OpenAI 从事早期机械可解释性研究、现任职于 Goodfire 的 Nick Cammarata 发布了一篇新文章（托管于 already-clean.goodfire.com），主张神经网络在本质上是「干净的」、可被解释的，反驳了长期以来认为特征因叠加（superposition）而纠缠不清的悲观看法。他同时在 X 上发布了发布帖进行宣传，该观点在 Hacker News 上引发了大规模且多为质疑的讨论，获得 489 分和 187 条评论。 如果神经网络确实是「干净的」，而非重度依赖叠加，那么机械可解释性将变得远比想象中容易，这对依赖理解模型内部行为的 AI 安全与对齐工作意义重大。因此，这篇文章直接卷入了关于可解释性究竟「可解」还是「无解」的长期战略争论。 该论证以一份证据汇编的形式呈现，重新审视那些出了名「混乱」的神经元、列举工具失效之处以及多义性（polysemanticity）仍然藏身的地方，而非提出某项单一的新实验。值得注意的是，Cammarata 表示自己曾在 OpenAI 参与早期机械可解释性工作并因此变得悲观，因此这篇文章明显是对他此前立场的反转。

hackernews · themgt · 10月15日 16:04 · [社区讨论](https://news.ycombinator.com/item?id=50105647)

**背景**: 机械可解释性是可解释 AI 的一个子领域，试图把神经网络内部的算法、回路和概念逆向工程成人类能够理解的形式。其核心障碍之一是叠加（superposition）：网络通过把特征排列在近乎正交的方向上，在其激活中塞入比神经元数量更多的稀疏特征，从而产生对看似无关输入都有反应的「多义」神经元。Goodfire 是一家位于旧金山的可解释性初创公司，专注于绘制并编辑模型内部的几何结构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanistic_interpretability">Mechanistic interpretability - Wikipedia</a></li>
<li><a href="https://www.greaterwrong.com/posts/8EyCQKuWo6swZpagS/suphttps-imgur-com-a-ufttll0erposition-is-not-just-neuron">Superposition is not &quot;just&quot; neuron polysemanticity - LessWrong...</a></li>
<li><a href="https://www.goodfire.com/">Goodfire AI</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者大多持怀疑态度，bluejay2387 认为这些主张「超出了实际所能证明的范围」，并指出特征复杂度的渐进增长以及「彩票假说」类现象与参数过载并不互斥。dleeftink 等人则质疑为何要把神经元简化为可互换的特征，认为神经元产生的外部语境与由来承载着不可替代的信息；antics 则把该文形容为一份「庞大的证据汇编」，意在论证「为 AI 基因组测序」比想象中更容易。

**标签**: `#mechanistic-interpretability`, `#neural-networks`, `#AI-alignment`, `#AI-research`, `#superposition`

---

<a id="item-3"></a>
## [Citizen Lab：以色列公司 Discover Tech 将定向广告变成零点击间谍软件投放渠道](https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/) ⭐️ 8.0/10

Citizen Lab 发布研究报告，指称以色列公司 Discover Tech 滥用定向广告基础设施对受害者进行画像、跟踪，并向其移动设备投放无需任何用户操作的零点击雇佣式间谍软件；《卫报》和 The Verge 于 2026 年 10 月 15 日报道了该发现。报告描述广告生态被改造成既能分发载荷、又能充当命令与控制（C&amp;C）通道的工具，而不再是需要用户点击的传统恶意广告诱饵。 如果该指控得到证实，这将是一种全新的攻击向量：几乎每个应用和网站都在使用的普通广告竞价基础设施，会变成政府级监控工具的隐蔽投放通道，进一步侵蚀用户、发布商与广告中间商之间本就脆弱的信任。它同时扩大了责任真空——间谍软件厂商、广告交易平台、需求方平台（DSP）和数据经纪商都在这条链条上，但没有任何一方明确为滥用行为负责。 据报道，该研究较为详细地披露了感染流程和命令与控制（C&amp;C）环节，但对于究竟靠什么技术机制实现无需用户任何操作的安装，仍语焉不详——安全工程师已指出这是整份报告最薄弱的一环。报告还牵涉一家以色列商业公司，延续了雇佣式监控企业以表面上民用商业外衣运作的惯常模式。

hackernews · jcomp · 10月15日 10:43 · [社区讨论](https://news.ycombinator.com/item?id=50101813)

**背景**: 零点击间谍软件通过利用软件、应用或操作系统中隐藏的漏洞来感染设备，目标无需点击链接或打开消息，这与依赖社会工程学的早期攻击方式不同。雇佣式间谍软件（最著名的例子是 NSO Group 的 Pegasus）是卖给政府的商业监控工具，攻击目标通常是记者、活动人士、反对派政治人物和外交官。实时竞价（RTB）是大多数程序化广告背后的拍卖机制，它暴露了大量设备、位置和行为信号，使攻击者能够精确锁定某一台手机下手，MITRE 将这种手法归类为“通过恶意广告获取基础设施”（T1583.008）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://me-en.kaspersky.com/about/press-releases/from-targeted-advertising-to-targeted-attacks-how-advertising-data-is-weaponized-by-cyberthreat-actors">From targeted advertising to targeted attacks: How ...</a></li>
<li><a href="https://attack.mitre.org/techniques/T1583/008/">Acquire Infrastructure: Malvertising, Sub-technique T1583.008 ...</a></li>
<li><a href="https://www.foreignaffairs.com/world/autocrat-in-your-iphone-mercenary-spyware-ronald-deibert">The Autocrat in Your iPhone: How Mercenary Spyware Threatens...</a></li>

</ul>
</details>

**社区讨论**: 讨论意见明显分裂：一位从业 13 年的广告技术工程师认为报告在“零点击”这一点上“极为耸动”，指出它始终没有解释激活机制，并反驳了“广告提供商应被追责”的说法，因为广告技术生态中并不存在这样一个单一主体。其他评论者则争论以色列网络安全公司是否可能被视为独立于国家意志，追问以色列何以成为顶级网络强国，并将该行业的根源追溯到长期被记录的“Download Valley”广告软件产业集群。

**标签**: `#security`, `#spyware`, `#adtech`, `#privacy`, `#cyber-espionage`

---

<a id="item-4"></a>
## [Libreboot 26.10 “Ominous Olive” 发布，新增 UEFI/EDK2 与 Chromebook 支持](https://libreboot.org/news/libreboot2610.html) ⭐️ 8.0/10

代号为 “Ominous Olive” 的 Libreboot 26.10 正式发布，带来两项重大更新：通过 EDK2 框架集成 UEFI 支持，以及从 MrChromebox 的 coreboot 发行版导入全部 233 款当前受支持的 Chromebook。该变更日志是相对于上一个版本 Libreboot 26.01 撰写的，且本次发布的 Chromebook 移植仅提供源码，不附带预编译二进制，用户必须自行从源码构建。 本次发布大幅增加了 Libreboot 可运行的设备数量，并降低了未来移植的门槛，对开源固件这一小众生态而言是重大扩展。同时，UEFI/EDK2 支持与 Chromebook 兼容性远比 Libreboot 过去瞄准的窄众硬件更主流，这使其有望触及更广泛的用户群体。 Chromebook 支持是整批从 MrChromebox 的 coreboot 发行版导入的，其中 Baytrail（Kip）已测试，其他型号仍有待测试；本次不提供二进制，用户需自行编译源码。该版本还因严格的反 AI 贡献政策而受到关注，该政策记录在项目 lbmk 仓库的 AGENTS 文件中，限制由大语言模型协助生成的贡献。

hackernews · iamnothere · 10月15日 12:52 · [社区讨论](https://news.ycombinator.com/item?id=50102923)

**背景**: Libreboot 是 coreboot 的自由开源发行版；coreboot 是一个轻量级固件项目，负责初始化硬件后再加载操作系统，旨在替代专有的 BIOS 与 UEFI 固件。由于 coreboot 需执行底层硬件初始化，必须针对每一款芯片组和主板单独移植，这历史上使 Libreboot 仅支持少量老旧机型。UEFI/EDK2 则是面向 UEFI 与 PI 规范的现代跨平台固件开发环境，将其集成进来，使 Libreboot 能够采用更当代的固件接口与硬件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://libreboot.org/news/libreboot2610.html">Libreboot – Libreboot 26.10 “Ominous Olive” released! With ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Libreboot">Libreboot</a></li>
<li><a href="https://en.wikipedia.org/wiki/Coreboot">Coreboot</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为 AI 政策掩盖了真正的新闻，有人指出 UEFI/EDK2 集成与 Chromebook 支持是“重大进步”，使可用设备数量成倍增加。Heads 项目的一位贡献者分享了相关 ChromeOS 移植工作，将 MrChromebox 的代码作为上游依赖；另一位则赞赏严格的反 LLM 贡献立场，认为对严肃的开源项目而言令人耳目一新。还有人对自己曾刷过 MrChromebox 固件的设备未来或许能跑 Libreboot 表示期待。

**标签**: `#libreboot`, `#coreboot`, `#UEFI`, `#open-source-firmware`, `#chromebook`

---

<a id="item-5"></a>
## [Anthropic 在 IPO 前向投资者披露季度收入增长近 50%，达 168 亿美元](https://simonwillison.net/2026/Oct/15/anthropic-tells-investors/) ⭐️ 8.0/10

据《金融时报》报道，Anthropic 周三向投资者披露其季度收入增长近 50% 至 168 亿美元，其中第一季度约 48 亿美元、第二季度 115 亿美元、第三季度 168 亿美元。公司还透露，竞争对手实验室的模型蒸馏业务占其收入的 5% 至 7%，并已在第三季度“大幅”削减了这部分业务。 这些来自头部 AI 实验室、在其计划 IPO 前公布的硬性数据，为外界了解前沿模型厂商究竟能创造多少收入提供了难得的具象参考；而披露的蒸馏打击行动则表明，实验室愿意牺牲付费 API 客户来保护自身模型权重。此事还值得关注，是因为 Anthropic 显然已不再对投资者使用更“好看”的“年化运行率收入”口径，这推动整个行业转向更清晰的季度财报披露。 第三季度 Anthropic 每在算力上花费 1 美元，就对应 1.70 美元的收入，调整后营业利润率（不含股权激励费用）为 11%。Simon Willison 的粗略推算显示，若蒸馏在削减前占第二季度收入的 5%，那么未具名的竞争对手实验室仅在该季度就为蒸馏 Anthropic 的模型花费了超过 5 亿美元。

rss · Simon Willison · 10月15日 13:04

**背景**: 模型蒸馏（又称知识蒸馏）是一种机器学习技术，即训练一个较小的“学生”模型去模仿更大、更强的“教师”模型的输出，通常是为了让最终模型运行成本更低。在大模型商业化时代，各实验室对竞争对手利用自身 API 输出进行蒸馏颇为不满，因为这实际上让竞争者通过大量付费调用就能获得模型能力，而无需从头训练。Anthropic 是头部 AI 实验室、Claude 系列模型的开发者，上述数据正是在其筹备首次公开募股（IPO）之际传出的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_distillation">Model distillation</a></li>
<li><a href="https://www.flozic.ai/blog/ai-model-distillation">AI Model Distillation : Smarter AI with Less Compute</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#AI industry`, `#IPO`, `#business`, `#revenue`

---

<a id="item-6"></a>
## [MIT 与 PNAS 研究：随机连接的神经元单元可自组装出学习回路](https://www.reddit.com/r/MachineLearning/comments/1x6hmyg/how_artificial_neural_networks_build_their_own/) ⭐️ 8.0/10

被 MIT 报道的一篇 PNAS 论文（2026 年 10 月 9 日发表，题为《生物突触如何自组装出梯度学习》）指出，由共享局部可塑性规则支配的、随机互连的类神经元单元，能够自组织形成具备模式识别与图像分类能力的学习回路。作者报告称，这些网络的表现与作为对照的反向传播训练网络相当。 这一结果重新定义了“学习”的问题框架：与其直接设计学习电路，不如规定局部规则，让学习机制自行组织生成，这对机器学习和神经科学都具有概念上的重要意义。它为不依赖反向传播的学习提供了一条具有生物合理性的思路，可能启发新的网络架构，但作者并未将其视为大规模模型中反向传播的替代方案。 作者明确提醒，自组织现象并不能证明大脑确实采用这一机制，其研究动机是生物合理性，而非追求基准性能上的领先。报道中提及的未解问题包括：所发现的学习回路在不同初始连接下是否保持稳定，以及能否推广到已验证任务之外的更广泛场景。

reddit · r/MachineLearning · /u/Dorian182 · 10月15日 10:01

**背景**: 反向传播是训练人工神经网络的标准算法：它通过把误差信号在整个网络中反向传播来计算梯度，这需要全局协调的非局部信息，而生物突触显然并不具备这样的条件。局部可塑性规则则不同，它仅利用突触自身可获得的信息（例如其所连接神经元的活动）来更新每个突触权重，因此被认为更接近真实大脑的学习方式。这项工作所探讨的问题是：把这类纯局部规则施加于随机连线的网络，能否让具有功能的学习结构自行涌现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.mit.edu/2026/how-artificial-neural-networks-build-their-own-learning-machinery-1013">How artificial neural networks build their own learning machinery</a></li>
<li><a href="https://infoscience.epfl.ch/server/api/core/bitstreams/fccff930-b75c-4944-9ddc-c9f6b24617a2/content">Local plasticity rules can learn deep representations</a></li>
<li><a href="https://www.nature.com/articles/s41467-026-70920-3">Intrinsic stabilization of synaptic plasticity improves ...</a></li>

</ul>
</details>

**社区讨论**: Reddit 讨论帖中的反馈整体积极但篇幅有限，主要围绕该研究的核心问题展开而非质疑结果：评论者指出，自组装学习回路在不同初始连接下的稳定性，以及该方法能否扩展到已验证任务之外，才是判断这一发现价值的关键检验。

**标签**: `#neural-networks`, `#self-organization`, `#synaptic-plasticity`, `#computational-neuroscience`, `#machine-learning`

---