---
layout: default
title: "Horizon Summary: 2026-07-26 (ZH)"
date: 2026-07-26
lang: zh
---

> 从 28 条内容中筛选出 5 条重要资讯。

---

1. [SGLang v0.5.16：引入 DSpark 推测解码与 Inkling 模型支持](#item-1) ⭐️ 9.0/10
2. [vLLM v0.26.0：支持 Inkling 模型、DeepSeek-V4 加速、fp32 lm\_head](#item-2) ⭐️ 8.0/10
3. [开源权重 AI 效仿 Kubernetes 崛起](#item-3) ⭐️ 8.0/10
4. [Ruff v0.16.0 默认规则从 59 条增至 413 条](#item-4) ⭐️ 8.0/10
5. [AMD 能否打破 CUDA 护城河？](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SGLang v0.5.16：引入 DSpark 推测解码与 Inkling 模型支持](https://github.com/sgl-project/sglang/releases/tag/v0.5.16) ⭐️ 9.0/10

SGLang v0.5.16 引入了基于置信度的推测解码算法 DSpark，在 DeepSeek-V4-Pro 上达到 383.7 tok/s，并新增对 Inkling 模型的支持——这是一个拥有 9750 亿参数、支持 100 万标记上下文的多模态 MoE 模型。 该版本显著提升了 LLM 推理性能，特别是针对大型 MoE 和多模态模型，能加速前沿 AI 系统的部署和服务。 DSpark 采用半自回归块草稿生成与基于置信度的验证窗口大小调整；Inkling 则混合了滑动窗口、全注意力和 Mamba2 线性注意力，并配备 NVFP4 MoE 和原生 MTP。此版本还将 UnifiedRadixTree 设为默认，并移除了实验性的 QServe 和 FBGEMM FP8 量化。

github · Qiaolin-Yu · 7月25日 00:13

**背景**: 推测解码通过轻量级草稿模型生成 token 并由目标模型验证，从而加速 LLM 推理。DSpark 是 DeepSeek 提出的新算法，根据草稿的置信度自适应调整验证长度。Mamba2 是一种线性注意力机制，计算复杂度随序列长度线性增长；NVFP4 是 NVIDIA 的量化格式，用于在 Blackwell GPU 上实现高效的 FP4 计算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.05147">[2607.05147] DSpark: Confidence-Scheduled Speculative ...</a></li>
<li><a href="https://www.marktechpost.com/2026/06/27/deepseek-releases-dspark-a-speculative-decoding-framework-that-accelerates-deepseek-v4-per-user-generation-60-85-over-mtp-1/">DeepSeek Releases DSpark, a Speculative Decoding Framework ...</a></li>
<li><a href="https://medium.com/@danieljsmit/mamba2-the-hardware-algorithm-co-design-that-unified-attention-and-state-space-models-77856d2ac4f4">Mamba2: The Hardware-Algorithm Co-Design That Unified Attention and ...</a></li>

</ul>
</details>

**标签**: `#speculative decoding`, `#LLM inference`, `#SGLang`, `#MoE`, `#high-performance`

---

<a id="item-2"></a>
## [vLLM v0.26.0：支持 Inkling 模型、DeepSeek-V4 加速、fp32 lm\_head](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 完全支持 TML Inkling 模型家族，为 DeepSeek-V4 带来性能提升（例如专用路由内核带来 2.94% 的 TPOT 提升），并通过 head\_dtype 引入 fp32 lm\_head 以提高生成准确率。该版本还支持按 KV 缓存组灵活选择注意力后端，并通过分层存储完善了 KV 卸载功能。 此版本通过支持 Inkling（1T 参数多模态 MoE）等前沿模型并优化 DeepSeek-V4，巩固了 vLLM 作为领先推理引擎的地位，直接惠及大规模 LLM 服务用户。注意力后端的灵活性和 KV 卸载改进使 vLLM 能更好地适应多样化硬件和内存受限的部署场景。 该版本包含来自 212 位贡献者的 411 次提交，支持 Inkling 的 MTP=1 推测解码，并添加了 ModelOpt NVFP4 量化。它还迁移了多个模型到 Transformers 5.13 后端，包括 Olmo/Olmo2、MistralLarge3 和 HunyuanVL。

github · khluu · 7月25日 10:38

**背景**: vLLM 是一个高吞吐、内存高效的 LLM 推理引擎，采用 PagedAttention。TML Inkling 是一个 975B 参数（41B 活跃）的多模态 MoE 模型，支持高达 1M token 的上下文。MTP（多 Token 预测）是一种推测解码技术，每次前向传播预测多个 token 以提高吞吐量，而 NVFP4 是一种针对 NVIDIA GPU 的 4 位量化格式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://vllm.ai/blog/2026-07-15-inkling">TML Inkling on vLLM: Day-0 Support with Optimized Performance | vLLM Blog</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/mtp/">MTP (Multi-Token Prediction) - vLLM</a></li>

</ul>
</details>

**标签**: `#vllm`, `#LLM inference`, `#performance optimization`, `#DeepSeek`, `#new model support`

---

<a id="item-3"></a>
## [开源权重 AI 效仿 Kubernetes 崛起](https://tobi.knaup.me/2026-07-25-open-weight-ai-is-having-its-kubernetes-moment/) ⭐️ 8.0/10

文章认为，开放权重 AI 模型正沿着与 Kubernetes 相似的轨迹发展，可能带来去中心化、低成本的 AI 生态系统，并引发了关于监管和定价的重要问题。 这很重要，因为它可能使 AI 的获取民主化、降低成本，并挑战集中式 AI 模型，类似于 Kubernetes 对云计算的变革。同时，它也迫使政策制定者重新考虑对开放权重模型的监管。 文章将开放权重 AI 的当前状态与 Kubernetes 的早期进行了类比，强调开放权重模型允许任何人运行和修改，但由于训练数据和代码可能未公开，它们并非完全开源。

hackernews · tknaup · 7月25日 14:49 · [社区讨论](https://news.ycombinator.com/item?id=49048034)

**背景**: 开放权重 AI 指的是公开发布训练后参数（权重）的模型，允许他人运行或微调模型，但无需获取完整的训练数据或代码。Kubernetes 是一个开源容器编排平台，已成为行业标准，推动了创新并降低了成本。文章认为，开放权重 AI 可能通过建立去中心化的模型和服务生态系统，以类似方式颠覆 AI 行业。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Open-weight_artificial_intelligence">Open-weight artificial intelligence</a></li>

</ul>
</details>

**社区讨论**: 评论讨论了基于权重禁止中国模型的技术不可行性（ozgung）、对 AI 定价波动的困惑（firasd）、类似 Linux 的协作开放模型的潜力（pianopatrick），以及希望 OpenAI 更频繁更新其开放模型（drnick1）。一条不完整的评论开始提及中国扩大生产。

**标签**: `#open-weight AI`, `#Kubernetes`, `#open source`, `#AI regulation`, `#AI pricing`

---

<a id="item-4"></a>
## [Ruff v0.16.0 默认规则从 59 条增至 413 条](https://simonwillison.net/2026/Jul/25/ruff/#atom-everything) ⭐️ 8.0/10

Astral 于 7 月 23 日发布了 Ruff v0.16.0，将默认 lint 规则从 59 条增加到 413 条，导致许多未固定 Ruff 依赖的项目 CI 失败。 这一重大扩展显著提高了 Python 代码质量的基线，能捕获许多以前默认忽略的语法错误和运行时问题，将迫使许多项目更新代码库。 该版本规则总数从 708 条增至 968 条，新默认规则涵盖时区参数缺失、盲目捕获异常等问题。Ruff 的自动修复功能在一个项目中修复了 1618 个错误中的 1538 个，但仍有 80 个需手动处理。

rss · Simon Willison · 7月25日 22:44

**背景**: Ruff 是一个极快的 Python 代码检查器和格式化工具，旨在替代 Flake8 和 Black 等工具。许多开发者使用未固定版本的依赖（例如写 &\#x27;ruff&\#x27; 而不指定版本），因此重大更新会自动应用到他们的 CI 流水线中，经常导致意外失败。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.astral.sh/ruff/linter/">The Ruff Linter | Ruff</a></li>
<li><a href="https://github.com/astral-sh/ruff">GitHub - astral-sh/ ruff : An extremely fast Python linter and code...</a></li>
<li><a href="https://realpython.com/ruff-python/">Ruff : A Modern Python Linter for Error-Free and Maintainable Code...</a></li>

</ul>
</details>

**标签**: `#Python`, `#Ruff`, `#linting`, `#version release`, `#CI/CD`

---

<a id="item-5"></a>
## [AMD 能否打破 CUDA 护城河？](https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing) ⭐️ 8.0/10

本文分析了 AMD 的战略，包括代理内核生成（Agentic Kernel Generation）和 Helios MI455X 机架，以挑战 NVIDIA 的 CUDA 生态系统主导地位。 这很重要，因为 AMD 成功克服 CUDA 护城河可能会重塑 AI 硬件格局，为 NVIDIA 的主导平台提供替代方案。 文章强调了 AMD 的内部困难，包括不稳定的开发集群和生产爬坡问题，但也提到财务工程带来的高达 105%的折扣。

rss · Semianalysis · 7月25日 00:33

**背景**: CUDA 护城河指的是 NVIDIA 的软件生态系统锁定，开发者依赖 CUDA 进行 GPU 计算。AMD 的 ROCm 是一个开源的替代方案，但在采用率和性能上滞后。代理内核生成使用 AI 自动优化内核，有可能拉平竞争。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2602.24286v1">CUDA AgentCUDA Agent: Large-Scale Agentic RL for High-Performance CUDA Kernel Generation</a></li>
<li><a href="https://www.storagereview.com/news/amd-mi455x-and-helios-432gb-hbm4-72-gpu-racks-and-a-real-answer-to-vera-rubin">AMD MI455X and Helios: 432GB HBM4, 72-GPU Racks, and a Real ...</a></li>

</ul>
</details>

**标签**: `#AMD`, `#CUDA`, `#AI hardware`, `#software ecosystem`

---