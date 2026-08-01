---
layout: default
title: "Horizon Summary: 2026-08-01 (EN)"
date: 2026-08-01
lang: en
---

> From 36 items, 5 important content pieces were selected

---

1. [Stateless MCP 2.0 Spec Reignites Interest and Sparks New Tools](#item-1) ⭐️ 9.0/10
2. [Huawei Open-Sources 505B-Parameter MoE Model openPangu-2.0-Pro](#item-2) ⭐️ 9.0/10
3. [DeepSeek V4 Flash 0731: Frontier-Level AI at $0.28 per Million Output Tokens](#item-3) ⭐️ 8.0/10
4. [MiniMax to Open-Source Multimodal Video Model H3 on August 3](#item-4) ⭐️ 8.0/10
5. [German Court Rules AI Music Firm Suno Violated Copyright](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Stateless MCP 2.0 Spec Reignites Interest and Sparks New Tools](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 9.0/10

The 2026-07-28 Model Context Protocol specification \(MCP 2.0\) makes the protocol stateless, replacing the two-request session handshake with a single HTTP call. Simon Willison built three implementations this week, including the open-source mcp-explorer CLI and datasette-mcp. This is the most significant change to MCP since its launch, sharply reducing implementation complexity and making tools easier to audit and control than shell-based agents. It could broaden adoption of MCP for AI agent tooling, especially for smaller models running on laptops. Legacy MCP required two HTTP requests: an initialize call returning a Mcp-Session-Id, followed by a tools/call with that header. The new stateless version uses one POST with MCP-Protocol-Version, Mcp-Method, and Mcp-Name headers, removing the need for server-side session state and session-aware routing.

rss · Simon Willison · Jul 31, 23:13

**Background**: MCP is an open standard introduced by Anthropic in November 2024 to connect AI assistants to external tools and data sources via a standardized interface. It surged in popularity through 2025 but was partly eclipsed by Claude Skills, which teach models how to use tools; this stateless update addresses key scalability and complexity pain points.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>
<li><a href="https://www.arcade.dev/blog/mcp-going-stateless/">MCP Is Going Stateless. Here&#x27;s What That Means - Arcade.dev</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#AI agents`, `#protocol`, `#LLM tools`, `#specification`

---

<a id="item-2"></a>
## [Huawei Open-Sources 505B-Parameter MoE Model openPangu-2.0-Pro](https://huggingface.co/openpangu/openPangu-2.0-Pro) ⭐️ 9.0/10

Huawei has open-sourced openPangu-2.0-Pro on Hugging Face, a 505B-parameter Mixture-of-Experts \(MoE\) language model trained on Ascend NPUs with 340 billion tokens and a 512k context window. Its &\#x27;Thinking&\#x27; variant achieves 95.4 on the AIME 2026 math benchmark and 87.9 on GPQA-Diamond. This release marks a major open-source milestone from a global tech leader, showcasing Huawei&\#x27;s full-stack AI strength spanning NPU hardware, training infrastructure, and model development. It provides a state-of-the-art MoE alternative that could accelerate adoption of Ascend-based AI ecosystems and spur further competition in open-weights LLMs. The architecture combines Multi-head Latent Attention \(MLA\) with a hybrid DSA \(DeepSeek Sparse Attention\) and SWA \(Sliding Window Attention\) layer design, plus a 3-head Multi-Token Prediction \(MTP\) self-speculative decoding module. Post-training involves fast-and-slow unified fine-tuning and multi-task reinforcement learning, with approximately 18B active parameters per token.

telegram · zaihuapd · Jul 31, 06:50

**Background**: MoE models activate only a fraction of their total parameters per token, enabling huge model sizes with manageable inference costs. MLA reduces key-value cache memory by compressing latent representations, while SWA restricts attention to a local window and DSA applies sparse attention patterns for efficiency. MTP allows a model to predict several future tokens simultaneously, which can be leveraged for speculative decoding to speed up generation. Huawei&\#x27;s Ascend NPUs represent a Chinese alternative to Nvidia GPUs for large-scale AI training.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/google-cloud/attention-evolved-how-multi-head-latent-attention-works-427a922dd6a1">Attention Evolved: How Multi - Head Latent Attention Works | Medium</a></li>
<li><a href="https://www.emergentmind.com/topics/sliding-window-attention-fbe25958-222c-4175-aa0e-3ec07d794708">Sliding Window Attention</a></li>
<li><a href="https://www.mox.es/2026/05/10/multi-token-prediction-mtp-how-llms-learn-to-look-ahead/">Multi - Token Prediction ( MTP ): How LLMs Learn to Look Ahead...</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#MoE`, `#Huawei`, `#open-source`, `#AI`

---

<a id="item-3"></a>
## [DeepSeek V4 Flash 0731: Frontier-Level AI at $0.28 per Million Output Tokens](https://artificialanalysis.ai/models/deepseek-v4-flash) ⭐️ 8.0/10

DeepSeek has released DeepSeek-V4-Flash-0731 as an official public-beta build, following additional post-training that improved agentic, coding, and tool-calling abilities. The model reportedly delivers near-frontier intelligence at $0.28 per million output tokens. This release pairs frontier-level benchmark performance with very low API pricing, which could shift expectations for LLM pricing and pressure competitors. It is especially significant for developers and heavy API users who care about token costs. DeepSeek-V4-Flash is a Mixture-of-Experts model with 284B total parameters, 13B activated parameters, and a 1M-token context window. The 0731 build is the official public-beta release that shipped on July 31, 2026, and community users also highlight that a lossless Q8 quantized version is about 162GB, making local deployment feasible.

hackernews · theanonymousone · Jul 31, 07:59 · [Discussion](https://news.ycombinator.com/item?id=49120299)

**Background**: Frontier AI models are the most advanced general-purpose models available at any given time. LLM APIs typically charge separately for input and output tokens, with output tokens typically costing 2-5x more than input tokens. DeepSeek-V4-Flash is a Mixture-of-Experts model designed for efficient reasoning, meaning only a subset of parameters is activated per token.

<details><summary>References</summary>
<ul>
<li><a href="https://ollama.com/library/deepseek-v4-flash">deepseek-v4-flash - ollama.com</a></li>
<li><a href="https://www.orcarouter.ai/blog/deepseek-v4-flash-official-release">DeepSeek V4 Flash: Official Release, Explained - orcarouter.ai</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work | NVIDIA Glossary</a></li>

</ul>
</details>

**Discussion**: Community reaction is largely enthusiastic: users call the model a &\#x27;fantastic&\#x27; daily driver and note it offers roughly GLM 5.2/Gemini 3.6-level intelligence for only $0.28 per million output tokens, including a 162GB Q8 build for local use. Others speculate that an upcoming V4 Pro could match or beat Opus 5, while some question the economics of Hugging Face hosting and whether DeepSeek will also release an optimized coding agent harness.

**Tags**: `#AI/ML`, `#DeepSeek`, `#Model Release`, `#Performance`, `#Pricing`

---

<a id="item-4"></a>
## [MiniMax to Open-Source Multimodal Video Model H3 on August 3](https://modelscope.cn/models/MiniMax/MiniMax-H3) ⭐️ 8.0/10

MiniMax announced that its H3 omni-modal video model will be open-sourced on ModelScope on August 3. H3 natively supports understanding and generation of text, images, audio, and video, producing videos at up to 2K resolution and 15 seconds with native stereo audio. Open-sourcing a state-of-the-art multimodal video model lowers the barrier for developers and creators, potentially accelerating AI-driven video production across film, advertising, e-commerce, and games. It also strengthens the open-source AI ecosystem and intensifies competition with proprietary video-generation models. The model is designed for commercial content creation, with fine-grained editing controls and the ability to combine multiple references into coherent output, including subtitles, brand info, effects, product demos, and UI animations. It is described as an open-weights model, though exact license details have not been fully specified.

telegram · zaihuapd · Jul 31, 12:37

**Background**: ModelScope \(魔搭\) is Alibaba&\#x27;s one-stop model community for exploring, deploying, and training machine learning models. H3 is an omni-modal generation model that jointly understands multimodal contexts across text, images, video, and audio in a single model, enabling tasks like video generation with synchronized audio that would otherwise require multiple separate models.

<details><summary>References</summary>
<ul>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H 3 : An Open Model Breaking the Boundaries Between Tasks...</a></li>
<li><a href="https://fal.ai/minimax-h3">MiniMax H 3 - Open-Weights General-Purpose Multimodal Video Model</a></li>
<li><a href="https://modelscope.ai/">ModelScope</a></li>

</ul>
</details>

**Tags**: `#multimodal`, `#video generation`, `#open source`, `#MiniMax`, `#AI model`

---

<a id="item-5"></a>
## [German Court Rules AI Music Firm Suno Violated Copyright](https://www.dw.com/en/german-court-rules-that-ai-music-firm-suno-violated-copyrights/a-78152227) ⭐️ 8.0/10

Munich Regional Court ruled that AI music company Suno infringed copyright by using protected music to train its models, ordering it to disclose profits and pay unspecified damages. Suno disagreed with the decision and said it will consider all options, including an appeal. This is one of the first major legal rulings specifically addressing AI music generation and could set a global precedent for how copyright law applies to AI training data. The case, brought by Germany&\#x27;s collecting society GEMA, may reshape licensing negotiations between generative AI companies and music rights holders. GEMA filed the lawsuit in January 2025 and demonstrated in court that songs generated by Suno were highly similar to original works. GEMA represents more than 95,000 German musicians and over 2 million rights holders worldwide.

telegram · zaihuapd · Jul 31, 13:11

**Background**: Suno is a generative AI music platform, widely available since December 2023 after launching a web app and partnering with Microsoft to become a Copilot plugin. Generative AI models typically learn by analyzing large datasets of existing works, which has led to disputes over whether such training constitutes copyright infringement or fair use. GEMA is a German collecting society and performance rights organization that licenses and enforces music copyrights for composers, lyricists, and music publishers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Suno_AI">Suno AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/GEMA_%28German_organization%29">GEMA (German organization) - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI`, `#copyright`, `#legal`, `#music`, `#Suno`

---