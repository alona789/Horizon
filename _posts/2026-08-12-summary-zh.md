---
layout: default
title: "Horizon Summary: 2026-08-12 (ZH)"
date: 2026-08-12
lang: zh
---

> 从 37 条内容中筛选出 9 条重要资讯。

---

1. [DeepSeek 发布 V4 Pro 0813，引发社区热议](#item-1) ⭐️ 8.0/10
2. [Tailscale 将数据库损坏追根溯源到存在 16 年的 SQLite WAL-Reset 漏洞](#item-2) ⭐️ 8.0/10
3. [Qwen 发布 2.4T 参数开源 MoE 模型 Qwen3.8-2.4T-A95B](#item-3) ⭐️ 8.0/10
4. [uBlock Origin 放弃屏蔽 Facebook 广告](#item-4) ⭐️ 8.0/10
5. [Grok 4.6 在 Artificial Analysis 智能指数上获得 61 分](#item-5) ⭐️ 8.0/10
6. [AI 正在淘汰软件工程的中间层](#item-6) ⭐️ 8.0/10
7. [车牌识别器搜索应要求搜查令](#item-7) ⭐️ 8.0/10
8. [Adam 逐坐标自适应破坏低秩偏置](#item-8) ⭐️ 8.0/10
9. [LTX 开源视频模型 LTX-2.5，单张 RTX 5090 即可本地运行](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek 发布 V4 Pro 0813，引发社区热议](https://openrouter.ai/deepseek/deepseek-v4-pro-0813) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek V4 Pro 0813 预览版，这是一个混合专家\(MoE\)模型，总参数 1.6T（激活 49B），支持 100 万 token 上下文。在 OpenRouter 上，输入价格为每百万 token 0.435 美元，输出价格为每百万 token 0.87 美元。 该发布之所以重要，是因为 DeepSeek 继续在低成本、开放权重的前沿模型上发力，直接影响开发者和企业在闭源与开源模型之间的选择。社区测试显示，它能以远低于 Grok 等竞品的成本完成大量编程任务，成为 AI 开发者的重要选项。 OpenRouter 上的页面本身几乎没有有用信息，社区用户建议参考官方 API 文档和基准测试帖子。V4 系列还包括总参数 284B（激活 13B）的 DeepSeek-V4-Flash，两款模型均支持 100 万 token 上下文。

hackernews · explosion-s · 8月12日 16:04 · [社区讨论](https://news.ycombinator.com/item?id=49274600)

**背景**: DeepSeek 是一家中国 AI 实验室，其 R1 聊天机器人于 2025 年 1 月发布后成为美国 iOS App Store 下载量最高的免费应用，被广泛认为颠覆了 AI 行业。此前的 DeepSeek-V3 等模型采用混合专家\(MoE\)和 Multi-Head Latent Attention\(MLA\)架构，以实现高效推理和低成本训练，V4 延续了这一架构方向。DeepSeek 模型以开放权重和低 API 价格著称，但也因内容审查和数据隐私问题受到关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_%28product%29">DeepSeek (product)</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Pro">deepseek-ai/DeepSeek-V4-Pro · Hugging Face</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-pro">DeepSeek V4 Pro - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一：有人批评这个帖文只链接了信息量不足的 OpenRouter 页面，也有人分享了实际测试结果。一位开发者报告称，DeepSeek V4 Pro 0813 处理一个功能耗时 12 分钟、花费 0.12 美元但有 bug，而 Grok 4.6 耗时更短、花费 1.41 美元且无 bug；另一位用户表示自己最关心的是以最低成本完成任务。还有多位用户表示，在使用 Flash 更新后体验积极，迫不及待想试试新模型。

**标签**: `#DeepSeek`, `#LLM`, `#AI`, `#model-release`, `#cost-analysis`

---

<a id="item-2"></a>
## [Tailscale 将数据库损坏追根溯源到存在 16 年的 SQLite WAL-Reset 漏洞](https://tailscale.com/blog/sqlite-wal-reset-bug) ⭐️ 8.0/10

Tailscale 定位到 SQLite 预写日志（WAL）机制中一个存在 16 年之久、可能导致数据库损坏的漏洞，并资助了一个开源 VFS shim，该工具几乎立即帮助隔离了竞态条件。SQLite 开发者将其正式命名为“WAL-Reset bug”。 这件事意义重大，因为它展示了即使像 SQLite 这样经过大量测试的软件，细微的数据库漏洞也可能潜伏超过十年，同时也说明了针对性的开源资助能如何加速问题诊断。对于依赖 SQLite 构建高可靠性应用的系统工程师而言，这具有很强的实践价值。 SQLite 开发者估计该漏洞至少已存在 16 年，而且极为罕见，以至于他们不得不在测试环境中加入代码来刻意触发它。Tailscale 资助的 VFS shim 是一个通用调试工具，未来也能帮助定位类似的漏洞。

hackernews · ropbear · 8月12日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=49272832)

**背景**: SQLite 是一种广泛使用的嵌入式数据库，支持预写日志（WAL）模式：变更先写入单独的“-wal”文件，之后才通过检查点（checkpoint）合并进主数据库。VFS（虚拟文件系统）层是 SQLite 的操作系统抽象接口，使 SQLite 能跨操作系统运行，并允许类似 checksum VFS shim 这样的扩展来增加完整性检查。WAL 重置过程中的一个竞态条件，即使在单一写入者的设计下（这正是 SQLite 的预期使用方式）也可能导致数据库损坏。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tailscale.com/blog/sqlite-wal-reset-bug">How Tailscale helped find the SQLite WAL - Reset bug</a></li>
<li><a href="https://antithesis.com/blog/2026/wal-reset-bug/">Breaking the WAL | Antithesis</a></li>
<li><a href="https://www.sqlite.org/wal.html">Write-Ahead Logging</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了这篇技术文章以及 Tailscale 资助开源调试工具的决定。Simon Willison 强调这是一个公司出资开发特定调试工具的有趣案例；其他人则对详细的 bug 分析表示赞赏，并表示对 Tailscale 的信任度有所提升。

**标签**: `#sqlite`, `#database-corruption`, `#debugging`, `#tailscale`, `#open-source`

---

<a id="item-3"></a>
## [Qwen 发布 2.4T 参数开源 MoE 模型 Qwen3.8-2.4T-A95B](https://huggingface.co/Qwen/Qwen3.8-2.4T-A95B) ⭐️ 8.0/10

Qwen 在 Hugging Face 上发布了 Qwen3.8-2.4T-A95B，这是一款混合专家（MoE）语言模型，总参数量 2.4 万亿，激活参数 950 亿。模型原生支持 262,144 个 token 的上下文长度，可扩展至 1,010,000 个 token，并提供 BF16 和 FP8 两种权重版本。 这是目前发布的最大开源权重 MoE 模型之一，使 Qwen 成为 Kimi k3 等模型的直接竞争者，并与 DeepSeek 的最新发布同台竞技。其巨大规模将前沿能力带入开源生态，同时也带来实际部署挑战，影响社区对模型的量化、服务化和评估方式。 完整的 BF16 权重约为 4.9TB，而 Unsloth 等社区的 1-bit 量化版本可将其压缩到约 397GB，每个 token 仍有 950 亿激活参数。此次开源版本不具备商业版 Qwen3.8-Max 的视觉输入和默认 1M 上下文功能，其许可证规定内部使用或年收入低于 5000 万美元时可免费使用，超出该门槛则受到限制。

hackernews · Philpax · 8月12日 15:01 · [社区讨论](https://news.ycombinator.com/item?id=49273478)

**背景**: 混合专家（MoE）是一种将模型拆分为多个专门化子网络（即专家）的架构，并通过路由器为每个 token 只激活其中一小部分参数。这使得总参数量达万亿级的模型，其推理计算量远低于同规模稠密模型。激活参数指的是推理时实际使用的参数子集，而总参数则包含网络中所有专家。FP8 等量化技术通过降低数值精度来缩小模型体积，并在支持的硬件上加速推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>
<li><a href="https://www.mindstudio.ai/blog/mixture-of-experts-architecture-glm-5-2-active-parameters">Mixture of Experts Architecture Explained: How GLM 5.2 Runs 40B Active ...</a></li>
<li><a href="https://aifor.dev/concepts/fp8-quantization">fp 8 - quantization</a></li>

</ul>
</details>

**社区讨论**: 社区反应褒贬不一：有人指出该模型发布时仅有 BF16 和 FP8 版本、尚无 QAT q4 量化，因此比 Kimi k3 更难部署；也有人兴奋地认为 397GB 的 1-bit 量化版本可能在一台价格合理的消费级机器上带来 Opus 4.5 级别的性能。另有评论指出开源版本缺少 Qwen3.8-Max 的视觉输入和 1M 上下文，还有用户调侃说自己会“直接在 Intel n100 上跑起来”。同时有人提到 DeepSeek V4-Pro-0813 的基准分数也已公布。

**标签**: `#AI/ML`, `#LLM`, `#Qwen`, `#MoE`, `#Open Weights`

---

<a id="item-4"></a>
## [uBlock Origin 放弃屏蔽 Facebook 广告](https://digitalescapetools.com/2026/08/ublock-origin-stops-chasing-facebook-ads.html) ⭐️ 8.0/10

uBlock Origin 已正式停止尝试屏蔽 Facebook 上的广告，理由是 Facebook 采取了越来越复杂的反广告拦截技术。维护者宣布不再维护针对 Facebook 广告的过滤规则。 这标志着广告拦截军备竞赛中的一次显著挫折，影响数以百万计使用 uBlock Origin 清理 Facebook 信息流的用户。这也凸显出，在那些大力投资反制措施的大型平台上屏蔽广告越来越困难，未来解决方案可能会转向基于人工智能的方法。 Facebook 通过频繁更新代码和混淆技术来使静态过滤列表失效，需要维护者持续不断进行维护，而 uBlock Origin 团队不再愿意承担这项工作。用户仍可通过自定义过滤规则或第三方工具等方式屏蔽 Facebook 广告，但这些方法可能并不稳定。

hackernews · Markoff · 8月12日 11:28 · [社区讨论](https://news.ycombinator.com/item?id=49270726)

**背景**: uBlock Origin 是一款免费、开源的浏览器广告拦截扩展，适用于 Firefox、Chrome、Edge 等浏览器，以低 CPU 和内存占用著称。广告拦截器通常依赖过滤列表来匹配与广告相关的 URL 和页面元素，但反广告拦截系统可以动态改变代码、检测拦截器，并通过混淆方式投放广告。Facebook 在这场军备竞赛中尤为激进，使得静态过滤列表几乎无法跟上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/UBlock_Origin">uBlock Origin - Wikipedia</a></li>
<li><a href="https://ublockorigin.com/">uBlock Origin - Free, open-source ad blocker extension</a></li>
<li><a href="https://support.adblockultimate.net/en/articles/9240458-anti-adblock-techniques">Anti - adblock techniques | AdBlocker Ultimate Help Center</a></li>

</ul>
</details>

**社区讨论**: 评论者的反应不一：有人支持这一决定，认为 Facebook 的商业模式使广告拦截难以奏效，平台最终可能会衰落；也有人推测这场军备竞赛最终会以能视觉识别并遮盖广告的计算机视觉模型收场。一些用户指出了这场猫鼠游戏的性质，并认为避免 Facebook 广告的唯一可靠方法就是彻底离开该平台。

**标签**: `#ad-blocking`, `#privacy`, `#facebook`, `#ublock-origin`, `#arms-race`

---

<a id="item-5"></a>
## [Grok 4.6 在 Artificial Analysis 智能指数上获得 61 分](https://artificialanalysis.ai/articles/grok-4-6-benchmarks-and-analysis) ⭐️ 8.0/10

SpaceXAI 发布的 Grok 4.6 在 Artificial Analysis 智能指数上获得 61 分，该指数是一个综合基准，衡量模型在推理、编程和多步任务等方面的能力。此次发布在 Grok 4.5 基础上，重点关注长时间运行的智能体以及交互式视觉工作。 这一基准测试结果使 Grok 4.6 跻身前沿模型之列，并标志着 AI 编程和智能体工具领域竞争加剧。定价变化和快速的编程性能可能会影响开发者在主流 AI 助手间的选择。 Artificial Analysis 智能指数 v4.1.1 包含 GDPval-AA v2、Terminal-Bench v2.1、SciCode 和 Humanity&\#x27;s Last Exam 等基准。社区反馈指出，与 Grok 4.5 相比，Grok 4.6 的缓存读取定价从 0.30 美元上升到 0.50 美元，同时一些用户认为 Grok Build 比 Claude Code 更快。

hackernews · wertyk · 8月12日 16:54 · [社区讨论](https://news.ycombinator.com/item?id=49275385)

**背景**: Grok 是 SpaceXAI 开发的一系列大语言模型，由 Elon Musk 于 2023 年 11 月推出，并集成到 X 社交网络中。Artificial Analysis 智能指数是一个综合得分，衡量语言模型在推理、编程、知识和多步任务方面的能力。Grok 4.6 基于 Grok 4.5，并与 SpaceXAI 子公司 Cursor 联合开发，Cursor 的套餐中也包含 Grok 模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/">AI Model &amp; API Providers Analysis | Artificial Analysis</a></li>
<li><a href="https://artificialanalysis.ai/evaluations/artificial-analysis-intelligence-index">Artificial Analysis Intelligence Index | Artificial Analysis</a></li>
<li><a href="https://x.ai/news/grok-4-6">Introducing Grok 4.6 | SpaceXAI</a></li>

</ul>
</details>

**社区讨论**: 社区评论者大多称赞 Grok 4.6 的编程能力，有人表示它沟通更好、比 Claude 更快，还有人指出 Grok Build 比 Claude Code 快 2 到 5 倍。另外一些人指出缓存读取定价从 0.30 美元几乎翻倍到 0.50 美元，还有评论者表示，如果达到前沿水平这么容易，这让他们看好 Gemini。

**标签**: `#AI`, `#Grok`, `#LLM`, `#Benchmarks`, `#Coding`

---

<a id="item-6"></a>
## [AI 正在淘汰软件工程的中间层](https://blog.florianherrengt.com/ai-removing-middle-class-software-engineering.html) ⭐️ 8.0/10

一篇新博文指出，AI 编程助手正在自动化日常编码工作，从而淘汰软件工程中层的职位。文章认为，职业阶梯正在被压缩，工程师只能更专注于高层次的判断和架构设计，而不是亲手编写代码。 这一论点切中了当前关于 AI 与就业争论的核心，表明基于大语言模型的工具不仅仅是在辅助开发者，而是在重塑整个软件工程就业市场。若该观点成立，它将改变企业的招聘方式、初级工程师的晋升路径，以及软件工程中真正有价值的技能。 文章警告说，&\#x27;糟糕的&\#x27;工程师可以借助 AI 将糟糕的工程实践在组织内放大十倍，并强调绝不能把批判性思维和学习过程外包给大语言模型。文章还指出，过去由资深工程师把任务拆成工单交给初级工程师完成的传统交接方式正变得不再必要。

hackernews · florianherrengt · 8月12日 13:20 · [社区讨论](https://news.ycombinator.com/item?id=49271994)

**背景**: AI 编程助手是使用大语言模型来帮助开发者完成代码生成、调试、测试和文档等任务的工具。这类工具近年来发展迅速，已经能够根据自然语言提示生成大量可运行的代码。这引发了一场更广泛的讨论：自动化是否会减少对人类程序员的需求，还是仅仅将他们的注意力转向代码审查、架构设计和产品决策。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_coding_assistant">AI coding assistant</a></li>
<li><a href="https://www.turing.com/blog/software-engineering-with-llms">Revolutionizing Software Engineering with LLMs | Turing</a></li>

</ul>
</details>

**社区讨论**: 评论者部分认同文章论点，但也进行了补充：有读者强调，长期任职但已失去热情的&\#x27;糟糕&\#x27;工程师可以用 AI 把自己的低质量产出扩大十倍；另有人将这一趋势称为&\#x27;Stack Overflow 工程师的自动化&\#x27;，并指出资深与初级工程师之间的交接在消失。还有人提醒不要把批判性思维外包给 LLM，质疑目前是否有确凿证据表明岗位确实流失，并提出经济学的看法：工具改进最终可能不会带来净变化。

**标签**: `#AI`, `#Software Engineering`, `#Career Impact`, `#LLMs`, `#Future of Work`

---

<a id="item-7"></a>
## [车牌识别器搜索应要求搜查令](https://andrewpwheeler.com/2026/08/12/license-plate-reader-searches-should-require-a-warrant/) ⭐️ 8.0/10

在一篇新博文中，犯罪学家 Andrew Wheeler 主张应禁止无搜查令搜索车牌识别器（ALPR）数据库。文章呼吁执法部门在查询自动车牌识别器收集的位置数据前须获得法院的监督许可。 这之所以重要，是因为 Flock 等 ALPR 网络在美国迅速扩张，使得对普通驾驶者的行踪进行大规模追踪成为可能。搜查令要求将增加司法监督，并回应有关警方滥用数据、跟踪行为以及公共场所隐私受到侵蚀的担忧。 Wheeler 认为摄像头覆盖所有公共空间是不可避免的趋势，但法律保障也必须跟上。评论者指出，ALPR 实际上是通用型联网相机，而且目前各地对数据访问的政策不一，有些地方既不愿要求搜查令，也不愿响应公共记录请求。

hackernews · apwheele · 8月12日 14:43 · [社区讨论](https://news.ycombinator.com/item?id=49273165)

**背景**: 自动车牌识别器（ALPR）是一种摄像头，能够捕捉车牌图像以及时间戳和位置信息，警方和市政部门常将其用于查找被盗车辆或执行停车规则等目的。隐私倡导者担心，汇总这些数据会形成个人长期行踪的可搜索记录。主要 ALPR 供应商 Flock 已在全国安装超过 10 万台摄像机，引发了草根阶层的隐私反弹。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sls.eff.org/technologies/automated-license-plate-readers-alprs">Automated License Plate Readers</a></li>
<li><a href="https://tribune.net.ph/2026/08/09/angers-mount-over-car-license-plate-cameras">Angers mount over car license plate cameras | Daily Tribune</a></li>
<li><a href="https://mass.streetsblog.org/2026/08/05/guest-column-for-privacy-advocates-license-plate-readers-are-a-bigger-threat-than-carefully-regulated-speed-enforcement-cameras">Guest Column: For Privacy Advocates, License Plate Readers Are...</a></li>

</ul>
</details>

**社区讨论**: 评论者对无搜查令的 ALPR 监控表达了强烈质疑。有人认为 ALPR 是可重新编程的通用摄像头，并指出没人预料门铃摄像头会加入大规模监控网络。还有人提议用加密方法让追踪变得更难，另有人认为搜查令要求仍是‘创可贴’式的补救，默认情况下不应允许大规模监视。

**标签**: `#privacy`, `#surveillance`, `#law`, `#license-plate-readers`, `#technology-policy`

---

<a id="item-8"></a>
## [Adam 逐坐标自适应破坏低秩偏置](https://www.reddit.com/r/MachineLearning/comments/1vmjb3p/the_loss_does_not_see_the_basis_but_adam_does_r/) ⭐️ 8.0/10

一项关于欠定矩阵感知的新研究表明，Adam 的逐坐标二阶矩会破坏因子化模型 W = UV^T 的旋转不变性，从而消除梯度下降固有的低秩偏置。在训练损失匹配的九种更新规则比较中，GD、共享标量 Adam、Muon 和 Shampoo 保留了该偏置，而 Adam、RMSProp、Lion、signum 和 Adafactor 失去了它。 该结果把破坏隐式低秩正则的机制归结为逐坐标各向异性，而非泛泛的自适应性。它为优化器设计者和实践者提供了一份具体指南，说明哪些自适应方法更可能保留矩阵分解和深度学习中的低秩结构。 所有九种更新规则都在匹配的训练损失下进行比较；在一个把 Adam 的分母从逐坐标插值为单一共享标量的一参数族中，恢复率单调上升。Muon 在真正低秩目标上表现精确，但加入谱尾后退化最快，交叉点约在 4% 谱尾能量处；作者还报告，把逐坐标裁剪改为全局范数裁剪后，他自己的优化器恢复误差从 0.347 降到 0.220。高光谱数据上 43–44% 的留出误差降低使用的是仅训练集的学习率规则，该规则让 Adam 在自己的网格上拿到最差的学习率，因此主要结论是机制本身，而非这个数字。

reddit · r/MachineLearning · /u/EtherealGlyph · 8月12日 16:39

**背景**: 在因子化模型 W = UV^T 中，同一个 W 可以通过插入一个旋转矩阵 Q 写成不同的因子对：\(U,V\) → \(UQ, VQ\)，因此损失函数对这类基变换是不变的。梯度下降尊重这种不变性，这与其在过参数化矩阵分解中隐式偏向低秩解的特性有关。Adam 等自适应优化器会按坐标估计二阶矩，而二阶矩取决于 U 和 V 写在哪一组基下，因此可能破坏这种不变性并消除低秩偏置。Muon 和 Shampoo 是预条件优化器，在大模型训练中表现强劲，本研究中它们属于保留该偏置的一类方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2011.13772">Gradient Descent for Deep Matrix Factorization</a></li>
<li><a href="https://grokipedia.com/page/muon-optimizer">Muon optimizer</a></li>
<li><a href="https://arxiv.org/pdf/1802.09568">Shampoo</a></li>

</ul>
</details>

**标签**: `#optimization`, `#Adam`, `#implicit bias`, `#low-rank`, `#matrix sensing`

---

<a id="item-9"></a>
## [LTX 开源视频模型 LTX-2.5，单张 RTX 5090 即可本地运行](https://ltx.io/model/ltx-2-5) ⭐️ 8.0/10

LTX 发布了开源视频生成基础模型 LTX-2.5，完整开放权重、训练代码与推理管线。该模型可在单张 RTX 5090 上本地运行，支持文生视频与图生视频，并改进了多镜头连贯性。 开源一个训练与推理代码完整的视频生成模型，大幅降低了开发者与研究人员的使用门槛。支持消费级 GPU 本地运行，使先进的视频生成从云端走向桌面，将加速相关实验与真实应用的落地。 LTX-2.5 采用了新的扩散视频解码器，该解码器本身是一个小型扩散模型，在潜变量条件下对像素去噪，而非传统卷积解码器。模型还使用 Gemma 4 12B 文本编码器；在基于 98 个提示词的自动瑕疵评测中，LTX 2.5 Pro 在十款模型中排名第一。

telegram · zaihuapd · 8月12日 02:15

**背景**: LTX 是一家专注于 AI 视频生成的厂商，此前已发布开源模型 LTX。视频生成模型可根据文本或图像输入合成新的视频帧，LTX-2.5 进一步通过扩散解码器对此进行了改进。Gemma 4 12B 是 Google 推出的统一、无编码器的多模态模型，参数量为 120 亿。完整开放权重并支持消费级 GPU 运行，使得这一发布对过去只能依赖昂贵云服务的从业者尤为重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ltx.io/model/ltx-2-5">LTX - 2 . 5 : LTX&#x27;s Latest AI Open-Source Foundation Model | LTX</a></li>
<li><a href="https://github.com/huggingface/diffusers/blob/main/src/diffusers/pipelines/ltx2/pipeline_ltx2_diffusion_decode.py">diffusers/src/diffusers/pipelines/ltx2/pipeline_ltx2_ diffusion _ decode .py...</a></li>
<li><a href="https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemma-4-12b/">Introducing Gemma 4 12 B</a></li>

</ul>
</details>

**标签**: `#video generation`, `#open-source`, `#AI`, `#diffusion model`, `#LTX`

---