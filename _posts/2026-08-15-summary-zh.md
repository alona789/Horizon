---
layout: default
title: "Horizon Summary: 2026-08-15 (ZH)"
date: 2026-08-15
lang: zh
---

> 从 23 条内容中筛选出 3 条重要资讯。

---

1. [BDH-CQ：以循环潜在推理在 ARC-AGI-1 上实现创纪录成本效率](#item-1) ⭐️ 9.0/10
2. [Codex 自动研究实现 232 倍内核加速](#item-2) ⭐️ 8.0/10
3. [阿里 Qwen 开源权重模型下载量破 30 亿，超越 Meta 与谷歌](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [BDH-CQ：以循环潜在推理在 ARC-AGI-1 上实现创纪录成本效率](https://www.reddit.com/r/MachineLearning/comments/1vov5r5/bdhcq_incontext_learning_with_recurrent_latent/) ⭐️ 9.0/10

研究者推出了 BDH-CQ，一个 150M 参数的上下文学习系统，通过循环潜在推理来解决 ARC-AGI-1 任务，而无需将中间状态解码为语言。该系统在 ARC-AGI-1 上达到 29.5%的 pass@2，每个任务的计算成本为 0.00070 美元，突破了此前报告的成本-准确率帕累托前沿。 这一结果表明，无需生成长篇思维链也能实现强大的抽象推理，为推理模型指出了更省算力的发展方向。如果得到验证，它可能使先进的上下文推理变得更加便宜、更便于实际部署。 BDH-CQ 在推理时随输入不断更新循环记忆，然后在潜在工作空间中进行迭代计算来求解查询；训练中未使用任务标识符或评测示范对，推理时也不更新任何参数。每个任务 0.00070 美元是按计算量估算的成本，作者强调中间推理过程不会以语言形式输出。

reddit · r/MachineLearning · /u/moschles · 8月15日 06:18

**背景**: ARC-AGI-1 是一个基准测试，旨在检验 AI 系统能否适应训练中未见过的新型抽象推理任务。主流推理模型通常通过生成很长的思维链来提升准确率，成本较高。BDH-CQ 则基于潜在推理的思路，让循环模块在高维空间中迭代而不生成词元，从而在不解码中间步骤的情况下扩展测试时计算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2608.09888">BDH-CQ: In-Context Learning with Recurrent Latent Reasoning</a></li>
<li><a href="https://arcprize.org/arc-agi/1">ARC - AGI - 1</a></li>
<li><a href="https://www.explainx.ai/blog/pathway-bdh-cq-150m-post-transformer-arc-agi-august-2026">Pathway BDH-CQ: 150M Model, 11x Cheaper Than GPT-5.6 ...</a></li>

</ul>
</details>

**标签**: `#in-context learning`, `#recurrent reasoning`, `#ARC-AGI`, `#latent space`, `#cost-efficiency`

---

<a id="item-2"></a>
## [Codex 自动研究实现 232 倍内核加速](https://sankalp.bearblog.dev/autoresearch/) ⭐️ 8.0/10

一位开发者使用 OpenAI Codex 自动化研究和优化 GPU 内核，实现了 232 倍的加速。这一结果展示了 AI 代理处理基准测试、性能分析和代码改进的新工作流。 这表明 AI 驱动的优化能在底层 GPU 编程领域带来显著的性能提升，而该领域传统上需要深厚的专业知识。然而，社区讨论提醒，这类方案往往过度拟合特定输入，可能缺乏鲁棒性。 这一加速是通过 Codex 的迭代研究循环——基准测试、性能分析、验证和改进——应用于 GPU 内核代码实现的。值得注意的是，一些由类似 AI 流程生成的竞赛方案在分布外输入上失效，而专家指导的方案则保持稳定。

hackernews · tosh · 8月15日 11:00 · [社区讨论](https://news.ycombinator.com/item?id=49309549)

**背景**: CUDA 内核是在 NVIDIA GPU 核心上运行的代码单元，通常由程序员编写以执行并行计算。OpenAI Codex 是一套 AI 编码代理，可以自动化代码审查和重构等软件工程任务。近期研究既强调了 LLM 驱动内核生成的前景，也指出了评估缺口——现有基准通常使用固定输入形状，可能无法反映真实世界的多样性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/codex/">Codex in ChatGPT | AI Coding Agents for Software... | OpenAI</a></li>
<li><a href="https://modal.com/gpu-glossary/device-software/kernel">What is a CUDA Kernel ? | GPU Glossary</a></li>
<li><a href="https://arxiv.org/html/2601.15727v1">Towards Automated Kernel Generation in the Era of LLMs</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了相关实验：有人尝试在带有验证器的视频编解码器上使用 DeepSeek v4，还有人指出 AI 优化产生的 10 个顶级竞赛方案中有 8 个在分布外形状上失效。其他人则欣赏这篇文章的人工写作风格，并推测 GPU 内核是否为 LLM 提供了丰富的训练领域。

**标签**: `#AI-assisted development`, `#kernel optimization`, `#GPU programming`, `#performance`, `#Codex`

---

<a id="item-3"></a>
## [阿里 Qwen 开源权重模型下载量破 30 亿，超越 Meta 与谷歌](https://www.bloomberg.com/news/articles/2026-08-15/alibaba-ai-models-hit-3-billion-downloads-passing-meta-google) ⭐️ 8.0/10

据 Hugging Face 报告，阿里巴巴的开放权重 Qwen AI 模型在六个月内全球下载量超过 30 亿次。2026 年，谷歌模型下载量为 4.18 亿次，Meta 为 2.27 亿次。 这一里程碑表明，阿里巴巴 Qwen 系列已成为领先的开放权重 AI 生态，在采用率上超过西方科技巨头。这标志着全球开源 AI 格局发生转变，中国模型正获得开发者广泛采用。 阿里称 Qwen 已开源超过 460 个模型，衍生版本超过 30 万个。这些模型采用 Apache 2.0、Qwen License 等许可协议分发。

telegram · zaihuapd · 8月15日 15:18

**背景**: 开放权重模型是指核心参数公开释出的 AI 模型，任何人都可以下载、检查、修改并在自己的基础设施上运行。Qwen 是阿里云推出的大语言模型与多模态模型系列，托管在 Hugging Face 上，在学术和商业领域被广泛使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://huggingface.co/Qwen">Org profile for Qwen on Hugging Face, the AI community building the...</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**标签**: `#AI`, `#Open Source`, `#Alibaba`, `#Qwen`, `#LLM`

---