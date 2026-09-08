---
layout: default
title: "Horizon Summary: 2026-09-08 (EN)"
date: 2026-09-08
lang: en
---

> From 32 items, 6 important content pieces were selected

---

1. [Google&\#x27;s InferenceX TPU Externalization Challenges NVIDIA CUDA Moat](#item-1) ⭐️ 8.0/10
2. [A 417k-Parameter Recurrent System Generates Bad Apple Autonomously](#item-2) ⭐️ 8.0/10
3. [LLM-Guided Program Evolution Improves 10 Circle-Packing Solutions](#item-3) ⭐️ 8.0/10
4. [31,352 Repeated Benchmarks Reveal LLM Performance Drift](#item-4) ⭐️ 8.0/10
5. [Huawei Debuts Kirin 9050 Pro With Logic-Folding Tech After Six-Year Gap](#item-5) ⭐️ 8.0/10
6. [China&\#x27;s Supreme Court Clarifies AI Liability in Judicial Interpretation](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google&\#x27;s InferenceX TPU Externalization Challenges NVIDIA CUDA Moat](https://newsletter.semianalysis.com/p/tpu-inferencex-full-steam) ⭐️ 8.0/10

According to a new SemiAnalysis report, Google is rapidly externalizing its TPU inference stack through an initiative called InferenceX, claiming up to 50% better performance per dollar than competing solutions. The report says the effort is attracting a growing customer base and encompasses both current Ironwood and next-generation TPUv8i hardware. If the reported performance-per-dollar advantage holds, it strengthens Google Cloud&\#x27;s position in AI inference and directly chips away at NVIDIA&\#x27;s CUDA software moat. A growing external TPU customer base could disrupt the AI accelerator market, forcing NVIDIA to respond with either more competitive pricing or a more open software ecosystem. The analysis specifically cites Ironwood, Google&\#x27;s seventh-generation inference-focused TPU announced in 2025, and TPUv8i \(codenamed &\#x27;Zebrafish&\#x27;\), a cost-efficient inference accelerator expected to be generally available by the end of 2026. The up-to-50% figure is reported without a specified baseline in the available summary, so the exact comparison set \(e.g., versus NVIDIA H100, B200, or other TPUs\) remains unclear.

rss · Semianalysis · Sep 7, 20:00

**Background**: AI inference—running a trained model to generate predictions—has become a critical workload for cloud providers like Google. Google designs custom Tensor Processing Units \(TPUs\) for AI workloads and has long used them internally, but is now increasingly making them available to external customers through Google Cloud and other channels. NVIDIA&\#x27;s CUDA software ecosystem has historically been the default for AI development, so Google&\#x27;s push to externalize a competitive TPU stack with a strong performance-per-dollar story is part of a broader strategy to erode NVIDIA&\#x27;s dominance.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/infrastructure-and-cloud/google-cloud/ironwood-google-tpu-things-to-know/">3 things to know about Ironwood, Google&#x27;s latest TPU</a></li>
<li><a href="https://www.servethehome.com/googles-tpuv8s-for-training-and-inference-at-hot-chips-2026/">Google&#x27;s TPUv 8 s for Training and Inference at Hot... - ServeTheHome</a></li>
<li><a href="https://www.nextplatform.com/2025/09/17/google-shows-off-its-inference-scale-and-prowess/">Google Shows Off Its Inference Scale And Prowess</a></li>

</ul>
</details>

**Tags**: `#TPU`, `#AI inference`, `#Google Cloud`, `#CUDA`, `#AI accelerators`

---

<a id="item-2"></a>
## [A 417k-Parameter Recurrent System Generates Bad Apple Autonomously](https://www.reddit.com/r/MachineLearning/comments/1wa8rub/generating_bad_apple_autonomously_from_a_single/) ⭐️ 8.0/10

The author trained a tiny recurrent dynamical system with 417,129 parameters that autonomously generates the entire ~6,500-frame Bad Apple video from a single initial latent state \(h\_0, c\_0\), without any per-frame timestamp inputs. Code, weights, and analysis tools are shared on GitHub. This work demonstrates that a compact recurrent network can learn continuous temporal dynamics and extrapolate far beyond its training horizon, eliminating the need for explicit time conditioning in implicit neural representations. It is technically interesting for video generation, dynamical systems research, and INR-based modeling. The inference model uses a 4-gate LSTM-style recurrent transition \(CTF\) with 16,640 parameters plus a 400,361-parameter frame decoder, running at over 200 FPS on an RTX 4080. Training relied on learned latent teacher tables, a rollout horizon curriculum doubling up to K=512, state perturbation noise, second-difference acceleration regularization, and AdamW/Muon optimization; despite being trained only on 512-frame horizons, the model can unroll the full ~6,573-step sequence.

reddit · r/MachineLearning · /u/SEBADA321 · Sep 8, 00:05

**Background**: Implicit neural representations \(INRs\), also known as neural fields, are neural networks that map continuous coordinates such as time and spatial position to signal values, enabling compact encoding of images, video, and 3D scenes. SIREN is an INR architecture that uses sinusoidal activation functions; a previous project memorized Bad Apple as a coordinate function \(t, y, x\) to pixel. This new work builds on that idea by replacing explicit timestamp input with a recurrent dynamical system that evolves its own latent state over time.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Implicit_neural_representation">Implicit neural representation</a></li>
<li><a href="https://deepwiki.com/vsitzmann/siren/2-siren-architecture">SIREN Architecture | vsitzmann/siren | DeepWiki</a></li>
<li><a href="https://www.emergentmind.com/topics/siren-architecture">SIREN: Sinusoidal Representation Networks</a></li>

</ul>
</details>

**Tags**: `#Recurrent Neural Networks`, `#Video Generation`, `#Implicit Neural Representations`, `#Machine Learning`

---

<a id="item-3"></a>
## [LLM-Guided Program Evolution Improves 10 Circle-Packing Solutions](https://www.reddit.com/r/MachineLearning/comments/1w9xlyi/llmguided_program_evolution_improves_10_bestknown/) ⭐️ 8.0/10

Using LLM-guided program evolution, the author iteratively refined an optimization algorithm from a simple seed solver, improving the best-known sum-of-radii for 10 values of N from 101 to 114 on the Packomania csqv benchmark by 2.4% to 5.4% in 15 iterations. The total LLM cost was $27.72, and Packomania independently accepted the results. This demonstrates that LLM-guided program evolution can improve well-established, best-known optimization benchmark results with independent validation at a very low cost. It highlights a promising and economical path toward automated algorithm discovery that could be applied to other hard optimization problems. The approach uses a scoreboard of results and a history of prior attempts to guide the LLM&\#x27;s proposals, and each candidate is scored by an independent verifier so improvements are kept while failures are discarded. The system is called Discovery Loop; code, solutions, and a paper are publicly available, and the author specifically invites critique on the plateau-detection stopping rule.

reddit · r/MachineLearning · /u/SIGH\_I\_CALL · Sep 7, 16:54

**Background**: Circle packing is a classic geometry and optimization problem about arranging circles inside a container without overlap; the csqv variant on Packomania asks for the maximum total radius of N variable-size circles in a unit square. LLM-guided program evolution is a technique in which a large language model proposes code-level mutations to an algorithm in an evolutionary loop, guided by measured performance, rather than solving the target problem directly. Packomania is a well-known public repository that tracks best-known packing results, so improvements independently accepted there carry additional credibility.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2609.05093v1">LLM-Guided Program Evolution for Circle Packing:Breaking 10 ...</a></li>
<li><a href="https://arxiv.org/abs/2403.11446">[2403.11446] LLM Guided Evolution -- The Automation of Models ... LLM Guided Evolution - The Automation of Models Advancing ... GitHub - clint-kristopher-morris/llm-guided-evolution: LLM ... LLM Guided Evolution - The Automation of Models Advancing Models LLM Guided Evolution - The Automation of Models Advancing Models llm-guided-evolution/README.md at main · clint-kristopher ...</a></li>
<li><a href="https://packomania.com/">Packomania (52C17)</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#program evolution`, `#optimization`, `#circle packing`, `#AI for science`

---

<a id="item-4"></a>
## [31,352 Repeated Benchmarks Reveal LLM Performance Drift](https://www.reddit.com/r/MachineLearning/comments/1w9llr4/measuring_llm_performance_drift_observations_and/) ⭐️ 8.0/10

The AI Stupid Level team published a longitudinal benchmarking methodology that uses 31,352 repeated score measurements across 49 models to detect LLM performance drift, treating evaluation as a time-series measurement rather than static leaderboard snapshots. Static leaderboard scores misrepresent API-served models because behavior behind the same name can change day-to-day due to infrastructure, configuration, or version changes. This work quantifies temporal variation and encourages the community to treat drift as a measurable phenomenon, improving the reliability of LLM evaluation. The analysis covers 49 models and 31,352 repeated score observations; within-day scores had a standard deviation of 2.80 points while between-day daily medians had a standard deviation of 8.43 points. The authors version benchmark configurations, use execution-based evaluation instead of LLM judges, separate availability failures from valid outcomes, and apply change-point detection to the resulting time series.

reddit · r/MachineLearning · /u/ionutvi · Sep 7, 07:44

**Background**: LLM performance drift refers to an AI model losing its edge or behaving differently over time. For API-served models, the endpoint behind a stable model name can change because providers update infrastructure, configuration, or versions. Traditional benchmarks are static snapshots, whereas longitudinal benchmarking continuously measures a model against its own prior behavior to detect drift. Related practical guides and frozen, deterministic benchmark suites emphasize version tracking to avoid misattributing changes to model capability.

<details><summary>References</summary>
<ul>
<li><a href="https://www.fiddler.ai/blog/how-to-monitor-llmops-performance-with-drift">How to Monitor LLMOps Performance with Drift Monitoring | Fiddler AI Blog</a></li>
<li><a href="https://medium.com/@tsiciliani/drift-detection-in-large-language-models-a-practical-guide-3f54d783792c">Drift Detection in Large Language Models: A Practical Guide | by Tony Siciliani | Medium</a></li>
<li><a href="https://github.com/jmeadlock/milo-bench">jmeadlock/milo-bench: Frozen, deterministic, longitudinal benchmark ...</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#benchmarking`, `#performance drift`, `#ML evaluation`, `#API models`

---

<a id="item-5"></a>
## [Huawei Debuts Kirin 9050 Pro With Logic-Folding Tech After Six-Year Gap](https://www.news.cn/20260907/adf46c5c003240d28cc3cf6de54f9b5f/c.html) ⭐️ 8.0/10

Huawei launched the Mate XT 2 triple-folding smartphone in Guangzhou on September 7, 2026, featuring the new Kirin 9050 Pro chip. It is the company&\#x27;s first high-performance chip using logic-folding technology and its first new flagship Kirin processor unveiled six years after the Mate 40. The launch ends Huawei&\#x27;s six-year gap without a new flagship Kirin chip and shows the company pursuing a different path amid restrictions on advanced manufacturing. If logic-folding delivers on its claimed performance gains, it could challenge conventional process-scaling assumptions and intensify competition in advanced packaging and 3D integration. The Kirin 9050 Pro stacks logic cells in layers within a single die and adds vertical interconnect paths, which shortens signal routes and reduces latency. It also features scenario-based CPU scheduling and a Da Vinci-architecture NPU capable of running an on-device multimodal model with 30 billion total parameters and 2 billion activated.

telegram · zaihuapd · Sep 7, 08:20

**Background**: Logic-folding technology was introduced by Huawei at ISCAS 2026, together with the &quot;tau law,&quot; as an alternative to traditional geometric scaling, and falls under 3D integrated circuits and advanced packaging. Because Huawei faces export controls that limit its access to leading-edge foundry processes, packaging and design innovations have become a strategic way to maintain chip competitiveness.

<details><summary>References</summary>
<ul>
<li><a href="https://baike.baidu.com/item/%E9%80%BB%E8%BE%91%E6%8A%98%E5%8F%A0%E6%8A%80%E6%9C%AF/67870423">逻辑折叠技术_百度百科</a></li>
<li><a href="https://www.ithome.com/0/999/337.htm">华为 Mate XT 2 非凡大师全新展翼三折叠手机发布：首发 麒 麟 9050 Pro ...</a></li>
<li><a href="https://www.sohu.com/a/1028674003_100085330">深度解读华为逻辑折叠技术:并非3D堆叠而是全新突破枷锁技术路线</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#semiconductor`, `#Kirin chip`, `#chip technology`, `#announcement`

---

<a id="item-6"></a>
## [China&\#x27;s Supreme Court Clarifies AI Liability in Judicial Interpretation](https://www.cnr.cn/news/20260907/t20260907_527806795.shtml) ⭐️ 8.0/10

On September 7, China&\#x27;s Supreme People&\#x27;s Court issued a 24-article judicial interpretation covering civil liability for AI-related disputes. It clarifies rules on unauthorized AI face-swapping and voice cloning, algorithmic price discrimination, AI impersonation in endorsements, and AI-enabled doxxing. This provides China&\#x27;s first comprehensive judicial framework for assigning civil liability in AI disputes, giving courts concrete legal grounds to rule on deepfakes and algorithmic pricing. It will push AI developers and platform operators to strengthen consent mechanisms and compliance, while offering consumers a clearer path for legal recourse. The interpretation spans 24 articles in five parts and also addresses liability in autonomous driving and intellectual property. It explicitly supports punitive damages claims when AI impersonation induces consumer purchases, and regulates AI-assisted doxxing and &\#x27;human flesh searches&\#x27; as privacy violations.

telegram · zaihuapd · Sep 7, 09:32

**Background**: Algorithmic price discrimination, known as &\#x27;big data killing the familiar&\#x27; \(大数据杀熟\), refers to platforms charging repeat customers higher prices than new ones for the same product or service based on data profiling; it has been banned by China&\#x27;s Personal Information Protection Law and e-commerce rules. &\#x27;Box opening&\#x27; \(网络开盒\) is a newer form of online violence in which perpetrators illegally obtain and publish a person&\#x27;s private information to harass or doxx them, often more aggressively than traditional &\#x27;human flesh searches&\#x27;.

<details><summary>References</summary>
<ul>
<li><a href="https://baike.baidu.com/item/%E5%A4%A7%E6%95%B0%E6%8D%AE%E6%9D%80%E7%86%9F/22456755">大数据杀熟_百度百科 算法滥用风险的监管现状与趋势探析-以“大数据杀熟”为视角 - 今日头条 算法加持下大数据“杀熟”？ - 知乎 算法厌恶背后：从伪装广告到大数据杀熟，用户为何感觉被收割？ 从程序员的角度出发：大数据杀熟，到底是什么原理？怎么反制？ 揭秘：为什么被杀熟的总是你？算法早已给你贴上了“待宰”标签</a></li>
<li><a href="https://xinwen.bjd.com.cn/content/s6669b8d8e4b035c6ca5eaf35.html">比“人肉搜索”更恶劣！ 焦点访谈起底新式 网 暴“ 开 盒 挂人”</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#China`, `#deepfake`, `#algorithmic discrimination`, `#legal compliance`

---