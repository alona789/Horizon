---
layout: default
title: "Horizon Summary: 2026-10-05 (EN)"
date: 2026-10-05
lang: en
---

> From 22 items, 2 important content pieces were selected

---

1. [Strata claims 125B Qwen3.8-Flash-Next on a single RTX 4090 at ~124 tok/s](#item-1) ⭐️ 8.0/10
2. [ARC-AGI-3 Kaggle scores reportedly jump from 7% to 56% in 30 days](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Strata claims 125B Qwen3.8-Flash-Next on a single RTX 4090 at ~124 tok/s](https://github.com/Niko1221/Strata) ⭐️ 8.0/10

A GitHub project called Strata \(Niko1221/Strata\) released an inference engine that claims to run the 125B-parameter Qwen3.8-Flash-Next on consumer hardware, including a single RTX 4090, at roughly 100-124 tokens per second. It ships one-click installers for Windows and Linux, exposes an OpenAI/Anthropic-compatible API on localhost, and supports optional image input. If the numbers hold up, it means a 125B-class mixture-of-experts model that would normally need a datacenter GPU can be served locally on a single consumer card, which is a meaningful step for privacy-preserving and offline LLM use. It also intensifies the competition among local inference stacks \(llama.cpp, ds4, Strata\) over how much quality you must trade for speed and memory savings. The headline claim is contested: one commenter benchmarked the same GGUF weights and vision adapter on both engines and measured a median coordinate error of 154.8 px under Strata versus 46.5 px under llama.cpp, while defenders report strong results running 4-bit quants on rented RTX Pro 6000/RTX 6000 Pro hardware \(prefill ~1,251 tok/s, decode up to ~255 tok/s\). Others caution that pushing below 4-bit quantization tends to degrade quality noticeably, so the extreme speeds may come with a real accuracy cost.

hackernews · snehesht · Oct 4, 12:51 · [Discussion](https://news.ycombinator.com/item?id=49953495)

**Background**: Qwen3.8-Flash-Next is a very large mixture-of-experts model: instead of activating all weights for every token, it routes each token through a small subset of experts \(the project&\#x27;s explainer cites 24,576 experts\), which is what makes running it on limited hardware conceivable. Local inference engines like llama.cpp rely on quantization — storing weights at 4 bits or fewer instead of 16 — to shrink a model&\#x27;s memory footprint enough to fit on consumer GPUs, at the cost of some numerical fidelity. Strata is a newer inference engine competing in that same space, and disputed benchmarks between engines on identical weights typically reflect differences in kernels, KV-cache handling, and how the vision adapter is executed.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Niko1221/Strata/releases">Releases · Niko1221/ Strata · GitHub</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-Flash-Next">Qwen / Qwen 3 . 8 - Flash - Next · Hugging Face</a></li>
<li><a href="https://www.youtube.com/watch?v=hJ_Iw2E7cnc">Strata GitHub Explained: How a 125B Qwen3.8-Flash-Next... - YouTube</a></li>

</ul>
</details>

**Discussion**: Sentiment is split between enthusiasm and skepticism. One commenter reproduced the ~124 tok/s result on an RTX 4090 with 128GB DDR5 and a Ryzen 7950x3d, and another praised the 4-bit quant of this model on an RTX 6000 Pro for supporting four concurrent streams at 400+ tok/s, while a third warned that going below 4-bit risks significant quality degradation. The sharpest pushback is the vision benchmark showing Strata&\#x27;s coordinate error being roughly three times worse than llama.cpp on identical weights, plus a broader complaint about heavy promotional spam and unproven hype.

**Tags**: `#local-llm-inference`, `#quantization`, `#consumer-gpu`, `#llm-serving`, `#model-compression`

---

<a id="item-2"></a>
## [ARC-AGI-3 Kaggle scores reportedly jump from 7% to 56% in 30 days](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/) ⭐️ 8.0/10

A Reddit post on r/MachineLearning reports that the top score on the ARC-AGI-3 Kaggle leaderboard rose from about 7% to 56% over the past 30 days, with the caveat that the posted leaderboard graphic is slightly out of date. The poster claims small local models running inside an evaluation harness have begun to beat average humans on the benchmark. ARC-AGI is explicitly designed to be easy for humans and hard for AI, so a rapid climb on its leaderboard would undercut the assumption that abstraction-based reasoning remains a durable human advantage. If the number holds up, it suggests that harness engineering and small local models — not just frontier-scale LLMs — may be enough to make fast progress on tasks previously considered out of reach. The claim comes from a single Reddit post with limited technical detail, and the poster notes the leaderboard screenshot is outdated, so the 56% figure is unverified. A key constraint is that Kaggle competitors are limited to relatively small local models, meaning the reported gains likely come from harness design and search or scaffolding rather than raw model scale.

reddit · r/MachineLearning · /u/we\_are\_mammals · Oct 4, 10:24 · [Discussion](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/)

**Background**: ARC-AGI \(Abstraction and Reasoning Corpus for Artificial General Intelligence\) is a benchmark built by the ARC Prize Foundation around the principle of &quot;easy for humans, hard for AI,&quot; deliberately removing scale advantages and task-specific cues so that systems must infer abstract rules from a handful of examples. Its newest iteration, ARC-AGI-3, is described by the foundation as a benchmark for agentic intelligence that has so far remained unbeaten. An evaluation harness is the standardized infrastructure that defines what gets evaluated, runs the scoring, and reports results — in competitions like this, much of the innovation happens in the harness rather than the model weights, and &quot;small local models&quot; are compact language models run on local hardware rather than accessed through large cloud APIs.

<details><summary>References</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi">ARC Prize - The only AI benchmark that measures AGI progress.</a></li>
<li><a href="https://arcprize.org/">ARC Prize Foundation is a nonprofit advancing open-source AGI ...</a></li>
<li><a href="https://arize.com/blog/what-is-an-evaluation-harness/">What is an evaluation harness ? Definition &amp; guide - Arize AI</a></li>

</ul>
</details>

**Tags**: `#ARC-AGI`, `#Kaggle`, `#AI benchmarks`, `#reasoning`, `#LLM evaluation`

---