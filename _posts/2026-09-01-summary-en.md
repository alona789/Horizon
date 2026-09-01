---
layout: default
title: "Horizon Summary: 2026-09-01 (EN)"
date: 2026-09-01
lang: en
---

> From 37 items, 7 important content pieces were selected

---

1. [Tim Cook Steps Down as Apple CEO; John Ternus Takes Over with AI Focus](#item-1) ⭐️ 9.0/10
2. [Google Removes Manifest V2 Extensions from Chrome Web Store, Including uBlock Origin](#item-2) ⭐️ 8.0/10
3. [NAT: the &\#x27;original sin&\#x27; pushing Internet toward centralization](#item-3) ⭐️ 8.0/10
4. [Sliding-window attention beats linear attention on long-context benchmarks](#item-4) ⭐️ 8.0/10
5. [SynthFin-AML Dataset Exposes Temporal Leakage in GNN Anti-Money Laundering Models](#item-5) ⭐️ 8.0/10
6. [OpenClaw 2.0 Delivers Largest Update with Over 16,000 Pull Requests](#item-6) ⭐️ 8.0/10
7. [DeepSeek Releases Experimental Multimodal Model V4-Flash-Vision-Exp](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Tim Cook Steps Down as Apple CEO; John Ternus Takes Over with AI Focus](https://www.bloomberg.com/news/articles/2026-08-30/apple-s-new-ceo-john-ternus-takes-reins-from-tim-cook-focusing-on-ai) ⭐️ 9.0/10

Tim Cook&\#x27;s final day as Apple CEO was August 31, 2026; John Ternus, a 51-year-old hardware engineering veteran, took over on September 1. Ternus&\#x27;s top priority is accelerating Apple&\#x27;s AI push, especially after delays to Siri upgrades, and the first foldable iPhone is expected at the September 9 event. A CEO transition at Apple is a rare, industry-shaping event because Apple is one of the world&\#x27;s most influential technology companies. The explicit strategic shift toward AI, coupled with a new foldable iPhone, will ripple across the smartphone and AI industries. The foldable iPhone is said to come with 12 GB RAM and deep Siri AI integration, letting Siri understand real-world scenes using the screen, calendar, and camera. Tim Cook will remain as executive chairman rather than leaving the company entirely.

telegram · zaihuapd · Aug 31, 10:21

**Background**: Tim Cook had been Apple&\#x27;s CEO for over a decade, succeeding Steve Jobs. Apple Intelligence, introduced in 2024, is Apple&\#x27;s AI feature suite that combines on-device and server processing, and includes tools like writing assistance, notification summaries, and ChatGPT integration; Siri is the company&\#x27;s voice assistant now being upgraded with these AI capabilities. The new CEO&\#x27;s hardware background suggests a focus on shipping AI-powered devices.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence</a></li>
<li><a href="https://www.apple.com/apple-intelligence/">Apple Intelligence and Siri - Apple</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#CEO transition`, `#AI`, `#Tim Cook`, `#John Ternus`

---

<a id="item-2"></a>
## [Google Removes Manifest V2 Extensions from Chrome Web Store, Including uBlock Origin](https://webiterate.dev/google-removed-extensions-ublock-origin-108/) ⭐️ 8.0/10

Google has removed all remaining Manifest V2 \(MV2\) extensions from the Chrome Web Store, including the popular ad blocker uBlock Origin. The removal follows the final deprecation of MV2 support in Chrome 151, which deleted the last MV2 code from the browser&\#x27;s source tree. This change affects millions of users who rely on uBlock Origin for ad-blocking and privacy protection. It also raises broader concerns about a single company exercising unilateral control over browser extensions and web standards, prompting many users to consider switching to Firefox. Manifest V3 was introduced by Google with claims of improved security, privacy, and performance, but it restricts ad-blocking extensions by replacing the webRequest API with declarativeNetRequest, which limits filter rulesets. Firefox continues to support uBlock Origin&\#x27;s full capabilities, and the extension&\#x27;s developer notes that uBlock Origin works best on Firefox.

hackernews · twapi · Aug 31, 21:10 · [Discussion](https://news.ycombinator.com/item?id=49514878)

**Background**: Manifest V2 and Manifest V3 are versions of the manifest file \(manifest.json\) that defines browser extensions&\#x27; capabilities and permissions. Google has been migrating Chrome to MV3 since the specification was announced, arguing it improves security by preventing extensions from executing remotely hosted code. The deprecation timeline saw the Chrome Web Store remove MV2 extensions in waves, with all remaining ones removed by August 31, 2026. uBlock Origin is a free, open-source content blocker widely regarded as efficient and user-friendly, available on both Firefox and Chromium-based browsers.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline">Manifest V 2 support timeline | Chrome for Developers</a></li>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3">Extensions / Manifest V3 | Chrome for Developers</a></li>
<li><a href="https://en.wikipedia.org/wiki/UBlock_Origin">uBlock Origin - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters expressed strong concerns, arguing ad-blocking is now a safety issue for less technical users and that Google and other companies failed to filter malicious ads themselves. Many users report they have already switched to Firefox, with one commenter noting uBlock Origin works best on Firefox, reflecting a broader distrust of Chrome&\#x27;s unilateral control.

**Tags**: `#Chrome`, `#Manifest V3`, `#privacy`, `#ad-blocking`, `#browser extensions`

---

<a id="item-3"></a>
## [NAT: the &\#x27;original sin&\#x27; pushing Internet toward centralization](https://dreamstation.systems/personal/ntppost.html) ⭐️ 8.0/10

An essay argues that Network Address Translation \(NAT\) is one of the earliest contributors to Internet centralization, and it sparked a deep community discussion, including a reflective comment from Rusty Russell, who implemented the current NAT system in Linux. The article frames NAT&\#x27;s address-conservation trade-offs as a historical turning point that made self-hosting and direct peer-to-peer connections harder for everyday users. This matters because NAT&\#x27;s design choices shaped the modern Internet: they accelerated the client-server model, normalized the idea that devices must talk to &\#x27;the cloud&\#x27; rather than each other, and created a market for NAT traversal and cloud relay services. The debate also resurfaces around IPv6 adoption, carrier-grade NAT, and proposals to return end-to-end connectivity to users. Rusty Russell, the Linux NAT implementer, says his port-allocation choice avoided port reservation to squeeze more connections per IP, but as a result incoming traffic from a different remote address is unroutable, leaving users without a public endpoint — a &\#x27;poor man&\#x27;s firewall&\#x27;. Commenters also distinguish ordinary home NAT \(fixable with port forwarding/UPnP\) from carrier-grade NAT, which they call a genuinely freedom-restricting technology.

hackernews · robinpie · Aug 31, 02:23 · [Discussion](https://news.ycombinator.com/item?id=49504905)

**Background**: Network Address Translation \(NAT\) lets multiple devices on a private network share one public IP address by rewriting IP addresses and ports as packets pass through a router. NAT was developed to slow the exhaustion of IPv4 addresses and also gives a basic layer of security by hiding internal hosts. Because NAT breaks the old end-to-end model of the Internet, techniques such as STUN, TURN, and ICE were created to let applications discover and traverse NAT mappings for peer-to-peer connections.

<details><summary>References</summary>
<ul>
<li><a href="https://www.geeksforgeeks.org/computer-networks/network-address-translation-nat/">Network Address Translation ( NAT ) - GeeksforGeeks</a></li>
<li><a href="https://en.wikipedia.org/wiki/NAT_traversal">NAT traversal - Wikipedia</a></li>
<li><a href="https://liveapi.com/blog/nat-traversal/">What Is NAT Traversal ? STUN , TURN , ICE Explained - LiveAPI Blog</a></li>

</ul>
</details>

**Discussion**: Comments span a wide spectrum: Rusty Russell offers a candid apology for his youthful implementation choices; solatic mourns the loss of the &\#x27;open Internet&\#x27; and argues NAT taught everyone to see client-server as natural; elric pushes back, saying ordinary NAT is fine and only CGNAT truly restricts freedom; and miki123211 claims the root mistake was applying real-world, meatspace norms to cyberspace.

**Tags**: `#NAT`, `#networking`, `#Internet history`, `#centralization`, `#infrastructure`

---

<a id="item-4"></a>
## [Sliding-window attention beats linear attention on long-context benchmarks](https://www.reddit.com/r/MachineLearning/comments/1w3j1vw/slidingwindow_attention_beats_linear_on/) ⭐️ 8.0/10

A new arXiv preprint \(2608.28444\) reports that sliding-window attention with sinks achieves 2 to 10 times higher performance than post-trained linear attention variants on the Needle-in-a-Haystack and BABILong long-context reasoning benchmarks. The authors recommend switching to SWA instead of post-training linear models. This challenges a major line of efficient-attention research, suggesting that simpler, already-existing baselines have been under-evaluated. If validated, it could redirect LLM architecture choices and save substantial post-training compute. Sliding-window attention with sinks requires no post-training, runs fast, and keeps memory low, according to the paper. The reported gaps are large on the two selected tasks, but the findings come from a single preprint and need independent validation.

reddit · r/MachineLearning · /u/Justgototheeffinmoon · Aug 31, 16:35

**Background**: Standard transformer attention has quadratic cost in sequence length, which makes long contexts expensive. Linear attention aims to reduce this to linear scaling, but often requires post-training to match quality. Sliding-window attention \(SWA\) restricts each token to attend only to nearby tokens within a fixed window, lowering cost; adding &\#x27;sinks&\#x27; \(special tokens that absorb extra attention\) helps preserve global information. BABILong is a benchmark that tests long-context reasoning with tasks such as multi-hop question answering over long documents.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.28444">[2608.28444] Sliding-window beats linear attention</a></li>
<li><a href="https://www.digitalocean.com/community/tutorials/sliding-window-attention-efficient-long-context-models">Sliding Window Attention: Efficient Long-Context Modeling | DigitalOcean</a></li>
<li><a href="https://github.com/booydar/babilong">GitHub - booydar/ babilong : BABILong is a benchmark for LLM...</a></li>

</ul>
</details>

**Tags**: `#attention mechanisms`, `#long-context reasoning`, `#linear attention`, `#LLMs`, `#efficiency`

---

<a id="item-5"></a>
## [SynthFin-AML Dataset Exposes Temporal Leakage in GNN Anti-Money Laundering Models](https://www.reddit.com/r/MachineLearning/comments/1w3imxy/your_gnn_is_probably_just_an_overcomplicated_mlp/) ⭐️ 8.0/10

The post introduces SynthFin-AML v10.0, a synthetic financial graph dataset with 100k nodes and 1.2M edges that enforces strict 3-snapshot causal splits to prevent temporal leakage in GNN training. The authors benchmarked tuned LightGBM against GraphSAGE, reporting PR-AUC of 0.848 versus 0.881 under the strict temporal split. This matters because it exposes a critical evaluation flaw: many GNN models on dynamic graphs may be overcomplicated MLPs that cheat by seeing future edges during training. By providing a concrete dataset and evaluation standard, it pushes the graph machine learning community toward more reliable benchmarks, especially for anti-money laundering and other time-sensitive applications. The dataset enforces a strict 3-snapshot point-in-time split: train graph uses edges up to Day 7, validation up to Day 8, and test up to Day 10, physically disjointing temporal windows to bound the GNN receptive field. It also removes tabular leakage by making fraud and retail transaction amounts share the same lognormal distribution \(μ=8.517, σ=0.8\). The authors have submitted the benchmark upstream to PyTorch Geometric as PR \#10774.

reddit · r/MachineLearning · /u/Glabmayt2075 · Aug 31, 16:21

**Background**: Temporal leakage in graph neural networks occurs when a GNN trained on a static snapshot of a dynamic graph can see future edges, features, or events during training, inflating performance. Standard random transductive splits fundamentally fail on financial transaction networks because they violate the arrow of time. Dynamic graph benchmarks require time-aware evaluation methods, such as causal splits, to ensure models learn genuine patterns rather than memorizing future information. SynthFin-AML builds on prior synthetic AML datasets, which are used to benchmark statistical and machine learning methods while preserving privacy.

<details><summary>References</summary>
<ul>
<li><a href="https://kumo.ai/pyg/concepts/data-leakage/">Data Leakage in Graph ML: When Future Information Contaminates Training | Kumo.ai | Kumo.ai</a></li>
<li><a href="https://kumo.ai/pyg/concepts/temporal-graph/">Temporal Graphs in PyG: Time-Evolving Graph Neural Networks | Kumo.ai | Kumo.ai</a></li>

</ul>
</details>

**Tags**: `#graph neural networks`, `#temporal leakage`, `#dataset`, `#anti-money laundering`, `#evaluation methodology`

---

<a id="item-6"></a>
## [OpenClaw 2.0 Delivers Largest Update with Over 16,000 Pull Requests](https://openclaw.ai/blog/openclaw-2-accidentally) ⭐️ 8.0/10

OpenClaw released version 2.0 on August 30, its largest update ever, incorporating over 16,000 pull requests from 933 contributors, including 569 first-time contributors. The release overhauls installation, messaging, memory, skills, models, browser, plugins, and security, and adds shared cloud sessions for collaborative use. This release marks a major milestone for the open-source AI assistant ecosystem, showcasing community-driven development at an extraordinary scale. The comprehensive updates could significantly improve usability and attract a broader user base. The team intentionally skipped nearly seven weeks of releases to prepare this update. It simplifies the installation process, rebuilds the browser experience, and introduces shared cloud sessions for multi-user collaboration.

telegram · zaihuapd · Aug 31, 04:38

**Background**: OpenClaw is a free, open-source autonomous AI agent that executes tasks via large language models, using messaging platforms as its main user interface. The project has attracted a large and active community; the 16,000 pull requests in this release account for about half of the project&\#x27;s total pull requests to date.

<details><summary>References</summary>
<ul>
<li><a href="https://openclaw.ai/">OpenClaw — Open -Source AI Assistant</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenClaw">OpenClaw</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#software-release`, `#AI-assistant`, `#development`, `#community`

---

<a id="item-7"></a>
## [DeepSeek Releases Experimental Multimodal Model V4-Flash-Vision-Exp](https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-Vision-Exp) ⭐️ 8.0/10

DeepSeek has released DeepSeek-V4-Flash-Vision-Exp, the first experimental multimodal model in the V4 series, adding a vision module to the V4-Flash architecture and continuing training. This version significantly improves multimodal agent performance, with ApexBench rising from 26.2 to 36.5, while text agent tasks remain roughly unchanged. This release signals DeepSeek&\#x27;s push into multimodal agent capabilities and open-weight research, giving the community access to a strong vision-language model for experimentation. It also demonstrates meaningful gains on agent-focused benchmarks, which are increasingly important as AI systems expand beyond chatbots into tool-use and autonomous workflows. The model is experimental and builds on the V4-Flash architecture, so it may not represent the full capabilities of the upcoming V4 stable release. Its benchmark improvements are concentrated in multimodal agent tasks: ApexBench \(Pass@1\) climbed from 26.2 to 36.5, while text-only agent performance stayed essentially flat, indicating the vision module is the main differentiator.

telegram · zaihuapd · Aug 31, 11:41

**Background**: Open weights means the trained numerical parameters of a model are publicly available, allowing anyone to download and run it, though it does not necessarily include the full training code and data. Multimodal agents are AI systems that integrate vision, audio, and text to understand and act on rich, real-world inputs, representing a shift beyond text-only interfaces. ApexBench is a multimodal agent benchmark that reports Pass@1 scores and is used to evaluate how well models can complete agentic tasks with visual and textual information. DeepSeek is a leading AI lab known for releasing capable models with open weights, and this experimental vision model is part of its V4 series.

<details><summary>References</summary>
<ul>
<li><a href="https://www.datalearner.com/en/benchmarks/apexbench">ApexBench : Multimodal Agent Benchmark and... | DataLearnerAI</a></li>
<li><a href="https://www.ai21.com/glossary/foundational-llm/open-weights-model/">What is an Open - Weights Model ? | AI21</a></li>
<li><a href="https://fast.io/resources/ai-agent-multimodal-processing/">AI Agent Multimodal Processing: The 2026 Guide | Fastio</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#multimodal`, `#AI model release`, `#open weights`, `#agent`

---