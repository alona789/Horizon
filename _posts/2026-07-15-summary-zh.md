---
layout: default
title: "Horizon Summary: 2026-07-15 (ZH)"
date: 2026-07-15
lang: zh
---

> 从 45 条内容中筛选出 14 条重要资讯。

---

1. [在 4 国 14 台 Mac 上完成强化学习后训练](#item-1) ⭐️ 9.0/10
2. [Inkling：最大的开源权重多模态音频模型](#item-2) ⭐️ 8.0/10
3. [Stripe 与 Advent 联合出价收购 PayPal](#item-3) ⭐️ 8.0/10
4. [欧盟法院裁定 OpenAI 商标缺乏显著性](#item-4) ⭐️ 8.0/10
5. [Claude 的 web_fetch 漏洞导致用户隐私数据泄露](#item-5) ⭐️ 8.0/10
6. [Linus Torvalds 捍卫在 Linux 中使用 AI，警告不要敌对](#item-6) ⭐️ 8.0/10
7. [德国 AI 联盟发布开源 30B 模型 Soofi S](#item-7) ⭐️ 8.0/10
8. [Inkling 成为美国第一开源权重模型](#item-8) ⭐️ 8.0/10
9. [DeepSeek 筹备 IPO，寻求 710 亿美元以上估值融资](#item-9) ⭐️ 8.0/10
10. [法官质疑 Epic 与谷歌 8 亿美元交易或削弱反垄断立场](#item-10) ⭐️ 8.0/10
11. [DeepSeek 完成逾 500 亿元首轮融资](#item-11) ⭐️ 8.0/10
12. [马斯克：X 将开源全部代码并接受第三方审查](#item-12) ⭐️ 8.0/10
13. [iOS 27 Beta 沙盒逃逸漏洞让 Filza 读取备忘录数据库](#item-13) ⭐️ 8.0/10
14. [ASML 计划涨价，台积电抵制，部分中企接受 DUV 涨 10%](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [在 4 国 14 台 Mac 上完成强化学习后训练](https://www.reddit.com/r/LocalLLaMA/comments/1uxb3zn/rl_posttraining_on_14_macs_across_4_countries/) ⭐️ 9.0/10

Pluralis Research 完成了首个强化学习后训练运行，所有 rollout 生成均使用 MLX 进行 int8 推理，在 4 个国家的 14 台消费级 Mac 上完成，而梯度更新则通过普通互联网在远程 B200 上进行。 这证明了无需数据中心互联即可实现分布式强化学习后训练，通过利用闲置的消费级硬件，有可能降低代理强化学习的计算门槛。 通过 PULSE 发送 int8 权重增量（每个版本仅约 0.5%变化，约 82MB 而非 9GB）以及 DPPO 风格的概率门控丢弃概率漂移的 token，控制了策略偏差。该系统在 PaperSearchQA 上将 cover pass@1 从 29%提升至 63%。

reddit · r/LocalLLaMA · /u/erfan_mhi · 7月15日 16:36

**背景**: 强化学习后训练是在初始预训练后使用 RL 对模型进行微调。代理 RL 中的 rollout 生成计算密集，通常需要昂贵的数据中心 GPU。MLX 是一个用于 Apple Silicon 上机器学习的开源数组框架。策略偏差是指生成 rollout 的模型权重相对于训练器模型过时。PULSE 仅传输量化模型版本间变化的参数，高效通信。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mlx-framework.org/">MLX framework</a></li>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple silicon · GitHub</a></li>

</ul>
</details>

**标签**: `#RL`, `#post-training`, `#distributed computing`, `#MLX`, `#Mac`

---

<a id="item-2"></a>
## [Inkling：最大的开源权重多模态音频模型](https://thinkingmachines.ai/news/introducing-inkling/) ⭐️ 8.0/10

Thinking Machines 发布了 Inkling，一个开放权重的多模态模型，据称是同类中最大的支持音频的模型，具有强大的音频能力和高效推理。 这一发布填补了具有强大音频能力的开源权重多模态模型的空白，支持企业定制和本地部署，可能加速音频相关 AI 应用。 Inkling 可在 Tinker 平台微调，并支持长上下文。早期社区基准测试表明它在音频任务上可能超越一些竞争对手，但并非整体最强。

hackernews · vimarsh6739 · 7月15日 18:12 · [社区讨论](https://news.ycombinator.com/item?id=48924912)

**背景**: 开源权重模型公开发布训练参数，允许任何人下载和修改。多模态模型处理多种数据类型如文本、音频和图像。Inkling 结合了这些，并强调音频。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>
<li><a href="https://en.wikipedia.org/wiki/Multimodal_model">Multimodal model</a></li>

</ul>
</details>

**社区讨论**: 社区成员对 Inkling 的音频能力和开放性表示兴奋，有人指出它可能是强大的代理应用基础。其他人将其与中国开源模型比较，并推测其对美国 AI 实验室的战略重要性。

**标签**: `#open-weights`, `#multimodal`, `#AI`, `#audio`, `#fine-tuning`

---

<a id="item-3"></a>
## [Stripe 与 Advent 联合出价收购 PayPal](https://www.reuters.com/business/finance/stripe-advent-offer-buy-paypal-more-than-53-billion-sources-say-2026-07-15/) ⭐️ 8.0/10

如果交易完成，此次收购将整合主要金融科技公司，可能大幅重塑在线支付格局，引发反垄断担忧，并影响数百万商家和消费者。 该出价对 PayPal 的估值超过 530 亿美元，交易将使 Stripe、PayPal、Venmo、Braintree 和 Xoom 归于同一旗下，可能导致非面对面交易市场高度集中。

hackernews · rvz · 7月15日 03:32 · [社区讨论](https://news.ycombinator.com/item?id=48915953)

**背景**: Stripe 是一家以开发者友好 API 著称的主要在线支付处理商，而 PayPal 是拥有 Venmo 和 Braintree 等品牌的数字支付先驱。Advent International 是一家全球私募股权公司。由于合并后在在线支付领域的市场份额，反垄断监管机构很可能会审查该交易。

**社区讨论**: 社区评论对该收购表示强烈担忧，提及潜在的反垄断问题、费用上涨以及 Stripe 对大麻和成人内容等行业的限制政策。用户担心整合减少竞争，使他们的业务面临风险。

**标签**: `#fintech`, `#acquisition`, `#paypal`, `#stripe`, `#antitrust`

---

<a id="item-4"></a>
## [欧盟法院裁定 OpenAI 商标缺乏显著性](https://dpa-international.com/economics/urn:newsml:dpa.com:20090101:260715-930-389143/) ⭐️ 8.0/10

欧盟普通法院裁定，OpenAI 的商标“OPENAI”在软件和 IT 服务上无效，因为该术语是描述性的，将“开放”意为自由访问与“AI”即人工智能相结合。 该裁决凸显了欧盟商标制度比美国更严格的显著性要求，影响主要 AI 公司，并可能影响品牌保护策略。 法院认为，对于某些软件和信息技术商品和服务，“OPENAI”纯粹是描述性的，在欧盟缺乏通过使用获得的显著性。

hackernews · hermanzegerman · 7月15日 14:32 · [社区讨论](https://news.ycombinator.com/item?id=48921461)

**背景**: 在商标法中，描述性商标直接描述商品或服务的特征，因此很难注册，除非通过广泛使用获得显著性。欧盟制度要求商标从一开始就具有固有显著性，而美国允许注册已获得第二含义的描述性商标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.justia.com/intellectual-property/trademarks/strength-of-marks/descriptive-marks/">Descriptive Trademarks and Service Marks & Their Potential Legal Protection | Intellectual Property Law Center | Justia</a></li>
<li><a href="https://www.inta.org/wp-content/uploads/public-files/resources/the-trademark-reporter/vol109_no3_a1_porangaba.pdf">Acquired Distinctiveness in the European Union</a></li>

</ul>
</details>

**社区讨论**: 评论者指出了欧盟和美国商标制度之间的对比，一些人赞扬法院对“开放”一词被劫持的合理质疑。其他人指出，该裁决与先前驳回描述性商标的案例一致。

**标签**: `#trademark`, `#AI`, `#OpenAI`, `#EU law`, `#open source`

---

<a id="item-5"></a>
## [Claude 的 web_fetch 漏洞导致用户隐私数据泄露](https://simonwillison.net/2026/Jul/15/claude-web-fetch-exfiltration/#atom-everything) ⭐️ 8.0/10

安全研究员 Ayush Paul 展示了一种提示注入攻击，绕过了 Anthropic 对 Claude 的 web_fetch 工具的保护，诱使其泄露用户的私人记忆信息，如姓名、位置和雇主。 该漏洞凸显了结合私有数据、不可信内容和外部通信的 AI 代理（即“致命三重奏”）在安全性上的持续挑战，并强调了广泛使用的 AI 聊天机器人面临的数据泄露风险。 该攻击利用了一个漏洞：web_fetch 可以跟随之前抓取页面中嵌入的 URL；通过创建一个呈现虚假身份验证提示的蜜罐网站，攻击者让 Claude 逐字母导航以泄露数据。

rss · Simon Willison · 7月15日 14:21

**背景**: “致命三重奏”指的是 AI 代理中的危险组合：访问私有数据、处理不可信内容以及发送外部通信的能力。Claude 的 web_fetch 工具本设计有保护措施，通过将 URL 导航限制为用户输入或搜索结果中的 URL 来防止数据泄露。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/agents-and-tools/tool-use/web-fetch-tool">Web fetch tool - Claude Platform Docs</a></li>
<li><a href="https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/">The lethal trifecta for AI agents: private data, untrusted content, and external communication</a></li>

</ul>
</details>

**社区讨论**: 在 Hacker News 上，讨论可能集中在攻击的严重性和 Anthropic 回应的充分性——因声称内部已发现而不支付赏金。一些人可能讨论了 AI 代理安全的更广泛影响。

**标签**: `#AI security`, `#prompt injection`, `#data exfiltration`, `#Claude`, `#Anthropic`

---

<a id="item-6"></a>
## [Linus Torvalds 捍卫在 Linux 中使用 AI，警告不要敌对](https://www.reddit.com/r/LocalLLaMA/comments/1uxbrw4/linus_torvalds_tells_people_to_stop_attacking/) ⭐️ 8.0/10

Linux 创始人 Linus Torvalds 公开表示，人工智能是一个有用的工具，并警告社区不要因使用 AI 而攻击他人，宣称 Linux 内核项目不是反 AI 的，并将继续专注于技术优势。 Linus Torvalds 的支持在开源社区具有重要影响力，可能塑造 Linux 及其他项目更加接纳 AI 工具的文化，从而加速 AI 在软件开发中的应用。 Torvalds 强调，尽管 AI 不完美，但其有用性已毋庸置疑，内核社区基于技术优势而非对新工具的恐惧做决策。他还警告持反对意见者可以分支项目或离开。

reddit · r/LocalLLaMA · /u/Illustrious_Car344 · 7月15日 16:59

**背景**: Linus Torvalds 是 Linux 内核的原始创建者和长期首席维护者，Linux 是世界上最庞大的开源项目之一。人工智能工具，特别是大型语言模型（LLM），已越来越多地用于代码生成、审查和错误检测，引发了关于其对代码质量和维护者工作量影响的辩论。

**标签**: `#AI`, `#Linux`, `#Open Source`, `#Linus Torvalds`, `#Community Debate`

---

<a id="item-7"></a>
## [德国 AI 联盟发布开源 30B 模型 Soofi S](https://www.reddit.com/r/LocalLLaMA/comments/1uxao7y/german_ai_consortium_releases_soofi_s_an_open_30b/) ⭐️ 8.0/10

德国 AI 联盟‘Soofi Project’发布了开源 30B 参数（30B-A3B）基础模型 Soofi S，在英语和德语基准测试中均达到领先性能。 这一发布意义重大，因为它展示了利用欧洲基础设施构建主权、开源多语言模型的能力，减少了对美国 AI 提供商的依赖，并促进了 AI 主权。 Soofi S 是一个 30B 参数模型，具有 3B 活跃参数，完全在慕尼黑德国电信运营的德国工业 AI 云上训练，并在 Hugging Face 上以开源许可证提供。

reddit · r/LocalLLaMA · /u/yogthos · 7月15日 16:21

**背景**: 像 GPT-4 或 Llama 这样的基础模型通常由美国公司在大型计算集群上开发。Soofi Project 旨在利用欧盟基础设施，创建专注于德语和英语的主权欧洲替代方案。Soofi S 是他们的首次重大发布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Soofi-Project/Soofi-S-Base">Soofi-Project/Soofi-S-Base - Hugging Face</a></li>
<li><a href="https://arxiv.org/abs/2607.09424">[2607.09424] A Sovereign, Open-Source Foundation Model for German and English - arXiv</a></li>

</ul>
</details>

**标签**: `#open-source`, `#LLM`, `#AI`, `#multilingual`, `#benchmarks`

---

<a id="item-8"></a>
## [Inkling 成为美国第一开源权重模型](https://www.reddit.com/r/LocalLLaMA/comments/1uxhpws/inkling_by_thinking_machines_is_the_1_us_open/) ⭐️ 8.0/10

Thinking Machines Lab 发布了 Inkling，这是一个总参数量 975B 的混合专家模型，目前在美国开源权重模型中排名第一，全球排名第五。 这标志着美国开源权重模型在追赶中国领先模型方面迈出了重要一步，凸显了开源 AI 开发的竞争力。 Inkling 采用混合专家架构，总参数量 975B，活跃参数量 41B，在评测中超越了 NVIDIA 的 Nemotron 3 Ultra（总参数 550B，活跃参数 55B）。

reddit · r/LocalLLaMA · /u/davidthesong · 7月15日 20:40

**背景**: 开源权重模型是指其训练参数公开发布的 AI 模型，允许任何人下载和微调。它们与完全开源模型不同，可能附带使用限制。此次发布是美中企业在 AI 领域争夺领导地位的持续竞争的一部分，此前 DeepSeek 等中国模型曾占据榜首。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our open-weights model - Thinking Machines Lab</a></li>
<li><a href="https://thinkingmachines.ai/inkling/">Inkling - Thinking Machines Lab</a></li>
<li><a href="https://techcrunch.com/2026/07/15/thinking-machines-amps-up-its-bet-against-one-size-fits-all-ai-with-its-first-open-model-inkling/">Thinking Machines amps up its bet against one-size-fits-all AI with its first open model, Inkling | TechCrunch</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**标签**: `#open weight models`, `#LLM`, `#AI competition`, `#NLP`, `#model benchmark`

---

<a id="item-9"></a>
## [DeepSeek 筹备 IPO，寻求 710 亿美元以上估值融资](https://t.me/zaihuapd/42577) ⭐️ 8.0/10

DeepSeek 已启动 IPO 筹备，计划最早 2025 年底或 2026 年初提交申请，目标 2027 年上市，同时寻求新一轮私募融资，投前估值至少 4800 亿元人民币（约 710 亿美元）。 这一估值从 2025 年 6 月的约 500 亿美元大幅攀升，显示出市场对 DeepSeek AI 能力的高度信心，其 IPO 将成为中国 AI 初创公司中规模最大的之一，影响全球 AI 投资格局。 DeepSeek 在 2025 年 6 月初完成了首轮外部融资，筹集 7 亿美元，投资者包括腾讯和宁德时代，新一轮目标至少融资 100 亿元人民币，最终金额可能因投资者数量而翻数倍。

telegram · zaihuapd · 7月15日 07:04

**背景**: DeepSeek 是一家领先的中国 AI 初创公司，以其大语言模型闻名。该公司在 2025 年 6 月的首轮外部融资中估值约 500 亿美元。新的 710 亿美元估值反映了在竞争激烈的 AI 领域的快速增长预期。创始人梁文锋的身家据报已大幅增长。

**标签**: `#DeepSeek`, `#AI`, `#funding`, `#IPO`, `#valuation`

---

<a id="item-10"></a>
## [法官质疑 Epic 与谷歌 8 亿美元交易或削弱反垄断立场](https://t.me/zaihuapd/42588) ⭐️ 8.0/10

在最近的一次听证会上，美国地区法官 James Donato 披露，Epic Games 与谷歌已达成新的商业合作，涵盖联合产品开发、营销及合作伙伴关系，Epic 未来 6 年内将向谷歌支付约 8 亿美元。法官担忧该协议可能影响 Epic 推动 Android 生态反垄断改革的立场。 这一进展可能削弱 Epic 在与谷歌反垄断诉讼中的可信度，降低 Android 应用分发和支付系统实现有意义改革的可能性。它也引发了关于平台巨头与其批评者之间利益一致性的更广泛质疑。 协议涉及 Unreal Engine、《堡垒之夜》及 Android 相关业务，Epic 将在 6 年内向谷歌支付约 8 亿美元。Epic CEO Tim Sweeney 表示协议未包含 Epic Games Store 在 Android 上的条款，但法官质疑该商业关系是否削弱了 Epic 的反垄断立场。

telegram · zaihuapd · 7月15日 11:15

**背景**: Epic Games 于 2020 年起诉谷歌，指控其通过 Google Play 和应用内支付系统对 Android 应用市场实施非法垄断。庭审于 2023 年 12 月结束，陪审团认定谷歌违反反垄断法，随后正在协商补救措施。新披露的商业合作出现在补救措施听证会中，引发了利益冲突的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Unreal_Engine">Unreal Engine</a></li>

</ul>
</details>

**标签**: `#antitrust`, `#epic games`, `#google`, `#android`, `#mobile ecosystem`

---

<a id="item-11"></a>
## [DeepSeek 完成逾 500 亿元首轮融资](https://t.me/zaihuapd/42589) ⭐️ 8.0/10

DeepSeek 完成了首轮融资，筹得逾 500 亿元人民币（约 74 亿美元），估值超过 500 亿美元。此次融资采用非常规的有限合伙架构，投资者需将资金注入 CEO 梁文锋管理的基金，并接受五年锁定期且无表决权。 这一大规模融资轮表明投资者对 DeepSeek 及中国 AI 行业充满信心，尤其考虑到该融资采用特殊治理结构以维持创始人控制权。腾讯和宁德时代等大型企业的参与凸显了 AI 在中国的战略重要性。 该融资采用有限合伙架构，实现钱权分离，创始人梁文锋个人投资了 200 亿元。腾讯考虑投资 100 亿元，宁德时代计划投资 50 亿元，成为本轮最大的外部投资者。

telegram · zaihuapd · 7月15日 12:56

**背景**: 有限合伙架构将合伙人分为普通合伙人（GP）和有限合伙人（LP）。在这种模式中，GP（此处为 CEO 梁文锋）管理基金并保留控制权，而 LP 提供资金但决策权有限。初创公司常采用这种结构来融资而不稀释创始人控制权。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cj.sina.com.cn/articles/view/1887344341/707e96d502001rse4">有限合伙、五年 锁 定 期 、 无 投票 权 ？传DeepSeek已完成500亿元 融 资</a></li>
<li><a href="https://www.163.com/dy/article/KOV0N13E0556KOZH.html">163.com/dy/article/KOV0N13E0556KOZH.html</a></li>
<li><a href="https://m.gelonghui.com/p/5264691">DeepSeek 融 资 500亿：量化大佬梁文锋的反 资 本实验</a></li>

</ul>
</details>

**标签**: `#AI`, `#funding`, `#DeepSeek`, `#corporate governance`, `#startup`

---

<a id="item-12"></a>
## [马斯克：X 将开源全部代码并接受第三方审查](https://x.com/elonmusk/status/2077361679034118271) ⭐️ 8.0/10

埃隆·马斯克宣布，在完成安全漏洞审查后，X（原 Twitter）将无条件开源其全部代码库，并邀请第三方审查者检查正在运行的系统，以确认开源代码与实际运行的代码一致。 此举可能显著提升 X 平台软件的透明度和信任度，为大型社交平台树立新标杆。它可能促使其他公司采取类似的开放措施，惠及更广泛的开源社区和用户隐私倡导者。 公告明确指出，开源将在安全漏洞审查之后进行，第三方审查者将检查生产系统的一致性。马斯克强调，完全透明带来的信任是唯一值得相信的东西。

telegram · zaihuapd · 7月15日 13:32

**背景**: X（原 Twitter）是一个主要社交媒体平台。开源通常指以开源许可证发布源代码，允许公众检查和贡献。第三方审查增加了一层验证，确保发布的代码与服务器上实际运行的代码一致，从而解决监控或操控方面的担忧。

**标签**: `#open source`, `#Twitter`, `#transparency`, `#software engineering`

---

<a id="item-13"></a>
## [iOS 27 Beta 沙盒逃逸漏洞让 Filza 读取备忘录数据库](https://x.com/0xjohnny/status/2077216973256274272) ⭐️ 8.0/10

开发者 Johnnys 修改了文件管理工具 Filza，利用 iOS 27 beta 3 中的沙盒逃逸漏洞，在 iPhone 17 Pro Max 上成功读取了备忘录数据库。 这一演示揭示了最新 iOS beta 版本中的关键安全漏洞，可能影响用户的隐私和数据安全。同时也展示了越狱社区与苹果安全措施之间持续的博弈。 该漏洞专门绕过了 iOS 27 beta 3 上的应用容器沙盒，使修改后的 Filza 能够浏览外部数据，包括敏感的系统数据库。该漏洞尚未分配 CVE 编号。

telegram · zaihuapd · 7月15日 14:35

**背景**: iOS 沙盒机制将每个应用限制在自己的容器内，阻止访问其他应用数据和系统文件。沙盒逃逸漏洞允许应用突破这种限制，通常通过内核漏洞或配置错误的权限实现。Filza 是一款流行的文件管理器，常用于越狱环境以访问 iOS 文件系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tigisoftware.com/default/?page_id=78">Filza – TIGI Software</a></li>
<li><a href="https://redfoxsecurity.medium.com/locked-in-a-box-how-ios-sandboxing-challenges-pentesters-8207476da296">Locked in a Box : How iOS Sandboxing Challenges Pentesters | Medium</a></li>

</ul>
</details>

**标签**: `#iOS security`, `#sandbox escape`, `#vulnerability`, `#Filza`, `#jailbreak`

---

<a id="item-14"></a>
## [ASML 计划涨价，台积电抵制，部分中企接受 DUV 涨 10%](https://news.bloomberglaw.com/artificial-intelligence/asml-plans-price-increases-on-chipmaking-equipment-information) ⭐️ 8.0/10

ASML 宣布计划提高其 EUV 和 DUV 光刻设备的价格，其中 EUV 产能已预订至 2027 年。台积电抵制 EUV 涨价，而部分中国芯片制造商已接受 DUV 设备涨价 10%。 ASML 的定价权反映了其在先进光刻领域的近乎垄断地位，对芯片制造至关重要。此举可能扩大先进制程与成熟制程芯片制造商之间的差距，并在出口限制背景下，部分中国企业接受 DUV 涨价具有地缘政治影响。 ASML 首席财务官 Roger Dassen 表示公司拥有较强定价权；EUV 系统产能已全部预订至 2027 年底。部分中国客户已同意 DUV 设备涨价 10%，而与台积电就 EUV 价格的谈判仍存在分歧。

telegram · zaihuapd · 7月15日 16:49

**背景**: 光刻设备是用于在硅片上印制电路图案的关键设备。EUV（极紫外）光刻采用 13.5 纳米波长，能实现先进芯片（如 5nm、3nm 节点）的最小特征尺寸，且由 ASML 独家生产。DUV（深紫外）光刻使用 193 纳米波长，广泛应用于非关键层和成熟节点。ASML 在 EUV 领域的垄断地位以及在 DUV 领域的强势地位使其对全球芯片制造商拥有显著议价能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EUV_lithography">EUV lithography</a></li>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://www.asml.com/en/products/euv-lithography-systems">EUV lithography systems – Products | ASML</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#ASML`, `#chip manufacturing`, `#pricing`, `#geopolitics`

---