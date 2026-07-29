---
layout: default
title: "Horizon Summary: 2026-07-29 (ZH)"
date: 2026-07-29
lang: zh
---

> 从 41 条内容中筛选出 10 条重要资讯。

---

1. [AI 蠕虫通过微软 Word Copilot 自我传播](#item-1) ⭐️ 9.0/10
2. [月之暗面融资 350 亿美元，Kimi K3 模型突破带动估值飙升](#item-2) ⭐️ 9.0/10
3. [TurboFieldfare：开源引擎在 M 系列 Mac 上用 2GB 内存运行 Gemma 4 26B 模型](#item-3) ⭐️ 8.0/10
4. [Mitchell Hashimoto 宣布成立基于 libghostty 的新公司 Superlogical](#item-4) ⭐️ 8.0/10
5. [长政策文档无法可靠约束 AI 智能体](#item-5) ⭐️ 8.0/10
6. [马修·格林谈后量子密码学的历史性转变](#item-6) ⭐️ 8.0/10
7. [ncnn 的 Vulkan 后端实现边缘设备上厂商无关的 GPU 推理](#item-7) ⭐️ 8.0/10
8. [Claude 共享对话和 Artifacts 被谷歌索引，Anthropic 称设计如此](#item-8) ⭐️ 8.0/10
9. [Hugging Face 被大量用于深度伪造裸照](#item-9) ⭐️ 8.0/10
10. [中国电信停止第三方互联网渠道销售 SIM 卡](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [AI 蠕虫通过微软 Word Copilot 自我传播](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/) ⭐️ 9.0/10

研究人员 Håkon Måløy 展示了一种新的提示注入变体，可创建针对微软 Word Copilot 的自我复制 AI 蠕虫，使隐藏在文档中的恶意指令能够自主传播到其他文档。 这一发现揭示了广泛使用的 AI 助手中的关键安全漏洞，表明 AI 蠕虫可以利用代理对文档和电子邮件系统的访问权限自主传播，对企业数据安全和用户隐私构成重大风险。 该攻击将对抗性自我复制提示嵌入外部共享文档中；当 Copilot 处理文档时，它会遵循指令修改内容并将攻击传播到新文档，从而创建一个通过自然语言运行的计算机蠕虫。

hackernews · Canopy9560 · 7月29日 11:44 · [社区讨论](https://news.ycombinator.com/item?id=49096188)

**背景**: 提示注入是一种网络安全攻击手段，利用大型语言模型（LLM）无法可靠区分开发者定义的提示和用户输入的弱点，诱使其遵循隐藏在数据中的恶意指令。当 LLM 被集成到具有文件或电子邮件访问权限的应用程序中时，它们容易受到间接提示注入的攻击，即嵌入在检索内容中的对抗性文本可以命令模型执行意外操作。这项研究将这一概念扩展为通过文档生态系统自主传播的自我复制蠕虫。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://thehackernews.com/2026/06/researchers-build-self-replicating-ai.html">Researchers Build Self-Replicating AI Worm That Operates Entirely on Local, Open-Weight Models</a></li>
<li><a href="https://www.infosecurity-magazine.com/news/worm-created-generative-ai-systems/">Self-Propagating Worm Created to Target Generative AI Systems - Infosecurity Magazine</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为，区分指令与数据是 AI 安全中一个根本未解决的问题；一位用户提到他们已经卸载了 Copilot 并禁用了本地 AI。另一位指出，像白色文本这样的技术仍然有效，并担心在缓解措施出现之前，授予代理广泛的访问权限会使问题恶化。

**标签**: `#AI security`, `#prompt injection`, `#Copilot`, `#worms`, `#Microsoft Word`

---

<a id="item-2"></a>
## [月之暗面融资 350 亿美元，Kimi K3 模型突破带动估值飙升](https://www.bloomberg.com/news/articles/2026-07-29/china-s-moonshot-ai-passes-funding-goal-to-hit-35-billion-value) ⭐️ 9.0/10

月之暗面完成一轮 350 亿美元融资，投后估值达 3500 亿美元，远超最初 10 亿至 20 亿美元的目标，这得益于其突破性的 Kimi K3 模型，该模型性能接近前沿水平。公司已启动新一轮融资，pre-money 估值为 500 亿美元，并计划最早今年内在香港 IPO。 此次融资事件标志着中国 AI 能力的范式转变，Kimi K3 的性能接近美国前沿模型水平，引发科技股抛售，成为业界又一个“DeepSeek 时刻”。巨额估值和 IPO 计划凸显了投资者对中国 AI 公司的信心，可能加剧全球 AI 竞争。 Kimi K3 是一个开源模型，拥有 2.8 万亿参数，基于 Kimi Delta Attention 和 Attention Residuals 构建，支持百万 token 上下文窗口和原生视觉理解。公司 6 月年化经常性收入达 3 亿美元，K3 发布后日销售额增长至少 6 倍。

telegram · zaihuapd · 7月29日 10:12

**背景**: 月之暗面是一家中国人工智能公司，以其 Kimi 系列大语言模型闻名。“DeepSeek 时刻”指的是 2025 年初，另一家中国 AI 实验室 DeepSeek 发布 R1 模型时引发的行业震动，表明用不那么先进的芯片和较低成本也能实现前沿 AI，重塑了全球 AI 格局。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://www.siliconflow.com/models/kimi-k3">SiliconFlow – AI Infrastructure for LLMs &amp; Multimodal Models</a></li>
<li><a href="https://news.google.com/stories/CAAqNggKIjBDQklTSGpvSmMzUnZjbmt0TXpZd1NoRUtEd2lNMDRITkVSRUl2TF92dzd0MjFDZ0FQAQ?hl=en-IN&amp;gl=IN&amp;ceid=IN:en">Google News - Moonshot AI launches Kimi K 3 model - Overview</a></li>

</ul>
</details>

**标签**: `#AI`, `#Funding`, `#Moonshot AI`, `#Kimi K3`, `#Chinese AI`

---

<a id="item-3"></a>
## [TurboFieldfare：开源引擎在 M 系列 Mac 上用 2GB 内存运行 Gemma 4 26B 模型](https://github.com/drumih/turbo-fieldfare) ⭐️ 8.0/10

TurboFieldfare 是一个开源推理引擎，通过从 SSD 流式传输路由专家，在任何 M 系列 Mac 上仅用约 2 GB 内存即可运行 4-bit 量化的 Gemma 4 26B-A4B-IT 模型。它在 8 GB M2 MacBook Air 上达到每秒 5–6 个 token，在 M5 MacBook Pro 上达到每秒 31–35 个 token。 该引擎使得在内存受限的 Mac 上运行总参数量达 250 亿的大型混合专家模型成为可能，降低了设备端 AI 的门槛。它展示了一种从 SSD 流式传输模型权重的实用技术，可惠及其他 MoE 模型和边缘设备。 4-bit 量化后的模型权重约占 14 GB，但 TurboFieldfare 仅将共享层和 KV 缓存保留在 RAM（约 2 GB）中，通过使用有限并行 pread 和专家缓存，从 SSD 流式传输每个 token 所需的路由专家。它还包括一个实验性的兼容 OpenAI 的本地服务器，支持流式输出、工具调用和 KV 缓存前缀复用。

hackernews · gitpusher42 · 7月29日 15:05 · [社区讨论](https://news.ycombinator.com/item?id=49098510)

**背景**: Gemma 4 26B-A4B-IT 是 Google DeepMind 的混合专家（MoE）模型，总参数达 252 亿，但每个 token 仅激活 38 亿参数。在 MoE 模型中，每个输入仅激活部分专家层，因此非活跃专家可存储在片外并按需流式加载。TurboFieldfare 利用这一特性，将专家权重存储在 SSD 上，仅在需要时加载，而共享层和注意力缓存则保留在 RAM 中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/tonbistudio/moe-ssd-streaming-windows">GitHub - tonbistudio/ moe - ssd - streaming -windows: Running a 32 GB...</a></li>
<li><a href="https://andrew.ooo/posts/flash-moe-397b-model-macbook-local-inference/">Flash- MoE : Running a 397B Parameter Model on... — andrew.ooo</a></li>
<li><a href="https://openrouter.ai/google/gemma-4-26b-a4b-it:free">Gemma 4 26 B A 4 B (free) - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**社区讨论**: 社区对该技术成就表达了浓厚兴趣，称赞其创新性，并将其与 llama.cpp 的 mmap 方法进行比较。一些用户指出 llama.cpp 已经可以通过 mmap 在 2 GB 内存下运行 26B 模型，但 TurboFieldfare 将 SSD 读取与推理活动同步，可能提供更低的延迟。有人分享了在较旧 macOS 版本上编译的变通方法，一位正在构建 DiffusionGemma 的开发者表示有兴趣合作。

**标签**: `#inference engine`, `#Gemma`, `#on-device AI`, `#memory optimization`, `#Swift/Metal`

---

<a id="item-4"></a>
## [Mitchell Hashimoto 宣布成立基于 libghostty 的新公司 Superlogical](https://www.superlogical.com/) ⭐️ 8.0/10

Mitchell Hashimoto 宣布成立新公司 Superlogical，该公司将基于他最初为 Ghostty 终端模拟器开发的开源 libghostty 终端库构建商业产品。 此举验证了围绕开源库构建商业模式同时保持核心技术采用 MIT 许可的可行性，可能为可持续的开源开发树立先例。同时，这也表明可嵌入终端仿真在现代应用中的重要性日益增加。 Mitchell Hashimoto 已将 Ghostty 项目的所有权转让给一个非营利组织，确保该终端模拟器保持独立。Superlogical 将像其他外部使用者一样使用 libghostty，并将共享的终端改进上游到该项目。

hackernews · yan · 7月29日 15:41 · [社区讨论](https://news.ycombinator.com/item?id=49098965)

**背景**: Mitchell Hashimoto 是著名的软件工程师，以创建 HashiCorp 以及 Vagrant、Terraform 和 Consul 等工具而闻名。Ghostty 是他从头构建的一款快速、GPU 加速的终端模拟器，而 libghostty 是其以 MIT 许可发布的可嵌入终端库。该库允许任何应用程序集成现代终端模拟器，而无需从头编写。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mitchellh.com/writing/libghostty-is-coming">Libghostty Is Coming - Mitchell Hashimoto</a></li>
<li><a href="https://ghostty.org/">Ghostty</a></li>
<li><a href="https://docsmith.aigne.io/docs/ghostty/en/libghostty-ed730d">libghostty API - docsmith.aigne.io</a></li>

</ul>
</details>

**社区讨论**: 社区成员普遍赞扬了这一开源策略，指出将 Ghostty 转让给非营利组织可确保可持续性。有人将 libghostty 与过去的组件技术（如 OLE/COM）进行比较，少数人批评原始公告标题为标题党。总体情绪积极且富有洞察力。

**标签**: `#open source`, `#terminal`, `#company`, `#libghostty`, `#software engineering`

---

<a id="item-5"></a>
## [长政策文档无法可靠约束 AI 智能体](https://arxiv.org/abs/2607.25398) ⭐️ 8.0/10

一篇题为《Handbook.md》的新 arXiv 论文表明，由于上下文窗口限制和模型退化，冗长的政策文档无法可靠地约束 AI 智能体。 这一发现挑战了 AI 智能体能够忠实遵循详尽书面指南的假设，影响了安全合规自主系统的设计。 该论文强调，即使拥有 100 万 token 上下文窗口的模型，在处理长政策文档时也会出现性能下降和指令遗忘的问题。

hackernews · spIrr · 7月29日 13:01 · [社区讨论](https://news.ycombinator.com/item?id=49096969)

**背景**: 大语言模型（LLM）的上下文窗口有限，即它们一次能处理的文本量。随着上下文长度增加，模型常出现上下文退化，即输入早期部分被遗忘或处理不当。这对于需要一致遵循长政策文档的 AI 智能体来说尤其成问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.geeksforgeeks.org/artificial-intelligence/tokens-and-context-windows-in-llms/">Tokens and Context Windows in LLMs - GeeksforGeeks</a></li>
<li><a href="https://www.emergentmind.com/topics/context-degradation-in-llms">Context Degradation in LLMs</a></li>

</ul>
</details>

**社区讨论**: 评论者指出了实际中的类似问题，用户报告称 Claude 在短时间内会忽略 CLAUDE.md 中的指令，而显式的提示内提醒效果更好。有人认为，真正的智能体行为需要针对特定数据集进行大量后训练，而非仅依赖上下文。

**标签**: `#AI agents`, `#long context`, `#LLM limitations`, `#policy compliance`, `#benchmark`

---

<a id="item-6"></a>
## [马修·格林谈后量子密码学的历史性转变](https://simonwillison.net/2026/Jul/29/matthew-green/#atom-everything) ⭐️ 8.0/10

马修·格林指出，我们正处于从传统公钥算法向后量子算法转型的历史时期，并认为 AI 在此过程中可能提升密码分析能力。 这一评论恰逢其时，因为安全社区正在积极标准化像 HAWK 这样的后量子方案，AI 驱动的密码分析可能验证或削弱这些新算法，对未来密码学产生重大影响。 格林提到了 Impagliazzo 的 Minicrypt 概念（其中不存在公钥密码学），作为 AI 破解所有难题的可能场景；他还指出像 HAWK 这样的标准正在被考虑，这是一种基于格的后量子签名方案。

rss · Simon Willison · 7月29日 18:18

**背景**: 后量子密码学旨在开发能够抵抗量子计算机的密码算法。传统算法如 RSA 和 ECC 易受 Shor 算法攻击。NIST 正在标准化后量子方案，HAWK 是一种基于格的签名候选。Impagliazzo 的五世界理论对密码学可能性进行分类；Minicrypt 假设仅存在单向函数，而无公钥密码学。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://eprint.iacr.org/2026/1078">Post-Quantum HAWK Signature Acceleration with RISC-V-Based Hardware-Software Co-Design</a></li>
<li><a href="https://blog.computationalcomplexity.org/2004/06/impagliazzos-five-worlds.html">Computational Complexity: Impagliazzo&#x27;s Five Worlds</a></li>
<li><a href="https://blog.cloudflare.com/another-look-at-pq-signatures/">A look at the latest post-quantum signature standardization candidates | The Cloudflare Blog</a></li>

</ul>
</details>

**标签**: `#cryptography`, `#post-quantum`, `#AI`, `#cryptanalysis`, `#security`

---

<a id="item-7"></a>
## [ncnn 的 Vulkan 后端实现边缘设备上厂商无关的 GPU 推理](https://www.reddit.com/r/MachineLearning/comments/1v9s4mz/vendoragnostic_ml_inference_on_production_edge/) ⭐️ 8.0/10

PostSlate 团队利用 ncnn 的 Vulkan 后端，在生产边缘设备上实现了厂商无关的 GPU 加速机器学习推理，在人脸检测和嵌入模型上相比 ONNX CPU 推理获得了约 10 倍的加速。 这种方法消除了对 CUDA 等特定厂商运行时的依赖，使得单一的推理后端能够在所有 GPU 厂商（NVIDIA、AMD、Intel、Apple Silicon）上运行，这对跨平台边缘部署至关重要。 在 NVIDIA 4070 上的性能数据显示，ArcFace R50 人脸嵌入从 30 毫秒（ONNX CPU）降至 3 毫秒（ncnn Vulkan），SCRFD 人脸检测从 25 毫秒降至 2.5 毫秒，并且由于 fp16 权重存储，模型大小减半。

reddit · r/MachineLearning · /u/ppchaos · 7月29日 10:22

**背景**: ncnn 是由腾讯开发的高性能神经网络推理框架，针对移动和嵌入式部署进行了优化。Vulkan 是一个跨平台的图形和计算 API，提供跨厂商的低层级 GPU 访问。ONNX 是一种用于表示机器学习模型的开放格式，常用于框架间的互操作性。许多边缘设备缺乏 CUDA 支持，使得厂商无关的 GPU 推理具有挑战性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Tencent/ncnn">GitHub - Tencent/ ncnn : ncnn is a high-performance neural network...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vulkan">Vulkan - Wikipedia</a></li>
<li><a href="https://formats.jarhalab.com/formats/onnx">ONNX Model Format . onnx Format | File Formats</a></li>

</ul>
</details>

**标签**: `#ML Inference`, `#Vulkan`, `#Edge Computing`, `#ncnn`, `#Vendor-agnostic`

---

<a id="item-8"></a>
## [Claude 共享对话和 Artifacts 被谷歌索引，Anthropic 称设计如此](https://thenextweb.com/news/claude-shared-chats-artifacts-google-search-indexed) ⭐️ 8.0/10

上周末，Claude 用户创建的共享对话和 Artifacts 链接被谷歌索引，导致医疗记录、公司文件等敏感信息暴露。Anthropic 称系统未被入侵，共享链接由用户主动生成，设计上就是公开的。 这一事件凸显了 AI 聊天功能中用户共享内容可能被公开访问的持续隐私漏洞，削弱了用户信任。此前 Claude、ChatGPT 和 Grok 也曾出现类似问题，表明这是行业系统性问题。 Anthropic 已于周一下午阻止新的索引，但已索引的链接仍可访问。用户可在设置中撤销已共享链接，但已暴露的数据可能仍存在于搜索缓存中。

telegram · zaihuapd · 7月29日 02:40

**背景**: Claude 的共享对话功能允许用户创建可公开访问的对话或 Artifacts 链接，Artifacts 是 Claude 生成的可共享的独立内容，如交互式代码预览或应用。这些链接本质上用于分享，但默认非私有；若发布到公平台，搜索引擎可能抓取。Artifacts 是 Claude 的一项功能，可将想法转化为可共享的应用、工具或内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.claude.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them">What are artifacts and how do I use them? | Claude Help Center</a></li>
<li><a href="https://grokipedia.com/page/Claude_Artifacts">Claude Artifacts</a></li>

</ul>
</details>

**标签**: `#隐私安全`, `#Claude`, `#数据泄露`, `#谷歌索引`

---

<a id="item-9"></a>
## [Hugging Face 被大量用于深度伪造裸照](https://www.theverge.com/ai-artificial-intelligence/971723/hugging-face-nudify-deepfake-undress-women-children) ⭐️ 8.0/10

AI Forensics 的报告发现，Hugging Face 被广泛用于生成非自愿的深度伪造裸照，在一个蜜罐中收到的 1000 多条请求中，73% 涉及性内容，近 7% 针对儿童，而该平台缺乏有效的防护措施。 这突显了 AI 安全方面平台责任的严重缺失，一个领先的开源模型中心在几乎没有审核的情况下助长了有害内容的生成，伤害了受害者，并可能削弱对 AI 平台的信任。 研究人员设置了一个蜜罐，在七天内收到了超过 1000 条请求，Hugging Face 上排名前九的图像编辑模型中有七个可以通过简单提示轻易为女性“脱衣”，无需任何越狱技巧。

telegram · zaihuapd · 7月29日 08:20

**背景**: Hugging Face 是一个流行的机器学习模型和数据集共享平台。蜜罐是一种用于检测和分析恶意活动的诱饵系统。报告表明，Hugging Face 的内容政策并未得到有效执行，模型可被用于生成禁止的内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hugging_Face">Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/Honeypot_%28computing%29">Honeypot (computing)</a></li>

</ul>
</details>

**标签**: `#AI ethics`, `#deepfakes`, `#Hugging Face`, `#content moderation`, `#AI safety`

---

<a id="item-10"></a>
## [中国电信停止第三方互联网渠道销售 SIM 卡](https://www.189.cn/web/notice/detail?order=1&amp;amp;offerCode=519526800001&amp;amp;provinceCode=600304) ⭐️ 8.0/10

中国电信在其官方网站发布落款日期为 7 月 31 日的公告，称自 8 月 1 日起，第三方互联网渠道将不再提供电信号卡办理业务。 这一政策变化直接影响了消费者在线购买中国电信 SIM 卡的方式，将购买渠道限制在官方渠道，可能增加成本或降低便利性。 还发现了另一份日期为 7 月 29 日且 provinceCode 参数不同的公告。该禁令适用于所有第三方互联网平台，包括电商网站和在线转售商。

telegram · zaihuapd · 7月29日 12:45

**背景**: 中国电信是中国三大国有电信运营商之一，提供移动和宽带服务。第三方互联网渠道一直是客户在线购买 SIM 卡的常见方式，通常提供有竞争力的价格和促销活动。

**标签**: `#China Telecom`, `#telecom policy`, `#SIM card`, `#Internet channels`, `#China`

---