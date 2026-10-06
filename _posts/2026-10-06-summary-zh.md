---
layout: default
title: "Horizon Summary: 2026-10-06 (ZH)"
date: 2026-10-06
lang: zh
---

> 从 33 条内容中筛选出 6 条重要资讯。

---

1. [vLLM v0.31.0 发布：717 个提交，带来 DeepSeek-V4.1-Flash 优化与快速重启](#item-1) ⭐️ 8.0/10
2. [ChatGPT 在伪造的《纽约客》漫画上添加真实漫画家签名](#item-2) ⭐️ 8.0/10
3. [Reflection 发布 Beam：5010 亿参数开放权重 MoE 模型](#item-3) ⭐️ 8.0/10
4. [Anthropic 将用户私人 Claude 日记上报警方，当事人面临重罪指控](#item-4) ⭐️ 8.0/10
5. [高通获得华为 LogicFolding 芯片封装技术专利授权](#item-5) ⭐️ 8.0/10
6. [Quad9 拒绝法国 DNS 封锁令，面临每日 58 万欧元罚款](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.31.0 发布：717 个提交，带来 DeepSeek-V4.1-Flash 优化与快速重启](https://github.com/vllm-project/vllm/releases/tag/v0.31.0) ⭐️ 8.0/10

vLLM 发布了 v0.31.0，这是一个包含来自 307 位贡献者（其中 96 位是新贡献者）共 717 个提交的大型更新，核心亮点是 DeepSeek-V4.1-Flash 的性能优化和全新的快速重启机制。主要新增内容包括：以 V4.1 NVFP4 压缩 KV cache 为基础的 FlashMLA mega attention 成为 SM100 默认配置；新的 \`vllm preload\` CLI 会启动权重缓存守护进程，使量化后的权重在引擎重启期间常驻 GPU 显存；以及通过 \`vllm snapshot create/restore\` 提供的实验性 CRIU 引擎快照功能。 vLLM 是部署最广泛的开源 LLM 推理引擎之一，其默认配置直接影响着业界大量生产环境的服务成本和延迟。快速重启与权重预加载之所以重要，是因为目前大模型重新加载会让滚动升级、自动扩缩容和故障切换变得缓慢且昂贵；而针对 DeepSeek 的优化和融合 kernel 的工作，则把低比特推理（NVFP4/MXFP8）在 Blackwell 级别硬件上进一步推向主流。 该版本还引入了大量融合 kernel（如用于 indexer 的 DeepGEMM 稀疏 MQA logits、将 gate GEMM 与专家选择融合的 Mega-Gate、SM100/SM103 上融合逆 RoPE 的小批量 WO-A）、Model Runner V2 上的投机解码与新的 LiLiCorr drafter、MoonEP 均衡式 EP all2all，以及 \`--max-num-active-seqs\` 等新调度控制项。同时包含破坏性变更：逐请求的多模态 kwargs 现在必须开启 \`--trust-request-mm-kwargs\` 才被接受，\`tokenizer\_mode=&quot;slow&quot;\` 被移除，\`--enable-mamba-fine-grained-prefix-cache\` 被重命名，通过 \`quantization=&quot;fp8&quot;\` 进行的在线量化被 \`fp8\_per\_tensor\` 简写取代，AllSpark INT8 W8A16 后端被删除。

github · khluu · 10月5日 06:44

**背景**: vLLM 是一个面向大语言模型的开源高吞吐推理服务引擎，以 PagedAttention、连续批处理等技术著称，可显著提升 GPU 推理的显存与算力效率。FlashMLA 是 DeepSeek 针对多头潜在注意力（MLA）架构优化的 attention kernel 库，vLLM 通过集成它来加速 DeepSeek 系列模型的解码；DeepGEMM 则提供同一技术栈中使用的 FP8/FP4 GEMM 与 indexer 打分 kernel。量化 KV cache（FP8、NVFP4）与低比特 GEMM 能降低长上下文模型服务所需的显存和带宽，这也是本次发布大量聚焦于这些方向的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/FlashMLA">GitHub - deepseek-ai/FlashMLA: FlashMLA: Efficient Multi-head ...</a></li>
<li><a href="https://github.com/deepseek-ai/DeepGEMM">GitHub - deepseek-ai/ DeepGEMM : DeepGEMM : clean and efficient...</a></li>
<li><a href="https://docs.vllm.ai/en/latest/design/attention_backends/">Attention Backend Feature Support - vLLM</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#DeepSeek`, `#performance optimization`, `#release`

---

<a id="item-2"></a>
## [ChatGPT 在伪造的《纽约客》漫画上添加真实漫画家签名](https://www.niemanlab.org/2026/10/chatgpt-is-adding-real-cartoonists-signatures-to-fake-new-yorker-cartoons/) ⭐️ 8.0/10

据 Nieman Lab 于 2026 年 10 月发布的报道，ChatGPT 生成的《纽约客》风格单格漫画中，出现了仍在世的真实漫画家的伪造签名。这些签名并非用户刻意添加，而是从模型的图像生成过程中自发产生，相关图片传播开后引发了广泛讨论。 这一事件把关于 AI 训练数据的长期抽象争论，变成了一个具体的“署名伪造”案例，强化了“生成模型不仅模仿风格，还会复制可识别的作者标识”的说法。它直接影响到那些名字被冒用、作品被嫁祸的职业插画师，也为围绕 AI 公司的版权与责任争论提供了新的素材。 评论者指出，这种行为其实是训练数据的直接产物：由于某位漫画家的签名经常出现在真实《纽约客》漫画的角落里，模型便把这个涂鸦当成该类漫画的正常视觉元素，而不是受保护的身份标识。正如一位观察者所言，默认流程中没有任何机制会把签名标记为“语义特殊”，因此现实可行的办法只有两种：在训练阶段显式干预，或由写提示词的人在分享前发现并裁掉、重新生成图像。

hackernews · rdmuser · 10月5日 22:46 · [社区讨论](https://news.ycombinator.com/item?id=49971846)

**背景**: 《纽约客》漫画是单格漫画，通常配有文字说明，按照行业惯例，作者会在画面角落签名，这个签名在业内被视为作者身份的标记。生成式图像模型通过在海量抓取数据中寻找统计规律来学习，因此那些与某一视觉类别稳定共现的特征——例如出现在《纽约客》风格画作旁的签名——就可能被当作该类别的一部分而一并复现。这一事件处于一场更大争论之中：用受版权保护的作品训练模型、并输出带有原作者痕迹的结果，究竟属于侵权、抄袭，还是这类系统运作方式的固有属性。

**社区讨论**: 整体情绪以尖锐批评为主：最高赞评论把这一现象称为“Plagiarism as a Service”（抄袭即服务），并认为真正的问题在于 OpenAI 没有因此被“告到破产”。另一些偏技术视角的评论给出了更机制化的解释，指出模型并不理解签名在此语境中的含义，只是在复现训练数据中的相关性，并认为提示词编写者本应在发布前发现这个问题。还有评论者指出更深层的不满在于双重标准：个人盗版或伪造签名会遭到严厉惩罚，而大规模 AI 复制却似乎无人追责。

**标签**: `#AI ethics`, `#copyright`, `#generative AI`, `#plagiarism`, `#New Yorker`

---

<a id="item-3"></a>
## [Reflection 发布 Beam：5010 亿参数开放权重 MoE 模型](https://reflection.ai/blog/introducing-beam) ⭐️ 8.0/10

Reflection 发布了 Beam，这是一个开放权重的稀疏混合专家（MoE）模型，总参数量 5010 亿、激活参数 230 亿，面向编程、推理和智能体（agentic）任务。据官方介绍，该模型在来自网络及专有授权数据集的 23.8 万亿高质量 token 上完成预训练，并额外投入了强化学习训练。 在 DeepSeek、Moonshot、阿里巴巴等中国实验室日益主导的开放权重领域，Beam 为西方阵营再添一员，其发布立刻引发了架构与基准的正面对比。对无法依赖闭源 API 的团队而言，一个激活参数仅 230 亿、性能接近前沿的模型，扩大了可用于编程和智能体流水线的可自托管选项。 讨论中引用的关键数字显示：Beam 总参数 5010 亿、激活 230 亿；对比的 DeepSeek V4.1 Flash 总参数 5520 亿，预填充激活约 80 亿、解码激活 160 亿，另有 1960 亿 n-gram/PLE 参数。一位评论者列出 Beam 预训练 token 为 28 万亿，而对比模型为 45 万亿，与官方公告中的 23.8 万亿并不一致。Reflection 主打的泛化能力证据来自一个几天前才出现的“陆地或海洋”网格谜题（180×90 网格、16200 个点），Beam 据称覆盖率达到 95.5%，介于 Opus 5（92.5%）与另一模型之间。

hackernews · Philpax · 10月5日 19:16 · [社区讨论](https://news.ycombinator.com/item?id=49969183)

**背景**: 稀疏混合专家（MoE）模型把参数拆分为众多“专家”子网络，每个 token 只路由到其中少数几个，因此总参数决定显存占用，激活参数决定单 token 计算量——这正是 5010 亿参数模型能以更小稠密模型的速度运行的原因。“开放权重”指训练好的参数被公开发布供下载，但许可证决定用户能否微调或再分发。开放权重领域已带有明显的地缘政治色彩：中国实验室普遍以宽松许可证发布大型前沿模型，而美国主要实验室的最大模型多为闭源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_model">Open-weight model</a></li>
<li><a href="https://en.wikipedia.org/wiki/Sparse_mixture-of-experts">Sparse mixture-of-experts</a></li>
<li><a href="https://localmodel.run/guides/mixture-of-experts">Mixture of experts (MoE) explained for local LLMs · localmodel.run</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者总体欢迎又一款开放权重模型，但对宣传口径持怀疑态度：有人将 Beam 的参数规模、激活参数划分和 token 预算与 DeepSeek V4.1 Flash 对比后认为并不占优，也有人质疑用一个几天前才出现的谜题图片来论证泛化能力是否严谨。还有一种反复出现的观点是，西方的开放模型仍落后于体量更小的中国模型，评论者希望出现更多供应商，并把 Google 的 Gemma 系列视为少有的亮点。

**标签**: `#open-weight-models`, `#mixture-of-experts`, `#LLM`, `#model-release`, `#AI-research`

---

<a id="item-4"></a>
## [Anthropic 将用户私人 Claude 日记上报警方，当事人面临重罪指控](https://www.techspot.com/news/114091-florida-woman-used-claude-diary-anthropic-reported-shoot.html) ⭐️ 8.0/10

一名佛罗里达州女性把 Anthropic 的 Claude 当作私人日记使用，Anthropic 将她其中一篇日记内容标记并上报给执法部门，导致她面临一项重罪指控。案件的核心是她在日记式记录中写到了与开枪射击相关的内容，检方依据佛罗里达州关于书面威胁的法规提起指控。 此案引发了激烈争论：AI 服务商是否有权监控并上报用户自认为私密的对话，以及这种做法是否会对言论表达产生寒蝉效应。它也为大模型公司如何平衡安全责任、用户隐私与法律义务提供了早期先例，而这是如今每一家主流 AI 厂商都必须回答的问题。 佛罗里达州法规 836.10 规定，发送、发布或传输威胁杀害或伤害他人、实施大规模枪击或恐怖主义的书面或电子记录构成二级重罪，但前提是该通信是以他人可能看到的方式作出的。评论者认为，一篇私人日记显然未必满足这一构成要件；而 Anthropic 自身的政策声明，它仅依据服务条款和适用法律披露账户记录，其中也包括紧急披露请求。

hackernews · emptybits · 10月5日 05:37 · [社区讨论](https://news.ycombinator.com/item?id=49961057)

**背景**: Claude 是 Anthropic 推出的大语言模型助手，许多用户把聊天机器人当作倾诉对象或日记本，但这些对话实际上是由公司处理的，而不是保存在一本密封的笔记本里。Anthropic 公开了执法请求政策以及透明度中心，说明它如何处理政府和紧急情况下的数据请求。佛罗里达州的书面威胁法规早于 AI 聊天机器人出现，当初是针对人们向他人发送的信息而制定的。此案之前，OpenAI 曾因未上报一名潜在枪手而受到批评，这也影响了 AI 公司如今对“保持沉默”风险的权衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.claude.com/en/articles/9035075-law-enforcement-requests">Law Enforcement Requests | Claude Help Center - Anthropic</a></li>
<li><a href="https://www.anthropic.com/transparency/system-trust-reporting">Anthropic’s Transparency Hub</a></li>
<li><a href="https://www.anthropic.com/news/usage-policy-update">Usage Policy update \ Anthropic</a></li>

</ul>
</details>

**社区讨论**: 评论者意见分歧明显。许多人认为该法规要求信息必须处于他人可能看到的状态，因此私人日记不应构成犯罪，还有人建议集资自建本地开源模型以避开服务商的监控。也有人对 Anthropic 表示同情，认为在 OpenAI 未上报枪手事件之后，它陷入了“不报也错、报也错”的两难，同时提醒用户：他们面对的是大型科技公司，而不是可以保密的挚友。

**标签**: `#AI privacy`, `#surveillance`, `#free speech`, `#Anthropic`, `#LLM safety`

---

<a id="item-5"></a>
## [高通获得华为 LogicFolding 芯片封装技术专利授权](https://www.bloomberg.com/news/articles/2026-10-05/qualcomm-licenses-patents-on-huawei-s-logicfolding-chip-tech) ⭐️ 8.0/10

2026 年 10 月 5 日，华为与高通宣布达成一项多年期、范围广泛的专利交叉授权协议，其中不同寻常的一点是，高通获得了华为 LogicFolding 芯片封装技术的专利授权，协议还覆盖 5G、计算、AI 和网络等领域的专利组合。这笔交易标志着技术流向的逆转：一家美国芯片巨头付费使用由一家被列入美国实体清单的中国企业开发的封装创新。 这是一个罕见案例：美国半导体领军企业为中国开发的芯片知识产权付费，说明中国的封装级创新已具备足以被授权的价值，即便在出口管制紧张的背景下也是如此。这可能改变业界对先进封装作为提升性能替代路径的看法，并引发关于美国在 5G 与计算领域领导地位的战略疑问。 LogicFolding 不把 CPU、GPU、NPU 和内存放在单一裸片上，也不通过传统中介层互连，而是借助混合键合界面将它们垂直堆叠，据称可在 7nm DUV 工艺上实现约每平方毫米 2.38 亿个晶体管，且无需 EUV。由于信号是在层间空间而非横跨整块芯片传输，该设计缩短了信号整体传输距离，因此尽管增加了堆叠层数，反而有助于降低发热。

hackernews · 0xedb · 10月5日 07:46 · [社区讨论](https://news.ycombinator.com/item?id=49961861)

**背景**: 集成电路封装是芯片制造的最后环节，负责将裸片封装并连接到电路板上；由于单纯缩小晶体管越来越困难且成本高昂，先进封装已成为提升性能的关键手段。受出口管制影响，华为基本无法获得 EUV 光刻设备，因此 LogicFolding 这类创新让它可以绕开最先进的制程节点，转而在封装与架构层面追求密度和能效提升。专利交叉授权在半导体行业十分常见，但通常是由西方知识产权持有方授权给中国实施方，因此这份协议的方向格外引人注目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.sedaily.com/international/2026/10/06/qualcomm-licenses-huaweis-logicfolding-chip-technology">Qualcomm Licenses Huawei&#x27;s LogicFolding Chip Technology</a></li>
<li><a href="https://m1k.tech/2026/07/huawei-logicfolding-architecture/">Huawei LogicFolding: 238M Transistors/mm² on 7nm DUV</a></li>
<li><a href="https://www.geeky-gadgets.com/huawei-logic-folding-moores-law/">Huawei Logic Folding: A New Approach to Moore&#x27;s Law - Geeky ...</a></li>

</ul>
</details>

**社区讨论**: 评论者的态度在技术赞赏与战略忧虑之间分化：有人指出 LogicFolding 事后看似乎理所当然，却通过缩短信号传输路径巧妙地降低了发热；也有人质疑，鉴于华为在实体清单上的身份，高通如何能签署这样的协议。一些人指出了明显的讽刺意味——美国正在曾经被其视为至关重要的 5G 竞赛中让出优势；还有评论者推测华为如今可能从高通获得净收入，但该评论者本人也提醒这一说法可能存在选择性呈现。

**标签**: `#semiconductors`, `#huawei`, `#qualcomm`, `#chip-design`, `#geopolitics`

---

<a id="item-6"></a>
## [Quad9 拒绝法国 DNS 封锁令，面临每日 58 万欧元罚款](https://torrentfreak.com/dns-resolver-quad9-rejects-french-piracy-blocks-weighs-exit-as-bein-seeks-up-to-e580k-a-day/) ⭐️ 8.0/10

瑞士非营利公共 DNS 解析服务商 Quad9 拒绝执行由转播商 beIN Sports 申请的法国法院封锁令，该命令要求其封锁 58 个与盗版体育直播相关的域名。巴黎法院上周四开庭审理，预计三周内作出裁决，beIN 要求按每个域名每日 1 万欧元罚款，合计每日最高 58 万欧元。 这起案件是对 DNS 层封锁令适用范围的重大考验——即能否从互联网接入服务商延伸到中立、注重隐私的公共解析服务商。如果 Quad9 被迫合规，它要么必须让全球用户共同承担封锁后果，要么退出法国市场；这一先例可能促使其他公共解析器按国界碎片化服务。 Quad9 表示自己从未封锁过任何域名，且由于不记录、不收集用户数据，它无法只针对法国用户实施地域性封锁，因此只能在全球封锁或退出法国市场之间二选一。它还批评法国 7 月通过的可实时自动将域名加入黑名单的法律「鲁莽且危险」。

telegram · zaihuapd · 10月5日 08:05

**背景**: DNS（域名系统）是互联网的「通讯录」，负责把人类可读的域名转换为计算机连接的 IP 地址；像 Quad9 这样的递归解析器代表用户完成这一查询，其公共地址为 9.9.9.9 和 149.112.112.112。封锁令传统上针对互联网接入服务商，因为它们可以按用户执行封锁；但对解析器下达同样命令在技术上完全不同，因为解析器面向全球用户服务，且往往刻意不留日志。此次涉及的法国规则源自 2024 年 5 月通过的第 2024-449 号法律（SREN 法），该法加强了国家对数字空间的监管能力以及对侵权网站实施封锁的能力，包括采用更快、更自动化的程序。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wipo.int/wipolex/en/legislation/details/22589">Law No. 2024-449 of May 21, 2024, France, WIPO Lex</a></li>
<li><a href="https://www.twobirds.com/en/insights/2024/france/la-loi-sren-securisation-et-regulation-de-l-espace-numerique-en-france">The SREN Law: Securing and Regulating Digital Space in France</a></li>
<li><a href="https://enterno.io/articles/quad9-dns">Quad 9 DNS 9.9.9.9: что это, как настроить и чем отличается</a></li>

</ul>
</details>

**标签**: `#DNS`, `#Internet privacy`, `#France`, `#censorship`, `#piracy blocking`

---