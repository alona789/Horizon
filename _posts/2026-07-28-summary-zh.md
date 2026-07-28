---
layout: default
title: "Horizon Summary: 2026-07-28 (ZH)"
date: 2026-07-28
lang: zh
---

> 从 29 条内容中筛选出 12 条重要资讯。

---

1. [月之暗面发布 Kimi-K3 权重及修改版许可](#item-1) ⭐️ 9.0/10
2. [谷歌 CEO 透露 Gemini 4：迄今最雄心预训练，年底发布](#item-2) ⭐️ 9.0/10
3. [Fastjson2 远程代码执行漏洞未修复](#item-3) ⭐️ 9.0/10
4. [vLLM v0.26.0 发布：支持 Inkling 模型、DeepSeek-V4 优化、灵活注意力后端](#item-4) ⭐️ 8.0/10
5. [Anthropic 明确其对开放权重模型的立场](#item-5) ⭐️ 8.0/10
6. [法官驳回谷歌用数字千年版权法抗辩爬取行为](#item-6) ⭐️ 8.0/10
7. [论坛项目用 HTMX 替换 React.js](#item-7) ⭐️ 8.0/10
8. [《Paged Out \#9》：致黑客文化的一封情书](#item-8) ⭐️ 8.0/10
9. [Libsm64 将《超级马力欧 64》转化为可复用的游戏引擎库](#item-9) ⭐️ 8.0/10
10. [长鑫科技科创板首日暴涨 471%](#item-10) ⭐️ 8.0/10
11. [阿里推出千问办公 AI 办公平台，支持电脑操控](#item-11) ⭐️ 8.0/10
12. [中国启动国产 DUV 光刻机量产](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [月之暗面发布 Kimi-K3 权重及修改版许可](https://simonwillison.net/2026/Jul/27/kimi-k3/#atom-everything) ⭐️ 9.0/10

月之暗面于 2026 年 7 月 27 日在 Hugging Face 上发布了其 2.8 万亿参数的 Kimi-K3 模型权重，新许可要求大型模型即服务提供商另行签订协议。 Kimi-K3 是有史以来最大的开放权重模型之一，但其对大企业的限制性商业许可可能为 AI 公司平衡开放性与商业利益树立先例。 K3 许可去掉了&\#x27;修改版 MIT&\#x27;的标签，并增加条款要求任何 12 个月内从模型即服务获得超过 2000 万美元总收入的实体签订单独协议。模型权重在 Hugging Face 上大小为 1.56 TB，支持高达 100 万 token 的上下文。

rss · Simon Willison · 7月27日 23:39

**背景**: 月之暗面是一家中国 AI 公司，开发了 Kimi 系列大语言模型。其之前的模型 Kimi K2 使用修改版 MIT 许可，要求月活超过 1 亿或月收入超过 2000 万美元的实体进行署名。Kimi-K3 许可对大商业用户收紧了这些限制。开放权重模型允许任何人下载和运行，但许可规定了允许的使用方式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/moonshotai/Kimi-K3/blob/main/LICENSE">LICENSE · moonshotai/ Kimi - K 3 at main</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>

</ul>
</details>

**标签**: `#AI`, `#Open Source`, `#Large Language Model`, `#Hugging Face`

---

<a id="item-2"></a>
## [谷歌 CEO 透露 Gemini 4：迄今最雄心预训练，年底发布](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 9.0/10

Sundar Pichai 在 Alphabet 2026 年第二季度财报电话会议上宣布，下一代大语言模型 Gemini 4 已进入预训练阶段，称其为公司迄今最具雄心的预训练项目。该模型预计于 2026 年底发布。 这表明谷歌持续大力投资前沿 AI，预训练更大的基础模型对于在快速发展的 LLM 领域保持竞争力至关重要。Gemini 4 的发布可能在推理、代码生成和多模态理解等领域推动能力边界。 Pichai 强调，谷歌将优先将算力分配给前沿 AGI 研发，以确保 Gemini 4 在发布时仍处行业前沿。此外，Gemini 3.x Flash 系列将保持几乎每月一次的迭代频率，重点提升智能编码能力。

telegram · zaihuapd · 7月27日 04:06

**背景**: 预训练是大语言模型初始阶段，通过从海量文本语料中学习预测下一个 token，得到一个基础模型，后续需要针对特定任务进行微调。Google 的 Gemini 系列包含多种变体，每一代都旨在提升性能和安全性。该公司一直在快速迭代，Gemini 3.x Flash 模型已几乎每月发布一次。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gist.github.com/ritwikraha/77e79990992043f60a9588610b2781c5">Pretraining of Large Language Models · GitHub</a></li>
<li><a href="https://ai.google.dev/gemini-api/docs/models">Models - Gemini API | Google AI for Developers</a></li>

</ul>
</details>

**标签**: `#AI`, `#Google Gemini`, `#Large Language Model`, `#Pre-training`, `#AGI`

---

<a id="item-3"></a>
## [Fastjson2 远程代码执行漏洞未修复](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 9.0/10

7 月 27 日，长亭科技披露 Fastjson2 存在远程代码执行漏洞，影响 2.0.62 及以前所有版本，攻击者可绕过 AutoType 类型校验执行恶意代码。目前尚无正式补丁。 该漏洞非常严重，因为 Fastjson2 被广泛用于 Java 应用的 JSON 处理。由于没有补丁，许多系统面临远程代码执行风险，可能导致受影响服务器被完全控制。 项目维护者已确认该安全问题，但 PR \#7695 中的修复方案被关闭且未合入主分支。建议用户在补丁发布前彻底禁用 AutoType 作为临时措施。

telegram · zaihuapd · 7月27日 10:31

**背景**: Fastjson2 是阿里巴巴开发的高性能 Java JSON 库，常用于序列化和反序列化。AutoType 功能可在反序列化时自动解析类型，若验证不严则可能被利用执行任意代码。此前 Fastjson1 中的类似漏洞也要求禁用 AutoType 作为缓解措施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://alibaba.github.io/fastjson2/">FASTJSON 2 is a Java JSON library with excellent performance.</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#RCE`, `#fastjson`, `#Java`

---

<a id="item-4"></a>
## [vLLM v0.26.0 发布：支持 Inkling 模型、DeepSeek-V4 优化、灵活注意力后端](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 引入了对 Inkling 模型系列的支持、DeepSeek-V4 的显著性能优化（端到端提升高达 2.94%）、fp32 lm\_head 改进，以及每个 KV 缓存组可选择的灵活注意力后端。 此版本巩固了 vLLM 作为多种 LLM 架构领先推理引擎的地位，提供新模型支持和显著的性能提升，使运行 DeepSeek-V4 等模型的大规模部署的用户受益。 此版本包含来自 212 位贡献者的 411 次提交，值得注意的新增功能包括 Inkling 的分段 CUDA 图支持、DeepSeek-V4 的专用路由内核，以及通过 head\_dtype 为生成模型提供的可选 fp32 lm\_head。KV 卸载和分层存储也已显著成熟。

github · khluu · 7月27日 01:06

**背景**: vLLM 是一个开源的高吞吐量 LLM 推理引擎。Inkling 模型系列由 Thinking Machines Lab 以 Apache 2.0 许可证发布，是一个通用的多模态模型。DeepSeek-V4 是 DeepSeek 的一个流行大型语言模型，vLLM 的优化旨在提升其推理性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/model-card/inkling/">Inkling Model Card - Thinking Machines Lab</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/mtp/">MTP (Multi-Token Prediction) - vLLM</a></li>
<li><a href="https://nvidia.github.io/TensorRT-LLM/features/quantization.html">Quantization — TensorRT LLM</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#vLLM`, `#performance optimization`, `#DeepSeek`, `#GPU`

---

<a id="item-5"></a>
## [Anthropic 明确其对开放权重模型的立场](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 8.0/10

Anthropic 发布了一份政策声明，澄清其不主张禁止开放权重模型，但支持对所有足够强大的模型（无论是开放还是封闭的）进行强制性安全测试。 这一立场可能影响关于 AI 安全与开放性的监管辩论，可能影响开放权重模型的开发和分发方式。它也突显了促进创新与防止滥用之间的紧张关系。 该提案涉及强制性安全测试，但未明确由谁执行测试或标准如何，导致批评者认为如果成本或限制过高，可能实际上等同于禁止开放权重模型。

hackernews · surprisetalk · 7月27日 22:03 · [社区讨论](https://news.ycombinator.com/item?id=49076057)

**背景**: 开放权重模型是核心组件（例如训练后的权重）公开发布的 AI 模型，允许任何人下载、检查和修改。Anthropic 是一家领先的 AI 安全公司，开发 Claude 模型系列，其政策立场在 AI 社区具有影响力。关于开放权重模型的争论集中在平衡可及性与安全性上，一些人认为它们促进创新，另一些人则警告潜在滥用风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://www.microsoft.com/en-us/corporate-responsibility/topics/open-weight/">Open Weights and American AI Leadership</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了怀疑，许多人认为该提议是变相禁止开放权重模型以保护 Anthropic 的商业利益。一些人指出 Anthropic CEO Dario Amodei 先前关于禁令的言论存在矛盾，其他人则注意到涉及对华芯片出口的地缘政治影响。

**标签**: `#AI safety`, `#open-weights`, `#Anthropic`, `#AI regulation`, `#policy`

---

<a id="item-6"></a>
## [法官驳回谷歌用数字千年版权法抗辩爬取行为](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 8.0/10

一位联邦法官裁定，谷歌不能援引《数字千年版权法》的安全港条款来阻止第三方抓取其搜索引擎结果页面（SERPs）。 这一裁决树立了重要的法律先例，可能限制企业利用版权法限制网络爬取，尤其是在其已弃用官方 API 的情况下。 法院认为谷歌搜索结果属于事实性数据，缺乏版权保护所需的独创性，因此数字千年版权法不适用。

hackernews · cdrnsf · 7月27日 18:15 · [社区讨论](https://news.ycombinator.com/item?id=49073513)

**背景**: 数字千年版权法的安全港条款保护在线服务提供商免于因其用户的版权侵权行为而承担责任，但并不保护公司自身的网站内容不被爬取。网络爬取是指从网站自动提取数据的行为，通常在官方 API 不可用时被采用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DMCA_safe_harbor">DMCA safe harbor</a></li>
<li><a href="https://www.eff.org/issues/dmca">DMCA | Electronic Frontier Foundation</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，谷歌本是建立在爬取网络的基础上，如今却试图阻止他人抓取其搜索结果，这颇具讽刺意味。许多人指出，谷歌弃用搜索 API 后，爬取成了唯一替代方案，并批评该诉讼是欺压小公司之举。

**标签**: `#law`, `#web scraping`, `#Google`, `#DMCA`, `#copyright`

---

<a id="item-7"></a>
## [论坛项目用 HTMX 替换 React.js](https://misago-project.org/t/removing-reactjs-from-the-codebase-and-adapting-htmx-for-ui-interactivity/1267/) ⭐️ 8.0/10

Misago 论坛项目从代码库中移除了 React.js，改用 HTMX 实现 UI 交互，获得了更简洁的代码和更好的性能。 这个案例展示了从重型客户端框架转向超媒体驱动方法的实际迁移，可降低复杂度并改善论坛等内容密集型网站的加载速度。 HTMX 通过 server-rendered HTML 片段（使用 hx-get、hx-post 等属性）实现动态 UI 更新，无需编写 JavaScript。据报道，这次迁移简化了代码库并提升了感知性能。

hackernews · Ralfp · 7月27日 09:58 · [社区讨论](https://news.ycombinator.com/item?id=49067301)

**背景**: HTMX 是一个开源 JavaScript 库，通过自定义属性扩展 HTML，允许开发者直接在 HTML 中执行 AJAX、WebSocket 和 Server-Sent Events。它遵循超媒体驱动的方法，与 React 基于组件的虚拟 DOM 模型形成对比。这一替换反映了某些开发者认为服务器渲染方法对特定应用更简单、更快速的趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Htmx">Htmx</a></li>
<li><a href="https://htmx.org/">htmx - high power tools for html</a></li>

</ul>
</details>

**社区讨论**: 社区评论呈现了不同的经验：一些用户发现 HTMX 在复杂过滤界面中因 HTML 负载过大而变慢，而其他人则称赞它适合论坛软件，并推荐与 TailwindCSS 搭配使用。许多人同意 HTMX 适合内容驱动的网站，一位用户建议在需要高度交互的部分使用迷你 Vue 或 React 组件。

**标签**: `#HTMX`, `#React`, `#web development`, `#server-side rendering`, `#frontend architecture`

---

<a id="item-8"></a>
## [《Paged Out \#9》：致黑客文化的一封情书](https://pagedout.institute/download/PagedOut_009.pdf) ⭐️ 8.0/10

《Paged Out》第 9 期以 PDF 形式免费发布，包含关于亚像素渲染、可计算拼贴等深度技术文章。 该杂志复兴了 Phrack 和 2600 等经典黑客杂志的精神，以精美设计为小众技术内容提供平台，激发好奇心和深度学习。 本期包含题为《C 语言婴儿步》的幽默文章，以及一项未注明出处的再发现：王浩在 20 世纪 60 年代关于可计算拼贴的工作，将拼贴问题与停机问题联系起来。

hackernews · laurensr · 7月27日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=49070138)

**背景**: 《Paged Out》是一本免费的、由社区驱动的技术杂志，专注于底层编程、黑客和计算机科学主题。它旨在兼具美学愉悦和智力启发，吸引那些热衷于深入探索冷门或基础主题的读者。

**社区讨论**: Hacker News 上的读者称赞该杂志的技术深度和设计，将其与 Phrack 和 2600 等经典杂志相提并论。一位评论者指出，关于可计算拼贴的文章未注明出处地重新发现了王浩的工作，引发了人们对拼贴问题与停机问题之间联系的兴趣。

**标签**: `#hacking`, `#programming`, `#computer science`, `#zine`, `#technical articles`

---

<a id="item-9"></a>
## [Libsm64 将《超级马力欧 64》转化为可复用的游戏引擎库](https://github.com/libsm64/libsm64) ⭐️ 8.0/10

开源项目 libsm64 将《超级马力欧 64》反编译为一个 C++ 库，提供马力欧的移动和渲染代码，使开发者能将马力欧嵌入任何外部游戏引擎。 该项目实现了创意跨界，例如马力欧出现在《半条命 2》中，并展示了无需依赖元宇宙等概念，即可将经典游戏资产重新用于现代引擎。 Libsm64 基于 n64decomp 的完整 SM64 反编译项目构建；用户需自行提供 ROM 用于资源提取。有一个 awesome-list 仓库用于追踪基于 libsm64 的项目。

hackernews · klaussilveira · 7月27日 10:04 · [社区讨论](https://news.ycombinator.com/item?id=49067352)

**背景**: 《超级马力欧 64》最初于 1996 年在 Nintendo 64 上发布。n64decomp 项目将游戏的二进制文件完全反编译为源代码，使得像 libsm64 这样的项目能够提取并重新封装其功能，作为独立库集成到自定义游戏引擎中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/libsm64/libsm64">GitHub - libsm 64 / libsm 64 : Mario 64 as a library for use in external...</a></li>
<li><a href="https://asibiont.com/en/blog/libsm64-kak-kultovyy-super-mario-64-prevratili-v-biblioteku-dlya-igrovykh-dvizhkov">Libsm 64 : Super Mario 64 Reborn as a Library for... — ASI Biont Blog</a></li>
<li><a href="https://github.com/n64decomp/sm64">GitHub - n64decomp/ sm 64 : A Super Mario 64 decompilation , brought...</a></li>

</ul>
</details>

**社区讨论**: 社区成员对该库的潜力表示兴奋，将其与元宇宙的承诺相比但无炒作。有人要求演示视频，视频已被提供，还分享了一个使用 libsm64 的项目精选列表。

**标签**: `#game development`, `#software engineering`, `#decompilation`, `#open source`, `#C++`

---

<a id="item-10"></a>
## [长鑫科技科创板首日暴涨 471%](https://www.stcn.com/article/detail/4042119.html) ⭐️ 8.0/10

这一里程碑凸显了中国推动半导体自主化的决心，长鑫科技是国内关键的 DRAM 制造商。创纪录的 IPO 为其提供了大量资金以扩大产能，与三星、SK 海力士等全球存储巨头竞争。 本次 IPO 实际募资约 579 亿元，超额配售权行使后预计达 666 亿元。公司预计 2026 年上半年归母净利润 500-570 亿元，同比大幅扭亏。

telegram · zaihuapd · 7月27日 01:29

**背景**: 长鑫科技是中国领先的 DRAM 芯片制造商，专注于消费电子和数据中心的存储芯片。科创板是上海面向科技公司的纳斯达克式板块，上市条件较为宽松。DRAM 是电脑和智能手机的关键组件，中国长期以来寻求减少对外国供应商的依赖。

**标签**: `#IPO`, `#semiconductor`, `#memory`, `#China tech`, `#stock market`

---

<a id="item-11"></a>
## [阿里推出千问办公 AI 办公平台，支持电脑操控](https://qwenwork.cn/) ⭐️ 8.0/10

阿里巴巴上线了“千问办公”Beta 版，这是一站式 AI 办公平台，可通过自然语言生成和编辑文档、表格、演示文稿、网页、代码及多媒体内容。桌面客户端还具备电脑操控功能，能执行浏览器自动化和跨应用的点击、输入、数据提取等操作。 该产品将阿里巴巴的 AI 办公工具整合到一个与钉钉深度绑定的平台中，提供有竞争力的定价和全新的电脑操控功能，有望显著提升专业人士的工作效率。这表明阿里在 AI 办公领域积极进取，可能重塑办公自动化方式。 该平台提供免费版、个人标准版（78 元/月）和高级版（158 元/月），新用户限时获赠 2000 积分。电脑操控功能可能截取屏幕内容并执行不可撤销操作，因此平台默认会在操作前征求用户确认。

telegram · zaihuapd · 7月27日 05:45

**背景**: 阿里巴巴的千问（Qwen）是大语言模型系列，千问办公利用其能力实现办公自动化。能够操控电脑的 AI 智能体（Computer Use）概念日益流行，如 Browser Use 和 OpenAI 的 Computer Use 智能体等项目。千问办公与钉钉（中国主要企业协作工具）的整合，为其提供了强大的分发优势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://36kr.com/p/3909382165419144">AI办公，阿里得靠“千问办公”换个打法-36氪</a></li>
<li><a href="https://www.aihub.cn/tools/qwenwork/">千问办公 - 阿里推出的一站式 AI Agent 办公平台，把任务做完并交付产物 - AIHub</a></li>
<li><a href="https://github.com/browser-use/browser-use">browser- use /browser- use : Make websites accessible for AI agents.</a></li>

</ul>
</details>

**标签**: `#AI office`, `#Alibaba`, `#Qwen`, `#computer control`, `#productivity`

---

<a id="item-12"></a>
## [中国启动国产 DUV 光刻机量产](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 8.0/10

据知情人士透露，中国已开始大规模生产自主研发的浸没式深紫外（DUV）光刻机，计划今年生产约 5 台，2027 年约 20 台，将交付中芯国际、华虹半导体等国内芯片制造商。 这标志着中国在减少对外国半导体设备依赖方面迈出了重要一步，尤其是在当前出口限制持续的情况下，荷兰供应商 ASML 首当其冲。尽管该设备在性能和可靠性上仍落后于 ASML，但产量的提升可能逐步侵蚀 ASML 在中国市场的份额。 国产设备主要使用国产零部件，但部分关键部件仍来自日本，今年本地供应链延误已影响进度。芯片制造商需要数月甚至更长时间测试其精度与兼容性，方能投入量产产线。

telegram · zaihuapd · 7月27日 14:10

**背景**: 深紫外（DUV）光刻是半导体制造中的关键工艺，使用 248 纳米或 193 纳米波长的光在晶圆上刻印电路。浸没式光刻通过在镜头和晶圆之间加入液体（通常是水）来提高分辨率，可实现 45 纳米以下的特征尺寸。ASML 目前主导 DUV 市场，但出口限制促使中国自主研发同类设备。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography</a></li>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://www.asml.com/en/products/duv-lithography-systems">DUV lithography systems | Products - ASML</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#lithography`, `#China`, `#ASML`, `#manufacturing`

---