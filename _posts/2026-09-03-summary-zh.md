---
layout: default
title: "Horizon Summary: 2026-09-03 (ZH)"
date: 2026-09-03
lang: zh
---

> 从 39 条内容中筛选出 8 条重要资讯。

---

1. [谷歌推出 Gemini 3.8 Flash 与 3.8 Flash Cyber 模型](#item-1) ⭐️ 9.0/10
2. [Meta 发布 Muse Spark 1.3：低成本、接近顶级基准](#item-2) ⭐️ 8.0/10
3. [三个网站生成 21.5 万个“最佳软件”页面，Perplexity 等 AI 频繁引用](#item-3) ⭐️ 8.0/10
4. [Paint.NET 开发者披露为 WINE 用 AI 重写 18 万行 Direct2D](#item-4) ⭐️ 8.0/10
5. [Jasper Research 发布技术指南，展示如何从零构建文生图模型](#item-5) ⭐️ 8.0/10
6. [评测显示：多数开源 AI 检测器无法保持 0.5%的误报率](#item-6) ⭐️ 8.0/10
7. [月之暗面与微软、亚马逊、谷歌谈判 Kimi K3 收入分成](#item-7) ⭐️ 8.0/10
8. [FBI 调查 Nexus 暗网售卖 1.53 亿张驾照扫描件](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [谷歌推出 Gemini 3.8 Flash 与 3.8 Flash Cyber 模型](https://blog.google/innovation-and-ai/models-and-research/gemini-models/3-8-flash-and-3-8-flash-cyber/) ⭐️ 9.0/10

谷歌发布了 Gemini 3.8 Flash 与 3.8 Flash Cyber，为 Gemini 系列新增了一个快速、高性能的通用模型和一个面向网络安全的调优变体。Flash Cyber 通过新的 Fairwind 计划提供给受信任的防御者，具备漏洞检测与自动修补方面的高水平能力。 此次发布进一步加快了谷歌 Flash 系列更新频率——六周内的第三款 Flash 模型——并以较低价格提供接近前沿水平的智能。这对正在构建智能体、编程和多模态媒体分析应用的开发者，以及需要自动化漏洞修补的安全团队具有重要意义。 讨论中引用的社区基准显示，Gemini 3.8 Flash 在 Artificial Analysis 上的智能得分为 59，与 Opus 5 medium 持平，并在 DeepSwe 排行榜上名列第一。Cyber 模型使用相同的基础架构，但专门针对漏洞检测与缓解进行调优，并非广泛开放使用。

hackernews · bratao · 9月2日 15:12 · [社区讨论](https://news.ycombinator.com/item?id=49537553)

**背景**: 在谷歌 Gemini 系列中，&\#x27;Flash&\#x27;代表高吞吐量、低成本的模型层级，旨在充当日常‘主力’模型，与擅长深度推理的 Pro 模型和更轻量的 Flash-Lite 变体形成互补。这类模型针对令牌效率、多模态输入和智能体工作流进行了优化。Gemini 3.8 Flash 延续了这一系列，其模型卡已发布在 Google DeepMind 网站上；谷歌表示 Cyber 版本专门为一线安全工作进行了调优。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/3-8-flash-and-3-8-flash-cyber/">Introducing Gemini 3.8 Flash and 3.8 Flash Cyber</a></li>
<li><a href="https://arstechnica.com/ai/2026/09/google-releases-gemini-3-8-flash-its-third-flash-model-in-six-weeks/">Google releases Gemini 3.8 Flash, its third Flash model in six weeks - Ars Technica</a></li>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3.8 Flash — Google DeepMind</a></li>

</ul>
</details>

**社区讨论**: 开发者评论整体非常积极。Simon Willison 展示了一个仅需 1.8 美分、13 秒即可完成的 HTML 生成演示，并肯定其多模态输入支持，指出 OpenAI 和 Anthropic 的旗舰模型仍然仅支持图像输入。还有用户报告该模型在 DeepSwe 排行榜上超过 Opus 5，在 Artificial Analysis 上与 Opus 5 medium 持平，并认为对&\#x27;Flash&\#x27;模型来说这些基准表现令人印象深刻。也有声音提醒，低&\#x27;思考强度&\#x27;模式可能相比 3.7 有所回退，因此仍需实际测试。

**标签**: `#Gemini`, `#Google`, `#AI models`, `#LLM`, `#Machine Learning`

---

<a id="item-2"></a>
## [Meta 发布 Muse Spark 1.3：低成本、接近顶级基准](https://developer.meta.com/ai/models/muse-spark/) ⭐️ 8.0/10

Meta 发布了 Muse Spark 1.3，这是其面向编码和智能体任务模型的更新版本，新增了 max reasoning 模式并提升实际可用性。基准测试中它取得 DeepSWE 75.4 分，社区认为这是迄今最佳成绩。 Muse Spark 1.3 以明显更低的价格提供接近最先进水平的基准表现，让更多开发者能够用上强大的 AI 编程能力。它还加剧了模型厂商之间的价格竞争，有望推动整个行业的成本下降。 社区测试显示，单次生成成本约为 4.2266 美分、耗时 38 秒，说明单次查询价格非常低。Meta 还提供“贡献者”（contributor）版本，用户允许 Meta 使用数据进行训练，以换取更低或定价策略不同的服务。

hackernews · bvaldivielso · 9月2日 19:35 · [社区讨论](https://news.ycombinator.com/item?id=49541256)

**背景**: Muse Spark 是 Meta 面向代码生成和自主智能体任务优化的模型系列。DeepSWE 是一个用于评估模型解决真实软件工程问题能力的基准。Meta 表示，Muse Spark 1.3 汲取了 Muse Code 和 Meta Model API 被广泛采用后学到的经验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.meta.com/ai/models/muse-spark/">Muse Spark 1.3 | Meta</a></li>
<li><a href="https://research.meta.ai/blog/introducing-muse-spark-1-3">Introducing Muse Spark 1.3 | Meta AI Research</a></li>
<li><a href="https://artificialanalysis.ai/models/muse-spark-1-3">Muse Spark 1.3 (max) - Intelligence, Performance &amp; Price Analysis | Artificial Analysis</a></li>

</ul>
</details>

**社区讨论**: 整体反馈积极：Simon Willison 的对比测试发现，1.3 生成 SVG 的质量优于 1.2，成本仅约 4 美分；superfrank 也赞赏此前的 Spark 版本在低成本开发中可靠好用。多位评论者强调定价竞争和“贡献者”选项的透明性，但也有人担心让 Meta 用自己数据训练带来的隐私影响。

**标签**: `#AI`, `#LLM`, `#Meta`, `#Model Release`, `#Benchmarks`

---

<a id="item-3"></a>
## [三个网站生成 21.5 万个“最佳软件”页面，Perplexity 等 AI 频繁引用](https://trellner.com/reports/manufactured-sources-behind-ai-recommendations/) ⭐️ 8.0/10

Trellner 的一份新报告发现，三个网站合计发布了 215,128 个“最佳软件”页面，而 Perplexity 等 AI 助手在回答中频繁引用这些页面。这表明批量生产的 SEO 内容正在影响 AI 生成的推荐结果。 这一发现暴露了 AI 搜索的机制性弱点：以引用为驱动的系统可能大规模放大低价值、程序化生成的内容。依赖 AI 推荐做决策的用户，可能在不自知的情况下得到由 SEO 垃圾信息而非真正专业知识驱动的内容。 这些页面是程序化 SEO（programmatic SEO）的典型产物，即用自动化方式批量生成页面以获取搜索流量。报告指出，Perplexity 这类 AI 引用系统缺乏足够的信息来源辨别力，因而容易被这种大批量生产的对比页面所利用。

hackernews · jakobgreenfeld · 9月2日 13:59 · [社区讨论](https://news.ycombinator.com/item?id=49536375)

**背景**: 程序化 SEO（programmatic SEO）利用脚本和数据模板批量生成成百上千个针对特定搜索查询的落地页。Perplexity 等 AI 搜索引擎在生成回答时会检索并引用网页，而其来源选择可能被针对 AI 优化的内容干扰。因此，如果低质量的机器生成页面在检索结果中排名靠前，它们就可能成为 AI 回答的“依据”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://otterly.ai/blog/perplexity-seo/">Perplexity SEO (2026): How to Rank by Getting Cited as a Source ...</a></li>
<li><a href="https://unosearch.io/blogs/how-does-perplexity-ai-choose-citations-2/">How Does Perplexity AI Choose Citations in 2026? | UnoSearch</a></li>
<li><a href="https://leadorigin.com/programmatic-seo/">Programmatic SEO And How It Help Boost Digital Presence | TX</a></li>

</ul>
</details>

**社区讨论**: 评论者大多认同报告的担忧，并分享了亲身经历：AI 工具会引用不可靠甚至根本不存在的来源。一位用户提到，Claude 和 Codex 在搜索时常会选择机器生成的网站；另一位用户则描述 AI 自信地推荐了一个完全虚构的“Foobar 广场”。多名评论者认为模型需要更强的来源辨别能力，而利用这一弱点的窗口终将收窄。

**标签**: `#AI`, `#SEO spam`, `#search quality`, `#Perplexity`, `#content authenticity`

---

<a id="item-4"></a>
## [Paint.NET 开发者披露为 WINE 用 AI 重写 18 万行 Direct2D](https://simonwillison.net/2026/Sep/2/rick-brewster/) ⭐️ 8.0/10

Paint.NET 开发者 Rick Brewster 透露，该应用现在内置了一个从头开始、净室逆向工程的 Direct2D API 重写版，以在 WINE 上运行，通过 /wine 命令行参数触发。约 18 万行代码主要由 Anthropic 的 Claude AI 模型生成，且未经过全面审查。 这是一个标志性案例：AI 智能体大规模地重新实现了一个复杂的专有 API，既展示了“vibe coding（氛围编程）”在大规模项目中的潜力，也暴露了其风险。这对 WINE 社区、AI 辅助软件开发，以及所有关心代码质量、可维护性和生成代码可信度的人都很重要。 该重写代码位于 PaintDotNet.Windows.Direct2D1.Managed.dll 中，并包含针对 Direct2D 内置效果库的逆向工程公式。Brewster 表示他不得不“盯紧”Claude，确保 COM 引用计数（AddRef）正确，并在开发过程中否决了若干糟糕的设计或架构决策。

rss · Simon Willison · 9月2日 05:50

**背景**: Direct2D 是微软的硬件加速、即时模式的 2D 图形 API，被许多 Windows 应用程序使用，它一直是 Paint.NET 在 WINE 下运行的主要障碍；WINE 是一个兼容层，能让 Windows 软件在 Linux 及其他类 Unix 系统上运行。Vibe coding（氛围编程）指的是不进行严格审查就接受 AI 生成的代码，而依赖测试和迭代提示来修正。Brewster 的描述表明，即使是庞大而复杂的代码库也能以这种方式生成，但同时也强调了仔细监督的必要性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Direct2D">Direct2D - Wikipedia</a></li>
<li><a href="https://www.winehq.org/">WineHQ - Run Windows applications on Linux, BSD, Solaris and macOS</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vibe_coding">Vibe coding - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI-assisted development`, `#reverse engineering`, `#Direct2D`, `#WINE`, `#software reliability`

---

<a id="item-5"></a>
## [Jasper Research 发布技术指南，展示如何从零构建文生图模型](https://www.reddit.com/r/MachineLearning/comments/1w5c9rd/detailed_explanation_of_how_to_create_a/) ⭐️ 8.0/10

Jasper Research 发布了一本交互式技术手册、nano-t2i 代码库，以及一个包含约 1 亿张图像的 MONET 数据集，用于从零训练文生图模型。这些材料记录了完整的推理过程、设计取舍和中间结果，而不仅仅是最终代码。 对机器学习从业者而言，这是一份价值很高的开放教育资源，揭示了前沿实验室如何构建文生图系统，并降低了动手实验的门槛。它提供了可复现的代码和数据，让通常需要大量算力的研究课题也能被个人和小型团队接触。 该手册托管在 Hugging Face Spaces 上，名称为 t2i-technical-interactive-report；配套的 MONET 数据集包含约 1.049 亿个图文对。GitHub 仓库 nano-t2i 提供了一个小规模模型，专门为了让使用者能够真正从零开始跑通文生图模型的训练流程。

reddit · r/MachineLearning · /u/dh7net · 9月2日 14:40

**背景**: 文生图模型是指用深度学习技术，根据自然语言描述生成图像的模型。通常，从零训练这样的模型需要收集并清洗海量图文数据，再长时间训练大型神经网络。Jasper 这套开放资源的特点是用一个可运行的最小示例把这些环节串联起来，让入门者能够看到每一步的具体做法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/datasets/jasperai/monet">jasperai/monet · Datasets at Hugging Face</a></li>
<li><a href="https://arxiv.org/html/2605.21272v1">MONET: A Massive, Open, Non-redundant and Enriched Text-to-image dataset</a></li>
<li><a href="https://stable-diffusion-web.com/">Stable Diffusion Online - Free Browser AI Image Generator</a></li>

</ul>
</details>

**标签**: `#text-to-image`, `#machine learning`, `#tutorial`, `#dataset`, `#generative models`

---

<a id="item-6"></a>
## [评测显示：多数开源 AI 检测器无法保持 0.5%的误报率](https://www.reddit.com/r/MachineLearning/comments/1w58erw/most_opensource_ai_detectors_cant_hold_a_05/) ⭐️ 8.0/10

一项对六个开源 AI 文本检测器的系统基准评测发现，其中四个在对齐到 0.5%误报率后实际无法达标，而且所有模型在改写\(paraphrase\)文本面前性能严重下降。表现最好的 tropa-mini 能识别 93.2%的原始 AI 文本，但对改写文本仅捕获 41.6%；旧版 OpenAI RoBERTa 检测器在现代生成器上的 AUC 仅为 0.31，比随机猜测更差。 这项证据很重要，因为可靠检测模型生成内容的需求日益增加，但结果表明，当前开源检测器无法满足现实应用（如学术诚信、招聘或内容审核）所需的低误报率。所有模型一致地对非英语母语写作者表现出歧视，也使整类工具面临公平性方面的严重担忧。 该基准测试将所有检测器的阈值在 6,930 篇人类写作文本上对齐到 0.5%误报率，然后分别测量其对原始 AI 文本、改写文本以及 1,060 篇前沿模型文本的召回率。值得注意的是，yaful/MAGE 在 26%的普通人类网页文本上给出超过 0.9999 的分数，且在任何阈值下都无法达到 0.5%误报率目标；作者也披露六款检测器中有一款是他们自己发布的开源模型。

reddit · r/MachineLearning · /u/grumpyp2 · 9月2日 12:04

**背景**: AI 文本检测器是试图区分大型语言模型生成的文本与人类撰写文本的分类器，误报（false positive）指的是把人类创作的内容错误地标记为 AI 生成。0.5%这样低的误报率是实际部署中常见的指标要求，因为错误的指控可能带来严重后果，尤其是对学生、求职者和非母语作者而言。该评测使用公开数据，包括 5,000 篇由人类写于 LLM 普及之前的 FineWeb 网页；FineWeb 是一个从 96 个 Common Crawl 快照构建的 15 万亿 token 数据集。旧版 OpenAI RoBERTa 检测器是针对 GPT-2 输出专门训练的，这也解释了它为何在现代大模型面前表现不佳。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/datasets/HuggingFaceFW/fineweb">HuggingFaceFW/fineweb · Datasets at Hugging Face</a></li>
<li><a href="https://huggingface.co/openai-community/roberta-base-openai-detector">openai-community/roberta-base-openai-detector · Hugging Face</a></li>
<li><a href="https://arxiv.org/abs/2406.17557">[2406.17557] The FineWeb Datasets: Decanting the Web for the Finest Text Data at Scale</a></li>

</ul>
</details>

**标签**: `#AI detection`, `#benchmarking`, `#LLM`, `#false positives`, `#open-source`

---

<a id="item-7"></a>
## [月之暗面与微软、亚马逊、谷歌谈判 Kimi K3 收入分成](https://www.jiemian.com/article/15040119.html) ⭐️ 8.0/10

据路透社报道，月之暗面正与微软、亚马逊和谷歌就收入分成协议进行早期谈判，计划让这些美国云巨头托管其 Kimi K3 模型。这家中国初创公司最初寻求最高 30% 的分成比例；若达成，将成为中国 AI 公司与美国云服务商之间的首例重大此类协议。 如果达成协议，将改变中国大模型触达全球用户的方式，使月之暗面在美国主流云平台中获得罕见的发行渠道。这也可能预示着 AI 模型托管整体向按使用量分成模式转变，对云厂商、模型开发者和企业用户都将产生深远影响。 谈判仍处于早期阶段，核心条款未定，微软、亚马逊、谷歌和月之暗面均拒绝置评。Kimi K3 于 2026 年 7 月发布，总参数达 2.8 万亿，是全球首个开源 3T 级模型；据报道，月之暗面截至 6 月中旬的年度经常性收入已突破 3 亿美元。

telegram · zaihuapd · 9月2日 07:36

**背景**: 月之暗面是一家总部位于北京的 AI 初创公司，以 Kimi 系列模型著称。Kimi K3 于 2026 年 7 月发布，是一个总参数达 2.8 万亿的开源旗舰模型，公司称过去一年中大多时候都由其模型确立开源模型的规模上限。在收入分成安排下，云厂商将在自家平台托管该模型，并将模型使用或 API 产生的收入按比例分给月之暗面，而非由月之暗面支付固定的托管费。这种模式在应用商店中很常见，但在前沿模型领域、尤其是涉及中国开发者与美国云巨头的交易中极为罕见。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://money.usnews.com/investing/news/articles/2026-08-26/exclusive-chinas-moonshot-in-talks-with-microsoft-amazon-google-over-k3-revenue-sharing-sources-say">Exclusive-China&#x27;s Moonshot in Talks With Microsoft, Amazon, Google...</a></li>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://huggingface.co/moonshotai/Kimi-K3">moonshotai/ Kimi - K 3 · Hugging Face</a></li>

</ul>
</details>

**标签**: `#AI`, `#Moonshot AI`, `#Cloud Computing`, `#Revenue Sharing`, `#Kimi K3`

---

<a id="item-8"></a>
## [FBI 调查 Nexus 暗网售卖 1.53 亿张驾照扫描件](https://krebsonsecurity.com/2026/09/fbi-probes-service-selling-153m-drivers-licenses/) ⭐️ 8.0/10

FBI 正在调查名为 Nexus 的暗网服务，该服务宣称持有超过 1.53 亿张美国和加拿大民众的驾照数字扫描件，并已开始对外售卖。 由于驾照包含姓名、住址、出生日期等敏感个人信息，这批数据可能被用于大规模身份冒用与欺诈。1.53 亿条记录的规模凸显了聚合数据泄露带来的持续威胁。 Krebs 报道称，这些扫描件可能来自此前汽车经销商、保险公司等机构泄露的旧扫描文件。官方尚未公布数据的具体来源和受影响人数。

telegram · zaihuapd · 9月2日 09:31

**背景**: Nexus 被描述为一个需要借助 Tor 浏览器访问的暗网交易平台，常见交易内容包括被盗数据和非法商品。驾照扫描件对犯罪分子尤其有价值，因为它在包含身份信息的同时还有照片，可用于绕过验证或开设欺诈账户。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/vp4m455xi/nexus-web-dark/blob/main/README.md">nexus - web - dark /README.md at main · vp4m455xi/ nexus - web - dark</a></li>
<li><a href="https://cyble.com/knowledge-hub/top-dark-web-marketplaces-of-2024/">Top Dark Web Marketplaces In 2026: Market Analysis</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#data breach`, `#dark web`, `#privacy`, `#identity theft`

---