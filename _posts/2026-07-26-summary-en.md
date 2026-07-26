---
layout: default
title: "Horizon Summary: 2026-07-26 (EN)"
date: 2026-07-26
lang: en
---

> From 28 items, 5 important content pieces were selected

---

1. [SGLang v0.5.16: DSpark Speculative Decoding &amp; Inkling Support](#item-1) ⭐️ 9.0/10
2. [vLLM v0.26.0: Inkling support, DeepSeek-V4 speedups, fp32 lm\_head](#item-2) ⭐️ 8.0/10
3. [Open-Weight AI Mirrors Kubernetes Rise](#item-3) ⭐️ 8.0/10
4. [Ruff v0.16.0 Boosts Default Rules from 59 to 413](#item-4) ⭐️ 8.0/10
5. [Can AMD Break the CUDA Moat?](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SGLang v0.5.16: DSpark Speculative Decoding &amp; Inkling Support](https://github.com/sgl-project/sglang/releases/tag/v0.5.16) ⭐️ 9.0/10

SGLang v0.5.16 introduces DSpark, a confidence-driven speculative decoding algorithm that achieves 383.7 tok/s on DeepSeek-V4-Pro, and adds support for Inkling, a 975B-parameter multimodal MoE model with a 1M-token context. This release significantly advances LLM inference performance, especially for large MoE and multimodal models, enabling faster serving and broader deployment of cutting-edge AI systems. DSpark uses semi-autoregressive block drafting with confidence-based verify window sizing, while Inkling mixes sliding-window, full, and Mamba2 linear attention with NVFP4 MoE and native MTP. The release also makes UnifiedRadixTree the default and removes experimental QServe and FBGEMM FP8 quantization.

github · Qiaolin-Yu · Jul 25, 00:13

**Background**: Speculative decoding accelerates LLM inference by using a lightweight draft model to generate tokens that a target model verifies. DSpark is a novel algorithm from DeepSeek that adaptively determines verification lengths based on draft confidence. Mamba2 is a linear attention mechanism that scales linearly with sequence length, and NVFP4 is an NVIDIA quantization format for efficient FP4 computation on Blackwell GPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.05147">[2607.05147] DSpark: Confidence-Scheduled Speculative ...</a></li>
<li><a href="https://www.marktechpost.com/2026/06/27/deepseek-releases-dspark-a-speculative-decoding-framework-that-accelerates-deepseek-v4-per-user-generation-60-85-over-mtp-1/">DeepSeek Releases DSpark, a Speculative Decoding Framework ...</a></li>
<li><a href="https://medium.com/@danieljsmit/mamba2-the-hardware-algorithm-co-design-that-unified-attention-and-state-space-models-77856d2ac4f4">Mamba2: The Hardware-Algorithm Co-Design That Unified Attention and ...</a></li>

</ul>
</details>

**Tags**: `#speculative decoding`, `#LLM inference`, `#SGLang`, `#MoE`, `#high-performance`

---

<a id="item-2"></a>
## [vLLM v0.26.0: Inkling support, DeepSeek-V4 speedups, fp32 lm\_head](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 adds full support for the TML Inkling model family, delivers performance improvements for DeepSeek-V4 \(e.g., 2.94% TPOT gain from a specialized routing kernel\), and introduces fp32 lm\_head via head\_dtype for improved generation accuracy. The release also enables flexible attention backend selection per KV-cache group and matures KV offloading with tiered storage. This release strengthens vLLM as a leading inference engine by supporting cutting-edge models like Inkling \(1T-parameter multimodal MoE\) and optimizing DeepSeek-V4, which directly benefits users serving large-scale LLMs. The attention backend flexibility and KV offloading improvements make vLLM more adaptable to diverse hardware and memory-constrained deployments. The release includes 411 commits from 212 contributors, covers MTP=1 speculative decoding for Inkling, and adds ModelOpt NVFP4 quantization. It also migrates several models to the Transformers 5.13 backend, including Olmo/Olmo2, MistralLarge3, and HunyuanVL.

github · khluu · Jul 25, 10:38

**Background**: vLLM is a high-throughput, memory-efficient LLM inference engine with PagedAttention. The TML Inkling model is a 975B-parameter \(41B active\) multimodal MoE model supporting up to 1M tokens context. MTP \(Multi-Token Prediction\) is a speculative decoding technique that predicts multiple tokens per forward pass to boost throughput, while NVFP4 is a 4-bit quantization format for NVIDIA GPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://vllm.ai/blog/2026-07-15-inkling">TML Inkling on vLLM: Day-0 Support with Optimized Performance | vLLM Blog</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/mtp/">MTP (Multi-Token Prediction) - vLLM</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#LLM inference`, `#performance optimization`, `#DeepSeek`, `#new model support`

---

<a id="item-3"></a>
## [Open-Weight AI Mirrors Kubernetes Rise](https://tobi.knaup.me/2026-07-25-open-weight-ai-is-having-its-kubernetes-moment/) ⭐️ 8.0/10

The article argues that open-weight AI models are following a trajectory similar to Kubernetes, potentially leading to a decentralized, cost-effective AI ecosystem. It highlights that this shift raises important questions about regulation and pricing. This matters because it could democratize AI access, reduce costs, and challenge centralized AI models, similar to how Kubernetes transformed cloud computing. It also forces policymakers to reconsider regulation of open-weight models. The article draws parallels between the current state of open-weight AI and Kubernetes&\#x27; early days, emphasizing that open-weight models enable anyone to run and modify them, but they are not fully open-source as training data and code may not be included.

hackernews · tknaup · Jul 25, 14:49 · [Discussion](https://news.ycombinator.com/item?id=49048034)

**Background**: Open-weight AI refers to models where the trained parameters \(weights\) are publicly released, allowing others to run or fine-tune the model without full access to training data or code. Kubernetes is an open-source container orchestration platform that became the industry standard, driving innovation and reducing costs. The article suggests open-weight AI could similarly disrupt the AI industry by enabling a decentralized ecosystem of models and services.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_artificial_intelligence">Open-weight artificial intelligence</a></li>

</ul>
</details>

**Discussion**: Comments discuss the technical impossibility of banning Chinese models based on weights \(ozgung\), confusion about AI pricing volatility \(firasd\), the potential for collaborative open models akin to Linux \(pianopatrick\), and a desire for more frequent updates from OpenAI&\#x27;s open models \(drnick1\). A cut-off comment begins to mention China scaling production.

**Tags**: `#open-weight AI`, `#Kubernetes`, `#open source`, `#AI regulation`, `#AI pricing`

---

<a id="item-4"></a>
## [Ruff v0.16.0 Boosts Default Rules from 59 to 413](https://simonwillison.net/2026/Jul/25/ruff/#atom-everything) ⭐️ 8.0/10

Astral released Ruff v0.16.0 on July 23rd, increasing the number of default linting rules from 59 to 413, causing widespread CI failures for projects with unpinned Ruff dependencies. This major expansion significantly raises the baseline for Python code quality, catching many syntax errors and runtime issues that were previously ignored by default, and will require many projects to update their codebases. The release includes 968 total rules, up from 708, with the new defaults covering issues like missing timezone arguments and blind exception catching. Ruff&\#x27;s automatic fix feature fixed 1538 out of 1618 errors in one project, but 80 remained for manual review.

rss · Simon Willison · Jul 25, 22:44

**Background**: Ruff is an extremely fast Python linter and code formatter, designed as a drop-in replacement for tools like Flake8 and Black. Many developers specify dependencies with unpinned versions \(e.g., &\#x27;ruff&\#x27; without a version constraint\), so major updates automatically apply to their CI pipelines, often causing unexpected failures.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.astral.sh/ruff/linter/">The Ruff Linter | Ruff</a></li>
<li><a href="https://github.com/astral-sh/ruff">GitHub - astral-sh/ ruff : An extremely fast Python linter and code...</a></li>
<li><a href="https://realpython.com/ruff-python/">Ruff : A Modern Python Linter for Error-Free and Maintainable Code...</a></li>

</ul>
</details>

**Tags**: `#Python`, `#Ruff`, `#linting`, `#version release`, `#CI/CD`

---

<a id="item-5"></a>
## [Can AMD Break the CUDA Moat?](https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing) ⭐️ 8.0/10

The article analyzes AMD&\#x27;s strategies, including agentic kernel generation and the Helios MI455X rack, to challenge NVIDIA&\#x27;s CUDA ecosystem dominance. This is significant because AMD&\#x27;s success in overcoming the CUDA moat could reshape the AI hardware landscape, offering alternatives to NVIDIA&\#x27;s dominant platform. The article highlights AMD&\#x27;s internal struggles, including unstable development clusters and production ramp issues, but also notes up to 105% discounts from finance engineering.

rss · Semianalysis · Jul 25, 00:33

**Background**: The CUDA moat refers to NVIDIA&\#x27;s software ecosystem lock-in, where developers rely on CUDA for GPU computing. AMD&\#x27;s ROCm is an open-source alternative but has lagged in adoption and performance. Agentic kernel generation uses AI to automatically optimize kernels, potentially leveling the playing field.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2602.24286v1">CUDA AgentCUDA Agent: Large-Scale Agentic RL for High-Performance CUDA Kernel Generation</a></li>
<li><a href="https://www.storagereview.com/news/amd-mi455x-and-helios-432gb-hbm4-72-gpu-racks-and-a-real-answer-to-vera-rubin">AMD MI455X and Helios: 432GB HBM4, 72-GPU Racks, and a Real ...</a></li>

</ul>
</details>

**Tags**: `#AMD`, `#CUDA`, `#AI hardware`, `#software ecosystem`

---