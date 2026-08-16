---
layout: default
title: "Horizon Summary: 2026-08-16 (ZH)"
date: 2026-08-16
lang: zh
---

> 从 32 条内容中筛选出 7 条重要资讯。

---

1. [Anthropic 公开 Claude 系统提示词，引发技术分析与社区热议](#item-1) ⭐️ 8.0/10
2. [Cloudflare 在切换 DNS 后静默注入分析脚本](#item-2) ⭐️ 8.0/10
3. [Qwen 3.8 27B 表现出色但默认过度思考](#item-3) ⭐️ 8.0/10
4. [阿莫迪：公众对 AI 的不信任源于机构信任危机](#item-4) ⭐️ 8.0/10
5. [PJM 建模失误浪费 120 亿美元，改革或重蹈覆辙](#item-5) ⭐️ 8.0/10
6. [Reddit 文章质疑 ECA-Net 的跨通道交互假设](#item-6) ⭐️ 8.0/10
7. [Anthropic 第二季营收暴涨 14 倍至逾 115 亿美元，IPO 在即](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 公开 Claude 系统提示词，引发技术分析与社区热议](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 8.0/10

Anthropic 在官方 Claude 平台发布说明页面公开了 Claude 模型的详细系统提示词（system prompts），按模型版本列出带日期的条目，并用加粗标出版本间改动。这一举措首次让原本不公开的内部指令集可以被外部查看。 系统提示词通常是不公开的，因此这次透明度提升让开发者、研究者和用户能够检查塑造 Claude 行为的实际指令，有助于更深入的安全分析和提示工程。这也树立了一个先例，可能促使其他 AI 厂商更开放地披露系统指令。 文档说明这些系统提示会定期更新以改进 Claude 的回复，但更新不适用于 Claude API；从 Claude 4.6 代开始，每个模型 ID 是一个单一固定快照，因此只有一个条目。文档中版本间改动以加粗显示，社区成员 Simon Willison 还制作了 git 提交历史，方便对比差异。

hackernews · tosh · 8月16日 12:48 · [社区讨论](https://news.ycombinator.com/item?id=49319556)

**背景**: 系统提示词有时也被称为系统消息，是在 AI 模型与用户交互前提供的预定义指令，相当于模型的行为准则。它们影响模型的行为，包括安全约束、语气以及如何处理任务。过去厂商很少公开这些提示词，而提示工程——通过设计输入来引导模型输出的实践——已成为一个重要领域。公开提示词让外部人士能够分析驱动已部署模型的具体指令。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/release-notes/system-prompts">System Prompts - Claude Platform Docs - Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prompt_engineering">Prompt engineering</a></li>
<li><a href="https://thebrainyacts.beehiiv.com/p/225-ask-ai-vendor-system-prompts">225 | Ask your AI vendor for their system prompts</a></li>

</ul>
</details>

**社区讨论**: Simon Willison 在评论区分享了自己构建的 git 提交历史，用来追踪提示词变化，并指出 Opus 4.8 与 Opus 5 之间的差异，提到了新增的&quot;Claude Fable 5&quot;和&quot;Claude Mythos 5&quot;等名称。另有评论者认为，明确写出&quot;检查图片是否存在&quot;这类常识性规则，说明模型&quot;智能&quot;可能有限；还有用户表达了对论坛首页移除负面 AI 报道的担忧。

**标签**: `#AI`, `#Claude`, `#system-prompts`, `#Anthropic`, `#prompt-engineering`

---

<a id="item-2"></a>
## [Cloudflare 在切换 DNS 后静默注入分析脚本](https://news.ycombinator.com/item?id=49322107) ⭐️ 8.0/10

一位用户发现，在将域名服务器切换到 Cloudflare 以启用 R2 存储桶服务后，Cloudflare 静默向其纯 HTML、无 JavaScript 的网站注入了分析脚本片段。用户不得不在 Analytics 控制台中手动关闭该功能，而不是主动选择开启。 这一做法引发了关于 Cloudflare 默认开启分析注入的透明度和隐私担忧，可能会让只想使用 DNS 或代理服务的用户感到意外。这可能削弱用户信任，并促使他们转向尊重主动同意原则的替代服务。 这种注入似乎只在 Cloudflare 作为代理（橙色云图标）时发生，而仅在 DNS 模式下不会出现。用户可以通过 Content-Security-Policy 请求头阻止该脚本，或在 Cloudflare 控制台中停用 Web Analytics。

hackernews · stagas · 8月16日 17:49

**背景**: Cloudflare 是一家主要的 CDN 和云服务提供商，其 Web Analytics 产品是免费的隐私优先分析工具。当网站通过 Cloudflare 代理时，默认会从 static.cloudflareinsights.com 注入一段 JavaScript beacon 脚本来收集访问者统计信息。用户需要在控制台中手动禁用这一功能，这正是用户认为具有侵犯性的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.cloudflare.com/web-analytics/about/">Cloudflare Web Analytics · Cloudflare Web Analytics docs</a></li>
<li><a href="https://www.cloudflare.com/web-analytics/">Cloudflare Web Analytics</a></li>

</ul>
</details>

**社区讨论**: 评论者确认了这一问题，并指出注入的脚本带有完整性哈希。有人指出这种注入只在启用 Cloudflare 代理时发生，而 DNS-only 模式不会，另一些人建议使用 Content-Security-Policy 请求头作为替代方案。

**标签**: `#cloudflare`, `#privacy`, `#analytics`, `#dns`, `#web`

---

<a id="item-3"></a>
## [Qwen 3.8 27B 表现出色但默认过度思考](https://simonwillison.net/2026/Aug/16/qwen-38-27b/) ⭐️ 8.0/10

阿里巴巴 Qwen 实验室发布了 Qwen 3.8 27B，这是一款采用 Apache-2.0 许可的 27B 参数视觉语言模型，据称性能超越其前代和闭源的 Qwen 3.7-Plus。Simon Willison 发现该模型能生成令人惊艳的内容（如漂亮的鹈鹕 SVG 图像），但其默认的 xhigh 推理强度会导致严重的过度思考，生成一张简单图片竟耗时 21 分钟。 27B 参数规模非常适合在消费级笔记本电脑和单 GPU 上运行，而且 Apache 2.0 许可证使其可以自由使用。默认的过度思考问题突显了本地 LLM 部署中的一个关键可用性问题——用户必须主动降低推理强度，才能在质量、速度和成本之间取得平衡。 该模型默认采用 reasoning\_effort=xhigh，在 LM Studio 的 8,192 token 默认上下文窗口中处理简单提示词时，整个上下文都会被耗尽；需要将其扩展到完整的 262,144 token 才能解决问题。一个示例消耗了 22,276 个推理 token 和 3,223 个输出 token，作者在 MacBook Pro 和 NVIDIA DGX Spark 上运行的是 17GB 的 Q4\_K\_M 量化版本。

rss · Simon Willison · 8月16日 22:00

**背景**: Qwen 是阿里巴巴的开源 LLM 研究实验室，以发布有竞争力的开放权重模型而闻名。推理强度（reasoning effort）是一种控制模型使用多少思维链的机制，像 xhigh 这样的高设置旨在应对复杂任务，但在简单问题上容易导致过度思考。27B 参数规模是本地硬件部署的甜点区间，在 4-bit 量化下大约需要 16GB 显存；这类视觉语言模型还可以处理图像和视频。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-27B">Qwen/Qwen3.8-27B · Hugging Face</a></li>
<li><a href="https://arxiv.org/pdf/2510.07880">Do LLMs Really Need 10+ Thoughts for &quot;Find the Time 1000 Days...&quot;</a></li>
<li><a href="https://www.yottalabs.ai/post/qwen-3-8-27b-specs-hardware-requirements-how-to-run-2026">Qwen 3.8 27B: Specs, Hardware Requirements, and How to Run It (2026) | Yotta Labs</a></li>

</ul>
</details>

**标签**: `#qwen`, `#llm`, `#open-source`, `#benchmark`, `#reasoning`

---

<a id="item-4"></a>
## [阿莫迪：公众对 AI 的不信任源于机构信任危机](https://simonwillison.net/2026/Aug/16/dario-amodei/) ⭐️ 8.0/10

在 2026 年 8 月 16 日被 Simon Willison 引用的推文中，Anthropic CEO Dario Amodei 认为，公众对 AI 的负面看法主要源于对机构深层次的信任危机，而非 AI 领袖的风险警告。他表示，花哨的正面营销并非解决办法，只有像真正治愈癌症这样的实际成就才能赢回信任。 Amodei 是 AI 领域的领军人物，他的评论同时反驳了行业内“风险警告”和“营销包装”两种叙事。这凸显了 AI 公司面临的问责挑战：要想化解公众怀疑，关键不是宣传话术，而是切实兑现惠及世界的实际利益。 Amodei 特别批评了有人建议 Anthropic 开展华丽营销活动的做法，认为“AI 将治愈癌症”已成陈词滥调，多数人会视其为欺骗。他还指出，对 AI 公司（包括 Anthropic）最准确的批评是：它们尚未兑现惠及世界的重大承诺。

rss · Simon Willison · 8月16日 15:05

**背景**: Dario Amodei 是 Anthropic 公司的 CEO，该公司开发了 Claude AI 助手。这番言论出现在公众激烈争论 AI 风险与益处的背景之下，许多人担心失业、偏见、虚假信息以及生存性安全问题。Amodei 的观点将焦点从风险沟通转向信任与兑现承诺，暗示科技行业长期以来一边承诺创新、一边又时有辜负用户信任的做法，已经让公众对任何 AI 宣传都心存怀疑。

**标签**: `#AI`, `#Anthropic`, `#public trust`, `#AI safety`, `#tech industry`

---

<a id="item-5"></a>
## [PJM 建模失误浪费 120 亿美元，改革或重蹈覆辙](https://newsletter.semianalysis.com/p/12b-of-us-ratepayers-money-wasted) ⭐️ 8.0/10

SemiAnalysis 的一篇文章指出，PJM Interconnection 对其容量市场的错误建模浪费了美国纳税人 120 亿美元。PJM 目前正提议新的容量市场改革，批评者警告称这可能会重蹈建模失误的覆辙。 此事意义重大，因为它暴露了美国最大电力市场在可靠性规划方面存在的系统性缺陷，直接影响数百万纳税人。如果 PJM 重蹈覆辙，未来的容量拍卖可能继续向消费者多收费，同时又无法确保电网可靠性。 $120 亿这个数字与 PJM 的可靠性定价模型（RPM）相关，该模型提前三年向发电商支付费用，以换取其供电承诺。面对日益增长的需求和外界审视，PJM 提出了三种改革容量市场的总体框架，包括稳定现有的 RPM。

rss · Semianalysis · 8月16日 22:27

**背景**: PJM Interconnection 运营着美国最大的电力市场，服务 13 个州和数百万消费者。其容量市场“可靠性定价模型”旨在通过提前三年向发电商支付费用，以换取其发电（或削减需求）的承诺，从而确保电网的长期可靠性。批评者认为，PJM 的规划短板、市场设计失败和治理问题导致了电价上涨和纳税人资金浪费。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/PJM_Interconnection">PJM Interconnection - Wikipedia</a></li>
<li><a href="https://marylandmatters.org/2024/09/02/market-problems-poor-planning-cause-price-hikes-in-nations-largest-electric-market-critics-say/">Market problems, poor planning cause price hikes... - Maryland Matters</a></li>
<li><a href="https://www.linkedin.com/posts/nania-energy_pjm-floats-options-for-capacity-market-overhaul-activity-7460064337202925568-gH3K">PJM Interconnection considers market changes for... | LinkedIn</a></li>

</ul>
</details>

**标签**: `#energy grid`, `#PJM`, `#modeling`, `#ratepayers`, `#capacity market`

---

<a id="item-6"></a>
## [Reddit 文章质疑 ECA-Net 的跨通道交互假设](https://www.reddit.com/r/MachineLearning/comments/1vptaw9/revisiting_the_efficient_channel_attention_paper/) ⭐️ 8.0/10

一篇 Reddit 帖子重新审视了 ECA 论文，认为其核心假设——跨通道交互至关重要——与实验结果相矛盾：k=1（无交互）的表现几乎与 k=3 相当。作者使用国际象棋残局库数据指出，在通道维度上进行一维卷积在概念上是一种“被诅咒的卷积”，因为通道之间没有内在拓扑结构。 ECA 是一个被广泛引用（12,000 次）且广泛使用的注意力模块，能以极少的参数提升 CNN 性能。这一批评挑战了该热门技术的理论基础，可能影响实践者对通道注意力模块的理解与设计。 作者的象棋残局库实验中，k=3 的 ECA 达到 96.68% 准确率，k=1 为 96.61%，而中心掩码的 k=3 变体为 96.63%——表明局部交互并非关键因素。作者认为，CNN 在类似表格数据的通道上仍可通过初始 1x1 投影重排通道来学习，但这样做效率低下。

reddit · r/MachineLearning · /u/arkuto · 8月16日 10:13

**背景**: 像 Squeeze-and-Excitation（SE）这样的通道注意力机制会对特征图通道之间的相互依赖关系建模。ECA-Net 提出了一种高效通道注意力模块，对通道平均特征使用一维卷积来捕获局部跨通道交互，而无需降维。卷积假设局部性和平移不变性，这对空间/图像数据成立，但对任意排列的通道列表并不成立。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/1910.03151">[1910.03151] ECA-Net: Efficient Channel Attention for Deep ... ECA-Net: Efficient Channel Attention for Deep Convolutional ... ECA-Net: Efficient Channel Attention for Deep Convolutional ... (PDF) ECA-Net: Efficient Channel Attention for Deep ... Paper page - ECA-Net: Efficient Channel Attention for Deep ... ECA-Net: Efficient Channel Attention - GitHub CVPR 2020 Open Access Repository</a></li>
<li><a href="https://openaccess.thecvf.com/content_CVPR_2020/papers/Wang_ECA-Net_Efficient_Channel_Attention_for_Deep_Convolutional_Neural_Networks_CVPR_2020_paper.pdf">ECA-Net: Efficient Channel Attention for Deep Convolutional ...</a></li>

</ul>
</details>

**标签**: `#deep learning`, `#attention mechanisms`, `#research critique`, `#efficiency`, `#neural networks`

---

<a id="item-7"></a>
## [Anthropic 第二季营收暴涨 14 倍至逾 115 亿美元，IPO 在即](https://www.cnbc.com/2026/08/15/anthropic-revenue-jumps-to-over-11point5-billion-in-q2-report.html) ⭐️ 8.0/10

Anthropic 第二季度初步营收超过 115 亿美元，是去年同期的 7.87 亿美元的 14 倍多，也高于 2026 年第一季度的 47.3 亿美元。该公司当季调整后营业利润也已转正。 这一里程碑突显了 Anthropic 作为领先 AI 公司在商业化上的迅猛成功，也印证了企业对其 AI 模型的强劲需求。同时，这为最早可能于今年秋季启动的大型首次公开募股（IPO）铺平了道路，反映出整个 AI 行业的强劲势头。 这些营收数字为初步数据，仍可能进行调整。据 CNBC 援引彭博社的文件报道，Anthropic 正在筹备可能于今年秋季启动的大型 IPO。

telegram · zaihuapd · 8月16日 07:26

**背景**: Anthropic 是一家以开发 Claude 系列大语言模型而闻名的 AI 安全与研究公司。其营收的快速增长反映了生成式 AI 在各行各业的广泛采用。调整后营业利润转正通常被视为公司上市前的重要一步，因为它向潜在投资者传递了财务可持续性的信号。

**标签**: `#Anthropic`, `#AI`, `#revenue`, `#IPO`, `#tech-business`

---