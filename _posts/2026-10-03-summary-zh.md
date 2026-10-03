---
layout: default
title: "Horizon Summary: 2026-10-03 (ZH)"
date: 2026-10-03
lang: zh
---

> 从 31 条内容中筛选出 5 条重要资讯。

---

1. [新 AI 以少 34 倍的对局量击败顶尖人类 Stratego 选手](#item-1) ⭐️ 8.0/10
2. [Redis 之父 antirez 发布本地 LLM 推理引擎 ds4](#item-2) ⭐️ 8.0/10
3. [Greg Kroah-Hartman 驳斥 Anthropic 的 LLM 内核漏洞发现声明](#item-3) ⭐️ 8.0/10
4. [Zig v0.17.0 发布，引发设计理念与 LLM 使用之争](#item-4) ⭐️ 8.0/10
5. [Google Research 发布 Cogentic 多智能体系统，称在五个开放数学问题上取得新结果](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [新 AI 以少 34 倍的对局量击败顶尖人类 Stratego 选手](https://arstechnica.com/science/2026/10/ai-finally-beat-the-best-stratego-player-in-history-and-did-it-on-a-budget/) ⭐️ 8.0/10

研究者构建了一个 AI 系统，据发表在《Nature》上的论文及配套的 arXiv 预印本（2511.07312）显示，它成为首个击败历史上最强人类 Stratego 选手的 AI。据称该系统在达到超越人类水平的同时，所进行的对局数量比 DeepMind 2022 年的 DeepNash 少了约 34 倍。 Stratego 是一种非完美信息博弈，玩家看不到对方棋子的身份，因此对 AI 而言比国际象棋或围棋这类完全可观测的博弈要困难得多。样本效率提升 34 倍这一结果，意味着这类方法可能迁移到谈判、安全对抗以及现实世界的战略规划等其他隐藏信息场景中。 其核心创新点在于学习速度：该算法比 DeepNash 少玩约 34 倍的对局，最终却强得多。这一点很关键，因为在隐藏信息下，向前搜索——即“我这样走，对方就会那样走”的推理——从根本上变得不可靠。该成果经过同行评审并发表于《Nature》，同时有 arXiv 论文，因此比一般性的基准测试发布更具分量。

hackernews · PaulHoule · 10月2日 14:11 · [社区讨论](https://news.ycombinator.com/item?id=49933740)

**背景**: Stratego 是一种双人棋盘游戏，双方的棋子对对手都是隐藏的，揭示或推断棋子身份是取胜的关键。DeepMind 于 2022 年 7 月公布的 DeepNash 使用无模型的多智能体强化学习，在该游戏上达到了人类专家水平。Stratego 和扑克这类非完美信息博弈长期以来都是 AI 的难题，因为标准的搜索与评估技术都假设完整状态是已知的。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Google_DeepMind">Google DeepMind - Wikipedia</a></li>
<li><a href="https://www.deeplearning.ai/the-batch/deepnash-the-rl-system-that-plays-stratego-like-a-master">DeepNash, the RL System That Plays Stratego like a Master</a></li>
<li><a href="https://dl.acm.org/doi/10.5555/3060621.3060765">Imperfect - information games and generalized planning | Proceedings...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为样本效率才是真正的看点，有人指出正因隐藏信息让搜索变得不可靠，快速学习才使这一方法真正行得通。也有人把该成果与 DeepMind 2022 年宣称的“掌握 Stratego”作对比，认为四年后新方法才真正首次超越人类；另有几位分享了童年玩这款桌游的怀旧趣事（其中一位还提到对手的棋子有细微磕痕，借此作弊）。

**标签**: `#AI/ML`, `#game-playing AI`, `#imperfect-information games`, `#reinforcement learning`, `#research papers`

---

<a id="item-2"></a>
## [Redis 之父 antirez 发布本地 LLM 推理引擎 ds4](https://dwarfstar.sh/) ⭐️ 8.0/10

Redis 的作者 Salvatore Sanfilippo（antirez）发布了开源本地推理引擎 ds4，可在消费级硬件上运行 DeepSeek V4 Flash、PRO 等大语言模型。该项目提供 Metal、CUDA 和 ROCm 三种后端，近期还加入了 Vision 与 Qwen 模型的支持。 它为用户提供了 llama.cpp、Ollama、vLLM 之外的轻量选择，让个人开发者和爱好者能在自己的机器上运行能力不错的模型，而不必依赖云端 API 付费调用。围绕它的热烈讨论、FFI 分支以及衍生推理引擎，说明“在普通硬件上跑本地模型”的需求非常旺盛。 ds4 面向 Metal、CUDA 和 ROCm 后端，支持 DeepSeek V4 Flash/PRO 系列，并在最近几周加入了 Vision 和 Qwen 支持。社区成员提到，SSD 存储或许可以替代超大容量内存，但其吞吐率和工具调用（tool calling）性能目前仍缺乏公开的实测数据。

hackernews · fibo · 10月2日 18:01 · [社区讨论](https://news.ycombinator.com/item?id=49936575)

**背景**: 推理引擎是负责加载模型权重并执行文本生成的软件层，ds4 由因创建内存数据库 Redis 而闻名的 antirez 编写。llama.cpp、Ollama、vLLM 等本地推理引擎让用户可以在自己的 GPU 上运行开放权重模型，而不必调用云端 API，用一些速度与便利换取隐私、可控成本和离线可用性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/antirez/ds4">GitHub - antirez/ds4: DeepSeek 4 Flash and PRO local ...</a></li>
<li><a href="https://developer.amd.com/playbooks/deepseek-v4-flash-ds4/">Running DeepSeek V4 Flash with ds4 | AMD AI Playbooks</a></li>
<li><a href="https://www.local-llm.net/compare/inference-engines-2026/">Local LLM Inference Engines Compared: The Definitive 2026 ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的反响热烈且十分务实：neomantra 维护了一个把 ds4 打包成共享库的分支，可通过 FFI 供其他语言调用，并开发了 Go 绑定 ds4go；cuttothechase 关心工具调用支持情况，以及 SSD 能否在约 50 TPS 下替代大内存 Mac；ttoinou 表示在 M5 Max 128GB 上配合 DeepSeek V4 Flash 和 Qwen 3.8 Flash 效果很好；simoiacos 则受其启发为 Intel Xe-LP 笔记本写了衍生引擎 xenolith。讨论中也有人指出，可靠性和吞吐率数据仍多属个案，模型出现的异常行为也可能来自智能体框架而非 ds4 本身。

**标签**: `#local-llm`, `#inference-engine`, `#antirez`, `#ds4`, `#hackernews`

---

<a id="item-3"></a>
## [Greg Kroah-Hartman 驳斥 Anthropic 的 LLM 内核漏洞发现声明](https://www.youtube.com/watch?v=NnV_cWeoo5Q) ⭐️ 8.0/10

在内核维护者 Greg Kroah-Hartman 题为《LLM 时代的安全》的演讲中，他逐项拆解了 Anthropic 的 Mythos 声称发现的 79 个 Linux 内核漏洞，指出其中 24 个毫无细节、14 个根本不是缺陷、3 个是凭空捏造的数据、15 个在最新版本中早已修复——真正需要修复的仅约 20 个，且大多只是把开发者多年前的补丁模式套用到别处。 这番言论直接挑战了头部 AI 实验室把 LLM 漏洞发现宣传为安全突破的营销叙事，并处在关于 AI 安全炒作更广泛争论的中心——尤其讽刺的是，Anthropic 一边以安全为由限制其最强模型的发布，一边用它来宣传自身能力。 在真正需要修复的约 20 个漏洞中，有 7 个的前提是&quot;恶意文件系统镜像&quot;，还有 2 个假设攻击者能够注入恶意输入，意味着许多漏洞在现实威胁模型中只是理论性的；Kroah-Hartman 还指出，Anthropic 并未对最初编写这些补丁的内核开发者给予任何署名。

hackernews · usernomdeguerre · 10月2日 02:51 · [社区讨论](https://news.ycombinator.com/item?id=49929391)

**背景**: CVE（通用漏洞披露）是一套为公开安全缺陷分配标准编号的体系，因此&quot;发现 79 个 CVE&quot;听起来既惊人又可量化。Anthropic 的 Claude Mythos 被称为其迄今最强的模型，能够自主发现漏洞，并出于安全考量仅向经过审核的合作伙伴开放预览版。Greg Kroah-Hartman 是长期担任 Linux 内核维护者的资深人物，他的评估在开源社区中具有极高的可信度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/mythos">Claude Mythos \ Anthropic</a></li>
<li><a href="https://www.cve.org/">CVE : Common Vulnerabilities and Exposures</a></li>
<li><a href="https://labs.cloudsecurityalliance.org/research/ai-vuln-discovery-containment-claude-mythos-v1-0-csa-styled/">Claude Mythos: AI Vulnerability Discovery and Containment ...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍赞赏 Kroah-Hartman 的坦诚和逐页统计，认为这暴露了 AI 实验室&quot;模型会毁灭世界&quot;的安全论调与其夸大宣传之间的强烈矛盾。也有人批评 Anthropic 未对 Mythos 所套用补丁的原始内核开发者给予署名，同时少数人指出，若用针对内核细节专门训练的模型，这种方法未来仍可能真正变得有用。

**标签**: `#LLM security`, `#Linux kernel`, `#vulnerability research`, `#AI hype critique`, `#Anthropic`

---

<a id="item-4"></a>
## [Zig v0.17.0 发布，引发设计理念与 LLM 使用之争](https://ziglang.org/download/0.17.0/release-notes.html) ⭐️ 8.0/10

Zig 项目发布了 v0.17.0 的发布说明，这是这门系统编程语言及其工具链最新的带标签版本，详细列出了编译器、构建系统与平台支持方面的改动。伴随而来的 Hacker News 讨论集中在 Zig 广泛的目标平台支持、新的构建与工具链集成，以及创始人 Andrew Kelley 对使用 LLM 查找 bug 日益开放的态度上。 Zig 被广泛视为 C 语言在系统编程领域最受关注的现代替代者之一，其异常广泛的目标平台支持甚至被部分开发者认为可与 C 匹敌，因此每次版本发布都会影响跨平台与嵌入式开发者的工具选择。LLM 这一角度同样重要：一个历史上对 AI 贡献持强硬立场的项目，如今似乎开始务实地用 LLM 查找 bug，这可能影响其他开源编译器与基础设施项目对 AI 的态度。 Zig 目前仍处于 1.0 之前，因此 v0.17.0 只是持续演进、经常发生破坏性改动过程中的一个版本节点，而非稳定里程碑，评论者也指出其生态仍然偏小。用户表示期待的无栈协程 IO 实现和一等公民的 fuzzer 工具，被描述为未来版本的目标而非本次发布的成果；此外还有一位评论者声称因与核心成员产生摩擦而离开了 Zig 生态。

hackernews · ErenayDev · 10月2日 20:56 · [社区讨论](https://news.ycombinator.com/item?id=49938521)

**背景**: Zig 是由 Andrew Kelley 创造、2016 年首次公布的通用系统编程语言，定位为对 C 语言的通用性改进：它不使用宏和预处理器，支持编译期泛型（comptime），需要手动内存管理，并提供 packed struct、任意位宽整数和多种指针类型等底层特性。它以 MIT 许可证开源，由 Zig 软件基金会（ZSF）通过企业赞助和个人捐赠资助开发，每个带标签的版本都会在 ziglang.org 上发布详细的发布说明。由于该语言尚未达到 1.0，版本之间的破坏性改动相当常见，因此发布说明备受用户关注。讨论中关于 LLM 辅助查找 bug 的兴趣，常被追溯到 SQLite 使用 LLM 帮助发现代码缺陷所报告的成果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ziglang.org/">Home Zig Programming Language</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_%28programming_language%29">Zig (programming language)</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的整体氛围偏正面：一位长期以 JS、C、Pascal、Go 为业的开发者称 Zig 是自己尝试过设计最好的语言，另一位则盛赞其目标平台支持可能是唯一能与 C 一较高下的存在，还有不少人对 Kelley 务实地转向 LLM 辅助查找 bug 表示欢迎。反对意见则来自那些指出 Zig 仍不稳定、生态偏小的人，另有一位评论者声称因核心成员对贡献者的态度问题而离开 Zig、转投 Odin。

**标签**: `#Zig`, `#programming languages`, `#systems programming`, `#release notes`, `#LLM-assisted development`

---

<a id="item-5"></a>
## [Google Research 发布 Cogentic 多智能体系统，称在五个开放数学问题上取得新结果](https://arxiv.org/abs/2609.40324v1) ⭐️ 8.0/10

Google Research 提出了 Cogentic——一套面向开放研究问题的自动证明发现多智能体框架，底层以 Gemini 作为基础模型。该系统采用“证明—验证”循环：多个相互独立的证明器分头探索不同方向，另有专门组件进行对抗式验证，据称已在在线学习、拍卖理论和机制设计领域的五个开放问题上产出新结果，并全部由领域专家独立验证、在配套论文中展开论述。 如果这些说法成立，这将是 LLM 驱动数学研究的一个重要里程碑：不再是面对难题容易卡住的单次生成，而是一套协同的多智能体系统被认为在真正开放的问题上产出了经专家验证的新定理。这将把自动定理证明从“辅助复现已知证明”推向“贡献原创研究”，并影响数学家和理论研究者把 AI 当作合作者的方式。 该架构最具特色的部分是可持续使用的验证账本：它累积已确认的结果，使中间进展能在长时间探索中得以保留，并配合对抗式验证而非模型自我检查。但仍需注意：该条目的 arXiv 链接疑似有误且日期在未来（2609.40324），目前也没有独立复现或社区讨论，因此仅凭该投稿无法确认“专家验证”这一说法。

telegram · zaihuapd · 10月2日 12:04

**背景**: 自动定理证明传统上依赖形式化系统和 Lean 之类的证明助手，由机器逐步机械地验证推理；而近年 LLM 常被用来生成非形式化的证明思路，再交给验证环节检查。前沿模型在单次生成中能给出不错的数学想法，但开放问题通常需要探索多个互相竞争的猜想，并在很长的推理链条中克服细微的技术障碍。多智能体方法试图让多个智能体并行生成与相互批评来应对这一点，而“验证账本”是一种已知模式，用于持久记录校验结果，让后续步骤能建立在已被验证的输出之上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.40324">[2609.40324] Cogentic: Multi-Agent Orchestration for ...</a></li>
<li><a href="https://agentpatterns.ai/verification/verification-ledger/">Verification Ledger for Tracking Agent Output Quality</a></li>
<li><a href="https://research.google/blog/towards-a-science-of-scaling-agent-systems-when-and-why-agent-systems-work/">Towards a science of scaling agent systems: When and why ...</a></li>

</ul>
</details>

**标签**: `#multi-agent-systems`, `#automated-theorem-proving`, `#llm-reasoning`, `#google-research`, `#formal-verification`

---