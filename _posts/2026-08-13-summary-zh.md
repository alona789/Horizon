---
layout: default
title: "Horizon Summary: 2026-08-13 (ZH)"
date: 2026-08-13
lang: zh
---

> 从 34 条内容中筛选出 9 条重要资讯。

---

1. [谷歌发布 Gemini 3.7 Flash 高效 AI 模型](#item-1) ⭐️ 9.0/10
2. [用&\#x27;意面化&\#x27;DRAM 技术解锁 CPU 隐藏区域](#item-2) ⭐️ 9.0/10
3. [DeepMind 手语转文字模型 SL2T 落地 Pixel 11](#item-3) ⭐️ 9.0/10
4. [DeepSeek-V4-Pro 正式版上线，API 实行峰谷定价](#item-4) ⭐️ 9.0/10
5. [Cerebras 与 OpenAI 推出 GPT-5.6 Sol 超快模式，HLE 测试提速近 7 倍](#item-5) ⭐️ 8.0/10
6. [DeepSeek Harness 开发者预览版：开源智能体执行框架](#item-6) ⭐️ 8.0/10
7. [选择无聊技术：把创新代币留给真正的问题](#item-7) ⭐️ 8.0/10
8. [Worldproof 工具揭示像素指标常常无法区分世界模型优劣](#item-8) ⭐️ 8.0/10
9. [特朗普签署备忘录，允许私企开展政府背书的海外网络攻击](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [谷歌发布 Gemini 3.7 Flash 高效 AI 模型](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 9.0/10

谷歌正式发布 Gemini 3.7 Flash，这是一款面向高频、低成本场景的高效 AI 模型。社区实测显示其在图像转 HTML 任务中表现出色，但价格策略引发争议。 Gemini 3.7 Flash 提升了谷歌“工作马”级模型的能力，让先进多模态推理更易获得且成本更低。在 OpenAI Luna 等竞争对手采取激进定价的背景下，这增强了谷歌在 AI 模型市场的竞争力。 谷歌数据显示，3.7 Flash 在复杂文档理解（GDP.pdf：34.0%对 22.0%）和业务流程自动化（AutomationBench：30.4%对 17.0%）上明显优于 3.6 Flash。社区评论指出其促销定价预计将上调，给长期成本带来不确定性。

hackernews · thisisauserid · 8月13日 17:23 · [社区讨论](https://news.ycombinator.com/item?id=49289112)

**背景**: Gemini 是谷歌 DeepMind 开发的多模态大语言模型系列，其中 Flash 系列定位为高效、低延迟的版本，适合处理高并发任务。图像转 HTML 是一种常见评测任务，要求 AI 将图片或截图转换为可运行的 HTML 代码，同时考验视觉理解与代码生成能力。新的 3.7 Flash 还被用于搭配 Nano Banana 和 Gemini Omni 等工具生成交互式页面和游戏。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/">Gemini 3.7 Flash: our most intelligent workhorse model</a></li>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3.7 Flash — Google DeepMind</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gemini_2.5_Flash_Image">Gemini 2.5 Flash Image</a></li>

</ul>
</details>

**社区讨论**: 评论者进行了多组实测：有人对比后认为 Opus 5 在图像转 HTML 上仍是标杆，但 Gemini 3.7 在其价位表现不错；也有人测试了 SVG 渲染并质疑其奇怪的价格安排。还有多位评论者指出 OpenAI 的 Luna 更便宜且更强，质疑 Flash 系列是否仍有必要。总体情绪复杂，既认可其视觉能力，又担心定价与竞争劣势。

**标签**: `#AI`, `#Google`, `#Gemini`, `#LLM`, `#Machine Learning`

---

<a id="item-2"></a>
## [用&\#x27;意面化&\#x27;DRAM 技术解锁 CPU 隐藏区域](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 9.0/10

安全研究员 Christopher Domas 发布了工具&\#x27;skitter-creek-bath-salts&\#x27;，通过操控 DRAM 控制器的物理地址转换来重映射内存，从而访问平台安全处理器（PSP）、系统管理模式（SMM）和微代码等隐藏 CPU 区域。该技术已在 AMD Family 16h（Jaguar）CPU 上演示。 该攻击绕过了所有更高级别的软件防护，使 ring-0 级 root 权限可以访问此前被认为无法触及的深层硬件秘密。它对硬件安全有重大影响，尤其是 Xbox 和 PlayStation 等游戏机，其安全团队现在可能会感到担忧。 该利用通过翻转内存控制器基地址中的一个比特，打乱物理 DRAM 地址转换，并利用线性代数重建地址映射。除 AMD Jaguar 外，README 指出 Zen 3 的内存控制器寄存器基地址不同，目前尚不清楚还有哪些较新的 CPU 受影响。

hackernews · matt\_d · 8月13日 14:17 · [社区讨论](https://news.ycombinator.com/item?id=49286341)

**背景**: DRAM 地址映射是一个复杂过程，内存控制器将物理地址转换为内存芯片特定的行、列、bank 和通道。先前的研究（如 USENIX Security 2016 论文《DRAMA：利用 DRAM 寻址进行跨 CPU 攻击》）已证明这些映射可能被泄露和利用。这项新工作更进一步，通过直接操控控制器来解锁即使操作系统通常也无法看到的隐藏处理器区域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/xoreaxeaxeax/skitter-creek-bath-salts">Spaghettifying DRAM</a></li>
<li><a href="https://zeli.app/en/story/49286341">Spaghettifying DRAM: Unlock Everything on the CPU | Zeli</a></li>

</ul>
</details>

**社区讨论**: 评论者们热情高涨，许多人称赞 Christopher Domas 的演讲风格，并热切期待 Black Hat 演讲。一些评论质疑除了 AMD Jaguar 外该攻击还适用于哪些较新的 CPU；另一些人则指出 DRAM 的复杂性使其成为一个巨大的攻击面，并认为 Xbox 和 PlayStation 安全团队可能会感到紧张。

**标签**: `#security`, `#DRAM`, `#hardware hacking`, `#exploitation`, `#reverse engineering`

---

<a id="item-3"></a>
## [DeepMind 手语转文字模型 SL2T 落地 Pixel 11](https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/) ⭐️ 9.0/10

谷歌 DeepMind 发布了大规模多语言手语转文字模型 SL2T，并首次将其部署到消费产品中。该模型目前已在 Pixel 11 的 Gboard 和 Live Transcribe 中支持美国手语转英语翻译，后续将扩展到更多设备和语言。 这标志着手语 AI 翻译模型首次进入主流消费设备，大幅扩展了聋人和听障人士的无障碍能力。它也证明大规模多语言手语翻译可以做到实用、保护隐私且具有商业可行性。 SL2T 使用超过 10 万小时、涵盖 50 多种语言的手语视频进行训练，在 FLEURS-ASL 基准上零样本得分 70 BLEURT，远高于之前的历史纪录。为保护隐私，它只处理手部和身体姿态关键点，而非原始视频。

telegram · zaihuapd · 8月13日 08:55

**背景**: SL2T 是一种手语转文字翻译模型，让聋人用户可以通过对手机打手语来输入消息、搜索或交流，而无需使用键盘。FLEURS-ASL 是 FLORES/FLEURS 大规模多语平行基准向美国手语的扩展，用于评估手语翻译质量。BLEURT 是一种基于 BERT 的学习式文本生成评估指标，衡量候选句子在多大程度上传达参考句的含义。谷歌称其在 FLEURS-ASL 上零样本得分 70 BLEURT，表明即使在未见过的数据上也有很强的语义保真度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/">Putting sign language AI into users’ hands — Google DeepMind</a></li>
<li><a href="https://arxiv.org/html/2408.13585">FLEURS - ASL : Including American Sign Language in Massively...</a></li>
<li><a href="https://github.com/google-research/bleurt">GitHub - google-research/bleurt: BLEURT is a metric for Natural Language Generation based on transfer learning. · GitHub</a></li>

</ul>
</details>

**标签**: `#sign language`, `#machine translation`, `#accessibility`, `#Google DeepMind`, `#AI`

---

<a id="item-4"></a>
## [DeepSeek-V4-Pro 正式版上线，API 实行峰谷定价](https://api-docs.deepseek.com/zh-cn/updates) ⭐️ 9.0/10

DeepSeek 已正式发布 DeepSeek-V4-Pro，现已在 DeepSeek App、网页端和 API 上线，模型名为 deepseek-v4-pro。本次发布增强了智能体（Agent）能力，原生支持 Responses API 格式以适配 Codex，并为 V4-Pro 和 V4-Flash 新增 low、high、max 三档思考模式。 DeepSeek 是最广泛使用的开源权重模型家族之一，本次发布将影响大量基于其 API 和自托管权重进行开发的开发者。峰谷定价可显著降低批量或后台任务的使用成本，而 Responses API 支持则减少了使用 Codex 及 OpenAI 兼容工具的开发者的接入摩擦。 新价格于 2026 年 8 月 17 日 0 时生效，闲时价格为高峰价格的一半。DeepSeek-V4-Pro-0813 的开源权重也已发布到 Hugging Face（1.7T 参数，约 893 GB），并在 OpenRouter 上以 deepseek/deepseek-v4-pro-0813 提供。

telegram · zaihuapd · 8月13日 11:12

**背景**: DeepSeek-V4-Pro 是 DeepSeek V4 系列的旗舰模型，一款面向 1M token 上下文窗口推理的混合专家（Mixture-of-Experts）大语言模型。Responses API 是众多开发者工具支持的 OpenAI 兼容接口，原生支持它意味着 Codex 等客户端无需额外转换层即可调用该模型。思考模式可调节模型在回答前进行思维链（chain-of-thought）计算量，让开发者在延迟、成本与回答质量之间做取舍。峰谷定价对非高峰时段的使用收取更低费用，为有成本意识的开发者提供了将重任务安排在夜间执行的激励。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://api-docs.deepseek.com/guides/responses_api/">Using the Responses API | DeepSeek API Docs</a></li>
<li><a href="https://api-docs.deepseek.com/guides/thinking_mode/">Thinking Mode | DeepSeek API Docs</a></li>
<li><a href="https://api-docs.deepseek.com/">Your First API Call | DeepSeek API Docs</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体积极，尤其是开源权重上传 Hugging Face 之后，但基准测试的发布流程引发批评：数据先在官方微信群流传，在 Reddit 被以“低质量”删除，最后出现在 Hacker News 的 ASCII 表格中。Willison 还特别指出三个思考层级生成的图像差异极大，这种不寻常的现象引发了关于思考模式如何影响模型行为的讨论。

**标签**: `#DeepSeek`, `#AI`, `#API`, `#LLM`, `#pricing`

---

<a id="item-5"></a>
## [Cerebras 与 OpenAI 推出 GPT-5.6 Sol 超快模式，HLE 测试提速近 7 倍](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 8.0/10

Cerebras 与 OpenAI 推出了 GPT-5.6 Sol 的“超快”（Ultrafast）模式，该模式在 11 小时 11 分钟内答完了“人类最后的考试”（HLE）的全部 2500 道题，比 Claude Fable 5 所需的 78 小时 27 分钟快了近 7 倍，同时保持了相近的准确率。 这是 AI 推理速度领域的一次重大突破，也标志着 OpenAI 与 Cerebras 的重要合作，可能让前沿推理在实时和迭代应用中变得更加实用。这也可能促使行业更加关注推理延迟和推理时算力这些关键竞争指标。 此次评测使用了 HLE 基准中的 2500 道专家编写题目，速度提升来自 Cerebras 的晶圆级硬件与 OpenAI 优化部署的组合。公告并未明确说明 Ultrafast 模式与标准 Sol 模型的结果完全一致，只提到“准确率相近”，并且没有公布任何定价信息。

hackernews · pr337h4m · 8月13日 18:10 · [社区讨论](https://news.ycombinator.com/item?id=49289844)

**背景**: “人类最后的考试”（HLE）是由 AI 安全中心与 Scale AI 联合创建的语言模型基准，包含 2500 道旨在测试前沿知识与推理能力的问题。Cerebras 以其晶圆级引擎（WSE）闻名，这是一种将计算、内存和互连结构集成在单颗晶圆上的处理器。更快的推理意义重大，因为它能让模型进行更多迭代，而有评论者指出，更多迭代往往与更高质量的思考密切相关。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Humanity&#x27;s_Last_Exam">Humanity&#x27;s Last Exam - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cerebras">Cerebras - Wikipedia</a></li>
<li><a href="https://www.cerebras.ai/chip">Product - Chip - Cerebras</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一：一些人称赞其原始速度及其对迭代推理的意义，另一些人则对准确率是否真的保持不变持怀疑态度。Topfi 指出，Cerebras 和 OpenAI 都没有明确确认 Ultrafast 模式与标准 Sol 表现完全一致；GodelNumbering 则指出，缺少定价信息可能意味着价格昂贵或仅限企业使用。wxw 引用了独立的输出速度对比，称 Ultrafast 比 Fable 5 快 11 倍，比 Fast 模式下的 Opus 4.8 快 5 倍。

**标签**: `#AI`, `#OpenAI`, `#Cerebras`, `#LLM performance`, `#hardware acceleration`

---

<a id="item-6"></a>
## [DeepSeek Harness 开发者预览版：开源智能体执行框架](https://deepseek.com/harness/en/) ⭐️ 8.0/10

深度求索（DeepSeek）发布了 DeepSeek Harness（dsh）的早期开源开发者预览版，采用 MIT 许可证。该预览版具备完整的运行可追溯性、重放/分叉能力，以及基于 Cordis 的动态插件系统。 其重要性在于，一家领先的 AI 实验室开源了能让开发者完全看见每次代理运行过程的基础设施，而这在商用美国模型中通常是加密或混淆的。插件架构与可追溯性有望加速构建可靠、可调试的生产级 LLM 智能体。 该框架将每一次上下文注入、系统提示、推理步骤、工具调用和子代理调度记录在只追加的会话日志中。通过轨迹视图，开发者可按来源检查记录；恢复、分叉、搜索和重放均基于同一事件流。目前仍是早期预览版，预计会有破坏性变更。

hackernews · bjin · 8月13日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=49285244)

**背景**: DeepSeek Harness 是一个智能体执行框架（agent harness），它连接前沿 LLM 与工具和记忆，使其能作为智能体运行。它构建在 Cordis 插件系统之上，该系统无需重启进程即可热加载和卸载插件，并能回滚插件的副作用。DeepSeek 正在招聘智能体执行框架研发工程师，负责构建模型与生产级智能体之间缺失的层级，这表明该项目在 LLM 智能体生态中的定位。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.deepseek.com/harness/en/">DeepSeek Harness developer preview: Everything is a plugin</a></li>
<li><a href="https://github.com/deepseek-ai/deepseek-harness">GitHub - deepseek -ai/ deepseek - harness : DeepSeek Harness ...</a></li>
<li><a href="https://dlcmh.github.io/">DeepSeek Agent Harness : Technical deep -dive &amp; the open-source...</a></li>

</ul>
</details>

**社区讨论**: 一位作者承认这只是早期预览版并欢迎反馈。有用户称赞完整的运行可追溯性是‘杀手级功能’，并将其与美国模型中加密、混淆的轨迹进行对比。还有人将其与 Cordis v4 和 Koishi 联系起来，也有评论者表示对“一切都是插件”的架构感到‘插件疲劳’。

**标签**: `#deepseek`, `#open source`, `#LLM observability`, `#agent framework`, `#AI tools`

---

<a id="item-7"></a>
## [选择无聊技术：把创新代币留给真正的问题](https://mcfunley.com/choose-boring-technology) ⭐️ 8.0/10

这条新闻重点介绍了 Dan McKinley 在 2015 年发表的有影响力的文章《选择无聊技术》，该文章主张公司应默认选用成熟可靠的技术，并仅在确实需要真正创新的地方花费有限的“创新代币”。这篇文章为工程组织的技术选型提供了一个实用框架。 这篇文章已成为工程文化讨论的基石，工程领导者在评估新工具和新框架时经常引用它。其“创新代币”概念帮助团队做出权衡并向同事清晰解释这些决策，评论者甚至将其应用于现代 AI Agent，显示出它持续的相关性。 文章指出，每家公司或团队大约拥有三个创新代币，采用新数据库、新框架或新部署范式就会花掉一个代币。所谓“无聊”技术是指那些故障模式有充分文档记录、已知其局限的技术，因此团队应精通少数几个成熟工具，避免不必要的创新。

hackernews · tosh · 8月13日 17:48 · [社区讨论](https://news.ycombinator.com/item?id=49289512)

**背景**: 这篇文章由曾在 Etsy 工作的 Dan McKinley 撰写，于 2015 年首次发表。它提出了这样一个观点：每个组织对新奇技术的接纳能力是有限的——用三个“创新代币”来表示——而这些代币一旦花掉，很长一段时间内不会补充。文章主张，公司在大多数情况下应使用无聊且成熟的技术，以便将创新预算集中在少数真正需要创新的产品领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://concepts.dsebastien.net/concept/innovation-tokens/">Innovation Tokens - Concepts</a></li>
<li><a href="https://blog.matt-rickard.com/p/innovation-tokens">Innovation Tokens - Matt Rickard</a></li>
<li><a href="https://danieljamesglover.com/blog/2025-12-25-boring-it-infrastructure-reliability/">Why Boring IT Infrastructure Wins | Daniel J Glover</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体非常正面：像 NickNaraghi 这样的工程师称“创新代币”概念是产品和技术领导者最有用的理念之一。其他人将其扩展到现代 AI Agent，建议团队把创新投入 Agent，并使用无聊的“分布内”技术；而至少一位评论者 insanitybit 提出了反对，称这一概念很随意，认为应该根据需求、风险和权衡来评估新技术的价值，而不是用一些薄弱的代理指标。

**标签**: `#engineering-culture`, `#technology-choice`, `#software-engineering`, `#innovation`, `#essay`

---

<a id="item-8"></a>
## [Worldproof 工具揭示像素指标常常无法区分世界模型优劣](https://www.reddit.com/r/MachineLearning/comments/1vnliv7/worldproof_diagnosing_where_worldmodel/) ⭐️ 8.0/10

作者发布了开源世界模型诊断工具 worldproof，并报告了一个关键发现：在真实机器人视频上，一个简单的“预测最后一帧”基线就能达到 0.983 SSIM 和 53.9 dB PSNR，且误差并不随预测步长增加。这意味着标准像素指标往往根本无法对世界模型进行有效排序。 这一发现挑战了常见的评估做法：如果像素指标缺乏区分能力，那么基于 SSIM/PSNR 的模型比较和排名可能毫无意义。从事世界模型和机器人研究的人员应该在自己的数据上测量有效评估区间，而不是沿用其他论文的默认设置。 在 15fps、48 步的 DROID 数据上，该基线表现出三个阶段：第 1–3 步近乎完美且模型难以区分；第 4–24 步误差单调下降，是唯一能区分模型优劣的区间；第 28 步之后在约 0.20 SSIM 和 10.3 dB 处触底，不再有趋势。作者使用了 64 次 rollout、四分位均值与分层自助置信区间，并指出 LPIPS 在掩码模型上的表现与其他指标不一致。

reddit · r/MachineLearning · /u/georgia\_bucea · 8月13日 19:58

**背景**: 世界模型是一类从初始上下文和动作序列预测未来帧的系统，在机器人和规划中至关重要。PSNR 和 SSIM 是常用的像素级图像质量指标，但在运动较少的视频中，一个简单的“复制最后一帧”基线就能获得高分。由于这类基线会抬高汇总指标，评估协议需要针对数据的帧率和任务速度进行仔细校准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/kurt-glore1_artificialintelligence-worldmodels-machinelearning-activity-7398017216987922432-iffX">What are World Models and why are they important? | LinkedIn</a></li>
<li><a href="https://ieeexplore.ieee.org/document/5596999/">Image Quality Metrics: PSNR vs. SSIM | IEEE Conference Publication | IEEE Xplore</a></li>
<li><a href="https://www.academia.edu/165787940/Decomposing_Motion_and_Content_for_Natural_Video_Sequence_Prediction">(PDF) Decomposing Motion and Content for Natural Video Sequence...</a></li>

</ul>
</details>

**标签**: `#world-models`, `#evaluation`, `#metrics`, `#robotics`, `#machine-learning`

---

<a id="item-9"></a>
## [特朗普签署备忘录，允许私企开展政府背书的海外网络攻击](https://www.bloomberg.com/news/articles/2026-08-13/trump-enlists-private-sector-to-boost-cyber-offensive-arsenal) ⭐️ 8.0/10

特朗普总统签署了一份备忘录，授权受联邦政府直接控制和监督的私营企业在海外开展监控和网络攻击，以打击针对美国人的外国跨国犯罪组织。国土安全部将负责运行该项目，并与司法部协调监督工作。 这标志着私营部门在政府认可的进攻性网络行动中角色显著扩大，模糊了企业行为与国家网络行动的界限。它可能为其他国家开创先例，并在全球网络安全界引发严重的法律、伦理和问责担忧。 参与企业须维持至少 100 万美元的保证金或托管款，如不遵守合同约定，该款项将被没收。该项目由国土安全部和司法部联合监督。

telegram · zaihuapd · 8月13日 05:10

**背景**: 这份备忘录基于美国政府在开展进攻性网络行动和监控方面的长期授权，但传统上此类行动由国家安全局或网络司令部等情报和军事机构执行。通过引入私营企业，政府获得了额外能力和法律掩护，而企业则在国家安全中获得正式角色。此举引发了对监督、问责和滥用可能性的质疑，尤其是私营部门的行动可能不受同样的公共透明度规则约束。

**标签**: `#cybersecurity`, `#surveillance`, `#US policy`, `#private sector`, `#cyber warfare`

---