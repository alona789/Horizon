---
layout: default
title: "Horizon Summary: 2026-07-18 (ZH)"
date: 2026-07-18
lang: zh
---

> 从 33 条内容中筛选出 11 条重要资讯。

---

1. [LG 显示器通过 Windows Update 静默安装软件](#item-1) ⭐️ 9.0/10
2. [特朗普政府拟设类似 FINRA 的独立机构审查顶尖 AI 模型](#item-2) ⭐️ 9.0/10
3. [GPT-5.6 用一条提示解决 30 年凸优化猜想](#item-3) ⭐️ 8.0/10
4. [Kimi K3 通过蒸馏达到前沿性能](#item-4) ⭐️ 8.0/10
5. [Fable 5 对比 GPT-5.6 Sol：/goal 指令在 NP-hard 问题上有效吗？](#item-5) ⭐️ 8.0/10
6. [TP-Link Kasa 摄像头未认证 UDP 泄露 GPS 位置 6 年](#item-6) ⭐️ 8.0/10
7. [涉嫌的低质量 AI 作品赢得 DeepMind Kaggle 2.5 万美元大奖](#item-7) ⭐️ 8.0/10
8. [豆包手机放弃 GUI 自动化，转向 MCP](#item-8) ⭐️ 8.0/10
9. [Meta 拟向 Anthropic 出租 AI 算力，潜在交易规模达 100 亿美元](#item-9) ⭐️ 8.0/10
10. [台积电宣布 A14 制程技术将于 2028 年投产](#item-10) ⭐️ 8.0/10
11. [旧金山责令苹果谷歌下架“脱衣”应用](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [LG 显示器通过 Windows Update 静默安装软件](https://videocardz.com/newz/lg-monitors-silently-install-software-through-windows-update-without-user-consent) ⭐️ 9.0/10

LG 显示器在通过 HDMI 连接时，会利用 Windows Update 的驱动更新机制，自动安装如“LG Customer Support”或“LG Update”等软件，全程无需用户同意，且无任何交互提示。 这种静默安装带来了严重的安全和隐私风险，因为该软件拥有完整的系统访问权限，没有沙盒保护，并可能成为供应链攻击的载体。所有连接 LG 显示器的 Windows 用户都受到影响。 软件在插入 LG 显示器时立即安装，即使已连接过旧款 LG 显示器也会再次安装。它随系统每次启动而运行。解决方法包括通过组策略或设备安装设置禁用设备应用的自动下载。

hackernews · baranul · 7月18日 10:21 · [社区讨论](https://news.ycombinator.com/item?id=48956688)

**背景**: Windows Update 会自动下载并安装驱动更新及关联软件，以确保设备正常运行。这一功能虽为便利而设，但可能被硬件厂商滥用，推送无关或潜在不受欢迎的软件。供应链攻击正是利用可信的分发渠道来投递恶意或不需要的软件，本次事件即为其典型案例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.microsoft.com/en-US/Windows/Hardware/Drivers/automatically-get-recommended-and-updated-hardware-drivers">Automatically get recommended and updated hardware drivers</a></li>
<li><a href="https://en.wikipedia.org/wiki/Supply_chain_attack">Supply chain attack - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者表达强烈担忧，指出微软应为此负责，因其允许在未经同意的情况下自动安装。有人提供了组策略的解决方法，并强调这可能被恶意软件利用。还有评论者讽刺道，显示器现在也成了推送垃圾软件的途径。

**标签**: `#security`, `#windows`, `#privacy`, `#supply-chain-attack`, `#lg`

---

<a id="item-2"></a>
## [特朗普政府拟设类似 FINRA 的独立机构审查顶尖 AI 模型](https://www.bloomberg.com/news/articles/2026-07-17/us-considers-creating-finra-like-watchdog-to-vet-top-ai-models) ⭐️ 9.0/10

特朗普政府正考虑设立一个类似金融业监管局（FINRA）的独立 AI 监管机构，负责审查顶尖 AI 模型的安全性，该方案由财政部长斯科特·贝森特牵头，目前正由白宫幕僚长苏茜·威尔斯审阅。 该提案可能将 AI 监管从临时性政府干预转变为结合行业自律与政府监督的结构化框架，直接影响 OpenAI、Anthropic 等顶级 AI 公司的模型发布流程，并回应华尔街和硅谷的关切。 该新机构将向美国证券交易委员会（SEC）汇报；值得注意的是，Anthropic 和 OpenAI 此前曾对政府要求修改或延迟发布最新模型提出异议。该计划与 Google DeepMind 首席执行官德米斯·哈萨比斯的建议方向一致，但总统特朗普尚未审阅，方案仍在讨论中，内容可能调整。

telegram · zaihuapd · 7月18日 05:45

**背景**: FINRA 是由美国证券交易委员会（SEC）监督的独立监管机构，旨在保护投资者并维护证券市场诚信。该提案旨在将类似模式应用于 AI 安全领域，让华尔街和硅谷在联合制定安全标准方面拥有更大发言权，而非依赖临时性政府管控。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hans/美国证券法">美国证券法 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.oanda.com/bvi-ft/lab-education/invest_us_stock/finra/">FINRA是什麼？介紹其成立宗旨與功能所在 - OANDA Lab</a></li>
<li><a href="https://lazarusalliance.com/zh-CN/什么是FINRA合规性/">什么是 FINRA 合规性？ - Lazarus Alliance, Inc.</a></li>

</ul>
</details>

**标签**: `#AI监管`, `#政策`, `#特朗普政府`, `#FINRA`, `#AI安全`

---

<a id="item-3"></a>
## [GPT-5.6 用一条提示解决 30 年凸优化猜想](https://old.reddit.com/r/math/comments/1uxj3cy/after_openais_cdc_proof_announcement_gpt56_used_a/) ⭐️ 8.0/10

OpenAI 的 GPT-5.6 模型通过使用一条提示解决了凸优化领域中一个长达 30 年的未解问题，展示了大型语言模型为数学研究做出贡献的能力。 这表明先进的 AI 能够解决长期存在的数学问题，可能加速发现，并将人类研究者的角色转向更具创造性的工作。 该问题涉及证明在球形域上的 Lipschitz 凸函数优化复杂性的上界，这是一个小众但公认的猜想。根据 Reddit 上的澄清，所用的模型是 Sol Pro 而非 Ultra。

hackernews · mbustamanter · 7月18日 13:00 · [社区讨论](https://news.ycombinator.com/item?id=48957779)

**背景**: 凸优化是数学优化的一个子领域，专注于在凸集上最小化凸函数，许多问题有多项式时间算法。然而，一些特定问题类别几十年来一直未解决。GPT-5.6 是一种大型语言模型，能够在适当提示下进行推理并生成证明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Convex_optimization">Convex optimization - Wikipedia</a></li>
<li><a href="https://whatdoesmeanings.com/general/gpt-5-6-used-a-prompt-to-close-a-30-year-gap-in-convex-optimization/">GPT-5.6 Used A Prompt To Close A 30 - Year Gap In Convex ...</a></li>
<li><a href="https://pulseaugur.com/cluster/149817-gpt-5-6-solves-30-year-convex-optimization-problem">GPT-5.6 Solves 30 - Year Convex Optimization Problem · PulseAugur</a></li>

</ul>
</details>

**社区讨论**: 社区普遍认可该结果的重要性，指出该问题比 OpenAI 的循环双覆盖证明更小众，但仍是真正的贡献。一些人讨论了这对数学研究的影响，认为它可能消除低垂的果实，但需要人类创造力来提出新颖方法。还有澄清说明使用的是 Sol Pro 而非 Ultra，引发了关于模型之间差异的好奇。

**标签**: `#AI`, `#convex optimization`, `#mathematical research`, `#LLM applications`, `#open problem`

---

<a id="item-4"></a>
## [Kimi K3 通过蒸馏达到前沿性能](https://stephen.bochinski.dev/blog/2026/07/18/the-kimi-k3-moment/) ⭐️ 8.0/10

中国实验室 Moonshot AI 发布了 Kimi K3，这是一个拥有 2.8 万亿参数的模型，通过知识蒸馏达到了前沿性能，引发了关于此类进展的必然性及其地缘政治影响的讨论。 这一事件表明，蒸馏可以使非前沿实验室快速追赶，可能加速人工智能竞赛，并促使更严格的国家安全措施出台。它挑战了前沿模型需要大量资源和原创研究的假设。 Kimi K3 采用了新颖的 Kimi Delta Attention 机制，并支持 100 万词元的上下文窗口。蒸馏涉及训练一个较小的“学生”模型来复制更大“教师”模型的输出，从而在降低成本的同时保持性能。

hackernews · sbochins · 7月18日 17:32 · [社区讨论](https://news.ycombinator.com/item?id=48960218)

**背景**: 知识蒸馏是一种模型压缩技术，小型模型通过从大型模型的预测中学习，实现高效部署。Moonshot AI 是一家以长上下文模型闻名的中国公司，Kimi K3 是其最新旗舰模型，专为软件工程和推理等前沿任务设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_(chatbot)">Kimi (chatbot) - Wikipedia</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K3 - Kimi API Platform</a></li>
<li><a href="https://www.linkedin.com/pulse/knowledge-distillation-how-large-language-models-learn-fahim-ahamed-2inie">Knowledge Distillation in AI : How Large Models Train Smaller</a></li>

</ul>
</details>

**社区讨论**: 评论者们就蒸馏是否削弱了原创研究展开了辩论，一些人认为这是不可避免的一步，就像前沿实验室蒸馏人类知识一样。其他人分享了不同的实际体验：一位用户发现 Kimi K3 比替代方案更慢且效率更低，而另一位推测地缘政治上的挫败感使得尽管存在技术缺陷仍有人支持该模型。

**标签**: `#AI`, `#Distillation`, `#Frontier Models`, `#Geopolitics`, `#Performance Comparison`

---

<a id="item-5"></a>
## [Fable 5 对比 GPT-5.6 Sol：/goal 指令在 NP-hard 问题上有效吗？](https://charlesazam.com/blog/fable-5-gpt-5-6-sol-goal/) ⭐️ 8.0/10

一篇博客文章在 NP-hard 问题上对比了 Anthropic 的 Fable 5 和 OpenAI 的 GPT-5.6 Sol，测试 /goal 指令是否能提升模型在复杂推理任务上的表现。 该评估揭示了先进大语言模型如何处理结构化问题求解，以及目标设定指令是否能增强其推理能力，这对人工智能研究和优化领域的实际应用具有重要意义。 博客指出，/goal 指令在单线程调查或小规模分散/收集中效果更好，而 Ultra 模式（具有并行调查和对抗性审查）可能更适合更广泛的搜索策略。

hackernews · couAUIA · 7月18日 11:00 · [社区讨论](https://news.ycombinator.com/item?id=48956879)

**背景**: NP-hard 问题以其难以找到最优解而闻名，大语言模型越来越多地被测试于此类任务以评估其推理能力。/goal 指令是一种提示功能，指示模型专注于特定目标，有望在需要持续注意力和战略规划的任务上提升表现。Fable 5 和 GPT-5.6 Sol 分别代表 Anthropic 和 OpenAI 最新一代的前沿 AI 模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>

</ul>
</details>

**社区讨论**: 社区成员指出，GPT 模型在优化竞赛中表现出色，暗示其具有固有优势。其他人分享经验称，Claude 模型有时会忘记长上下文指令，而 /goal 指令可能有助于缓解这一问题。一位评论者认为图表因 y 轴颠倒而令人困惑。

**标签**: `#AI`, `#LLM`, `#NP-hard`, `#benchmark`, `#problem-solving`

---

<a id="item-6"></a>
## [TP-Link Kasa 摄像头未认证 UDP 泄露 GPS 位置 6 年](https://github.com/BadChemical/IoT-Vulnerability-Research-Public/blob/main/TP-Link_Kasa_EC71/Kasa_EC71.md) ⭐️ 8.0/10

安全研究员 BadChemical 披露，TP-Link Kasa EC70 v4 和 EC71 v4 摄像头通过未认证的 UDP 数据包持续广播精确的 GPS 坐标，此漏洞已存在六年。 该漏洞使得任何本地网络攻击者无需认证即可精确定位用户位置，构成严重的隐私风险。这再次凸显了物联网设备安全设计的缺陷以及改进的必要性。 GPS 数据通过无连接、未加密的 UDP 广播传输，允许被动窃听。虽然攻击者需位于同一本地网络，但若设备被设置为 DMZ，则可能暴露在互联网上。

hackernews · BadChemical · 7月17日 21:42 · [社区讨论](https://news.ycombinator.com/item?id=48952565)

**背景**: TP-Link Kasa 摄像头是流行的智能家居安防设备。UDP（用户数据报协议）是一种轻量级网络协议，默认不提供认证或加密。许多物联网设备因硬编码密钥或不安全的通信协议而存在类似漏洞，易被本地网络攻击者利用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/tp-link-cameras-vulnerability/">Multiple TP-Link Cameras Vulnerability Allows Hackers to ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/User_Datagram_Protocol">User Datagram Protocol - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了对物联网安全的担忧，部分指出该漏洞仅限本地网络，若设备未暴露在互联网上则危害较小。也有人批评报告疑似 AI 生成，并质疑未加密数据泄露到云 IP 的广泛问题。

**标签**: `#IoT`, `#security`, `#privacy`, `#vulnerability`, `#TP-Link`

---

<a id="item-7"></a>
## [涉嫌的低质量 AI 作品赢得 DeepMind Kaggle 2.5 万美元大奖](https://www.reddit.com/r/MachineLearning/comments/1uzyf66/did_blatant_ai_slop_just_win_a_25k_usd_deepmind/) ⭐️ 8.0/10

Reddit 上的一篇帖子声称，在 Google DeepMind 赞助的 Kaggle 竞赛「衡量 AGI 进展」中，获得 2.5 万美元大奖的作品质量低下，包含毫无根据的主张和无意义的输出，并未经过适当的评审。 这场争议凸显了高知名度 AI 竞赛评审过程中的潜在缺陷，引发了对研究诚信和权威奖项公信力的担忧。 该竞赛要求参与者设计新的基于认知科学的 AI 基准；据称获胜作品使用了大语言模型（LLM）的替代视角，但最终提交的成果杂乱无章，超出要求格式十倍。

reddit · r/MachineLearning · /u/TheWerkmeister · 7月18日 15:10

**背景**: Kaggle 是谷歌旗下的数据科学竞赛平台。DeepMind 赞助的挑战赛旨在通过认知科学任务衡量 AGI 进展。评审过程依赖评审员，但发帖者声称他们未能仔细审阅获胜作品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kaggle">Kaggle - Wikipedia</a></li>
<li><a href="https://www.kaggle.com/competitions">Kaggle Competitions</a></li>
<li><a href="https://cognitiveaibenchmarking.org/">Cognitive-AI Benchmarking - CAB @ CogSci 2023</a></li>

</ul>
</details>

**标签**: `#Kaggle`, `#DeepMind`, `#AI ethics`, `#research integrity`, `#controversy`

---

<a id="item-8"></a>
## [豆包手机放弃 GUI 自动化，转向 MCP](https://www.latepost.com/news/dj_detail?id=3648) ⭐️ 8.0/10

字节跳动的豆包手机改变了策略，从 GUI 自动化（读取屏幕和模拟点击）转向要求阿里、腾讯等超级应用自行提供 MCP 服务才能接入，备货量从 3 万台提升至数十万台。 这一举动标志着行业从脆弱的 GUI 自动化转向基于 API 的协作式 AI 智能体互操作性，可能标准化移动 AI 助手与第三方应用的交互方式，并减少与应用开发者的摩擦。 豆包手机助手于 2025 年 7 月 15 日获得生成式人工智能服务备案，产品于 2024 年 12 月首次预览，但因微信和淘宝的封禁而下线相关能力。新方法与苹果和谷歌正在采用的类似 MCP 框架一致。

telegram · zaihuapd · 7月18日 00:29

**背景**: GUI 自动化涉及读取屏幕和模拟点击来操作应用，这种方法脆弱且常被应用开发者封禁。MCP（Model Context Protocol）是一种开放标准，允许 AI 助手通过官方 API 请求数据和操作，使交互更可靠、更安全。这一转变象征着 AI 助手与应用服务之间从对抗性集成转向合作式集成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/mobile-next/mobile-mcp">GitHub - mobile-next/mobile-mcp: Model Context Protocol ...</a></li>
<li><a href="https://modelcontextprotocol.io/docs/getting-started/intro">What is the Model Context Protocol (MCP)?</a></li>
<li><a href="https://www.36kr.com/p/3589329638146309">00后大模型实习生「扒光」豆包手机，千字实测揭秘-36氪</a></li>

</ul>
</details>

**标签**: `#AI assistant`, `#MCP`, `#mobile strategy`, `#Chinese tech industry`

---

<a id="item-9"></a>
## [Meta 拟向 Anthropic 出租 AI 算力，潜在交易规模达 100 亿美元](https://www.nytimes.com/2026/07/17/technology/meta-anthropic-ai-computing-power.html) ⭐️ 8.0/10

据《纽约时报》2026 年 7 月 17 日报道，Meta 正与 Anthropic 进行早期谈判，拟向其出租 AI 算力，潜在交易规模高达 100 亿美元，为期两年。 这笔交易凸显出 AI 算力的极度稀缺；对 Meta 而言，既能开辟新收入来源，也有助于缓解投资者对其数据中心巨额支出的担忧。 Anthropic 于 2026 年 6 月提出该方案，Meta 正在评估；若达成协议，Anthropic 将按月付款，双方均可提前退出。

telegram · zaihuapd · 7月18日 01:14

**背景**: 像 Anthropic 这样的 AI 公司需要巨大的算力来训练和运行大型语言模型，但专用硬件（如 GPU）供应紧张。Meta 今年计划投入高达 1450 亿美元用于 AI 和数据中心建设，向外出租闲置算力是优化利用率的策略性举措。

**标签**: `#AI computing`, `#Meta`, `#Anthropic`, `#data centers`, `#industry news`

---

<a id="item-10"></a>
## [台积电宣布 A14 制程技术将于 2028 年投产](https://t.me/zaihuapd/42643) ⭐️ 8.0/10

台积电宣布其下一代 A14（1.4 纳米级）制程技术，计划于 2028 年量产。与 N2（2 纳米级）制程相比，A14 在相同功耗下速度提升 15%，或在相同速度下功耗降低 30%，同时逻辑密度提升超过 20%。 这一宣布巩固了台积电在先进半导体制造领域的技术领先地位，对驱动未来人工智能、高性能计算和移动设备至关重要。相比 N2，A14 在性能和能效上的提升将催生更强大、更节能的芯片，影响整个电子行业。 台积电还计划在 2026 年末推出中间节点 A16 制程，采用背面供电技术。董事长魏哲家确认 A14 的产量规模将大于 2nm 制程，并且台积电正在开发新的芯片封装技术以补充 CoWoS。

telegram · zaihuapd · 7月18日 05:00

**背景**: 台积电是全球领先的半导体代工厂，为苹果、英伟达和 AMD 等公司制造芯片。N2（2 纳米级）等制程节点采用全环绕栅极（GAA）纳米片晶体管，相比之前的 FinFET 技术提供了显著的性能和能效提升。A14 代表了 N2 之后的下一步，延续了缩小晶体管、增强芯片能力的趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/tsmc-begins-quietly-volume-production-of-2nm-class-chips-first-gaa-transistor-for-tsmc-claims-up-to-15-percent-improvement-at-iso-power">TSMC begins quietly volume production of 2nm-class chips — first GAA transistor for TSMC claims up to 15% improvement at ISO power | Tom's Hardware</a></li>
<li><a href="https://xab.info/en/posts/tsmc-a14-performance-surpasses-n2">TSMC Breaks Its Own Records: New A 14 (1.4nm) Process ... - XAB.info</a></li>
<li><a href="https://www.newkerala.com/news/a/tsmc-projects-mass-production-advanced-a14-chips-2028-477.htm">TSMC A 14 Chips Mass Production by 2028</a></li>

</ul>
</details>

**标签**: `#TSMC`, `#semiconductor`, `#process technology`, `#A14`, `#hardware`

---

<a id="item-11"></a>
## [旧金山责令苹果谷歌下架“脱衣”应用](https://techcrunch.com/2026/07/17/apple-and-google-ordered-to-purge-nudify-apps-from-app-stores/) ⭐️ 8.0/10

旧金山市检察长邱信福要求苹果和谷歌从其应用商店中下架数十款 AI 驱动的“脱衣”应用，理由是这些应用生成非自愿的深度伪造图像。信件警告称，两家公司可能因允许这些应用运营而不干预，获利数百万美元。 此举为解决 AI 驱动的图像滥用和深度伪造生成问题，确立了平台责任的法律先例。它凸显了言论自由、技术创新与保护个人免受非自愿性内容侵害之间的持续斗争。 苹果表示已下架三款应用并终止相关开发者账号，谷歌则确认已暂停信件中点名的五款 Play 商店应用。科技透明项目此前已在 2026 年 1 月和 4 月多次警告这两家公司。

telegram · zaihuapd · 7月18日 08:45

**背景**: “脱衣”应用利用人工智能修改个人（通常是女性）的照片，生成逼真但未经同意的裸体图像。这些工具是更广泛的深度伪造生态系统的一部分，能够实施基于图像的性虐待，包括生成儿童性虐待材料。这种 AI 技术的日益普及引发了监管机构的关注，并要求平台制定更严格的政策。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techtransparencyproject.org/articles/apple-and-google-are-steering-users-to-nudify-apps">TTP - Apple and Google Are Steering Users to Nudify Apps</a></li>
<li><a href="https://www.wired.com/story/deepfake-nudify-technology-is-getting-darker-and-more-dangerous/">Deepfake ‘Nudify’ Technology Is Getting Darker—and More Dangerous | WIRED</a></li>

</ul>
</details>

**标签**: `#AI ethics`, `#deepfakes`, `#app store regulation`, `#privacy`, `#platform responsibility`

---