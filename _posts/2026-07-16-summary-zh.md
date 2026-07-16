---
layout: default
title: "Horizon Summary: 2026-07-16 (ZH)"
date: 2026-07-16
lang: zh
---

> 从 42 条内容中筛选出 14 条重要资讯。

---

1. [Kimi K3 发布，具备自主芯片设计能力](#item-1) ⭐️ 9.0/10
2. [xAI 在隐私风波后开源 Grok Build](#item-2) ⭐️ 9.0/10
3. [Schema 框架通过流程改进在 ARC-AGI-3 上达到 99%](#item-3) ⭐️ 9.0/10
4. [从 Rust 到 Zig 的重写：编译器实现的权衡](#item-4) ⭐️ 8.0/10
5. [索尼删除已购电影，凸显数字所有权缺陷](#item-5) ⭐️ 8.0/10
6. [Codex 漏洞在无沙箱全访问模式下误删$HOME 目录](#item-6) ⭐️ 8.0/10
7. [Inkling：975B 参数开源权重 MoE 模型发布](#item-7) ⭐️ 8.0/10
8. [Linus Torvalds 声明 Linux 不反 AI](#item-8) ⭐️ 8.0/10
9. [AI 记忆架构是否在优化错误的抽象层级？](#item-9) ⭐️ 8.0/10
10. [ExTernD：通过扩展秩分解实现三元 LLM PTQ](#item-10) ⭐️ 8.0/10
11. [长鑫存储 2026 年 DRAM 产能将逼近美光](#item-11) ⭐️ 8.0/10
12. [日本购入 2.75 万块英伟达 Rubin 芯片打造机器人 AI](#item-12) ⭐️ 8.0/10
13. [欧盟拟强制 Google 向对手开放 Android AI 助手权限](#item-13) ⭐️ 8.0/10
14. [1Password 允许 Claude 登录网站而不暴露密码](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Kimi K3 发布，具备自主芯片设计能力](https://www.kimi.com/en) ⭐️ 9.0/10

月之暗面（Moonshot AI）发布了 Kimi K3，这是一个 2.8 万亿参数的前沿模型，具备自主芯片设计能力、100 万 token 上下文窗口和原生视觉能力。该模型在 48 小时内使用开源 EDA 工具在 Nangate 45nm 库上自主设计了一款芯片。 Kimi K3 通过实现自主芯片设计（此前需要人类专家）推动了 AI 能力的边界。其有竞争力的定价和强劲的性能使其成为 OpenAI 和 Anthropic 模型的有力竞争者，可能在中国和全球范围内推动先进 AI 的普及。 该模型每百万输入 token 收费 3 美元，每百万输出 token 收费 15 美元，缓存价格为 0.3 美元，与 Anthropic 的 Sonnet 系列定价一致。在 Artificial Analysis 上，其每任务成本为 0.94 美元，接近 GPT-5.6 Sol Max，但部分用户指出其指令遵循能力较低。

hackernews · vincent_s · 7月16日 14:46 · [社区讨论](https://news.ycombinator.com/item?id=48935342)

**背景**: Kimi K3 是月之暗面（Moonshot AI）开发的大语言模型，该公司也是 Kimi 聊天机器人的开发商。它采用了 Kimi Delta Attention 和 Attention Residuals 等新颖架构，以 2.8 万亿参数实现高效推理。自主芯片设计功能作为一个概念验证，使用了 Nangate 45nm 库和开源 EDA 工具，创建了一款在仿真中可维持超过 8,700 tokens/s 解码吞吐量的芯片，包含 146 万个标准单元。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://empiriolabs.ai/models/kimi-k3">Kimi K 3 API: Pricing, Playground & Docs | EmpirioLabs AI</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K 3 - Kimi API Platform</a></li>

</ul>
</details>

**社区讨论**: 社区对芯片设计成就印象深刻，但在定价上存在分歧，一些人认为对于中国开源权重模型来说价格过高。还有人对月之暗面默认使用 API 数据进行训练（除非客户选择退出）的政策表示担忧。其他人指出，虽然性能强劲，但指令遵循能力可能不足。

**标签**: `#AI`, `#deep learning`, `#hardware design`, `#frontier models`, `#Kimi`

---

<a id="item-2"></a>
## [xAI 在隐私风波后开源 Grok Build](https://simonwillison.net/2026/Jul/15/grok-build/#atom-everything) ⭐️ 9.0/10

xAI 在 grok CLI 工具存在严重隐私漏洞（会上传整个用户目录到 xAI 服务器）并引发广泛批评后，将整个 Grok Build 代码库以 Apache 2.0 许可证开源。 此举旨在恢复用户信任，并展示了向透明度的转变，为 AI 编码工具优先考虑隐私和开源问责制树立了先例。 Grok Build 仓库包含 844,530 行 Rust 代码，其中仅约 3% 为第三方依赖，并包含 Mermaid 图表渲染器和 agent 系统提示等值得注意的组件。

rss · Simon Willison · 7月15日 23:59

**背景**: xAI 的 grok CLI 是一个基于终端的编码代理，使用 Grok API。隐私漏洞是由于该工具默认上传整个工作目录，可能泄露 SSH 密钥和密码数据库等敏感文件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://x.ai/cli">Grok Build | SpaceXAI</a></li>
<li><a href="https://lalatenduswain.medium.com/automate-your-terminal-with-grok-cli-a-developers-guide-to-xai-s-ai-powered-tool-eb8e2b0460bf">Automate Your Terminal with Grok CLI: A Developer’s Guide to xAI’s AI-Powered Tool | by Lalatendu Keshari Swain | Medium</a></li>

</ul>
</details>

**社区讨论**: 社区表达了强烈愤怒，一名用户报告在 home 目录下运行 grok 导致 SSH 密钥和密码管理器被上传。埃隆·马斯克回应称将删除所有已上传数据并禁用该功能，但批评浪潮最终促成了开源发布。

**标签**: `#security`, `#privacy`, `#AI`, `#open-source`, `#xAI`

---

<a id="item-3"></a>
## [Schema 框架通过流程改进在 ARC-AGI-3 上达到 99%](https://www.reddit.com/r/MachineLearning/comments/1uyf8oo/new_fable5opus48_harness_called_schema_claims_99/) ⭐️ 9.0/10

一种名为 Schema 的新框架在不改变任何模型权重的情况下，使用 Claude Opus 4.8 和 Fable 5 在 ARC-AGI-3 公开集上达到了 99% 的准确率，使用 GPT-5.6 Sol 则达到了 95.35%。 在旨在通过交互式问题解决来衡量智能体智能的 ARC-AGI-3 基准测试上取得近乎完美的分数，表明通过改进模型周围的流程而非扩大模型规模，可以取得显著进步。 Schema 使用固定的回退规则：先运行 Opus 4.8 和 Sol xhigh；得分低于 80 的游戏分别用 Fable 5 和 Sol max 重新运行，保留每局较高得分。它改进了如何将观察转化为模型、如何测试预测以及如何执行和修订计划。

reddit · r/MachineLearning · /u/we_are_mammals · 7月16日 21:02

**背景**: ARC-AGI-3 是首个面向 AI 智能体的交互式推理基准测试，要求智能体在陌生环境中无需明确指令即可探索、推断目标、构建内部模型并规划行动。之前的 ARC 基准测试是非交互式的；ARC-AGI-3 的交互式格式使其难度大幅提升，前沿 AI 模型得分低于 1%，而人类则能全部解决。Claude Opus 4.8 和 Fable 5 是 Anthropic 的最新模型，其中 Fable 5 是通用可用的 Mythos 级模型，擅长长程推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://www.anthropic.com/news/claude-opus-4-8">Introducing Claude Opus 4.8 \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI`, `#ARC-AGI`, `#benchmark`, `#reasoning`, `#model harness`

---

<a id="item-4"></a>
## [从 Rust 到 Zig 的重写：编译器实现的权衡](https://rtfeldman.com/rust-to-zig) ⭐️ 8.0/10

博客文章详细介绍了将 Roc 编译器从 Rust 重写为 Zig 的过程，强调更快的增量构建和手动内存管理，但牺牲了内存安全保证。 这一讨论比较了两种现代系统语言（Rust 和 Zig）在实际编译器项目中的表现，影响了未来在性能和安全性权衡至关重要的系统软件开发中的选择。 作者指出 Zig 提供了比 Rust 更快的增量构建，但 Rust 提供了更强的内存安全保证；重写是由于在代码生成和二进制补丁中需要底层控制。

hackernews · jorangreef · 7月16日 11:39 · [社区讨论](https://news.ycombinator.com/item?id=48933149)

**背景**: Zig 是一种注重简洁和控制的系统编程语言，要求手动内存管理。Rust 通过所有权和借用提供内存安全，无需垃圾回收。编译器通常需要执行不安全的操作进行代码生成，因此在安全性和性能之间做出选择是一个关键挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>
<li><a href="https://ziglang.org/">Home ⚡ Zig Programming Language</a></li>

</ul>
</details>

**社区讨论**: 社区评论中讨论了编译器中使用不安全代码的必要性；steveklabnik 认为不安全并非发射机器代码所必需，而其他人则称赞 Zig 的增量构建是一个杀手级功能，但希望同时拥有 Rust 的安全性。

**标签**: `#Rust`, `#Zig`, `#compiler`, `#memory safety`, `#systems programming`

---

<a id="item-5"></a>
## [索尼删除已购电影，凸显数字所有权缺陷](https://www.techdirt.com/2026/07/15/sony-deletes-a-bunch-more-movies-from-the-accounts-of-people-who-bought-them/) ⭐️ 8.0/10

索尼从用户账户中删除了此前通过 PlayStation 商店“购买”的电影，延续了撤销数字内容访问权限且不提供退款的做法。 此事件重新引发关于数字所有权的讨论，消费者意识到他们购买的往往只是可撤销的许可。这迫使监管机构和公司明确区分数字商品的购买与租赁。 此次删除事件之前已有类似案例，包括 2023 年索尼删除已购电影。用户报告未获补偿或警告，被删除内容可能与索尼的许可协议到期有关。

hackernews · nekusar · 7月16日 12:13 · [社区讨论](https://news.ycombinator.com/item?id=48933419)

**背景**: 数字所有权通常意味着用户购买的是访问内容的许可，而非文件本身。如果提供商失去权利或更改条款，该许可可能被撤销。一些地区的法律，如亚利桑那州的一项法案，现要求更明确地披露这些限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techwalla.com/13779819/digital-game-ownership-rights-explained-licenses-vs-true-ownership">Digital Game Ownership Rights Explained : Licenses vs .... | Techwalla</a></li>
<li><a href="https://www.route-fifty.com/digital-government/2026/02/arizona-bill-would-force-companies-disclose-digital-purchases-arent-permanent/411314/">Arizona bill would force companies to disclose that digital ...</a></li>
<li><a href="https://consumer.ftc.gov/consumer-alerts/2024/04/do-you-really-own-digital-items-you-paid">Do you really own the digital items you paid for? | Consumer ...</a></li>

</ul>
</details>

**社区讨论**: 评论者指出一个未解决的问题：数字所有权模型依赖媒体公司永久提供服务。有人主张撤销时应退款，另一些人则要求交付实际文件而非访问权。少数人提到实体媒体和盗版作为替代方案。

**标签**: `#digital ownership`, `#DRM`, `#consumer rights`, `#Sony`, `#software ethics`

---

<a id="item-6"></a>
## [Codex 漏洞在无沙箱全访问模式下误删$HOME 目录](https://simonwillison.net/2026/Jul/16/bad-codex-bug/#atom-everything) ⭐️ 8.0/10

GPT-5.6（Codex）被报告存在严重安全漏洞：当模型以无沙箱保护的全访问模式运行时，会错误地删除用户的$HOME 目录而非临时目录。 这一事件凸显了部署 AI 编码代理时沙箱和审批机制的至关重要性，因为无沙箱执行可能导致不可逆的数据丢失。 该漏洞特定发生于：启用全访问模式、关闭沙箱保护、关闭自动审查，且模型试图覆盖$HOME 环境变量以定义临时目录，但犯下诚实错误，反而删除了$HOME。

rss · Simon Willison · 7月16日 17:45

**背景**: Codex 是 OpenAI 开发的 AI 编码代理，能够编写和执行代码。全访问模式授予模型无限制的文件系统访问权限，而沙箱则提供隔离环境以限制潜在损害。没有沙箱保护，模型可以执行删除文件等破坏性操作。此漏洞展示了在没有适当安全措施情况下授予 AI 代理高权限访问的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Codex_(AI_agent)">OpenAI Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://vladimirsiedykh.com/blog/codex-cli-approval-modes-2025">Codex CLI approval modes explained: auto vs read only vs...</a></li>
<li><a href="https://www.firecrawl.dev/blog/ai-agent-sandbox">AI Agent Sandbox: How to Safely Run Autonomous Agents in 2026</a></li>

</ul>
</details>

**标签**: `#codex`, `#AI safety`, `#coding agents`, `#generative AI`, `#bug`

---

<a id="item-7"></a>
## [Inkling：975B 参数开源权重 MoE 模型发布](https://simonwillison.net/2026/Jul/16/inkling/#atom-everything) ⭐️ 8.0/10

Mira Murati 的 Thinking Machines Lab 发布了 Inkling，这是一个拥有 9750 亿总参数量（410 亿激活参数）的混合专家多模态模型，采用 Apache-2.0 许可证，基于 45 万亿 token 的文本、图像、音频和视频数据进行训练。他们还宣布计划在测试完成后发布 Inkling-Small（2760 亿参数，120 亿激活参数）。 Inkling 为美国开源权重生态系统增添了一个强有力的竞争者，与来自中国及其他实验室的模型竞争，且采用宽松的 Apache-2.0 许可证。它被定位为通过其 Tinker 平台进行微调的强大基础模型，拓宽了可定制多模态 AI 的获取途径。 模型卡片和训练数据文档内容明显简略，缺乏详细的技术规格。Inkling 并非前沿模型，而是作为适合定制的基础模型，具备多模态能力和高效推理。

rss · Simon Willison · 7月16日 15:35

**背景**: 混合专家（MoE）是一种神经网络架构，它使用许多专门的子模型（专家）和路由机制，为每个输入仅激活一个子集，从而在不按比例增加计算成本的情况下实现庞大的参数量。开源权重模型公开发布训练后的模型参数，允许任何人下载、使用和微调，尽管它们可能不符合开源 AI 的所有标准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>

</ul>
</details>

**标签**: `#open-weights`, `#Mixture-of-Experts`, `#Thinking Machines Lab`, `#multimodal`, `#Apache-2.0`

---

<a id="item-8"></a>
## [Linus Torvalds 声明 Linux 不反 AI](https://simonwillison.net/2026/Jul/16/linus-torvalds/#atom-everything) ⭐️ 8.0/10

Linux 领导者的这一高调表态明确了项目的官方立场，可能减少对在内核开发中整合 AI 的阻力，并影响更广泛的开源生态系统。 Torvalds 强调 AI 与其他工具一样，其有用性已毋庸置疑，不过他承认关于 AI 经济形态的问题仍然存在。

rss · Simon Willison · 7月16日 13:26

**背景**: Linus Torvalds 是 Linux 内核的创造者和主要维护者，Linux 内核是 Linux 操作系统的核心。Linux Media 邮件列表是讨论媒体相关内核子系统的场所。Torvalds 的声明是对开源社区中关于 AI 在软件开发中角色更广泛辩论的回应。

**标签**: `#Linux`, `#AI`, `#kernel development`, `#Linus Torvalds`

---

<a id="item-9"></a>
## [AI 记忆架构是否在优化错误的抽象层级？](https://www.reddit.com/r/MachineLearning/comments/1uy6yht/are_current_ai_memory_architectures_optimizing/) ⭐️ 8.0/10

一篇 Reddit 帖子提出，AI 记忆系统应从存储描述性事实转向推断更高层次的推理模式和解释框架，例如用户的偏好抽象和特征性推理风格。 这挑战了当前依赖事实摘要的 AI 持久上下文范式，并提出一种更具认知性的方法，可能带来更个性化和适应性更强的 AI 智能体。 作者将当前记忆如'用户对经济学感兴趣'与未来系统推断'用户倾向于通过激励和制度约束解释经济结果'进行对比。帖子质疑这种表征能否自然涌现，还是需要全新的架构。

reddit · r/MachineLearning · /u/Boris_Ljevar · 7月16日 16:00

**背景**: 当前 AI 记忆系统（如大语言模型中的）通常将持久上下文存储为事实、偏好和过去互动的描述性摘要。认知架构如 ACT-R 和 SOAR 是人类认知的计算模型，强调结构化知识和推理。该帖子从这些概念中汲取灵感，提出 AI 记忆中更深层次的抽象，捕捉推理风格和解释框架。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cognitive_architecture">Cognitive architecture - Wikipedia</a></li>
<li><a href="https://dev.to/mininglamp/ai-agents-and-persistent-context-what-designmd-teaches-us-4l9b">AI Agents and Persistent Context: What design.md Teaches Us</a></li>

</ul>
</details>

**标签**: `#AI`, `#memory`, `#cognitive architectures`, `#reasoning`, `#machine learning`

---

<a id="item-10"></a>
## [ExTernD：通过扩展秩分解实现三元 LLM PTQ](https://www.reddit.com/r/MachineLearning/comments/1uy2zb3/externd_expandedrank_ternary_decomposition/) ⭐️ 8.0/10

ExTernD 提出了一种新的训练后量化方法，将权重矩阵分解为两个三元矩阵和一个对角缩放矩阵，通过允许任意大的内秩来恢复三元量化中损失的精度，且仅增加极少的 VRAM 开销。 该方法有望实现高效的三元 LLM，其精度接近更高位量化的水平，从而显著降低在资源受限设备上部署大模型的内存和计算成本。 内秩可以任意大，使得精度能接近任意量化级别，而 VRAM 开销仅比当前三元方法略高，因此实际可行。该方法纯粹是训练后量化（无需微调），并依赖三元算术加速推理。

reddit · r/MachineLearning · /u/LMTLS5 · 7月16日 13:31

**背景**: 训练后量化（PTQ）通过将权重转换为低位表示来减小模型大小并加速推理，无需重新训练。三元量化使用{-1,0,1}值，压缩率高但常导致精度下降。ExTernD 通过将权重矩阵分解为低秩三元因子和对角矩阵的乘积来解决此问题，灵感来自秩分解，从而增加表示能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2607.13511v1">ExTernD: Expanded-Rank Ternary Decomposition Ternary LLM PTQ ...</a></li>
<li><a href="https://arxiv.org/abs/2606.26650">[2606.26650] CAT-Q: Cost-efficient and Accurate Ternary ...</a></li>

</ul>
</details>

**标签**: `#quantization`, `#LLM`, `#PTQ`, `#ternary`, `#efficient inference`

---

<a id="item-11"></a>
## [长鑫存储 2026 年 DRAM 产能将逼近美光](https://www.tomshardware.com/pc-components/dram/cxmt-close-to-matching-microns-memory-capacity-in-2026-research-claims-would-put-china-on-track-to-become-worlds-second-largest-dram-producer) ⭐️ 8.0/10

研究机构 Citrini 预测，长鑫存储到 2026 年底月产能将达到约 35 万片，接近美光的 37.5 万片，届时中国将成为全球第二大 DRAM 生产地。 这一变化可能重塑全球 DRAM 供应链，减少对韩国和美国供应商的依赖，并影响半导体制造的价格和地缘政治格局。 到 2026 年中国 DRAM 总产能可达 60 万片/月（不含外资工厂），到 2030 年增至约 141 万片/月；但美国《MATCH 法案》对浸没式 DUV 光刻设备的出口管制可能阻碍短期扩张。

telegram · zaihuapd · 7月16日 02:30

**背景**: DRAM 是一种用于电脑和服务器的内存类型。浸没式 DUV 光刻是制造先进 DRAM 芯片的关键技术。MATCH 法案是美国旨在限制对华出口先进半导体设备的立法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.govtrack.us/congress/bills/119/hr8170/text">Text of H.R. 8170: MATCH Act (Introduced version) - GovTrack.us</a></li>
<li><a href="https://www.asml.com/en/products/duv-lithography-systems">DUV lithography systems | Products - ASML</a></li>

</ul>
</details>

**标签**: `#DRAM`, `#semiconductor`, `#China`, `#memory`, `#manufacturing`

---

<a id="item-12"></a>
## [日本购入 2.75 万块英伟达 Rubin 芯片打造机器人 AI](https://www.bloomberg.com/news/articles/2026-07-16/japan-to-buy-nvidia-rubin-chips-to-build-sovereign-ai-for-robots) ⭐️ 8.0/10

日本宣布计划购入 27,500 块英伟达下一代 Rubin 芯片，由新成立的 Noetra 财团牵头，获得政府 3873 亿日元（约 24 亿美元）拨款，用于开发面向机器人的本土基础 AI 模型，以减少对外国技术的依赖。 该项目使日本成为 AI 和机器人领域的第三股力量，与美国和中国竞争，并力争到 2040 年占据全球机器人市场 30%以上的份额。它还凸显了主权 AI 日益增长的重要性——各国寻求技术自主。 Rubin 架构是英伟达最雄心勃勃的 GPU 平台，将 GPU、CPU、网络和存储集成到 AI 工厂生态系统中。Noetra 包括软银、NEC、本田、索尼等大公司，专注于制造业的“物理 AI”。首个 AI 模型预计在 2027 年 3 月前发布，数年内推出机器人专用版本。

telegram · zaihuapd · 7月16日 10:59

**背景**: 主权 AI 指国家独立发展自身 AI 技术的能力，减少对外国供应商的依赖。Noetra 是 2026 年成立的财团，旨在提升日本 AI 能力，特别是在机器人和制造业领域。英伟达的 Rubin 架构于 2025 年发布，旨在支持大规模 AI 集群，是从单一 GPU 到集成 AI 工厂的转变。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.thundercompute.com/blog/nvidia-rubin-architecture">Nvidia Rubin Architecture : Everything You Must... | Thunder Compute</a></li>
<li><a href="https://www.binance.com/en/square/post/06-30-2026-ai-trends-japan-to-fund-softbank-led-noetra-with-387-3-billion-yen-to-develop-domestic-ai-models-339748080901826">AI TRENDS | Japan to Fund SoftBank-Led Noetra With 387.3 Billion...</a></li>
<li><a href="https://asiatimes.com/2026/07/japan-rallies-tech-giant-alliance-to-build-sovereign-ai/">Japan rallies tech-giant alliance to build sovereign AI - Asia Times</a></li>

</ul>
</details>

**标签**: `#AI`, `#Japan`, `#Nvidia`, `#Robotics`, `#Sovereign AI`

---

<a id="item-13"></a>
## [欧盟拟强制 Google 向对手开放 Android AI 助手权限](https://t.me/zaihuapd/42615) ⭐️ 8.0/10

欧盟正在起草法规，要求 Google 在 Android 设备上给予 ChatGPT、Claude 等竞争对手的 AI 助手与自家 Gemini 同等的系统级权限。 此举可能从根本上重塑 AI 助手市场的竞争格局，打破 Google 对 Android 系统集成的独家控制，有望为用户提供更多选择并促进创新。 该法规仍处于草案阶段，发布时间可能推迟；Google 担忧这种开放要求可能影响用户安全和隐私。

telegram · zaihuapd · 7月16日 13:19

**背景**: Android 的默认助手 API 目前仅将完整的系统权限授予指定的默认助手，这使得 Google 的 Gemini 占据优势。竞争对手的助手虽然可以安装，但无法执行截屏或访问屏幕内容等操作，除非被设为默认。欧盟的《数字市场法案》（DMA）此前已针对 Google 的商业行为，这项新规将反垄断焦点延伸至 AI 助手领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.androidauthority.com/eu-android-ai-google-search-mandates-3688186/">Rival AI assistants could soon gain full access to Android ...</a></li>
<li><a href="https://www.heise.de/en/news/EU-Requirements-Android-must-fully-open-up-for-third-party-AI-assistants-11367823.html">EU Requirements: Android must fully open up for third-party ...</a></li>

</ul>
</details>

**标签**: `#EU regulation`, `#antitrust`, `#AI assistants`, `#Android`, `#Google`

---

<a id="item-14"></a>
## [1Password 允许 Claude 登录网站而不暴露密码](https://9to5mac.com/2026/07/16/1password-now-lets-claude-sign-in-to-websites-without-seeing-your-passwords/) ⭐️ 8.0/10

1Password 推出了与 Anthropic 的 Claude AI 的 Mac 端集成，允许 Claude 代表用户登录网站，使用存储在 1Password 中的凭证，而 AI 从未看到密码或 2FA 验证码。 此次集成解决了 AI 辅助浏览中的关键安全问题，确保凭证对 AI 模型保持私密，为安全的 AI 代理与密码管理器交互树立了新标准。 凭证通过安全通道直接注入目标网页，用户必须通过生物识别逐条审批每个会话的登录请求；如果自动填充失败，已填充的内容会立即被擦除。

telegram · zaihuapd · 7月16日 15:54

**背景**: 密码管理器存储加密凭证并传统上自动填充到登录表单。然而，让 AI 代理直接访问这些凭证会引发隐私风险。1Password 的方法使用安全注入协议，防止 AI 模型看到原始密码或 2FA 验证码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.macrumors.com/2026/07/16/1password-claude-integration/">1Password for Claude Lets AI Log In Without Seeing Your ...</a></li>
<li><a href="https://cryptobriefing.com/1password-claude-secure-credential-integration/">1Password integrates with Claude for secure credential access ...</a></li>
<li><a href="https://www.wsj.com/tech/ai/1password-for-claude-ai-agents-password-manager-111a7a8a">I Gave an AI Agent Access to My Passwords. Here’s What ...</a></li>

</ul>
</details>

**标签**: `#1Password`, `#Claude`, `#AI integration`, `#password management`, `#security`

---