---
layout: default
title: "Horizon Summary: 2026-08-14 (ZH)"
date: 2026-08-14
lang: zh
---

> 从 34 条内容中筛选出 11 条重要资讯。

---

1. [无需训练：将《毁灭战士》渲染器编译为 210 亿参数 Transformer](#item-1) ⭐️ 9.0/10
2. [GLM-5.3 发布：Z.ai Code Bench 提升 50%，权重两周后开源](#item-2) ⭐️ 9.0/10
3. [Qwen 3.8 27B：新本地模型推理与图像表现亮眼](#item-3) ⭐️ 8.0/10
4. [Opus 5 为何让人感觉更难用？文风隐晦、疑似面向智能体](#item-4) ⭐️ 8.0/10
5. [Firefox 成为唯一支持 uBlock Origin 的主流浏览器](#item-5) ⭐️ 8.0/10
6. [戏仿网站盘点烦人网页设计套路](#item-6) ⭐️ 8.0/10
7. [torch-preflight：静态检查 PyTorch 训练错误并估算显存的 linter](#item-7) ⭐️ 8.0/10
8. [小红书开源 dots3-note：280B MoE，仅 16B 激活参数](#item-8) ⭐️ 8.0/10
9. [法院下令谷歌一周内移除第三方应用商店安装障碍](#item-9) ⭐️ 8.0/10
10. [PostgreSQL 修复高危 to\_char 漏洞，攻击者可执行任意代码](#item-10) ⭐️ 8.0/10
11. [苹果联手阿里自研中国专属 AI 大模型，或成首个获批外企](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [无需训练：将《毁灭战士》渲染器编译为 210 亿参数 Transformer](https://www.reddit.com/r/MachineLearning/comments/1voazhm/i_compiled_dooms_renderer_into_a_21bparameter/) ⭐️ 9.0/10

作者使用自己编写的 Torchwright 编译器，将《毁灭战士》的渲染算法对应的计算图直接编译进一个 210 亿参数的 Transformer 权重中。生成的检查点是标准 Hugging Face 格式，无需任何训练即可在给定场景提示后输出包含像素绘制命令的 token 序列，重建游戏第一关 E1M1 的画面。 这个项目展示了从程序代码到 Transformer 参数的一条可行编译路径，意味着模型可以像执行程序一样精确运行算法，而不是仅靠训练来近似。这可能启发可解释、可验证的 AI 新方法，以及将传统代码库嵌入神经网络权重的新思路。 渲染一帧需要输入 3,614 个 token 的场景提示，并生成 53,747 个 token，解析为光标移动和像素绘制命令；在 NVIDIA B200 上整个生成约需 40 分钟，作者将其调侃为“35 FPD”（每天帧数），对比原版《毁灭战士》在 486 上的 35 FPS。加载检查点并解析输出的宿主程序仅 43 行 Python，而更长的计算图定义源码则被编译进权重中。

reddit · r/MachineLearning · /u/notforrob · 8月14日 15:50

**背景**: Transformer 是一种基于注意力机制的深度学习架构，通常需要在大型数据集上训练来学习统计规律。Torchwright 是一个编译器，能将固定的符号计算图直接翻译成 Transformer 权重——包括嵌入、注意力、前馈和输出权重矩阵——从而无需梯度下降即可将任意算法嵌入模型中。这项工作延续了作者之前“把计算器编译进 Transformer”的项目，也属于“在 Transformer 中精确实现算法”这一研究脉络。生成的检查点是标准 transformers 检查点，加载时无需 trust\_remote\_code。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ood.dev/posts/calculator/">A calculator, compiled into a transformer — Out of Distribution</a></li>
<li><a href="https://towardsdatascience.com/i-built-a-tiny-computer-inside-a-transformer/">I Built a Tiny Computer Inside a Transformer | Towards Data Science</a></li>

</ul>
</details>

**标签**: `#transformer`, `#compiler`, `#doom`, `#machine learning`, `#computation graphs`

---

<a id="item-2"></a>
## [GLM-5.3 发布：Z.ai Code Bench 提升 50%，权重两周后开源](http://z.ai/) ⭐️ 9.0/10

智谱发布了 GLM-5.3，沿用 GLM-5.2 基座，全部提升来自后训练。在 Z.ai 内部 Code Bench 上成绩较 GLM-5.2 提升 50%，并在 Terminal Bench 3.0 上达到开源最优。 GLM 是最广泛使用的开源权重大模型系列之一，此次在编程基准上提升 50% 且两周后开源权重，将对开发者和 AI 研究者产生广泛影响。这也表明仅靠后训练就能在不大改基座的情况下带来显著能力提升。 安全能力提升显著：漏洞利用基准成绩较 GLM-5.2 翻倍以上，智谱称已协助安全团队在 269 个项目中识别 2436 个漏洞，其中 1097 个为中高危。权重将在发布两周后开源。

telegram · zaihuapd · 8月14日 05:27

**背景**: GLM 是智谱 AI（Z.ai）开发的大语言模型系列，其开源权重版本在 AI/ML 社区中被广泛使用。后训练（post-training）是指在基座模型预训练之后进行的微调和对齐。Z.ai Code Bench 是智谱内部的编程评估基准，而 Terminal Bench 3.0 则是面向智能体命令行和计算机操作任务的公开基准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.turing.com/blog/introducing-terminal-bench-3-0">Terminal-Bench 3.0: Hard for the Right Reasons</a></li>
<li><a href="https://openrouter.ai/z-ai/glm-5.2">GLM 5.2 - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**社区讨论**: 评论者对 GLM-5.3 的智能体安全研究能力印象深刻，有人称它成功执行了包括零日漏洞和内核利用在内的红队场景。也有评论指出智谱似乎在大规模扫描开源软件并披露大量 CVE，还有人认为 GLM-5.3 仍落后于 Sol、Fable 等顶级闭源模型，且本质上是“GLM 5.2 加后训练魔法”。部分评论称赞发布说明读起来像研究论文而非营销宣传。

**标签**: `#AI`, `#LLM`, `#GLM-5.3`, `#open-source`, `#benchmark`

---

<a id="item-3"></a>
## [Qwen 3.8 27B：新本地模型推理与图像表现亮眼](https://huggingface.co/Qwen/Qwen3.8-27B-FP8) ⭐️ 8.0/10

阿里巴巴 Qwen 系列发布了 Qwen 3.8 27B，这是一个面向本地使用的 270 亿参数模型，提供 FP8 版本。早期社区测试显示，它能推理解决具有挑战性的私人基准测试并生成高质量图像，不过存在一些效率上的权衡。 该发布之所以重要，是因为社区成员称它是继 Gemma 4 之后第二个通过其私人推理基准的本地模型，而且能在笔记本电脑上运行。这表明先进的推理和多模态能力正日益走向本地用户，可能加速端侧 AI 的采用。 在私人基准测试中，该模型消耗的 token 数约为 Gemma 4 的 5 倍，启用 MTP 时耗时 12 分 30 秒。用户还注意到，与 Qwen 3.6 相比，其思考痕迹呈现出独特的“穴居人风格”，一些人报告显存使用效率不佳以及 Ollama 集成问题。

hackernews · erdaltoprak · 8月14日 15:00 · [社区讨论](https://news.ycombinator.com/item?id=49299605)

**背景**: Qwen 是阿里巴巴的大语言模型家族，其中许多模型以自由开源的 Apache 许可证分发。本地 LLM 完全在用户自己的设备上运行，无需云端调用，也不会将数据发送到外部服务器。这个 27B 模型是量化版本，旨在适配较高级的消费级硬件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://www.linkedin.com/pulse/quiet-revolution-why-local-llms-deserve-more-our-attention-kasam-g2l0e">The Quiet Revolution: Why Local LLMs Deserve More of Our Attention</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体积极，但在效率方面评价不一。一位用户称赞其推理与图像生成能力，称它通过了其他模型未能通过的私人基准测试，同时也注意到显存占用更高、速度更慢。另一位用户猜测这种不寻常的思考痕迹可能拖累 MTP 预测；还有人询问如何在 Ollama 中关闭思考，并分享了 Jinja 模板的解决思路。

**标签**: `#AI/ML`, `#Local LLMs`, `#Qwen`, `#Model Release`, `#Reasoning`

---

<a id="item-4"></a>
## [Opus 5 为何让人感觉更难用？文风隐晦、疑似面向智能体](https://mun-logadan.github.io/why-does-opus-5-feel-worse/) ⭐️ 8.0/10

Anthropic 的 Opus 5 因写作风格过于省略、抽象而受到开发者批评，用户推测其后续训练更重视智能体之间的通信而非人类可读性。 这反映出 AI 能力与用户体验之间日益加剧的矛盾：模型变得更强，但人类用起来可能更不舒服。同时，它预示着行业可能转向“智能体优先”的设计理念，从而改变 AI 系统与人的沟通方式。 评论指出 Opus 5 常用无生命名词作主语、句子绕弯子并突然跳跃。有用户因体验更自然而改用 OpenAI 的“Sol”，也有用户退回 Claude 4.8，还有一句代表性输出是：“The anti-vacuity floor is what blinds the gate to a vacuous case.”

hackernews · numeri · 8月14日 10:12 · [社区讨论](https://news.ycombinator.com/item?id=49296740)

**背景**: 像 Claude 这样的 AI 模型在大量人类文本上训练，输出通常模仿人类风格，但研究表明 LLM 会形成带有自己特点的写作模式。与此同时，随着多智能体系统日益普及，有人推测模型越来越针对简洁、机器可读的通信进行优化——这与 GibberLink 将 AI 智能体间交互延迟降低近 80%的现象类似。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.trinka.ai/blog/what-is-elliptical-construction-in-academic-writing/">What is Elliptical Construction in Academic Writing? Trinka 1</a></li>
<li><a href="https://www.futurity.org/large-language-models-artificial-intelligence-writing-3281512/">Text-generating AI models have different writing styles - Futurity</a></li>
<li><a href="https://medium.com/@adnanmasood/ai-to-ai-communication-strategies-among-autonomous-ai-agents-916c01d49c15">AI-to-AI Communication: Strategies Among Autonomous AI Agents | by Adnan Masood, PhD. | Medium</a></li>

</ul>
</details>

**社区讨论**: 评论者大多认为 Opus 5 的风格令人疲惫，但也承认其能力更强。一些人认为这证明模型如今是为智能体而非人类训练的，另一些人则表示更喜欢 OpenAI 的 Sol 或 Claude 4.8 等旧版本。

**标签**: `#AI`, `#LLM`, `#Opus5`, `#Model Training`, `#UX`

---

<a id="item-5"></a>
## [Firefox 成为唯一支持 uBlock Origin 的主流浏览器](https://www.pcworld.com/article/3212428/firefox-is-now-the-last-major-browser-that-still-supports-ublock-origin.html) ⭐️ 8.0/10

Firefox 现在是唯一完全支持 uBlock Origin 的主流浏览器，因为 Google Chrome 的 Manifest V3 变更有效限制了功能强大的广告拦截扩展。这一转变使 Firefox 成为想要完整广告拦截功能的用户的最后选择。 这一点很重要，因为 Chrome 拥有约 75% 的浏览器市场份额，其扩展变更影响到数百万用户的默认广告拦截体验。Firefox 现在成为注重隐私的用户和完整广告拦截扩展未来的主要避风港。 Chrome 的 Manifest V3 用 declarativeNetRequest API 取代了阻塞式 webRequest API，限制了 uBlock Origin 等扩展可以应用的规则数量和复杂度。Firefox 继续支持旧版 API 模式，使 uBlock Origin 能够保留其完整的过滤能力。

hackernews · DemiGuru · 8月14日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=49303202)

**背景**: Manifest V3 是 Chrome 扩展平台的最新版本，旨在改善隐私、安全和性能，但它限制了扩展拦截或修改网络请求的能力。declarativeNetRequest API 在浏览器本身评估请求，但允许的过滤规则数量远少于以前的 webRequest API。这使得在 Chrome 中无法实现 uBlock Origin 这样强大的内容拦截器，而 Firefox 则继续支持更宽松的扩展 API。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Manifest_V3">Manifest V3</a></li>
<li><a href="https://developer.chrome.com/docs/extensions/reference/api/declarativeNetRequest">chrome.declarativeNetRequest | API | Chrome for Developers</a></li>
<li><a href="https://www.eff.org/deeplinks/2021/12/googles-manifest-v3-still-hurts-privacy-security-innovation">Google’s Manifest V 3 Still Hurts Privacy, Security, and Innovation</a></li>

</ul>
</details>

**社区讨论**: 评论者大多批评 Google 的 Manifest V3 变更，有人称其故意关闭 API 自由，并指出现在只有在 Firefox 中才能从 Google 搜索中移除广告。还有人指出 Firefox 会在每次更新时审查 uBlock Origin 等流行扩展的安全性，少数用户则询问 uBlock Origin Lite 的有效性。

**标签**: `#browsers`, `#ad-blocking`, `#privacy`, `#Manifest V3`, `#Firefox`

---

<a id="item-6"></a>
## [戏仿网站盘点烦人网页设计套路](https://lxe.github.io/everywebsite/) ⭐️ 8.0/10

《Every Fucking Website》\(2020\) 是一个单页讽刺网站，通过重现弹窗、Cookie 横幅等常见恼人网页设计模式来嘲讽现代用户体验。该网站在 Hacker News 上引发了关于网站为何使用这些模式的激烈讨论。 该网站表达了用户对侵扰性设计的普遍不满，而讨论也揭示了真实的矛盾：用户讨厌的设计模式之所以存在，常常是因为它们能提升商业指标。这对需要在用户体验与转化目标之间权衡的网页开发者和设计师而言具有现实意义。 评论者指出，这个讽刺作品其实不够逼真：页面加载很快且只使用一个域名，而真实的网站往往会加载十几个第三方脚本。网站还遗漏了其他常见模式，比如自动播放视频、“在 App 中打开更好”的提示以及强制登录账户等。

hackernews · doubletwoyou · 8月14日 14:31 · [社区讨论](https://news.ycombinator.com/item?id=49299222)

**背景**: 现代网站经常使用暗黑模式（dark patterns），即经过精心设计、诱使用户做出非本意行为的界面技巧，例如订阅新闻邮件或接受 Cookie。用户体验设计师 Harry Brignull 在 2010 年创造了这个术语，目的是点名批评这类欺骗性界面。Every Fucking Website 通过单独一个页面重现其中最恼人的模式来讽刺这一趋势，让用户发现原来这么多网站的样式和行为如此雷同。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lxe.github.io/everywebsite/">Every Fucking Website</a></li>
<li><a href="https://everyfuckingwebsite.com/">every fucking website . — a short essay in two screens</a></li>
<li><a href="https://en.wikipedia.org/wiki/Dark_pattern">Dark pattern</a></li>

</ul>
</details>

**社区讨论**: 评论者很欣赏这个讽刺作品，并开玩笑式地补充了缺失的恼人元素，比如加载过慢和来自多个域名的追踪器。一位用户分享说，一个“某人刚刚购买了某商品”的弹窗显著提升了他们 Shopify 店铺的转化率，因此即使有些自我厌恶也值得使用——这就是他们所说的“切斯特顿弹窗”。还有人开玩笑说要提交 bug 报告，因为该网站加载太快，而且不需要 JavaScript 也能访问。

**标签**: `#web design`, `#UX`, `#satire`, `#frontend`, `#popups`

---

<a id="item-7"></a>
## [torch-preflight：静态检查 PyTorch 训练错误并估算显存的 linter](https://www.reddit.com/r/MachineLearning/comments/1vo8vv0/a_linter_for_pytorch_torchpreflight_p/) ⭐️ 8.0/10

开发者发布了 torch-preflight，这是一个用于 PyTorch 的静态 linter，可检测 13 种常见训练循环错误，例如通过 loss.append\(loss\) 保留 autograd 计算图、缺少 zero\_grad\(\)、以及梯度累积时未缩放损失。它还能在不运行代码、不安装 GPU 环境的情况下估算训练脚本的 GPU 显存需求。 这些错误经常让机器学习工程师浪费大量 GPU 时间，并导致显存溢出，因此在运行前发现它们可以节省大量时间和金钱。显存估算功能还能帮助开发者在付费租用实例前判断训练能否在目标 GPU 上跑通。 该工具仍处于开发阶段，作者指出误报是 linter 的关键问题，目前主要的大型测试目标只有 PyTorch 源码树。显存估算目前与实测峰值相差在 4% 以内，但仅基于四模型在一张 T4 GPU 上的测试结果。

reddit · r/MachineLearning · /u/LeJanbandhu · 8月14日 14:30

**背景**: PyTorch 的 autograd 通过动态计算图来自动计算梯度；调用 backward\(\) 后旧图会被释放，并在下一次迭代时重新构建。如果把 loss 张量追加到列表中，整张计算图会一直被保留，导致显存不断增长直至溢出。缺少 zero\_grad\(\) 会让梯度跨迭代累积，而梯度累积时若不除以累积步数，会改变有效学习率。在 DDP 分布式训练中，DistributedSampler 用于确保每个 rank 拿到不同的数据子集；缺少它时所有 rank 会在相同 batch 上训练。torch-preflight 通过静态分析来发现这些错误，而无需导入或执行用户代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.pytorch.org/tutorials/beginner/blitz/autograd_tutorial.html">A Gentle Introduction to torch.autograd — PyTorch Tutorials 2 ...</a></li>
<li><a href="https://docs.pytorch.org/tutorials/beginner/ddp_series_theory.html">What is Distributed Data Parallel (DDP) — PyTorch Tutorials...</a></li>
<li><a href="https://iq.opengenus.org/gradient-accumulation/">Gradient Accumulation [+ code in PyTorch]</a></li>

</ul>
</details>

**标签**: `#PyTorch`, `#linter`, `#static analysis`, `#deep learning`, `#debugging`

---

<a id="item-8"></a>
## [小红书开源 dots3-note：280B MoE，仅 16B 激活参数](https://x.com/dotsstudioai/status/2088083314855018521) ⭐️ 8.0/10

小红书 dots 实验室开源了 dots3-note preview，这是 dots3 系列首个开放权重模型。它拥有 280B 总参数、仅 16B 激活参数，支持 512K 上下文，并可处理文字、图片、视频和音频等模态。 此次发布意义重大：它将一个大规模混合专家模型以较低推理成本带入开源社区，使先进 AI 更加可及。同时，它引入了新的强化学习方法（TEMPO）和真实场景智能体基准，可能影响未来智能体的训练与评估方式。 该模型总参数 280B，但每次仅激活 16B，且支持 512K token 的上下文窗口。它采用名为 TEMPO 的新强化学习方法，通过自批判和测试时价值估计训练长程智能体；权重已在 Hugging Face 开源，并同步发布 VibeSearchBench、VibeLifeBench 两个新基准。

telegram · zaihuapd · 8月14日 08:27

**背景**: 混合专家（MoE）模型是一种使用多个专用子网络（专家）的神经网络，但每次输入只激活其中一部分。这将总参数与激活参数解耦：激活参数决定推理速度和成本，因此一个 280B 的 MoE 模型仅激活 16B 时，其运行速度可媲美 16B 稠密模型，同时保留更大模型的容量。本次新发布的基准和强化学习方法旨在提升智能体在真实场景中的长程行为表现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://localmodel.run/guides/mixture-of-experts">Mixture of experts (MoE) explained for local LLMs · localmodel.run</a></li>
<li><a href="https://arxiv.org/abs/2605.27882">[2605.27882] VibeSearchBench: Benchmarking Long-horizon ...</a></li>
<li><a href="https://github.com/VibeBench/VibeSearchBench">GitHub - VibeBench/VibeSearchBench: The hardest search ...</a></li>

</ul>
</details>

**标签**: `#MoE`, `#Open Source`, `#LLM`, `#Reinforcement Learning`, `#Multimodal`

---

<a id="item-9"></a>
## [法院下令谷歌一周内移除第三方应用商店安装障碍](https://www.androidauthority.com/google-play-store-remove-third-party-app-store-friction-3698697/) ⭐️ 8.0/10

美国地区法官 James Donato 下令谷歌在一周内简化竞品安卓应用商店的安装流程。法院命令要求移除 Play Store 中额外的步骤和警告弹窗，这些被法院称为蓄意制造的“反竞争摩擦”。 这项裁决挑战了谷歌对安卓应用分发的控制，可能重塑用户发现和安装应用的方式。它为针对主导平台运营者的反垄断执法开创了先例，可能使 Epic Games Store 等第三方应用商店受益。 该禁令源于 Epic 诉谷歌反垄断案，陪审团裁定谷歌在安卓应用分发领域构成非法垄断。谷歌须让安装第三方应用商店像安装普通安卓应用一样直接。该裁决针对当前的多人操作流程，即用户必须先点击“查看”后才会出现“安装”按钮。

telegram · zaihuapd · 8月14日 09:55

**背景**: 安卓是一个开放平台，允许侧载（sideloading），即从官方 Google Play Store 以外安装应用。然而，谷歌历来在安装第三方应用商店时增加警告和额外步骤，并以 Google Play Protect 的安全考虑为由。Epic 诉谷歌一案对这一做法提出质疑，认为谷歌利用技术壁垒劝阻用户放弃 Play Store。法院的命令旨在减少这些障碍，但谷歌仍可能保留部分安全警告。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.google.com/googleplay/answer/2812853?hl=en">Use Google Play Protect to help keep your apps safe &amp; your ... Developer Guidance for Google Play Protect Warnings Use Google Play Protect to help keep your apps safe and your ... Google Play Protect is blocking your apps now—here&#x27;s how to ... Why Your Phone Suddenly Shows Security Warning After ... New Google Play Store Alert—Stop Using This Dangerous Setting</a></li>
<li><a href="https://www.xda-developers.com/how-to-sideload-install-android-app-apk/">How to sideload and install apps on Android as APKs or App Bundles</a></li>

</ul>
</details>

**标签**: `#Android`, `#Google`, `#Antitrust`, `#App Store`, `#Epic Games`

---

<a id="item-10"></a>
## [PostgreSQL 修复高危 to\_char 漏洞，攻击者可执行任意代码](https://www.postgresql.org/support/security/CVE-2026-14669/) ⭐️ 8.0/10

PostgreSQL 披露高危漏洞 CVE-2026-14669，该漏洞存在于 to\_char\(timestamptz\) 函数处理超长 POSIX 时区缩写时，可导致堆缓冲区溢出，从而允许执行任意代码。修复版本为 18.6、17.11、16.15、15.19 和 14.24。 该漏洞对数据库管理员至关重要，因为低权限的已认证数据库用户可在 PostgreSQL 服务器上获得操作系统级别的代码执行能力。由于 PostgreSQL 使用广泛，建议立即升级以防止服务器被入侵。 该漏洞的 CVSS 评分为 8.8，且需要低权限数据库账户，并非无需认证即可利用。升级只需替换程序文件并重启服务，无需运行 pg\_upgrade 或转储数据库；由于 18.5 存在回归问题，18 系列用户应直接升级至 18.6。

telegram · zaihuapd · 8月14日 14:35

**背景**: PostgreSQL 的 to\_char\(\) 函数用于将时间戳、间隔和数字转换为格式化字符串。堆缓冲区溢出是指向堆内存区域写入超出分配范围的数据，可能被利用来执行任意代码。POSIX 时区缩写是时区规范的一部分，过长的缩写会触发 to\_char\(timestamptz\) 代码路径中的溢出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.postgresql.org/docs/current/functions-formatting.html">PostgreSQL : Documentation: 18: 9.8. Data Type Formatting Functions</a></li>
<li><a href="https://en.wikipedia.org/wiki/Heap_overflow">Heap overflow - Wikipedia</a></li>
<li><a href="https://cwe.mitre.org/data/definitions/122.html">CWE - CWE-122: Heap-based Buffer Overflow (4.20)</a></li>

</ul>
</details>

**标签**: `#PostgreSQL`, `#CVE`, `#security`, `#vulnerability`, `#database`

---

<a id="item-11"></a>
## [苹果联手阿里自研中国专属 AI 大模型，或成首个获批外企](https://www.reuters.com/business/retail-consumer/apple-trains-its-own-ai-model-china-market-with-alibabas-support-sources-say-2026-08-14/) ⭐️ 8.0/10

据知情人士称，苹果已在阿里巴巴支持下为中国市场专门训练了一款大语言模型。Apple Intelligence 预计将在未来数月随 iOS 更新在华上线，中国网信办已于 2026 年 7 月对该服务完成备案。 若获批，苹果将成为首家获准在华提供自有生成式 AI 模型的外国公司，这是重要的监管里程碑。此举让苹果能更好地掌控中国市场的 AI 体验，并可能重塑中国 AI 助手领域的竞争格局。 这一转变标志着苹果不再像此前那样依赖中国的第三方模型。网信办备案属于中国生成式 AI 算法登记与安全评估流程的一部分；2026 年 7 月 15 日发布的端侧生成式 AI 备案名单中明确列入了 Apple Intelligence。

telegram · zaihuapd · 8月14日 14:47

**背景**: Apple Intelligence 是苹果于 2024 年 6 月 10 日在 WWDC 上发布的 AI 功能套件，结合设备端与服务器端处理，并集成到 iOS 18、iPadOS 18 和 macOS Sequoia 中。在中国大陆，根据《生成式人工智能服务管理暂行办法》等相关规定，生成式 AI 服务在向公众提供前必须完成算法备案与安全评估。此次备案是一种备案披露要求而非新规，有助于苹果满足当地监管预期。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theleveragedyears.com/ai-regulation-news/china-cac-on-device-generative-ai-filing-apple-intelligence-2026">China Publishes On-Device GenAI Filing List, Names Apple ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence</a></li>
<li><a href="https://multigrid.ai/learn/china-generative-ai-measures-filing">China&#x27;s Generative AI Measures: the Registration and Filing ...</a></li>

</ul>
</details>

**标签**: `#Apple`, `#AI`, `#China`, `#Alibaba`, `#Regulation`

---