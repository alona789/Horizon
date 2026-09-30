---
layout: default
title: "Horizon Summary: 2026-09-30 (ZH)"
date: 2026-09-30
lang: zh
---

> 从 41 条内容中筛选出 4 条重要资讯。

---

1. [OpenAI 发布 GPT-6.1 Sol：以五分之一价格实现接近 Astra 的智能](#item-1) ⭐️ 8.0/10
2. [PS5 Relapse 漏洞利用可越狱 7.00–13.60 固件](#item-2) ⭐️ 8.0/10
3. [网页与移动端对话式 AI 智能体的隐私分析](#item-3) ⭐️ 8.0/10
4. [Anthropic：智谱 GLM-5.3 可自主实施网络攻击](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-6.1 Sol：以五分之一价格实现接近 Astra 的智能](https://openai.com/index/introducing-gpt-6-1-sol/) ⭐️ 8.0/10

OpenAI 发布了 GPT-6.1 Sol，这是 GPT-6 Sol 的一次小版本升级；官方称其在智能体编程、计算机操作和专业任务上接近 GPT-6 Astra 的水平，而价格仅为 Astra 标准价的五分之一。它的输入/输出价格与 GPT-6 Sol 持平，为每百万 token 2 美元/10 美元，但缓存输入折扣从 90% 提高到 95%，即缓存输入每百万 token 仅 0.10 美元；开发者可通过 API 以 gpt-6.1-sol 名称调用，同时也通过 ChatGPT 付费档位和 Amazon Bedrock 提供。 这次发布表明，前沿实验室之间的主要竞争战场已经从原始能力转向性价比，这不仅给 Anthropic 等竞争对手带来压力，也冲击着 OpenAI 自家更便宜的替代方案。对于以缓存上下文为主要 token 开销的智能体和编程类工作负载而言，缓存价格减半会直接转化为更低的运营成本。 据 Artificial Analysis 的评测，GPT-6.1 Sol 在其智能指数上仅比 GPT-6 Astra 低 1 分，而每任务成本不到 Astra 的四分之一；OpenAI 还表示该模型比 GPT-6 Sol 事实错误更少，在智能体任务中更能可靠地遵守显式限制和用户意图。该模型距离 GPT-6 Sol 发布仅约一周，部分报道指出它尚未覆盖所有 ChatGPT 入口，API 仍是开发者的主要接入途径。

hackernews · crorella · 9月29日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=49896586)

**背景**: OpenAI 的 GPT-6 系列采用分层设计：Astra 是旗舰级前沿模型，而 Sol 是更廉价、能力更弱的版本；这一命名延续了此前 GPT-5.6 系列中 Luna、Terra、Sol 的变体划分。GPT-6 Astra 被定位为在编程、数学以及操作电脑和浏览器方面达到最先进水平，但其价格对高频智能体使用而言过于昂贵。GPT-6.1 Sol 这样的小版本更新，正是 OpenAI 在拉近与旗舰差距的同时把成本压低到日常开发可承受范围的手段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-1-sol/">Introducing GPT - 6 . 1 Sol | OpenAI</a></li>
<li><a href="https://artificialanalysis.ai/articles/gpt-6-1-sol-replaces-gpt-6-sol-after-just-7-days-with-near-astra-intelligence">GPT-6.1 Sol replaces GPT-6 Sol after just 7 days, with near-Astra ...</a></li>
<li><a href="https://openrouter.ai/openai/gpt-6.1-sol">GPT - 6 . 1 Sol - API Pricing &amp; Providers | OpenRouter</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论总体偏怀疑：不少人表示 GPT-6 Sol 相较 Sol 5.6 是明显退步，自己已转而独家使用 Anthropic 的 Opus 5.5，并怀疑时隔一周的小版本更新不会带来多大改变。一条高赞评论认为真正的重点其实是缓存输入 95% 的折扣，因为更便宜的缓存能让编程智能体跑得更多；也有人质疑在 DeepSeek 便宜得多、智能差距感知不明显的情况下，每月 200 美元的档位是否合理；还有评论者把竞争转向 token 价格视为对行业和投资者的不祥信号。

**标签**: `#OpenAI`, `#GPT-6.1`, `#LLM`, `#AI pricing`, `#model release`

---

<a id="item-2"></a>
## [PS5 Relapse 漏洞利用可越狱 7.00–13.60 固件](https://github.com/ntfargo/Relapse-Exploit) ⭐️ 8.0/10

一个名为 &quot;Relapse&quot; 的公开漏洞利用链已针对运行 7.00 至 13.60 固件的 PlayStation 5 主机发布，它将一个 WebKit JavaScriptCore 浏览器漏洞与内核漏洞串联，从而进入越狱环境。该仓库由 ntfargo 发布，浏览器阶段利用 JSC 信息泄露和结构化克隆对象池不匹配来破坏一个 typedarray，随后通过地址泄露和 aio\_multi\_wait 释放后使用竞争建立内核读写能力，并加载 ELF 载荷。 这是一次影响广泛固件范围的越狱，意味着许多仍在货架上的零售 PS5 和 PS5 Pro 主机都可能存在漏洞，从而为用户打开运行自制应用、游戏备份以及索尼官方不允许的其他功能的大门。它恰逢数字游戏所有权争论升温之际，为用户提供了一条绕过限制（例如无法将存档备份到 USB）的实用途径——尽管这是非官方且可能违法的。 该漏洞利用支持 7.00 至 13.60 固件，但据称在 9 月 16 日更新的主机不兼容，因此并非所有 PS5 用户都能使用。它提供了一个 ELF 加载器，越狱成功后用户可以运行自制载荷；社区成员推测索尼可能会通过禁用 WebKit 中的 JIT 来缩小攻击面作为回应。

hackernews · therepanic · 9月29日 15:44 · [社区讨论](https://news.ycombinator.com/item?id=49895304)

**背景**: WebKit 是 Safari 及许多嵌入式浏览器视图所使用的浏览器引擎，而 JavaScriptCore（JSC）是它的 JavaScript 引擎，攻击者可通过内存破坏漏洞在浏览器沙箱内实现代码执行。越狱通常串联两个或更多漏洞：一个用户态或浏览器阶段的漏洞用于逃逸沙箱，一个内核阶段的漏洞用于取得操作系统的完整控制权。PS5 运行的是索尼严格控制、高度锁定的系统，禁止未获批准的软件；与早期 PlayStation 主机不同，它还限制将游戏存档备份到外部介质。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ntfargo/Relapse-Exploit">GitHub - ntfargo/ Relapse - Exploit : Exploit chain for PS 5 7.00 - 13.60</a></li>
<li><a href="https://www.superpsx.com/ps5-relapse-jailbreak-13-60-and-lower-complete-guide/">PS 5 Relapse Jailbreak 13.60 and Lower – Complete Guide</a></li>
<li><a href="https://decrypt.co/379583/sony-ps5-jailbreak-digital-games-ownership">Someone Finally Jailbroke the PS5—Just After Sony Said Players Don’t Own Their Games - Decrypt</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者聚焦于实际用途，有人询问这是否终于能把游戏存档备份到 USB，并提到因数据损坏丢失了一年的《我的世界》进度，凸显了对仅限 PS Plus 云备份的沮丧。其他人推测资深主机破解团体很可能掌握用于引导程序层逃逸的更多零日漏洞，还有人认为索尼可能会禁用 JSC 的 JIT 以缩小攻击面；有人希望该漏洞推迟到《GTA 6》发布后再公开，也有人期待它能让 PS5 运行 Steam 上的 PC 游戏。

**标签**: `#PS5`, `#exploit`, `#security`, `#WebKit`, `#jailbreak`

---

<a id="item-3"></a>
## [网页与移动端对话式 AI 智能体的隐私分析](https://jorgegarciaherrero.com/wp-content/interactivos/20260916-Prompt-like-a-butterfly-sting-like-a-tracker-%28clean%29.pdf) ⭐️ 8.0/10

一篇题为《A Privacy Analysis of Web and Mobile Conversational AI Agents》的新研究论文（发布于 jorgegarciaherrero.com）系统性地考察了网页端与移动端对话式 AI 智能体的隐私风险，重点关注提示词泄露、提交前的数据外泄以及薄弱的基于 URL 的访问控制。该论文在 Hacker News 上以“Prompt like a butterfly, sting like a tracker”为题被讨论，获得 408 分和 130 条评论。 研究结果表明，用户与主流 AI 聊天助手的日常交互——无论是输入草稿、粘贴文档，还是分享会话链接——都可能在你按下发送键之前就把敏感内容泄露给分析或追踪基础设施。随着 LLM 助手被嵌入浏览器、手机和企业工作流，这给终端用户以及正在评估商业 AI 产品与本地开源模型隐私状况的团队都提出了直接的问题。 评论者指出了具体的技术路径：据报道，ChatGPT 网页端会在用户提交前把未完成的提示词发送到 \`conversation/prepare\` 端点，这可能是为了预热缓存，但同时也暴露了用户的写作节奏和尚未成形的想法；而 Perplexity 会把完整对话暴露给任何持有会话 URL 的人，因为它把 URL 中的 UUID 当成了隐私保障。这些都是典型的访问控制失效和不安全直接对象引用（IDOR）模式，论文还比较了风险究竟有多少来自智能体本身、多少来自周边的平台 API 与权限设置。

hackernews · damaru2 · 9月29日 09:03 · [社区讨论](https://news.ycombinator.com/item?id=49890226)

**背景**: 对话式 AI 智能体是指基于聊天的助手（如 ChatGPT、Perplexity 或 Gemini），它们与用户维持会话，通常运行在浏览器或移动应用中并拥有平台权限。“提示词泄露”是已被认可的一类 LLM 安全问题——OWASP 将系统提示词泄露列为 LLM07:2025——指隐藏指令或用户输入被意外暴露；而“提交前外泄”则呼应了更早的网页研究，例如 USENIX 的“Leaky Forms”研究，发现邮箱和密码字段在表单提交之前就被追踪器采集。基于 URL 的访问控制失效（包括 IDOR）指的是资源仅靠一个看似不可猜测的标识符来保护，而非真正的授权校验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://genai.owasp.org/llmrisk/llm07-insecure-plugin-design/">LLM07:2025 System Prompt Leakage - OWASP Gen AI Security Project</a></li>
<li><a href="https://portswigger.net/web-security/access-control">Access control vulnerabilities and privilege escalation | Web Security Academy</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者大体上印证并扩展了论文的结论，并提供了亲身经历：有人描述 ChatGPT 会周期性地发送未完成的提示词，有人指出 Perplexity 把 URL 中的 UUID 等同于隐私，还有人将其与 OpenAI 训练数据争议（私人 Codex 会话中未发表的草稿）联系起来，主张“开源模型必须胜出”。也有人追问风险究竟有多少来自智能体、多少来自底层平台 API，还有人以《辛普森一家》中“Milhouse 什么都告诉 Willie”的梗来调侃用户对这类助手的毫无保留。

**标签**: `#privacy`, `#conversational-ai`, `#llm-security`, `#web-tracking`, `#research-paper`

---

<a id="item-4"></a>
## [Anthropic：智谱 GLM-5.3 可自主实施网络攻击](https://www.anthropic.com/research/glm-5-3-and-the-spread-of-advanced-cyber-capabilities) ⭐️ 8.0/10

Anthropic 发布评估结论称，智谱 AI（Z.ai）的开放权重模型 GLM-5.3 已能自主构建并执行端到端网络攻击，在 ExploitBench 的 410 次尝试中成功 50 次，接近其自研 Claude Mythos Preview 的 56 次成功。报告还指出，GLM-5.3 的安全护栏可用简单方法绕过，模拟测试成功率为 64% 至 100%。 这一发现表明，自主攻击性网络能力已不再局限于闭源前沿模型——一个可公开下载的模型如今已接近领先闭源系统的水平。这也让开放权重发布的争论更加尖锐：模型内置的安全对齐可被下载者自行剥离，从而可能扩大能够实施自动化攻击的行为者范围。 从绝对数字看，成功率依然偏低——GLM-5.3 为 410 次尝试中成功 50 次，Claude Mythos Preview 为 56 次，因此该能力更应被视为“部分自主”而非稳定可靠。Anthropic 补充称，由于 GLM-5.3 以开放权重形式发布，用户可通过微调或改造削弱其拒答行为；而在模拟测试中，其护栏用直接了当的绕过手法即可突破，成功率介于 64% 至 100%。

telegram · zaihuapd · 9月29日 23:58

**背景**: ExploitBench 是安全研究人员用于开发、测试并评分漏洞利用代码的基准与工作台，覆盖多种漏洞类型，因此成功次数越高，意味着模型从发现漏洞到将其武器化的链条上能走得更远。开放权重（open weights）指模型训练所得的参数（即训练过程中学到的数值）被公开发布、任何人可下载运行，它与开源并不等同，因为训练数据和代码未必一同公开。越狱（jailbreak）则是指通过精心构造提示词，诱导模型输出其安全训练本应拒绝的内容；这属于对齐失效而非软件漏洞，因此即便模型本身未被攻破，这类问题依然存在。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.datalearner.com/benchmarks/exploitbench-jun-aug-2026">ExploitBench (Jun–Aug 2026)... | DataLearnerAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Open_weights">Open weights - Wikipedia</a></li>
<li><a href="https://casrai.org/dictionary/term/jailbreak-llm">LLM Jailbreak: How Prompts Bypass Guardrails — CASRAI</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#cybersecurity`, `#LLM`, `#open weights`, `#Anthropic`

---