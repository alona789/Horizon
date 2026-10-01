---
layout: default
title: "Horizon Summary: 2026-10-01 (ZH)"
date: 2026-10-01
lang: zh
---

> 从 34 条内容中筛选出 6 条重要资讯。

---

1. [谷歌发布前沿模型 Gemini 4 Argon](#item-1) ⭐️ 9.0/10
2. [EDG 在公司停运之际将其历史悠久的商业 C++ 前端开源](#item-2) ⭐️ 8.0/10
3. [DeepSeek 开源华为昇腾全套基础软件栈](#item-3) ⭐️ 8.0/10
4. [Cloudflare 宣布进军公共证书颁发机构](#item-4) ⭐️ 8.0/10
5. [Kimi K3 经 Baseten 接入 OpenAI Codex 企业付费通道](#item-5) ⭐️ 8.0/10
6. [Reddit 将停用 RSS 订阅并关闭公开 API](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [谷歌发布前沿模型 Gemini 4 Argon](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/) ⭐️ 9.0/10

谷歌发布了新一代前沿模型 Gemini 4 Argon，定位高于 9 月推出的 Gemini 3.8 系列，主要面向真实世界编程、企业知识工作（如法律类任务）和网络防御三大领域，并计划很快向开发者、企业和消费者开放。该消息在 Hacker News 上获得 984 分和 666 条评论，同时还有一篇关于其智能水平、性能与价格的分析文章。 Argon 是谷歌迄今最先进的模型，也标志着前沿实验室之间又一轮快速交替超越；这被越来越多的人视为 AI 能力正在向超大规模云厂商、新型云服务商和初创公司扩散，而非集中于单一“赢家通吃”的领导者。它向智能体编程与网络防御领域的推进，也显示出大型厂商认为企业价值的下一个落点在哪里。 谷歌表示会在向开发者、企业和消费者开放之前，继续从早期测试者那里收集反馈并迭代护栏机制，这一点被批评为“模型还没能真正发布就先宣布”；博客中还提到 Argon 智能体正在谷歌内部把 C/C++ 代码库迁移到 Rust。

hackernews · bradleyg223 · 9月30日 20:04 · [社区讨论](https://news.ycombinator.com/item?id=49913571)

**背景**: Gemini 是谷歌的大语言模型系列，每一代命名版本（此前的 Gemini 3.8 系列和如今的 Gemini 4 Argon）通常都意味着在推理、编程和长周期任务能力上的提升。所谓“智能体编程”，指 AI 系统在项目层面而非文件层面工作：它会阅读配置文件和测试文件、追踪依赖关系，并在较少人工干预下完成多步开发任务。与 Anthropic 首席执行官 Dario Amodei 相关的“集中化（concentrating）”论认为，AI 是赢家通吃的领域，先取得领先的一方不会把优势交还出去。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/">Introducing Gemini 4 Argon - The Keyword</a></li>
<li><a href="https://www.cnbc.com/2026/09/30/google-gemini-4-argon-ai.html">Google rolls out Gemini 4 Argon, its most advanced model - CNBC</a></li>
<li><a href="https://www.datacamp.com/blog/gemini-4-argon">Gemini 4 Argon: Benchmarks, Pricing, and Access | DataCamp</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对模型的智能体能力印象深刻——有人回忆 Gemini 3.8 Flash 曾把 GDB 附加到 GPU 驱动上、逆向工程内核队列 ioctl 接口，并编写 LD\_PRELOAD 垫片让 ROCm 版 llama.cpp 在 Strix Halo 机器上跑通。不少人借这次发布反驳 Amodei 的赢家通吃论，指出如今 AI 能力更分散于新型云、超大云厂商、GPU 与 ASIC 阵营以及初创公司之间；也有人批评谷歌“先宣布再发布”（“发布不了模型的指控”），并建议开发者保持模型与供应商可替换，让智能真正变成商品。

**标签**: `#AI/ML`, `#Google Gemini`, `#LLM`, `#Model Release`, `#Industry Analysis`

---

<a id="item-2"></a>
## [EDG 在公司停运之际将其历史悠久的商业 C++ 前端开源](https://edgcpp.org/#transition) ⭐️ 8.0/10

长期开发商业 C++ 编译器前端的 Edison Design Group（EDG）已在 GitHub（github.com/edgcpp/compiler）上将其 C++ 前端开源，公告发布于 edgcpp.org。此举似乎与公司即将停运有关，而代码库的历史最早可追溯到 1990 年的提交记录。 EDG 的前端因其严谨的标准符合性而广受认可，并被授权给其他商业编译器与分析工具使用，因此这次开源为整个 C++ 生态提供了一个此前只能通过商业授权获得的、经过实战检验的解析器与语义分析器。由于公司正在停运，此举可能保住了一项许多工具历来依赖的关键编译器基础设施。 该仓库采用 Apache-2.0 WITH LLVM-exception 许可证，源码保留了自 1990 年以来的完整版本历史，评论者指出这对一次开源事件而言十分罕见。该前端支持到 C++17 的 ISO C++ 标准（C++20 特性仍在开发中），还可配置为支持 ANSI/ISO C 以及微软的语言扩展。

hackernews · iandinwoodie · 9月30日 19:26 · [社区讨论](https://news.ycombinator.com/item?id=49913192)

**背景**: 编译器前端是编译器中与语言相关的那一部分，负责对源代码进行预处理、解析和分析，将其转换为与目标机器无关的中间表示，之后再交由后端阶段生成目标代码。EDG（Edison Design Group）打造的 C++ 前端是最知名的商业前端之一，被广泛用于其他编译器与代码分析工具中，尤其值得注意的是它充当了 Visual C++ IntelliSense 的解析引擎，尽管 Visual C++ 实际生成代码时用的是 MSVC 编译器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Edison_Design_Group">Edison Design Group - Wikipedia</a></li>
<li><a href="https://www.edg.com/c">The C++ Front End - edg.com</a></li>
<li><a href="https://jszhn.github.io/brain/Compiler-front-end">Compiler front - end</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为这是 C++ 领域的一件大事，其中 jabl 指出公告未提及公司停运这一可能的动机。其他人从实用角度展开讨论：badsectoracula 猜测能否利用其源到源编译能力把 C++ 库转译成像 Free Pascal 这样的语言，vintagedave 提到 EDG 前端正是 Visual C++ IntelliSense 背后的引擎，而 trebligdivad 则感叹这样能追溯到 1990 年的提交历史在开源发布中实属罕见。

**标签**: `#C++`, `#compilers`, `#open-source`, `#EDG`, `#tooling`

---

<a id="item-3"></a>
## [DeepSeek 开源华为昇腾全套基础软件栈](https://mp.weixin.qq.com/s/X41mKH4Ds-VXUAnK6M8Eww) ⭐️ 8.0/10

DeepSeek 开源了面向华为昇腾平台的一整套基础组件，包括 TileLang 高级语言编译工具、计算库与分布式通信库，以及 DeepGEMM Ascend、DeepEP Ascend、TileKernels、FlashMLA 和 DeepSelect 等昇腾版本。DeepSeek 表示这些组件在多项测试中性能接近硬件上限，并正与华为推进昇腾 950 的 128 卡超节点方案。 这相当于把 DeepSeek 面向英伟达的整套工具链复刻到了华为芯片上，是从“零散移植”走向“可用的非英伟达生态”的重要一步。如果接近硬件上限的性能说法成立，将显著降低把 DeepSeek 系列模型与工具迁移到昇腾 NPU 的成本，也会增强国内实验室与企业采用国产 AI 硬件的信心。 DeepGEMM 的昇腾移植版号称与原版完全 API 兼容，支持 BF16、FP8、FP4 精度的 GEMM 以及 MQA logits，并采用 MIT 许可证；TileLang 则是一种可组合的 tile 编程模型，将数据流与调度解耦，让开发者可以把大部分优化工作交给编译器。由于保留了原有 API 形态，基于 DeepGEMM 接口编写的既有代码在迁移到昇腾 NPU 时仍可沿用相同的开发流程。

telegram · zaihuapd · 9月30日 03:09

**背景**: 华为昇腾 NPU 是国产 AI 芯片的代表，被视为英伟达 GPU 的主要替代方案，但其软件生态长期落后于 CUDA，导致现代大模型训练与推理负载很难迁移过去。DeepSeek 此前发布的 DeepGEMM（高效 GEMM 算子，尤其是 FP8 精度）、DeepEP（面向 MoE 模型的专家并行通信库）和 FlashMLA（支撑 DeepSeek-V3 的优化多头潜在注意力算子）都是为英伟达硬件打造的，而 TileLang 是用于编写这类 AI 算子的高层 tile DSL。此次推出昇腾版本，意味着 DeepSeek 训练和部署模型所依赖的整套软件层，如今在国产芯片上也有了对应实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/DeepGEMM-Ascend">GitHub - deepseek-ai/ DeepGEMM - Ascend : DeepGEMM - Ascend ...</a></li>
<li><a href="https://arxiv.org/abs/2504.17577">[2504.17577] TileLang: A Composable Tiled Programming Model ...</a></li>
<li><a href="https://github.com/deepseek-ai/FlashMLA">GitHub - deepseek-ai/ FlashMLA : FlashMLA : Efficient Multi-head...</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#Huawei Ascend`, `#open-source`, `#AI infrastructure`, `#distributed training`

---

<a id="item-4"></a>
## [Cloudflare 宣布进军公共证书颁发机构](https://blog.cloudflare.com/cloudflare-certificate-authority/) ⭐️ 8.0/10

Cloudflare 宣布计划成为公共证书颁发机构，已申请加入 Chrome、Apple、Microsoft 和 Mozilla 的根证书计划，并与 GlobalSign 签署协议收购一个被广泛信任的根证书。该公司目前尚未开始签发证书，但表示将优先支持基于 ACME 的自动签发与续期，并计划在 2027 年第一季度签发生产级默克尔树证书（MTC），以服务后量子互联网。 作为主要的 CDN 与安全厂商，Cloudflare 进入公共 CA 市场可能重塑长期由少数商业机构和非营利组织主导的 PKI 行业格局，也让它有机会把 ACME 优先的自动化流程和后量子证书格式直接推进 WebPKI 的信任存储中。未来托管在 Cloudflare 网络上的网站或许可以直接在该平台上获得证书，从而加深它与整个 TLS 生态的整合。 Cloudflare 在信任基础上并非从零开始：与 GlobalSign 的协议让它获得一个已被广泛信任的根证书，这可以缩短新 CA 通常需要经历的多年审计与浏览器审查流程。其最受关注的技术承诺是默克尔树证书（MTC）——一种旨在让后量子认证足够轻量、适合互联网使用的拟议证书格式，目标是在 2027 年第一季度实现生产级签发。

telegram · zaihuapd · 9月30日 06:26

**背景**: 证书颁发机构（CA）是指其根证书被内置于浏览器和操作系统的机构，从而能够通过 TLS 为网站身份背书。要获得这一地位，CA 必须通过审计并被 Chrome、Apple、Microsoft、Mozilla 等厂商运营的根证书计划接纳。ACME 是业界标准协议，最初为 Let&\#x27;s Encrypt 设计，用于自动完成证书签发与续期；而默克尔树证书（MTC）则是一项较新的提案，旨在让体积大得多的后量子签名方案在公共互联网上具备实用性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automatic_Certificate_Management_Environment">Automatic Certificate Management Environment - Wikipedia</a></li>
<li><a href="https://www.sectigo.com/blog/what-are-merkle-tree-certificates-mtcs">What are Merkle Tree Certificates (MTCs)? | Sectigo® Official</a></li>
<li><a href="https://www.ssl.com/article/what-are-root-certificates-and-why-do-they-matter/">What are Root Certificates , and Why Do They Matter? - SSL.com</a></li>

</ul>
</details>

**标签**: `#PKI`, `#TLS`, `#Cloudflare`, `#Post-Quantum`, `#ACME`

---

<a id="item-5"></a>
## [Kimi K3 经 Baseten 接入 OpenAI Codex 企业付费通道](https://36kr.com/newsflashes/4005691489112198) ⭐️ 8.0/10

美国 AI 基础设施公司 Baseten 宣布，企业用户现在可以在 OpenAI 的编程工具 Codex 中使用 Kimi K3，相关调用费用直接计入企业已有的 OpenAI 采购承诺额度，而无需走新增供应商的采购流程。据报道，这是中国开源模型首次进入 OpenAI 的企业付费结算通道。 如果消息属实，这表明企业 AI 采购正在结算层面走向“模型无关”：买家可以把任务交给中国开源模型，却不必新开一套供应商关系，从而大幅降低采用门槛。这也说明 OpenAI 的企业通道愿意充当第三方模型的结算层，标志着相互竞争的模型生态在商业层面的互操作出现了值得关注的变化。 据报道，这一安排是由推理基础设施提供商 Baseten 承接，而非 Kimi 与 OpenAI 的直接集成，其关键便利之处在于费用可以直接复用企业已有的 OpenAI 采购承诺额度。Kimi K3 本身是一款 2.8T 参数的开源模型，采用 Kimi Delta Attention 与 Attention Residuals 架构，原生支持视觉理解，拥有 100 万 token 上下文窗口，主要面向长周期编程与知识型工作。

telegram · zaihuapd · 9月30日 11:23

**背景**: Baseten 是一家美国 AI 推理基础设施公司，帮助企业将模型部署并服务于生产环境；它近期完成了 3 亿美元的成长型融资，投后估值约 50 亿美元，并通过收购 Blaxel 向智能体沙箱方向扩张。OpenAI Codex 是 OpenAI 面向开发者的编程工具，而大型企业通常通过“承诺消费”（committed spend）协议采购 OpenAI 算力，这类额度类似于必须在合约期内用完的预付信用。Kimi K3 是中国月之暗面（Moonshot AI）最新的旗舰开源模型，其 Kimi 系列因编程与智能体任务能力在海外获得了越来越多的关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kimi.ai/zh-hans/ai-models/kimi-k3">Kimi K3：2.8T 开放模型，适合编程与知识工作</a></li>
<li><a href="https://www.baseten.co/">Inference Platform: Deploy AI models in production | Baseten</a></li>
<li><a href="https://finance.huanqiu.com/article/4TQj8f3mzIJ">中国开源模型首次进入 OpenAI 企 业 客户 采 购 体 系 | 环球网</a></li>

</ul>
</details>

**标签**: `#AI`, `#Kimi K3`, `#OpenAI Codex`, `#Enterprise AI`, `#China LLM`

---

<a id="item-6"></a>
## [Reddit 将停用 RSS 订阅并关闭公开 API](https://techcrunch.com/2026/09/30/reddit-is-killing-rss-feeds-ending-public-api-access-because-of-ai-bots/) ⭐️ 8.0/10

Reddit 宣布将于 2026 年 11 月 13 日停止 RSS 订阅支持，并计划在 2027 年 3 月关闭公开 API 访问，理由是其已成为大规模抓取和自动化滥用（尤其是 AI 机器人）的常见渠道。第三方应用与机器人开发者必须在 2027 年 1 月 12 日前完成注册，否则将被移除 API 访问权限；同时 Reddit 建议版主改用 Discord Relay 替代原有基于订阅源的工作流。 这是全球最大用户生成内容平台之一对公开数据访问的又一次重大收紧，延续了 Reddit 在 2023 年 API 定价风波后的路线。它直接冲击依赖 Reddit 讨论数据的第三方客户端开发者、研究人员、网络存档者以及 AI/ML 团队，也印证了平台在限制开放访问的同时通过授权协议将数据变现的整体趋势。 RSS 支持将在 2026 年 11 月 13 日终止，公开 API 则定于 2027 年 3 月关闭，开发者须在 2027 年 1 月 12 日前完成注册。值得注意的是，关闭公开 API 并不意味着商业用途被完全禁止——希望将 Reddit 数据用于商业目的的组织预计需要与公司另行签署授权协议。

telegram · zaihuapd · 10月1日 00:27

**背景**: RSS（简易资讯聚合）是一种历史悠久的开放格式，网站借此以机器可读的订阅源发布更新，让阅读器和工具无需逐一访问网站就能自动获取新内容。公开 API 则是官方开放的编程接口，允许外部程序以程序化方式读取平台数据，长期以来第三方 Reddit 客户端、研究数据集和数据管道大多依赖它运行。Reddit 早在 2023 年推出付费 API 定价、导致多个热门第三方应用关停时就曾引发广泛批评。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.lavx.hu/zh-Hans/article/reddit-guan-bi-rss-ding-yue-yuan-she-ding-2027-nian-wei-gong-gong-api-guan-ting-de-zui-hou-qi-xian">Reddit 关闭 RSS 订阅源，设定 2027 年为公共 API 关停的最后期限 | L...</a></li>
<li><a href="https://www.digitaltoday.co.kr/cn/view/109373/reddit-to-end-rss-support-in-november-public-api-to-stop-in-march-2027">Reddit将于11月13日停止RSS支持 开放API拟于2027年3月关闭</a></li>
<li><a href="https://zh.wikipedia.org/zh-hans/RSS">RSS - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**标签**: `#Reddit`, `#API deprecation`, `#RSS`, `#AI scraping`, `#platform policy`

---