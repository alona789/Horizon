---
layout: default
title: "Horizon Summary: 2026-08-05 (ZH)"
date: 2026-08-05
lang: zh
---

> 从 38 条内容中筛选出 11 条重要资讯。

---

1. [Waymo 在达拉斯全面开放无人驾驶打车服务](#item-1) ⭐️ 8.0/10
2. [DeepSeek V4 Flash 可在单个 AMD MI300X 上运行](#item-2) ⭐️ 8.0/10
3. [联邦快递的合法邮件正在削弱钓鱼邮件检测](#item-3) ⭐️ 8.0/10
4. [Oxide Computer 完成 4.45 亿美元 D 轮融资，推进机架级云硬件](#item-4) ⭐️ 8.0/10
5. [Keyv 及相关 npm 包在 Shai-Hulud 供应链攻击中沦陷](#item-5) ⭐️ 8.0/10
6. [Xbox 宕机导致实体光盘游戏无法游玩，暴露在线 DRM 依赖](#item-6) ⭐️ 8.0/10
7. [MiniMax-H3 全能模态模型已移植到 MLX，苹果芯片可本地运行](#item-7) ⭐️ 8.0/10
8. [华为科学家警告英伟达芯片规模扩张将触及物理极限](#item-8) ⭐️ 8.0/10
9. [谷歌为 Anthropic 搭建 2000 亿美元 AI 芯片融资机器](#item-9) ⭐️ 8.0/10
10. [我国首部 L3/L4 自动驾驶强制性国标正式发布。](#item-10) ⭐️ 8.0/10
11. [白宫急转开源 AI 监管立场，硅谷分歧加剧](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Waymo 在达拉斯全面开放无人驾驶打车服务](https://waymo.com/blog/shorts/dallas-open-to-all/) ⭐️ 8.0/10

Waymo 宣布，其无人驾驶打车服务现已在德克萨斯州达拉斯向所有人开放。这标志着其自动驾驶汽车业务向新的主要都市区的最新扩张。 此次扩张将全无人驾驶打车服务带给这个庞大、高度依赖汽车的都会区的数百万居民。它标志着 Waymo 在美国的持续扩张，并可能加剧打车市场的竞争。 达拉斯-沃斯堡是美国最大、最分散的大都市区之一，人口密度低且公共交通有限。该服务面向所有客户开放，而非排队名单或受限试点，这反映出 Waymo 对其技术的信心。

hackernews · xnx · 8月4日 18:29 · [社区讨论](https://news.ycombinator.com/item?id=49172836)

**背景**: Waymo 是 Alphabet 旗下开发自动驾驶汽车技术并在美国多个城市运营无人驾驶出租车服务的子公司。“无人驾驶打车服务”意味着顾客可以通过应用叫车，且车内没有任何人类安全驾驶员。扩展到达拉斯意义重大，因为需要适应当地的交通模式、天气和道路基础设施。

**社区讨论**: 评论者们的看法褒贬不一。有人称赞 Waymo 车辆是安全且可预测的道路参与者；一位商业房地产专业人士则提出，无人驾驶汽车可能通过降低停车和交通成本，成为一种非常有效的可负担住房政策。另一些人则担心资金会从地方经济中外流，因为利润可能流向外地，但也有人指出仍需本地岗位来维护和清洁车辆。

**标签**: `#autonomous vehicles`, `#Waymo`, `#ride-hailing`, `#urban mobility`, `#transportation`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash 可在单个 AMD MI300X 上运行](https://github.com/ryanzhou/deepseek-v4-flash-mi300x) ⭐️ 8.0/10

一份新的指南和分析演示了 DeepSeek V4 Flash 在单个 AMD MI300X 上以高吞吐量运行，但上下文长度从 1M 降至 256k token。 这证明大型 MoE 模型可以在单块 GPU 上提供服务，使 DeepSeek V4 Flash 在 AMD 硬件上更容易使用，并可能降低高吞吐量场景的部署成本。 该指南报告吞吐量超过每秒 150 token，但上下文窗口从原生 1M 降至 256k。MI300X 是配备 192GB HBM3 的 OAM 模块，而 DeepSeek V4 Flash 的 MoE 导出为原生 MXFP4 量化，因此能装入显存。

hackernews · zhoutong · 8月4日 10:00 · [社区讨论](https://news.ycombinator.com/item?id=49166386)

**背景**: DeepSeek V4 Flash 是一个混合专家（MoE）语言模型，总参数 284B，激活参数 13B，支持 1M token 上下文。AMD MI300X 是基于 CDNA 3 架构的加速器，配备 192GB HBM3 显存和 5.3 TB/s 带宽。MoE 模型每个 token 只激活部分参数，因此能在单块 GPU 上高效推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/DeepSeek-V4-Flash · Hugging Face</a></li>
<li><a href="https://www.amd.com/en/products/accelerators/instinct/mi300/mi300x.html">AMD Instinct™ MI300X Accelerators</a></li>
<li><a href="https://deepinfra.com/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/DeepSeek-V4-Flash - Demo - DeepInfra</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍赞赏这项工作并指出实际注意点：MI300X 仅以 OAM 模块形式出售（如 8 卡整块约 25 万欧元），而基于 PCIe 的 MI350P 只有 144GB 显存。有用户提到像 DwarfStar 这样的先前工作能用更少显存达到类似效果，另一位则认为把上下文降至 256k 是相当实用的折中，可与 Codex 相提并论。

**标签**: `#deepseek`, `#AMD`, `#MI300X`, `#inference`, `#quantization`

---

<a id="item-3"></a>
## [联邦快递的合法邮件正在削弱钓鱼邮件检测](https://www.troyhunt.com/thanks-fedex-this-is-why-we-keep-getting-phished/) ⭐️ 8.0/10

在 2024 年的一篇博文中，安全研究员 Troy Hunt 批评了联邦快递（FedEx）的合法邮件做法，认为它们训练用户接受看起来完全像钓鱼邮件的消息。他强调，FedEx 官方邮件能绕过垃圾邮件过滤器，却包含与钓鱼攻击相同的警示信号，从而削弱了用户识别诈骗的能力。 这件事很重要，因为钓鱼仍然是主要的攻击途径之一；当可信品牌发送令人困惑、出其不意的邮件时，安全培训与自动过滤器的价值都会大打折扣。它说明仅靠邮件认证无法解决用户信任问题，企业和邮件服务商都需要重新思考合法邮件的设计与投递方式。 这篇文章的核心是域名验证与钓鱼向量：FedEx 的邮件能够通过 SPF、DKIM 和 DMARC 检查，却仍包含类似诈骗的链接、附件和快递通知措辞。问题在于结构性的——认证协议验证的是发件人身份，而非邮件是否恶意，因此一封通过认证的 FedEx 邮件仍可能看起来与钓鱼邮件一模一样。

hackernews · stymaar · 8月4日 21:09 · [社区讨论](https://news.ycombinator.com/item?id=49175192)

**背景**: SPF、DKIM 和 DMARC 等邮件认证协议通过 DNS 记录与加密签名来证明哪些系统可以代表某个域名发信，从而帮助收件方拦截伪造邮件。反钓鱼检测通常结合自动内容扫描、发件人信誉以及用户自身的警惕性，但当合法发件人表现得像钓鱼者时，这套机制就很难发挥作用。这也是为什么一封来自大品牌且通过认证的邮件，仍然可能让过滤系统和普通用户都感到困惑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techtarget.com/searchsecurity/answer/Email-authentication-How-SPF-DKIM-and-DMARC-work-together">SPF , DKIM and DMARC : What are they and how do they... | TechTarget</a></li>
<li><a href="https://www.volanea.com/blog/email-authentication-protocols">Email Authentication Protocols : SPF , DKIM and DMARC Guide</a></li>
<li><a href="https://www.expressvpn.com/blog/phishing-detection/">How to detect phishing and prevent scams online</a></li>

</ul>
</details>

**社区讨论**: 评论区用户分享了类似案例：有人收到过 FedEx 官方但看起来可疑的海关通知，邮件来自某位具体员工并附带 PDF；有人发现 Google 官方存储空间提醒邮件使用了短域名 c.gle；还有人指出 IRS 电话系统的语音与诈骗呼叫中心一模一样。多位评论者还认为，大量新通用顶级域名的出现让普通用户更难判断钓鱼链接。整体来看，讨论强烈支持 Hunt 的观点，并补充了更多合法机构助长钓鱼问题的实例。

**标签**: `#security`, `#phishing`, `#email`, `#FedEx`, `#Troy Hunt`

---

<a id="item-4"></a>
## [Oxide Computer 完成 4.45 亿美元 D 轮融资，推进机架级云硬件](https://www.sec.gov/Archives/edgar/data/1795071/000179507126000002/xslFormDX01/primary_doc.xml) ⭐️ 8.0/10

根据美国证券交易委员会（SEC）的 Form D 文件，Oxide Computer Company 近日完成了 4.45 亿美元的 D 轮融资。此前的 C 轮融资为 2 亿美元，此次融资意味着公司融资步伐显著加快。 这轮大规模融资表明，投资者对机架级云硬件作为超大规模公有云的本地替代方案抱有强烈信心。这笔资金可能加速 Oxide 的产品交付，并影响企业构建私有云基础设施的方式。 这轮 D 轮融资记录在 SEC Form D 文件中，此前公司已完成 2 亿美元 C 轮融资、2025 年 1 亿美元 B 轮融资以及 2023 年 4400 万美元 A 轮融资。社区讨论中对销售跟进和是否大规模发货提出了实际担忧，尽管其技术团队备受好评。

hackernews · depr · 8月4日 20:13 · [社区讨论](https://news.ycombinator.com/item?id=49174407)

**背景**: Oxide Computer Company 是一家硬件初创公司，专注于机架级“云计算机”（Cloud Computer）系统，将硬件和软件统一用于本地数据中心，旨在将超大规模云架构引入企业内部。该公司于 2023 年发布了首款商用产品，此后完成了多轮融资。其理念是将整个机架视为一台计算机，这与传统服务器设计形成鲜明对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://oxide.computer/blog/how-oxide-cuts-data-center-power-consumption-in-half">A rack - scale design that drives data center power efficiency.</a></li>
<li><a href="https://oxide.computer/blog/oxide-unveils-the-worlds-first-commercial-cloud-computer">Oxide Unveils the World&#x27;s First Commercial Cloud Computer</a></li>
<li><a href="https://www.bloomberg.com/profile/company/1776316D:US">Oxide Computer Co - Company Profile and News - Bloomberg Markets</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论对产品理念和团队总体持正面态度，用户称赞其技术愿景，并对未来的“Oxide and Friends”播客表示期待。但也出现了一些实际担忧：一位工程副总裁称自己提交了销售咨询却从未收到回复，尽管公司每年在 AWS 上花费 90 万美元；另一位评论者质疑该公司是否真的发货，因为公开的图片和部署案例很少。

**标签**: `#funding`, `#hardware`, `#startup`, `#oxide`, `#cloud`

---

<a id="item-5"></a>
## [Keyv 及相关 npm 包在 Shai-Hulud 供应链攻击中沦陷](https://www.aikido.dev/blog/keyv-and-friends-compromised-in-npm-supply-chain-attack) ⭐️ 8.0/10

Shai-Hulud 蠕虫的新一波攻击已攻破 Keyv 及包括 cacheable 在内的相关 npm 包，并正在 npm 生态中活跃传播。该蠕虫会窃取凭据、向每个可写的 npm 包发布自身，并在 GitHub 仓库中植入执行钩子。 Keyv 是一款被广泛使用的键值存储库，有 1700 多个项目依赖它，因此它的沦陷可能在 JavaScript 生态中产生连锁反应。此次攻击凸显了开源依赖供应链攻击的系统性风险，以及采用更完善安全实践的紧迫性。 据 JFrog 安全研究，该活动以 npm 包为目标，已影响超过 400 个包。该蠕虫具备窃取凭据、向可写的 npm 包自发布以及在 GitHub 仓库中植入执行钩子的能力，因此具有很强的持久性。

hackernews · cimi\_ · 8月4日 11:01 · [社区讨论](https://news.ycombinator.com/item?id=49166874)

**背景**: npm 是 JavaScript 最大的包注册表，拥有数百万个包和数十亿次下载。Shai-Hulud 是一种自我复制的蠕虫，它通过窃取维护者凭据并利用这些凭据发布恶意版本来攻破包；它可以自动传播到其他可写包，导致整个生态的大范围沦陷。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.jfrog.com/post/shai-hulud-is-back-august/">Major Shai Hulud campaign strikes npm again, affecting keyv and 400+ packages - JFrog Security Research</a></li>
<li><a href="https://www.cisa.gov/news-events/alerts/2025/09/23/widespread-supply-chain-compromise-impacting-npm-ecosystem">Widespread Supply Chain Compromise Impacting npm Ecosystem | CISA</a></li>
<li><a href="https://unit42.paloaltonetworks.com/npm-supply-chain-attack/">&quot;Shai-Hulud&quot; Worm Compromises npm Ecosystem in Supply Chain Attack (Updated November 26)</a></li>

</ul>
</details>

**社区讨论**: 社区评论以担忧但积极的态度为主，用户分享了缓解策略，例如使用 devcontainers 隔离开发环境、对新增包禁用 pre-install/post-install 钩子，以及使用 Packj 等工具扫描入侵指标。也有人批评脆弱的依赖系统，并建议 GitHub 可检测并阻止 Shai-Hulud 的数据外泄仓库。

**标签**: `#security`, `#npm`, `#supply-chain`, `#open-source`, `#malware`

---

<a id="item-6"></a>
## [Xbox 宕机导致实体光盘游戏无法游玩，暴露在线 DRM 依赖](https://birchtree.me/blog/xbox-goes-down-you-cant-play-games-you-own-on-disc/) ⭐️ 8.0/10

在最近一次 Xbox 网络故障期间，用户发现自己连已拥有的实体光盘游戏也无法启动，因为主机在运行游戏前需要进行在线验证。这一事件让人们直观看到了如今约束 Xbox 游戏「所有权」的始终在线 DRM。 这一事件表明，实体介质已不再保证离线可用，因为「拥有」光盘仍然取决于微软服务器持续可用。它让整个行业围绕数字所有权、以及消费者几十年后是否还能玩到已购游戏的争论进一步升温。 始终在线 DRM 即使内容本身存放在光盘上，也可能在服务器故障时导致游戏无法运行。此次事件还凸显出，许多光盘实际只充当许可证密钥，而不是完整的游戏数据，不少游戏在游玩前仍需下载大量内容。

hackernews · surprisetalk · 8月4日 12:01 · [社区讨论](https://news.ycombinator.com/item?id=49167448)

**背景**: 始终在线 DRM（always-online DRM）是一种数字版权管理形式，要求消费者在使用产品时持续连接服务器，通常用于防止盗版。它一直存在争议，因为会给合法购买者带来不便，并会在服务器宕机时形成单点故障。近年来，实体游戏光盘越来越多地被当作许可证密钥而非完整游戏数据的载体，这意味着即使是「离线」所有权也可能依赖在线验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Always-on_DRM">Always-on DRM</a></li>
<li><a href="https://cardozoaelj.com/2021/09/27/always-online-drm-and-video-games/">Always Online DRM and Video Games - Cardozo AELJ</a></li>
<li><a href="https://houstonianonline.com/its-time-to-say-goodbye-to-physical-games-vertical/">It&#x27;s time to say goodbye to physical games | vertical</a></li>

</ul>
</details>

**社区讨论**: 评论者大多表达了沮丧和无奈，并将如今依赖网络的游戏与旧世代主机进行对比——旧机器无需联网就能运行光盘，并且可在本地托管多人游戏。一些人认为，核心问题不在于实体版还是数字版，而在于所有权权利，例如永久访问、离线游玩、转售和传给后代。还有用户讲述，自己为了启动 Steam 上的《光环：士官长合集》，被迫走完创建账户的流程。

**标签**: `#DRM`, `#gaming`, `#digital-ownership`, `#Xbox`, `#outage`

---

<a id="item-7"></a>
## [MiniMax-H3 全能模态模型已移植到 MLX，苹果芯片可本地运行](https://simonwillison.net/2026/Aug/4/minimax-h3-mlx/#atom-everything) ⭐️ 8.0/10

MiniMax 发布了 MiniMax-H3，这是一个通用的全能模态生成系统，可接收文本、图像、音频和视频，并生成最长 15 秒、带音频的视频片段。两天后，Python 包 PipeNetwork/minimax-h3-mlx 将该模型移植到 MLX，使其能够在苹果芯片上本地运行；Simon Willison 在 M5 Max MacBook Pro 上演示了这一过程。 该移植让个人开发者和创作者可以在本地苹果硬件上使用尖端的全能模态视频生成模型，减少对云端 API 的依赖。它也凸显了 MLX 生态系统的活力：新模型发布数天内就被适配到苹果芯片。 运行该模型需要下载约 115 GB 的模型文件，在 Simon Willison 的机器上生成一段视频耗时不到 45 分钟。由于没有提供音频提示词指导，初次输出的音频是“类似语音的奇怪噪音”，MiniMax 的提示词指南中包含了获得更好结果的说明。

rss · Simon Willison · 8月4日 19:10

**背景**: MLX 是苹果机器学习研究团队推出的数组框架，专为在苹果芯片上进行高效、灵活的机器学习研究而设计。全能模态 AI 系统能够以统一方式理解和生成多种数据类型——文本、图像、音频和视频。MiniMax-H3 是一个开放权重、通用的多模态模型，可以结合这些模态生成带原生立体声的 2K 视频，而这次 MLX 移植使得这类生成可以完全在设备端完成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple silicon · GitHub</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between Tasks and Modalities - MiniMax Research | MiniMax</a></li>
<li><a href="https://huggingface.co/MiniMaxAI/MiniMax-H3">MiniMaxAI/MiniMax-H3 · Hugging Face</a></li>

</ul>
</details>

**标签**: `#AI`, `#MLX`, `#video generation`, `#multimodal`, `#Apple Silicon`

---

<a id="item-8"></a>
## [华为科学家警告英伟达芯片规模扩张将触及物理极限](https://www.bloomberg.com/news/articles/2026-08-04/huawei-s-top-scientist-warns-of-chip-limit-nvidia-will-soon-face) ⭐️ 8.0/10

7 月底，华为首席半导体科学家廖恒在一次罕见的四小时公开采访中警告，英伟达等芯片巨头通过不断增加计算芯片和高带宽内存来扩展规模的做法终将触及物理极限。他还介绍了华为提出的 LogicFolding 替代路径，首款采用该框架的手机芯片预计今年晚些时候亮相。 这一警告凸显了半导体产业正分化为两个独立生态系统的趋势，并对主流的规模扩张路径提出挑战。随着华为推动替代架构以绕过物理极限和美国制裁，AI 硬件领域的竞争格局可能发生重大变化。 LogicFolding 将逻辑电路物理折叠并堆叠为双层架构，从而缩短布线长度、降低负载和传播延迟。华为的韬定律（τ Scaling Law）用“时间缩放”取代“几何缩放”，优先关注信号速度而非组件尺寸，有望在不使用 EUV 光刻的情况下将晶体管密度提升 55%。

telegram · zaihuapd · 8月4日 08:04

**背景**: 摩尔定律预测晶体管密度大约每两年翻一番，但几何微缩正逼近根本性的物理极限。美国制裁限制了华为获得先进 EUV 光刻设备，因此 LogicFolding 提供了一种在不依赖尖端制造工具的情况下提升密度与性能的途径。韬定律（τ Scaling Law）是一个“时间缩放”框架，优化的是数据在系统中移动的速度，而非组件有多小。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/huawei-claims-sanctions-busting-breakthrough-with-1-4nm-class-chips-by-2031-claims-55-percent-higher-transistor-density-firm-claims-new-logicfolding-chip-architecture-can-bypass-euv-restrictions-introduces-tau-scaling-law-to-replace-moores-law">Huawei claims sanctions-busting breakthrough with 1.4nm-class chips by 2031, claims 55% higher transistor density — firm claims new LogicFolding chip architecture can bypass EUV restrictions, introduces &#x27;Tau Scaling Law&#x27; to replace Moore&#x27;s Law | Tom&#x27;s Hardware</a></li>
<li><a href="https://www.huaweicentral.com/huawei-logicfolding-architecture-everything-you-need-to-know/">Huawei LogicFolding Architecture: Everything you need to know - Huawei Central</a></li>
<li><a href="https://www.chosun.com/english/industry-en/2026/05/26/Z4I566GOLJAPNOE53763RN7V2E/">Huawei&#x27;s &#x27;Tao Law&#x27; Challenges TSMC, Samsung in Semiconductor Race</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#AI chips`, `#Huawei`, `#Nvidia`, `#hardware limits`

---

<a id="item-9"></a>
## [谷歌为 Anthropic 搭建 2000 亿美元 AI 芯片融资机器](https://www.ft.com/content/549f2e23-5aa2-49c7-9ea6-a9784ab7087c) ⭐️ 8.0/10

据《金融时报》调查，谷歌悄然搭建了史上最大规模的基础设施融资架构之一，总额约 2000 亿美元，用于向 Anthropic 交付超 1500 亿美元 AI 芯片。今年 6 月，特殊目的载体 Compute SPV 完成首批交易，购入约 350 亿美元硬件，约合 1 吉瓦算力、100 万颗 TPU。 这一前所未有的融资结构使没有信用评级的 Anthropic 能够获得大规模 AI 算力，而无需将数千亿美元硬件计入自身资产负债表。它还创建了由谷歌、博通、阿波罗、黑石和摩根士丹利参与的 AI 基础设施新型风险分担模式，对整个行业如何为超大规模 AI 提供资金具有深远影响。 约 2000 亿美元合同中约八成直接与芯片挂钩；博通购买并协助融资芯片，阿波罗与黑石出资购买硬件后回租给 Anthropic。该模式借鉴波音、GE 推销飞机和发动机的厂商融资玩法，多家加密矿企也参与分担风险。

telegram · zaihuapd · 8月4日 10:52

**背景**: 特殊目的载体（SPV）是一种法律壳实体，用于为巨额资本支出融资，而无需将债务合并到发起人资产负债表上。谷歌的 TPU（张量处理单元）是为加速机器学习工作负载专门设计的定制 ASIC 芯片；Compute SPV 购入的硬件包括约 100 万颗 TPU，约合 1 吉瓦算力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rondodson.substack.com/p/the-new-shadow-system-ai-finance">The New Shadow System: AI Finance and the SPV</a></li>
<li><a href="https://magdigit.com/ironwood-the-first-google-tpu-for-the-age-of-inference/">Ironwood: The first Google TPU for the age of inference - MagDIGIT</a></li>
<li><a href="https://www.financely-group.com/ai-data-center-finance-sale-leasebacks">AI Data-Center Finance &amp; Sale - Leasebacks</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#Google`, `#Anthropic`, `#finance`, `#AI chips`

---

<a id="item-10"></a>
## [我国首部 L3/L4 自动驾驶强制性国标正式发布。](https://wap.miit.gov.cn/jgsj/zbys/qcgy/art/2026/art_a1d2072374884287b67048a77560014e.html) ⭐️ 8.0/10

工业和信息化部组织制定并发布了强制性国家标准 GB 44721—2026《智能网联汽车 自动驾驶系统安全要求》，这是我国首部针对 L3、L4 级自动驾驶系统的强制性国标。该标准拟于 2027 年 7 月 1 日起实施，将 2024 年的推荐性国标升级为强制要求。 这是监管领域的重要里程碑：中国自动驾驶从自愿性指导转向强制性安全要求，将影响 L3/L4 车辆的整车厂、供应商和运营商。该标准为高级别自动驾驶在公开道路上的规模化落地提供了法律与技术基础，也为行业确立了安全底线。 该标准适用于搭载 L3、L4 级系统的 M 类（载客）和 N 类（载货）车辆，不适用于自动泊车系统。标准从企业全生命周期安全保障、系统动态驾驶能力、人机交互与用户告知、多维度检验检测四个维度构建安全要求体系；对 L3 级系统还要求具备驾驶人接管能力监测功能。

telegram · zaihuapd · 8月4日 13:06

**背景**: 该标准采用 SAE 驾驶自动化分级：L0-L2 为辅助驾驶，L3 为有条件自动驾驶，系统在特定条件下可完成驾驶操作，但驾驶员必须随时准备接管；L4 为高度自动驾驶，在限定运行设计域内可无需驾驶员介入。此前我国 2024 年发布的是推荐性国标，此次升级为强制性，表明政策层面支持 L3/L4 车辆商业化落地。工信部公告称，标准要求自动驾驶系统安全水平至少达到合格且专注驾驶人的水平。注意：M 类为载客车辆，N 类为载货车辆，标准不适用于自动泊车系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.autohome.com.cn/news/202608/1316205.html">autohome.com.cn/news/202608/1316205.html</a></li>
<li><a href="https://m.21jingji.com/article/20260804/herald/2ce85d00b1498fe646e9b8d576be5564.html">《智能网联汽车 自 动 驾 驶 系 统 安 全 要 求 》强制性国家标准正式发布 - 21...</a></li>
<li><a href="https://www.tmtpost.com/6496374.html">自 动 驾 驶 ，是忽悠吗？ -钛媒体官方网站</a></li>

</ul>
</details>

**标签**: `#autonomous-driving`, `#national-standard`, `#regulation`, `#smart-vehicles`, `#L3-L4`

---

<a id="item-11"></a>
## [白宫急转开源 AI 监管立场，硅谷分歧加剧](https://www.nytimes.com/2026/08/04/technology/ai-washington-regulation-whiplash.html) ⭐️ 8.0/10

白宫突然逆转了对开源 AI 模型的监管立场，在内部争论和硅谷的反对下放弃了制裁和贸易黑名单计划。2026 年 8 月 4 日，白宫邀请科技公司商议一个新框架，聚焦提升竞争力和发布前的网络安全审查。 这一政策逆转重塑了美国政府监管 AI 的方式，影响国家安全和美国 AI 企业的全球竞争力。它标志着英伟达（Nvidia）和 Meta 等开源 AI 倡导者取得了重大胜利，而 OpenAI 和 Anthropic 此前曾推动限制中国竞争对手。 导火索是中国开源模型 Kimi，其部分性能比肩 OpenAI 顶级模型。白宫幕僚长 Susie Wiles 和财长 Scott Bessent 曾考虑制裁措施，而英伟达 CEO 黄仁勋首次在 X 上发帖为开源辩护，并组建了有逾 230 家成员的安全联盟。

telegram · zaihuapd · 8月4日 15:22

**背景**: 开源 AI 指的是权重公开的模型，任何人都可以运行、修改并在此基础上构建，这使其成为一种战略性技术。Kimi 是中国公司月之暗面（Moonshot AI）开发的一系列大语言模型，以长上下文支持和有竞争力的性能著称。白宫的争论反映了全球范围内的更深层博弈：是出于国家安全限制中国开源模型，还是拥抱开放生态以加速创新。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_%28chatbot%29">Kimi (chatbot) - Wikipedia</a></li>
<li><a href="https://www.linkedin.com/pulse/open-source-ai-has-become-worlds-most-strategic-heres-luke-lovell-0bcte">Open source AI has become the world&#x27;s most strategic technology.</a></li>
<li><a href="https://huggingface.co/blog/daya-shankar/open-source-llms">Best Open - Source LLM Models in 2026: Coding, Local, Agentic AI ...</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#open source`, `#geopolitics`, `#policy`, `#Silicon Valley`

---