---
layout: default
title: "Horizon Summary: 2026-07-29 (EN)"
date: 2026-07-29
lang: en
---

> From 41 items, 10 important content pieces were selected

---

1. [AI worms self-propagate through Microsoft Word Copilot](#item-1) ⭐️ 9.0/10
2. [Moonshot AI raises $35B at $350B valuation after Kimi K3 breakthrough](#item-2) ⭐️ 9.0/10
3. [TurboFieldfare: Open-source engine runs Gemma 4 26B in 2GB RAM on M-series Mac](#item-3) ⭐️ 8.0/10
4. [Mitchell Hashimoto Launches Superlogical Company on libghostty](#item-4) ⭐️ 8.0/10
5. [Long policy documents fail to govern AI agents reliably](#item-5) ⭐️ 8.0/10
6. [Matthew Green on Historic Shift to Post-Quantum Crypto](#item-6) ⭐️ 8.0/10
7. [ncnn Vulkan backend enables vendor-agnostic GPU inference on edge](#item-7) ⭐️ 8.0/10
8. [Claude shared chats and Artifacts indexed by Google, Anthropic says by design](#item-8) ⭐️ 8.0/10
9. [Hugging Face widely used for deepfake nude images](#item-9) ⭐️ 8.0/10
10. [China Telecom ends SIM card sales via third-party internet channels](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [AI worms self-propagate through Microsoft Word Copilot](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/) ⭐️ 9.0/10

Researcher Håkon Måløy demonstrated a new prompt injection variant that creates self-replicating AI worms targeting Microsoft Word&\#x27;s Copilot, allowing malicious instructions hidden in documents to autonomously spread to other documents. This discovery reveals a critical security vulnerability in widely used AI assistants, showing that AI worms can exploit agent access to documents and email systems to autonomously propagate, posing significant risks to enterprise data security and user privacy. The attack embeds adversarial self-replicating prompts in externally shared documents; when Copilot processes the document, it follows instructions to alter content and propagate the attack to new documents, effectively creating a computer worm that operates through natural language.

hackernews · Canopy9560 · Jul 29, 11:44 · [Discussion](https://news.ycombinator.com/item?id=49096188)

**Background**: Prompt injection is a cybersecurity exploit where large language models \(LLMs\) are tricked into following malicious instructions hidden in data, because they cannot reliably distinguish between developer-defined prompts and user input. When LLMs are integrated into applications with access to files or emails, they become vulnerable to indirect prompt injection, where adversarial text embedded in retrieved content can command the model to perform unintended actions. This research extends that concept to create self-propagating worms that spread autonomously through document ecosystems.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://thehackernews.com/2026/06/researchers-build-self-replicating-ai.html">Researchers Build Self-Replicating AI Worm That Operates Entirely on Local, Open-Weight Models</a></li>
<li><a href="https://www.infosecurity-magazine.com/news/worm-created-generative-ai-systems/">Self-Propagating Worm Created to Target Generative AI Systems - Infosecurity Magazine</a></li>

</ul>
</details>

**Discussion**: Commenters widely agreed that distinguishing instructions from data is a fundamental unsolved problem for AI safety; one user noted they have uninstalled Copilot and disabled AI locally. Another pointed out that techniques like white text remain effective, and expressed concern that granting agents extensive access will worsen the issue before mitigations appear.

**Tags**: `#AI security`, `#prompt injection`, `#Copilot`, `#worms`, `#Microsoft Word`

---

<a id="item-2"></a>
## [Moonshot AI raises $35B at $350B valuation after Kimi K3 breakthrough](https://www.bloomberg.com/news/articles/2026-07-29/china-s-moonshot-ai-passes-funding-goal-to-hit-35-billion-value) ⭐️ 9.0/10

Moonshot AI has raised $35 billion in a funding round at a $350 billion post-money valuation, far exceeding its initial $1-2 billion target, driven by its Kimi K3 model which approaches frontier performance. The company has also initiated a new round at a $50 billion pre-money valuation and plans a Hong Kong IPO as early as this year. This funding event signals a paradigm shift in Chinese AI capabilities, as Kimi K3&\#x27;s performance approaches that of leading US frontier models, triggering a tech stock selloff and marking another &\#x27;DeepSeek moment&\#x27; for the industry. The massive valuation and planned IPO underscore investor confidence in Chinese AI firms and could intensify global AI competition. Kimi K3 is an open-source model with 2.8 trillion parameters, built on Kimi Delta Attention and Attention Residuals, supporting a 1-million-token context window and native visual understanding. The company&\#x27;s annualized recurring revenue reached $300 million in June, and daily sales have increased at least sixfold since K3&\#x27;s launch.

telegram · zaihuapd · Jul 29, 10:12

**Background**: Moonshot AI is a Chinese artificial intelligence company known for its Kimi series of large language models. The &\#x27;DeepSeek moment&\#x27; refers to the industry shock when DeepSeek, another Chinese AI lab, released its R1 model in early 2025, demonstrating that frontier AI could be achieved with less advanced chips and lower costs, reshaping global AI dynamics.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://www.siliconflow.com/models/kimi-k3">SiliconFlow – AI Infrastructure for LLMs &amp; Multimodal Models</a></li>
<li><a href="https://news.google.com/stories/CAAqNggKIjBDQklTSGpvSmMzUnZjbmt0TXpZd1NoRUtEd2lNMDRITkVSRUl2TF92dzd0MjFDZ0FQAQ?hl=en-IN&amp;gl=IN&amp;ceid=IN:en">Google News - Moonshot AI launches Kimi K 3 model - Overview</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Funding`, `#Moonshot AI`, `#Kimi K3`, `#Chinese AI`

---

<a id="item-3"></a>
## [TurboFieldfare: Open-source engine runs Gemma 4 26B in 2GB RAM on M-series Mac](https://github.com/drumih/turbo-fieldfare) ⭐️ 8.0/10

TurboFieldfare is an open-source inference engine that runs a 4-bit quantized Gemma 4 26B-A4B-IT model on any M-series Mac using only about 2 GB of RAM by streaming routed experts from SSD. It achieves 5–6 tokens per second on an 8 GB M2 MacBook Air and 31–35 tokens per second on an M5 MacBook Pro. This engine makes it possible to run a large Mixture-of-Experts model with 25 billion total parameters on memory-constrained Macs, lowering the barrier for on-device AI. It demonstrates a practical technique for streaming model weights from SSD that could benefit other MoE models and edge devices. The 4-bit quantized model weights occupy about 14 GB, but TurboFieldfare keeps only the shared layers and KV cache in RAM \(approximately 2 GB\), streaming the routed experts for each token from SSD using bounded parallel pread with an expert cache. It also includes an experimental OpenAI-compatible local server supporting streaming, tool calls, and KV cache prefix reuse.

hackernews · gitpusher42 · Jul 29, 15:05 · [Discussion](https://news.ycombinator.com/item?id=49098510)

**Background**: Gemma 4 26B-A4B-IT is a Mixture-of-Experts \(MoE\) model from Google DeepMind, featuring 25.2 billion total parameters but only activating 3.8 billion per token. In MoE models, only a subset of expert layers are active for each input, so the inactive experts can be stored off-chip and streamed on demand. TurboFieldfare exploits this property by storing expert weights on SSD and loading them only when needed, while the shared layers and attention cache remain in RAM.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/tonbistudio/moe-ssd-streaming-windows">GitHub - tonbistudio/ moe - ssd - streaming -windows: Running a 32 GB...</a></li>
<li><a href="https://andrew.ooo/posts/flash-moe-397b-model-macbook-local-inference/">Flash- MoE : Running a 397B Parameter Model on... — andrew.ooo</a></li>
<li><a href="https://openrouter.ai/google/gemma-4-26b-a4b-it:free">Gemma 4 26 B A 4 B (free) - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**Discussion**: The community expressed strong interest, praising the technical achievement and comparing it to llama.cpp&\#x27;s mmap approach. Some users noted that llama.cpp can already run 26B models with 2 GB RAM via mmap, but TurboFieldfare&\#x27;s synchronous SSD reads with inference activity may offer lower latency. A workaround was shared for compiling on older macOS versions, and a developer building DiffusionGemma expressed interest in collaboration.

**Tags**: `#inference engine`, `#Gemma`, `#on-device AI`, `#memory optimization`, `#Swift/Metal`

---

<a id="item-4"></a>
## [Mitchell Hashimoto Launches Superlogical Company on libghostty](https://www.superlogical.com/) ⭐️ 8.0/10

Mitchell Hashimoto announced Superlogical, a company that will build commercial products on top of the open-source libghostty terminal library, which he originally developed for the Ghostty terminal emulator. This move validates the viability of building a business around an open-source library while keeping the core technology MIT-licensed, potentially setting a precedent for sustainable open-source development. It also signals the growing importance of embeddable terminal emulation in modern applications. Mitchell Hashimoto has transferred ownership of the Ghostty project to a non-profit organization, ensuring the terminal emulator remains independent. Superlogical will consume libghostty exactly like any other external consumer, and will upstream shared terminal improvements.

hackernews · yan · Jul 29, 15:41 · [Discussion](https://news.ycombinator.com/item?id=49098965)

**Background**: Mitchell Hashimoto is a well-known software engineer, best known for creating HashiCorp and tools like Vagrant, Terraform, and Consul. Ghostty is a fast, GPU-accelerated terminal emulator that he built from scratch, and libghostty is its embeddable terminal library released under the MIT license. The library allows any application to integrate a modern terminal emulator without writing one from scratch.

<details><summary>References</summary>
<ul>
<li><a href="https://mitchellh.com/writing/libghostty-is-coming">Libghostty Is Coming - Mitchell Hashimoto</a></li>
<li><a href="https://ghostty.org/">Ghostty</a></li>
<li><a href="https://docsmith.aigne.io/docs/ghostty/en/libghostty-ed730d">libghostty API - docsmith.aigne.io</a></li>

</ul>
</details>

**Discussion**: Community members largely praised the open-source strategy, noting that transferring Ghostty to a non-profit ensures sustainability. Some compared libghostty to past component technologies like OLE/COM, and a few criticized the original announcement title as clickbait. Overall sentiment was positive and insightful.

**Tags**: `#open source`, `#terminal`, `#company`, `#libghostty`, `#software engineering`

---

<a id="item-5"></a>
## [Long policy documents fail to govern AI agents reliably](https://arxiv.org/abs/2607.25398) ⭐️ 8.0/10

A new arXiv paper titled &\#x27;Handbook.md&\#x27; demonstrates that lengthy policy documents cannot reliably govern AI agents due to context window limitations and model degradation. This finding challenges the assumption that AI agents can faithfully follow extensive written guidelines, impacting the design of safe and compliant autonomous systems. The paper highlights that even models with 1M-token context windows suffer from degraded performance and instruction forgetting when processing long policy documents.

hackernews · spIrr · Jul 29, 13:01 · [Discussion](https://news.ycombinator.com/item?id=49096969)

**Background**: Large language models \(LLMs\) have a limited context window, which is the amount of text they can process at once. As context length increases, models often experience context degradation, where earlier parts of the input are forgotten or mishandled. This is particularly problematic for AI agents that are expected to follow long policy documents consistently.

<details><summary>References</summary>
<ul>
<li><a href="https://www.geeksforgeeks.org/artificial-intelligence/tokens-and-context-windows-in-llms/">Tokens and Context Windows in LLMs - GeeksforGeeks</a></li>
<li><a href="https://www.emergentmind.com/topics/context-degradation-in-llms">Context Degradation in LLMs</a></li>

</ul>
</details>

**Discussion**: Commenters noted similar issues in practice, with users reporting that Claude ignores CLAUDE.md instructions after a short period, and that explicit in-prompt reminders work better. Some argued that true agentic behavior requires extensive post-training on specific datasets rather than relying on context alone.

**Tags**: `#AI agents`, `#long context`, `#LLM limitations`, `#policy compliance`, `#benchmark`

---

<a id="item-6"></a>
## [Matthew Green on Historic Shift to Post-Quantum Crypto](https://simonwillison.net/2026/Jul/29/matthew-green/#atom-everything) ⭐️ 8.0/10

Matthew Green highlighted that we are in a historic transition from traditional public-key algorithms to post-quantum algorithms, and suggested that AI could improve cryptanalysis during this period. This commentary is timely because the security community is actively standardizing post-quantum schemes like HAWK, and AI-driven cryptanalysis could either validate or undermine these new algorithms, significantly impacting future cryptography. Green references Impagliazzo&\#x27;s Minicrypt concept, where public-key cryptography does not exist, as a possible scenario if AI breaks all hard problems; he also notes that standards like HAWK are being considered, which are lattice-based post-quantum signature schemes.

rss · Simon Willison · Jul 29, 18:18

**Background**: Post-quantum cryptography aims to develop cryptographic algorithms resistant to quantum computers. Traditional algorithms like RSA and ECC are vulnerable to Shor&\#x27;s algorithm. NIST is standardizing post-quantum schemes, and HAWK is a lattice-based signature candidate. Impagliazzo&\#x27;s Five Worlds classify cryptographic possibilities; Minicrypt assumes only one-way functions exist, not public-key crypto.

<details><summary>References</summary>
<ul>
<li><a href="https://eprint.iacr.org/2026/1078">Post-Quantum HAWK Signature Acceleration with RISC-V-Based Hardware-Software Co-Design</a></li>
<li><a href="https://blog.computationalcomplexity.org/2004/06/impagliazzos-five-worlds.html">Computational Complexity: Impagliazzo&#x27;s Five Worlds</a></li>
<li><a href="https://blog.cloudflare.com/another-look-at-pq-signatures/">A look at the latest post-quantum signature standardization candidates | The Cloudflare Blog</a></li>

</ul>
</details>

**Tags**: `#cryptography`, `#post-quantum`, `#AI`, `#cryptanalysis`, `#security`

---

<a id="item-7"></a>
## [ncnn Vulkan backend enables vendor-agnostic GPU inference on edge](https://www.reddit.com/r/MachineLearning/comments/1v9s4mz/vendoragnostic_ml_inference_on_production_edge/) ⭐️ 8.0/10

The PostSlate team achieved vendor-agnostic GPU-accelerated ML inference on production edge devices using ncnn&\#x27;s Vulkan backend, obtaining ~10x speedups over ONNX CPU inference for face detection and embedding models. This approach eliminates dependency on vendor-specific runtimes like CUDA, enabling a single inference backend to run across all GPU vendors \(NVIDIA, AMD, Intel, Apple Silicon\), which is critical for cross-platform edge deployment. Performance numbers on an NVIDIA 4070 show ArcFace R50 face embedding dropping from 30 ms \(ONNX CPU\) to 3 ms \(ncnn Vulkan\), and SCRFD face detection from 25 ms to 2.5 ms, with model size halved due to fp16 weight storage.

reddit · r/MachineLearning · /u/ppchaos · Jul 29, 10:22

**Background**: ncnn is a high-performance neural network inference framework developed by Tencent, optimized for mobile and embedded deployment. Vulkan is a cross-platform graphics and compute API that provides low-level GPU access across vendors. ONNX is an open format for representing machine learning models, commonly used for interoperability between frameworks. Many edge devices lack CUDA support, making vendor-agnostic GPU inference challenging.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Tencent/ncnn">GitHub - Tencent/ ncnn : ncnn is a high-performance neural network...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vulkan">Vulkan - Wikipedia</a></li>
<li><a href="https://formats.jarhalab.com/formats/onnx">ONNX Model Format . onnx Format | File Formats</a></li>

</ul>
</details>

**Tags**: `#ML Inference`, `#Vulkan`, `#Edge Computing`, `#ncnn`, `#Vendor-agnostic`

---

<a id="item-8"></a>
## [Claude shared chats and Artifacts indexed by Google, Anthropic says by design](https://thenextweb.com/news/claude-shared-chats-artifacts-google-search-indexed) ⭐️ 8.0/10

Over the weekend, shared conversation and Artifacts links created by Claude users were indexed by Google, exposing sensitive information such as medical records and company documents. Anthropic stated that the system was not breached and that shared links are user-generated and designed to be public. This incident highlights persistent privacy vulnerabilities in AI chat features where user-shared content can be publicly accessed, eroding user trust. It follows similar incidents with Claude, ChatGPT, and Grok, underscoring a systemic issue in the industry. Anthropic has prevented new indexing as of Monday afternoon, but previously indexed links remain accessible. Users can revoke shared links in their settings, but already exposed data may persist in search caches.

telegram · zaihuapd · Jul 29, 02:40

**Background**: Claude&\#x27;s shared chat feature allows users to create publicly accessible links to their conversations or Artifacts—interactive code previews and apps generated by Claude. These links are intended for sharing but are not automatically private; if posted on public platforms, search engines can index them. Artifacts are a feature that generates shareable standalone content like tools or visualizations.

<details><summary>References</summary>
<ul>
<li><a href="https://support.claude.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them">What are artifacts and how do I use them? | Claude Help Center</a></li>
<li><a href="https://grokipedia.com/page/Claude_Artifacts">Claude Artifacts</a></li>

</ul>
</details>

**Tags**: `#隐私安全`, `#Claude`, `#数据泄露`, `#谷歌索引`

---

<a id="item-9"></a>
## [Hugging Face widely used for deepfake nude images](https://www.theverge.com/ai-artificial-intelligence/971723/hugging-face-nudify-deepfake-undress-women-children) ⭐️ 8.0/10

A report by AI Forensics found that Hugging Face is widely used to generate non-consensual deepfake nude images, with 73% of 1,000+ requests in a honeypot being sex-related and 7% targeting children, and the platform lacks effective safeguards. This highlights a serious gap in platform responsibility for AI safety, as a leading open-source model hub enables harmful content generation with minimal moderation, affecting victims and potentially undermining trust in AI platforms. The researchers set up a honeypot that received over 1,000 requests in seven days, and the top nine image editing models on Hugging Face could easily undress women with simple prompts without any jailbreaking.

telegram · zaihuapd · Jul 29, 08:20

**Background**: Hugging Face is a popular platform where machine learning models and datasets are shared. A honeypot is a decoy system used to detect and analyze malicious activity. The report indicates that Hugging Face&\#x27;s content policies are not effectively enforced, as models can be used to generate prohibited content.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Hugging_Face">Hugging Face</a></li>
<li><a href="https://en.wikipedia.org/wiki/Honeypot_%28computing%29">Honeypot (computing)</a></li>

</ul>
</details>

**Tags**: `#AI ethics`, `#deepfakes`, `#Hugging Face`, `#content moderation`, `#AI safety`

---

<a id="item-10"></a>
## [China Telecom ends SIM card sales via third-party internet channels](https://www.189.cn/web/notice/detail?order=1&amp;amp;offerCode=519526800001&amp;amp;provinceCode=600304) ⭐️ 8.0/10

China Telecom posted a notice on its official website dated July 31 stating that starting August 1, third-party internet channels will no longer be allowed to sell its SIM cards. This policy change directly affects how consumers purchase China Telecom SIM cards online, restricting availability to official channels only and potentially increasing costs or reducing convenience for customers. An additional notice with a July 29 date and a different provinceCode parameter was also found. The ban applies to all third-party internet platforms, including e-commerce sites and online resellers.

telegram · zaihuapd · Jul 29, 12:45

**Background**: China Telecom is one of the three major state-owned telecom operators in China, providing mobile and broadband services. Third-party internet channels have been a common way for customers to purchase SIM cards online, often offering competitive prices and promotions.

**Tags**: `#China Telecom`, `#telecom policy`, `#SIM card`, `#Internet channels`, `#China`

---