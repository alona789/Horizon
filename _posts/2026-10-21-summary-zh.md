---
layout: default
title: "Horizon Summary: 2026-10-21 (ZH)"
date: 2026-10-21
lang: zh
---

> 从 36 条内容中筛选出 7 条重要资讯。

---

1. [eMudhra 中间 CA 私钥泄露，全球信任库被迫紧急更新](#item-1) ⭐️ 9.0/10
2. [DeepSeek-ai 开源 DeepInfer：面向自家模型的高吞吐推理框架](#item-2) ⭐️ 8.0/10
3. [Mistral 发布 Voxtral 3 语音模型与实时语音智能体 SDK](#item-3) ⭐️ 8.0/10
4. [谷歌开源 TorchTPU：面向 TPU 的原生 PyTorch 后端](#item-4) ⭐️ 8.0/10
5. [tsrs：TypeScript 的 Rust 移植版提速 8 倍，动因竟是为在 WASM 沙箱中运行](#item-5) ⭐️ 8.0/10
6. [Google Cloud 伦敦区域供电故障导致欧洲多家银行服务中断](#item-6) ⭐️ 8.0/10
7. [作者借助 exitmap 促成 333 个恶意 Tor 出口节点被移除](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [eMudhra 中间 CA 私钥泄露，全球信任库被迫紧急更新](https://simonwillison.net/2026/Oct/20/emudhra-certificates/) ⭐️ 9.0/10

八张 eMudhra 中间 CA 证书的私钥已被泄露，这些中间证书可链回 Mozilla、Microsoft、Apple 和 Chrome 根计划所信任的根证书。由于所有自带受信证书列表的软件都必须发布新的证书包，uv 0.13.4、pip 26.2.2、certifi 2026.10.19 以及各 Linux 发行版的 ca-certificates 包均已发布更新。 一张能链回主流根存储的中间 CA 可以为几乎所有域名签发被全球浏览器和 TLS 客户端接受的证书，因此此次泄露动摇了几乎整个互联网的 HTTPS 信任基础。对那些自带 CA 证书包的软件而言后果尤其棘手，因为仅修补系统信任库并不能覆盖这些内嵌副本，它们仍将处于脆弱状态。 当务之急是把这八张中间证书从各个信任库中移除，we-have-a-problem.com 网站正通过其 GitHub 仓库跟踪下游修复进展，Linux 发行版也被要求更新 ca-certificates 包。在 Python 生态中，修复通过 certifi 传导：该包提供 Mozilla 维护的 CA 证书包，被 requests 等众多库使用，而 uv 和 pip 又各自内置了它。

rss · Simon Willison · 10月20日 23:50

**背景**: 公钥基础设施依赖一条信任链：根 CA 证书被放在操作系统或浏览器的信任库中，它签发中间 CA 证书，中间 CA 再签发网站出示的终端实体证书。由于根的私钥离线保存，日常签发由中间 CA 完成，因此中间 CA 的私钥是高价值目标——持有者可以签发看起来完全合法的证书。信任库就是一个应用认为可信的根证书与中间证书的集合；如果证书能链回库中某一项，TLS 连接就继续，否则被拒绝。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Intermediate_certificate_%28cryptography%29">Intermediate certificate (cryptography)</a></li>
<li><a href="https://www.ssl.com/article/what-is-a-root-store/">What is a Root Store? - SSL.com</a></li>
<li><a href="https://pypi.org/project/certifi/">Python package for providing Mozilla&#x27;s CA Bundle .</a></li>

</ul>
</details>

**社区讨论**: 有报道称这些被泄露的私钥弱得离谱——据称只有单个字节，其中一把私钥字面上就是“4”——评论者对此既震惊又嘲讽，认为用“泄露”一词都算轻描淡写。一位 Mozilla 贡献者指出影响分布极不均衡：受 OneCRL 类吊销机制覆盖的浏览器可在数小时内完成修复且无需用户更新，而生态中其余部分缺乏同等的吊销投入。还有人指出许多项目毫无理由地自带 CA 证书包，导致全面修补进展缓慢、系统将长期处于易受攻击状态；另有评论引用 Mozilla bug 报告中的 eMudhra 解释，称问题出在当天用于生成 ECC 签发者的 KGC 脚本缺陷上。

**标签**: `#security`, `#TLS certificates`, `#PKI`, `#supply chain`, `#open source`

---

<a id="item-2"></a>
## [DeepSeek-ai 开源 DeepInfer：面向自家模型的高吞吐推理框架](https://github.com/deepseek-ai/DeepInfer) ⭐️ 8.0/10

DeepSeek-ai 在 GitHub 上发布了 DeepInfer，这是一个面向自家 DeepSeek 系列模型的高性能推理（服务）框架，并且是开源的。该仓库迅速在 Hacker News 上获得 2100 多分和 800 多条评论，成为本周讨论度最高的 AI 基础设施项目之一。 多数实验室只公开模型权重而把服务栈保留为专有资产，因此开源真正支撑前沿 API 的推理引擎，会显著降低小型团队和自建部署者低成本运行 DeepSeek 级模型的门槛。这也会加剧与商业推理服务商和 GPU 厂商的竞争，因为一个经过优化的开源服务层会直接影响每服务一个 token 所需的硬件量。 社区与二手报道提到了自定义算子（kernel）、针对 DeepSeek 大规模混合专家（MoE）模型的专家并行处理（涉及数百个专家），以及每 GPU 每秒数万 token 量级的吞吐数字，还有对非 NVIDIA 加速器支持的兴趣。读者应把其中的性能与成本数字视为厂商和社区的自述，尚未经过独立复现；同时需注意该项目与哈佛医学院一个同名的医学影像工具包并无关系。

hackernews · ggcr · 10月20日 09:08 · [社区讨论](https://news.ycombinator.com/item?id=50163277)

**背景**: DeepSeek 是一家中国 AI 实验室，以在开放权重（open-weight）许可下发布 DeepSeek-V4、DeepSeek-R1 等前沿大模型而闻名——这意味着训练好的参数可以被下载并在本地运行，而不必只通过 API 调用。要高效运行这类模型，就需要推理框架，也就是负责请求批处理、GPU 显存管理、以及在多设备间切分网络层或专家模块的服务引擎，而现实中的大部分成本和工程难度往往正集中在这一层。DeepInfer 就是 DeepSeek 自己版本的这一引擎，此前主要用于内部支撑其 API。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek_%28AI%29">DeepSeek (AI) - Wikipedia</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://www.youtube.com/watch?v=rJjQNdnBC8I">DeepSeek Open-Sourced Their Engine — 90K tok/s/GPU ( DeepInfer ...)</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论远超工程范畴：有人争论所公布的吞吐量和单卡收益经济性，有人讨论公开完整服务栈是否会冲击美国前沿实验室的商业模式，还有人推测此次发布与美方政策动作在时间上的关联。另一些人强调支持华为昇腾（Ascend）NPU 等非 NVIDIA 硬件的战略价值，认为开放且可移植的技术栈可能松动 NVIDIA 的主导地位——不过讨论中若干关于政策与性能的说法属于猜测，并未经过验证。

**标签**: `#LLM inference`, `#DeepSeek`, `#open-weight models`, `#model serving`, `#AI infrastructure`

---

<a id="item-3"></a>
## [Mistral 发布 Voxtral 3 语音模型与实时语音智能体 SDK](https://mistral.ai/news/voxtral-3/) ⭐️ 8.0/10

Mistral AI 发布了 Voxtral 3，这是一套全新的语音转文本与文本转语音模型系列，并配套提供支持 50 多种语言、可进行实时多轮对话的语音智能体 SDK。官方价格表显示，Voxtral Mini Transcribe 3 的转写价格为每分钟 0.0035 美元，Voxtral Speech 3 的语音合成价格为每 100 万字符 13 美元。 此次发布让 Mistral 从单一的转写模型供应商升级为覆盖“听、思考、调用工具、说”全链路的实时语音智能体方案，直接与既有语音 API 厂商以及大型模型公司的语音产品展开竞争。由于该服务提供欧盟托管或自部署选项，它对受数据驻留与合规要求约束的欧洲企业尤具吸引力。 按照 Mistral 的说法，该 SDK 将聆听、推理、工具调用与语音输出整合在一起，使智能体能够在电话或网页的实时对话中检索信息并与业务系统交互。值得注意的是，Voxtral 3 似乎是闭源的托管服务，这与此前开放权重的 Voxtral 模型形成对比；其宣称的延迟表现与语言覆盖范围仍需独立基准测试来验证。

hackernews · ilreb · 10月20日 16:02 · [社区讨论](https://news.ycombinator.com/item?id=50168396)

**背景**: 自动语音识别（ASR）将口语转换为书面文本，是实时字幕、会议记录和语音助手的基础技术。实时语音智能体则把 ASR、大语言模型、文本转语音合成以及外部工具调用串成一个低延迟闭环，由于每个环节都会叠加延时，其难度远高于离线批量转写。Mistral 于 2025 年 7 月凭借 Voxtral 首次进入该领域，发布了包括 Voxtral Mini 4B Realtime 在内的开放权重模型，其体量小到可在消费级硬件上离线运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mistral.ai/news/voxtral-3/">Voxtral 3: Voice Agent SDK &amp; Speech Models in 50+ Languages</a></li>
<li><a href="https://fourweekmba.com/ai-mistrals-voxtral-3-transcribes-speech-from-0-0035-a-minute/">Mistral’s Voxtral 3 Transcribes Speech From $0.0035 a Minute</a></li>
<li><a href="https://mistral.ai/news/voxtral/">Voxtral | Mistral AI</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者普遍持怀疑态度：有人称发布演示“非常不真实”，因为在法国根本不可能这么快预约到皮肤科医生；也有人表示 Microsoft Teams 和 8x8 生成的会议转写质量太差，几乎无法交给大模型使用，希望这些厂商提供插件把音频流转发给更好的模型。正面反馈方面，一位开发者称已将其离线版 Voxtral Mini 4B Realtime 推理商业化，在配备 4GB 显存的 Ryzen 5 5600U 核显笔记本上运行速度超过实时；同时也有人遗憾 Voxtral 3 采用闭源形式、无法用于本地部署，并对把语音智能体直接接入企业内网的安全风险表示担忧。

**标签**: `#speech-to-text`, `#voice-agents`, `#Mistral AI`, `#ASR`, `#model release`

---

<a id="item-4"></a>
## [谷歌开源 TorchTPU：面向 TPU 的原生 PyTorch 后端](https://github.com/google-pytorch/torch_tpu) ⭐️ 8.0/10

谷歌在 google-pytorch 的 GitHub 组织下开源了 TorchTPU 项目，提供一个原生 PyTorch 后端，使 PyTorch 模型可以直接运行在谷歌 TPU 加速器上。这标志着 TPU 支持从过去外挂式、惰性张量风格的集成方式，转向由谷歌自己维护的第一方支持。 PyTorch 是大多数机器学习从业者的主流框架，因此原生 TPU 支持消除了一个长期存在的摩擦点——过去这往往迫使团队要么选择 GPU，要么把代码重写成 JAX。在 AWS 等厂商纷纷搭建类似“框架到芯片”桥梁的当下，这也能让谷歌在加速器市场中更具竞争力，因为使用 TPU 不再需要放弃已有的 PyTorch 代码库。 该后端依赖 XLA 编译器将 PyTorch 计算图下沉到 TPU 硬件上执行，而这套编译基础设施本身已经支持 PyTorch、TensorFlow 和 JAX 模型。社区成员指出，硬件相关的差异正越来越多地集中在 kernel 层，还有评论者表示，借助一个实验性的开源 libtpu 实现，TorchTPU 的大部分功能已经可以运行在 Tenstorrent 加速器上。

hackernews · ilreb · 10月20日 16:40 · [社区讨论](https://news.ycombinator.com/item?id=50169053)

**背景**: TPU 是谷歌为机器学习定制的专用芯片（ASIC），多年来在 TPU 上运行 PyTorch 的主要途径是 PyTorch/XLA，它把 PyTorch 算子追踪成 XLA 计算图再编译到芯片上执行。XLA（Accelerated Linear Algebra）是一个开源的机器学习编译器，现由 OpenXLA 项目管理，可以接收来自 PyTorch、TensorFlow 和 JAX 的模型并针对 GPU、CPU 及其他加速器进行优化。JAX 是谷歌推出的、类 NumPy 风格的数组计算库，支持自动微分与 JIT 编译，向来是与 TPU 最契合的框架，这也正是原生 PyTorch 通路值得关注的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/openxla/xla">GitHub - openxla/ xla : A machine learning compiler for GPUs, CPUs...</a></li>
<li><a href="https://openxla.org/xla">OpenXLA Project</a></li>
<li><a href="https://docs.jax.dev/en/latest/">JAX: High performance array computing — JAX documentation</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论整体积极，有人称这是“amazing news”，因为过去为了让 PyTorch 跑在 TPU 上不得不“和 XLA 较劲”。不少人认为这强化了 XLA 作为编译基础设施的地位，从而让所有硬件都受益，还有人认为这是“给 TensorFlow 棺材钉上的最后一颗钉子”；另一些人则提到 AWS 面向 Trainium 的 torch-neuronx 以及实验性的 Tenstorrent libtpu 移植等类似努力。也有评论者认为，既然硬件细节都集中在 kernel 层，JAX 与 PyTorch 之争如今更多只是风格偏好问题。

**标签**: `#PyTorch`, `#TPU`, `#XLA`, `#Machine Learning`, `#Open Source`

---

<a id="item-5"></a>
## [tsrs：TypeScript 的 Rust 移植版提速 8 倍，动因竟是为在 WASM 沙箱中运行](https://blog.cloudflare.com/typescript-rust-port/) ⭐️ 8.0/10

Cloudflare 发布博客介绍 tsrs——一个由 oxc-project 主导的开源项目，将 TypeScript 7 的类型检查器移植到 Rust；早期基准测试显示，在相同类型检查工作线程数量下，它比 TypeScript 7.0 快最多 8 倍，内存占用减少约 70%。该项目还采用了一种特殊的内存模型——永不释放的 arena（区域分配）来模拟垃圾回收器，从而绕开了把 TypeScript 这类依赖 GC 的语言移植到 Rust 时通常必须做的数据结构重构。 一个可用的 Rust 版 TypeScript 编译器意味着，在大型代码库上开发者有望获得大幅加速的类型检查，而 tsc 在本地编辑-测试循环中往往慢得令人难受。这也给在纯 WASM 沙箱中运行完整 TypeScript 编译器提供了一条可行路径，无需附带整个 Go 运行时，这对只允许 WebAssembly 执行的边缘计算与 Serverless 平台意义重大。 这些亮眼数字来自与 TypeScript 7.0 在相同类型检查工作线程数下的对比，且项目定位是对 TypeScript 的忠实移植而非重写实现。arena 方案的做法是把长生命周期对象放进永不释放的内存区域，以此伪造 GC 语义——评论者认为这一思路巧妙，但其内存安全性与内存持续增长的行为值得进一步审视。值得注意的是，博客还提到前沿 AI 模型如今几乎能独立地在数天内完成大规模移植，作者称自己“一行代码都没写”。

hackernews · hnisjafx40 · 10月20日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=50165953)

**背景**: TypeScript 编译器（tsc）本身用 TypeScript 编写，运行在 JavaScript 引擎上，因此其对象由垃圾回收器自动管理内存。Rust 没有垃圾回收器，直接移植就必须重新组织数据的归属与生命周期——这正是 TypeScript 团队当初为其原生性能编译器重写选择不使用 Rust 的主要原因之一。arena 分配器通过把对象批量放在大块内存区域中、再一次性释放（在 tsrs 中长生命周期对象甚至完全不释放）来绕开这一难题，以放弃细粒度回收换取速度和简单的生命周期。与此同时，WebAssembly 是一种为在沙箱虚拟机中运行而设计的可移植二进制格式，而这正是促成此次移植的约束条件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/typescript-rust-port/">Introducing tsrs : a Port of TypeScript to Rust | Cloudflare Blog</a></li>
<li><a href="https://news.ycombinator.com/item?id=49923536">tsrs : Rust port of the TypeScript 7 type checker | Hacker News</a></li>
<li><a href="https://www.javacodegeeks.com/2026/09/rethinking-memory-arena-allocation-vs-garbage-collection-in-modern-systems.html">Rethinking Memory: Arena Allocation vs. Garbage Collection in ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论质量相当高：TypeScript 团队成员 DanRosenwasser 亲自参与，表示团队一直在研究 tsrs 的优化手段，并怀疑其中很大一部分加速来自这些优化而非单纯的语言选择，相关经验也将用于 TS 7.1。评论者指出“永不释放的 arena”内存模型是让 Rust 移植变得可行的关键技巧；有人点明真正的动机是得到一个能在纯 WASM 沙箱中运行、无需完整 Go 运行时的编译器，提速只是顺带的副产品。也有人欢迎大型代码库上的性能提升，但对这次移植据称几乎由前沿 AI 模型在无手写代码的情况下完成表示担忧。

**标签**: `#typescript`, `#rust`, `#compilers`, `#performance`, `#wasm`

---

<a id="item-6"></a>
## [Google Cloud 伦敦区域供电故障导致欧洲多家银行服务中断](https://www.neowin.net/news/google-cloud-outage-takes-down-hsbc-revolut-bank-of-scotland-llyods-equifax-more/) ⭐️ 8.0/10

Google Cloud 位于伦敦区域的 europe-west2-b 可用区发生供电事件，自 2026 年 10 月 19 日（周一）23:08（太平洋夏令时）起引发持续数小时的中断，导致 HSBC、Revolut、Lloyds、苏格兰银行、Equifax 等多家机构在欧洲的服务下线或性能下降。谷歌表示供电事件本身已得到缓解，基础设施服务预计在约 30 分钟内部分恢复，其余服务随后跟上。 这起事故是云集中度风险的真实案例：单一云厂商单个可用区的故障，迅速波及多个国家数百万用户的零售银行、银行卡支付和征信服务。它也为欧洲长期存在的数字主权争论添了一把火，推动欧洲建设可与美国超大规模云厂商相抗衡的替代方案。 故障局限于 europe-west2 三个可用区中的 -b 区，但谷歌警告该区域的其他服务可能出现错误率升高和间歇性网络问题。可用区隔离只对真正做了多可用区或多区域冗余架构的客户有效；有用户反映，作为纯线上运营的数字银行，在事故期间甚至没有可拨打的电话客服。

hackernews · paweladamczuk · 10月20日 10:26 · [社区讨论](https://news.ycombinator.com/item?id=50163961)

**背景**: Google Cloud 将基础设施划分为多个区域（例如伦敦的 europe-west2），每个区域内又划分出相互隔离的可用区，理论上单个可用区故障不会影响其他可用区。银行和金融科技公司越来越多地把应用跑在这类超大规模云上，而不是自建数据中心，这提高了效率，但也意味着云厂商一侧的事故可能同时打击多家机构。监管机构和分析师已将这种“云集中度风险”列为新兴的系统性隐患，而欧盟政策制定者也在讨论究竟应有多少基础设施由本地建设和掌控。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://status.cloud.google.com/incidents/Xs2XTHzAVC9YnafnPyzj">Incident details | Google Cloud Service Health</a></li>
<li><a href="https://www.theregister.com/paas-and-iaas/2026/10/20/google-clouds-london-zones-takes-a-nap-multiple-services-disrupted/5304084">Google Cloud &#x27;s London zones takes a nap, multiple services disrupted</a></li>
<li><a href="https://www.gartner.com/en/newsroom/press-releases/2023-10-30-gartner-says-cloud-concentration-now-a-significant-emerging-risk-for-many-organizations">Gartner Says Cloud Concentration Now a Significant Emerging ...</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了一手受影响经历：一位 Revolut 用户称整个上午无法登录主账户、无法取现、也无法刷卡；但也有人质疑影响被夸大，指出大量“服务中断”的证据来自 Downdetector，而该平台反映的是用户报告而非经过核实的服务状态。另一个反复出现的主题是对依赖美国超大规模云厂商的不满，有评论者主张欧盟应优先建设体现欧洲价值观的 AWS、Google Cloud 替代方案。

**标签**: `#cloud-infrastructure`, `#outage-postmortem`, `#google-cloud`, `#site-reliability`, `#fintech`

---

<a id="item-7"></a>
## [作者借助 exitmap 促成 333 个恶意 Tor 出口节点被移除](https://kaba.cx/posts/20261020_Tor/) ⭐️ 8.0/10

在 kaba.cx 发布的一篇第一手记述中，作者描述了 10 月 2 日发生的一起事件：333 个 Tor 出口中继（约占全部出口的 10%）开始把 22 端口的流量重定向到 12 台拦截服务器，这些服务器运行基于 paramiko 的 SSH 中间人攻击，窃取密码并试图在目标机器上植入 Ebury 恶意软件。作者利用 exitmap 扫描工具识别出这些恶意中继，并成功让 300 多个节点从 Tor 网络中被移除。 一场协同行动控制了 Tor 约十分之一的出口能力，本可以在无人察觉的情况下窃取任何依赖该网络进行匿名 SSH 访问的用户的凭据，因此这次清剿对 Tor 用户以及出口中继模式的公信力都意义重大。这也说明，像 exitmap 这样由志愿者维护的扫描基础设施，仍是抵御大规模恶意中继的一种有效且低成本的防御手段。 此次攻击的薄弱点在于 SSH 主机密钥校验：拦截服务器提供的是不同的主机密钥，导致 SSH 客户端打印出醒目的中间人攻击警告横幅，而这种指纹不匹配为管理员提供了一条追踪每个被感染节点的直接途径。作者指出，基于密码的登录面临风险，而基于密钥的认证基本不受影响；此外攻击者还试图植入 Ebury——一个与 Windigo 组织相关、自 2009 年起活跃的 OpenSSH 后门兼凭据窃取程序。

hackernews · kabakabakaba · 10月20日 13:39 · [社区讨论](https://news.ycombinator.com/item?id=50166257)

**背景**: Tor 通过志愿者运营的中继转发流量，而最后一跳——出口节点——在流量离开匿名网络时能够看到明文内容，这也是出口节点成为实施拦截攻击天然场所的原因。exitmap 是 Philipp Winter 开发的模块化 Python 扫描器，它借助 Stem 库把测试连接分别经由单个出口中继发出，从而让研究者发现 TLS 剥离、凭据窃取等篡改行为，Tor 项目本身也用它来发现行为不端的出口节点。Ebury 是一个长期存在的 Linux 恶意软件家族，通过修改共享库在 OpenSSH 中留下后门；据 ESET 估计，自 2009 年以来它已入侵约 40 万台服务器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/NullHypothesis/exitmap">GitHub - NullHypothesis/exitmap: A fast and modular scanner ... How Tor Identifies and Removes Bad Exit Nodes - tor Exitmap - A Fast and Modular Scanner for TOR Exit Relays Tor Exit Nodes: Risks, Monitoring, and Defensive Use How Tor Ensures Exit Node Integrity - tor - salivity.github.io How to Get Tor Exit Node IP Address Over Control Port ...</a></li>
<li><a href="https://attack.mitre.org/software/S0377/">Ebury, Software S0377 | MITRE ATT&amp;CK®</a></li>
<li><a href="https://nhimg.org/glossary/ssh-man-in-the-middle-ssh-mitm-attack/">What Is SSH Man-in-the-Middle (SSH MITM) Attack? Definition</a></li>

</ul>
</details>

**社区讨论**: 评论者大多对该事件印象深刻，但对攻击者的手法持批评态度：jandrese 认为选择 SSH 作为攻击向量考虑不周，因为中间人警告横幅立刻暴露了行动，如果坚持用电子邮件方式本可以持续更久；另一位评论者指出，基于密钥的认证削弱了密码窃取的危害。exitmap 的原作者 phw 现身表示，这个工具是他十多年前开发的，很高兴它依然有用；jszymborski 则指出，对于只有约 3000 个出口节点的网络而言，约 300 个节点已是极大比例。

**标签**: `#Tor`, `#network-security`, `#malware`, `#man-in-the-middle`, `#exitmap`

---