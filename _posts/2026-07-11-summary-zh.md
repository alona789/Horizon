---
layout: default
title: "Horizon Summary: 2026-07-11 (ZH)"
date: 2026-07-11
lang: zh
---

> 从 26 条内容中筛选出 7 条重要资讯。

---

1. [vLLM v0.25.0：Model Runner V2 成为默认，PagedAttention 被移除](#item-1) ⭐️ 9.0/10
2. [人形机器人完成全球首例活体猪手术](#item-2) ⭐️ 9.0/10
3. [U-Boot 引导程序 6 漏洞可致启动前代码执行](#item-3) ⭐️ 9.0/10
4. [SGLang v0.5.15 提升 GLM-5.2 NVFP4 和推测解码性能](#item-4) ⭐️ 8.0/10
5. [VultronRetriever 模型在 MTEB 上排名第一并支持边缘部署](#item-5) ⭐️ 8.0/10
6. [苹果起诉 OpenAI 系统性窃取商业机密](#item-6) ⭐️ 8.0/10
7. [OpenAI 发布 GPT-5.6 系列：Sol、Terra、Luna](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0：Model Runner V2 成为默认，PagedAttention 被移除](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 9.0/10

vLLM v0.25.0 将 Model Runner V2 设为所有稠密模型的默认执行路径，并移除了传统的 PagedAttention 后端。同时，Transformers 建模后端性能达到与原生 vLLM 持平，本次发布包含来自 232 位贡献者的 558 次提交。 此版本标志着 vLLM 架构的重要里程碑，简化了代码库并提升了后端性能的一致性。PagedAttention 的移除标志着全面过渡到更新、更模块化的 Model Runner V2，这将通过实现更高效的扩展和更易集成，惠及更广泛的 LLM 推理生态系统。 Model Runner V2 现在支持 EVS、实时嵌入、Mamba 混合模型的前缀缓存，以及带完整 CUDA 图的动态推测解码。Transformers 后端获得了 FP8 MoE 支持，并完成了 GPTBigCode、Starcoder2 和 RoBERTa 的迁移。

github · khluu · 7月11日 20:06

**背景**: vLLM 是一个开源的高吞吐量 LLM 推理引擎，最初由加州大学伯克利分校开发。PagedAttention 于 2023 年提出，利用分页技术优化了 KV 缓存内存管理，但 vLLM 已逐渐将其替换为从头设计的更高效的 Model Runner V2 架构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/PagedAttention">PagedAttention</a></li>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm inference`, `#release`, `#model runner`, `#transformers`

---

<a id="item-2"></a>
## [人形机器人完成全球首例活体猪手术](https://arstechnica.com/ai/2026/07/humanoid-robots-controlled-by-surgeons-did-world-first-operation-on-live-pigs/) ⭐️ 9.0/10

加州大学圣地亚哥分校的外科医生远程操控宇树 G1 人形机器人，成功在活猪身上完成了两例微创胆囊切除手术，这是全球首次将通用人形机器人用于活体手术。研究结果已发表在《自然》期刊上。 这一突破表明，低成本、通用的人形机器人有望使外科手术服务普及到偏远地区、农村、战场甚至太空等场景，其成本远低于达芬奇等专用手术机器人（售价 50 万至数百万美元）。 宇树 G1 机器人基础款售价低至 13,500 美元，配备灵巧手后约 67,000 美元，高约 1.5 米，重约 27 公斤。该机器人拥有 23 至 43 个自由度，并通过力控实现精确操作。

telegram · zaihuapd · 7月11日 02:29

**背景**: 人形机器人是一种通用型机器，旨在模仿人类形态和运动。此前，机器人辅助手术依赖达芬奇手术系统等专用设备，这些设备价格昂贵且仅限于特定手术。使用通用、低成本的人形机器人进行手术可能彻底改变手术可及性。远程操作使外科医生能够远程控制机器人，从而在专家不在场的情况下进行手术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medicalxpress.com/news/2026-07-surgeons-teleoperated-humanoid-robots-surgery.html">Surgeons use teleoperated humanoid robots to perform live...</a></li>
<li><a href="https://www.popsci.com/technology/humanoid-robots-perform-surgery/">In groundbreaking first, humanoid robots performed surgery</a></li>
<li><a href="https://www.unitree.com/g1/">Humanoid robot G1_Humanoid Robot Functions ... - Unitree G1</a></li>

</ul>
</details>

**标签**: `#robotics`, `#surgery`, `#humanoid robots`, `#medical technology`, `#AI`

---

<a id="item-3"></a>
## [U-Boot 引导程序 6 漏洞可致启动前代码执行](https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/) ⭐️ 9.0/10

Binarly 披露了 U-Boot 引导程序 FIT 签名验证中的六个漏洞，其中两个可在操作系统启动前实现任意代码执行。 这些漏洞可绕过安全启动机制，使攻击者能够禁用固件安全功能、修改启动流程或植入持久性恶意软件，影响自 2013.07 版本以来使用 U-Boot 的设备。 这些漏洞编号为 BRLY-2026-037 至 BRLY-2026-042，其中两个导致代码执行，四个导致拒绝服务。补丁已被 U-Boot 维护者接受，但需要硬件厂商集成到固件更新中。

telegram · zaihuapd · 7月11日 08:32

**背景**: U-Boot 是一种广泛用于嵌入式设备的开源引导程序。FIT（扁平镜像树）是一种可启动镜像格式，包含用于安全启动的签名验证功能。这些漏洞存在于签名验证代码中，允许攻击者绕过检查并加载恶意代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybersecuritynews.com/u-boot-fit-signature-verification/">Six U - Boot FIT Signature Verification Flaws Enable Code Execution...</a></li>
<li><a href="https://docs.u-boot-project.org/en/latest/usage/fit/signature.html">U - Boot FIT Signature Verification — Das U - Boot unknown version...</a></li>

</ul>
</details>

**标签**: `#security`, `#u-boot`, `#bootloader`, `#vulnerabilities`, `#firmware`

---

<a id="item-4"></a>
## [SGLang v0.5.15 提升 GLM-5.2 NVFP4 和推测解码性能](https://github.com/sgl-project/sglang/releases/tag/v0.5.15) ⭐️ 8.0/10

SGLang v0.5.15 为 GLM-5.2 NVFP4 在 Blackwell 上推出优化生产服务，在 8x B300 上实现 500+ tok/s/user，在 4x GB300 上实现 450 tok/s/user。它还默认启用推测解码 V2，端到端 TPS 提升 11%，并引入 IndexShare MTP，将 draft-step 成本降低高达 1.9 倍。 这些优化显著提高了大语言模型的推理吞吐量和成本效率，尤其惠及 GLM-5.2 和其他先进模型的用户。推测解码改进和 IndexShare 技术使高性能 LLM 服务更易于部署，更具实用性。 推测解码 V2 通过可 CUDA 图的 DSA draft-extend 和融合元数据操作实现零开销调度。IndexShare MTP 在 draft 步骤之间重用索引器 top-k，在长上下文中将成本降低高达 1.9 倍。此外，TopK V2 将 top-k 选择与页表变换融合，支持高达 2048 的运行时 k 值。

github · Fridge003 · 7月10日 22:58

**背景**: SGLang 是一个开源的大语言模型推理框架，提供高性能和灵活性。推测解码是一种技术，通过草稿模型快速生成多个 token，然后由目标模型验证以加速生成。NVFP4 是 NVIDIA 的 4 位浮点精度格式，在保持准确性的同时减少内存使用，在 Blackwell GPU 上特别有效。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/nvidia-nvfp4-blackwell-how-glm-52-broke-300-ts-orion-nikola-vurdelja-8zb9f/">NVIDIA NVFP4 on Blackwell: How GLM-5.2 Broke 300 t/s at Orion - LinkedIn</a></li>
<li><a href="https://build.nvidia.com/z-ai/glm-5.2/modelcard">glm-5.2 Model by Z-ai | NVIDIA NIM</a></li>
<li><a href="https://alphasignal.ai/news/nvidia-shrinks-glm-5-2-memory-by-1-8x-with-nvfp4-without-losing-accuracy">NVIDIA Shrinks GLM-5.2 Memory by 1.8x With NVFP4 Without Losing ...</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#performance optimization`, `#speculative decoding`, `#version release`

---

<a id="item-5"></a>
## [VultronRetriever 模型在 MTEB 上排名第一并支持边缘部署](https://www.reddit.com/r/MachineLearning/comments/1utmxq8/vultronretriever_family_of_models_released_on/) ⭐️ 8.0/10

VultronRetriever 模型家族（包括 Prime-8B、Core-4.5B 和 Flash-0.8B）已在 HuggingFace 上发布，在 MTEB 排行榜上取得了最先进的检索性能。其中 8B 模型为全球第一，而 0.8B 模型可在边缘设备上低温运行，并能在完全离线状态下每分钟索引多达 60 张图像。 此次发布表明，高性能检索模型既能在标准基准测试中名列前茅，又能针对边缘高效部署进行优化，从而可能推动在消费设备上实现保护隐私的离线 AI 应用。相比之前的领先模型，索引存储和吞吐量的显著提升有望降低在资源受限环境中部署高级检索的门槛。 VultronRetrieverPrime-8B 相比之前的 9B 类领先模型，索引存储占用最多减少 16 倍，吞吐量提高 12 倍。所有模型均在零跨数据集重复和零评估污染的数据集上训练，并在私有 MTEB 评估中未出现过度拟合。

reddit · r/MachineLearning · /u/madkimchi · 7月11日 15:22

**背景**: MTEB（大规模文本嵌入基准）排行榜在包括检索、分类和聚类在内的广泛任务中对嵌入模型进行排名。后期交互检索（如 ColBERT 等模型使用）将查询和文档分解为多向量表示以实现更细粒度的匹配，这通常能提高准确性但需要更多内存。VultronRetriever 模型采用 Hydra 架构，以更小的内存占用实现后期交互检索，并支持高效的边缘部署。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/spaces/mteb/leaderboard">MTEB Leaderboard - a Hugging Face Space by mteb</a></li>
<li><a href="https://weaviate.io/blog/late-interaction-overview">An Overview of Late Interaction Retrieval Models: ColBERT ...</a></li>

</ul>
</details>

**标签**: `#Machine Learning`, `#NLP`, `#Embeddings`, `#MTEB`, `#Edge AI`

---

<a id="item-6"></a>
## [苹果起诉 OpenAI 系统性窃取商业机密](https://www.cnbc.com/2026/07/10/apple-openai-lawsuit-trade-secrets.html) ⭐️ 8.0/10

2026 年 7 月 10 日，苹果在美国加州北区联邦法院起诉 OpenAI、两名前员工及 io Products，指控其系统性窃取苹果的产品设计、制造工艺和供应链机密。 这场诉讼凸显了两大科技巨头在 AI 硬件竞争中的紧张关系升级，可能影响 OpenAI 的消费硬件野心，并为 AI 行业的商业机密执法树立先例。 苹果指控前员工刘畅（Chang Liu）离职后仍访问内部网络并下载数十份硬件文件，OpenAI 硬件负责人陈育陈（Tang Yew Tan）则在离职前将供应商数据发送至个人邮箱，并要求求职者携带苹果零部件参加面试。

telegram · zaihuapd · 7月11日 03:14

**背景**: 商业机密诉讼在硅谷保护专有技术中很常见。苹果有严格的保密政策，而 OpenAI 一直在拓展消费硬件领域。诉讼称目前有超过 400 名前苹果员工在 OpenAI 工作。

**标签**: `#Apple`, `#OpenAI`, `#法律诉讼`, `#商业机密`, `#AI硬件`

---

<a id="item-7"></a>
## [OpenAI 发布 GPT-5.6 系列：Sol、Terra、Luna](https://t.me/zaihuapd/42497) ⭐️ 8.0/10

OpenAI 发布了 GPT-5.6 系列，包含三个模型：Sol（旗舰）、Terra（平衡性能与成本）和 Luna（面向高并发低成本）。该系列引入了 max/ultra 推理模式、多智能体协作和 Programmatic Tool Calling，在代码、知识工作、设计、科研和网络安全方面有显著提升。 此次发布标志着 AI 模型在效率和能力上的重大进步，通过分级选项平衡性能与成本。新的推理模式和多智能体能力可支持更复杂的任务自动化，降低企业和开发者的 token 消耗。 根据 Vellum 的信息，GPT-5.6 系列于 2026 年 7 月 9 日发布，包含三个模型。Sol 是最强的模型，支持 max 推理以进行更深入的思考，以及 ultra 模式，可生成子智能体分解复杂工作。Programmatic Tool Calling 增加了代码执行步骤，以提升 token 节省和准确性。

telegram · zaihuapd · 7月11日 13:34

**背景**: GPT-5.6 是 OpenAI 的最新迭代版本，距 GPT-5.5 发布仅两个月。它引入了分级模型，类似于前几代提供不同能力。Max 和 Ultra 推理是新的努力级别：Max 让模型有更多时间进行深度推理，Ultra 则使用并行子智能体。Programmatic Tool Calling 是一种让模型编写并执行代码来调用工具的技术，提高了效率。这些进步旨在降低复杂 AI 任务的成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.vellum.ai/blog/gpt-5-6-benchmarks-explained">GPT - 5 . 6 Sol vs Terra vs Luna : Which Tier Should You Actually Use?</a></li>
<li><a href="https://www.linkedin.com/posts/vaibhavs10_introducing-gpt-56-sol-terra-and-luna-activity-7476322117161058304-W_mZ">Introducing GPT - 5 . 6 : Sol , Terra and Luna . Sol is our strongest...</a></li>
<li><a href="https://www.u7buy.com/blog/gpt-5-6-reasoning-modes-explained/">GPT-5.6 Reasoning Modes Explained - Medium vs High vs Max vs Ultra</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-5.6`, `#AI models`, `#multi-agent`, `#tool calling`

---