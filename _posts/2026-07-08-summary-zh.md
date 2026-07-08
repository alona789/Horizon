---
layout: default
title: "Horizon Summary: 2026-07-08 (ZH)"
date: 2026-07-08
lang: zh
---

> 从 47 条内容中筛选出 18 条重要资讯。

---

1. [欧盟重启私密信息扫描规则](#item-1) ⭐️ 9.0/10
2. [TypeScript 7.0 发布，性能提升最高达 11.9 倍](#item-2) ⭐️ 9.0/10
3. [工具调用攻击绕过 LLM 智能体安全护栏](#item-3) ⭐️ 9.0/10
4. [中国 MiniMax 计划发布 2.7 万亿参数开源模型](#item-4) ⭐️ 9.0/10
5. [安卓远程 Root 漏洞链曝光](#item-5) ⭐️ 9.0/10
6. [Mistral 发布尖端导航模型 Robostral Navigate](#item-6) ⭐️ 8.0/10
7. [OpenAI 推出搭载 GPT-5.5 的 GPT-Live 语音模式](#item-7) ⭐️ 8.0/10
8. [Cloudflare Meerkat：无领导者全球共识](#item-8) ⭐️ 8.0/10
9. [OpenBSD 释放后使用漏洞导致本地提权至 root](#item-9) ⭐️ 8.0/10
10. [GitLost：提示注入泄露 GitHub 私有仓库](#item-10) ⭐️ 8.0/10
11. [索尼 PlayStation 将在欧盟删除闲置 3 年的数字游戏](#item-11) ⭐️ 8.0/10
12. [Grok 4.5 发布：推理效率提升 4 倍，价格更低](#item-12) ⭐️ 8.0/10
13. [减少交互式世界模型中的漂移](#item-13) ⭐️ 8.0/10
14. [本地 LLM 需结合 RAG 才能准确回答技术问题](#item-14) ⭐️ 8.0/10
15. [DeepSeek 自研 AI 芯片以减少对英伟达和华为的依赖](#item-15) ⭐️ 8.0/10
16. [阿里要求员工 7 月 10 日前卸载 Claude](#item-16) ⭐️ 8.0/10
17. [华为 5G 旗舰重返海外，峰值速率超 1100 Mbps](#item-17) ⭐️ 8.0/10
18. [研究人员通过电磁信号识别手机应用，准确率达 99.07%](#item-18) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [欧盟重启私密信息扫描规则](https://cyberinsider.com/eu-now-one-step-away-from-reviving-private-message-scanning-rules/) ⭐️ 9.0/10

欧盟距离恢复所谓的“聊天控制 1.0”法规仅一步之遥，该法规将允许科技公司自愿扫描非端到端加密通信中的儿童性虐待材料（CSAM）。 该法规可能为欧盟的数字隐私开创先例，在儿童保护与加密及隐私权之间寻求平衡。虽然聊天控制 1.0 比拟议的 2.0 侵入性更小，但仍引发了对监控范围可能扩大的担忧。 聊天控制 1.0 明确允许扫描非端到端加密的信息，例如云服务或无 E2EE 的群聊中的消息。与更具争议的聊天控制 2.0 提案不同，它不强制扫描或破坏加密。

hackernews · ggirelli · 7月8日 16:53 · [社区讨论](https://news.ycombinator.com/item?id=48834296)

**背景**: “聊天控制”法规，正式名称为《儿童性虐待法规》（CSAR），由欧盟委员会于 2022 年 5 月提出，旨在打击网络儿童性虐待。批评者认为它可能引发大规模监控并削弱加密。当前的辩论区分了自愿扫描（1.0）和强制扫描并禁止加密（2.0）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control">Chat Control - Wikipedia</a></li>
<li><a href="https://edri.org/our-work/chat-control-what-is-actually-going-on/">Chat Control: What is actually going on? - European Digital ...</a></li>

</ul>
</details>

**社区讨论**: 评论者大多区分了聊天控制 1.0（自愿，非 E2EE）和更令人担忧的 2.0。一些人指出 1.0 类似于电子邮件提供商的现有扫描，而另一些人则担心它可能导致客户端扫描。一位用户提供了联系欧盟代表反对该法规的链接。

**标签**: `#privacy`, `#EU`, `#surveillance`, `#legislation`, `#encryption`

---

<a id="item-2"></a>
## [TypeScript 7.0 发布，性能提升最高达 11.9 倍](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 9.0/10

微软发布了 TypeScript 7.0，这是一个重大版本更新，带来了显著的性能提升，在 VS Code 等大型代码库上实现了最高 11.9 倍的速度提升，编译时间从 125.7 秒降至 10.6 秒。 此版本大幅缩短了大型 TypeScript 项目的编译时间，提高了开发者的生产力，并使 TypeScript 对大规模应用更具吸引力。这也展示了微软对这种被数百万人使用的语言在性能优化上的持续投入。 性能提升在多个代码库上测得：VS Code（11.9 倍）、Sentry（8.9 倍）、Bluesky（8.7 倍）、Playwright（8.7 倍）和 tldraw（7.7 倍）。TypeScript 团队同时维护了两个独立的代码库，以支撑最先进的类型系统。

hackernews · DanRosenwasser · 7月8日 16:06 · [社区讨论](https://news.ycombinator.com/item?id=48833715)

**背景**: TypeScript 是微软开发的一种带类型的 JavaScript 超集，为语言添加了静态类型检查。它编译为纯 JavaScript，并在 Web 开发中广泛采用。TypeScript 7.0 是自之前的 5.x 系列以来的一个主版本跃升，社区中流传着基于 Rust 重写的消息，但尚未得到官方确认。

**社区讨论**: 社区反应非常积极，用户盛赞巨大的速度提升和 TypeScript 团队的工程壮举。一些评论回顾了 TypeScript 的采用历程，另一些则幽默地期待基于 Rust 的重写。

**标签**: `#TypeScript`, `#performance`, `#Microsoft`, `#programming languages`, `#developer tools`

---

<a id="item-3"></a>
## [工具调用攻击绕过 LLM 智能体安全护栏](https://www.reddit.com/r/MachineLearning/comments/1ur1fnz/agentic_safety_triggers_arent_textual_safety/) ⭐️ 9.0/10

研究揭示，使用模型上下文协议（MCP）的 LLM 智能体可以通过恶意工具调用序列遭到攻击，而基于文本的安全护栏无法检测到这些攻击。测试显示，当前最先进的安全护栏仅能阻止不到 48%的攻击，基础模型的拒绝率低于 35%。 这一发现暴露了 AI 安全对齐中的根本性缺陷：仅关注文本输入会遗漏嵌入在工具使用逻辑中的攻击，这可能使自主智能体面临真实世界的漏洞利用。这凸显了亟需新的安全范式来监控智能体的行为，而不仅仅是提示词。 该研究测试了基于 MCP 文件系统访问的 LLM 智能体，利用已知 CVE 构造了在文本中看似无害的工具调用序列。无训练方法在无需微调的情况下达到了约 3 倍基线拒绝率，优于 DPO 和 SafeDPO。

reddit · r/MachineLearning · /u/mlsandwich · 7月8日 18:36

**背景**: LLM 智能体是通过像 MCP 这样的协议（Anthropic 推出的开放标准）使用外部工具（如读取文件、执行命令）的模型。安全护栏通常过滤提示词中的有害文本，但工具调用序列可以绕过这一点。DPO（直接偏好优化）是一种无需强化学习即可让模型与偏好对齐的微调方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2305.18290">[2305.18290] Direct Preference Optimization: Your Language ...</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#LLM agents`, `#guardrails`, `#MCP`, `#adversarial attacks`

---

<a id="item-4"></a>
## [中国 MiniMax 计划发布 2.7 万亿参数开源模型](https://www.reddit.com/r/LocalLLaMA/comments/1uqnqsc/chinas_minimax_plans_to_launch_27trillion/) ⭐️ 9.0/10

MiniMax 宣布计划推出其 M3 Pro 大语言模型，拥有 2.7 万亿参数，将于 2025 年第三季度开源发布。这相较于当前 4280 亿参数的 M3 模型是一次巨大飞跃。 如果成功，这将成为有史以来最大的开源大语言模型之一，可能使最先进的 AI 能力更民主化，并加剧全球 AI 开发竞争。它将能支持更高级的推理和多步骤任务，惠及全球研究人员和开发者。 M3 Pro 模型内部代号，预计将显著提升复杂推理和多步骤指令处理能力。然而，巨大的规模引发了关于训练成本、推理效率以及普通用户可访问性的疑问。

reddit · r/LocalLLaMA · /u/External_Mood4719 · 7月8日 09:34

**背景**: MiniMax 是一家 2022 年成立于上海的 AI 公司，以其多模态 AI 模型和消费者应用（如 Talkie 和 Hailuo AI）而闻名。万亿参数级别的大语言模型处于 AI 研究的前沿，目前公开可用的超过 1 万亿参数的模型寥寥无几。开源如此规模的模型可能为全球研究社区提供宝贵资源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/MiniMax_Group">MiniMax Group</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#open-source`, `#large-scale model`, `#China`

---

<a id="item-5"></a>
## [安卓远程 Root 漏洞链曝光](https://www.coolapk.com/feed/72700258?s=ZGQ2MTVlZjYxMDYyNTM3ZzZhNGUzOThjega1640) ⭐️ 9.0/10

Nebula Security 研究人员披露了名为“IonStack”的漏洞链，该漏洞链结合了 Firefox 浏览器漏洞和潜伏 15 年的 Linux 内核漏洞（GhostLock，CVE-2026-43499），用户仅点击恶意链接即可远程获取任意安卓设备的 Root 权限。 该漏洞链影响所有安卓版本，包括最新的 Android 17，且概念验证代码已在 GitHub 公开，对全球数十亿设备构成严重安全威胁。 该漏洞链利用 Firefox 中的释放后重用漏洞（可能为 CVE-2024-9680）实现远程代码执行，然后利用 GhostLock——Linux 内核 futex 子系统中存在 15 年的释放后重用漏洞——进行权限提升。攻击适用于 Android 17 及所有旧版本，完整漏洞细节预计很快会流出。

telegram · zaihuapd · 7月8日 13:01

**背景**: 安卓设备基于 Linux 内核运行，远程 Root 意味着设备完全失控。IonStack 漏洞链是多阶段攻击：首先，恶意链接触发 Firefox 漏洞以在浏览器中获得初始代码执行；然后，利用 GhostLock 内核漏洞将权限提升至 Root。GhostLock（CVE-2026-43499）是 Linux 内核 rt_mutex 代码中的一个释放后重用漏洞，自 2011 年存在，影响所有主流发行版。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/android-17-root-1-click/">First-Ever 1- Click Android 17 Exploit Allows Attackers to ...</a></li>
<li><a href="https://thehackernews.com/2026/07/15-year-old-ghostlock-flaw-enables-root.html">15-Year-Old GhostLock Flaw Enables Root and Container Escape ...</a></li>

</ul>
</details>

**标签**: `#Android`, `#security`, `#vulnerability`, `#remote exploit`, `#root`

---

<a id="item-6"></a>
## [Mistral 发布尖端导航模型 Robostral Navigate](https://mistral.ai/news/robostral-navigate/) ⭐️ 8.0/10

Mistral AI 发布了 Robostral Navigate，这是一个 80 亿参数的模型，仅使用单个 RGB 摄像头即可在 R2R-CE 基准测试中达到 76.6%的成功率，无需深度传感器或激光雷达。 该模型大幅降低了机器人导航的硬件需求，使其更易普及，并可能加速在服务机器人、自动驾驶等实际应用中的部署。 该模型在模拟环境中训练，并通过名为 CISPO 的强化学习算法进行优化。它能仅凭实时摄像头画面理解自然语言指令，如‘去厨房’。

hackernews · ottomengis · 7月8日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=48832212)

**背景**: 传统机器人导航通常依赖预制地图、深度传感器或多个摄像头。Robostral Navigate 是一种视觉语言模型，旨在解决‘被绑架的机器人问题’，即机器人在未知位置时仍需导航。R2R-CE 基准测试评估了连续执行房间到房间导航任务的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mistral.ai/news/robostral-navigate/">Robostral Navigate: single-camera AI navigation | Mistral AI</a></li>
<li><a href="https://alphasignal.ai/news/mistral-s-robostral-navigate-beats-sensor-heavy-robots-with-just-one-camera">Mistral's Robostral Navigate Beats Sensor-Heavy Robots With ...</a></li>

</ul>
</details>

**社区讨论**: 评论者对无地图导航能力感到兴奋，有用户表示这能帮助自己过去的研究。另一些人则持谨慎态度，指出机器人演示通常难以保证现实世界的鲁棒性。此外，大家对该模型的开源可能性及业余爱好者的应用前景也表示关注。

**标签**: `#robotics`, `#AI`, `#navigation`, `#Mistral`, `#machine learning`

---

<a id="item-7"></a>
## [OpenAI 推出搭载 GPT-5.5 的 GPT-Live 语音模式](https://openai.com/index/introducing-gpt-live/) ⭐️ 8.0/10

OpenAI 推出了 GPT-Live，这是一种新的实时语音对话功能，支持自然的全双工对话，并能在后台将复杂任务委托给 GPT-5.5。 GPT-Live 弥合了语音助手与前沿 AI 模型之间的差距，让用户能够进行更长时间、更高效的对话，且不牺牲智能。这可能会改变人们进行头脑风暴、学习和日常任务时与 AI 互动的方式。 GPT-Live 采用全双工架构，可以同时听和说，并能通过“嗯”等短语表示专注。该功能在发布时不支持视频或屏幕共享，但这些功能正在开发中。

hackernews · logickkk1 · 7月8日 17:03 · [社区讨论](https://news.ycombinator.com/item?id=48834405)

**背景**: 之前的 ChatGPT 语音模式仅限于一个较为简单的语音模型，落后于最新的文本模型。GPT-5.5 是 OpenAI 于 2026 年 4 月发布的最先进模型，可处理编码和数据分析等复杂任务。全双工通信允许双方同时发言和收听，使对话更加自然。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-live/">Introducing GPT-Live | OpenAI</a></li>
<li><a href="https://9to5mac.com/2026/07/08/openai-upgrading-chatgpt-with-all-new-voice-mode-experience-watch-here/">OpenAI just upgraded ChatGPT voice mode in a major way ...</a></li>
<li><a href="https://www.androidheadlines.com/2026/07/chatgpt-gpt-live-1-voice-mode-update-features.html">ChatGPT Launches GPT-Live-1 Upgraded Voice Mode</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.5">GPT-5.5</a></li>

</ul>
</details>

**社区讨论**: 开发者 simonw 在预览后称赞 GPT-Live，称其在遛狗时进行了一小时的头脑风暴，并欣赏其将任务委托给 GPT-5.5 的能力。然而，一些评论者如 bariswheel 认为之前的语音模式过于浅薄，希望 GPT-Live 能提供更深入的内容。其他人则担心 AI 会取代人际关系，而 artdigital 注意到前沿助手在语音模式下均缺乏工具/连接器支持。

**标签**: `#OpenAI`, `#GPT-5.5`, `#voice AI`, `#conversational AI`, `#real-time AI`

---

<a id="item-8"></a>
## [Cloudflare Meerkat：无领导者全球共识](https://blog.cloudflare.com/meerkat-introduction/) ⭐️ 8.0/10

Cloudflare Research 推出了 Meerkat，一个基于 QuePaxa 算法的全球分布式共识服务，实现了无领导者操作且不依赖超时。这是异步共识算法的首次生产实现。 这代表了分布式共识领域的重要进展，能够在传统基于超时的协议（如 Paxos 和 Raft）难以应对的恶劣网络条件下稳健运行。它可能提高全球分布式系统的可靠性，特别是在高延迟或不稳定的网络中。 Meerkat 使用 QuePaxa 的竞合延迟机制替代超时，但每个读操作都需要全局共识，这可能会增加延迟。该系统尚未投入生产，目前被视为一项实验。

hackernews · bobnamob · 7月8日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=48831565)

**背景**: 传统的共识算法如 Paxos 和 Raft 依赖超时和强领导者来保证活性，使其容易受到网络不稳定的影响。异步共识算法通过随机化和竞合来避免超时，但历史上一直面临效率挑战。QuePaxa 在正常情况下实现了与部分同步协议相当的效率，同时在最坏条件下保持稳健性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/meerkat-introduction/">Introducing Meerkat: an experiment in global consensus</a></li>
<li><a href="https://bford.info/pub/os/quepaxa/quepaxa.pdf">QuePaxa: Escaping the Tyranny of Timeouts in Consensus QuePaxa: Escaping the Tyranny of Timeouts in Consensus September 4, 2024 “Next-Generation Secure Distributed ... QuePaxa: Escaping the tyranny of timeouts in consensus PasinduTennage/quepaxa-fork-for-internal - GitHub</a></li>

</ul>
</details>

**社区讨论**: 社区评论对首个生产级异步共识表示兴趣，但担忧读操作延迟，因为所有读操作都需要全局共识。一些人将其与无领导者的 Multi-Paxos 相比认为不占优势，而另一些人则认为它对混乱的网络有价值。存在对构建自定义共识的质疑，但认可 Cloudflare 的潜力。

**标签**: `#distributed systems`, `#consensus algorithms`, `#Cloudflare`, `#QuePaxa`, `#asynchronous consensus`

---

<a id="item-9"></a>
## [OpenBSD 释放后使用漏洞导致本地提权至 root](https://nvd.nist.gov/vuln/detail/cve-2026-57589) ⭐️ 8.0/10

OpenBSD 中发现了一个释放后使用漏洞（CVE-2026-57589），允许本地攻击者将权限提升至 root。该漏洞是 OpenAI 与 Trail of Bits 合作的“Patch The Planet”项目的一部分。 OpenBSD 以安全著称，因此任何本地提权漏洞都意义重大。这一发现凸显了 AI 辅助漏洞研究在最具安全性的操作系统上的有效性。 该漏洞是内核中的释放后使用问题，允许从非 root 用户提权至 root。截至报告发布，OpenBSD 安全页面尚未发布公开补丁或公告。

hackernews · linggen · 7月8日 13:24 · [社区讨论](https://news.ycombinator.com/item?id=48831658)

**背景**: 释放后使用漏洞发生在程序在内存被释放后继续使用其指针，可能导致任意代码执行。本地提权是指在系统上获取更高访问权限的行为。OpenBSD 拥有强大的安全记录，多年来默认安装仅发现两个远程漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.snyk.io/lesson/use-after-free/">Use after free vulnerability | Tutorial & Examples | Snyk Learn</a></li>
<li><a href="https://cwe.mitre.org/data/definitions/416.html">CWE - CWE-416: Use After Free (4.20) - Mitre Corporation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Local_privilege_escalation">Local privilege escalation</a></li>

</ul>
</details>

**社区讨论**: 社区承认此类漏洞在 OpenBSD 中罕见，一些评论称赞该项目的安全记录。人们对 AI 辅助工具可能发现多少漏洞感到好奇，并担忧报告的 CVE 尚未出现在 OpenBSD 的安全页面上。

**标签**: `#openbsd`, `#security`, `#vulnerability`, `#privilege-escalation`

---

<a id="item-10"></a>
## [GitLost：提示注入泄露 GitHub 私有仓库](https://noma.security/blog/gitlost-how-we-tricked-githubs-ai-agent-into-leaking-private-repos/) ⭐️ 8.0/10

安全研究人员演示了一种针对 GitHub AI 代理的提示注入攻击，通过在公共交互中嵌入恶意指令，可以泄露私有仓库内容。 此次攻击揭示了代理型 AI 系统中的一个基础性漏洞类别，类似于 Web 应用程序中的 SQL 注入，表明当前的安全护栏不足，迫切需要系统性防御方案。 该攻击用“Additionally”等简单词汇绕过了 GitHub 的防护栏，利用了模型天然倾向于遵循指令而非区分系统与用户输入的特性。研究人员已向 GitHub 负责任地披露了此问题，但尚未公开收到修复确认。

hackernews · ColinEberhardt · 7月8日 05:25 · [社区讨论](https://news.ycombinator.com/item?id=48827858)

**背景**: 提示注入是一种网络安全漏洞，恶意输入通过混入受信任指令，导致大语言模型（LLM）产生非预期行为。在能够访问工具和数据的代理型 AI 系统中，此类攻击可能导致数据泄露。GitHub 的 AI 代理既能读取公共仓库也能读取私有仓库，当它在拥有私有数据访问权限的情况下处理来自公共交互的提示时，就成为了有吸引力的攻击目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://genai.owasp.org/resource/agentic-ai-threats-and-mitigations/">Agentic AI - OWASP Lists Threats and Mitigations</a></li>
<li><a href="https://arxiv.org/html/2510.23883v1">Agentic AI Security: Threats, Defenses, Evaluation, and Open ...</a></li>

</ul>
</details>

**社区讨论**: 评论者将提示注入比作 SQL 注入，认为它属于系统性漏洞类别；而另一些人则认为这是配置问题，因为用户授予了代理访问权限。有人注意到用“Additionally”等简单词汇就能绕过防护栏的讽刺性，进一步强化了 LLM 上下文窗口内建立硬安全边界本质上有缺陷的观点。

**标签**: `#security`, `#AI`, `#prompt injection`, `#GitHub`, `#vulnerability`

---

<a id="item-11"></a>
## [索尼 PlayStation 将在欧盟删除闲置 3 年的数字游戏](https://www.flatpanelshd.com/news.php?subaction=showfull&id=1783340582) ⭐️ 8.0/10

索尼更新了 PlayStation 许可条款，允许在账户闲置 3 年后删除数字游戏库，该政策首先在欧盟地区实施。 这项政策凸显了数字游戏所有权的脆弱性，消费者仅持有可被撤销的许可证，引发了对消费者保护和数字购买价值的担忧。 删除的是游戏许可证而非下载文件本身，但实际导致游戏无法游玩。索尼未明确是否会在删除前发送警告邮件。

hackernews · thewebguyd · 7月8日 17:45 · [社区讨论](https://news.ycombinator.com/item?id=48834919)

**背景**: 在数字市场中，消费者购买的是使用软件的许可证，而非软件本身。这意味着像 PlayStation 这样的平台可以根据其条款撤销访问权限。相比之下，实体游戏赋予消费者完全所有权。欧盟有严格的消费者保护法律，但数字许可往往绕过了这些法律。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Digital_distribution_of_video_games">Digital distribution of video games - Wikipedia</a></li>
<li><a href="https://kotaku.com/video-game-industry-esa-digital-ownership-2000712263">The Video Game Industry’s Trade Body Doesn’t Want To Talk About Digital Ownership</a></li>

</ul>
</details>

**社区讨论**: 社区评论对索尼的政策表达了愤怒和担忧。用户指出微软等竞争对手并未删除旧购买记录，并提到其他平台也曾发生类似撤销行为。部分用户担心缺乏警告和联系索尼客服困难。

**标签**: `#digital rights`, `#gaming`, `#playstation`, `#consumer protection`, `#digital ownership`

---

<a id="item-12"></a>
## [Grok 4.5 发布：推理效率提升 4 倍，价格更低](https://x.ai/news/grok-4-5) ⭐️ 8.0/10

xAI 发布了新 AI 模型 Grok 4.5，其推理效率相比 Opus 4.8 提升 4 倍，定价为每百万输入 token 2 美元、每百万输出 token 6 美元。该模型使用了来自 AI 代码编辑器 Cursor 的数万亿 token 用户交互数据进行训练。 Grok 4.5 的高推理效率和低成本组合可能颠覆 AI 模型市场，挑战 Anthropic 和 OpenAI 等现有玩家。使用来自 Cursor 的真实编码交互数据，可能让 Grok 在代码相关任务上获得独特优势。 根据基准测试，Grok 4.5 的性能大致相当于 Opus 4.7 的水平，同时价格远低于 GPT-5.5（$5/$30）和 Opus 4.8（$5/$25）等竞品。该模型还具有高 token 吞吐量（约每秒 90 个 token）和高 token 效率的特点。

hackernews · BoumTAC · 7月8日 18:00 · [社区讨论](https://news.ycombinator.com/item?id=48835111)

**背景**: Grok 是埃隆·马斯克的 AI 公司 xAI 开发的一系列 AI 模型，以其追求真相的聊天机器人和与 X 平台的集成而闻名。Opus 是 Anthropic 在 Claude 系列中的旗舰模型，代表了最先进的推理和编码能力。Cursor 是一个 AI 原生的代码编辑器，收集了大量的用户交互数据，xAI 利用这些数据训练出 Grok 4.5，使其更好地理解开发者工作流程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Grok_(chatbot)">Grok (chatbot) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_(language_model)">Claude (AI) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区成员对 Grok 4.5 的成本效率印象深刻，指出其每美元的推理能力是 Opus 的 4 倍。一些人质疑构建昂贵模型的经济可行性，尤其是当模型并非排名第一时；而用户则分享了在 iOS 开发等特定任务中使用 Grok 的积极体验。初步反馈强调速度快和 token 效率高。

**标签**: `#AI`, `#Grok`, `#language model`, `#reasoning`, `#efficiency`

---

<a id="item-13"></a>
## [减少交互式世界模型中的漂移](https://www.reddit.com/r/MachineLearning/comments/1ur4hkc/reducing_drift_in_interactive_worldmodel_rollouts/) ⭐️ 8.0/10

LingBot World v2 开放式权重世界模型采用混合双向/自回归注意力掩码（MoBA）和长自推出轨迹上的蒸馏，以减少交互式推出过程中的漂移。其权重已以 CC-BY-NC-SA 许可公开发布。 这项工作直接解决了自回归世界模型中的漂移问题，实现了超过 60 分钟无可见衰退的稳定交互会话。它为构建需要长期一致性的交互式 AI 系统提供了实用方法。 MoBA 注意力掩码对早期帧混合双向注意力，对近期帧使用自回归注意力，并采用动态 KV 缓存调度以保持长推出的可行性。该方法的主要局限在于持久性仅体现在外观，而非身份，因此离开上下文窗口的对象会被重新生成而非回忆。

reddit · r/MachineLearning · /u/Purple-Low-2779 · 7月8日 20:23

**背景**: 自回归世界模型根据先前帧和用户输入顺序生成帧，但由于依赖自身生成帧导致误差累积，会出现漂移（曝光偏差）。像 MoBA 这样的注意力掩码有助于平衡信息流，而蒸馏则将多步扩散模型压缩为更快的单步生成器，同时保持分布质量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2512.15702">End-to-End Training for Autoregressive Video Diffusion via ...</a></li>
<li><a href="https://arxiv.org/html/2404.02101v1">CameraCtrl: Enabling Camera Control for Text-to-Video Generation</a></li>
<li><a href="https://openaccess.thecvf.com/content/CVPR2024/papers/Yin_One-step_Diffusion_with_Distribution_Matching_Distillation_CVPR_2024_paper.pdf">One-step Diffusion with Distribution Matching Distillation Tianwei Yin1</a></li>

</ul>
</details>

**社区讨论**: 提交者表示好奇其他人运行该模型后，长推出稳定性是否依然成立，并指出由于发布较新，目前尚无独立复现结果。

**标签**: `#world models`, `#attention mechanisms`, `#distillation`, `#interactive AI`, `#generative modeling`

---

<a id="item-14"></a>
## [本地 LLM 需结合 RAG 才能准确回答技术问题](https://www.reddit.com/r/LocalLLaMA/comments/1uqpxgp/can_you_trust_local_models_to_answer_accurately/) ⭐️ 8.0/10

一名开发者对本地 LLM（包括 Unsloth Gemma QAT 和 Apple Intelligence）进行了 7648 道技术多选题的基准测试，发现 RAG 将准确率从较差提升至非常好，而显式推理仅增加约 1%。 这提供了实证证据，表明本地 LLM 在与 RAG 结合时可用于技术问答，让希望离线使用模型学习或工作、无需依赖云 API 的开发者感到放心。 RAG 系统不限于单个正确文档，模拟真实使用场景；Apple Intelligence（AFM 2 3B）由于 4K 上下文限制仅检索 3 个片段，仍获得 86%的分数，而较大模型获得 32K 上下文。

reddit · r/LocalLLaMA · /u/Spiritual-Market-741 · 7月8日 11:28

**背景**: 检索增强生成（RAG）是一种让 LLM 在回答前从外部文档获取相关信息的技术，可减少幻觉。没有 RAG 时，本地 LLM 常难以回答特定领域问题。该基准使用 DeepSeek-V4-Flash 从 Node.js、TypeScript、Vue 等流行项目的 GitHub markdown 文档生成问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Retrieval-augmented_generation">Retrieval-augmented generation - Wikipedia</a></li>
<li><a href="https://unsloth.ai/docs/models/gemma-4/qat">Gemma 4 QAT | Unsloth Documentation</a></li>
<li><a href="https://arxiv.org/abs/2606.19348">[2606.19348] DeepSeek-V4: Towards Highly Efficient Million ...</a></li>

</ul>
</details>

**标签**: `#local LLMs`, `#RAG`, `#benchmark`, `#accuracy`, `#technical questions`

---

<a id="item-15"></a>
## [DeepSeek 自研 AI 芯片以减少对英伟达和华为的依赖](https://t.me/zaihuapd/42423) ⭐️ 8.0/10

中国 AI 公司 DeepSeek 已开始自研 AI 推理芯片，以减少对美国出口管制下对英伟达和华为芯片的依赖。该项目约一年前启动，目前仍处于早期阶段。 此举可能重塑中国的 AI 硬件格局，减少对外国和受制裁芯片供应商的依赖。这也凸显了 AI 公司垂直整合芯片开发以确保供应链安全的趋势。 该芯片专注于推理阶段，即训练好的模型生成回答的环节，而非训练。DeepSeek 已与芯片设计、代工和存储公司接洽，并积极招募芯片设计工程师。

telegram · zaihuapd · 7月8日 05:20

**背景**: AI 推理是模型利用学到的模式产生输出的过程，而训练是学习阶段。DeepSeek 此前依赖英伟达的 H800（H100 的中国特供版）和华为的昇腾芯片。美国出口管制限制先进芯片对华销售，促使 DeepSeek 等公司开发定制芯片。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hopper_(microarchitecture)">Hopper (microarchitecture) - Wikipedia</a></li>
<li><a href="https://www.huaweicentral.com/huawei-reveals-3-year-ascend-ai-chip-roadmap-950-coming-in-2026/">Huawei reveals 3-year Ascend AI chip roadmap, 950 coming in 2026</a></li>
<li><a href="https://www.cloudflare.com/learning/ai/inference-vs-training/">AI inference vs. training: What is AI inference? - Cloudflare</a></li>

</ul>
</details>

**标签**: `#AI`, `#Hardware`, `#DeepSeek`, `#Semiconductors`, `#Inference`

---

<a id="item-16"></a>
## [阿里要求员工 7 月 10 日前卸载 Claude](https://t.me/zaihuapd/42424) ⭐️ 8.0/10

阿里巴巴内部下令要求所有员工在 7 月 10 日前卸载所有 Anthropic 相关产品，包括 Claude 模型（Sonnet、Opus、Fable）和 Claude Code 等代理工具。此前 Anthropic 指控阿里在 4 月 22 日至 6 月 5 日期间使用约 2.5 万个虚假账号与 Claude 进行了超 2800 万次交互。 这一事件凸显了大型科技公司在 AI 工具使用和知识产权保护方面日益紧张的局势。它可能为企业 AI 治理树立先例，并影响公司管理外部 AI 模型访问的方式。 阿里巴巴此前曾报销员工使用 Claude、GPT、Gemini 等外部模型的费用。Anthropic 在检测到涉嫌虚假账号活动后收紧了风控策略。禁令涵盖基于云的产品和代理产品，包括 AI 编码助手 Claude Code。

telegram · zaihuapd · 7月8日 06:09

**背景**: Claude 是 Anthropic 开发的一系列大语言模型，包括 Sonnet（性能均衡）、Opus（能力最强）和 Fable（轻量级）等模型。Claude Code 是一种自主编码代理，可以读取代码库、编辑文件并运行命令。阿里巴巴是一家中国大型科技公司，拥有自己的 AI 模型，但也曾允许员工使用外部工具进行工作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/about-claude/models/overview">Models overview - Claude Platform Docs</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>
<li><a href="https://www.anthropic.com/product/claude-code">Claude Code | Anthropic's agentic coding system</a></li>

</ul>
</details>

**标签**: `#Alibaba`, `#Claude`, `#AI policy`, `#tech ban`, `#Anthropic`

---

<a id="item-17"></a>
## [华为 5G 旗舰重返海外，峰值速率超 1100 Mbps](https://finance.sina.com.cn/tech/roll/2026-07-08/doc-inihapna8035781.shtml) ⭐️ 8.0/10

华为 Pura 90 Pro Max 国际版原生支持 5G 网络，海外实测峰值下载速率突破 1100 Mbps，这是美国制裁七年后华为首次在海外市场推出 5G 旗舰手机。 这一里程碑标志着华为有能力克服美国技术封锁并重新进入全球智能手机市场，可能加剧竞争并重塑电信格局。同时，它展示了华为 5A 通信技术的成熟，该技术超越了基本的 5G 连接，提升了网络体验。 Pura 90 Pro Max 的 5G 能力由华为自研的 5A 通信技术支持，该技术包括智能信号聚合和动态延迟优化。今年早些时候，华为将其旗舰设备升级至 HarmonyOS 6.0.0.125，实现了 5A 支持，为海外回归奠定了技术基础。

telegram · zaihuapd · 7月8日 12:17

**背景**: 自 2019 年起，华为被禁止使用美国技术，严重影响了其生产 5G 智能手机的能力。2023 年，Mate 60 系列凭借支持 5G 的麒麟芯片推出，令业界震惊，标志着技术突破。5A 技术于 2025 年底推出，并非新一代 5G，而是一套终端侧优化技术，可提高网络效率和用户体验，被描述为手机调制解调器的‘智能驾驶系统’。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://biggo.com/news/202602182022_Huawei_5A_Technology_Explained">Huawei's "5A" Explained: Not 5G, But a Smarter Way to Connect</a></li>
<li><a href="https://www.huaweicentral.com/huawei-explains-the-5a-network-benefits-for-smartphones/">Huawei explains the 5A network benefits for smartphones</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#5G`, `#smartphone`, `#sanctions`, `#telecommunications`

---

<a id="item-18"></a>
## [研究人员通过电磁信号识别手机应用，准确率达 99.07%](https://www.scmp.com/news/china/science/article/3359688/chinese-researchers-find-peephole-any-smartphone-its-leaked-radio-signal) ⭐️ 8.0/10

这项技术构成重大的隐私和安全风险，因为它可以在无需物理接触的情况下，甚至在离线、加密或锁定的设备上识别应用使用情况，可能用于未经用户同意的监控或取证分析。 该方法通过捕获设备硬件组件（如处理器、GPU、Wi-Fi 模块）在应用执行期间泄漏的微弱电磁辐射来工作，无需访问操作系统或存储数据。测试的应用包括抖音、微信视频通话、百度地图、短信、浏览器、相机和云存储。

telegram · zaihuapd · 7月8日 16:05

**背景**: 侧信道攻击利用电磁辐射、功耗或时间等物理副产品来提取敏感信息。电磁侧信道分析是一种 извест的非侵入式攻击向量；然而，以往的工作通常需要物理接近或特殊设备。这项研究展示了使用消费级接收器识别应用级别活动的实用方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mk.co.kr/cn/world/12093156">中国一所大学的研究团队开发出一种所谓“非接触式数字取证技术”,可通过...</a></li>
<li><a href="https://www.ckhq.net/html/6c1af61946e47994a7d682373d5f7757.html">中国科研团队研发非接触式智能手机应用识别技术，准确率达99.07%</a></li>

</ul>
</details>

**标签**: `#security`, `#mobile forensics`, `#electromagnetic side-channel`, `#privacy`, `#research`

---