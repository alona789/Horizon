---
layout: default
title: "Horizon Summary: 2026-07-09 (ZH)"
date: 2026-07-09
lang: zh
---

> 从 37 条内容中筛选出 14 条重要资讯。

---

1. [OpenAI 发布 GPT-5.6，在 ARC-AGI-3 上达到 SOTA](#item-1) ⭐️ 9.0/10
2. [Bun 从 Zig 重写为 Rust](#item-2) ⭐️ 9.0/10
3. [TypeScript 7.0 正式发布：Go 重写带来最高 12 倍速度提升](#item-3) ⭐️ 9.0/10
4. [欧盟议会批准聊天控制 1.0，争议不断](#item-4) ⭐️ 8.0/10
5. [腾讯 Hy3 小型 AI 模型对标 DeepSeek V4 Flash](#item-5) ⭐️ 8.0/10
6. [2026 年 12 月不会增加闰秒](#item-6) ⭐️ 8.0/10
7. [Meta 发布 Muse Spark 1.1，具备自主智能体能力](#item-7) ⭐️ 8.0/10
8. [GPT-Live：OpenAI 新语音模式，可委托 GPT-5.5 处理复杂任务](#item-8) ⭐️ 8.0/10
9. [Meta 超级智能进展：计算扩张与强化学习初创公司](#item-9) ⭐️ 8.0/10
10. [IMGNet：通过符号模式匹配进行人脸验证](#item-10) ⭐️ 8.0/10
11. [蚂蚁集团开源 LingBot-Video，全球首个 MoE 具身视频模型](#item-11) ⭐️ 8.0/10
12. [大疆 EV50 无人机飞越珠峰 8861 米创纪录](#item-12) ⭐️ 8.0/10
13. [国家超算互联网核心节点在郑州上线](#item-13) ⭐️ 8.0/10
14. [OpenAI 与美国战争部达成禁止 AI 用于国内监控的协议](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-5.6，在 ARC-AGI-3 上达到 SOTA](https://openai.com/index/gpt-5-6/) ⭐️ 9.0/10

OpenAI 发布了最新旗舰模型 GPT-5.6，在 ARC-AGI-3 基准测试中取得了 7.8%的新 SOTA 成绩。该模型提供三种规格：Luna、Terra 和 Sol。 在 ARC-AGI-3 上创下新基准标志着智能体智能的重大进步，因为该模型首次能够完成 ARC-AGI-3 游戏。此次发布巩固了 OpenAI 在前沿 AI 能力方面的领先地位，并提供三个层级以满足不同部署需求。 根据开发者指南，GPT-5.6 改进了意图理解并保留原始图像尺寸。Sol 是首个经验证的在 ARC-AGI-3 游戏中获胜的前沿模型，得分为 7.8%。

hackernews · logickkk1 · 7月9日 17:04 · [社区讨论](https://news.ycombinator.com/item?id=48849066)

**背景**: ARC-AGI-3 是一个用于评估智能体智能的交互式基准测试，要求模型在没有明确指令的情况下在陌生环境中探索、推断目标并规划行动。GPT-5.6 是 OpenAI 的最新模型，接替 GPT-5.5，提供三种以天体命名的规格：Luna（小）、Terra（中）和 Sol（大）。该模型可通过 OpenAI API 访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">Arc-agi-3</a></li>
<li><a href="https://arxiv.org/abs/2603.24621">ARC-AGI-3: A New Challenge for Frontier Agentic Intelligence</a></li>
<li><a href="https://arcprize.org/leaderboard">ARC-AGI-3 Leaderboard - ARC Prize</a></li>

</ul>
</details>

**社区讨论**: 社区成员注意到开发者指南中的有趣语义提示，并分享了自己的测试。一位用户报告称，GPT-5.6 Terra 在玩具 RTS 游戏上的表现与 GPT-5.5 相似，落后于 Sonnet 5。另一位用户指出，OpenAI 在比较中排除了 Fable 5，因为它拒绝回答高级生物学问题，这被视为“默认获胜”的情况。

**标签**: `#AI`, `#GPT`, `#OpenAI`, `#Large Language Models`, `#Machine Learning`

---

<a id="item-2"></a>
## [Bun 从 Zig 重写为 Rust](https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/#atom-everything) ⭐️ 9.0/10

Bun 的创建者 Jarred Sumner 使用 AI 编码代理将整个 JavaScript 运行时从 Zig 重写为 Rust，新版本现已用于驱动 Claude Code。 这次重写挑战了长期以来“大型代码库不应重写”的观点，表明 AI 辅助移植是可行且成本有效的，同时通过利用 Rust 的所有权模型显著提升了内存安全性。 重写耗费了大约 165,000 美元的 API 令牌，消耗了 59 亿未缓存输入令牌和 6.9 亿输出令牌。包含超过一百万个断言的 TypeScript 测试套件充当一致性测试套件，用于验证移植。

rss · Simon Willison · 7月8日 23:57

**背景**: Bun 是一个快速的 JavaScript 运行时，类似于 Node.js 或 Deno，最初用 Zig 编写，Zig 是一种需要手动内存管理的系统编程语言。相比之下，Rust 通过其所有权系统在编译时强制内存安全。这一重写得益于 AI 编码代理的进步，它们可以在人类监督下自主移植大型代码库。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>
<li><a href="https://simonwillison.net/guides/agentic-engineering-patterns/what-is-agentic-engineering/">What is agentic engineering? - Agentic Engineering Patterns - Simon Willison's Weblog</a></li>
<li><a href="https://asdlc.io/patterns/adversarial-code-review/">Adversarial Code Review | ASDLC.io</a></li>

</ul>
</details>

**标签**: `#Bun`, `#Rust`, `#Zig`, `#JavaScript runtime`, `#software engineering`

---

<a id="item-3"></a>
## [TypeScript 7.0 正式发布：Go 重写带来最高 12 倍速度提升](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 9.0/10

微软发布了用 Go 语言重写的 TypeScript 7.0 原生版本，完整构建速度提升 8 到 12 倍，并支持共享内存多线程。用户可通过 npm 安装，编辑器也能通过 LSP 使用新的语言服务器。 这一重大版本更新通过大幅缩短构建时间，显著提升了开发效率，并为 TypeScript 生态未来的性能增强铺平了道路。但 Vue、Svelte 等嵌入式语言的工具链尚未兼容，可能会暂时导致生态分裂。 TypeScript 7.0 引入了 --checkers 和 --builders 参数以自定义并行度，并提供了兼容包以便与 TypeScript 6 共存。Go 重写针对的是编译器和语言服务器，而非语言运行时，因此 TypeScript 代码的执行速度保持不变。

telegram · zaihuapd · 7月9日 04:01

**背景**: TypeScript 是 JavaScript 的超集，增加了静态类型，其编译器（tsc）长期以来由 TypeScript 自身编写，随着项目规模增长导致性能瓶颈。Go 重写通过利用 Go 的原生编译和并发能力，实现了 8-12 倍的构建速度提升。语言服务器协议（LSP）允许编辑器提供自动补全和错误检查等语言功能，TypeScript 7.0 的新 LSP 支持确保了广泛的编辑器兼容性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.totaltypescript.com/typescript-announces-go-rewrite">TypeScript Announces Go Rewrite, Achieves 10x Speedup | Total TypeScript</a></li>
<li><a href="https://en.wikipedia.org/wiki/Language_Server_Protocol">Language Server Protocol</a></li>

</ul>
</details>

**标签**: `#TypeScript`, `#性能优化`, `#微软`, `#Go`

---

<a id="item-4"></a>
## [欧盟议会批准聊天控制 1.0，争议不断](https://www.patrick-breyer.de/en/eu-parliament-greenlights-chat-control-1-0-breyer-our-children-lose-out/) ⭐️ 8.0/10

2025 年 7 月 9 日，欧洲议会批准了一项对 ePrivacy 指令的临时减损，允许美国科技公司自愿扫描私人消息以查找儿童性虐待材料，直到 2028 年，尽管投票的欧洲议会议员多数反对。 这一决定实际上使针对数百万用户私人通信的大规模监视合法化，涉及 Instagram、Gmail 和 Skype 等平台，为欧盟的数字隐私和加密设立了令人担忧的先例。 该措施得以通过，是因为拒绝动议需要所有 705 名议员的绝对多数（361 票），而不仅仅是出席议员的多数。只有 276 票赞成，314 票反对，17 票弃权，但 113 人缺席，导致拒绝动议未达到门槛。

hackernews · rapnie · 7月9日 11:03 · [社区讨论](https://news.ycombinator.com/item?id=48843923)

**背景**: 所谓的'聊天控制 1.0'是早期自愿扫描措施的临时延长，基于客户端扫描技术，该技术在加密前在设备上分析消息内容。这延续了欧盟 2022 年提出的更广泛的'聊天控制'提案，旨在打击在线儿童性虐待材料，但引发了重大的隐私和加密辩论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.internetsociety.org/resources/doc/2020/fact-sheet-client-side-scanning/">Fact Sheet: Client-Side Scanning - Internet Society</a></li>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control">Chat Control - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者对程序操作表示愤怒，指出投票安排在暑假前夕，且拒绝需要绝对多数。许多人批评其为'为了孩子'的措辞，并警告极权主义暗示，还有人指出欧盟被用来洗白国内不受欢迎的法律。

**标签**: `#surveillance`, `#privacy`, `#EU legislation`, `#encryption`, `#civil liberties`

---

<a id="item-5"></a>
## [腾讯 Hy3 小型 AI 模型对标 DeepSeek V4 Flash](https://hy.tencent.com/research/hy3) ⭐️ 8.0/10

腾讯发布了 Hy3，这是一个 295B 参数的混合专家模型，具有 21B 激活参数，其性能可与 DeepSeek V4 Flash 媲美，在某些基准测试中甚至超越 V4 Pro。 Hy3 展示了高能力 AI 模型可以以相对较低的计算成本运行，可能使先进 AI 更易于本地部署，并降低推理成本。 Hy3 共有 295B 参数，但每个 token 仅激活 21B，外加 3.8B MTP 层；它支持智能体任务，并已集成到腾讯的 Marvis OS 助手和微信/WeChat 场景中。

hackernews · andai · 7月9日 15:27 · [社区讨论](https://news.ycombinator.com/item?id=48847552)

**背景**: 混合专家（MoE）模型将网络划分为专门的‘专家’，每个输入仅激活其中一部分，从而在保持高效率的同时实现大参数量。激活参数决定了每个 token 的计算成本。Hy3 的激活参数（21B）介于 DeepSeek V4 Flash（13B 激活）和 V4 Pro（49B 激活）之间，提供了能力与效率的平衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Tencent-Hunyuan/Hy3">GitHub - Tencent-Hunyuan/Hy3: Hy3 (295B A21B), a leading ...</a></li>
<li><a href="https://www.tencent.com/en-us/articles/2202386.html">Tencent Hunyuan Officially Releases Hy3, Advancing Agent ...</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/DeepSeek-V4-Flash · Hugging Face</a></li>

</ul>
</details>

**社区讨论**: 社区成员对 Hy3 在较小激活参数下展现的能力感到好奇，有人指出它在基准测试中可与更大模型匹敌。然而，定价的混乱以及 OpenRouter 上截至 7 月 21 日的免费层级引发了讨论。一些人质疑 Hy3 相比 DeepSeek V4 Flash 是否具备足够的优势值得采用，尤其是在本地部署方面。

**标签**: `#AI model`, `#LLM`, `#performance`, `#Tencent`, `#comparison`

---

<a id="item-6"></a>
## [2026 年 12 月不会增加闰秒](https://datacenter.iers.org/data/latestVersion/bulletinC.txt) ⭐️ 8.0/10

国际地球自转与参考系统服务（IERS）宣布，2026 年 12 月底不会增加闰秒，当前 UTC 偏移量保持不变。 这一决定避免了可能对依赖精确计时计算机系统和网络造成的干扰，也反映了关于闰秒在全球时间标准中未来的持续讨论。 根据 IERS 公报 C，UTC 与国际原子时（TAI）的差值仍为-37 秒，UTC 与 GPS 的偏移量仍为-18 秒。

hackernews · ChrisArchitect · 7月9日 14:16 · [社区讨论](https://news.ycombinator.com/item?id=48846281)

**背景**: 闰秒偶尔会添加到协调世界时（UTC）中，使其与基于地球自转的天文时间（UT1）保持在 0.9 秒以内。由于地质活动、天气等因素导致地球自转不可预测，闰秒的插入不规则。IERS 负责监测地球自转并在需要时宣布闰秒。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Leap_second">Leap second - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/International_Earth_Rotation_and_Reference_Systems_Service">International Earth Rotation and Reference Systems Service</a></li>

</ul>
</details>

**社区讨论**: 评论者质疑地球自转的不可预测性以及对 UNIX 时间戳和维护较少的系统的影响。其他人则指出了 UTC、TAI 和 GPS 时间尺度之间的具体偏移量，显示出对计时细节的技术讨论。

**标签**: `#leap second`, `#timekeeping`, `#UTC`, `#IERS`, `#earth rotation`

---

<a id="item-7"></a>
## [Meta 发布 Muse Spark 1.1，具备自主智能体能力](https://ai.meta.com/blog/introducing-muse-spark-meta-model-api/) ⭐️ 8.0/10

Meta 发布了 Muse Spark 1.1，这是一款具备增强自主智能体能力的人工智能模型，能够自主规划并使用工具执行任务。该模型通过 API 提供，并附带新的评估报告和定价方案。 此次发布标志着 Meta 进入自主智能体 AI 的前沿竞争领域，提供了比 OpenAI 和 Anthropic 模型更便宜的替代方案，可能削弱其收入。这也重新引发了关于开源策略和评估标准的辩论。 Muse Spark 1.1 的评估报告因在 Terminal-Bench 2.1 测试中覆盖资源上限而受到批评，可能使结果无效。定价显著低廉，输入/输出每百万 token 分别为 1.25 美元/4.5 美元，缓存输入仅为 0.15 美元。

hackernews · ot · 7月9日 14:10 · [社区讨论](https://news.ycombinator.com/item?id=48846184)

**背景**: 自主智能体 AI 指能够自主规划、使用工具并适应环境以在最少监督下完成目标的系统。Muse Spark 是 Meta 首款原生多模态推理模型，支持文本、图像和语音输入，上下文窗口达 26.2 万 token。它代表了 Meta 向个人超级智能迈进的努力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai.meta.com/blog/introducing-muse-spark-msl/">Introducing Muse Spark: Scaling Towards Personal Superintelligence</a></li>
<li><a href="https://artificialanalysis.ai/models/muse-spark">Muse Spark - Intelligence, Performance & Price Analysis</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained - MIT Sloan</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一：一些人批评评估方法违反基准规则，另一些人则称赞低价和竞争性表现。讨论还涉及 Meta 通过开放权重将编码模型商品化的'搅局者'角色。

**标签**: `#Meta`, `#Muse Spark`, `#AI model`, `#open-source`, `#evaluation`

---

<a id="item-8"></a>
## [GPT-Live：OpenAI 新语音模式，可委托 GPT-5.5 处理复杂任务](https://simonwillison.net/2026/Jul/8/introducing-gptlive/#atom-everything) ⭐️ 8.0/10

OpenAI 推出了 GPT-Live，这是 ChatGPT 的新一代语音模型，能够在保持对话流畅的同时将复杂任务委托给 GPT-5.5 处理。 这一升级显著提升了语音模式的能力和响应速度，使 ChatGPT 成为更实用的实时头脑风暴和自然交互助手。 GPT-Live 会自动将需要网络搜索、深度推理或复杂工作的任务在后台委托给 GPT-5.5，并将结果无缝带回对话中。OpenAI 计划随着新前沿模型的发布持续更新底层模型。

rss · Simon Willison · 7月8日 23:20

**背景**: ChatGPT 的语音模式允许用户与 AI 进行自然对话。之前的语音模式基于较旧的 GPT-4o 模型，知识截止于 2024 年，限制了其实用性。GPT-Live 使用更新的、能力更强的语音模型，可以将繁重任务卸载到 OpenAI 最先进的模型上，从而提高响应速度和准确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-live/">Introducing GPT-Live | OpenAI</a></li>
<li><a href="https://openai.com/index/introducing-gpt-5-5/">Introducing GPT‑5.5 - OpenAI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-Live`, `#ChatGPT`, `#Voice Mode`, `#AI Models`

---

<a id="item-9"></a>
## [Meta 超级智能进展：计算扩张与强化学习初创公司](https://newsletter.semianalysis.com/p/the-future-of-meta-superintelligence) ⭐️ 8.0/10

Meta 发布了其超级智能项目的进展更新，详细描述了激进的算力增长计划以及一家新兴的强化学习环境初创公司。 这一更新凸显了 Meta 在 AI 基础设施和强化学习方面的加大投入，可能加速超级智能的进展，并重塑科技巨头之间的竞争格局。 此次算力增长计划被称为有史以来最激进的扩张，而强化学习初创公司突然出现；更新内容还包括对 Google DeepMind 的建议。

rss · Semianalysis · 7月9日 19:16

**背景**: 超级智能指的是超越人类认知能力的人工智能。算力基础设施对于训练大规模 AI 模型至关重要，而强化学习环境则为训练 RL 智能体提供模拟空间。Meta 正与其他科技巨头在高级 AI 竞赛中竞争。

**标签**: `#AI`, `#reinforcement learning`, `#compute infrastructure`, `#Meta`, `#deep learning`

---

<a id="item-10"></a>
## [IMGNet：通过符号模式匹配进行人脸验证](https://www.reddit.com/r/MachineLearning/comments/1urxvxh/i_built_imgnet_a_face_verification_model_that/) ⭐️ 8.0/10

IMGNet 提出了一种人脸验证模型，用滑动窗口符号模式匹配替代余弦相似度，在 LFW 上达到 96.27% 的准确率，模型大小仅 10.58 MB，基于 CASIA-WebFace 训练。 这项工作挑战了人脸验证中默认使用余弦相似度的做法，证明与训练目标协同设计的替代相似性度量可以在减小模型规模的同时达到竞争性能并提高稳定性。 该模型使用三个互补指标（IMG Sign Score、AMP IMG Score、Chain Score），它们共享单一阈值，并采用投票系统进行决策；当直接应用于 ArcFace 嵌入而不重新训练时，IMG Sign Score 在 LFW 上达到 99.58%。

reddit · r/MachineLearning · /u/img-_- · 7月9日 18:00

**背景**: 传统人脸验证模型使用余弦相似度比较嵌入向量，即测量向量之间的夹角。IMGNet 则通过检查嵌入向量的重叠窗口中的局部符号模式，寻找关系一致性而非绝对方向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/imghost11/imgnetV1">imghost11/imgnetV1 · Hugging Face</a></li>
<li><a href="https://github.com/imamgh11/imgnet/blob/main/README.md">imgnet/README.md at main · imamgh11/imgnet · GitHub</a></li>

</ul>
</details>

**标签**: `#face verification`, `#deep learning`, `#computer vision`, `#representation learning`

---

<a id="item-11"></a>
## [蚂蚁集团开源 LingBot-Video，全球首个 MoE 具身视频模型](https://www.qbitai.com/2026/07/446458.html) ⭐️ 8.0/10

蚂蚁集团开源了 LingBot-Video，这是全球首个基于混合专家（MoE）架构的具身视频生成基础模型。该模型总参数量为 300 亿，但每次推理仅激活约 30 亿参数，在 RBench 基准测试中以 0.620 的总分取得领先。 该开源发布大幅降低了具身视频生成的计算成本，同时保持了高质量，有望加速机器人研究和应用。采用 Apache 2.0 许可证开源，使从事机器人学习和世界模型研究的开发者能够更广泛地使用。 LingBot-Video 采用 DiT+MoE 设计以平衡容量和成本，并在覆盖灵巧操作、机器人移动和第一视角交互的 7 万小时具身数据上训练。多维强化学习奖励系统在美学和运动一致性之外，重点强调物理合理性和任务完成度。

telegram · zaihuapd · 7月9日 04:30

**背景**: 混合专家（MoE）是一种机器学习技术，每次输入仅激活部分模型参数，从而实现更大规模模型与更低推理成本。扩散 Transformer（DiT）取代了传统 U-Net 架构，在视频生成中提供更好的可扩展性。RBench 是一个面向机器人的基准测试，评估五个任务域和四种机器人形态的视频生成能力。LingBot-Video 结合 MoE 和 DiT，推理效率约为同等规模密集模型的 3 倍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://dagroup-pku.github.io/ReVidgen.github.io/">Rethinking Video Generation Model for the Embodied World</a></li>
<li><a href="https://arxiv.org/abs/2507.13343">[2507.13343] Taming Diffusion Transformer for Efficient ... Video Diffusion Transformer (DiT) Overview - emergentmind.com VideoDiT: Bridging Image Diffusion Transformers for ... [2407.21705] Tora: Trajectory-oriented Diffusion Transformer ... Diffusion Transformers Explained: Why DiT Is Replacing U-Net ... Diffusion Transformers Explained: Why DiT Is Replacing U-Net ... The Diffusion Transformer Shift: Inside the Technical Re ... Images</a></li>

</ul>
</details>

**标签**: `#embodied AI`, `#video generation`, `#MoE`, `#open-source`, `#robotics`

---

<a id="item-12"></a>
## [大疆 EV50 无人机飞越珠峰 8861 米创纪录](https://www.163.com/dy/article/L1CUCV940514R9OJ.html) ⭐️ 8.0/10

在珠峰“巅峰使命”科考中，大疆尚未发布的 EV50 垂直起降运载无人机在北坡飞越 8861 米高度，创下全球同类公开测试中的最高飞行升限纪录。 这一成就展示了商用无人机在极端高度运行的潜力，为高海拔物流、科学研究和此前无法到达区域的环境监测开启了新可能。 EV50 是一款复合翼无人机，可垂直起降，起飞后切换为固定翼巡航。在为期 12 天的任务中，共完成 32 架次起降，连续爬升 3730 米，返程时仍剩余 30%电量。

telegram · zaihuapd · 7月9日 06:00

**背景**: 复合翼无人机结合了多旋翼垂直起降的灵活性和固定翼长航时、高速的优势，适用于需要兼具灵活性和航程的任务。大气剖面数据指不同海拔高度的温度、气压、湿度等大气变量的垂直测量值，对天气预报建模和气候研究至关重要。传统气象气球方式续航短、覆盖有限，使无人机成为在复杂环境中收集此类数据的有前途替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://baike.baidu.com/item/复合翼无人机/67152229">复合翼无人机 - 百度百科</a></li>
<li><a href="https://jandan.net/p/116703">不懂物理也没关系，AI预测天 气 现在很厉害 - 煎蛋</a></li>

</ul>
</details>

**标签**: `#drone`, `#DJI`, `#high-altitude`, `#UAV`, `#technology`

---

<a id="item-13"></a>
## [国家超算互联网核心节点在郑州上线](https://36kr.com/newsflashes/3887797387344387) ⭐️ 8.0/10

2026 年 7 月 9 日，国家超算互联网核心节点在郑州正式上线，提供超过 10 万张国产 AI 算力卡组成的单一资源池。 这一里程碑极大增强了中国的国产 AI 算力能力，并在构建统一的国家计算资源调度体系方面取得了进展。它可能减少对外国 AI 芯片的依赖，并支持各行业的大规模 AI 模型训练与推理。 该核心节点是国家超算互联网平台接入的最大单体国产 AI 算力资源池。它承担运营管理、资源调度等功能，并整合了供需对接、产业孵化等综合服务。

telegram · zaihuapd · 7月9日 07:00

**背景**: 国家超算互联网是一个国家级平台，将全国的高性能计算和 AI 计算资源汇聚成统一网络进行高效调度。其目标是满足重大科技项目、重点工程以及经济社会发展的计算需求。算力资源池（或称'算力池'）利用虚拟化和软件定义技术，将分散、异构的计算资源汇聚成统一资源池，以提高利用率并降低成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="http://paper.people.com.cn/rmrb/images/2024-05/06/19/rmrb2024050619.pdf">KJZKRMRB19B20240506C</a></li>
<li><a href="https://baike.baidu.com/item/算力池化/65662046">算力池化_百度百科</a></li>

</ul>
</details>

**标签**: `#supercomputing`, `#AI computing`, `#national infrastructure`, `#China tech`

---

<a id="item-14"></a>
## [OpenAI 与美国战争部达成禁止 AI 用于国内监控的协议](https://t.me/zaihuapd/42459) ⭐️ 8.0/10

OpenAI 与美国战争部（前身为国防部）已同意修订双方的 AI 合作协议，明确禁止将该 AI 系统用于对美国公民的国内监控。此举由 OpenAI 首席执行官 Sam Altman 主动提议，旨在回应对 AI 可能用于大规模监控的担忧。 这项协议为 AI 伦理和军事合同订立了重要先例，可能为 AI 公司如何与国防机构合作建立标准。它解决了关键的公众信任问题，并可能影响全球未来的 AI 治理政策。 修订后的条款明确禁止将 AI 用于对本国公民的蓄意监控，并禁止利用商业获取的个人身份信息进行追踪或监测。该协议尚未正式签署，此前 Anthropic 与同一部门的合作协议因类似争议而中止。

telegram · zaihuapd · 7月9日 13:22

**背景**: 美国战争部是国防部更名后的称谓，旨在强调其军事角色。最初的战争部存在于 1789 年至 1947 年，之后更名为国防部。这一背景很重要，因为与 AI 公司的国防合同引发了关于将 AI 用于监控和自主武器的伦理担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cgr9r4qr0ppo">Trump rebrands Department of Defense as Department of War</a></li>
<li><a href="https://www.war.gov/">Home | U . S . Department of War</a></li>

</ul>
</details>

**标签**: `#AI ethics`, `#OpenAI`, `#government policy`, `#surveillance`, `#AI regulation`

---