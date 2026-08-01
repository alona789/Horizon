---
layout: default
title: "Horizon Summary: 2026-08-01 (ZH)"
date: 2026-08-01
lang: zh
---

> 从 38 条内容中筛选出 9 条重要资讯。

---

1. [OpenAI Astra 在十项长期未解数学难题上取得突破](#item-1) ⭐️ 9.0/10
2. [谷歌关闭 Google Reader 如何加速 RSS 衰落](#item-2) ⭐️ 8.0/10
3. [NetBSD 11.0 发布，带来增强的 NPF 防火墙和快速启动的 MicroVM 内核](#item-3) ⭐️ 8.0/10
4. [加拿大签署联合国网络犯罪公约，批评者警告其或为监控条约](#item-4) ⭐️ 8.0/10
5. [DeepSeek V4 Flash 0731 发布：304B 参数模型以极具竞争力的价格强化智能体能力](#item-5) ⭐️ 8.0/10
6. [围棋网络内部到底有多对称？](#item-6) ⭐️ 8.0/10
7. [VLM 基准奖励空洞放射报告，抹去罕见临床术语](#item-7) ⭐️ 8.0/10
8. [三大唱片公司提议将 AI 歌曲挡在榜单之外](#item-8) ⭐️ 8.0/10
9. [微软 CEO 确认今年推出 Copilot‘超级应用’](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Astra 在十项长期未解数学难题上取得突破](https://openai.com/index/ten-advances-in-mathematics/) ⭐️ 9.0/10

OpenAI 宣布其下一代模型 Astra 的内部版本在十个长期悬而未决的数学与理论计算机科学问题上取得了新结果，相关证明已在 Lean 证明助手中形式化。这些问题至少十年未有重大进展，研究过程由人类与模型协作完成。 这标志着 AI 作为数学研究协作者的一个重要里程碑，可能加速解决几十年来人类难以攻克的难题。同时，它也引发了关于成果归属、验证方式以及人类数学家未来角色的重要讨论。 OpenAI 表示，按 GPT-5.6 Sol 的 token 价格计算，每个问题的论证生成成本不到 2000 美元。这些结果尚未经过同行评审；团队在 openai/ten-proofs 仓库发布了 Lean 4 形式化证明，并提供了论文和由 LLM 生成的推理回顾 PDF。

telegram · zaihuapd · 8月1日 07:59

**背景**: 这十个问题包括非索菲克群的存在性、Connes 刚性猜想反例、高维球体堆积、算术电路下界、量子并行重复、最近向量问题的困难性以及多色 Ramsey 数等。索菲克群是指可以用有限置换近似刻画的一类无限群；自 Gromov 引入这一概念以来，非索菲克群是否存在一直是几何群论的核心开放问题。Lean 是一种交互式证明助手，能够机械化验证数学证明，从而提升结果的可靠性和可复现性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mathoverflow.net/questions/513821/existence-of-non-sofic-groups">gr.group theory - Existence of non sofic groups - MathOverflow</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_%28proof_assistant%29">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://vibemathed.com/problem/non-sofic-groups-exist">Existence of Non-Sofic Groups - VibeMathed</a></li>

</ul>
</details>

**社区讨论**: 数学界在线上反应复杂，既有惊叹也有存在性焦虑；有人将这一时刻比作‘深蓝’事件，也有人像 Kirwin Hampshire 在《数学的暗夜》中那样描述‘深刻的精神危机’。在 MathOverflow 上，一位刚入学的博士生提到 OpenAI 关于非索菲克群的宣称结果，并表示对此类开放问题很感兴趣。

**标签**: `#AI research`, `#mathematics`, `#OpenAI`, `#formal verification`, `#breakthrough`

---

<a id="item-2"></a>
## [谷歌关闭 Google Reader 如何加速 RSS 衰落](https://openrss.org/blog/how-google-helped-destroy-adoption-of-rss-feeds) ⭐️ 8.0/10

文章认为，谷歌——尤其是 2013 年关闭 Google Reader——是 RSS 采用率下降的关键因素。该文在 Hacker News 上引发了关于谷歌责任与开放网络命运的激烈讨论。 RSS 是一种去中心化的开放标准，让用户能够自主控制新闻阅读；它的衰落助长了集中式平台和算法推荐的统治地位。理解这段历史对于有关互联网去中心化、平台权力和内容分发的讨论具有重要意义。 谷歌于 2005 年推出 Google Reader，并于 2013 年 7 月 1 日以使用量下降为由将其关闭——许多用户认为这一理由站不住脚，因为当时谷歌正在力推 Google+。Mozilla 也在 Firefox 64 中移除了 Live Bookmarks 和 RSS 订阅支持，进一步削弱了浏览器原生的 RSS 功能。

hackernews · pudgywalsh · 8月1日 18:07 · [社区讨论](https://news.ycombinator.com/item?id=49136821)

**背景**: RSS（简易信息聚合）是一种标准化的网络订阅格式，允许用户订阅网站更新并在单个聚合器（如新闻阅读器）中阅读。Google Reader 于 2005 年推出，曾是最受欢迎的 RSS 聚合器之一，并成为许多其他应用的基础平台。它在 2013 年 7 月 1 日被关闭，使数百万用户失去了通向 RSS 的主流入口，加速了向社交媒体和集中式新闻分发的转变。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/RSS">RSS</a></li>
<li><a href="https://en.wikipedia.org/wiki/Google_Reader">Google Reader</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了对 2000 年代早期互联网的怀念，并对谷歌“使用量下降”的借口感到愤怒，指出当时谷歌正在力推 Google+。有人指出 Mozilla 移除 Live Bookmarks 是另一次打击，还有人推荐 NetNewsWire 等替代方案，而不是依赖谷歌的产品。

**标签**: `#RSS`, `#Google`, `#Web History`, `#Internet`, `#Decentralization`

---

<a id="item-3"></a>
## [NetBSD 11.0 发布，带来增强的 NPF 防火墙和快速启动的 MicroVM 内核](https://blog.netbsd.org/tnf/entry/netbsd_11_0_released) ⭐️ 8.0/10

NetBSD 11.0 已正式发布，带来了多项重大更新，包括 NPF 防火墙中的二层过滤和用户/组过滤、面向 x86 的 MICROVM 内核（约 10 ms 启动），以及广泛的硬件支持改进。 此版本为 NetBSD 作为通用开源操作系统的地位增添了砝码：新增的现代防火墙功能与超快速启动的 microVM 内核，使其在云、虚拟化和嵌入式场景中相比 Linux 和其他 BSD 更具吸引力。 NPF 防火墙现在支持二层过滤以及按用户和组进行过滤；新的 MICROVM 内核启动时间约为 10 ms，整个虚拟机仅约 10 MB。此外，该版本还包含大量硬件和驱动程序改进。

hackernews · jaypatelani · 8月1日 17:56 · [社区讨论](https://news.ycombinator.com/item?id=49136736)

**背景**: NetBSD 是一个免费开源、类 Unix 的操作系统，以支持广泛的硬件架构而著称。NPF 是 NetBSD 采用 BSD 许可证的状态化包过滤防火墙，相当于 Linux 的 iptables 或 FreeBSD 的 pf。MICROVM 内核是为快速启动虚拟机而设计的轻量级内核，smolBSD 等项目展示了这一概念。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ostechnix.com/build-10mb-netbsd-vms-boot-10ms-smolbsd/">Build 10MB NetBSD VMs That Boot in 10ms Using... - OSTechNix</a></li>
<li><a href="https://www.wikiwand.com/EN/NPF_%28firewall%29">NPF ( firewall ) - Wikiwand</a></li>

</ul>
</details>

**社区讨论**: Hacker News 评论者质疑 BSD 与 Linux 当前的对比状况，并询问 NetBSD 上运行 Wine 以支持 Windows 软件的可能性。一些人赞赏 NPF 二层过滤和 10 ms microVM 启动的价值，另一些人则注意到发布公告对遗留问题的语气似乎近乎道歉。

**标签**: `#NetBSD`, `#BSD`, `#operating-system`, `#release`, `#firewall`

---

<a id="item-4"></a>
## [加拿大签署联合国网络犯罪公约，批评者警告其或为监控条约](https://www.michaelgeist.ca/2026/07/a-surveillance-treaty-in-disguise-the-trouble-with-canadas-quiet-decision-to-sign-the-un-cybercrime-convention/) ⭐️ 8.0/10

加拿大于 2026 年 5 月悄悄签署了《联合国打击网络犯罪公约》，批评者称此举实为一项伪装成反网络犯罪的监控条约。签署使加拿大成为 76 个签署国之一，但目前尚未批准。 如果该条约获得批准，可能会扩大跨境获取电子证据的范围，并影响加拿大人的数字隐私权。这也表明加拿大加入了一项遭到人权组织批评、可能被滥用于监控的公约。 该公约由俄罗斯提出，并于 2024 年 12 月由联合国大会通过。澳大利亚、欧盟、英国等多个西方国家也已签署，但在正式批准之前，条约的影响仍然有限。

hackernews · iamnothere · 8月1日 14:19 · [社区讨论](https://news.ycombinator.com/item?id=49134694)

**背景**: 《联合国打击网络犯罪公约》又称“河内公约”，是首个关于网络犯罪的全球性全面条约。它旨在加强严重犯罪电子证据共享方面的国际合作，但人权组织忧虑其可能导致监控和隐私侵犯。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/United_Nations_Convention_against_Cybercrime">United Nations Convention against Cybercrime - Wikipedia</a></li>
<li><a href="https://www.unodc.org/unodc/en/cybercrime/convention/home.html">United Nations Convention against Cybercrime</a></li>
<li><a href="https://www.unodc.org/unodc/en/cybercrime/convention/text/convention-full-text.html">UN Cybercrime Convention - Full Text</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，签署并不等于批准，澳大利亚、欧盟、英国等国家也签署了该公约。有人称赞 Michael Geist 在隐私调查方面的工作，也有人指出加拿大通常会签署大多数联合国文书，还有评论者就国际政治中固有的信号博弈发表了看法。

**标签**: `#privacy`, `#surveillance`, `#cybercrime`, `#digital-rights`, `#policy`

---

<a id="item-5"></a>
## [DeepSeek V4 Flash 0731 发布：304B 参数模型以极具竞争力的价格强化智能体能力](https://simonwillison.net/2026/Jul/31/deepseek-v4-flash-0731/#atom-everything) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek-V4-Flash-0731，这是一个拥有 3040 亿参数（Hugging Face 上约 167GB）且智能体能力大幅增强的模型。其定价为每百万输入 token 0.14 美元、每百万输出 token 0.27 美元，Artificial Analysis 将其排在更大的 4280 亿参数模型 MiniMax M3 之前。 该模型似乎是目前市场上性价比最高的选择，在 Artificial Analysis 的智能指数与单任务成本对比图中胜过价格高得多的竞争对手。这进一步印证了高性价比开源权重模型正给高价前沿模型带来压力的行业趋势。 Simon Willison 的测试显示，输出质量在很大程度上取决于推理强度设置：默认级别下他的鹈鹕插图测试结果不佳，而通过 OpenRouter 将 reasoning\_effort 设为 high 后输出质量明显改善。该模型在 Hugging Face 上以 deepseek-ai/DeepSeek-V4-Flash-0731 发布。

rss · Simon Willison · 7月31日 23:59

**背景**: “智能体能力”指 AI 模型自主进行推理、规划、行动和交互以完成复杂多步任务的能力，而不仅仅是生成一次性回答。Artificial Analysis 智能指数是一个模型级别的综合评分，它聚合了包括推理和知识测试在内的多项基准来衡量整体智能水平。DeepSeek 是一家以激进定价发布强大开源权重模型而闻名的中国 AI 实验室，V4 Flash 是其 V4 系列的最新成员。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2503.23037">[2503.23037] Agentic Large Language Models, a survey</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained | MIT Sloan</a></li>
<li><a href="https://artificialanalysis.ai/models">Comparison of AI Models across Intelligence , Performance, and Price</a></li>

</ul>
</details>

**标签**: `#deepseek`, `#llm`, `#model-release`, `#ai`, `#cost-effective`

---

<a id="item-6"></a>
## [围棋网络内部到底有多对称？](https://www.reddit.com/r/MachineLearning/comments/1vcrki2/how_symmetric_are_the_insides_of_a_go_network_r/) ⭐️ 8.0/10

开源围棋引擎 KataGo 的作者发布了一项新的机器学习可解释性研究，分析该神经网络在仅使用随机 8 折数据增强训练的情况下，其内部表征在多大程度上对棋盘旋转和镜像保持对称。文章提到，其中一项发现出乎意料。 理解神经网络能否自动发现对称性，有助于改进在已知不变性领域中的架构设计和数据增强策略。这也为超人级游戏 AI 模型的可解释性研究做出了贡献。 这项研究面向非机器学习读者编写，相关代码已从同一代码库中提供链接。文章的写作大多借助 AI 完成，但在过程中有详细的人工指导和反馈。

reddit · r/MachineLearning · /u/icosaplex · 8月1日 16:18

**背景**: 围棋是一种规则在旋转和镜像下对称的棋类游戏：任何棋局经过 8 种对称变换后，其评估结果应该是等价的。KataGo 是一款主要通过自对弈训练的开源强围棋引擎，但它的神经网络架构并没有强制这种对称性，而是依赖训练过程中随机的 8 折数据增强。这项研究考察的是，网络是自动发展出与方向无关的概念，还是为每种旋转/镜像分别记忆不同的表征。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://katagotraining.org/">KataGo Distributed Training</a></li>

</ul>
</details>

**标签**: `#ML interpretability`, `#Go`, `#neural networks`, `#symmetry`, `#KataGo`

---

<a id="item-7"></a>
## [VLM 基准奖励空洞放射报告，抹去罕见临床术语](https://www.reddit.com/r/MachineLearning/comments/1vcipzz/vlms_can_score_well_on_benchmarks_while_silently/) ⭐️ 8.0/10

Parikh 等人的新论文表明，标准评估指标会奖励重复、缺乏临床内容的模板，并悄悄抹去罕见但有临床意义的术语，这些问题出现在胸部 X 光报告生成的视觉语言模型中。作者提出了一个框架来量化临床术语的擦除和偏置术语的引入。 由于这些有缺陷的指标被用于验证医疗 AI，基准测试中得分高的模型可能会生成临床上无用甚至误导性的报告。这项工作揭示了高风险放射学 AI 中一个隐藏的失败模式，并可能改变医学报告生成模型的评估方式。 作者观察到，被描述为“正常”或写成重复模板的报告在基准指标下能获得高分，而有临床意义的罕见词汇却被擦除。他们进一步假设，这种语义擦除源于推理策略为降低生成风险而系统性地抑制临床术语。

reddit · r/MachineLearning · /u/ade17\_in · 8月1日 09:27

**背景**: 视觉语言模型（VLM）越来越多地被用于从胸部 X 光片生成放射学报告。BLEU 和 ROUGE 等标准评估指标基于与参考文本的 n-gram 重叠，因此倾向于奖励重复、保守的语言，并可能忽略关键临床发现是否被提及。这篇论文指出了“术语擦除”问题并提出了量化框架，补充了像 RaTEScore 这样的临床感知指标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2603.01625">Measuring What VLMs Don&#x27;t Say: Validation Metrics Hide Clinical ...</a></li>
<li><a href="https://aclanthology.org/2024.emnlp-main.836/">RaTEScore: A Metric for Radiology Report Generation - ACL ...</a></li>
<li><a href="https://www.emergentmind.com/topics/weighted-association-erasure-wae">Weighted Association Erasure in Clinical NLP</a></li>

</ul>
</details>

**标签**: `#Vision-Language Models`, `#Medical AI`, `#Evaluation Metrics`, `#Radiology`, `#Bias`

---

<a id="item-8"></a>
## [三大唱片公司提议将 AI 歌曲挡在榜单之外](https://www.theverge.com/ai-artificial-intelligence/973741/ai-music-major-record-labels-charts) ⭐️ 8.0/10

环球音乐、索尼音乐和华纳音乐联合提议，AI 生成的歌曲必须「实质由人创作」才有资格进入官方音乐榜单。该提案已获得 IFPI 的支持，但目前尚无榜单机构立即采纳。 这标志着音乐产业对待 AI 生成内容的政策发生了重大转变，从简单标注走向正式的准入规则。如果被采纳，它可能为整个创意产业中 AI 监管和版权执行开创先例。 该提案比 RIAA 和 IFPI 早前提出的 AI 音乐标注方案更进一步，还要求所用 AI 服务获得合法授权、模型训练数据拥有版权，且不得存在刷量或操纵榜单的行为。「实质由人创作」等关键术语目前定义模糊，索尼音乐和环球音乐均未回应置评请求。

telegram · zaihuapd · 8月1日 02:53

**背景**: 像 Billboard Hot 100 或英国官方榜单这样的音乐榜单，决定着一首作品的商业成功和行业认可。国际唱片业联合会（IFPI）代表全球录制音乐产业，美国唱片业协会（RIAA）则是美国的行业组织，两者此前都曾提出为 AI 生成音乐标注的方案。新提案将讨论重点从透明度转向了人类创作身份的定义和内容准入资格。

**标签**: `#AI music`, `#copyright`, `#music industry`, `#regulation`, `#charts`

---

<a id="item-9"></a>
## [微软 CEO 确认今年推出 Copilot‘超级应用’](https://www.theverge.com/tech/972927/microsoft-copilot-super-app-confirmed) ⭐️ 8.0/10

微软 CEO 萨蒂亚·纳德拉在季度财报电话会议上确认，公司将于今年推出一款 Copilot“超级应用”，将聊天、编程和智能体（agentic）能力整合在一起，同时覆盖消费者和商用场景。他表示，本季度将把这些体验（包括代码功能）合并进一个超级应用。 这表明微软正致力于将 AI 产品统一为单一入口，可能重塑开发者和企业使用 AI 编程与自动化工具的方式。这也加剧了与 OpenAI 的竞争，后者近期推出了整合 ChatGPT 与 Codex 的 ChatGPT Work 应用。 该超级应用预计将整合 Copilot 聊天机器人、GitHub Copilot、Copilot Cowork 和 Autopilot 系统。微软上季度营收增至 900 亿美元，主要由 AI 与云业务推动，但具体产品细节仍较为笼统。

telegram · zaihuapd · 8月1日 13:18

**背景**: Copilot 是微软嵌入 Windows、Microsoft 365 和开发工具中的 AI 助手，而 GitHub Copilot 专门辅助编程。智能体 AI（Agentic AI）指的是能够自主设定目标并采取行动的系统。Copilot Cowork 可以自动执行发送邮件、安排会议、创建文档等任务；Autopilot 则是常驻后台、无需反复提示即可自主行动的智能体。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/agentic-ai">What is Agentic AI? | IBM</a></li>
<li><a href="https://www.microsoft.com/en-us/microsoft-365-copilot/cowork">Copilot Cowork: Automate Tasks and Workflows | Microsoft</a></li>
<li><a href="https://www.microsoft.com/en-us/microsoft-365/blog/2026/06/02/introducing-microsoft-scout-your-always-on-personal-agent/">Introducing Microsoft Scout: Your always-on personal agent | Microsoft 365 Blog</a></li>

</ul>
</details>

**标签**: `#Microsoft`, `#Copilot`, `#AI`, `#Agentic`, `#Super App`

---