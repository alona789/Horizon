---
layout: default
title: "Horizon Summary: 2026-10-18 (ZH)"
date: 2026-10-18
lang: zh
---

> 从 34 条内容中筛选出 2 条重要资讯。

---

1. [DeepSeek 发布 v4.1-Flash-1017，编程基准测试超越前沿竞品](#item-1) ⭐️ 8.0/10
2. [传闻 iPhone 18 Pro 实现 untethered 越狱，或为 iOS 9 以来首个公开完整越狱](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek 发布 v4.1-Flash-1017，编程基准测试超越前沿竞品](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash-1017) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek-V4.1-Flash-1017，官方新闻页将其称为 DeepSeek-V4.1-Flash 的“小版本更新”，但在推理、编程和智能体任务上带来了“大幅”提升。该模型已在 DeepSeek API 上线，并同步登陆 OpenRouter，根据发布说明，它在 11 项编程基准中的 10 项上超过了 Sol 5.6。 这次发布为开发者提供了一个速度快、相对开放的闭源前沿模型替代方案；Hacker News 上异常热烈的讨论（675 分、575 条评论）表明，许多开发者评判这类模型时，比起榜单分数，更看重吞吐量、首 token 延迟（TTFT）以及能否查看思维链。它也进一步印证了一种观点：维系低价格和智能体工具可移植性的，是多元的模型生态，而非少数几家厂商。 V4.1-Flash 是基于 DeepSeek 因果编码器-解码器（CED）架构的稀疏混合专家模型，在 552B 参数主干上，输入端约激活 8B 参数、输出端约激活 16B 参数，原生支持多模态输入，上下文窗口最长可达一百万 token。“1017”后缀代表一个带日期的检查点，而非全新架构，因此这些亮眼的基准成绩应当与社区反馈一并看待——在混乱的真实代码审查任务上，提升仍不均衡。

hackernews · theykk · 10月17日 08:21 · [社区讨论](https://news.ycombinator.com/item?id=50129045)

**背景**: DeepSeek 是一家中国 AI 实验室，以发布开放权重模型、并与 OpenAI、Anthropic、Google 的闭源系统竞争而知名。其“Flash”系列采用混合专家（MoE）设计，即每个 token 只激活超大参数池中的一小部分，从而在保持大知识容量的同时让推理更便宜、更快速。智能体编程基准测试的是模型加上其智能体执行框架在多步骤软件任务上的表现；开发者最常提及的两个指标是每秒 token 数（tok/s）和首 token 延迟（TTFT），它们直接决定编程智能体的响应手感。OpenRouter 是一个模型路由服务，把包括 DeepSeek 在内的众多模型统一到一套兼容 OpenAI 的 API 之后，便于跨厂商比较。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4.1-flash">DeepSeek V 4 . 1 Flash - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash">deepseek -ai/ DeepSeek - V 4 . 1 - Flash · Hugging Face</a></li>
<li><a href="https://www.deepseek.com/en/news/deepseek-v4-1-flash/">Introducing DeepSeek - V 4 . 1 - Flash : smarter, faster, more efficient.</a></li>

</ul>
</details>

**社区讨论**: 整体情绪偏正面但并非一味吹捧：多位评论者认为，DeepSeek 之所以比 Sol 和 Gemini“感觉”更好，是因为服务商吞吐高、TTFT 低，且可以自由查看思维链而不被安全审查拦截；不过一位开发者让四个智能体对同一份改动超 200 个文件的 C++ 代码库做审查，非正式对比显示 GPT 6.1 Sol 约 4.5 分钟就找出三个相关问题，而 DeepSeek v4.1 Flash 用了 20 分钟才找到一个。也有人以此说明多元模型生态的重要性，还有人调侃“小版本更新、大幅提升”这一措辞。

**标签**: `#LLM release`, `#DeepSeek`, `#AI benchmarks`, `#coding agents`, `#open models`

---

<a id="item-2"></a>
## [传闻 iPhone 18 Pro 实现 untethered 越狱，或为 iOS 9 以来首个公开完整越狱](https://x.com/calif_io/status/2111080240978223545?s=20) ⭐️ 8.0/10

一个由研究者 @calif\_io 署名的 Telegram 频道帖文声称，已在 iPhone 18 Pro 上实现 untethered 越狱：设备重启后越狱状态依然保留，且无需借助电脑重新注入，如果属实，这将是自 iOS 9 以来首个公开演示的完整越狱。帖文称该攻击链横跨三层：cryptex 子系统、TSS 票签欺骗以及 PAC 绕过。 如果得到验证，这将是 iOS 安全研究领域的一个重要里程碑，说明 Apple 层层叠加的防御——cryptex 封装的系统组件、服务器端 TSS 签名、以及 A12 及之后芯片上的指针认证——仍可被组合攻破，且针对的是当代最新机型。这对长期萎缩的越狱社区而言也是一个重要时刻，同时对 Apple 的安全团队与漏洞赏金计划构成强烈信号。 该说法出现在 Apple 于 9 月 14 日发布、据称修复了 273 个漏洞的安全更新之后不久，帖文以此作为“仍存在未公开攻击链”的证据。但帖文本身只是一条简短的社交媒体转发，没有提供漏洞利用代码、CVE 编号、受影响的 iOS 具体版本号，也没有第三方复现，因此在出现技术细节或演示之前，应将其视为未经证实的说法。

telegram · zaihuapd · 10月17日 10:34

**背景**: 所谓“untethered（不完美绑定/完全脱离）”越狱，是指越狱状态在设备重启后依然保留、无需再连接电脑重新执行漏洞利用，这是实现难度最高的一类越狱。Apple 的现代防御手段包括 cryptex——一种经过签名封装的磁盘映像，自带文件系统，在启动过程中被挂载到随机路径（最初是为推送快速安全响应而引入）；以及 TSS（Ticket Signature Server，票签签名服务器），这是 Apple 的服务器端签名服务，负责签发安装或恢复固件所需的票据，正是它阻止用户降级到存在漏洞的旧版 iOS。PAC（Pointer Authentication Code，指针认证码）则是在指针的未使用位中写入密码学签名，并在使用前校验，因此篡改指针只会导致崩溃而无法执行代码；自 A12（iPhone XS）及之后的芯片起引入，大幅提高了控制流劫持的难度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://eclecticlight.co/2022/11/16/cryptex-how-a-custom-iphone-is-changing-macos-updates/">Cryptex : how a custom iPhone is changing macOS updates</a></li>
<li><a href="https://tin-z.github.io/ios-exploit-starterpack/en/pac/">PAC -- Pointer Authentication Code | iOS Exploit Starterpack</a></li>
<li><a href="https://idevicecentral.com/ios-signing-status/">iOS Signing Status Tool - iDevice Central</a></li>

</ul>
</details>

**标签**: `#iOS jailbreak`, `#security research`, `#Apple`, `#PAC bypass`, `#vulnerability exploitation`

---