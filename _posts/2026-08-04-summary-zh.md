---
layout: default
title: "Horizon Summary: 2026-08-04 (ZH)"
date: 2026-08-04
lang: zh
---

> 从 33 条内容中筛选出 12 条重要资讯。

---

1. [Qwen 发布 3.8-Max：2.4 万亿参数，首次开源 Max 级模型](#item-1) ⭐️ 9.0/10
2. [文章：大语言模型奖励专业能力，而非取代专家](#item-2) ⭐️ 8.0/10
3. [OpenAI 发文盘点数学与理论计算机科学十项进展](#item-3) ⭐️ 8.0/10
4. [开发者工具必须开源以支持 AI 驱动定制](#item-4) ⭐️ 8.0/10
5. [MiniMax H3 获 ComfyUI 首发支持：开放权重、原生音频与 2K 视频](#item-5) ⭐️ 8.0/10
6. [安迪·帕夫洛加入 ClickHouse，领导新成立的 ClickHouse Labs](#item-6) ⭐️ 8.0/10
7. [SemiAnalysis 深度解析 Kimi K3：压缩内存、跨层注意力与潜在专家路由](#item-7) ⭐️ 8.0/10
8. [审稿人呼吁：无复现代码的论文应被直接拒稿](#item-8) ⭐️ 8.0/10
9. [美犯罪实验室 DNA 设备曝安全漏洞，30 年证据面临篡改风险](#item-9) ⭐️ 8.0/10
10. [美至少 50 名警员被控以摄像头窥探前任](#item-10) ⭐️ 8.0/10
11. [苹果遭 325 亿美元集体诉讼：相册人脸识别被指违规](#item-11) ⭐️ 8.0/10
12. [苹果就英国政府 iCloud 后门要求提起诉讼](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Qwen 发布 3.8-Max：2.4 万亿参数，首次开源 Max 级模型](https://qwen.ai/blog?id=qwen3.8) ⭐️ 9.0/10

阿里巴巴通义千问团队发布了 Qwen 3.8-Max，这是一个总参数达 2.4 万亿、活跃参数为 95B 的混合专家（MoE）模型，并宣布将于下周开源模型权重。这是 Qwen 首次开放 Max 级别模型的权重。 开源 Max 级模型是开放权重大模型领域的重要里程碑，让开发者首次获得以往仅通过封闭 API 才能使用的前沿规模能力。这可能加速编码、智能体工作流和长周期任务相关的研究与应用开发。 Qwen 3.8-Max 基于 Qwen 3.5 架构，采用混合专家（MoE）设计，每个 token 仅激活 2.4 万亿总参数中的 95B。团队表示，该模型可自主运行超 10 天完成自我进化的编码项目，并在 24 小时内于 WWW2025 多模态对话意图识别竞赛中击败了 526 支队伍中的 458 支。

telegram · zaihuapd · 8月3日 02:31

**背景**: 混合专家（MoE）是一种神经网络设计，将模型划分为多个专门的“专家”子网络，并通过路由器为每个输入 token 仅选择少数专家。这种方式让模型可以拥有庞大的总参数量，同时保持可控的计算成本，因为实际计算每个 token 时只用到活跃参数。Qwen 是阿里巴巴开发的大语言模型系列，Max 是其中最高规格的序列，通常仅通过 API 提供。在 MoE 模型中，活跃参数是指处理每个 token 时实际参与计算的那部分参数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/mixture-of-experts">What is mixture of experts? | IBM</a></li>
<li><a href="https://llmcheck.net/blog/moe-vs-dense-llm-explained/">MoE vs Dense LLMs Explained: Why It Matters for Your... — LLM Check</a></li>

</ul>
</details>

**标签**: `#Qwen`, `#LLM`, `#open-source`, `#AI release`, `#model weights`

---

<a id="item-2"></a>
## [文章：大语言模型奖励专业能力，而非取代专家](https://www.seangoedecke.com/llms-reward-expertise/) ⭐️ 8.0/10

Sean Goedecke 的一篇新文章认为，LLM 能放大具有深厚领域知识的人的生产力，而不是拉平专家与新手之间的差距。这篇文章在 Hacker News 上获得了大量关注，得到了 322 分和 141 条评论。 这一观点挑战了常见的叙事，即 AI 将贬低或取代人类专业知识，反而表明深厚领域知识正变得更有价值。这对正在决定如何将 LLM 融入工作流程的软件工程师和其他知识工作者而言意义重大。 这篇文章借鉴了作者在软件工程方面的经验，强调虽然通用的软件知识很有用，但对特定代码库的熟悉程度至关重要，并且通常需要动手实践来获得。评论讨论了“放大镜”类比，即 LLM 反映用户自身的专业能力，并警告如果过度看重提示工程，可能会失去领域专家。

hackernews · MaxMussio · 8月3日 21:13 · [社区讨论](https://news.ycombinator.com/item?id=49161518)

**背景**: 大型语言模型（LLM）是在海量文本数据上训练、能够生成类似人类回复的 AI 系统。关于这些工具是否会取代工作者或让技能变得不那么重要，存在着广泛的争论。这篇文章的立场是，LLM 扮演着放大器的角色：专家能够有效地引导它们，因为他们知道什么才是真正重要的，而新手可能难以评估或引导输出。

**社区讨论**: 评论者大体上赞同文章的观点。一位用户指出，对代码库的熟悉是一种需要动手实践、类似“先有鸡还是先有蛋”的挑战；另一位则把 LLM 描述为用户自身思维的放大镜。还有少数人担心，过度依赖提示工程可能会意外贬低或削弱真正的领域专业知识；还有一位评论者呼吁进行正式研究，以排除确认偏差。

**标签**: `#LLMs`, `#AI`, `#Expertise`, `#Productivity`, `#Software Engineering`

---

<a id="item-3"></a>
## [OpenAI 发文盘点数学与理论计算机科学十项进展](https://openai.com/index/ten-advances-in-mathematics/) ⭐️ 8.0/10

OpenAI 发布了一篇文章，重点介绍数学与理论计算机科学领域的十项近期进展，并称这些进展表明 AI 驱动的研究发现正在加速。该消息在 Hacker News 上引发了广泛讨论。 这篇文章之所以重要，是因为它表明 AI 越来越能够生成、验证甚至推翻数学证明，而这些工作传统上由人类数学家完成。如果这一趋势持续下去，可能会改变数学研究和证明验证的方式。 据社区评论者提及的具体条目，这十项进展涉及高维球堆积和多色拉姆齐数等主题。该文章本身似乎没有给出详细证明，而是将这些成果定位为 AI 辅助数学研究的里程碑。

hackernews · milkshakes · 8月3日 16:27 · [社区讨论](https://news.ycombinator.com/item?id=49157930)

**背景**: 数学和理论计算机科学长期以来被认为是 AI 难以攻克的领域，因为它们需要严谨的推理和创造力。近期的 LLM 在生成证明草图、搜索反例和验证形式化论证方面展现出潜力，使一些原本繁琐的证明工作变得更易于计算。OpenAI 是积极探索这一方向的研究机构之一。

**社区讨论**: 评论者的情绪既有兴奋也有谨慎：有人预测任何可计算的问题最终都会被计算机解决，也有人指出 AI 目前擅长通过大量演算来证伪猜想，而非提出直觉性猜想。有评论者担心，那些近年依靠人工搜索证明的数学家可能被颠覆；另一些人则把指数级的进步速度视为关键问题。

**标签**: `#AI`, `#mathematics`, `#theoretical computer science`, `#research`, `#OpenAI`

---

<a id="item-4"></a>
## [开发者工具必须开源以支持 AI 驱动定制](https://blog.exe.dev/devtools-must-be-open-source) ⭐️ 8.0/10

一篇题为《Devtools must be open source》的博客文章认为，开发者工具必须开源，以便基于 LLM（大语言模型）进行定制和维护。该文在 Hacker News 等平台引发了激烈讨论，获得 479 分和 173 条评论。 这场讨论在当代 LLM 的背景下重新审视了经典的开源论点，认为 AI 编程助手可能让“自由修改”的承诺对普通用户变得实际可行。它促使工具厂商和维护者重新思考授权方式、可配置性以及 AI 在软件维护中的未来角色。 该文不仅提出主张，还给出了具体工作流建议，例如设置夜间 cron 任务，让 LLM 获取上游变更、变基本地补丁并验证功能。评论者提出了现实反对意见，包括反复由 LLM 驱动的重建会浪费能源、基于 AI 的验证不可靠，以及当上游功能与下游改动冲突时维护分支的实际困难。

hackernews · bryanmikaelian · 8月3日 14:15 · [社区讨论](https://news.ycombinator.com/item?id=49156111)

**背景**: 开源软件长期以来都承诺用户可以自由查看和修改代码，但历史上大多数用户（即便是专业程序员）由于时间成本问题，往往依赖他人来完成修改。人们认为 LLM 降低了这一成本，可能让“个人定制”的梦想成为现实。但这场讨论也凸显出维护者付出的是实际劳动，而自动化又带来了新的低效和风险。

**社区讨论**: 评论者总体认可这一愿景，但对其可行性提出质疑。Simon Willison 指出 LLM 让最初的开源梦想变得更可行；kelnos 强烈反对取消配置文件、改由硬编码修改的做法，称其低效且浪费。theamk 形容提议的夜间 AI 驱动变基是“地狱般”的，因为 AI 是不可靠的执行者；维护者 lalitmaganti 则认为这过于理想化，因为工程师只希望工具能用，而维护开发工具是实实在在的工作。

**标签**: `#open source`, `#devtools`, `#LLM`, `#software engineering`, `#community discussion`

---

<a id="item-5"></a>
## [MiniMax H3 获 ComfyUI 首发支持：开放权重、原生音频与 2K 视频](https://blog.comfy.org/p/minimax-h3-day-0-support-in-comfyui) ⭐️ 8.0/10

ComfyUI 宣布对 MiniMax H3 提供 Day-0 支持。H3 是一个开放权重的全模态生成模型，能够在一次生成中输出带有原生同步音频的 2K 视频，早期社区测试表明其质量令人印象深刻。 这标志着开放权重视频生成迈出重要一步，将原生音频和 2K 输出带入本地可控的工作流。它巩固了 ComfyUI 作为 AI 视频制作模块化引擎的地位，也为创作者提供了闭源商业视频模型的免费替代方案。 H3 以两个任务专用 checkpoint 形式发布，每个 checkpoint 包含一个 Omni Transformer，以及处理器、分词器、文本编码器、Visual VAE 和独立的 Audio VAE。权重开放，结合动态 VRAM 卸载，2K 模型据称可在 RTX 3060 等 GPU 上本地运行。

hackernews · vblanco · 8月3日 13:34 · [社区讨论](https://news.ycombinator.com/item?id=49155629)

**背景**: MiniMax H3 是一个通用全模态生成模型，能够联合理解并生成文本、图像、视频和音频。ComfyUI 于 2023 年 1 月发布，是一个流行的开源节点式扩散模型界面，让用户通过精细控制构建自定义流程。Day-0 支持意味着模型发布当天就有可用的 ComfyUI 工作流和节点，降低了社区的实验门槛。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between Tasks and Modalities - MiniMax Research | MiniMax</a></li>
<li><a href="https://huggingface.co/MiniMaxAI/MiniMax-H3">MiniMaxAI/MiniMax-H3 · Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/ComfyUI">ComfyUI - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区成员分享实测结果，称赞模型的速度和输出质量，同时指出在非典型场景下仍存在伪影。一个值得注意的技术观点质疑了通过权重剪枝实现 66% 内存缩减的说法，并追问这种“无损”技术能否推广到 LLM；也有人报告在 16GB 的 4070 Ti Super 上生成 10 秒 480p 片段需要 10 分钟。

**标签**: `#AI`, `#video generation`, `#ComfyUI`, `#open weights`, `#audio`

---

<a id="item-6"></a>
## [安迪·帕夫洛加入 ClickHouse，领导新成立的 ClickHouse Labs](https://clickhouse.com/blog/andy-pavlo-joins-clickhouse) ⭐️ 8.0/10

知名数据库研究者、卡内基梅隆大学教授安迪·帕夫洛（Andy Pavlo）加入 ClickHouse，创立并领导 ClickHouse Labs。该合作旨在将学术数据库研究与产业开发连接起来。 此举对 OLAP 和数据库社区意义重大，因为它加强了产学研合作，有望加速分析型数据库系统的创新。同时，这也表明在公共数据库研究经费减少的情况下，大型数据库公司仍在投资研究。 该消息由 ClickHouse 官方博客发布，但 ClickHouse Labs 的具体研究方向尚未完全公布。帕夫洛以其在卡内基梅隆大学的数据库系统课程闻名，在新的岗位上他很可能继续其教学和教育活动。

hackernews · nikolay\_sivko · 8月3日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=49156011)

**背景**: ClickHouse 是一个面向联机分析处理（OLAP）优化的列式 SQL 数据库管理系统，既提供开源软件版本，也提供云服务。OLAP 是一种快速回答多维分析查询的方法，常用于商业智能和实时分析。安迪·帕夫洛是卡内基梅隆大学教授、知名数据库研究者，长期倡导数据库系统的学术研究。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://clickhouse-docs.vercel.app/docs/intro">What is ClickHouse ? | ClickHouse Docs</a></li>
<li><a href="https://en.wikipedia.org/wiki/Online_analytical_processing">Online analytical processing - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论区反应积极。有用户请帕夫洛推动 ClickHouse 资助学术界数据库研究，因为经费紧张。还有用户对 ClickHouse、StarRocks 等高性能 OLAP 产品与 Trino 在存储与计算分离、数据摄取方面如何融合表示好奇。也有人希望他卡内基梅隆的系列讲座能以赞助形式继续。

**标签**: `#databases`, `#clickhouse`, `#research`, `#olap`, `#industry-academia`

---

<a id="item-7"></a>
## [SemiAnalysis 深度解析 Kimi K3：压缩内存、跨层注意力与潜在专家路由](https://newsletter.semianalysis.com/p/kimi-k3-the-manos-the-mythos-the) ⭐️ 8.0/10

SemiAnalysis 发布了对 Kimi K3 架构的详细技术分析，重点介绍了压缩内存、跨层注意力和潜在专家路由这三项提升推理性能的核心创新。 这些技术针对长上下文和混合专家推理中的关键瓶颈，有望实现更快、更具成本效益的模型服务。对于 AI 基础设施工程师和模型开发者而言，这项分析对最前沿的推理优化具有参考价值。 该分析描述了三种机制：压缩内存（减少缓存开销）、跨层注意力（允许跨层信息检索）和潜在专家路由（改进专家选择）。摘要中未包含量化基准或模型规模的具体信息。

rss · Semianalysis · 8月3日 19:42

**背景**: 标准 Transformer 在推理时需要维护不断增长的键值缓存；压缩 Transformer 通过压缩旧激活而非直接丢弃来解决这一问题。普通注意力只在同一层内沿序列维度运作，而跨层注意力方法允许 token 从其他层检索信息。混合专家（MoE）模型每个 token 只激活部分参数，潜在路由方法通过学习对输入聚类，以实现更均衡、更有效的专家利用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/1911.05507">COMPRESSIVE TRANSFORMERS FOR LONG-RANGE SEQUENCE MODELLING Jack W. Rae∗∗† ‡</a></li>
<li><a href="https://www.datacamp.com/blog/attention-residuals-explained">Attention Residuals Explained: Rethinking Transformer Depth | DataCamp</a></li>
<li><a href="https://arxiv.org/html/2506.21328">Latent Prototype Routing: Achieving Near-Perfect Load Balancing in Mixture-of-Experts Preprint - Work in Progress. Code: Here</a></li>

</ul>
</details>

**标签**: `#AI`, `#Kimi K3`, `#architecture`, `#inference`, `#memory`

---

<a id="item-8"></a>
## [审稿人呼吁：无复现代码的论文应被直接拒稿](https://www.reddit.com/r/MachineLearning/comments/1vei12v/its_time_to_desk_reject_papers_that_dont_include/) ⭐️ 8.0/10

一位机器学习审稿人在 Reddit 发帖称，今年审阅的 12 篇论文中只有 1 篇附有可完整复现结果的代码，并呼吁顶会直接拒收未提供可复现代码的论文。作者认为，若不附代码就无法验证结果，因此应将其设为投稿的基本门槛。 此事关乎机器学习研究领域的可复现性危机：缺少代码时，审稿人无法验证结果，隐藏的 bug 可能使结论失效。若该政策被采纳，将改变现有激励机制，促使作者公开代码，从而提升已发表研究的可靠性。 作者提到，12 篇论文中 4 篇只有部分代码、7 篇完全没有代码，而在 5 篇提供了部分代码的论文中有 3 篇存在明显错误，足以推翻其实验结果。作者认为根本问题在于激励机制扭曲：公开代码只会增加被审稿人发现问题的风险，因此必须对隐藏代码的行为施加实质性惩罚。

reddit · r/MachineLearning · /u/Flaky-Ambition5900 · 8月3日 16:17

**背景**: Desk rejection（直接拒稿）指编辑在稿件送外审之前就将其退回，通常是因为稿件不满足基本要求。AUROC（受试者工作特征曲线下面积）是二分类任务常用指标，用于衡量模型将正样本排在负样本之前的能力。可复现性即“运行相同代码得到相同结果”，一直是机器学习领域关注的焦点，因为细小的实现错误也可能造成巨大影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://peerreviewai.org/guides/desk-rejection-prevention">How to Avoid Desk Rejection | PeerReviewAI</a></li>
<li><a href="https://glassboxmedicine.com/2019/02/23/measuring-performance-auc-auroc/">Measuring Performance: AUC ( AUROC ) – Glass Box Medicine</a></li>
<li><a href="https://www.moderndescartes.com/essays/auc_intuition/">Understanding the AUROC metric</a></li>

</ul>
</details>

**标签**: `#reproducibility`, `#machine learning`, `#research policy`, `#code review`, `#conferences`

---

<a id="item-9"></a>
## [美犯罪实验室 DNA 设备曝安全漏洞，30 年证据面临篡改风险](https://www.wsj.com/tech/cybersecurity/security-flaw-placed-30-years-of-dna-evidence-at-risk-of-hacking-1932775a) ⭐️ 8.0/10

研究人员发现，美国多数犯罪实验室使用的 DNA 分析设备存在安全漏洞，可让自 1995 年以来的数字 DNA 证据文件遭到无法检测的篡改。他们借助 Anthropic 的 Claude AI，约 45 分钟就篡改了一份 DNA 扫描文件，且未触发常用分析软件的警报。 该漏洞威胁到美国约 30 年来用于刑事侦查和法庭审判的法医 DNA 证据的完整性。一旦被利用，可能影响司法判决、削弱公众对司法系统的信任，并暴露出全美 200 多家犯罪实验室缺乏统一安全监管的问题。 设备制造商 Thermo Fisher Scientific 已于 7 月私下承认该漏洞，并于上周五发布高危安全公告，推出加入数字签名的软件更新以保护文件。研究人员指出，该漏洞是否影响在审或已结案件尚不明确，目前也没有漏洞被实际利用的报告。

telegram · zaihuapd · 8月3日 05:15

**背景**: DNA 分析仪是一种自动化仪器，利用毛细管电泳技术分离和识别 DNA 片段，并生成用于法医鉴定的数字数据文件。美国许多犯罪实验室几十年来一直依赖这类设备，但这些文件缺乏数字签名等强完整性保护，因此容易被篡改。这项研究也表明，Claude 等 AI 工具可能让针对法医系统的复杂网络攻击变得更加容易实施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theverge.com/science/974287/a-security-flaw-in-widely-used-crime-lab-equipment-exposed-digital-dna-evidence-to-undetectable-tampering">A security flaw in widely used crime lab equipment exposed digital DNA evidence to undetectable tampering. | The Verge</a></li>
<li><a href="https://www.hindustantimes.com/technology/security-flaw-placed-30-tears-of-dna-evidence-at-risk-of-hacking-101785681888060.html">Security flaw placed 30 tears of DNA evidence at risk of hacking | Technology News (HT Tech)</a></li>
<li><a href="https://news.am/en/news/1053194">Wall Street Journal: DNA test data in US found to be vulnerable to hacking for 30 years - NEWS.am</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#forensic-science`, `#vulnerability`, `#DNA-analysis`, `#public-safety`

---

<a id="item-10"></a>
## [美至少 50 名警员被控以摄像头窥探前任](https://www.washingtonpost.com/technology/2026/08/02/how-police-officers-used-vast-network-cameras-spy-their-exes/) ⭐️ 8.0/10

《华盛顿邮报》8 月 2 日报道，至少 50 名美国执法人员被指控或起诉滥用 Flock 等自动车牌识别系统进行非法监控。其中 26 起案件涉嫌窥探配偶、女友、前任或心仪女性，46 起案件涉及使用 Flock 系统。 这项调查暴露出执法监控技术监管方面的系统性缺陷，显示广泛部署的车牌识别网络可被用作个人跟踪工具。随着此类网络在全国铺开，它凸显了加强州和联邦法规、审计及问责机制的紧迫性。 Flock 表示其网络拥有逾 12 万台摄像头，覆盖 6000 多个社区，每月记录约 200 亿次车牌扫描。公司承认滥用难以完全避免，已推出可选的“审计辅助”功能，而目前仅 13 个州要求审计，至少 8 个州将这类滥用定为犯罪。

telegram · zaihuapd · 8月3日 09:03

**背景**: 自动车牌识别（ALPR）系统通过摄像头和软件自动捕获、分析并存储车辆车牌信息，常与数据库比对并生成警报。Flock Safety 是美国主要的 ALPR 摄像头及监控设备私营供应商，其全国网络可在各执法机构间共享数据。此类系统正越来越多地被执法部门用于破案，但其大规模数据采集也引发了隐私和公民自由方面的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety - Wikipedia</a></li>
<li><a href="https://www.dhs.gov/science-and-technology/saver/automatic-license-plate-readers">Automatic License Plate Readers | Homeland Security</a></li>
<li><a href="https://www.flocksafety.com/products/license-plate-readers">License Plate Readers (LPR) Cameras | Flock Safety</a></li>

</ul>
</details>

**标签**: `#surveillance`, `#privacy`, `#law enforcement`, `#license plate recognition`, `#investigative report`

---

<a id="item-11"></a>
## [苹果遭 325 亿美元集体诉讼：相册人脸识别被指违规](https://appleinsider.com/articles/26/08/03/apple-photos-facial-features-prompt-a-325b-class-action-lawsuit) ⭐️ 8.0/10

美国第七巡回上诉法院驳回苹果的上诉，允许一起索赔高达 325 亿美元的集体诉讼继续审理。诉讼指控苹果相册应用未经同意收集人脸生物识别数据，为照片中的人物生成面部特征并经 iCloud 同步，波及约 650 万伊利诺伊州居民。 该案件可能为美国生物识别隐私诉讼树立重要先例，让大型科技公司面临巨额赔偿风险。它也凸显了设备端与云端人脸识别功能日益增长的合规法律风险。 根据伊利诺伊州《生物识别信息隐私法》（BIPA），每次过失违规赔偿 1000 美元，故意或鲁莽违规赔偿 5000 美元，且无需证明实际损害。苹果曾辩称其面部识别不构成生物识别标识符、且已有隐私保护措施，但法院仍裁定该集体诉讼可以推进。

telegram · zaihuapd · 8月3日 14:33

**背景**: 《生物识别信息隐私法》（BIPA）于 2008 年在伊利诺伊州颁布，是美国第一部规范私营实体收集、使用和存储生物识别标识符或信息的州法律。人脸识别技术通过将面部独特特征转换为数字面部特征（faceprint），再用于识别或验证个人身份。由于 BIPA 无需证明实际损害即可主张法定赔偿，它已成为针对科技公司的集体诉讼的常用法律工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kelleydrye.com/trending/the-illinois-biometric-information-privacy-act-bipa">The Illinois Biometric Information Privacy …</a></li>
<li><a href="https://www.wikiwand.com/en/articles/Biometric_Information_Privacy_Act">Biometric Information Privacy Act - Wikiwand</a></li>
<li><a href="https://builtin.com/articles/facial-recognition-technology-explained">Facial Recognition , Explained | Built In</a></li>

</ul>
</details>

**标签**: `#privacy`, `#legal`, `#biometric-data`, `#apple`, `#class-action`

---

<a id="item-12"></a>
## [苹果就英国政府 iCloud 后门要求提起诉讼](https://www.ft.com/content/2cc9c96a-0e5b-4c33-a95a-3d11072a145c?syn-25a6b1a6=1) ⭐️ 8.0/10

苹果已向英国调查权力法庭提起法律申诉，挑战英国政府要求其开放加密 iCloud 云备份访问权限的「技术能力通知」。此举质疑政府签发此类通知的权限。 这是围绕加密与隐私的一次重大法律与政策交锋，苹果主张任何「后门」都会削弱所有用户的安全。结果可能为全球政府与科技公司如何处理加密要求树立先例。 在内政部发出新通知后，苹果于 2025 年 2 月在英国下架了 iCloud 高级数据保护功能。Privacy International 和 Liberty 也就同一份 TCN 提起了申诉，法庭已定于下月举行案件管理听证。

telegram · zaihuapd · 8月3日 15:40

**背景**: 「技术能力通知」是英国政府根据《2016 年调查权力法》发出的命令，要求服务提供商维持或开发技术能力，以便未来能够配合执行令状。调查权力法庭是独立的司法机关，负责审理针对公共机构监控行为的投诉。苹果的「高级数据保护」功能采用端到端加密保护 iCloud 备份，意味着即便是苹果，在没有用户密钥的情况下也无法访问这些数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://predaxia.com/glossary/technical-capability-notice/">Technical Capability Notice : UK government order under... | Predaxia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Investigatory_Powers_Tribunal">Investigatory Powers Tribunal</a></li>
<li><a href="https://support.apple.com/en-us/108756">How to turn on Advanced Data Protection for iCloud - Apple Support</a></li>

</ul>
</details>

**标签**: `#Apple`, `#UK Government`, `#iCloud`, `#Encryption`, `#Privacy`

---