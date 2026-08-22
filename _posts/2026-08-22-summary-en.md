---
layout: default
title: "Horizon Summary: 2026-08-22 (EN)"
date: 2026-08-22
lang: en
---

> From 30 items, 5 important content pieces were selected

---

1. [SGLang v0.5.18 Release Adds New Models and Faster Startup](#item-1) ⭐️ 8.0/10
2. [MCP Roadmap: Remote Servers as Standard HTTP, Standardized Agent Identity](#item-2) ⭐️ 8.0/10
3. [Developer Trains 250M-Param Quantized LLM From Scratch, Deploys in 60 MB](#item-3) ⭐️ 8.0/10
4. [Open-Source Roguelike DelveRL Bridges Game and RL Agent Training](#item-4) ⭐️ 8.0/10
5. [SemiAnalysis: Open Models Halve Time to Parity Each Generation](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SGLang v0.5.18 Release Adds New Models and Faster Startup](https://github.com/sgl-project/sglang/releases/tag/v0.5.18) ⭐️ 8.0/10

SGLang v0.5.18 was released, incorporating 710 pull requests from 212 contributors. The release adds support for new models including Meta&\#x27;s Muse Glimmer, SANA-Video, LTX-2.5, and Cosmos3 Edge, plus optimizations such as overlapped checkpoint staging and TP LMHead with All-to-All. SGLang is a widely adopted LLM inference engine, and this update significantly expands its model coverage to include diffusion models and agentic model like Muse Glimmer. The performance optimizations reduce startup time and lower latency, benefiting AI/ML serving infrastructure. The release adds overlapped checkpoint staging that speeds Qwen3-32B startup on H100 by up to 2.38x, and TP LMHead all-to-all that reduces LMHead time from 320us to 169us on DeepSeek-V4-Pro. The FlashInfer MNNVL pure allreduce mode provides up to +6.9% decode gains on Blackwell. Dependencies were updated to torch 2.13.0, flashinfer 0.6.17, and sgl-kernel 0.4.6.post1.

github · Fridge003 · Aug 22, 00:09

**Background**: SGLang is an open-source inference engine designed for serving large language models and other generative models, focusing on high throughput and low latency. This release continues the project&\#x27;s expansion beyond LLM serving into diffusion models for image and video generation, reflecting the convergence of different generative AI workloads. The project provides a cookbook with deployment recipes for each supported model.

<details><summary>References</summary>
<ul>
<li><a href="https://research.meta.ai/blog/introducing-muse-glimmer-open-agentic-model">Introducing Muse Glimmer: An Open Agentic Model That Runs on Your Device | Meta AI Research</a></li>
<li><a href="https://huggingface.co/Efficient-Large-Model/SANA-Video_2B_480p">Efficient-Large- Model / SANA - Video _2B_480p · Hugging Face</a></li>
<li><a href="https://ltx.io/model/ltx-2-5">LTX - 2 . 5 : LTX&#x27;s Latest AI Open-Source Foundation Model | LTX</a></li>

</ul>
</details>

**Tags**: `#sglang`, `#LLM inference`, `#release`, `#AI/ML`, `#model serving`

---

<a id="item-2"></a>
## [MCP Roadmap: Remote Servers as Standard HTTP, Standardized Agent Identity](https://blog.modelcontextprotocol.io/posts/mcp-roadmap/) ⭐️ 8.0/10

The MCP team published a new roadmap in which, as of the 2026-07-28 release, a remote MCP server is treated as no different from any other HTTP workload. It also outlines plans to standardize how MCP servers recognize and trust agent identities that act on behalf of users. This directly addresses two major community criticisms: MCP&\#x27;s bespoke protocol complexity and its browser-centric authorization model, which fails for cloud agents with their own identity. Standardizing agent identity and treating remote MCP as HTTP could make the protocol easier to adopt and improve security for agentic AI workloads. The roadmap notes that MCP authorization today still requires a person to approve access in a browser, whereas an increasing number of callers are agents running as cloud workloads with their own identity, acting on behalf of an absent user, or delegating narrower authority to sub-agents. These changes are built on existing identity and OAuth-based authorization foundations rather than yet another bespoke standard.

hackernews · pentagrama · Aug 22, 13:31 · [Discussion](https://news.ycombinator.com/item?id=49399591)

**Background**: The Model Context Protocol \(MCP\) is an open standard introduced by Anthropic in November 2024 to standardize how AI systems connect to external data and tools, and it has since been adopted by OpenAI and Google DeepMind. Remote MCP servers have traditionally relied on interactive flows such as OAuth and user consent in a browser, which does not fit agent-to-agent or cloud workloads, prompting the roadmap&\#x27;s push for standardized HTTP deployment and agent identity.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol</a></li>
<li><a href="https://modelcontextprotocol.io/docs/2026-07-28/getting-started/intro">What is the Model Context Protocol (MCP)? - Model Context Protocol</a></li>
<li><a href="https://www.redhat.com/en/blog/mcp-security-implementing-robust-authentication-and-authorization">MCP security: Implementing robust authentication and authorization</a></li>

</ul>
</details>

**Discussion**: Commenters reacted approvingly to the move toward plain HTTP, with one saying introducing a bespoke new protocol was &\#x27;bone-headed.&\#x27; Others remained skeptical, questioning whether many servers will implement the full roadmap, whether MCP endpoints are really easier than REST plus a skills.md file, and citing past pivots and context-hungry features as reasons they abandoned MCP; one commenter joked they still read &\#x27;MCP&\#x27; as &\#x27;Master Control Program.&\#x27;

**Tags**: `#MCP`, `#AI`, `#protocol`, `#roadmap`, `#agent authentication`

---

<a id="item-3"></a>
## [Developer Trains 250M-Param Quantized LLM From Scratch, Deploys in 60 MB](https://www.reddit.com/r/MachineLearning/comments/1vv2nkh/i_developed_my_own_quantized_llm_from_scratch/) ⭐️ 8.0/10

A developer trained a 250M-parameter LLM from scratch on 30B tokens of FineWeb, quantized it to under 2 bits per weight, and achieved a 60 MB deployment that runs at ~400 tokens/sec on a laptop CPU with only 80 MB RAM. The model&\#x27;s long-context system compresses tokens older than 2048 into a 1-bit format stored on disk, supporting retrieval from up to 100M tokens of history. This shows that extremely compact, quantized models can be built from scratch and run efficiently on resource-constrained devices, while still leveraging long contexts through disk offloading. It could advance edge AI applications in privacy-sensitive or low-cost settings, and challenges the assumption that useful LLMs require billions of parameters and large GPUs. Instead of a trained embedding table, the model uses fixed 512-bit codes for each of 131k tokens \(8.4 MB total\), scoring 0.619 Spearman on WordSim-353 versus 0.029 for random codes. The disk cache stores older tokens at ~320 bytes per token \(≈320 MB for 1M tokens\), and the model was trained to retrieve answers from disk history up to 100M tokens but not to reason across them.

reddit · r/MachineLearning · /u/Final-Data-1410 · Aug 22, 04:39

**Background**: Quantization reduces the precision of a model&\#x27;s weights \(e.g., from FP16 to 1-2 bits\) to shrink memory footprint and speed up inference, at the cost of some accuracy. During text generation, LLMs maintain a KV cache of past key-value pairs to avoid recomputing attention; for long contexts this cache becomes very large, motivating techniques like compression and offloading to CPU or disk. FineWeb, a large curated English web-text dataset from Hugging Face, is often used for pretraining small and large models alike. The developer&\#x27;s approach combines these ideas: sub-2-bit quantization, a disk-backed KV cache with 1-bit compression, and a lightweight model trained from scratch.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2511.11907v1">KVSwap: Disk-aware KV Cache Offloading for Long-Context On-device Inference</a></li>
<li><a href="https://lzwjava.github.io/fineweb-overview-usage-en">FineWeb Dataset Overview and Usage</a></li>
<li><a href="https://github.com/pprp/Awesome-LLM-Quantization">GitHub - pprp/Awesome-LLM- Quantization : Awesome list for LLM...</a></li>

</ul>
</details>

**Discussion**: The Reddit thread was overwhelmingly positive; the author noted they expected to be &\#x27;roasted&\#x27; but instead received curious, helpful comments. Users engaged with the technical details, and the GitHub repo gained traction with 7 stars shortly after posting.

**Tags**: `#LLM`, `#quantization`, `#efficient inference`, `#long context`, `#edge AI`

---

<a id="item-4"></a>
## [Open-Source Roguelike DelveRL Bridges Game and RL Agent Training](https://www.reddit.com/r/MachineLearning/comments/1vvii1j/i_built_an_opensource_roguelike_specifically_for/) ⭐️ 8.0/10

A developer released DelveRL, an open-source, human-playable roguelike designed as a reinforcement learning environment. It features a structured API, deterministic simulation, procedural levels, partial observability, and a recurrent PPO trainer, with baseline results reaching a median floor of 18 and extended runs reaching floor 33. This addresses a real gap in reinforcement learning research by providing a game that is both engaging for humans and easy to integrate with agent training harnesses. It could lower the barrier for researchers and hobbyists to experiment with RL in a rich, strategic environment, similar to NetHack but more accessible. The game runs entirely locally with batched renderer-free environments, and includes a recurrent PPO \(LSTM\) baseline. All code, training scripts, checkpoints, bridge documentation, and raw benchmarks are open source.

reddit · r/MachineLearning · /u/SnyderConsulting · Aug 22, 17:32

**Background**: Roguelikes are a game genre featuring procedural level generation and permadeath, where players explore floors, fight enemies, and manage resources. Reinforcement learning \(RL\) trains agents to make sequential decisions through rewards; PPO \(Proximal Policy Optimization\) is a popular algorithm, and recurrent PPO uses LSTM networks to handle partial observability—situations where an agent only perceives a limited view of the environment and must use memory to infer hidden states. DelveRL provides a structured API and deterministic simulation specifically to make integrating such RL agents easier.

<details><summary>References</summary>
<ul>
<li><a href="https://sb3-contrib.readthedocs.io/en/master/modules/ppo_recurrent.html">Recurrent PPO — Stable Baselines3 - Contrib 2.9.0 documentation</a></li>
<li><a href="https://arxiv.org/abs/2204.08967">[2204.08967] When Is Partially Observable Reinforcement Learning Not Scary?</a></li>

</ul>
</details>

**Tags**: `#reinforcement learning`, `#game environment`, `#open-source`, `#AI training`, `#procedural generation`

---

<a id="item-5"></a>
## [SemiAnalysis: Open Models Halve Time to Parity Each Generation](https://newsletter.semianalysis.com/p/are-open-models-catching-up) ⭐️ 8.0/10

SemiAnalysis published a report splitting LLM history into three eras \(early scaling, inference, agentic\) and found that open-source models close the capability gap with closed frontier models faster each generation, with parity time halving per generation. In the agentic era, Kimi K2.6 overtook Opus 4.5 in 4.8 months, and GLM-5.2 surpassed GPT-5.2 in 6 months. The accelerating catch-up suggests the model layer is becoming commoditized, threatening the pricing power of closed labs like Anthropic, which derived over $65 billion in annualized revenue partly from coding and agentic capabilities. For enterprises and developers, this means capable open alternatives may erode the premium for proprietary frontier models. The article cites GLM 5.3 and Kimi K3 as open models now handling many coding and agentic tasks that previously underpinned Anthropic&\#x27;s revenue, but cautions that benchmarks are not everything and Anthropic&\#x27;s productization remains a strength. The measurements represent capability parity on specific tasks, not full feature or experience equivalence.

telegram · zaihuapd · Aug 22, 08:26

**Background**: Large language models have evolved through distinct phases: early scaling of pretraining, the inference era focused on reasoning, and now the agentic era where AI systems perceive, reason, and act autonomously. Open-source models like Kimi K2.6 \(a 1-trillion-parameter Mixture-of-Experts model\) and GLM-5.2 \(744B parameters with a 1M context window\) are posting state-of-the-art results on long-horizon coding and agentic tasks. SemiAnalysis&\#x27;s analysis quantifies how quickly these open models close the gap with proprietary frontier models across these eras.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/moonshotai/Kimi-K2.6">moonshotai/Kimi-K2.6 · Hugging Face</a></li>
<li><a href="https://huggingface.co/zai-org/GLM-5.2">zai-org/GLM-5.2 · Hugging Face</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained | MIT Sloan</a></li>

</ul>
</details>

**Tags**: `#AI`, `#open-source`, `#large-language-models`, `#industry-analysis`, `#model-competition`

---