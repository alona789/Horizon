---
layout: default
title: "Horizon Summary: 2026-09-11 (ZH)"
date: 2026-09-11
lang: zh
---

> 从 36 条内容中筛选出 7 条重要资讯。

---

1. [Calif Research 发布 WeWorm：AI 协助打造的微信零点击蠕虫](#item-1) ⭐️ 9.0/10
2. [Shopify 放弃 React Native，回归原生 Swift 与 Kotlin 开发](#item-2) ⭐️ 8.0/10
3. [研究者质疑能否放心把未发表的数学想法交给 OpenAI](#item-3) ⭐️ 8.0/10
4. [微软正式将 Rust 列为一级\(Tier-1\)语言](#item-4) ⭐️ 8.0/10
5. [trynix.dev 让你在浏览器里启动过去 13 年的任意 Nix 软件包](#item-5) ⭐️ 8.0/10
6. [SemiAnalysis 深度解析：数据中心「表后供电」为何如此困难](#item-6) ⭐️ 8.0/10
7. [真实果蝇连接组学不会打乒乓球，审计过程才是真正的看点](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Calif Research 发布 WeWorm：AI 协助打造的微信零点击蠕虫](https://simonwillison.net/2026/Sep/10/calif-research/) ⭐️ 9.0/10

Calif Research 发布了一个名为 WeWorm 的演示，声称这是首个可通过微信通话在 iOS 和 Android 上传播的零点击蠕虫。该团队表示，借助 AI 他们在约两天内找到了漏洞并写出首个远程代码执行（RCE）利用程序，随后又用一周时间构建出蠕虫。 如果得到验证，这将成为攻击性安全与 AI 风险领域的双重里程碑：针对一款拥有超过十亿用户的通讯应用，构建出可自我传播的零点击攻击，而耗时仅数天而非数月。这也表明 AI 正在压缩把漏洞转化为可用利用程序所需的时间与团队规模，从而降低大规模攻击的门槛。 据 Calif Research 描述，受害者完全不需要接听通话或对手机做任何操作，即便接听也听不到任何声音，利用仍然成功。需要注意的局限在于：这是一份演示而非完整披露的安全公告，目前没有独立的第三方验证，也未给出受影响的版本号或修补状态。

rss · Simon Willison · 9月10日 00:56

**背景**: 零点击攻击是指存在漏洞的应用或服务在处理恶意输入时自动触发的攻击，无需钓鱼链接之类的用户欺骗手段。远程代码执行（RCE）指攻击者能够通过网络在目标设备上运行任意代码，通常是植入恶意软件或窃取数据的跳板；而蠕虫则是一种无需用户操作就能从一台设备自我复制到另一台设备的恶意软件。AI 辅助漏洞发现是近年兴起的方向，模型可帮助研究人员发现甚至修复原本容易被忽视的缺陷，而本次事件是该能力被用于利用程序开发的早期案例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kaspersky.com/resource-center/definitions/what-is-zero-click-malware">Zero-Click Exploits</a></li>
<li><a href="https://en.wikipedia.org/wiki/Remote_code_execution">Remote code execution</a></li>
<li><a href="https://www.vulncheck.com/blog/ai-assisted-vulnerability-discovery">The First CVE Wave: Signs That AI-Assisted Vulnerability Discovery Is Reshaping Disclosure Volumes | Blog | VulnCheck</a></li>

</ul>
</details>

**标签**: `#security`, `#AI`, `#WeChat`, `#zero-click exploit`, `#RCE`

---

<a id="item-2"></a>
## [Shopify 放弃 React Native，回归原生 Swift 与 Kotlin 开发](https://shopify.engineering/back-to-native) ⭐️ 8.0/10

Shopify 宣布其移动应用将放弃 React Native，回归使用 Swift 开发 iOS、Kotlin 开发 Android 的完全原生路线。这篇工程博客在 Hacker News 上引发了近 500 条评论，被视为 Shopify 对早先押注单一 JavaScript 跨平台共享代码库这一策略的逆转。 Shopify 运营着全球流量最高的电商应用之一，因此它从 React Native 撤退对跨平台与原生开发之争具有重要的信号意义。这也强化了业界日益流行的一种观点：像 Shopify 这种体量的公司最终会希望拥有能针对各平台单独优化的专職原生工程师。 据报道，这次迁移的做法是依据现有的 React Native 代码逐屏重写，并创建独立的 Android 与 iOS 目录，同时借助 Maestro 等工具进行应用测试。有评论者指出，跨越 JavaScript、C++ 和原生线程的崩溃调试，其成本可能比直接维护两套代码库还高。

hackernews · fnthawar2 · 9月10日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=49643982)

**背景**: React Native 由 Meta 维护，允许开发者用 JavaScript 和 React 编写移动应用，并在 iOS 与 Android 之间共享大部分代码，其吸引力在于 Web 开发者也能直接参与移动端开发。Swift 是 Apple 为 iOS 和 macOS 应用打造的编译型语言，Kotlin 则是 JetBrains 推出的静态类型语言，也是现代 Android 开发的首选。其代价在于：跨平台框架减少了重复工作，却增加了抽象层，使性能调优与原生调试变得更困难。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://reactnative.dev/">React Native</a></li>
<li><a href="https://en.wikipedia.org/wiki/Swift_%28programming_language%29">Swift (programming language) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Kotlin">Kotlin - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论总体倾向于支持脱离 React Native，一位 iOS 工程师表示这一决定验证了他多年来反对共享代码库的坚持。不过，也有不少评论者反驳“是大模型让迁移首次变得可负担”的说法，指出类似的代码重写在大模型辅助出现之前就已完成，而模型只是在生成原生应用方面变得更擅长了。

**标签**: `#React Native`, `#Mobile Development`, `#Swift`, `#Kotlin`, `#Cross-Platform`

---

<a id="item-3"></a>
## [研究者质疑能否放心把未发表的数学想法交给 OpenAI](https://mathstodon.xyz/@andreasthom/117240535270608201) ⭐️ 8.0/10

Mastodon 用户 @andreasthom 发起的一场讨论引发关注：在有报道称 OpenAI 利用研究者的协作对话得出研究成果、却未给予署名之后，数学家们是否还能放心地把尚未发表的想法分享给 OpenAI。讨论中还提到，OpenAI 声称用于生成某项结果的模型并未在这些协作对话上训练过。 这一事件触及 AI 实验室与学术界互动时的研究伦理与署名规范这一根本问题，可能导致研究者不再愿意使用商业模型或向其分享想法。它也牵涉更广泛的争论：AI 究竟是在真正解决未决问题，还是其“发现”其实来自被喂入的那些想法。 相关说法仍有争议：有人认为在用户对话上做预训练会微妙地提升模型的潜在直觉，也有人指出在可验证数学任务上用大规模算力做强化学习，本身就可能独立地产生超越人类的技巧。另一个复杂细节是，有报道称 OpenAI 在得知某个重要数学证明可能存在于训练数据中之后不久，就让一个仍在训练中的模型生成了约 3000 亿个输出 token。

hackernews · pred\_ · 9月10日 06:49 · [社区讨论](https://news.ycombinator.com/item?id=49639408)

**背景**: 像 OpenAI 这样的大语言模型是分阶段训练的，包括在海量文本语料上做预训练，以及在数学题等可自动验证的任务上做强化学习。在数学界，署名与优先权至关重要，因为证明或定理的首创权就是核心的学术回报，因此未经致谢地使用他人未发表的想法被视为严重违反学术规范。争论的焦点在于：接收研究者私人想法的 AI 公司究竟相当于负有署名义务的合作者，还是仅仅是一个工具提供方。

**社区讨论**: 评论者总体上认为这一情况令人不安。有人用“人类合作者”作类比，认为如果换成真人这样做显然是不道德的；也有人主张两件事可以同时成立——对话数据可能提升了模型直觉，而强化学习也可能独立发现结果。还有人担心研究者在被引导去攻破新问题的同时，成果却被吸取，并指出 3000 亿输出 token 的时机很可疑，同时质疑人们究竟该在多大程度上信任公司保管自己的数据。

**标签**: `#AI ethics`, `#OpenAI`, `#research integrity`, `#mathematics`, `#AI safety`

---

<a id="item-4"></a>
## [微软正式将 Rust 列为一级\(Tier-1\)语言](https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/) ⭐️ 8.0/10

在 Rust 基金会发布的一篇客座文章中,微软确认 Rust 已在公司内部正式获得一级\(tier-1\)语言地位,在新建系统级项目时与 C++ 等长期主力语言并列可选。与此同时,此前仅停留在传闻层面的 MSVC 工具链对 Rust 的集成也有了新的公开信号。 微软是全球最大的 C 和 C++ 代码持有方之一,因此赋予 Rust 一级语言地位,意味着内存安全的系统级语言已从实验性选择变成企业主流默认选项。这也进一步巩固了 Rust 在“更好的 C/C++”这一赛道中的地位,而当前各大操作系统厂商都在为新建项目扩充可用的系统级语言,这一变化尤为关键。 一级语言地位并不等于与 C++ 平起平坐:文章指出,经过数十年积累,C++ 仍然占据主导,社区成员也提出 Visual Studio 中“一级水准”的调试支持目前仍是个未知数。评论者还引用了微软公开的目标——借助自动化工具在 2030 年前把 10 亿行 C/C++ 代码转换为 Rust,其效率目标被描述为“1 名工程师、1 个月、100 万行代码”,此外还有由 DARPA 资助、六支团队分别探索不同 C 到 Rust 自动转换路径的项目。

hackernews · mmastrac · 9月10日 13:39 · [社区讨论](https://news.ycombinator.com/item?id=49643546)

**背景**: 在大型软件厂商内部,编程语言通常按其获得的官方投入程度分级,包括编译器、构建系统、调试器、库以及安全审查流程等方面的支持;被列为一级语言意味着工程师无需额外审批即可用它开发生产环境代码。Rust 是一门系统级编程语言,于 2015 年发布 1.0 版本,其核心卖点是在编译期强制保证内存安全,从而在源头杜绝缓冲区溢出、释放后使用\(use-after-free\)等一整类缺陷。这对微软尤为重要,因为其产品历史上的安全漏洞\(CVE\)中,绝大多数都源于 C 和 C++ 代码的内存安全问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/">Guest Post: Rust Is Tier - 1 Language at Microsoft</a></li>
<li><a href="https://news.ycombinator.com/item?id=49643546">Rust Is Tier - 1 Language at Microsoft | Hacker News</a></li>
<li><a href="https://markaicode.com/legacy-code-migration-c-to-rust-tools-2025/">C to Rust Migration in 2025: Tools , Strategies, and... | Markaicode</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论\(592 分、334 条评论\)整体态度积极:有评论者认为,这类公告说明 Rust 不再是那个“快速迭代、打破常规”的年轻语言,而是 C++ 和 C\# 的成熟竞争者,相比之下 Zig、Odin 等“更好的 C”阵营的对手仍然毛刺较多。一位有五年 Rust 职业开发经验的工程师表示,如今做高层应用开发已经没有技术理由再选其他语言;也有人乐见各大操作系统厂商在系统级语言上多元化,并追问 Visual Studio 何时才能提供真正一级水准的 Rust 调试支持。

**标签**: `#Rust`, `#Microsoft`, `#programming-languages`, `#systems-programming`, `#software-engineering`

---

<a id="item-5"></a>
## [trynix.dev 让你在浏览器里启动过去 13 年的任意 Nix 软件包](https://simonwillison.net/2026/Sep/10/trynix/) ⭐️ 8.0/10

Farid Zakaria 发布了 trynix.dev，它借助 qemu-wasm 在浏览器中完整运行一个 x86\_64 Linux 虚拟机，并可用过去 13 年间构建的任意 Nix 软件包启动该虚拟机。这些环境可通过 URL 直接寻址，例如访问 https://trynix.dev/?pkg=python3%403.6.2 就能进入一个运行 2017 年 Python 3.6.2 的交互式 shell；他还发布了 trynix-preview 这个 GitHub Action，会在 pull request 下评论一个链接，让评审者直接在浏览器里启动该 PR 的构建产物。 它极大降低了复现历史软件环境的门槛：无需在本地重建十年前的整套工具链，任何人打开一个链接就能获得可用的 shell。trynix-preview 还展示了它在代码审查和 CI 验证中的实际价值，评审者无需准备任何服务器，就能直接启动 pull request 生成的构建产物。 浏览器中的虚拟机基于 ktock 的 qemu-wasm，它把 QEMU 的 TCI 解释器与 TCG 后端结合起来，只把被多次执行（例如执行上千次）的翻译块编译成 WebAssembly。整个流程完全在客户端运行、不需要服务器，但它依赖 Nix 已缓存的二进制构建产物，页面刷新后状态不会保留，而且用 Wasm 模拟完整的 x86\_64 机器在速度上天然慢于本地原生执行。

rss · Simon Willison · 9月10日 23:44

**背景**: Nix 是 Eelco Dolstra 于 2003 年创建的纯函数式包管理器，它把构建结果存放在一个不可变的 store 中，地址由完整依赖树的哈希决定，因此构建可复现，并且同一软件包的多个版本可以共存。正是这种内容寻址的存储机制，让 trynix.dev 能够可靠地取回多年前构建的软件包。qemu-wasm 则是通过 Emscripten 编译成 WebAssembly 的 QEMU 模拟器，使完整的 Linux 系统可以运行在浏览器标签页中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ktock/qemu-wasm">GitHub - ktock/ qemu - wasm : QEMU on browser · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nix_%28package_manager%29">Nix (package manager)</a></li>
<li><a href="https://nixos.org/">Nix &amp; NixOS | Declarative builds and deployments</a></li>

</ul>
</details>

**标签**: `#nix`, `#webassembly`, `#virtualization`, `#qemu`, `#developer-tools`

---

<a id="item-6"></a>
## [SemiAnalysis 深度解析：数据中心「表后供电」为何如此困难](https://newsletter.semianalysis.com/p/what-is-so-hard-about-behind-the) ⭐️ 8.0/10

SemiAnalysis 发布了深度分析通讯的第一部分，专门探讨数据中心「表后供电」（behind-the-meter power）方案在技术与经济层面面临的挑战，副标题为「愚蠢的科学实验 vs. 印钞机」。文章构建了一个对比框架，区分那些在科学上看似有趣但过于投机、与那些真正能产生可观利润回报的供电方案。 随着 AI 训练与推理需求激增，制约数据中心扩张的核心瓶颈已从土地和资本转变为电力，因此运营商获取电力的方式直接决定了新增 AI 算力上线速度。表后发电正被越来越多地宣传为绕开拥堵的电网并网排队的手段，这使得该分析对超大规模云厂商、公用事业公司和基础设施投资者都具有直接参考价值。 表后系统把发电资产直接放在用户电表之后，使数据中心能够独立于公共电网满足主要用电需求，这与标准的购电协议（PPA）或公用事业供电合同截然不同。这类方案通常依赖由燃气轮机、燃料电池或模块化核反应堆驱动的微电网，同时也带来各自的融资、监管与技术风险。

rss · Semianalysis · 9月10日 14:28

**背景**: 「表后供电」指的是设施在电表的用户侧自行发电，而非从电网购电，从而将数据中心的用电需求与社区用电区分开来。这一点之所以重要，是因为在主要数字枢纽，电网并网排队往往长达数年，而电力（而非空间）已成为现代数据中心的关键制约因素。代价是运营商必须自行承担燃料供应、许可审批、排放和可靠性等原本由公用事业公司负责的义务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.williams.com/2026/03/17/powering-data-centers-behind-the-meter-power-explained/">Powering data centers: behind-the-meter power, explained | Williams Companies</a></li>
<li><a href="https://datacenterhawk.com/resources/market-insights/behind-the-meter-power-solutions-the-data-center-industry-s-new-reality">Behind-the-Meter Power Solutions: The Data Center Industry&#x27;s New Reality - datacenterHawk</a></li>
<li><a href="https://www.aoshearman.com/en/insights/data-center-insights/powering-data-centers-the-rise-and-challenges-of-the-behind-the-meter-model">Data centers and the rise of behind-the-meter power</a></li>

</ul>
</details>

**标签**: `#datacenters`, `#power-infrastructure`, `#AI-infrastructure`, `#energy`, `#behind-the-meter`

---

<a id="item-7"></a>
## [真实果蝇连接组学不会打乒乓球，审计过程才是真正的看点](https://www.reddit.com/r/MachineLearning/comments/1wc67ci/i_tried_to_make_a_real_fly_connectome_learn_to/) ⭐️ 8.0/10

一位开发者尝试用新发布的 MaleCNS v1.0 果蝇连接组（16.6 万个神经元，基于真实电子显微镜重建）中的一个小型真实子图，通过类多巴胺可塑性来学习打乒乓球，结果完全没有学会。审计失败原因时发现了一个 neuPrint 正则表达式 bug（静默地把两个神经元群体清零）、一套从感光细胞出发没有任何通路的神经元选择，以及一些从任何感觉通路都没有任何突触连接、无论如何都不可能放电的运动神经元。 本周疯传的「果蝇大脑玩 Doom / Minecraft / Beat Saber」视频被当成连接组规模仿真能产生涌现行为的证据，但作者指出这些项目自己的代码仓库和创作者回复都承认：它们要么没通过自身的验证门槛，要么真实运动检测通路始终静默，要么行为是手工注入的。这个负面结果对「基于连接组的学习」这一说法的评估方式提出了急需的方法论检验，对任何容易把游戏引擎演示当成证据的计算神经科学或机器学习从业者都很有价值。 即便修好 bug、跑通流程之后，开启与关闭可塑性在多个随机种子下仍给出逐比特完全相同的结果，尽管权重确实在变——原因是四个可用运动神经元中有一半没有任何感觉突触输入；作者基于求偶追逐中的视觉目标追踪假设重建了回路，结果该假设被数据推翻。最终学习开/关首次出现差异，但效果看起来只是学习规则把整个系统「压安静」了——漏球多于击中时惩罚占主导，导致运动响应萎缩，而不是产生任何技巧。

reddit · r/MachineLearning · /u/oPeraza2007 · 9月10日 02:28

**背景**: 连接组（connectome）是通过追踪电子显微镜图像得到的、神经系统全部神经元及其突触连接的地图；MaleCNS v1.0 是 Janelia 对完整雄性果蝇中枢神经系统的重建，涵盖中央脑、视叶和腹神经索。neuPrint 是用于从这类数据集中查询神经元及其连接关系的接口。本文特意选用乒乓球（Pong）作为毫不留情的测试平台，因为它每帧只给一个二值的击中/未击中信号，无法用「它会动所以是活的」这类模糊说法蒙混过关；类多巴胺可塑性指的是通过类似奖赏/惩罚的信号来调节突触强度的学习规则。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://male-cns.janelia.org/">Male CNS Connectome - MaleCNS connectome</a></li>
<li><a href="https://connectome-neuprint.github.io/neuprint-python/docs/changelog.html">Changelog — neuprint-python 0.5.1+10 ... - GitHub Pages</a></li>
<li><a href="https://www.nature.com/articles/s41586-022-05485-4">Dopamine promotes head direction plasticity during orienting movements | Nature</a></li>

</ul>
</details>

**标签**: `#connectomics`, `#computational neuroscience`, `#reinforcement learning`, `#plasticity`, `#negative results`

---