---
layout: default
title: "Horizon Summary: 2026-09-09 (ZH)"
date: 2026-09-09
lang: zh
---

> 从 37 条内容中筛选出 14 条重要资讯。

---

1. [关于纳维-斯托克斯千年奖问题](#item-1) ⭐️ 9.0/10
2. [OpenAI 宣称解决纳维-斯托克斯千禧年难题](#item-2) ⭐️ 9.0/10
3. [NeurIPS 用不可靠的 AI 检测器将 178 篇论文直接拒稿](#item-3) ⭐️ 9.0/10
4. [Meta 推出个人 AI 代理 Muse，具备分层提示注入防御](#item-4) ⭐️ 8.0/10
5. [AlphaGenome Atlas 绘制人类基因组所有单碱基变化的高分辨率图谱](#item-5) ⭐️ 8.0/10
6. [数学家声明引发纳维-斯托克斯与 AI 研究伦理争议](#item-6) ⭐️ 8.0/10
7. [OpenAI 声称 AI 模型攻克 Navier-Stokes 千禧年问题，引发争议](#item-7) ⭐️ 8.0/10
8. [Qwen3.8 27B 量化基准测试：4-bit 保持质量，1-bit 崩溃](#item-8) ⭐️ 8.0/10
9. [陶哲轩警告：AI 或耗尽数学开放问题](#item-9) ⭐️ 8.0/10
10. [马来西亚拟用华为 Ascend 910C 建主权 AI 项目，弃用美芯片](#item-10) ⭐️ 8.0/10
11. [张一鸣亲自督导字节跳动空间视频模型，面向 Pico 头显](#item-11) ⭐️ 8.0/10
12. [ASML 与台积电合作推进 High NA EUV 升级至 12 英寸光掩模](#item-12) ⭐️ 8.0/10
13. [中国设定 2030 年智能算力 9800 EFLOPS 目标](#item-13) ⭐️ 8.0/10
14. [OpenAI 发布 ChatGPT Images 2.5 图像模型](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [关于纳维-斯托克斯千年奖问题](https://simonwillison.net/2026/Sep/8/on-navier-stokes/) ⭐️ 9.0/10

OpenAI 宣布一个未发布的模型解决了纳维-斯托克斯存在性和光滑性问题，但结果因一名合作数学家的欺诈指控而蒙上阴影。

rss · Simon Willison · 9月8日 23:55

**标签**: `#OpenAI`, `#Navier-Stokes`, `#mathematics`, `#AI research`, `#Millennium Prize Problems`

---

<a id="item-2"></a>
## [OpenAI 宣称解决纳维-斯托克斯千禧年难题](https://www.reddit.com/r/MachineLearning/comments/1wavdi7/openal_says_it_has_cracked_one_of_maths/) ⭐️ 9.0/10

OpenAI 通过其官网和《纽约时报》的报道宣布，它已给出纳维-斯托克斯方程存在性与光滑性问题的一个解答，这是克莱数学研究所七大千禧年难题之一。该证明尚未经过同行评审，也未得到数学界的独立验证。 如果证明正确，这将是自庞加莱猜想以来首个被解决的千禧年难题，也是 AI 与纯数学交汇的标志性事件。它还将证实关于流体行为的长期数学猜想，对物理学、工程学和气象建模产生深远影响，但专家提醒，非凡的主张需要非凡的验证。 这一声明针对三维纳维-斯托克斯方程的存在性与光滑性问题，即从光滑初值出发是否总存在全局光滑解。截至 2026 年，千禧年难题中仅有庞加莱猜想被正式认定解决，因此 OpenAI 的证明仍未得到数学界的广泛验证。

reddit · r/MachineLearning · /u/Shizuka\_Kuze · 9月8日 17:42

**背景**: 纳维-斯托克斯方程是描述牛顿流体（如水和空气）动量守恒的偏微分方程。千禧年难题由克莱数学研究所在 2000 年设立，是数学界七个最困难的未解问题，每个问题的解决者将获得一百万美元奖金。由于三维纳维-斯托克斯系统支配着湍流等流体现象，证明其解在有限时间内不会爆炸或产生奇点，一直是数学和物理领域的核心挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_equations">Navier–Stokes equations - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Millennium_Prize_Problems">Millennium Prize Problems - Wikipedia</a></li>
<li><a href="https://www.claymath.org/millennium-problems/">The Millennium Prize Problems - Clay Mathematics Institute</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Navier-Stokes`, `#Mathematics`, `#AI Research`, `#Millennium Problem`

---

<a id="item-3"></a>
## [NeurIPS 用不可靠的 AI 检测器将 178 篇论文直接拒稿](https://www.reddit.com/r/MachineLearning/comments/1wakf62/neurips_deskrejected_178_papers_for_being/) ⭐️ 9.0/10

NeurIPS 的立场论文赛道使用专有的 Pangram 检测器，将 178 篇（占投稿 18.4%）论文以“AI 生成”为由直接拒稿，既无人工审核，也没有申诉渠道。独立研究人员的测试发现，同一检测器将三位赛道主席自己的近期论文标记为 24%至 69%的 AI 生成概率，意味着这些主席若按规则执行也会面临风险。 这一事件暴露了在高风险决策中依赖黑箱式 AI 文本检测器的危险，尤其是在没有发布校准数据或申诉机制的情况下。它还会伤害非英语母语的研究者，因为规范的 ESL 学术写作被大量研究证实更容易被误判为 AI 生成。 Pangram 的默认设置最初标记了整个赛道 42.7%的投稿；组织方不得不缩小文本窗口，才将标记率降至 12.7%。有 22 篇论文因得分高于 0.5 且作者否认使用 AI 而被拒；原帖援引的一项 Stanford 研究显示，61.22%的人类撰写 TOEFL 作文也可能被误判为 AI 生成。

reddit · r/MachineLearning · /u/tughanbulut · 9月8日 10:19

**背景**: Pangram 是由位于布鲁克林的 Pangram Labs（前 OpenAI 研究人员创办）开发的专有 AI 文本检测器，其原理是通过分析文本中的语言模式，估计内容由大语言模型生成的可能性。这类 AI 检测工具常被用于学术诚信审查，但它们存在已知的误报问题，尤其对具有固定结构或由非英语母语者撰写的正式文本误判率偏高，并已被批评助长针对 AI 使用情况的“猎巫”风气。NeurIPS 是最负盛名的机器学习会议之一，其立场论文赛道接收论证充分、兼具推测性或争议性的观点论文。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Pangram_Labs">Pangram ( AI detector ) - Wikipedia</a></li>
<li><a href="https://www.quetext.com/blog/pangram-ai-detector-review">Pangram AI Detector Review: Is It Worth It for Educators?</a></li>
<li><a href="https://www.pangram.com/research/how-it-works">How AI Detection Works | Pangram</a></li>

</ul>
</details>

**标签**: `#AI detection`, `#NeurIPS`, `#academic publishing`, `#ethics`, `#machine learning`

---

<a id="item-4"></a>
## [Meta 推出个人 AI 代理 Muse，具备分层提示注入防御](https://ai.meta.com/muse/) ⭐️ 8.0/10

Meta 推出了面向普通用户的个人 AI 代理“Muse”，并宣称其具备针对提示注入的分层防护机制。该公告发布在 ai.meta.com/muse 上，将安全视为核心设计要素。 这一事件意义重大，因为 Meta 正将 AI 代理带给庞大的大众用户群体，而不仅仅是 AI 爱好者。它也表明，提示注入防护已成为 AI 代理类产品的关键考量。 据 Meta AI 的 David Singleton 介绍，其提示注入防御是分层的：模型经过训练能够识别并抵抗攻击；运行框架会标记来自不可信来源的内容；确定性代码会对结果进行校验；另外还有一组分类器在代理无法触及的位置运行。

hackernews · yks · 9月8日 19:25 · [社区讨论](https://news.ycombinator.com/item?id=49615537)

**背景**: 提示注入是一种网络安全攻击手段，攻击者通过精心构造的输入，使大语言模型产生超出其预期规则的违规行为。能够浏览网页或处理上传文件的 AI 代理尤其容易遭受间接提示注入——恶意指令被隐藏在代理检索到的内容中。Meta 在 Facebook、Instagram 和 WhatsApp 上拥有庞大的用户基础，这使得 Muse 在向普通用户推广个人 AI 助手方面具有潜在的分发优势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection</a></li>
<li><a href="https://www.ibm.com/think/topics/prompt-injection">What Is a Prompt Injection Attack? | IBM</a></li>

</ul>
</details>

**社区讨论**: 评论者认为 Muse 是 Meta 面向主流“大众层级”AI 用户的尝试，部分人赞赏 David Singleton 分享的详细的提示注入防御方案。另一些人则对由 Meta 运营一个掌握个人数据的代理表示不信任，担心数据收集风险；也有至少一位用户希望用 Muse 来抓取自己的 Facebook 群组内容。

**标签**: `#AI`, `#Meta`, `#virtual-assistant`, `#security`, `#prompt-injection`

---

<a id="item-5"></a>
## [AlphaGenome Atlas 绘制人类基因组所有单碱基变化的高分辨率图谱](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/alphagenome-atlas/) ⭐️ 8.0/10

Google DeepMind 已发布 AlphaGenome Atlas，这是一个交互式目录，可预测人类基因组中 90 亿个单核苷酸变异的分子效应与 AVI 分数。该资源现已在线开放给研究人员使用。 它将高分辨率解读能力扩展到约占人类基因组 98%的非编码区域，这些区域中包含许多与疾病相关的变异。这使得 AI 驱动的变异解读能更广泛地应用于人类疾病研究和基因组分析。 AlphaGenome 是一个统一的 DNA 序列模型，以 1 Mb 的 DNA 序列作为输入，该图谱提供了 90 亿个变异的预测结果。相关研究旨在克服现有方法中常见的输入序列长度与预测分辨率之间的权衡问题。

hackernews · utiiiD · 9月8日 14:55 · [社区讨论](https://news.ycombinator.com/item?id=49611251)

**背景**: 人类 DNA 由编码蛋白质的编码区，以及占比更大的、控制基因表达方式和时间的非编码区组成。DNA 单碱基的改变被称为单核苷酸变异，它可能影响这两类区域，并与疾病相关。AlphaGenome 利用深度学习来解读这些长 DNA 序列，并预测此类变异的分子效应。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nature.com/articles/s41586-025-10014-0">Advancing regulatory variant effect prediction with AlphaGenome | Nature</a></li>
<li><a href="https://deepmind.google/blog/alphagenome-atlas-a-predictive-map-of-every-possible-dna-letter-change-in-the-human-genome/">AlphaGenome Atlas: Molecular predictions for 9 Billion human DNA variants — Google DeepMind</a></li>
<li><a href="https://deepmind.google/blog/alphagenome-ai-for-better-understanding-the-genome/">AlphaGenome: AI for better understanding the genome — Google DeepMind</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍欢迎这次发布，并说明访问图谱时“所属机构”并非必填项。还有人追问技术局限，例如是否覆盖启动子序列；也有人询问能否将其用于解读 23andMe 等个人基因数据。有评论者指出，并非所有 DeepMind 的生物学模型都能像 AlphaFold 一样产生持久影响。

**标签**: `#genomics`, `#deep learning`, `#AI for science`, `#human genome`, `#Google DeepMind`

---

<a id="item-6"></a>
## [数学家声明引发纳维-斯托克斯与 AI 研究伦理争议](https://cims.nyu.edu/~tristanb/statement.pdf) ⭐️ 8.0/10

Tristan Buckmaster 发布个人声明，介绍他与 Levent Alpöge 在纳维-斯托克斯相关问题上的进展，包括带强迫的多孔介质、Boussinesq 和三维不可压缩 Euler 方程的有限时间爆破结果。他们并没有宣称解决悬赏 100 万美元的千禧年问题，但声称证明了一个类似（非千禧年版）的纳维-斯托克斯问题；这份声明与 OpenAI、Anthropic 之间围绕一项未经证实的 OpenAI 纳维-斯托克斯解破坏声明所产生的优先权争议交织在一起。 这一争议凸显了 AI 实验室对用户生成数据的访问可能威胁学术优先权：一个私有模型可能在数学家尚未公开其推理过程时就吸收这些内容，并将其变成一项声明。若要让 AI 驱动的发现获得信任，数学界需要经过验证的证明、透明的数据来源，以及明确规则来为可能影响模型的研究人员提供署名。 所链接的条目是 PDF 格式的个人声明，并非同行评审论文或正式证明。Buckmaster 和 Alpöge 报告了在 Euler、Boussinesq 和多孔介质方程爆破问题上的进展；搜索结果将 OpenAI 关于纳维-斯托克斯解破坏的未经证实声明标为 2026 年 9 月 8 日。Levent Alpöge 受雇于 Anthropic，而 OpenAI 表示无法排除来自产品使用数据的去标识化信息帮助改进了其模型。

hackernews · procedurecall · 9月8日 05:42 · [社区讨论](https://news.ycombinator.com/item?id=49605915)

**背景**: 纳维-斯托克斯方程用于描述流体运动，其存在性与光滑性问题属于克莱数学研究所七个千禧年大奖问题之一，悬赏 100 万美元。Euler 方程是忽略黏性的理想化流体方程，证明这类偏微分方程系统的有限时间爆破是当前活跃的研究方向。此次事件的核心是：AI 公司是否能在借助用户与其产品交互所获得的信息来加速或产生新证明的同时，不为所涉及的人类研究人员提供恰当署名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier-Stokes_problem">Navier-Stokes problem</a></li>
<li><a href="https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_existence_and_smoothness">Navier–Stokes existence and smoothness - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_equations">Navier–Stokes equations - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者几乎一致批评 OpenAI，认为该事件相当于窃取研究人员的工作，并用“你为什么要毁掉自己的职业生涯？”这类威胁进行施压。也有人提醒，如果这些成果并未进入 OpenAI 模型，这可能只是被 AI 加速的恶性学术竞争；但最引人注目的是 OpenAI 自己也承认“不能排除”经去标识化的产品使用数据帮助改进了模型。

**标签**: `#navier-stokes`, `#academic-ethics`, `#openai`, `#ai-research`, `#mathematics`

---

<a id="item-7"></a>
## [OpenAI 声称 AI 模型攻克 Navier-Stokes 千禧年问题，引发争议](https://openai.com/index/navier-stokes-solution/) ⭐️ 8.0/10

OpenAI 发表博客文章称，一个训练时间不到两周的内部模型能够更好地解决 Navier–Stokes 存在性与光滑性问题，这是千禧年大奖难题之一。该公司表示，该模型生成的证明显示 Navier–Stokes 方程能在有限时间内产生奇点。 如果这一说法成立，这将在数学界最难的问题之一上取得历史性突破，并有力展示 AI 辅助研究的能力。随之而来的争议也引发了关于研究署名、开放共享以及大规模 AI 努力如何影响数学家分享早期工作意愿的紧迫问题。 该博客文章提供的技术细节很少，结果尚未经过同行评审或独立验证。社区批评主要集中在模型可能建立在他人的既有研究和特定提示词之上；Terence Tao 警告说，此类 AI 驱动的努力可能会在先驱研究充分发展之前就将其“夷平”。

hackernews · tedsanders · 9月8日 17:13 · [社区讨论](https://news.ycombinator.com/item?id=49613262)

**背景**: Navier–Stokes 存在性与光滑性问题问的是：描述流体运动的方程的解是否始终光滑，还是可能在有限时间内形成奇点。2000 年，克莱数学研究所将其列为七个千禧年大奖难题之一，每个难题的正确解答可获得 100 万美元奖金。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Millennium_Prize_Problems">Millennium Prize Problems - Wikipedia</a></li>
<li><a href="https://www.claymath.org/millennium-problems/">The Millennium Prize Problems - Clay Mathematics Institute</a></li>
<li><a href="https://openai.com/index/navier-stokes-solution/">On the Navier – Stokes Millennium Prize Problem | OpenAI</a></li>

</ul>
</details>

**社区讨论**: 评论者分歧严重：有人认为这证明了 AI 数学能力的快速提升，也有人怀疑该工作是否基于他人的研究和提示词。多人引用 Terence Tao 的观察，即仅凭研究传闻就可能触发大规模 AI 竞逐，从而抑制数学家之间的开放交流。由于证明尚未得到验证且模型属于专有，许多人对该声明持怀疑态度。

**标签**: `#AI`, `#mathematics`, `#OpenAI`, `#Navier-Stokes`, `#research integrity`

---

<a id="item-8"></a>
## [Qwen3.8 27B 量化基准测试：4-bit 保持质量，1-bit 崩溃](https://quesma.com/blog/qwen38-27b-quantizations-benchmarked/) ⭐️ 8.0/10

一项针对 Qwen3.8 27B 的新基准测试显示，4-bit 量化版本基本保留了模型质量，2-bit 分数略低，而 1-bit 版本则彻底崩溃。 这为本地运行开源权重 LLM 的用户提供了实用的参考，说明量化到多低位才会让质量明显下降。它表明 4-bit 量化是在节省显存与保留性能之间非常可靠的选择，而 1-bit 仍然无法用于实际任务。 图表标注了 Wilson 95% 置信区间，但评论区指出该区间并不能反映多次运行的随机波动；2-bit 的分数也明显低于 4-bit。该基准未覆盖 3-bit（Q3）档位和 KV cache 量化，而这正是多位读者希望进一步测试的方向。

hackernews · stared · 9月8日 14:49 · [社区讨论](https://news.ycombinator.com/item?id=49611128)

**背景**: 量化（quantization）是一种将模型权重从 16 位浮点数等高精度格式降低到 4-bit、2-bit 甚至 1-bit 等更低比特数的技术，能让大语言模型大幅缩小体积并降低运行成本。Qwen 是阿里巴巴云开发的开源权重大语言模型系列，Qwen3.8 27B 是该系列中一个约 270 亿参数的版本。像 1-bit 这种极端量化会把权重压缩到极少数取值，虽然能大幅节省内存，但也可能导致输出质量严重下降。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen">Org profile for Qwen on Hugging Face, the AI community building the...</a></li>
<li><a href="https://www.ibm.com/think/topics/quantization">What is Quantization? | IBM</a></li>
<li><a href="https://www.maartengrootendorst.com/blog/quantization/">A Visual Guide to Quantization - Maarten Grootendorst</a></li>

</ul>
</details>

**社区讨论**: 评论区对方法论提出了批评：有评论者指出 Wilson 置信区间并不代表运行间的随机波动，与文章暗示的用法不符；也有人认为 Qwen 会通过更长时间的思考来弥补量化损失，因此测试结果比直觉预期的更好。还有读者希望继续评测 KV cache 量化，并指出测试缺少对 16GB 以下显卡至关重要的 Q3 档位；另有一位新手询问在个人电脑上运行这类模型是否安全。

**标签**: `#LLM`, `#quantization`, `#benchmarking`, `#local-inference`, `#Qwen`

---

<a id="item-9"></a>
## [陶哲轩警告：AI 或耗尽数学开放问题](https://simonwillison.net/2026/Sep/9/terence-tao/) ⭐️ 8.0/10

著名数学家陶哲轩在 Mathstodon 上警告：好的开放性问题正被 AI 驱动的努力以不可再生的方式“开采”。他说，仅凭某人正在研究某个问题的传闻就可能触发大规模 AI 抢跑求解，从而让研究人员不愿再公开分享有前景的研究方向。 陶哲轩的警告凸显了一个新风险：AI 的速度和规模可能侵蚀长期以来支撑数学及其他科学的合作规范。如果研究者纷纷隐藏思路，延续数百年的开放科学传统可能受到严重损害。 该评论发布在 Mathstodon 上，并被 Simon Willison 的博客引用。陶哲轩特别聚焦于激励机制：当一个有前景的问题被公开提及，AI 驱动的努力可能会在原始研究项目充分发挥潜力之前就将其“夷平”。

rss · Simon Willison · 9月9日 00:20

**背景**: 陶哲轩是加州大学洛杉矶分校的菲尔兹奖得主，以分析学和数论研究闻名，也以在网上开放分享数学思路著称。在数学中，“开放问题”指尚未解决的难题，研究者通常会公开它们以邀请合作。随着 AI 系统开始具备辅助科研级数学的能力，公开提出的问题可能很快被大量 AI 驱动的智能体竞相求解，这让人们担忧共享问题会被当作稀缺且不可再生的资源。

**标签**: `#AI ethics`, `#mathematics`, `#open science`, `#research impact`, `#Terence Tao`

---

<a id="item-10"></a>
## [马来西亚拟用华为 Ascend 910C 建主权 AI 项目，弃用美芯片](https://www.businesstimes.com.sg/international/malaysia-eyes-huawei-chips-ai-project-despite-us-warning) ⭐️ 8.0/10

马来西亚正在认真评估采用华为 Ascend 910C 芯片，作为其规模 20 亿林吉特（约 4.94 亿美元）主权 AI 项目的核心。若最终敲定，马来西亚将成为首个公开选择中国 AI 加速器而非美国产品的外国政府。 如果成行，这将是首个政府层面弃用美国 AI 芯片的案例，可能重塑全球 AI 供应链，并考验美国出口管制的影响力。这也表明尽管受到制裁，华为硬件正获得更多认可，可能为中国打开新的出口市场。 此举面临美国的警告，即使用华为 AI 加速器芯片可能违反美国出口规定，但据称马来西亚认为采购纯属商业决定。采购芯片的具体数量尚未公开。

telegram · zaihuapd · 9月8日 03:35

**背景**: 主权 AI（Sovereign AI）指一个国家将自身 AI 技术栈（包括数据、模型、基础设施和运营）置于本地司法管辖与控制之下。华为 Ascend 910C 是一款基于 chiplet 封装的 AI 加速芯片，被视为 NVIDIA 产品的主要中国替代方案；DeepSeek 的研究显示，其推理性能约为 NVIDIA H100 的 60%。美国已对向中国出口先进 AI 芯片实施限制，并警告外国买家购买部分华为芯片可能违反出口管制规则。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/ai-sovereignty">What is AI sovereignty? - IBM</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/deepseek-research-suggests-huaweis-ascend-910c-delivers-60-percent-nvidia-h100-inference-performance">DeepSeek research suggests Huawei &#x27;s Ascend 910 C delivers 60% of...</a></li>
<li><a href="https://www.macrostack.net/silicon/huawei-ascend-910c">Huawei Ascend 910 C specs and availability — Macrostack</a></li>

</ul>
</details>

**标签**: `#华为`, `#AI芯片`, `#地缘政治`, `#出口管制`, `#马来西亚`

---

<a id="item-11"></a>
## [张一鸣亲自督导字节跳动空间视频模型，面向 Pico 头显](https://www.bloomberg.com/news/articles/2026-09-07/bytedance-founder-joins-ai-elite-in-race-to-perfect-world-models) ⭐️ 8.0/10

字节跳动创始人张一鸣正亲自督导一款基于 Seedance 的实时空间视频生成模型，最快可能在 2026 年 10 月发布。该模型可为 Pico 头显生成响应语音或动作的互动虚拟世界。 如果实现，该技术可将高强度计算转移至云端，降低虚拟现实设备的硬件门槛，让更轻便的头显也能运行沉浸式世界。这也表明字节跳动正加入打造世界模型与空间智能的 AI 竞赛。 据称该系统能以大约每秒 20 帧的速度生成视频，延迟约 0.05 秒，并将高强度计算转移至云端。发布时间尚未证实，仍可能调整，官方也未公布相关细节。

telegram · zaihuapd · 9月8日 04:05

**背景**: Seedance 是字节跳动的视频生成模型系列，Seedance 1.0 支持从文本和图像进行多镜头视频生成，Seedance 2.0 则采用统一的多模态音视频联合生成架构。空间视频生成与世界模型的目的是让 AI 生成具有一致 3D 几何关系和可控相机的交互场景或视频。实时生成用于 VR 需要极低延迟和高帧率，因此将计算转移到云端是该方案的核心。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Seedance">Seedance - Wikipedia</a></li>
<li><a href="https://seed.bytedance.com/en/seedance">Seedance 1.0 - seed.bytedance.com</a></li>
<li><a href="https://www.worldlabs.ai/blog/atlas">Atlas: A World Model for Spatial Intelligence | World Labs</a></li>

</ul>
</details>

**标签**: `#AI`, `#ByteDance`, `#Virtual Reality`, `#Video Generation`, `#Spatial Computing`

---

<a id="item-12"></a>
## [ASML 与台积电合作推进 High NA EUV 升级至 12 英寸光掩模](https://www.nrc.nl/nieuws/2026/09/08/asml-gaat-samenwerken-met-taiwanese-chipgigant-tsmc-om-zijn-nieuwste-chipmachines-te-upgraden-a4936073) ⭐️ 8.0/10

ASML 与台积电于 9 月 7 日发起产业合作，推动 High NA EUV 光刻从现有 6 英寸光掩模转向 12 英寸规格，以提高设备生产率、降低芯片制造成本并减少拼接限制。路线图计划在 2031 年建成 12 英寸光掩模试产线，2033 年将相关系统用于先进制程量产；台积电则拟从 2030 年起将 High NA EUV 用于先进节点的大规模制造。 这一合作很重要，因为 High NA EUV 是进入亚 2 纳米制程时代后下一代关键光刻技术，而光掩模尺寸正在成为成本和生产率的主要瓶颈。若能成功转向 12 英寸光掩模，将有助于降低制造成本、消除设计拼接限制，并可能加速整个半导体行业对 High NA EUV 的采用。 当前半导体光刻中使用的光掩模通常是 6 英寸（约 152 毫米）的熔融石英版，因此向 12 英寸光掩模的迁移意味着掩模制造、搬运、保护膜和曝光设备等环节都要发生重大变化。ASML 与台积电的计划具体目标是在 2031 年建成 12 英寸光掩模试产线，并在 2033 年将相关系统用于先进制程量产。

telegram · zaihuapd · 9月8日 06:55

**背景**: 极紫外（EUV）光刻利用激光激发锡等离子体产生的 13.5 纳米波长光线，在硅晶圆上刻画出集成电路图形。光掩模是一块熔融石英制成的母版，承载芯片某一层的图形，并在光刻过程中被投影到晶圆上。High NA EUV 是 EUV 系统的下一代技术，通过更高的数值孔径获得更精细的分辨率，以支撑亚 2 纳米制程时代。从业界标准的 6 英寸光掩模转向 12 英寸规格，需要在半导体制造基础设施各环节进行大量改造。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.asml.com/en/company/stories/2024/5-things-high-na-euv">5 things you should know about High NA EUV lithography - ASML</a></li>
<li><a href="https://en.wikipedia.org/wiki/EUV_lithography">EUV lithography - Wikipedia</a></li>
<li><a href="https://www.appliedmaterials.com/us/en/semiconductor/products/shape/photomask.html">Photomask | Applied Materials</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#EUV`, `#lithography`, `#ASML`, `#TSMC`

---

<a id="item-13"></a>
## [中国设定 2030 年智能算力 9800 EFLOPS 目标](https://www.scmp.com/tech/policy/article/3366733/china-targets-fourfold-boost-ai-computing-capacity-2030-major-tech-push) ⭐️ 8.0/10

中国工业和信息化部发布未来五年产业规划，提出到 2030 年智能算力达到 9800 EFLOPS 的目标。规划还提出 2026 至 2030 年累计投入 3.8 万亿元进行信息基础设施建设。 该目标表明，在算力已成为大型 AI 模型发展关键瓶颈的背景下，中国意在保持并扩大其在 AI 基础设施领域的优势地位。实现超过 4 倍的增长不仅有助于降低对进口高端芯片的依赖，也将为国内 AI 开发者提供更大算力底座，对全球产业链和竞争格局产生重要影响。 截至今年 6 月底，中国智能算力已达 2185 EFLOPS，同比增长 177%；要实现 2030 年目标，算力规模需在此基础上增长至 4 倍以上。规划还提出有序部署万卡级以及 10 万卡以上的智能计算集群，并加强基础设施与国产算力芯片的适配。

telegram · zaihuapd · 9月8日 11:23

**背景**: EFLOPS 即每秒百亿亿次（10^18 次）浮点运算，是衡量超级计算机和高性能计算系统性能的常用单位。智能算力是指面向 AI 训练与推理的计算能力，通常由 GPU、TPU 等专用加速芯片提供，而不是普通 CPU。所谓“万卡集群”，是指由一万张以上加速卡组成的高性能 AI 计算系统，可支持千亿乃至万亿参数大模型的训练。规划中的目标正是以这类加速集群和国产算力芯片的部署为基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Floating_point_operations_per_second">Floating point operations per second - Wikipedia</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/691429521">什么是智能算力？未来趋势如何？ - 知乎</a></li>
<li><a href="https://blog.csdn.net/hero272285642/article/details/144422260">AI大模型训练的万卡集群是什么概念-CSDN博客</a></li>

</ul>
</details>

**标签**: `#AI算力`, `#政策规划`, `#基础设施`, `#中国`, `#人工智能`

---

<a id="item-14"></a>
## [OpenAI 发布 ChatGPT Images 2.5 图像模型](https://openai.com/index/introducing-chatgpt-images-2-5/) ⭐️ 8.0/10

OpenAI 于 9 月 8 日发布 ChatGPT Images 2.5，相比 2.0 版本细节更清晰、编辑更精准，图像生成延迟最高降低 50%。新版模型正面向 ChatGPT、ChatGPT Work 和 Codex 全平台用户推出，并新增 Sketch 手绘引导、模板、图片评论与提示词分享功能。 此次发布升级了 OpenAI 一款广泛使用的 AI 图像生成服务，在加快渲染速度的同时提供更精细的编辑控制。同步上线的 API 使开发者能将 GPT-Image-2.5 集成进产品，两种模型变体分别针对速度与精度提供不同取舍。 OpenAI 同时推出两款 API 模型：GPT-Image-2.5 Flare 面向通用任务，提供质量、编辑和速度上的同样改进；GPT-Image-2.5 Sunburst 则适用于细致创意工作，生成时间更长但精度更高。Sunburst 按每百万图像输出 token 定价 30 美元；ChatGPT 新增的“图片评论”功能并非社交评论，而是让用户在图上的标记点供模型执行。

telegram · zaihuapd · 9月8日 18:45

**背景**: OpenAI 一直在为 ChatGPT 开发集成式图像生成能力，此前已有 GPT Image 系列模型。ChatGPT Images 产品线主打在对话中理解与编辑图像，能够处理参考图保真度、多轮一致性等任务。2.5 版本新增了 Sketch 等工具，可将粗略线条涂鸦转化为精致的成品图，并提供面向传单、产品照片等常见版式的模板；这些功能让不会设计的普通用户也能开展复杂的图像工作流。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-chatgpt-images-2-5/">Introducing ChatGPT Images 2.5 | OpenAI</a></li>
<li><a href="https://developers.openai.com/api/docs/models/gpt-image-2.5-sunburst">GPT-Image-2.5 Sunburst Model | OpenAI API</a></li>
<li><a href="https://www.techradar.com/ai-platforms-assistants/chatgpt/chatgpt-images-2-5-is-out-ive-been-testing-it-for-24-hours-and-these-are-the-3-new-features-youll-actually-use">ChatGPT Images 2 . 5 is out — I’ve been testing it for 24... | TechRadar</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#image generation`, `#AI model release`, `#ChatGPT`, `#API`

---