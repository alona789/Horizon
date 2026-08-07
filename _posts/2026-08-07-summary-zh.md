---
layout: default
title: "Horizon Summary: 2026-08-07 (ZH)"
date: 2026-08-07
lang: zh
---

> 从 36 条内容中筛选出 14 条重要资讯。

---

1. [DeepSeek V4 Flash 0731 发布，低成本且本地推理速度极快](#item-1) ⭐️ 8.0/10
2. [科技界的悲伤：当从业者对职业失去信心时](#item-2) ⭐️ 8.0/10
3. [甲骨文禁止 OpenJDK 接受 AI 生成代码，称版权与审查负担](#item-3) ⭐️ 8.0/10
4. [用批处理、算子融合与 SIMD 让 Postgres 分析提速 300 倍](#item-4) ⭐️ 8.0/10
5. [Cloudflare 发布 Kitesurf：基于 V8 隔离区的智能体优先浏览器](#item-5) ⭐️ 8.0/10
6. [2027 年内存产能售罄，HBM 挤压 DRAM 供应](#item-6) ⭐️ 8.0/10
7. [在 150 万页网站上与爬虫斗争的一年](#item-7) ⭐️ 8.0/10
8. [新墨西哥州法院裁定 Meta 因损害儿童心理健康赔偿 5.67 亿美元](#item-8) ⭐️ 8.0/10
9. [Codex + GPT-5.6 Sol Ultra 生成《浣熊大劫案》游戏，优于 Claude Fable 5](#item-9) ⭐️ 8.0/10
10. [SemiAnalysis：Gemini 受挫，GCP 短期受益于 AI 需求](#item-10) ⭐️ 8.0/10
11. [SEC 批准纳斯达克 23 小时交易制 12 月 6 日上线](#item-11) ⭐️ 8.0/10
12. [美国审查中国 AI 企业海外获取英伟达芯片渠道](#item-12) ⭐️ 8.0/10
13. [sub2api OAuth 高危漏洞：仅凭邮箱即可接管账户](#item-13) ⭐️ 8.0/10
14. [OpenAI 称新模型 Astra 或达「关键」网络攻击能力，扩大安全测试或致发布推迟](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek V4 Flash 0731 发布，低成本且本地推理速度极快](https://arcprize.org/results/deepseek-v4-flash-0731) ⭐️ 8.0/10

DeepSeek 于 7 月 31 日发布了 V4 Flash 0731，这是其注重效率的 V4 Flash 系列的一次更新，取代了此前的预览版。该模型兼具强劲性能、极低的 API 使用成本和快速的本地推理速度。 此次发布让接近前沿的模型质量以极低成本触手可及，开发者几乎可以忽略 token 费用，这可能加速从昂贵的专有 API 向开源权重模型的迁移。同时，其本地推理速度也为注重隐私或离线部署提供了更多实用选择。 DeepSeek V4 Flash 是一个专家混合（MoE）模型，总参数 284B，激活参数 13B，支持 100 万 token 上下文窗口。0731 标注代表 7 月 31 日发布的版本，与此前的“预览版”不同；本地用户报告在双 RTX Pro 6000 Blackwell GPU 上预填充速度约 8k token/s，单流生成速度约 250 token/s。

hackernews · tosh · 8月7日 17:56 · [社区讨论](https://news.ycombinator.com/item?id=49214008)

**背景**: DeepSeek V4 Flash 被设计为面向 100 万 token 上下文推理的效率优化模型，其规模使其既能用于 API 调用，也适合本地推理。ARC Prize 是一项非营利计划，通过基准测试和奖金来加速开源通用人工智能研究，该模型的结果现已发布在其网站上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek -ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>
<li><a href="https://ollama.com/library/deepseek-v4-flash">deepseek - v 4 - flash</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash">DeepSeek V 4 Flash - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**社区讨论**: 评论者大多热情高涨：有人表示该模型“几乎适用于所有任务”，即使同时开很多会话也“很难每天花超过 5 美元”；还有人认为 07/31 更新版“整体升了一个档次”，调试和数据分析能力出色。但也有用户反馈，与上一个 V4 Flash 版本相比，会出现无限循环和不执行工具调用的问题，浪费不少 token。

**标签**: `#AI`, `#LLM`, `#DeepSeek`, `#Model Release`, `#ARC Prize`

---

<a id="item-2"></a>
## [科技界的悲伤：当从业者对职业失去信心时](https://www.noemamag.com/why-is-everyone-in-tech-so-sad/) ⭐️ 8.0/10

《Noema》杂志发表了一篇文章，探讨为何众多科技从业者感到悲伤，审视整个行业中的职业幻灭现象。这篇文章引起广泛共鸣，在聚合网站上获得了 333 个点赞和 475 条评论。 这场讨论标志着科技行业文化上的重大转变——曾经满怀乐观的从业者如今开始怀疑自己的位置。如果整个阶层都失去信心，可能会影响创新、人才留存以及社会对科技职业的看法。 评论者引用了历史类比，例如印刷行业的衰落，并指出网络环境的毒性是一个因素。文章本身包含个人叙述和全行业分析，而非具体数据。

hackernews · RickJWagner · 8月7日 12:42 · [社区讨论](https://news.ycombinator.com/item?id=49209539)

**背景**: 科技职业长期以来被视为稳定、高地位且收入可观。然而近年来，裁员、倦怠和公众看法的变化等因素加剧了日益增长的幻灭感。这篇文章探讨了这种情绪，将个人故事与更大的行业趋势联系起来。

**社区讨论**: Animats 将科技行业的衰落与印刷行业相提并论，指出从业者最终会失去一切。marginalia\_nu 指出当代网络环境的毒性，dec0dedab0de 则表示这是他 20 年职业生涯中感觉最沮丧的一次。Havoc 认为文章语气有些沾沾自喜，但也看到讨论的社会价值。

**标签**: `#tech culture`, `#burnout`, `#software engineering`, `#career`, `#mental health`

---

<a id="item-3"></a>
## [甲骨文禁止 OpenJDK 接受 AI 生成代码，称版权与审查负担](https://app.dealroom.co/news/feed/oracle-bans-ai-generated-code-from-openjdk-despite-ellison-s-claim-oracle-isn-t-writing-its-own-code) ⭐️ 8.0/10

甲骨文发布了一项临时政策，禁止 OpenJDK 贡献中包含 AI 生成的代码，相关公告见 openjdk.org/legal/ai。该政策为临时措施，最终版本正由甲骨文法务团队起草。 这一决定可能为大型开源项目如何处理 AI 参与编写的代码开创先例，尤其在 AI 生成代码法律地位尚不明朗的背景下。同时，这也凸显了甲骨文一方面大力投资 AI、另一方面又作为 Java 开源实现管理者的角色矛盾。 临时政策指出，AI 生成的代码可能带来版权不确定性，并给“本已有限的人类审查者时间”增加过重负担。根据 OpenJDK 页面，最终政策将由甲骨文法务团队制定。

hackernews · delduca · 8月7日 17:36 · [社区讨论](https://news.ycombinator.com/item?id=49213754)

**背景**: OpenJDK 是 Java 平台标准版（Java SE）的自由开源实现，源自 Sun Microsystems 于 2006 年发起的一项计划。甲骨文于 2010 年收购 Sun，此后一直负责管理 OpenJDK；该开源项目是 Oracle JDK 和 Red Hat 构建版等多个生产级 Java 发行版的基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenJDK">OpenJDK - Wikipedia</a></li>
<li><a href="https://www.azul.com/blog/what-is-openjdk/">What is OpenJDK &amp; What is it Used For? | Azul</a></li>
<li><a href="https://www.redhat.com/en/topics/application-modernization/openjdk-vs-oracle-jdk">OpenJDK versus Oracle JDK</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了原始来源链接，总体上认为这一举措务实，但也有多人指出其中的讽刺之处。有人分析称，甲骨文法务部门意在保留就 AI 生成专有代码起诉他人的余地；还有人调侃称，甲骨文的发布说明可能已经被 AI 写了一年。

**标签**: `#Oracle`, `#OpenJDK`, `#AI-generated code`, `#Open Source Policy`, `#Java`

---

<a id="item-4"></a>
## [用批处理、算子融合与 SIMD 让 Postgres 分析提速 300 倍](https://malisper.me/how-we-made-postgres-hundreds-of-times-faster-the-query-engine/) ⭐️ 8.0/10

pgrust 的作者详细介绍了如何通过批处理、算子融合和 SIMD 让 Postgres 的分析查询提速数百倍，同时利用形式化验证和差分模糊测试来保证正确性。 如果这些性能声明属实，Postgres 将能处理目前需要专用列存储或向量化数据库才能胜任的分析工作负载。这种方法也展示了数据驱动的查询编译如何应用于像 Postgres 这样成熟的数据库系统。 该项目名为 pgrust，作者称已证明 1000 多个面向用户的函数与 Postgres 行为完全一致。仅算子融合这一项通常就能带来 1.7 到 2.5 倍的性能提升，因此报道的 300 倍加速很可能是多种技术组合的结果。

hackernews · poly2it · 8月7日 11:00 · [社区讨论](https://news.ycombinator.com/item?id=49208535)

**背景**: PostgreSQL 是一个通用关系型数据库，历来以 OLTP 工作负载见长，其逐行执行模型可能会拖累分析查询。算子融合将多个查询算子合并到一个循环中，以减少单行处理的开销；SIMD（单指令多数据）则让 CPU 用一条指令同时处理多个数据元素。差分模糊测试将相同输入分别送给两个实现并比较输出，无需手工编写预期结果即可发现不一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Differential_testing">Differential testing - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Single_instruction,_multiple_data">Single instruction, multiple data - Wikipedia</a></li>
<li><a href="https://db.cs.cmu.edu/papers/2017/p1-menon.pdf">Relaxed Operator Fusion for In-Memory Databases:</a></li>

</ul>
</details>

**社区讨论**: 评论者怀疑用户是否会放弃 Postgres 改用 pgrust，认为关键不在于原始性能，而在于对核心团队的信任和项目的长期延续性。有人称赞自适应规划是期待已久的功能，有望在学术/小众场景之外证明其可行性；也有人希望看到关于 IO 调度器和线程调度器更详细的架构介绍。

**标签**: `#postgres`, `#database`, `#performance`, `#SIMD`, `#query-engine`

---

<a id="item-5"></a>
## [Cloudflare 发布 Kitesurf：基于 V8 隔离区的智能体优先浏览器](https://blog.cloudflare.com/kitesurf/) ⭐️ 8.0/10

Cloudflare 宣布推出 Kitesurf，这是一款完全运行在 Cloudflare Workers 的 V8 隔离区中的智能体优先浏览器。它基于开源 Blitz 引擎构建，旨在为 Cloudflare 全球网络上的浏览器自动化和 AI 智能体提供服务。 此举意义重大，因为它将完整的浏览器运行时带到了 Cloudflare 的边缘平台，使 AI 智能体能够以低延迟和高可扩展性执行网页自动化、抓取和测试。同时，这也引发了人们对 Cloudflare 双重角色的质疑——它既是提供反机器人保护的 CDN，又是智能体驱动浏览的平台。 Kitesurf 是无状态的、高度可扩展且成本效益高，完全运行在 Workers 上。它基于 Blitz 构建，这是 DioxusLabs 用 Rust 编写的一个开源模块化 Web 引擎，目前处于 alpha 阶段，尚未准备好用于生产环境。

hackernews · m3h · 8月7日 10:42 · [社区讨论](https://news.ycombinator.com/item?id=49208393)

**背景**: V8 隔离区是用于运行 JavaScript 的隔离执行环境，Cloudflare Workers 利用它们以高密度和高安全性运行无服务器函数。Blitz 是一个激进模块化的 Web 引擎，提供 HTML/CSS 渲染，并可嵌入或与其他组件组合。智能体优先浏览器旨在让 AI 智能体以编程方式与网页交互，无需人工干预即可执行操作和提取数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/kitesurf/">Introducing Kitesurf : The agent - first browser that... | Cloudflare Blog</a></li>
<li><a href="https://github.com/DioxusLabs/blitz">GitHub - DioxusLabs/blitz: A radically modular HTML/CSS rendering engine · GitHub</a></li>
<li><a href="https://medium.com/@adityashete009/v8-isolates-for-serverless-functions-a-game-changer-0e8355cf7ac9">V8 isolates for Serverless Functions? A game changer | by Aditya Shete | Medium</a></li>

</ul>
</details>

**社区讨论**: 社区评论中，nicoburns 指出 Kitesurf 基于他开发了 2.5 年的 Blitz 构建，并提到 Cloudflare 打算将补丁开源并上游合并。minraws 对 Cloudflare 同时作为 CDN 和智能体平台的双重角色表示担忧，而 QuantumNomad\_ 则询问 Cloudflare 的反机器人系统是否会阻止其自身的浏览器实例。cautiouscat 质疑浏览器智能体的实际用例，ako 则开玩笑说风筝冲浪已经过时了。

**标签**: `#browser`, `#cloudflare`, `#web-automation`, `#v8`, `#browser-engine`

---

<a id="item-6"></a>
## [2027 年内存产能售罄，HBM 挤压 DRAM 供应](https://www.ign.com/articles/ramageddon-continues-another-year-as-2027-memory-capacity-is-reportedly-sold-out) ⭐️ 8.0/10

报道称，2027 年的内存产能已被全部预订售罄，原因是高带宽内存（HBM）制造消耗了过多的半导体晶圆产能。这导致 DDR5 等传统内存类型可用的产能减少。 这预示着 AI 硬件和消费级 PC 都将面临长期的内存短缺和价格上涨。同时，也凸显了 AI 对 HBM 的需求正在根本性地改变内存行业的生产优先次序。 根据行业分析，在相同的技术节点下，生产同样数量的比特，HBM3E 消耗的晶圆供应量大约是 DDR5 的三倍。由于最终采用 3D 封装工艺，HBM die 的尺寸也必须大于普通 DRAM die。

hackernews · inigyou · 8月7日 07:58 · [社区讨论](https://news.ycombinator.com/item?id=49207236)

**背景**: 高带宽内存（HBM）是由三星、AMD 和 SK 海力士共同开发的 3D 堆叠 DRAM 接口，专为 AI 加速器等高性能计算场景设计。晶圆产能指的是晶圆厂能加工的硅晶圆数量；由于 HBM 通过垂直堆叠多个 die、且每比特占用的晶圆面积更大，因此扩大 HBM 产量会限制行业对 DDR5 等非 HBM 内存的产能增长。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://www.techtimes.com/articles/317859/20260606/sk-hynix-dram-capacity-roadmap-revealed-yongin-alone-adds-360k-wafers-monthly.htm">SK hynix DRAM Capacity Roadmap Revealed: Yongin Alone Adds...</a></li>

</ul>
</details>

**社区讨论**: 评论者大多聚焦于 HBM 与 DDR5 之间的权衡，有人指出，一单位 HBM 产能消耗的晶圆量大约相当于原本可生产三单位 DDR5 的晶圆量。还有人抱怨内存价格上涨以及 AI 驱动的内存需求，甚至有人建议业界需要类似 USB 的通用内存标准来重新利用旧内存条。

**标签**: `#memory`, `#HBM`, `#semiconductors`, `#supply-chain`, `#AI-hardware`

---

<a id="item-7"></a>
## [在 150 万页网站上与爬虫斗争的一年](https://patronview.com/news/99-percent-of-my-website-traffic-is-bots/) ⭐️ 8.0/10

一个拥有 150 万页面的网站作者详细描述了一年多来与机器人流量的斗争，并透露某个月份的托管费用比通常每月 90 美元的账单暴涨了约 500%。这篇文章还承认该网站本身就抓取公开文档，使这一抱怨显得具有讽刺意味。 这一事件凸显了 AI 爬虫和抓取工具对独立网站发布者造成的财务和运营负担。它还引发了更广泛的问题：依赖 Cloudflare 等中心化服务来决定谁能访问网站是否合适，以及使用工作量证明挑战等替代方案是否更可持续。 成本飙升与 Cloudflare 的 D1 数据库有关，而不仅仅是带宽。评论区建议放弃 D1 改用静态站点，并指出 Anubis 这种工作量证明挑战可以有效识别真实浏览器软件，适合未放在 CDN 后面的网站。一位评论者测得 Claude-searchbot 在 72 小时内抓取了约 20.5 万个页面，却只带来了 1 次引荐流量。

hackernews · petercooper · 8月7日 14:51 · [社区讨论](https://news.ycombinator.com/item?id=49211386)

**背景**: 爬虫和机器人是自动程序，有时用于索引、价格监控或 AI 训练数据，但它们会带来巨大流量和成本。机器人缓解措施包括静态请求分析、行为指纹识别以及 Akamai 等厂商在边缘提供的基于 AI 的检测。Cloudflare 的 Bot Fight Mode 是常用的免费选项，但它也可能拦截合法的 AI 爬虫，并引发对集中控制的担忧。住宅代理允许抓取者绕过基于 IP 的封锁，使这场军备竞赛对网站所有者来说更加困难。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.imperva.com/learn/application-security/what-are-bots/">What are Bots | Bot Types &amp; Mitigation Techniques | Imperva</a></li>
<li><a href="https://community.cloudflare.com/t/community-tip-bot-fight-mode/117572">Community Tip - Bot Fight Mode - Tutorial - Cloudflare Community</a></li>
<li><a href="https://brightdata.com/">Bright Data - All in One Platform for Proxies and Web Scraping</a></li>

</ul>
</details>

**社区讨论**: 评论既包含担忧也包含实用建议。一些人担心将机器人决策外包给 Cloudflare 会损害开放互联网，另一些人则推荐 Anubis 等替代方案或改用静态托管。还有人抱怨 AI 爬虫免费获取内容而未给予补偿，同时也有评论承认许多网站（包括本网站）本身也是抓取者。

**标签**: `#web scraping`, `#bot mitigation`, `#cloudflare`, `#devops`, `#cost optimization`

---

<a id="item-8"></a>
## [新墨西哥州法院裁定 Meta 因损害儿童心理健康赔偿 5.67 亿美元](https://www.theguardian.com/technology/2026/aug/06/new-mexico-court-meta) ⭐️ 8.0/10

新墨西哥州一家法院裁定 Meta 败诉，责令其支付 5.67 亿美元（部分媒体报道总额为 9.42 亿美元），原因是其社交媒体平台损害儿童心理健康。判决认定 Meta 违反了该州公共妨害法，并要求其针对未成年用户作出整改。 这是针对大型社交媒体公司的最高额州级裁决之一，也是对利用公共妨害法监管在线平台的一次重大考验。它可能会鼓励其他司法管辖区就儿童安全和心理健康问题对科技公司提起类似诉讼。 不同报道给出的金额不同：路透社和《卫报》称 5.67 亿美元专门用于青少年心理健康基金，而《华尔街日报》报道为 9.42 亿美元，可能包含额外费用或救济措施。该命令还要求 Meta 对未成年用户作出整改。评论者指出裁决引用了新墨西哥州公共妨害法（NMSA 1978 § 30-8-1）。

hackernews · boplicity · 8月7日 00:06 · [社区讨论](https://news.ycombinator.com/item?id=49204352)

**背景**: 公共妨害法传统上针对危害公众健康、安全、道德或福利，或妨碍公共权利的活动。将其用于起诉社交媒体公司是一种新颖的法律策略；此前的案例主要针对污染或危险房产等物理妨害。这项裁决可能为追究平台对未成年人算法驱动伤害的责任开创先例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Public_nuisance">Public nuisance - Wikipedia</a></li>
<li><a href="https://www.lawandjusticewiki.org/wiki/Public_nuisance">Public nuisance - Justice Definitions Project</a></li>

</ul>
</details>

**社区讨论**: 评论者反应不一：有人认为罚款对 Meta 的收入来说只是“挠痒痒”，也有人指出对于新墨西哥州这样的小州，9.42 亿美元按比例已非常巨大。有评论者指出裁决引用了具体的公共妨害法条，还有人称 Instagram Reels 和 TikTok 是“在线版海洛因”，因其令人上瘾的设计。一个普遍担忧是，这笔罚款可能仍被科技公司视为“经营成本”。

**标签**: `#Meta`, `#legal`, `#mental-health`, `#regulation`, `#social-media`

---

<a id="item-9"></a>
## [Codex + GPT-5.6 Sol Ultra 生成《浣熊大劫案》游戏，优于 Claude Fable 5](https://simonwillison.net/2026/Aug/7/moonlight-mayhem/#atom-everything) ⭐️ 8.0/10

Simon Willison 在 Codex Desktop 上使用 GPT-5.6 Sol Ultra 运行完全相同的“浣熊大劫案”提示词，生成了名为《月光与混乱》（Moonlight &amp; Mayhem）的更优秀游戏。该游戏包含博物馆抢劫情节，浣熊队友叠罗汉盗取金色沙丁鱼，不同于 Claude Fable 5 生成的简单后院收集金币版本。 这次直接对比显示，使用 Codex 子代理的 GPT-5.6 Sol Ultra 在一次性游戏生成上胜过 Claude Fable 5，标志着智能体编程的快速进步。AI/ML 开发者在为长周期、多步骤创意任务选择模型时，可将其作为实用基准。 Codex 在该项目上花费了 52 分钟，并使用 gpt-image-2 生成纹理；按完整 API 价格计算，该会话成本约为 23.28 美元。一次性提示的初始输出存在一个 bug：浣熊的眼睛变成了巨大的球体，尽管 Codex 在开发过程中查看了截图却未能发现；Simon 通过提问“为什么浣熊身上有巨大的黑色球体？”然后说“修复它”才解决。

rss · Simon Willison · 8月7日 19:18

**背景**: GPT-5.6 Sol 是 OpenAI 最新的编程模型；Sol Ultra 是最大推理模式，会大量使用子代理，在编程基准上创下新的最高纪录。Codex 是 OpenAI 的智能体编程工具，可生成具有独立指令和工具上下文的子代理并行工作。Claude Fable 5 是 Anthropic 于 2026 年 6 月发布的最强大的通用模型。Simon 此前曾让 Claude Fable 5 基于四年前由 GPT-3 和 DALL-E 生成的创意构建了一个可运行的游戏，这成为本次对比的基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/gpt-5-6/">GPT - 5 . 6 : Frontier intelligence that scales with your ambition | OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>

</ul>
</details>

**标签**: `#AI`, `#Codex`, `#GPT`, `#Claude`, `#game-generation`

---

<a id="item-10"></a>
## [SemiAnalysis：Gemini 受挫，GCP 短期受益于 AI 需求](https://newsletter.semianalysis.com/p/gemini-is-cooked-but-gcp-is-cooking) ⭐️ 8.0/10

SemiAnalysis 发表分析称，谷歌的 Gemini AI 模型在长期战略上正陷入困境，但谷歌云平台（GCP）短期内却因这场 AI 竞赛带来的基础设施需求而受益。文章将此描述为 DeepMind 的长期失败成为 GCP 的短期利好。 这一观点凸显了 Alphabet 内部的分歧：DeepMind 在 Gemini 上的困境与 GCP 的商业势头形成鲜明对比。这很重要，因为它影响谷歌与微软/OpenAI、亚马逊等云与 AI 竞争对手的竞争格局，并可能重塑投资者对 Alphabet AI 战略的看法。 该分析来自 SemiAnalysis，一家专注于 AI、半导体和云基础设施的知名独立研究机构。文章的核心观点是，即使 Gemini 在模型质量竞赛中落败，训练和推理所需的巨大算力需求仍会流向 GCP，为后者带来短期收入顺风。

rss · Semianalysis · 8月7日 02:32

**背景**: Google DeepMind 是 Alphabet 旗下的 AI 研究实验室，由 DeepMind 与 Google Brain 于 2023 年合并而成，负责开发 Gemini 系列大语言模型。谷歌云平台（GCP）是 Alphabet 的云计算部门，与 AWS 和 Microsoft Azure 竞争。SemiAnalysis 是一家订阅制分析机构，以关于 AI 硬件和云经济的深度技术报告著称，常被行业讨论引用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepMind">DeepMind</a></li>
<li><a href="https://x.com/SemiAnalysis_">SemiAnalysis (@SemiAnalysis_) on X</a></li>

</ul>
</details>

**标签**: `#Google`, `#AI`, `#cloud computing`, `#Gemini`, `#GCP`

---

<a id="item-11"></a>
## [SEC 批准纳斯达克 23 小时交易制 12 月 6 日上线](https://finance.sina.com.cn/stock/bxjj/2026-08-07/doc-inimnkup0012339.shtml) ⭐️ 8.0/10

美国证券交易委员会（SEC）已批准纳斯达克的 23 小时交易制度（23/5），将于 2026 年 12 月 6 日正式上线。每天仅在美东时间 20:00 至 21:00 休市一小时，用于清算和数据处理。 这标志着美国主要交易所向近乎全天候股票交易迈出重要监管一步，对市场基础设施、算法交易系统和全球投资者都将产生深远影响。此举可能加速其他交易所跟进，并改变市场参与者的交易方式与时间段。 每日一小时的休市（美东时间 20:00–21:00）用于清算和数据处理。此前 NYSE Arca 已获 SEC 加速批准实行 22 小时交易，Cboe 也提交了接近 24×5 的提案，均瞄准 2026 年 12 月上线。

telegram · zaihuapd · 8月7日 10:03

**背景**: 美国交易所传统交易时段为美东时间上午 9:30 至下午 4:00，外加有限的盘前和盘后时段。近年来，隔夜交易通过另类交易系统（ATS）不断增长，例如 2021 年推出的 Blue Ocean ATS，让散户可以在亚洲交易时段买卖美股。SEC 计划于 9 月 17 日举行圆桌会议，讨论与近乎 24 小时市场相关的投资者保护问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.fastcompany.com/91293088/nasdaq-stock-market-trading-24-hour-new-schedule-challenging?ref=upstract.com">Nasdaq 24/ 5 trading ? New stock market hours could... - Fast Company</a></li>
<li><a href="https://www.blueocean-tech.io/blue-ocean-ats/">Blue Ocean ATS – Blue Ocean Technologies LLC</a></li>
<li><a href="https://www.investor.gov/introduction-investing/investing-basics/glossary/alternative-trading-systems-atss">Alternative Trading Systems (ATSs) | Investor.gov</a></li>

</ul>
</details>

**标签**: `#finance`, `#trading`, `#SEC`, `#Nasdaq`, `#market infrastructure`

---

<a id="item-12"></a>
## [美国审查中国 AI 企业海外获取英伟达芯片渠道](https://www.bloomberg.com/news/articles/2026-08-07/us-reviews-china-s-offshore-access-to-nvidia-chips-after-ai-breakthroughs) ⭐️ 8.0/10

美国商务部工业与安全局（BIS）已启动系统性审查，调查中国 AI 企业如何在海外获取和使用英伟达芯片，包括通过远程云计算访问的方式。此前月之暗面发布 Kimi K3 模型后，一名白宫高官指控其非法获取英伟达芯片并经泰国远程访问。 此次审查可能重塑 AI 算力供应链和出口管制体系，并可能赋予 BIS 对云计算协议的新监管权力。这对 AI 行业、国际关系以及全球云服务提供商都将产生重大影响。 审查内容包括整理两份国家名单：涉嫌将受限芯片走私入境中国的黑市所在地，以及中国企业远程租用芯片的国家。美国众议院已通过两党法案，拟明确授予 BIS 执法权力，但预计会遭到英伟达等科技公司反对。

telegram · zaihuapd · 8月7日 11:18

**背景**: 自 2022 年 10 月起，美国对向中国出口先进英伟达芯片实施许可限制，以延缓中国军事和监控 AI 能力的发展。远程访问云端芯片本身并不违法，这形成了 BIS 正在调查的法律灰色地带。据报道，阿里巴巴通过开曼实体控制的新加坡壳公司，经正被美方调查的 Megaspeed 使用位于马来西亚的英伟达芯片。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bis.gov/">Homepage | Bureau of Industry and Security</a></li>
<li><a href="https://thepulsegazette.com/article/china-ai-chip-smuggling-indictments">DOJ Indicts 12 for Smuggling AI Chips to China - The Pulse Gazette</a></li>

</ul>
</details>

**标签**: `#AI`, `#Nvidia`, `#Export Controls`, `#Geopolitics`, `#Semiconductors`

---

<a id="item-13"></a>
## [sub2api OAuth 高危漏洞：仅凭邮箱即可接管账户](https://github.com/Wei-Shaw/sub2api/issues/5350) ⭐️ 8.0/10

sub2api v0.1.171 及之前版本被披露存在一个 CVSS 8.8 的严重 OAuth 账户接管漏洞（CVE-2026-27812）。攻击者只需知道受害者的注册邮箱，无需密码、验证码或任何用户交互，即可将自有 OAuth 身份绑定到受害者账户。 该漏洞可完全控制受害者的 API 密钥、账单余额和订阅配额，影响所有使用 sub2api（一个聚合 AI API 能力的工具）的用户。由于利用门槛极低且悄无声息，所有部署方都必须立即升级或采取缓解措施。 漏洞源于 pending session 流程中的 existingUser 分支，在绑定 OAuth 身份时不校验密码和验证码。攻击者将目标用户 ID 设为受害者后完成一次 OAuth 绑定，此后每次 OAuth 登录都会解析为受害者账户。

telegram · zaihuapd · 8月7日 14:59

**背景**: OAuth 2.0 是一种广泛使用的认证标准，允许用户通过 Google、GitHub 等第三方服务登录。当应用为已有账户绑定 OAuth 时，必须确认当前用户确实是该账户的持有者；否则，攻击者就能通过接管 pending session 交换过程来劫持账户。这种“账户绑定”类型漏洞是 OAuth 已知的隐患，PortSwigger 的 Web 安全学院等安全培训中也有覆盖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://linux.do/t/topic/2721334">sub2api 曝 OAuth ... - LINUX DO</a></li>
<li><a href="https://www.sentinelone.com/vulnerability-database/cve-2026-27812/">CVE-2026-27812: Sub2API Auth Bypass Vulnerability</a></li>
<li><a href="https://portswigger.net/web-security/oauth">OAuth 2.0 authentication vulnerabilities | Web Security Academy</a></li>

</ul>
</details>

**标签**: `#security`, `#oauth`, `#vulnerability`, `#account-takeover`, `#sub2api`

---

<a id="item-14"></a>
## [OpenAI 称新模型 Astra 或达「关键」网络攻击能力，扩大安全测试或致发布推迟](https://openai.com/index/responding-next-frontier-critical-cyber-capabilities/) ⭐️ 8.0/10

OpenAI 于 2026 年 8 月 7 日披露，内部评估显示其即将推出的模型 Astra 在代理编码与网络安全方面进展显著，公司无法排除该模型达到「关键」网络能力阈值的可能性——这是此前 GPT-5.6-Sol 等模型未达到的水平。为此，OpenAI 已暂停不符合强化安全要求的相关活动，并扩大安全测试，Astra 的发布可能因此推迟。 这一消息意义重大，因为「关键」能力意味着 Astra 可能无需人工干预即可自主发现并利用加固系统中的零日漏洞，或仅凭高层目标策划并执行新型端到端网络攻击。这一决定可能为前沿 AI 实验室如何处理接近阈值模型、以及如何在发布节奏与灾难性风险之间权衡开创先例。 OpenAI 已暂停不符合强化安全要求的 Astra 相关内部活动，并正在实施隔离测试环境、增强加密和通用监控等措施。公司还将与政府机构和 AI 安全组织合作开展第三方测试。

telegram · zaihuapd · 8月7日 16:44

**背景**: OpenAI 的《预备框架》（Preparedness Framework）按风险等级对前沿模型进行分类，其中「关键」级别对应自主发现并利用零日漏洞等能力。Astra 据称是 OpenAI 的下一代主要模型系列，其名称于 2026 年 8 月 1 日确认，该模型已在解决开放数学问题方面展现出显著成果。框架中的风险阈值决定了模型是否需要特殊防护或推迟部署。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf">Preparedness Framework</a></li>
<li><a href="https://mykreatool.com/en/news/openai-astra-ii-agenty-reshenie-zadach">OpenAI Astra Model Solves 10 Open Math Problems — MyKreaTool</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI safety`, `#cybersecurity`, `#Astra`, `#model evaluation`

---