---
layout: default
title: "Horizon Summary: 2026-09-22 (ZH)"
date: 2026-09-22
lang: zh
---

> 从 38 条内容中筛选出 5 条重要资讯。

---

1. [小米开源 MiMo-V2.6 Pro 与 Flash 混合专家模型](#item-1) ⭐️ 8.0/10
2. [NASA 火星采样返回任务被取消](#item-2) ⭐️ 8.0/10
3. [Bryan Cantrill 谈 Sun Microsystems 究竟错在哪里](#item-3) ⭐️ 8.0/10
4. [Cloudflare Python Workers 正式发布，并通过 PEP 783 提供包支持](#item-4) ⭐️ 8.0/10
5. [将混合专家模型映射到推理硬件上的技术解析](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [小米开源 MiMo-V2.6 Pro 与 Flash 混合专家模型](https://mimo.xiaomi.com/mimo-v2-6) ⭐️ 8.0/10

小米 MiMo 团队于 9 月 22 日发布并开源 MiMo-V2.6 系列，包括旗舰版 MiMo-V2.6-Pro（总参数 1.02T / 激活 42B）和主打效率与成本的 MiMo-V2.6-Flash（总参数 309B / 激活 15B），两者均为原生全模态模型，覆盖编程、电脑操作、3D 场景与视听内容创作等智能体任务。面向高吞吐场景的 Pro-UltraSpeed 也在逐步推出，同时团队开放了网页体验、API、Hugging Face 模型权重、7000 个多样化环境以及完整的强化学习框架。 一家以硬件和消费电子为主业的中国公司推出接近前沿水平的开源权重模型，并以罕见的完整度公开训练细节，抬高了“开源发布”的门槛，也让中美实验室在能力与成本两个维度上的竞争更加激烈。如果 MiMo-V2.6-Pro 在智能体基准上真能与 Claude Opus 5、GPT-5.6 Sol 持平，开发者就多了一个可自行部署、成本低得多的智能体方案。 两个版本均采用混合专家（MoE）架构，因此尽管总参数量达到 1.02T 和 309B，每个 token 实际调用的只有 42B 和 15B 激活参数，推理成本远低于同等规模的稠密模型。小米称 Pro-UltraSpeed 在同等质量下输出速度最高可提升约 20 倍，同时这次发布还附带实时训练看板、详尽的技术报告，以及由 MiMo 训练轨迹蒸馏而来的 Qwen 模型。

hackernews · volf\_ · 9月21日 20:12 · [社区讨论](https://news.ycombinator.com/item?id=49792730)

**背景**: 混合专家（MoE）是一种神经网络设计：模型内部包含许多专门的子网络（“专家”），并通过门控机制将每个输入只路由到其中少数几个专家，从而以远低于稠密模型的算力获得极大的总容量。小米的 MiMo 是由罗福莉负责的自研大模型产品线，此次发布强调“公开构建”，通过规模化强化学习并配合实时训练看板展示过程。通常开源权重发布只公开最终模型权重，正因如此，这次额外公开数据、方法论与强化学习环境才显得格外突出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mimo.mi.com/">Xiaomi MiMo-V2.6 Series: 3 New Models Officially Released</a></li>
<li><a href="https://openrouter.ai/xiaomi/mimo-v2.6-pro-ultraspeed">MiMo-V2.6-Pro-UltraSpeed - API Pricing &amp; Providers | OpenRouter</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论区整体态度积极，但在“什么才算真正开源”上存在分歧：有网友盛赞实时训练看板和技术报告是极好的学习与教学工具，同时指出围绕开源定义的争论仍在继续。也有人表示如今对中国模型的期待超过美国模型，主要原因是价格可负担，另一些人则深挖细节，比如给出确切的参数规模并贴出 Hugging Face 上 RL 检查点的链接；还有人打趣说这些模型似乎都偏爱“01 - 全大写文字”的网页设计套路。

**标签**: `#llm`, `#open-source`, `#xiaomi`, `#mixture-of-experts`, `#model-release`

---

<a id="item-2"></a>
## [NASA 火星采样返回任务被取消](https://www.science.org/content/article/nasa-s-mars-sample-return-mission-dead) ⭐️ 8.0/10

据报道，NASA 已放弃其旗舰级的火星采样返回（Mars Sample Return，MSR）任务，也就是 2022 年获批、由 NASA 与 ESA 合作、旨在取回 Perseverance 漫游车在火星上封存的岩石与尘土样本的计划。此次取消至少暂时终结了由 NASA 采样取回着陆器、NASA 建造的火星上升飞行器以及 ESA 地球返回轨道器组成的多任务架构。 这对行星科学是一次重大挫折：继阿波罗时代的月球岩石之后，MSR 本应成为首个把未经污染的火星物质带回地球实验室的任务，用于在火星车无法完成的现场生命探测和同位素年代学分析。留下的空白很可能被中国的 Tianwen-3 填补——该任务计划于 2028 年发射、约在 2030 至 2031 年返回样本，这引发了人们对美国在深空科学领域领导地位的担忧。 该任务的预计成本已膨胀到大约 80 亿至 110 亿美元，且样本要等到 2040 年前后才能返回；批评者指出，其架构是围绕 Ariane 64 等传统运载火箭设计的，而没有采用 Starship 或 New Glenn 等更新、更便宜的重型运载方案。相比之下，阿波罗任务带回了 842 磅（约 382 公斤）月球岩石，而 MSR 原计划只取回约 1.1 磅（约 0.5 公斤）火星物质。

hackernews · Muhammad523 · 9月21日 19:14 · [社区讨论](https://news.ycombinator.com/item?id=49791939)

**背景**: 火星采样返回任务的目标是采集火星岩石和尘土并带回地球，由在地面上远比任何火星车所载仪器更灵敏的设备进行分析，以寻找火星曾经存在生命的迹象。NASA 的 Perseverance 漫游车自 2021 年着陆以来，一直在火星表面钻孔并将样本封存在钛管中，而 NASA 与 ESA 的火星采样返回计划于 2022 年正式获批，负责前往取回这些样本。ESA 负责贡献地球返回轨道器，NASA 则提供着陆器和将样本容器从火星发射升空的上升飞行器。中国的 Tianwen-3 平行任务计划在 2028 年 12 月至 2029 年 1 月的火星发射窗口采用双次发射架构，并沿用 Tianwen-1 的着陆技术以及嫦娥五号、嫦娥六号月球采样返回的经验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mars_sample-return_mission">Mars sample-return mission</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tianwen-3">Tianwen-3 - Wikipedia</a></li>
<li><a href="https://www.space.com/astronomy/mars/china-on-track-to-launch-mars-sample-return-mission-in-2028-if-accurate-this-represents-a-sputnik-moment">China on track to launch Mars sample-return mission in 2028: &#x27;If accurate, this represents a Sputnik moment&#x27; | Space</a></li>

</ul>
</details>

**社区讨论**: 评论者大多认同这个耗资 80 亿至 110 亿美元、要到 2040 年前后的臃肿架构必须终止，其中数人指责 JPL 领导层围绕传统火箭而非 Starship 或 New Glenn 进行设计，还有人认为这篇文章读起来像是依附旧资助模式的机构所写的&quot;自怜式宣传&quot;。另一些人则指出中国的 Tianwen-3 才是真正的竞争背景，一位曾参与 ExoMars 的人士提到，像 Rosalind Franklin 漫游车（现计划 2028 年发射）这样一再推迟的欧洲任务，说明行星探测的时间表已变得多么脆弱。

**标签**: `#space exploration`, `#NASA`, `#science-policy`, `#aerospace-engineering`, `#research-funding`

---

<a id="item-3"></a>
## [Bryan Cantrill 谈 Sun Microsystems 究竟错在哪里](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) ⭐️ 8.0/10

Bryan Cantrill 发表了题为《What Sun got wrong》的回顾性文章，剖析了导致 Sun Microsystems 衰落的一系列战略与技术失误。文章发布后迅速在 Hacker News 上引发热烈讨论，前客户和工程师们围绕 Solaris、SPARC 以及 Sun 的销售文化分享了大量亲历故事。 Sun 的衰落以及 2010 年被 Oracle 收购，至今仍是垂直整合型系统厂商如何失去主导市场的经典案例，而 Cantrill 是以亲历者而非旁观历史学家的身份来复盘这段经历。这场讨论在当下依然有意义，因为专有硬件与通用商品硬件的取舍、开源策略以及云计算时代的经济学，仍在深刻影响 Oracle 等厂商乃至整个服务器行业。 Cantrill 是 Sun 前工程师，与该公司的多项系统级创新密切相关，因此他的分析带有内部视角，而非外人只能看到的事后结果。由于目前只提供了标题与社区反应，文章中的具体论断无法依据现有材料进一步核实。

hackernews · chmaynard · 9月21日 14:03 · [社区讨论](https://news.ycombinator.com/item?id=49787436)

**背景**: Sun Microsystems 是 Solaris 与 SPARC 的缔造者。Solaris 是一款专有 Unix 操作系统，以可扩展性著称，并孕育了 DTrace、ZFS 等创新；SPARC 则是 Sun 自 1980 年代中期起开发的 RISC 指令集架构。Solaris 的大部分代码在 2005 年以 OpenSolaris 之名开源，但 2010 年 Oracle 收购 Sun 后该项目被终止，内核源码重新闭源，代码随后被分叉为 Illumos；Oracle 也在 2017 年停止了 SPARC 的开发。Cantrill 本人的职业生涯与声誉正是在这一生态中建立起来的，这也是他的复盘在系统圈内颇具分量的原因之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Solaris_operating_system">Solaris operating system</a></li>
<li><a href="https://en.wikipedia.org/wiki/SPARC_processor_architecture">SPARC processor architecture</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同 Sun 的工程技术一流，但商业执行很差：有人回忆当年从 Sun 或 DEC 采购硬件要经历冗长的销售会议和反复改报价，而一台戴尔服务器第二天就能送到；也有人列举了 2000 年代的具体失误，比如 2002 年短暂取消 x86 版 Solaris、以及未能与 Google 达成交易。还有人怀念 Sun 瘦客户机和 Pine、vi 的工作流，并调侃说 Sun「从来就没兴趣经营一家企业」，它在乎的是做出惊艳的技术，而不是把它卖出去。

**标签**: `#Sun Microsystems`, `#systems`, `#Solaris`, `#SPARC`, `#tech history`

---

<a id="item-4"></a>
## [Cloudflare Python Workers 正式发布，并通过 PEP 783 提供包支持](https://blog.cloudflare.com/python-workers-ga/) ⭐️ 8.0/10

Cloudflare 宣布 Python Workers 正式可用（GA），它在 Workers 边缘运行时上直接运行编译为 WebAssembly 的 CPython（基于 Pyodide），而不是跑在容器里。此次发布还带来了通过 PEP 783 标准化的“一等公民”包支持——该 PEP 为面向 Pyodide 构建的 wheel 引入了“pyemscripten”平台标签——并向社区上游贡献代码，使 Requests 等 HTTP 客户端能够通过 JavaScript 的 fetch API 发起请求。 Python 是世界上最广泛使用的语言之一，在无服务器边缘平台上原生支持它，为原本必须依赖容器或改用其他语言的开发者扫除了一个重要障碍。而通过 PEP 783 标准化 WASM 包的发布方式，也可能惠及 Cloudflare 之外的整个 Pyodide/Emscripten 生态，因为它为包维护者提供了一个统一的预编译 wheel 目标格式。 一个关键推动因素是上游合并进 urllib3 的 JSPI（JavaScript Promise Integration）支持，它让 Requests 这类同步 Python HTTP 客户端可以在 WebAssembly 环境下工作。PEP 783 定义了用于在 Pyodide 下运行的 wheel 的“pyemscripten”平台标签，且相关 CPython 版本是编译成 WebAssembly 而非原生运行时；据反映，Workers 模型仍存在一些架构上的限制。

hackernews · torutofu · 9月21日 13:38 · [社区讨论](https://news.ycombinator.com/item?id=49787142)

**背景**: Cloudflare Workers 是一个无服务器平台，基于 V8 引擎和隔离（isolate）机制在网络边缘运行代码，而非使用容器化的语言运行时，这使它启动很快，但长期以来以 JavaScript/WASM 为主。Pyodide 是编译为 WebAssembly 的 CPython 发行版，可让 Python 在浏览器和 Node.js 中运行。PEP 是 Python Enhancement Proposal（Python 增强提案）的缩写，是 Python 社区用来标准化各种改动的编号设计文档，PEP 783 中描述的 pyemscripten wheel 标签正是通过这一机制确立的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://peps.python.org/pep-0783/">PEP 783 – Emscripten Packaging - Python Enhancement Proposals</a></li>
<li><a href="https://github.com/pyodide/pyodide">GitHub - pyodide/pyodide: Pyodide is a Python distribution for the browser and Node.js based on WebAssembly · GitHub</a></li>
<li><a href="https://developers.cloudflare.com/workers/reference/how-workers-works/">How Workers works · Cloudflare Workers docs</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论总体积极但相当细致：一位 urllib3 维护者澄清，上游 Pyodide/JSPI 相关工作的资金给到了实际实现该功能的外部贡献者，而不是维护者本人，点出了常被忽视的维护生态问题。Wasmer 创始人赞赏 Cloudflare 在包支持上的进展，同时指出自首次发布以来仍存在的架构约束；其他评论者则将其与 2008 年 Google App Engine 的 Python 支持做尖锐的历史类比，也有人打趣说“Python Workers”这个说法听起来像是 Python 程序员被替换掉了。

**标签**: `#cloudflare-workers`, `#python`, `#webassembly`, `#serverless`, `#pyodide`

---

<a id="item-5"></a>
## [将混合专家模型映射到推理硬件上的技术解析](https://newsletter.semianalysis.com/p/computation-and-data-movement-for) ⭐️ 8.0/10

SemiAnalysis 发布了一篇技术深度分析，探讨混合专家（MoE）模型如何被映射到推理硬件上，涵盖模型结构、数据流动与高效服务三个方面。该文并非发布新模型或新产品，而是解释在生产环境中运行 MoE 推理的系统层面机制。 MoE 架构是当今许多最强大型模型（包括 GPT-4、Gemini 和 Mixtral）的基础，因此理解它们如何映射到硬件上直接影响推理延迟、吞吐量和成本。随着推理成为实时且能创造收入的工作负载，数据搬运而非单纯算力正逐渐成为主要系统瓶颈，这使得该分析对机器学习系统与基础设施工程师颇具价值。 MoE 的核心权衡在于它把权重拆分成众多专家，每个 token 只激活其中少数几个，从而获得小模型的速度与大模型的知识——代价则是显著更高的显存需求。这意味着服务效率在很大程度上取决于专家如何放置并在内存与计算单元之间搬运，而许多容量计算工具往往会把显存估算算错。

rss · Semianalysis · 9月21日 18:14

**背景**: 混合专家（MoE）是一种神经网络设计，它用许多并行的“专家”子网络替代单一稠密前馈层，并配合一个路由机制，为每个输入 token 只挑选少数几个专家。LLM 服务指的是把训练好的模型部署到生产环境中处理用户提示并生成回复，其中延迟、吞吐量和成本是关键运营指标。由于 MoE 模型需要把所有专家都保留在内存中，但每个 token 只用到其中一小部分，推理因此不仅是算力问题，同样是内存与互连问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://localmodel.run/guides/mixture-of-experts">Mixture of experts (MoE) explained for local LLMs · localmodel.run</a></li>
<li><a href="https://davision.ca/memory-bottleneck-ai-inference/">Why AI inference is turning memory into the bottleneck</a></li>
<li><a href="https://docs.anyscale.com/llm/serving/intro">What is LLM serving? | Anyscale Docs</a></li>

</ul>
</details>

**标签**: `#MoE`, `#Inference`, `#AI Hardware`, `#Systems`, `#LLM Serving`

---