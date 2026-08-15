---
layout: default
title: "Horizon Summary: 2026-08-15 (EN)"
date: 2026-08-15
lang: en
---

> From 23 items, 3 important content pieces were selected

---

1. [BDH-CQ Achieves Record Cost-Efficiency with Recurrent Latent Reasoning on ARC-AGI-1](#item-1) ⭐️ 9.0/10
2. [Codex Auto-Research Achieves 232x Faster Kernel](#item-2) ⭐️ 8.0/10
3. [Alibaba Qwen Open-Weight Models Top 3B Downloads, Pass Meta and Google](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [BDH-CQ Achieves Record Cost-Efficiency with Recurrent Latent Reasoning on ARC-AGI-1](https://www.reddit.com/r/MachineLearning/comments/1vov5r5/bdhcq_incontext_learning_with_recurrent_latent/) ⭐️ 9.0/10

Researchers introduced BDH-CQ, a 150M-parameter in-context learning system that solves ARC-AGI-1 tasks via recurrent latent reasoning without decoding intermediate states into language. It reached 29.5% pass@2 on ARC-AGI-1 at a computed cost of $0.00070 per task, breaking the previously reported cost–accuracy Pareto frontier. This result shows that strong abstract reasoning can be achieved without generating lengthy chains of thought, pointing to a more compute-efficient direction for reasoning models. If confirmed, it could make advanced in-context reasoning far cheaper and more practical for deployment. BDH-CQ updates its recurrent memory at inference time as inputs arrive, then solves the query using iterative computation in a latent workspace; no task identifiers or demonstration pairs are seen during training and no parameters are updated at inference. The $0.00070-per-task figure is a computed cost estimate, and the authors emphasize that intermediate reasoning is never verbalized.

reddit · r/MachineLearning · /u/moschles · Aug 15, 06:18

**Background**: ARC-AGI-1 is a benchmark designed to test an AI system&\#x27;s ability to adapt to novel abstract reasoning tasks that were not seen during training. Mainstream reasoning models typically improve accuracy by generating long chains of thought, which is expensive. BDH-CQ instead builds on latent-reasoning ideas in which a recurrent block iterates in a high-dimensional space without producing tokens, enabling test-time computation to scale without decoding intermediate steps.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2608.09888">BDH-CQ: In-Context Learning with Recurrent Latent Reasoning</a></li>
<li><a href="https://arcprize.org/arc-agi/1">ARC - AGI - 1</a></li>
<li><a href="https://www.explainx.ai/blog/pathway-bdh-cq-150m-post-transformer-arc-agi-august-2026">Pathway BDH-CQ: 150M Model, 11x Cheaper Than GPT-5.6 ...</a></li>

</ul>
</details>

**Tags**: `#in-context learning`, `#recurrent reasoning`, `#ARC-AGI`, `#latent space`, `#cost-efficiency`

---

<a id="item-2"></a>
## [Codex Auto-Research Achieves 232x Faster Kernel](https://sankalp.bearblog.dev/autoresearch/) ⭐️ 8.0/10

A developer used OpenAI Codex to automate the research and optimization of a GPU kernel, achieving a 232x speedup. The result highlights a new workflow where AI agents handle benchmarking, profiling, and code refinement. This demonstrates that AI-driven optimization can yield dramatic performance gains in low-level GPU programming, a domain traditionally requiring deep expertise. However, community discussion cautions that such solutions often overfit to specific inputs and may lack robustness. The speedup was achieved via Codex&\#x27;s iterative research loop—benchmark, profile, verify, and improve—applied to GPU kernel code. Notably, some competition entries produced by similar AI pipelines broke on out-of-distribution inputs, while expert-guided solutions remained stable.

hackernews · tosh · Aug 15, 11:00 · [Discussion](https://news.ycombinator.com/item?id=49309549)

**Background**: A CUDA kernel is the unit of code that runs on NVIDIA GPU cores, typically written by programmers to perform parallel computations. OpenAI Codex is a suite of AI coding agents that can automate software engineering tasks like code reviews and refactors. Recent research highlights both the promise and evaluation gaps in LLM-driven kernel generation, where benchmarks often use fixed input shapes and may miss real-world diversity.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/codex/">Codex in ChatGPT | AI Coding Agents for Software... | OpenAI</a></li>
<li><a href="https://modal.com/gpu-glossary/device-software/kernel">What is a CUDA Kernel ? | GPU Glossary</a></li>
<li><a href="https://arxiv.org/html/2601.15727v1">Towards Automated Kernel Generation in the Era of LLMs</a></li>

</ul>
</details>

**Discussion**: Commenters shared related experiments: one tried DeepSeek v4 on a video codec with a verifier, and another noted that 8 of 10 top competition solutions from AI optimization broke on out-of-distribution shapes. Others appreciated the human-written prose and speculated whether GPU kernels are a rich training domain for LLMs.

**Tags**: `#AI-assisted development`, `#kernel optimization`, `#GPU programming`, `#performance`, `#Codex`

---

<a id="item-3"></a>
## [Alibaba Qwen Open-Weight Models Top 3B Downloads, Pass Meta and Google](https://www.bloomberg.com/news/articles/2026-08-15/alibaba-ai-models-hit-3-billion-downloads-passing-meta-google) ⭐️ 8.0/10

Alibaba&\#x27;s open-weight Qwen AI models surpassed 3 billion global downloads in six months, according to a Hugging Face report. Google&\#x27;s models recorded 418 million downloads and Meta&\#x27;s 227 million in 2026. This milestone shows Alibaba&\#x27;s Qwen family has become a leading open-weight AI ecosystem, outpacing Western tech giants in adoption. It signals a shift in the global open-source AI landscape, with Chinese models gaining widespread developer traction. Alibaba says Qwen has open-sourced over 460 models, with more than 300,000 derived variants. The models are distributed under licenses such as Apache 2.0 and the source-available Qwen License.

telegram · zaihuapd · Aug 15, 15:18

**Background**: Open-weight models are AI models whose core parameters are publicly released, allowing anyone to download, inspect, modify, and run them on their own infrastructure. Qwen is Alibaba Cloud&\#x27;s family of large language and multimodal models, hosted on Hugging Face and widely used in both academic and commercial settings.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://huggingface.co/Qwen">Org profile for Qwen on Hugging Face, the AI community building the...</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Open Source`, `#Alibaba`, `#Qwen`, `#LLM`

---