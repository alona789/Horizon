---
layout: default
title: "Horizon Summary: 2026-07-11 (EN)"
date: 2026-07-11
lang: en
---

> From 26 items, 7 important content pieces were selected

---

1. [vLLM v0.25.0: Model Runner V2 Default, PagedAttention Removed](#item-1) ⭐️ 9.0/10
2. [Humanoid Robot Performs World-First Surgery on Live Pigs](#item-2) ⭐️ 9.0/10
3. [6 U-Boot Bootloader Flaws Allow Code Execution Before OS Boot](#item-3) ⭐️ 9.0/10
4. [SGLang v0.5.15 Boosts GLM-5.2 NVFP4 and Speculative Decoding](#item-4) ⭐️ 8.0/10
5. [VultronRetriever models achieve #1 on MTEB with edge deployment](#item-5) ⭐️ 8.0/10
6. [Apple Sues OpenAI for Systematic Trade Secret Theft](#item-6) ⭐️ 8.0/10
7. [OpenAI releases GPT-5.6 series with Sol, Terra, Luna models](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0: Model Runner V2 Default, PagedAttention Removed](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 9.0/10

vLLM v0.25.0 makes Model Runner V2 the default execution path for all dense models and removes the legacy PagedAttention backend. It also achieves Transformers modeling backend parity with native vLLM performance, adding 558 commits from 232 contributors. This release marks a major architectural milestone for vLLM, simplifying its codebase and improving performance uniformity across backends. The removal of PagedAttention signals the full transition to the newer, more modular Model Runner V2, which benefits the broader LLM inference ecosystem by enabling more efficient scaling and easier integration. Model Runner V2 now supports EVS, realtime embeddings, prefix caching for Mamba hybrids, and dynamic speculative decoding with full CUDA graphs. The Transformers backend gained FP8 MoE support and migrations for GPTBigCode, Starcoder2, and RoBERTa.

github · khluu · Jul 11, 20:06

**Background**: vLLM is an open-source high-throughput LLM serving engine originally developed at UC Berkeley. PagedAttention, introduced in 2023, optimized KV cache memory management using paging techniques, but vLLM has been gradually replacing it with the more efficient Model Runner V2 architecture designed from first principles.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/PagedAttention">PagedAttention</a></li>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#llm inference`, `#release`, `#model runner`, `#transformers`

---

<a id="item-2"></a>
## [Humanoid Robot Performs World-First Surgery on Live Pigs](https://arstechnica.com/ai/2026/07/humanoid-robots-controlled-by-surgeons-did-world-first-operation-on-live-pigs/) ⭐️ 9.0/10

Surgeons at UC San Diego teleoperated a Unitree G1 humanoid robot to successfully perform two minimally invasive gallbladder removal surgeries on live pigs, marking the world's first use of a general-purpose humanoid robot for live surgery. The results were published in the journal Nature. This breakthrough demonstrates the potential for low-cost, general-purpose humanoid robots to make surgical care accessible in remote, rural, battlefield, or space settings, drastically reducing costs compared to dedicated surgical robots like the da Vinci system (which costs $500,000 to millions). The Unitree G1 robot costs as low as $13,500 for the basic model and about $67,000 with a dexterous hand, standing 1.5 meters tall and weighing 27 kilograms. The robot has 23 to 43 degrees of freedom and uses force control for precise manipulation.

telegram · zaihuapd · Jul 11, 02:29

**Background**: Humanoid robots are general-purpose machines designed to mimic human form and movement. Until now, robot-assisted surgery has relied on specialized systems like the da Vinci Surgical System, which are expensive and limited to specific procedures. The ability to use a versatile, low-cost humanoid robot for surgery could revolutionize access to surgical care. Teleoperation allows surgeons to control the robot remotely, enabling procedures in settings where specialists are not physically present.

<details><summary>References</summary>
<ul>
<li><a href="https://medicalxpress.com/news/2026-07-surgeons-teleoperated-humanoid-robots-surgery.html">Surgeons use teleoperated humanoid robots to perform live...</a></li>
<li><a href="https://www.popsci.com/technology/humanoid-robots-perform-surgery/">In groundbreaking first, humanoid robots performed surgery</a></li>
<li><a href="https://www.unitree.com/g1/">Humanoid robot G1_Humanoid Robot Functions ... - Unitree G1</a></li>

</ul>
</details>

**Tags**: `#robotics`, `#surgery`, `#humanoid robots`, `#medical technology`, `#AI`

---

<a id="item-3"></a>
## [6 U-Boot Bootloader Flaws Allow Code Execution Before OS Boot](https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/) ⭐️ 9.0/10

Binarly disclosed six vulnerabilities in U-Boot's FIT signature verification, two of which enable arbitrary code execution before the operating system boots. These vulnerabilities bypass secure boot mechanisms, allowing attackers to disable firmware security, modify boot flow, or install persistent malware, affecting devices using U-Boot since version 2013.07. The vulnerabilities are tracked as BRLY-2026-037 through BRLY-2026-042; two lead to code execution and four cause denial of service. Patches have been accepted by U-Boot maintainers but require integration by hardware vendors.

telegram · zaihuapd · Jul 11, 08:32

**Background**: U-Boot is a widely used open-source bootloader for embedded devices. FIT (Flattened Image Tree) is a format for bootable images that includes signature verification for secure boot. The vulnerabilities exist in the signature verification code, allowing attackers to bypass checks and load malicious code before the OS loads.

<details><summary>References</summary>
<ul>
<li><a href="https://cybersecuritynews.com/u-boot-fit-signature-verification/">Six U - Boot FIT Signature Verification Flaws Enable Code Execution...</a></li>
<li><a href="https://docs.u-boot-project.org/en/latest/usage/fit/signature.html">U - Boot FIT Signature Verification — Das U - Boot unknown version...</a></li>

</ul>
</details>

**Tags**: `#security`, `#u-boot`, `#bootloader`, `#vulnerabilities`, `#firmware`

---

<a id="item-4"></a>
## [SGLang v0.5.15 Boosts GLM-5.2 NVFP4 and Speculative Decoding](https://github.com/sgl-project/sglang/releases/tag/v0.5.15) ⭐️ 8.0/10

SGLang v0.5.15 introduces optimized production serving for GLM-5.2 NVFP4 on Blackwell, achieving 500+ tok/s/user on 8x B300 and 450 on 4x GB300. It also enables speculative decoding V2 by default, delivering +11% end-to-end TPS, and introduces IndexShare MTP which reduces draft-step cost by up to 1.9x. These optimizations significantly improve inference throughput and cost-efficiency for large language models, especially benefiting users of GLM-5.2 and other state-of-the-art models. The speculative decoding improvements and IndexShare technique make high-performance LLM serving more accessible and practical for production deployments. Speculative decoding V2 achieves zero-overhead scheduling via CUDA-graphable DSA draft-extend and fused metadata ops. IndexShare MTP reuses the indexer top-k across draft steps, reducing costs up to 1.9x on long contexts. Additionally, TopK V2 fuses top-k selection with page-table transform, supporting runtime k up to 2048.

github · Fridge003 · Jul 10, 22:58

**Background**: SGLang is an open-source inference framework for large language models that provides high performance and flexibility. Speculative decoding is a technique that uses a draft model to generate multiple tokens quickly, which are then verified by the target model to accelerate generation. NVFP4 is a 4-bit floating-point precision format from NVIDIA that reduces memory usage while maintaining accuracy, particularly effective on Blackwell GPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/nvidia-nvfp4-blackwell-how-glm-52-broke-300-ts-orion-nikola-vurdelja-8zb9f/">NVIDIA NVFP4 on Blackwell: How GLM-5.2 Broke 300 t/s at Orion - LinkedIn</a></li>
<li><a href="https://build.nvidia.com/z-ai/glm-5.2/modelcard">glm-5.2 Model by Z-ai | NVIDIA NIM</a></li>
<li><a href="https://alphasignal.ai/news/nvidia-shrinks-glm-5-2-memory-by-1-8x-with-nvfp4-without-losing-accuracy">NVIDIA Shrinks GLM-5.2 Memory by 1.8x With NVFP4 Without Losing ...</a></li>

</ul>
</details>

**Tags**: `#LLM inference`, `#performance optimization`, `#speculative decoding`, `#version release`

---

<a id="item-5"></a>
## [VultronRetriever models achieve #1 on MTEB with edge deployment](https://www.reddit.com/r/MachineLearning/comments/1utmxq8/vultronretriever_family_of_models_released_on/) ⭐️ 8.0/10

The VultronRetriever family of models, including Prime-8B, Core-4.5B, and Flash-0.8B, has been released on HuggingFace, achieving state-of-the-art retrieval performance on the MTEB leaderboard. The 8B model is the global #1, while the 0.8B model runs cool on edge devices and indexes up to 60 images per minute fully offline. This release demonstrates that high-performance retrieval models can be both top-ranked on standard benchmarks and optimized for efficient edge deployment, potentially enabling privacy-preserving, offline AI applications on consumer devices. The significant improvements in index storage and throughput over previous leaders could lower the barrier for deploying advanced retrieval in resource-constrained environments. The VultronRetrieverPrime-8B model has up to 16x smaller index storage footprint and 12x higher throughput versus previous 9B-class leaders. All models were trained on datasets with 0% cross-dataset duplication and 0% eval contamination, and show no overfitting on privately run MTEB evals.

reddit · r/MachineLearning · /u/madkimchi · Jul 11, 15:22

**Background**: The MTEB (Massive Text Embedding Benchmark) leaderboard ranks embedding models on a wide range of tasks including retrieval, classification, and clustering. Late interaction retrieval, used by models like ColBERT, decomposes queries and documents into multi-vector representations for finer-grained matching, often improving accuracy but requiring more memory. The VultronRetriever models employ the Hydra Architecture to enable late interaction retrieval with reduced memory footprint and efficient edge deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/spaces/mteb/leaderboard">MTEB Leaderboard - a Hugging Face Space by mteb</a></li>
<li><a href="https://weaviate.io/blog/late-interaction-overview">An Overview of Late Interaction Retrieval Models: ColBERT ...</a></li>

</ul>
</details>

**Tags**: `#Machine Learning`, `#NLP`, `#Embeddings`, `#MTEB`, `#Edge AI`

---

<a id="item-6"></a>
## [Apple Sues OpenAI for Systematic Trade Secret Theft](https://www.cnbc.com/2026/07/10/apple-openai-lawsuit-trade-secrets.html) ⭐️ 8.0/10

On July 10, 2026, Apple filed a lawsuit in the U.S. District Court for the Northern District of California against OpenAI, two former employees, and io Products, alleging systematic theft of trade secrets related to product design, manufacturing processes, and supply chain information. This lawsuit underscores escalating tensions between two tech giants over AI hardware competition, potentially impacting OpenAI's consumer hardware ambitions and setting a precedent for trade secret enforcement in the AI industry. Apple alleges that former employee Chang Liu accessed internal networks and downloaded dozens of hardware files after resignation, while OpenAI hardware head Tang Yew Tan sent supplier data to his personal email and required job candidates to bring Apple components to interviews.

telegram · zaihuapd · Jul 11, 03:14

**Background**: Trade secret lawsuits are common in Silicon Valley to protect proprietary technology. Apple has strict confidentiality policies, and OpenAI has been expanding into consumer hardware. The lawsuit claims over 400 former Apple employees now work at OpenAI.

**Tags**: `#Apple`, `#OpenAI`, `#法律诉讼`, `#商业机密`, `#AI硬件`

---

<a id="item-7"></a>
## [OpenAI releases GPT-5.6 series with Sol, Terra, Luna models](https://t.me/zaihuapd/42497) ⭐️ 8.0/10

OpenAI announced the GPT-5.6 series, featuring three models: Sol (flagship), Terra (balanced), and Luna (cost-efficient). The series introduces max/ultra reasoning modes, multi-agent collaboration, and Programmatic Tool Calling, with significant improvements in code, knowledge work, design, research, and cybersecurity. This release marks a major step in AI model efficiency and capability, offering tiered options that balance performance and cost. The new reasoning modes and multi-agent capabilities could enable more complex task automation and reduce token usage for enterprises and developers. The GPT-5.6 series ships as three models on July 9, 2026, according to Vellum. Sol is the strongest model with max reasoning for deeper thinking and ultra mode that spawns sub-agents to decompose complex work. Programmatic Tool Calling adds a code execution step to improve token savings and accuracy.

telegram · zaihuapd · Jul 11, 13:34

**Background**: GPT-5.6 is the latest iteration from OpenAI, released only two months after GPT-5.5. It introduces tiered models similar to how previous generations offered different capabilities. Max and ultra reasoning are new effort levels: Max gives the model more time for deep reasoning, while Ultra uses parallel sub-agents. Programmatic Tool Calling is a technique where the model writes and executes code to call tools, improving efficiency. These advancements aim to reduce the cost of complex AI tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.vellum.ai/blog/gpt-5-6-benchmarks-explained">GPT - 5 . 6 Sol vs Terra vs Luna : Which Tier Should You Actually Use?</a></li>
<li><a href="https://www.linkedin.com/posts/vaibhavs10_introducing-gpt-56-sol-terra-and-luna-activity-7476322117161058304-W_mZ">Introducing GPT - 5 . 6 : Sol , Terra and Luna . Sol is our strongest...</a></li>
<li><a href="https://www.u7buy.com/blog/gpt-5-6-reasoning-modes-explained/">GPT-5.6 Reasoning Modes Explained - Medium vs High vs Max vs Ultra</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#GPT-5.6`, `#AI models`, `#multi-agent`, `#tool calling`

---