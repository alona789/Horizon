---
layout: default
title: "Horizon Summary: 2026-10-17 (ZH)"
date: 2026-10-17
lang: zh
---

> 从 37 条内容中筛选出 8 条重要资讯。

---

1. [Claude 揭开 NIST ECDSA 曲线种子来源：出自 lrand48 时间戳](#item-1) ⭐️ 9.0/10
2. [llama.cpp 在越狱 PS5 上原生运行任意 GGUF 模型](#item-2) ⭐️ 8.0/10
3. [Jake Archibald 实测对比 JPEG XL 与 AVIF 的网页实际表现](#item-3) ⭐️ 8.0/10
4. [研究人员利用 OpenBSD 中潜伏 37 年的内核漏洞](#item-4) ⭐️ 8.0/10
5. [ORL 与 dlmrt：单张 RTX 5090 上扩散语言模型解码达 2,788 tokens/s](#item-5) ⭐️ 8.0/10
6. [商务部拟对人工智能、生物医药、光伏技术出口实施临时登记](#item-6) ⭐️ 8.0/10
7. [法院文件曝光 Telegram 向美国执法部门提供用户数据](#item-7) ⭐️ 8.0/10
8. [Anthropic IPO 估值预期据报下调至 1.5 万亿美元](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Claude 揭开 NIST ECDSA 曲线种子来源：出自 lrand48 时间戳](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Anthropic 前沿红队报告称，Claude 在不到半小时内查明 NIST P-192、P-224、P-256、P-384 和 P-521 椭圆曲线所用种子值均来自 C 标准库的 lrand48 伪随机数生成器，并以 Unix 时间戳作为其种子。这些种子并非任何哈希算法的输出，也不是人们长期假设的某个易记短语的哈希结果。 这一发现解开了一个困扰密码学界约二十年的谜团——长期以来人们怀疑 NSA 刻意挑选 NIST 曲线以便植入后门；同时也表明前沿大模型能够独立完成原创性的密码学逆向分析，而不只是总结已有成果。这可能改变社区评估标准化曲线参数可信度、以及评估其&quot;可验证随机&quot;说法的方式。 第五个二进制种子 B-163 仍不符合 Claude 尝试过的任何生成方式，至今无法解释；研究人员还提醒，确认生成方法并不能排除当年反复生成并丢弃候选值、直到出现具有某种特定性质的曲线的可能。被证实的只是种子的产生方式，而非最终曲线的挑选过程。

hackernews · ahlCVA · 10月16日 18:55 · [社区讨论](https://news.ycombinator.com/item?id=50122800)

**背景**: ECDSA（椭圆曲线数字签名算法）是目前部署最广泛的椭圆曲线密码标准，NIST 于 2000 年在 FIPS 186-2 中标准化了一组具名椭圆曲线。每组参数都附带一个&quot;种子&quot;，理论上应通过哈希该种子推导出曲线系数，从而让使用者能够验证曲线并非被人为恶意构造。由于 NIST 从未解释这些种子的由来，加之 Dual\_EC\_DRBG 后门等历史事件，Neal Koblitz 和 Alfred Menezes 等密码学家对&quot;可验证随机&quot;的说法一直持怀疑态度。lrand48 是 C 标准库中一种古老的伪随机数生成器，基于 48 位整数的线性同余算法，一旦种子已知就极易预测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/ecdsa-curve-origins">Claude reveals ECDSA curve origins \ Anthropic</a></li>
<li><a href="https://www.ibm.com/docs/en/zvm/7.5.0?topic=descriptions-lrand48-generate-pseudorandom-number">lrand 48 () — Generate Pseudorandom Number</a></li>
<li><a href="https://www.explainx.ai/blog/claude-ecdsa-nist-curve-seeds-lrand48-anthropic-frontier-red-team-backdoor-question-2026">ECDSA Curve Seeds Solved: Claude Found lrand48 (2026 ...</a></li>

</ul>
</details>

**社区讨论**: 评论区反应夹杂着黑色幽默：有人总结为&quot;13 年的阴谋论，原来只是 srand48\(time\(NULL\)\)&quot;，Thomas Ptacek 则称这是&quot;对整整一代 NIST 密码学阴谋论的毁灭性消息&quot;。也有人更为谨慎，指出确认生成方式并不能说明当年挑选或丢弃了哪些候选值——这些值似乎是历时数月陆续生成的，因此不能完全排除通过搜索时间戳来定向挑选曲线的可能。还有人猜测无法解释的 B-163 种子或许只是发布过程中的一处笔误。

**标签**: `#cryptography`, `#ECDSA`, `#NIST curves`, `#random number generation`, `#AI/LLM`

---

<a id="item-2"></a>
## [llama.cpp 在越狱 PS5 上原生运行任意 GGUF 模型](https://github.com/cobanov/PS5LM) ⭐️ 8.0/10

一个名为 cobanov/PS5LM 的 GitHub 项目展示了如何在一台越狱的 PlayStation 5 上，通过 llama.cpp 原生进行 GGUF 模型推理，把索尼锁定的游戏主机变成通用本地大模型运行平台。该成果属于概念验证，据称能够以 2-bit 量化运行 Qwen 3 27B 模型。 这表明一台大规模量产且高度锁定的游戏主机可以被改造成便宜、可长期在线的 LLM 推理设备，对于长时间运行、低强度的任务而言，是不错的显卡替代方案。这也进一步巩固了 llama.cpp 作为事实标准便携推理内核的地位——从手机、服务器到游戏主机几乎都能移植。 据描述，该配置以 2-bit 量化运行 Qwen 3 27B，这会限制输出质量，但对于只需要稳定、中等水平 token 流量的任务仍然可用。评论者估算每天电费约 0.7 美元、可产出约 200 万 output token，并指出同样的思路或许也适用于基于 AMD 阉割版 &quot;Cyan Skillfish&quot; APU 的 BC250 主板，这类主板在 eBay 上售价约 150 至 200 美元。

hackernews · Anon84 · 10月16日 18:32 · [社区讨论](https://news.ycombinator.com/item?id=50122431)

**背景**: llama.cpp 是由 Georgi Gerganov 于 2023 年 3 月发起的开源 C/C++ 库，用于对大型语言模型进行推理，并与 GGML 张量库共同开发，如今已成为 Ollama、LM Studio 等大多数本地推理工具的核心。GGUF（GGML Universal File）是一种二进制格式，把模型张量和元数据存放在单个文件中，以便快速加载和保存。越狱 PlayStation 5 指的是利用软件或硬件漏洞在主机上运行未签名代码，而正常情况下主机只能运行索尼许可的软件。PS5 搭载带统一内存的定制 AMD APU，这也是它解锁后被视作低成本推理机器的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Llama.cpp">Llama.cpp</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp">GitHub - ggml-org/llama.cpp: LLM inference in C/C++</a></li>
<li><a href="https://grokipedia.com/page/PlayStation_5_jailbreak">PlayStation 5 jailbreak</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对把封闭设备变成通用计算机感到兴奋：有人把它视为长时间、低强度任务的理想选择，例如监控服务器错误率、查看监控录像或控制植物浇水，还有人畅想 LLM 驱动的 NPC 会成为游戏标配。主要担忧在于托管风险：一位评论者认为项目不应以 GitHub 为主要站点，因为索尼随时可能下架页面，建议改用自有域名。其他人则提到 BC250 这类采用 PS5 衍生阉割版 APU 的硬件，是更便宜的替代路线。

**标签**: `#LLM inference`, `#jailbreaking`, `#PS5`, `#llama.cpp`, `#GGUF`

---

<a id="item-3"></a>
## [Jake Archibald 实测对比 JPEG XL 与 AVIF 的网页实际表现](https://jakearchibald.com/2026/jpeg-xl-vs-avif/) ⭐️ 8.0/10

网页性能专家 Jake Archibald 发表了一篇面向真实网页场景的 JPEG XL 与 AVIF 对比文章，从编码速度、文件体积和画质权衡等角度进行了实测评估。该文在 Hacker News 上引发了 143 条评论的讨论，开发者们分享了具体的 ffmpeg/AVIF 参数配置，并解释了 libjxl 高 effort 模式为何如此缓慢。 图片格式的选择直接影响几乎每一个网站的页面体积、加载性能和带宽成本，因此一份来自可信作者的实际测试能帮助开发者做出具体的技术决策，而不是依赖厂商的基准测试。这也说明 JPEG XL 与 AVIF 之争尚无定论，对于当下需要决定编码和投放哪些格式的团队而言意义重大。 评论者指出，libjxl 的最高 effort 档位对照片仅比默认档小 2–7%（截图和插画约小 25%），却要耗时 9–46 秒，是默认档的 50–180 倍，主要原因是针对感知误差指标 Butteraugli 的迭代式评估—优化循环。有开发者分享了使用 yuva444p 配合 alpha 提取的 ffmpeg 参数，可生成比原图小 10 倍以上且保留 PNG 透明通道的 AVIF 文件；也有人认为 AVIF 对高光的处理（例如一张 F1 赛车照片）存在肉眼可见的画质损失。

hackernews · farlight · 10月16日 16:12 · [社区讨论](https://news.ycombinator.com/item?id=50120224)

**背景**: JPEG XL 是新一代图像格式，同时支持有损和无损压缩，由 JPEG 委员会联合 Google 和 Cloudinary 共同开发，并在 iPhone 16 系列原生支持后获得广泛关注。AVIF 则是由开放媒体联盟基于 AV1 视频编解码器打造的图像格式，目标是在保持观感画质的同时缩小图片体积；两者均免专利费，被普遍视为网页端 JPEG 和 WebP 的继任者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/JPEG_XL">JPEG XL - Wikipedia</a></li>
<li><a href="https://shortpixel.com/blog/what-is-avif-and-why-is-it-good/">What is AVIF and why is it good? - ShortPixel Blog</a></li>
<li><a href="https://www.keycdn.com/blog/avif">AV1 Image File Format ( AVIF ) - KeyCDN</a></li>

</ul>
</details>

**社区讨论**: 整体舆论偏向务实和谨慎，而非一边倒的追捧：评论者深入探讨了 libjxl 的 Butteraugli 优化循环等技术细节，并分享了经过实战检验的 AVIF 编码命令；一位经历过 MP3/LAME 时代的老手则提醒不要过早宣布某个编解码器为“赢家”，指出 WebP 当年的优越性宣传也并未完全兑现。此外还有人批评 AVIF 会把精细的高光细节替换成看似合理的伪影，认为这在某些摄影场景中难以接受。

**标签**: `#image-compression`, `#web-performance`, `#jpeg-xl`, `#avif`, `#codecs`

---

<a id="item-4"></a>
## [研究人员利用 OpenBSD 中潜伏 37 年的内核漏洞](https://calif.io/research/big-fish) ⭐️ 8.0/10

安全研究人员发布了一篇名为&quot;Big Fish&quot;的详细技术文章，描述了他们在 OpenBSD 中发现并成功利用一个潜伏约 37 年、可追溯到共享的 4.4BSD 时代代码的内核漏洞。该披露引发了讨论：为何即便是世界上审查最严格的代码库之一，也会遗漏如此长寿的漏洞。 OpenBSD 被普遍视为最注重安全的主流类 Unix 系统，因此一个潜伏 37 年且可被利用的内核漏洞，削弱了&quot;仅靠严格的源码审计就能避免严重缺陷&quot;这一假设。此事对整个 BSD 家族以及任何复用数十年前 C 代码的项目都具有意义，也让人重新思考对继承而来的、长期被审查过的代码应给予多少信任。 据社区讨论，同样的缺陷代码在 NetBSD 于 1999 年 8 月对该部分进行重写时被&quot;意外&quot;修正，这意味着 NetBSD 是顺带规避了该问题，而 OpenBSD 则一直保留着它。评论者还争论自动化的模糊测试或静态分析是否真有可能发现这一类特定缺陷，还是说利用它必须依靠人类对底层漏洞原语的洞察。

hackernews · rs\_rs\_rs\_rs\_rs · 10月16日 14:44 · [社区讨论](https://news.ycombinator.com/item?id=50118977)

**背景**: OpenBSD 是 Theo de Raadt 于 1995 年从 NetBSD 1.0 分叉而来的、以安全为核心的开源类 Unix 操作系统，其代码源自伯克利软件发行版（BSD），强调可移植性、正确性、主动安全和集成密码学。模糊测试（fuzzing）是一种自动化测试技术，向程序输入非法、意外或随机数据并监控崩溃与内存错误；静态分析则在不运行程序的情况下检查源码，标记可疑模式。由于这两种手段在成熟内核上已是常规做法，这个漏洞能存活近四十年，正是该发现引人注目的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenBSD">OpenBSD - Wikipedia</a></li>
<li><a href="https://www.openbsd.org/faq/faq1.html">OpenBSD FAQ: Introduction to OpenBSD What Is OpenBSD? Everything You Need to Know - MUO What Is OpenBSD? Everything You Need to Know - The Tech Edvocate What Is OpenBSD? - Computer Hope What Is OpenBSD? – ITU Online IT Training</a></li>
<li><a href="https://en.wikipedia.org/wiki/Fuzzing">Fuzzing - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（162 分、46 条评论）总体持赞赏态度，有人称赞文章采用了 OpenBSD 发行版风格的配图，并打趣期待配套主题曲。一个关键的技术观察是：NetBSD 在 1999 年 8 月的一次重写中意外修复了同一个漏洞；而反复出现的争论焦点在于，模糊测试或静态分析是否真能发现这类漏洞，还是说它从根本上需要人类去思考漏洞利用原语。

**标签**: `#security`, `#openbsd`, `#kernel`, `#vulnerability-research`, `#exploit-development`

---

<a id="item-5"></a>
## [ORL 与 dlmrt：单张 RTX 5090 上扩散语言模型解码达 2,788 tokens/s](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 8.0/10

一个研究团队发布了面向扩散语言模型（dLLM）的训练方法 ORL（On-Policy Residual Learning，在策略残差学习）以及配套的自研推理引擎 dlmrt，声称在单张 RTX 5090 上以 LLaDA-2.1-mini + ORL 实现最高 2,788 tokens/s 的单请求解码，在 8 张 B200 上以 NVFP4 精度运行 DiffusionGemma 26B MoE + ORL 达到 7,708 tokens/s，并让 QwenDLM-4B 的端到端吞吐最高提升约 6.9 倍且质量相当或更好。他们还在单张 H100 的单请求对比中报告 QwenDLM-4B + ORL 达到 1,298 tokens/s，在实测精度相当时比 DFlash 投机解码快 1.74 倍，并远超 EAGLE3 的 405 tokens/s。模型、训练代码、评测流程和推理引擎均已完全开源。 扩散语言模型一直承诺可以并行生成多个 token，但在实际速度上很少真正超过自回归模型；ORL 配合 dlmrt 声称改变了这一点，不仅在速度上超过了成熟的投机解码方法，还能在消费级 Blackwell 显卡上高效运行。如果这些结果可复现，推理经济性可能会向扩散解码倾斜，并让单张消费级 GPU 上的高吞吐本地部署变得更加可行。 团队明确指出，所有数字都是在特定基准上的单请求解码（batch size 1）峰值结果，而非并发请求的聚合吞吐或任意提示下的平均值；LLaDA-2.1-mini 版本仅需 420 万个自生成训练 token 和 36 个 H100 GPU 小时的后训练，而 QwenDLM-4B 的 HumanEval pass@1 从 82.9% 提升到 89.6%。dlmrt 将整个去噪循环捕获进一个 CUDA graph 并在 GPU 上执行，避免逐步从 CPU 发起与同步，同时支持 Blackwell（含 RTX 5090）上的 NVFP4 推理，在相同模型和设置下于单张 H100 上比 SGLang/vLLM 快 1.2–1.6 倍。

reddit · r/MachineLearning · /u/arty\_photography · 10月16日 20:03

**背景**: 自回归大模型一次只生成一个 token，每输出一个 token 就需要一次前向计算；而扩散语言模型从被掩码或加噪的序列出发，通过迭代去噪并行地确定多个位置的内容，一次前向就能敲定多个 token。残差学习指的是模型把自己此前的预测作为上下文携带进来，并在多个去噪步中逐步精化；ORL 的关键洞见在于这一过程天然是“在策略”的——推理时遇到的残差状态由当前模型自身产生，因此用离线陈旧残差训练会产生不匹配。Adjacent Entropy Contraction 是一个辅助目标，要求每一个去噪步相对上一步降低不确定性；NVFP4 是 Nvidia Blackwell GPU 上可用的 4 比特浮点格式，而 DFlash 和 EAGLE3 则是用于加速传统自回归模型的投机解码方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2610.20687v1">On-Policy Residual Learning for Diffusion Language Models</a></li>
<li><a href="https://github.com/Introspective-Diffusion/ORL/blob/main/">ORL: On-Policy Residual Learning for Diffusion Language Models</a></li>

</ul>
</details>

**标签**: `#diffusion-llm`, `#llm-inference`, `#inference-optimization`, `#open-source`, `#nvfp4-quantization`

---

<a id="item-6"></a>
## [商务部拟对人工智能、生物医药、光伏技术出口实施临时登记](https://aqygzj.mofcom.gov.cn/flzc/gzjgfxwj/art/2026/art_c99f95ca0cd043829ac9991495fc283c.html) ⭐️ 8.0/10

商务部就修订《中国禁止出口限制出口技术目录》公开征求意见，涉及人工智能、生物医药、光伏三个领域的 40 项技术。其中人工智能领域包括大模型、智能体、算力集群、信息处理相关 23 项技术；生物医药领域包括细胞和基因治疗、小核酸药、病原微生物相关 5 项技术；光伏领域包括多晶硅制造、硅片制造、电池制造相关 12 项技术。 这是一项重要的监管动向，表明中国有意保护其在人工智能、生物科技和光伏供应链中的竞争优势，可能对全球技术合作与跨境授权交易造成冲击。此举将影响从中国获得技术授权的跨国企业、开展国际合作的科研人员，以及半导体、可再生能源和制药等领域的全球供应链。 该提案包含若干豁免条款：已通过开源、发表学术论文等方式进入公共领域的技术不纳入管理范围；对不涉及所有权转让的对外授权模式，适用自动许可等便利措施。光伏领域的管理范围也包含承载相关技术的关键和核心设备。

telegram · zaihuapd · 10月16日 09:12

**背景**: 出口管制目录决定了中国企业和个人在向境外转让哪些技术前必须获得政府批准，此类修订通常先公开征求意见再正式生效。此次涉及的三个领域都是中国已具备全球领先地位的行业——大语言模型与 AI 算力集群、下一代核酸药物，以及供应全球多数光伏组件的太阳能制造链。“临时登记”意味着在目录最终定稿前，先对这些技术实施一种较轻量、过渡性的管制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pubmed.ncbi.nlm.nih.gov/39309508/">Current status and trends in small nucleic acid drug ... - PubMed</a></li>
<li><a href="https://ayarlabs.com/glossary/ai-compute-cluster/">AI Compute Cluster Definition | Understanding AI Clusters</a></li>

</ul>
</details>

**标签**: `#China regulation`, `#export controls`, `#AI policy`, `#biotechnology`, `#photovoltaics`

---

<a id="item-7"></a>
## [法院文件曝光 Telegram 向美国执法部门提供用户数据](https://www.404media.co/heres-what-telegram-giving-data-to-the-u-s-government-looks-like/) ⭐️ 8.0/10

新公开的法院文件显示，Telegram 在回应美国法院命令时，向美国执法部门提供了一名用户的手机号、用户 ID 和 IP 地址，并在信函中称此举系「自愿」，同时不承认受美国司法管辖。截至今年 1 月，Telegram 已累计向美方提供了 2253 名用户的数据。 这一曝光与 Telegram 长期塑造的「隐私优先」形象形成强烈反差，也说明美国法院实际上能够从公开否认受其管辖的境外平台那里获取数据。这同时对其他通讯服务及其用户释放信号：无论公司对外姿态如何，服务器上保存的手机号、账号 ID 和 IP 等元数据仍可能被执法部门取得。 该请求涉及被控参与 2023 年 10 月 7 日袭击以色列事件的 Mahmoud Al-Muhtadi，所交出的手机号、用户 ID 和 IP 地址正是通讯服务商在服务器上保存的那类账号元数据。Telegram 的措辞值得注意：它把交出数据描述为「自愿」而非被迫，这种法律姿态可以避免承认美国法院命令对其具有约束力。

telegram · zaihuapd · 10月16日 14:57

**背景**: Telegram 是由 Pavel Durov 创立的通讯应用，长期以隐私保护和不受多数国家政府触及为卖点，尽管其标准的云端聊天并非端到端加密。美国法院可通过所谓「长臂管辖权」将司法管辖延伸至境外的被告，只要该被告与管辖地存在「最低限度联系」。404 Media 是一家独立科技调查媒体，由前 Motherboard 记者于 2023 年创办，以发布泄露文件和调查报道著称。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/%E9%95%BF%E8%87%82%E7%AE%A1%E8%BE%96%E6%9D%83">长臂管辖权 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.kangdalawyers.com/library/834.html">从中兴、华为事件看美国法律的长臂管辖原则</a></li>
<li><a href="https://www.404media.co/">404 Media</a></li>

</ul>
</details>

**标签**: `#Telegram`, `#隐私`, `#数据披露`, `#政府监控`, `#科技政策`

---

<a id="item-8"></a>
## [Anthropic IPO 估值预期据报下调至 1.5 万亿美元](https://www.reuters.com/business/finance/investors-temper-anthropic-ipo-valuation-expectations-over-revenue-growth-2026-10-15/) ⭐️ 8.0/10

据路透社报道，部分投资者已将 Anthropic 首次公开募股的估值预期从约 2 万亿美元下调至约 1.5 万亿美元。此次下调发生在 Anthropic 第三季度营收达 168 亿美元、环比增长 45%、实现经调整后盈利且季度现金流转正的背景之下。 作为全球最大的非上市 AI 模型开发商之一，Anthropic 估值预期的下调可能成为整个行业的“压力测试”，并压低其他 AI 公司的估值。报道明确指出，智谱、MiniMax、月之暗面的 Kimi 以及 DeepSeek 等中国 AI 公司将面临考验，市场关注点将转向收入可持续性、毛利率和资本效率。 下调原因主要有三：增速放缓、前沿模型之间的价格竞争加剧，以及算力投入带来的沉重资本开支压力。值得注意的是，即便公司据报已实现经调整后盈利且现金流转正，估值预期依然被下调，这说明投资者折价的是未来增长预期，而非当前的财务健康度。

telegram · zaihuapd · 10月16日 15:46

**背景**: Anthropic 是一家以 Claude 系列大语言模型著称的 AI 公司，是 OpenAI 的主要竞争对手之一。IPO（首次公开募股）指非上市公司在证券交易所挂牌发行股票的过程，而估值预期反映的是投资者认为公司上市时值多少钱。该行业的估值主要由收入增长轨迹、模型定价能力，以及训练和推理所需的 GPU 与数据中心成本决定。路透社将此事的参照对象列为智谱、MiniMax、Kimi（月之暗面）和 DeepSeek 等中国模型公司，它们同样是潜在的上市或融资主体。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/%E6%99%BA%E8%B0%B1">智谱 - 维基百科，自由的百科全书</a></li>
<li><a href="https://duoke360.com/post/46091">MiniMax 大 模 型 简 介 - 多课网</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#IPO`, `#AI industry`, `#valuation`, `#market analysis`

---