---
layout: default
title: "Horizon Summary: 2026-08-13 (EN)"
date: 2026-08-13
lang: en
---

> From 34 items, 9 important content pieces were selected

---

1. [Google launches Gemini 3.7 Flash, efficient workhorse AI model](#item-1) ⭐️ 9.0/10
2. [DRAM Controller Hack &\#x27;Spaghettifies&\#x27; Memory to Expose Hidden CPU Regions](#item-2) ⭐️ 9.0/10
3. [DeepMind SL2T Brings Sign Language-to-Text to Pixel 11](#item-3) ⭐️ 9.0/10
4. [DeepSeek-V4-Pro Officially Launches with Peak/Off-Peak API Pricing](#item-4) ⭐️ 9.0/10
5. [Cerebras and OpenAI Launch GPT-5.6 Sol Ultrafast, 7x Faster on HLE](#item-5) ⭐️ 8.0/10
6. [DeepSeek Harness: Open-Source Agent Harness Developer Preview](#item-6) ⭐️ 8.0/10
7. [Choose Boring Technology: Conserve Innovation Tokens for Real Problems](#item-7) ⭐️ 8.0/10
8. [Worldproof tool shows pixel metrics often can&\#x27;t rank world models](#item-8) ⭐️ 8.0/10
9. [Trump signs memo letting private firms conduct US-backed overseas cyber attacks](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google launches Gemini 3.7 Flash, efficient workhorse AI model](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/) ⭐️ 9.0/10

Google has released Gemini 3.7 Flash, a new efficient AI model for high-volume, low-cost use cases. Community hands-on tests show strong vision-to-HTML performance, while pricing drew mixed reactions. Gemini 3.7 Flash improves the workhorse tier of Google&\#x27;s model lineup, making advanced multimodal reasoning more accessible and affordable. It strengthens Google&\#x27;s position in the competitive AI model market as rivals like OpenAI&\#x27;s Luna offer aggressive pricing. Google reports 3.7 Flash significantly outperforms 3.6 Flash on complex-document understanding \(GDP.pdf: 34.0% vs 22.0%\) and business workflow automation \(AutomationBench: 30.4% vs 17.0%\). Community comments note an introductory price that is scheduled to increase, creating uncertainty about long-term cost.

hackernews · thisisauserid · Aug 13, 17:23 · [Discussion](https://news.ycombinator.com/item?id=49289112)

**Background**: Gemini is Google DeepMind&\#x27;s family of multimodal large language models, with Flash models designed as efficient, low-latency variants for high-volume tasks. Vision-to-HTML is a common benchmark where an AI converts images or screenshots into working HTML code, testing both visual understanding and code generation. The new 3.7 Flash is also being used with tools like Nano Banana and Gemini Omni to generate interactive pages and games.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-3-7-flash/">Gemini 3.7 Flash: our most intelligent workhorse model</a></li>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3.7 Flash — Google DeepMind</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gemini_2.5_Flash_Image">Gemini 2.5 Flash Image</a></li>

</ul>
</details>

**Discussion**: Commenters provided hands-on evaluations: one user found Opus 5 still best-in-class for image-to-HTML but noted Gemini 3.7 does well for its price, while another tested SVG rendering and criticized the odd pricing schedule. Several commenters argued that OpenAI&\#x27;s Luna is much cheaper and more powerful, questioning whether Flash is still needed. Overall sentiment is mixed, with enthusiasm for the model&\#x27;s vision abilities tempered by pricing and competition concerns.

**Tags**: `#AI`, `#Google`, `#Gemini`, `#LLM`, `#Machine Learning`

---

<a id="item-2"></a>
## [DRAM Controller Hack &\#x27;Spaghettifies&\#x27; Memory to Expose Hidden CPU Regions](https://github.com/xoreaxeaxeax/skitter-creek-bath-salts) ⭐️ 9.0/10

Security researcher Christopher Domas has released &\#x27;skitter-creek-bath-salts,&\#x27; a tool that manipulates the DRAM controller&\#x27;s physical address translation to remap memory, enabling access to hidden CPU regions such as the Platform Security Processor, System Management Mode, and microcode. The technique was demonstrated on AMD Family 16h \(Jaguar\) CPUs. This attack bypasses all higher-level software protections, giving ring-0 root access to deeply hidden hardware secrets that were previously considered unreachable. It has major implications for hardware security, particularly for game consoles like Xbox and PlayStation, whose security groups may now be concerned. The exploit flips a single bit in the memory controller&\#x27;s base address to scramble physical DRAM address translations, and uses linear algebra to reconstruct the mapping. Besides AMD Jaguar, the README notes that Zen 3 has a different base address for memory controller registers, and it remains unclear which other modern CPUs are affected.

hackernews · matt\_d · Aug 13, 14:17 · [Discussion](https://news.ycombinator.com/item?id=49286341)

**Background**: DRAM address mapping is a complex process in which the memory controller translates physical addresses to specific rows, columns, banks, and channels of memory chips. Prior research, such as the USENIX Security 2016 paper &\#x27;DRAMA: Exploiting DRAM Addressing for Cross-CPU Attacks,&\#x27; already demonstrated that these mappings can be leaked and exploited. The new work goes further by directly manipulating the controller to unlock hidden processor regions that even the operating system normally cannot see.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/xoreaxeaxeax/skitter-creek-bath-salts">Spaghettifying DRAM</a></li>
<li><a href="https://zeli.app/en/story/49286341">Spaghettifying DRAM: Unlock Everything on the CPU | Zeli</a></li>

</ul>
</details>

**Discussion**: Commenters are highly enthusiastic, with many praising Christopher Domas&\#x27;s presentation style and eagerly awaiting the Black Hat talk. Some question which newer CPUs are affected beyond AMD Jaguar, while others note the growing complexity of DRAM as a large attack surface and suggest Xbox and PlayStation security teams may be worried.

**Tags**: `#security`, `#DRAM`, `#hardware hacking`, `#exploitation`, `#reverse engineering`

---

<a id="item-3"></a>
## [DeepMind SL2T Brings Sign Language-to-Text to Pixel 11](https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/) ⭐️ 9.0/10

Google DeepMind has released SL2T, a large-scale multilingual sign language-to-text model, and deployed it in consumer products for the first time. It now powers sign language-to-English translation in Pixel 11&\#x27;s Gboard and Live Transcribe, with more devices and languages planned. This marks the first time a sign language AI translation model has shipped in a mainstream consumer device, significantly expanding accessibility for Deaf and hard of hearing users. It demonstrates that large-scale multilingual sign language translation can be practical, privacy-preserving, and commercially viable. SL2T was trained on over 100,000 hours of sign language video spanning 50+ languages, and achieves a zero-shot score of 70 BLEURT on the FLEURS-ASL benchmark, far above previous records. To protect privacy, it processes only hand and body pose keypoints rather than raw video.

telegram · zaihuapd · Aug 13, 08:55

**Background**: SL2T is a sign-language-to-text translation model that lets Deaf users sign to their phone to type messages, search, or communicate without a keyboard. FLEURS-ASL is an extension of the FLORES/FLEURS multiway parallel benchmarks to American Sign Language, used to evaluate sign language translation. BLEURT is a learned evaluation metric for natural language generation that measures how well a candidate sentence conveys the meaning of a reference. Google&\#x27;s claim of a 70 BLEURT zero-shot score indicates strong semantic fidelity even on unseen sign language data.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/putting-sign-language-ai-into-users-hands/">Putting sign language AI into users’ hands — Google DeepMind</a></li>
<li><a href="https://arxiv.org/html/2408.13585">FLEURS - ASL : Including American Sign Language in Massively...</a></li>
<li><a href="https://github.com/google-research/bleurt">GitHub - google-research/bleurt: BLEURT is a metric for Natural Language Generation based on transfer learning. · GitHub</a></li>

</ul>
</details>

**Tags**: `#sign language`, `#machine translation`, `#accessibility`, `#Google DeepMind`, `#AI`

---

<a id="item-4"></a>
## [DeepSeek-V4-Pro Officially Launches with Peak/Off-Peak API Pricing](https://api-docs.deepseek.com/zh-cn/updates) ⭐️ 9.0/10

DeepSeek has released the official version of DeepSeek-V4-Pro, now available on the DeepSeek app, web, and API under the model name deepseek-v4-pro. The release adds stronger agent capabilities, native Responses API support for Codex compatibility, and three new thinking levels \(low, high, max\) for both V4-Pro and V4-Flash. DeepSeek is one of the most widely used open-weight model families, so this release affects a large developer base that builds on its API and self-hosted weights. Peak/off-peak billing could meaningfully lower costs for batch or background workloads, while Responses API support removes friction for developers using Codex and OpenAI-compatible tooling. The new pricing takes effect at 00:00 on August 17, 2026, with off-peak rates set at 50% of peak rates. Open weights for DeepSeek-V4-Pro-0813 are also available on Hugging Face \(1.7T parameters, ~893 GB\), and the model is listed on OpenRouter as deepseek/deepseek-v4-pro-0813.

telegram · zaihuapd · Aug 13, 11:12

**Background**: DeepSeek-V4-Pro is the flagship of DeepSeek&\#x27;s V4 series, a Mixture-of-Experts large language model designed for strong reasoning over a 1M-token context window. The Responses API is an OpenAI-compatible interface that many developer tools support; adding native support means Codex and similar clients can call the model without extra translation layers. Thinking modes adjust how much chain-of-thought the model computes before answering, letting developers trade latency and cost for answer quality. Peak/off-peak pricing charges less for usage outside busy hours, giving cost-conscious developers an incentive to schedule heavy jobs at night.

<details><summary>References</summary>
<ul>
<li><a href="https://api-docs.deepseek.com/guides/responses_api/">Using the Responses API | DeepSeek API Docs</a></li>
<li><a href="https://api-docs.deepseek.com/guides/thinking_mode/">Thinking Mode | DeepSeek API Docs</a></li>
<li><a href="https://api-docs.deepseek.com/">Your First API Call | DeepSeek API Docs</a></li>

</ul>
</details>

**Discussion**: Community reactions, as reflected in Simon Willison&\#x27;s coverage and the surrounding threads, are broadly positive — especially after the open weights appeared on Hugging Face — but the benchmark release process drew criticism: numbers circulated through the official WeChat group, were deleted from Reddit as &\#x27;low-effort&\#x27;, then ended up in an ASCII-art table on Hacker News. Willison also highlighted that the three reasoning levels produced strikingly different image outputs, an unusual behavior that sparked discussion about how thinking modes change model behavior.

**Tags**: `#DeepSeek`, `#AI`, `#API`, `#LLM`, `#pricing`

---

<a id="item-5"></a>
## [Cerebras and OpenAI Launch GPT-5.6 Sol Ultrafast, 7x Faster on HLE](https://www.cerebras.ai/blog/accelerating-gpt-5-6-sol-ultrafast-with-openai) ⭐️ 8.0/10

Cerebras and OpenAI unveiled GPT-5.6 Sol &\#x27;Ultrafast&\#x27; mode, which answered all 2,500 Humanity&\#x27;s Last Exam questions in 11 hours and 11 minutes, nearly 7x faster than Claude Fable 5&\#x27;s 78 hours and 27 minutes, while achieving comparable accuracy. This is a significant breakthrough in AI inference speed and marks a notable collaboration between OpenAI and Cerebras, potentially making frontier-level reasoning far more practical for real-time and iterative use. It could also push the industry to focus more on inference latency and inference-time compute as key competitive metrics. The evaluation used the HLE benchmark&\#x27;s 2,500 expert-authored questions, and the speed gain comes from Cerebras wafer-scale hardware paired with an optimized OpenAI deployment. The announcement does not explicitly state that Ultrafast produces identical results to the standard Sol model, only &\#x27;comparable accuracy,&\#x27; and no pricing information was released.

hackernews · pr337h4m · Aug 13, 18:10 · [Discussion](https://news.ycombinator.com/item?id=49289844)

**Background**: Humanity&\#x27;s Last Exam \(HLE\) is a language model benchmark created by the Center for AI Safety and Scale AI, consisting of 2,500 questions designed to test frontier knowledge and reasoning. Cerebras is known for its Wafer-Scale Engine \(WSE\), a single wafer-scale processor that integrates compute, memory, and interconnect fabric on one chip. Faster inference matters because it allows models to iterate more, and as one commenter noted, more iteration is often closely linked to higher-quality thinking.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Humanity&#x27;s_Last_Exam">Humanity&#x27;s Last Exam - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Cerebras">Cerebras - Wikipedia</a></li>
<li><a href="https://www.cerebras.ai/chip">Product - Chip - Cerebras</a></li>

</ul>
</details>

**Discussion**: Community reaction is mixed: some praise the raw speed and its implications for iterative reasoning, while others are skeptical about whether accuracy is truly preserved. Topfi noted that neither Cerebras nor OpenAI explicitly confirmed that Ultrafast performs identically to standard Sol, and GodelNumbering pointed out that the lack of pricing info could mean expensive enterprise-only access. wxw highlighted independent speed comparisons showing Ultrafast running 11x faster than Fable 5 and 5x faster than Opus 4.8 on Fast mode.

**Tags**: `#AI`, `#OpenAI`, `#Cerebras`, `#LLM performance`, `#hardware acceleration`

---

<a id="item-6"></a>
## [DeepSeek Harness: Open-Source Agent Harness Developer Preview](https://deepseek.com/harness/en/) ⭐️ 8.0/10

DeepSeek released DeepSeek Harness \(dsh\), an early open-source developer preview of its agent harness, licensed under MIT. The preview features full run traceability, replay/fork capabilities, and a dynamic plugin system built on Cordis. This matters because a leading AI lab is open-sourcing infrastructure that gives developers full visibility into every agent run, which commercial US models often obfuscate. The plugin architecture and traceability could accelerate building reliable, debuggable LLM agents in production. The harness records every context injection, system prompt, reasoning step, tool call, and subagent schedule in an append-only session log. A Trajectory view lets developers inspect records by source, and resume, fork, search, and replay all operate on the same event stream. It is an early preview, so breaking changes are expected.

hackernews · bjin · Aug 13, 12:58 · [Discussion](https://news.ycombinator.com/item?id=49285244)

**Background**: DeepSeek Harness is an agent harness, a layer that connects frontier LLMs to tools and memory so they can act as agents. It builds on Cordis, a plugin system that can hot-load and unload plugins without restarting the process and can revert plugin side effects. DeepSeek says it is hiring an Agent Harness R&amp;D Engineer to build this missing layer between models and production-ready agents, underscoring how the project fits into the broader LLM agent ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://www.deepseek.com/harness/en/">DeepSeek Harness developer preview: Everything is a plugin</a></li>
<li><a href="https://github.com/deepseek-ai/deepseek-harness">GitHub - deepseek -ai/ deepseek - harness : DeepSeek Harness ...</a></li>
<li><a href="https://dlcmh.github.io/">DeepSeek Agent Harness : Technical deep -dive &amp; the open-source...</a></li>

</ul>
</details>

**Discussion**: One author acknowledged the early preview and welcomed feedback. A user praised the full run traceability as a &\#x27;killer feature&\#x27;, contrasting it with encrypted, obfuscated traces in US models. Others connected the project to Cordis v4 and Koishi, while one commenter expressed &\#x27;plugin fatigue&\#x27; about the everything-is-a-plugin architecture.

**Tags**: `#deepseek`, `#open source`, `#LLM observability`, `#agent framework`, `#AI tools`

---

<a id="item-7"></a>
## [Choose Boring Technology: Conserve Innovation Tokens for Real Problems](https://mcfunley.com/choose-boring-technology) ⭐️ 8.0/10

This news item highlights Dan McKinley&\#x27;s influential 2015 essay &\#x27;Choose Boring Technology&\#x27;, which argues that companies should default to proven, mature technology and spend their limited &\#x27;innovation tokens&\#x27; only where genuine novelty is required. The essay offers a practical framework for making technology choices in engineering organizations. The essay has become a cornerstone of engineering-culture discussions and is widely cited by engineering leaders when evaluating new tools and frameworks. Its &\#x27;innovation tokens&\#x27; concept helps teams make tradeoffs and communicate those decisions clearly, and commenters are even applying it to modern AI agents, showing its continued relevance. The essay specifies that each company or team starts with roughly three innovation tokens, and that adopting a new database, framework, or deployment paradigm spends one token. &\#x27;Boring&\#x27; technology is defined as technology whose failure modes are well documented and whose limits are known, so teams should master a few proven tools and avoid unnecessary novelty.

hackernews · tosh · Aug 13, 17:48 · [Discussion](https://news.ycombinator.com/item?id=49289512)

**Background**: The essay was written by Dan McKinley, formerly of Etsy, and first published in 2015. It introduced the idea that every organization has a limited capacity for novelty—represented as three &\#x27;innovation tokens&\#x27;—and that once spent, these tokens are not replenished for a long while. The essay argues that companies should use boring, proven technology in most situations so they can concentrate their innovation budget on the few product areas that truly need it.

<details><summary>References</summary>
<ul>
<li><a href="https://concepts.dsebastien.net/concept/innovation-tokens/">Innovation Tokens - Concepts</a></li>
<li><a href="https://blog.matt-rickard.com/p/innovation-tokens">Innovation Tokens - Matt Rickard</a></li>
<li><a href="https://danieljamesglover.com/blog/2025-12-25-boring-it-infrastructure-reliability/">Why Boring IT Infrastructure Wins | Daniel J Glover</a></li>

</ul>
</details>

**Discussion**: The community reaction is largely positive: engineers like NickNaraghi call the innovation-tokens concept one of the most useful ideas for product and engineering leaders. Others extend it to modern AI agents, suggesting that teams should push innovation into agents and use boring &\#x27;in-distribution&\#x27; technology, while at least one commenter, insanitybit, pushes back, calling the concept arbitrary and arguing that novelty should be evaluated based on requirements, risks, and tradeoffs rather than weak proxies.

**Tags**: `#engineering-culture`, `#technology-choice`, `#software-engineering`, `#innovation`, `#essay`

---

<a id="item-8"></a>
## [Worldproof tool shows pixel metrics often can&\#x27;t rank world models](https://www.reddit.com/r/MachineLearning/comments/1vnliv7/worldproof_diagnosing_where_worldmodel/) ⭐️ 8.0/10

The author released worldproof, an open-source diagnostic tool for world models, and reported a key finding: on real robot video, a trivial &\#x27;predict last frame&\#x27; baseline scores 0.983 SSIM and 53.9 dB PSNR, and error does not grow with horizon. This means standard pixel metrics often cannot rank world models at all. The finding challenges common evaluation practices: if pixel metrics lack discriminative power, published comparisons and model rankings based on SSIM/PSNR may be meaningless. Researchers working on world models and robotics should measure the usable horizon on their own data instead of inheriting defaults from other papers. On DROID footage at 15fps over 48 steps, the baseline shows three regimes: near-perfect ties from steps 1–3, a steep monotonic decay with separable models from steps 4–24, and a floor around 0.20 SSIM / 10.3 dB with no trend after step 28. The author uses n=64 rollouts, interquartile mean and stratified bootstrap CIs, and notes that LPIPS behaves differently, pointing the opposite way on masked variants.

reddit · r/MachineLearning · /u/georgia\_bucea · Aug 13, 19:58

**Background**: World models are systems that predict future frames from initial context and action sequences; they are central to robotics and planning. PSNR and SSIM are standard pixel-level image quality metrics, but a trivial baseline that copies the last observed frame already achieves high scores when motion is limited. Because such baselines can inflate summary numbers, evaluation protocols need to be carefully calibrated to the data&\#x27;s frame rate and task speed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/kurt-glore1_artificialintelligence-worldmodels-machinelearning-activity-7398017216987922432-iffX">What are World Models and why are they important? | LinkedIn</a></li>
<li><a href="https://ieeexplore.ieee.org/document/5596999/">Image Quality Metrics: PSNR vs. SSIM | IEEE Conference Publication | IEEE Xplore</a></li>
<li><a href="https://www.academia.edu/165787940/Decomposing_Motion_and_Content_for_Natural_Video_Sequence_Prediction">(PDF) Decomposing Motion and Content for Natural Video Sequence...</a></li>

</ul>
</details>

**Tags**: `#world-models`, `#evaluation`, `#metrics`, `#robotics`, `#machine-learning`

---

<a id="item-9"></a>
## [Trump signs memo letting private firms conduct US-backed overseas cyber attacks](https://www.bloomberg.com/news/articles/2026-08-13/trump-enlists-private-sector-to-boost-cyber-offensive-arsenal) ⭐️ 8.0/10

President Trump signed a memorandum authorizing private companies, under direct federal control and supervision, to conduct overseas surveillance and cyber attacks against foreign transnational criminal organizations targeting Americans. The Department of Homeland Security will run the program and coordinate oversight with the Department of Justice. This marks a significant expansion of the private sector&\#x27;s role in government-sanctioned offensive cyber operations, blurring the line between corporate and state actions in cyberspace. It could set a precedent for other countries and raise serious legal, ethical, and accountability concerns within the global cybersecurity community. Participating companies must maintain a bond or escrow of at least $1 million, which can be confiscated if they fail to comply with contractual obligations. The program is jointly supervised by the Department of Homeland Security and the Department of Justice.

telegram · zaihuapd · Aug 13, 05:10

**Background**: This memorandum builds on longstanding US government authorities to conduct offensive cyber operations and surveillance, but traditionally such actions were carried out by intelligence and military agencies like the NSA or Cyber Command. By enlisting private firms, the government gains additional capacity and legal cover, while firms gain a formal role in national security. The move raises questions about oversight, liability, and the potential for abuse, especially since private sector actions may not be subject to the same public transparency rules.

**Tags**: `#cybersecurity`, `#surveillance`, `#US policy`, `#private sector`, `#cyber warfare`

---