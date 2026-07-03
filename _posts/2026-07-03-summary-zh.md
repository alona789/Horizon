---
layout: default
title: "Horizon Summary: 2026-07-03 (ZH)"
date: 2026-07-03
lang: zh
---

> 从 43 条内容中筛选出 11 条重要资讯。

---

1. [Anthropic 指控阿里巴巴对 Claude 发动大规模蒸馏攻击](#item-1) ⭐️ 9.0/10
2. [Karpathy 创建 nanochat 分支，打造 100 美元的 ChatGPT](#item-2) ⭐️ 8.0/10
3. [Wordgard：ProseMirror 创作者推出的新富文本编辑器](#item-3) ⭐️ 8.0/10
4. [Valve 开源 Steam Machine 电子墨水屏，支持 DIY 改装](#item-4) ⭐️ 8.0/10
5. [产品失败的原因：创始人动机与专业差距](#item-5) ⭐️ 8.0/10
6. [CDD 从 logits 中恢复微调数据，无需权重访问](#item-6) ⭐️ 8.0/10
7. [谷歌 Gemini Omni Flash 登顶 Video Arena 盲测榜](#item-7) ⭐️ 8.0/10
8. [中国拟规定半年不登录账号可注销](#item-8) ⭐️ 8.0/10
9. [华为 Mate 80 Pro 游戏能效超越骁龙 8 Gen3](#item-9) ⭐️ 8.0/10
10. [NASA 发射私人救援卫星拯救雨燕望远镜](#item-10) ⭐️ 8.0/10
11. [腾讯阿图因 AI 在 CyberGym 测试中超越 Mythos，成本仅 0.1%](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 指控阿里巴巴对 Claude 发动大规模蒸馏攻击](https://t.me/zaihuapd/42327) ⭐️ 9.0/10

Anthropic 致信美国参议院银行委员会，指控阿里巴巴在 2026 年 4 月 22 日至 6 月 5 日期间，通过近 2.5 万个欺诈账户与 Claude 进行了超过 2880 万次交互，利用蒸馏攻击窃取其模型能力。 这是已知最大规模的蒸馏攻击，凸显了 AI 模型知识产权的严重安全风险，可能加剧中美 AI 公司之间的紧张关系。 攻击涉及阿里巴巴及其 Qwen 实验室；蒸馏攻击是利用较弱模型未经许可学习较强模型输出的技术，Anthropic 声称这是针对该公司的最大规模此类攻击。

telegram · zaihuapd · 7月3日 06:21

**背景**: 模型蒸馏是一种通过从较大模型输出中学习来创建更小、更高效模型的技术。未经许可使用则构成知识产权盗窃。Anthropic 已发布检测此类攻击的方法，这些攻击通常涉及大量重复查询。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks?ref=cognitiverevolution.ai">Detecting and preventing distillation attacks \ Anthropic</a></li>
<li><a href="https://medium.com/a-microbiome-scientist-at-large/distillation-attack-a1df588f1f6f">Stealing the AI 's Brain: A Deep Dive into Distillation Attacks and AI ...</a></li>

</ul>
</details>

**标签**: `#AI security`, `#model theft`, `#distillation attack`, `#Anthropic`, `#Alibaba`

---

<a id="item-2"></a>
## [Karpathy 创建 nanochat 分支，打造 100 美元的 ChatGPT](https://github.com/karpathy/nanochat) ⭐️ 8.0/10

Andrej Karpathy 创建了一个新的 nanochat 仓库分支，宣称能提供 100 美元可买到的最佳类 ChatGPT 体验。 这一进展可能大幅降低获取高质量对话式 AI 的成本门槛，让个人和小型企业更容易使用。它代表着向大语言模型技术民主化迈出的一步。 该分支处于早期阶段，目标是在严格 100 美元预算下实现最佳性能。具体技术规格和模型细节尚未公布。

github · karpathy · 7月3日 17:47

**背景**: Nanochat 是 Andrej Karpathy 的一个项目，旨在创建高效、计算最优的语言模型。Karpathy 是知名的 AI 研究员，曾在 OpenAI 和 Tesla 工作，他的项目经常探索缩放定律和成本效益的 AI。该分支特别针对超低成本但功能强大的 ChatGPT 替代品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/karpathy/nanochat">NanoChat - The best ChatGPT that $100 can buy - GitHub</a></li>

</ul>
</details>

**标签**: `#AI`, `#ChatGPT`, `#open-source`, `#language models`, `#cost-effective`

---

<a id="item-3"></a>
## [Wordgard：ProseMirror 创作者推出的新富文本编辑器](https://wordgard.net/) ⭐️ 8.0/10

ProseMirror 的创作者 Marijn Haverbeke 发布了 Wordgard，这是一个新的浏览器内富文本编辑器，与 ProseMirror 共享许多概念，但是一个独立产品，没有直接的升级路径。 Wordgard 为开发富文本编辑体验的开发者提供了一个新的选择，通过更精良的设计和方式，可能对生态系统产生影响，相比 ProseMirror 的低级工具包更具优势。 Wordgard 需要当前使用 ProseMirror 的团队进行大量的迁移工作，因为它不向后兼容。该编辑器具有简洁的设计，并采用现代 Web 开发实践构建。

hackernews · indy · 7月3日 08:50 · [社区讨论](https://news.ycombinator.com/item?id=48772573)

**背景**: ProseMirror 是一个流行的开源富文本编辑器框架，提供语义化的编辑体验，并被用作 Tiptap 等许多编辑器的基础。由同一作者创建的 Wordgard 旨在解决 ProseMirror 的一些复杂性，同时保留其核心概念。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://prosemirror.net/">ProseMirror</a></li>
<li><a href="https://github.com/prosemirror">ProseMirror · GitHub</a></li>

</ul>
</details>

**社区讨论**: 评论对 Wordgard 背后的动机表示兴趣，指出从 ProseMirror 没有升级路径。一些用户赞赏其设计质量，而另一些用户则强调从 ProseMirror 文档中以编程方式提取数据的挑战，暗示 Wordgard 可能解决这些问题。

**标签**: `#rich-text-editor`, `#prosemirror`, `#wysiwyg`, `#web-development`

---

<a id="item-4"></a>
## [Valve 开源 Steam Machine 电子墨水屏，支持 DIY 改装](https://www.gamingonlinux.com/2026/07/valve-open-source-the-steam-machine-e-ink-screen-so-you-can-make-your-own/) ⭐️ 8.0/10

Valve 已公开 Steam Machine 上使用的电子墨水屏的设计文件和规格，将其开源，供任何人复制或自定义修改。 此举让社区能够制作定制前面板、维修或重新利用这些屏幕，促进了更开放的硬件生态系统，并延长了设备的使用寿命。 该屏幕被确认为标准的 Adafruit 5.83 英寸电子墨水面板（产品编号 6397），这意味着 DIY 项目可以直接使用市售元件。

hackernews · ahlCVA · 7月3日 13:01 · [社区讨论](https://news.ycombinator.com/item?id=48774518)

**背景**: 电子墨水屏模仿纸张上的墨水外观，仅在图像变化时耗电，非常适合低功耗静态信息显示。Steam Machine 是 Valve 推出的客厅游戏 PC，运行 SteamOS，其前面板配备了一块电子墨水屏，用于显示 logo 或系统信息。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jiclcd.com/what-is-e-ink-display-technology/">What Is E - Ink Display Technology ? Complete Guide to E-Paper...</a></li>
<li><a href="https://sesamedisk.com/valves-steam-machine-2026-launch-analysis/">Valve ’s Steam Machine Launches Today: The $1,049... - Sesame Disk</a></li>

</ul>
</details>

**社区讨论**: 社区成员赞赏 Valve 的开放态度，指出该屏幕是标准的 Adafruit 面板，易于复制。一些人表达了将其适配到 Framework Desktop 等其他形态的兴趣，另一些人则讨论了这种开源硬件举措的潜在商业优势。

**标签**: `#open-source`, `#hardware`, `#valve`, `#e-ink`, `#steam-machine`

---

<a id="item-5"></a>
## [产品失败的原因：创始人动机与专业差距](https://weli.dev/blog/half-baked-product/) ⭐️ 8.0/10

一篇题为《半成品》的博客文章分析了产品失败的常见原因，强调创始人动机与领域专业知识之间的不匹配，以及工程、销售和领导角色之间的脱节。 这一分析为初创公司和产品团队提供了常青的经验教训，强调除了市场分析之外，领域专业知识和跨职能协调对成功至关重要。 该文章以一个虚构的烤箱初创公司为中心例子，说明仅由财富动机驱动、缺乏领域专业知识的创始人如何导致产品无法满足真实客户需求。

hackernews · weli · 7月3日 08:23 · [社区讨论](https://news.ycombinator.com/item?id=48772388)

**背景**: 在创业界，许多产品因缺乏创始人与市场的契合而失败，创始人追逐趋势却对行业缺乏深刻理解。这篇文章通过一个案例研究的视角剖析了此类失败。

**社区讨论**: 评论者大多同意这一分析，指出创始人动机不匹配的重复模式。一些人幽默地将故事联系起来，而另一些人则呼吁更多视角，例如销售人员的观点，以充分理解失败的动态。

**标签**: `#startup`, `#product development`, `#founder`, `#market fit`, `#lessons`

---

<a id="item-6"></a>
## [CDD 从 logits 中恢复微调数据，无需权重访问](https://www.reddit.com/r/MachineLearning/comments/1umn2dk/contrastive_decoding_diffing_cdd_recovering/) ⭐️ 8.0/10

对比解码差异分析（CDD）是一种新颖的模型差异分析方法，仅通过 logit 访问即可从语言模型中恢复逐字微调数据，无需权重、激活或探测语料库。在 SDF 基准测试中，它在四个模型系列（1B 到 32B 参数）的 20 个模型对中的 19 个上实现了 4/5 或更高的逐字恢复得分。 该方法极大降低了提取私有微调数据的门槛，引发了对大语言模型部署中隐私和安全的关键担忧。它优于需要完全权重访问的白盒激活差异透镜（ADL）方法，后者在同一基准测试中从未超过 3/5 的得分。 单一默认配置即可在所有测试模型上工作，无需逐模型校准或层选择。一个意外发现是，名称'Dr. Elena Rodriguez'出现在多个微调领域中，因为 Claude Sonnet 3.6 在生成合成数据时偏好使用该名称。

reddit · r/MachineLearning · /u/CebulkaZapiekana · 7月3日 19:01

**背景**: 模型差异分析旨在识别和解释基础模型与微调版本之间的差异。对比解码（CD）是一种通过对比大模型和小模型的 logits 来提升文本质量的解码方法。激活差异透镜（ADL）利用激活差异引导生成，但需要完全权重访问，且只能恢复模糊的领域级描述，而非逐字数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2210.15097">Contrastive Decoding: Open-ended Text Generation as Optimization</a></li>
<li><a href="https://www.lesswrong.com/w/model-diffing">Model Diffing — LessWrong</a></li>
<li><a href="https://arxiv.org/html/2510.13900">Narrow Finetuning Leaves Clearly Readable Traces in Activation ...</a></li>

</ul>
</details>

**标签**: `#model diffing`, `#finetuning data extraction`, `#logit access`, `#LLM security`, `#contrastive decoding`

---

<a id="item-7"></a>
## [谷歌 Gemini Omni Flash 登顶 Video Arena 盲测榜](https://x.com/Designarena/status/2072759122366509130) ⭐️ 8.0/10

谷歌 DeepMind 的视频生成模型 Gemini Omni Flash 在 Video Arena 盲测排行榜上以 1404 分登顶，领先字节跳动的 Seedance 2.0 Mini 达 101 分。 这一里程碑显示了谷歌在 AI 视频生成领域重新夺回领导地位，打破了字节跳动的先前统治。它标志着视频生成领域竞争加剧，并凸显了用户偏好基准的重要性。 Video Arena 基准依赖于盲测用户投票来对模型进行排名。Gemini Omni Flash 是一个原生多模态视频模型，能够根据文本提示生成高分辨率、符合物理规律的视频，并通过对话进行编辑。

telegram · zaihuapd · 7月3日 05:51

**背景**: AI 视频生成模型发展迅速，谷歌、字节跳动等公司竞争激烈。Video Arena 是一个社区驱动的基准测试，用户在不了解模型身份的情况下比较不同模型的输出。谷歌之前的 Veo 系列排名较低，而 Gemini Omni Flash 现已提升了七个名次。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/models/model-cards/gemini-omni-flash/">Gemini Omni Flash - Model Card — Google DeepMind</a></li>
<li><a href="https://www.madebyagents.com/benchmarks/video-arena">Video Arena Benchmark : Scores, Methodology, and Top AI Models</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-omni/">Introducing Gemini Omni</a></li>

</ul>
</details>

**标签**: `#AI video generation`, `#Google DeepMind`, `#benchmark`, `#Gemini Omni Flash`, `#Video Arena`

---

<a id="item-8"></a>
## [中国拟规定半年不登录账号可注销](https://mp.weixin.qq.com/s/TfYZaC8ULPvu9JeTqYGkKg) ⭐️ 8.0/10

国家互联网信息办公室于 2025 年 7 月 3 日发布修订草案，提议平台可注销超过半年未登录的账号，要求 AI 生成内容进行标识，禁止强制使用智能服务及操纵热搜等行为。 该法规将显著影响中国的用户数据权利和平台责任，涉及数十亿用户和所有主要互联网公司。它加强了对 AI 生成内容和网络操纵行为的管控，与国际互联网治理趋势接轨。 草案要求大型平台在 24 小时内处理违法内容投诉，并规定用户更换手机号后应能解绑原账号。草案还明确禁止刷量、控评、制造虚假热点等行为。

telegram · zaihuapd · 7月3日 11:29

**背景**: 中国一直在加强互联网监管，包括 2025 年 9 月生效的 AI 内容标识法规，要求对生成内容进行显性和隐性标识。'刷量'和'控评'等行为通过操纵网站流量和社交媒体评论来误导用户，草案旨在遏制这些行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aiornot.com/blog/china-ai-content-detection-and-labeling-rules">China Unveils Strict AI Content Detection & Labeling Rules</a></li>
<li><a href="https://similarweb-ga.com/">Buy Similarweb Traffic and Ranking- Similarweb traffic Robt</a></li>

</ul>
</details>

**标签**: `#regulations`, `#internet governance`, `#China`, `#user data`, `#AI ethics`

---

<a id="item-9"></a>
## [华为 Mate 80 Pro 游戏能效超越骁龙 8 Gen3](https://www.bilibili.com/video/BV1F7T46wEyT) ⭐️ 8.0/10

极客湾对华为 Mate 80 Pro 系列的评测显示，得益于原生鸿蒙优化，麒麟 9030 芯片在游戏能效上超越骁龙 8 Gen3，尽管其理论性能较低。 这标志着华为芯片回归的重要里程碑，展示了软硬协同优化可以弥补性能差距，重塑移动旗舰市场的竞争格局。 麒麟 9030 Pro 采用 9 核 14 线程 CPU 和 6 核马良 935 GPU，晶体管规模约 150 亿。测试中，Mate 80 Pro Max 运行《原神》60 帧仅需 4.9W 功耗，《王者荣耀》120 帧仅 3W，优于骁龙 8 Gen3 设备。

telegram · zaihuapd · 7月3日 13:27

**背景**: 华为面临美国制裁，限制其获取先进芯片制造技术，因此依赖国内代工厂并自主研发麒麟芯片。公司还从安卓迁移至鸿蒙 OS，这是一个专为跨设备无缝集成设计的定制操作系统。“软硬芯云协同优化”是指华为调整整个技术栈——从应用到硬件再到云服务——以最大化性能和效率的方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.notebookcheck.net/HiSilicon-Maleoon-935-Benchmarks-and-Specs.1249609.0.html">Specifications and benchmarks of the HiSilicon Maleoon 935 GPU .</a></li>
<li><a href="https://gadgets.beebom.com/news/huawei-kirin-9030-geekbench-scores-leaked">Huawei Kirin 9030 Geekbench Listing Reveals CPU and GPU Details</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#Kirin`, `#chipset`, `#mobile`, `#gaming`

---

<a id="item-10"></a>
## [NASA 发射私人救援卫星拯救雨燕望远镜](https://apnews.com/article/swift-nasa-satellite-rescue-katalyst-a7ddd740ca099587c58865f583c7245a) ⭐️ 8.0/10

2026 年 7 月 3 日，NASA 利用诺斯罗普·格鲁曼公司的飞马座 XL 火箭发射了 LINK 航天器，准备与老旧的雨燕空间望远镜对接，由于太阳活动加剧，该望远镜轨道正在衰减，最快可能于 2026 年 10 月坠入地球大气层。 此次任务是私人航天器首次尝试捕获并提升美国政府卫星的轨道，展示了在轨服务的新能力，有助于减少太空碎片并延长宝贵资产的使用寿命。 LINK 将使用机械臂抓住雨燕，然后通过推进器将其轨道抬升约 240 公里。如果成功，雨燕最快可在 2026 年 9 月恢复科学观测。

telegram · zaihuapd · 7月3日 15:43

**背景**: 尼尔·格雷尔斯雨燕天文台于 2004 年发射，用于研究伽马射线暴及其他宇宙现象。二十多年来，其轨道因大气阻力而逐渐衰减，尤其在太阳活动极大期期间。若不干预，它将在 2026 年底前不受控地再入大气层。此次任务是商业卫星服务日益增长趋势的一部分，诺斯罗普·格鲁曼等公司是代表。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Swift_rescue_mission">Swift rescue mission - Wikipedia</a></li>
<li><a href="https://www.space.com/space-exploration/launches-spacecraft/nasa-to-launch-ambitious-mission-to-save-a-space-telescope-from-burning-up-in-earths-atmosphere">NASA launches rescue mission to save Swift space telescope from burning up in Earth's atmosphere | Space</a></li>
<li><a href="https://www.cnn.com/2026/07/03/science/nasa-swift-boost-rescue-mission">A daring rescue mission launches to save a falling NASA observatory | CNN</a></li>

</ul>
</details>

**标签**: `#NASA`, `#space telescope`, `#satellite rescue`, `#orbital debris`, `#private spaceflight`

---

<a id="item-11"></a>
## [腾讯阿图因 AI 在 CyberGym 测试中超越 Mythos，成本仅 0.1%](https://mp.weixin.qq.com/s/BzU7g-2iG7d6h4ViwMhxyg) ⭐️ 8.0/10

腾讯玄武实验室的阿图因 AI 在赛博健身房网络安全基准测试中取得 84.0%的得分，超越 Anthropic 的 Claude Mythos Preview，而预算不到 Mythos 的 0.1%。阿图因还在 curl、OpenSSL、Python cryptography 等项目中发现了多个 Mythos 未检出的高危逻辑漏洞。 这表明开源模型在漏洞发现等专业任务上能以极低成本媲美专有模型，可能推动 AI 驱动的安全测试的民主化。同时也凸显了 AI 代理在真实网络安全中的有效性不断提升。 阿图因基于开源模型 GLM-5.1 构建，该模型可自主连续工作长达 8 小时。在伯克利 BVI 真实世界漏洞榜单中，阿图因的严重漏洞严重程度排名第 1，总数排名第 5。

telegram · zaihuapd · 7月3日 16:12

**背景**: CyberGym 是加州大学伯克利分校推出的基准测试，评估 AI 代理在端到端网络安全任务（如漏洞检测、PoC 生成、修复）上的表现。GLM-5.1 是 Z.AI 的旗舰模型，专为长周期代理任务设计。伯克利漏洞指数（BVI）按严重程度对真实世界漏洞进行排名。这一新闻突显了 AI 在安全测试领域的快速进步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://llm-stats.com/benchmarks/cybergym">CyberGym Benchmark Leaderboard | LLM Stats</a></li>
<li><a href="https://docs.z.ai/guides/llm/glm-5.1">GLM - 5 . 1 - Overview - Z.AI DEVELOPER DOCUMENT</a></li>

</ul>
</details>

**标签**: `#AI`, `#cybersecurity`, `#vulnerability detection`, `#Tencent`, `#GLM-5.1`

---