---
layout: default
title: "Horizon Summary: 2026-07-28 (EN)"
date: 2026-07-28
lang: en
---

> From 29 items, 12 important content pieces were selected

---

1. [Moonshot AI Releases Kimi-K3 Weights with Modified License](#item-1) ⭐️ 9.0/10
2. [Google CEO reveals Gemini 4, most ambitious pretraining yet, due by end of 2026](#item-2) ⭐️ 9.0/10
3. [Fastjson2 RCE Vulnerability Unpatched](#item-3) ⭐️ 9.0/10
4. [vLLM v0.26.0: Inkling support, DeepSeek-V4 optimizations, flexible attention](#item-4) ⭐️ 8.0/10
5. [Anthropic Clarifies Position on Open-Weights Models](#item-5) ⭐️ 8.0/10
6. [Judge Rejects Google&\#x27;s DMCA Defense Against Scraping](#item-6) ⭐️ 8.0/10
7. [Replacing React with HTMX in a Forum Project](#item-7) ⭐️ 8.0/10
8. [Paged Out \#9: A Love Letter to Hacker Culture](#item-8) ⭐️ 8.0/10
9. [Libsm64 turns Super Mario 64 into a reusable library for game engines](#item-9) ⭐️ 8.0/10
10. [ChangXin Memory Tech surges 471% on STAR Market debut](#item-10) ⭐️ 8.0/10
11. [Alibaba Launches QwenWork AI Office Platform with Computer Control](#item-11) ⭐️ 8.0/10
12. [China begins mass production of domestic DUV lithography tools](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Moonshot AI Releases Kimi-K3 Weights with Modified License](https://simonwillison.net/2026/Jul/27/kimi-k3/#atom-everything) ⭐️ 9.0/10

Moonshot AI released the weights of its 2.8 trillion parameter Kimi-K3 model on Hugging Face on July 27, 2026, under a new license that requires large Model-as-a-Service providers to sign a separate agreement. Kimi-K3 is one of the largest open-weight models ever released, but its restrictive commercial license for large businesses may set a precedent for how AI companies balance openness with commercial interests. The K3 license drops the &\#x27;modified MIT&\#x27; label and adds a clause requiring a separate agreement for any entity with over $20 million aggregate revenue from Model-as-a-Service in 12 months. The model weights are 1.56 TB on Hugging Face and support up to 1 million token context.

rss · Simon Willison · Jul 27, 23:39

**Background**: Moonshot AI is a Chinese AI company behind the Kimi series of large language models. Their previous model, Kimi K2, used a modified MIT license requiring attribution for entities with over 100 million MAU or $20 million monthly revenue. The Kimi-K3 license tightens these restrictions for large commercial users. Open-weight models allow anyone to download and run the model, but the license governs permissible usage.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/moonshotai/Kimi-K3/blob/main/LICENSE">LICENSE · moonshotai/ Kimi - K 3 at main</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>
<li><a href="https://www.kimi.com/blog/kimi-k3">Kimi K 3 Tech Blog: Open Frontier Intelligence</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Open Source`, `#Large Language Model`, `#Hugging Face`

---

<a id="item-2"></a>
## [Google CEO reveals Gemini 4, most ambitious pretraining yet, due by end of 2026](https://9to5google.com/2026/07/26/google-gemini-4-teases/) ⭐️ 9.0/10

Sundar Pichai announced during Alphabet&\#x27;s Q2 2026 earnings call that Gemini 4, the next-generation large language model, is already in pretraining, calling it the company&\#x27;s most ambitious pretraining project to date. The model is expected to launch by the end of 2026. This signals Google&\#x27;s continued heavy investment in frontier AI, as pretraining larger foundation models is critical to stay competitive in the rapidly evolving LLM landscape. The release of Gemini 4 could push the boundaries of capabilities in areas such as reasoning, code generation, and multimodal understanding. Pichai emphasized that Google will prioritize compute allocation for frontier AGI research to ensure Gemini 4 remains at the cutting edge upon release. Additionally, the Gemini 3.x Flash series will maintain a nearly monthly update cadence, focusing on improving intelligent coding capabilities.

telegram · zaihuapd · Jul 27, 04:06

**Background**: Pretraining is the initial phase where a large language model learns to predict the next token from vast text corpora, resulting in a base model that requires further fine-tuning for specific tasks. Google&\#x27;s Gemini series includes multiple variants, with each generation aiming for improved performance and safety. The company has been iterating quickly, with Gemini 3.x Flash models already being released almost monthly.

<details><summary>References</summary>
<ul>
<li><a href="https://gist.github.com/ritwikraha/77e79990992043f60a9588610b2781c5">Pretraining of Large Language Models · GitHub</a></li>
<li><a href="https://ai.google.dev/gemini-api/docs/models">Models - Gemini API | Google AI for Developers</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Google Gemini`, `#Large Language Model`, `#Pre-training`, `#AGI`

---

<a id="item-3"></a>
## [Fastjson2 RCE Vulnerability Unpatched](https://mp.weixin.qq.com/s/LJaul1jNjK9pXRAkoUiMEA) ⭐️ 9.0/10

On July 27, Chaitin Technology disclosed a remote code execution vulnerability in Fastjson2 affecting all versions up to 2.0.62, allowing attackers to bypass AutoType validation via malicious JSON data. No patch is available yet. This vulnerability is critical because Fastjson2 is widely used in Java applications for JSON processing. Without a patch, many systems are at risk of remote code execution, potentially leading to full compromise of affected servers. Maintainers confirmed the issue but the proposed fix in PR \#7695 was closed and not merged into the main branch. As a workaround, users are advised to completely disable AutoType until a patch is released.

telegram · zaihuapd · Jul 27, 10:31

**Background**: Fastjson2 is a high-performance JSON library for Java developed by Alibaba, commonly used for serialization and deserialization. The AutoType feature automatically resolves types during deserialization, which can be exploited to execute arbitrary code if not properly validated. Similar vulnerabilities in Fastjson1 have historically required disabling AutoType as a mitigation.

<details><summary>References</summary>
<ul>
<li><a href="https://alibaba.github.io/fastjson2/">FASTJSON 2 is a Java JSON library with excellent performance.</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#RCE`, `#fastjson`, `#Java`

---

<a id="item-4"></a>
## [vLLM v0.26.0: Inkling support, DeepSeek-V4 optimizations, flexible attention](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 introduces support for the Inkling model family, significant performance optimizations for DeepSeek-V4 \(up to 2.94% E2E improvement\), fp32 lm\_head improvements, and flexible attention backend selection per KV-cache group. This release strengthens vLLM as a leading inference engine for diverse LLM architectures, offering both new model support and substantial performance gains that benefit users running large-scale deployments of models like DeepSeek-V4. The release includes 411 commits from 212 contributors, with notable additions like piecewise CUDA graph support for Inkling, a specialized routing kernel for DeepSeek-V4, and optional fp32 lm\_head via head\_dtype for generation models. KV offloading and tiered storage have also matured significantly.

github · khluu · Jul 27, 01:06

**Background**: vLLM is an open-source high-throughput LLM inference engine. The Inkling model family, released by Thinking Machines Lab under Apache 2.0, is a general-purpose multimodal model. DeepSeek-V4 is a popular large language model from DeepSeek, and vLLM optimizations aim to improve its inference performance.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/model-card/inkling/">Inkling Model Card - Thinking Machines Lab</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/mtp/">MTP (Multi-Token Prediction) - vLLM</a></li>
<li><a href="https://nvidia.github.io/TensorRT-LLM/features/quantization.html">Quantization — TensorRT LLM</a></li>

</ul>
</details>

**Tags**: `#LLM inference`, `#vLLM`, `#performance optimization`, `#DeepSeek`, `#GPU`

---

<a id="item-5"></a>
## [Anthropic Clarifies Position on Open-Weights Models](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 8.0/10

Anthropic published a policy statement clarifying that it does not advocate for banning open-weights models, but supports mandatory safety testing for all sufficiently capable models, both open and closed. This stance could shape ongoing regulatory debates on AI safety and openness, potentially affecting how open-weights models are developed and distributed. It also highlights the tension between promoting innovation and preventing misuse. The proposal entails mandatory safety testing but does not specify who would administer the tests or what the criteria would be, leading critics to argue it could function as a de facto ban on open-weights models if costs or restrictions are high.

hackernews · surprisetalk · Jul 27, 22:03 · [Discussion](https://news.ycombinator.com/item?id=49076057)

**Background**: Open-weights models are AI models whose core components \(e.g., trained weights\) are publicly released, allowing anyone to download, inspect, and modify them. Anthropic is a leading AI safety company that develops the Claude model series, and its policy positions carry weight in the AI community. The debate around open-weights models centers on balancing accessibility and safety, with some arguing they enable innovation and others warning of potential misuse.

<details><summary>References</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://www.microsoft.com/en-us/corporate-responsibility/topics/open-weight/">Open Weights and American AI Leadership</a></li>

</ul>
</details>

**Discussion**: Commenters expressed skepticism, with many viewing the proposal as a disguised ban on open-weights models to protect Anthropic&\#x27;s commercial interests. Some pointed out contradictions in Anthropic CEO Dario Amodei&\#x27;s previous statements about bans, and others noted geopolitical implications regarding chip exports to China.

**Tags**: `#AI safety`, `#open-weights`, `#Anthropic`, `#AI regulation`, `#policy`

---

<a id="item-6"></a>
## [Judge Rejects Google&\#x27;s DMCA Defense Against Scraping](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 8.0/10

A federal judge ruled that Google cannot invoke the DMCA&\#x27;s safe harbor provisions to block third-party scraping of its search engine results pages \(SERPs\). This decision sets a significant legal precedent that may limit how companies use copyright law to restrict web scraping, especially when they have deprecated official APIs. The court found that Google&\#x27;s search results constitute factual data lacking the originality required for copyright protection, and thus the DMCA did not apply.

hackernews · cdrnsf · Jul 27, 18:15 · [Discussion](https://news.ycombinator.com/item?id=49073513)

**Background**: The DMCA&\#x27;s safe harbor provisions protect online service providers from liability for copyright infringement committed by their users, but they do not shield companies from having their own content scraped. Web scraping is the automated extraction of data from websites, often used when no official API is available.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DMCA_safe_harbor">DMCA safe harbor</a></li>
<li><a href="https://www.eff.org/issues/dmca">DMCA | Electronic Frontier Foundation</a></li>

</ul>
</details>

**Discussion**: Commenters expressed irony that Google, built on crawling the web, now tries to block scraping of its own results. Many noted that Google&\#x27;s deprecation of its search API leaves scraping as the only alternative, and criticized the lawsuit as an attempt to bully a smaller company.

**Tags**: `#law`, `#web scraping`, `#Google`, `#DMCA`, `#copyright`

---

<a id="item-7"></a>
## [Replacing React with HTMX in a Forum Project](https://misago-project.org/t/removing-reactjs-from-the-codebase-and-adapting-htmx-for-ui-interactivity/1267/) ⭐️ 8.0/10

The Misago forum project removed React.js from its codebase and adopted HTMX for UI interactivity, achieving simpler code and better performance. This case study shows a real-world move away from heavy client-side frameworks to a hypermedia-driven approach, which can reduce complexity and improve load times for content-heavy sites like forums. HTMX enables dynamic UI updates via server-rendered HTML fragments using attributes like hx-get and hx-post, without writing JavaScript. The transition reportedly simplified the codebase and improved perceived performance.

hackernews · Ralfp · Jul 27, 09:58 · [Discussion](https://news.ycombinator.com/item?id=49067301)

**Background**: HTMX is an open-source JavaScript library that extends HTML with custom attributes, allowing developers to perform AJAX, WebSocket, and Server-Sent Events directly in HTML. It follows a hypermedia-driven approach, contrasting with React&\#x27;s component-based virtual DOM model. This replacement reflects a trend where some developers find server-rendered approaches simpler and faster for certain applications.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Htmx">Htmx</a></li>
<li><a href="https://htmx.org/">htmx - high power tools for html</a></li>

</ul>
</details>

**Discussion**: Community comments present mixed experiences: some users found HTMX slow for complex filter interfaces due to large HTML payloads, while others praise it for forum software and recommend pairing it with TailwindCSS. Many agree that HTMX is a good fit for content-driven sites, and one user suggests using a mini Vue or React component for highly interactive parts when needed.

**Tags**: `#HTMX`, `#React`, `#web development`, `#server-side rendering`, `#frontend architecture`

---

<a id="item-8"></a>
## [Paged Out \#9: A Love Letter to Hacker Culture](https://pagedout.institute/download/PagedOut_009.pdf) ⭐️ 8.0/10

Paged Out \#9, a free PDF magazine, was released, featuring deeply technical and eclectic articles on topics like subpixel rendering and computable tilings. This magazine revives the spirit of classic hacker zines like Phrack and 2600, offering a beautifully designed platform for niche technical content that inspires curiosity and deep learning. The issue includes a humorous piece titled &\#x27;Baby Steps in C&\#x27; and an uncredited rediscovery of Wang&\#x27;s 1960s work on computable tilings, linking tilings to the halting problem.

hackernews · laurensr · Jul 27, 14:22 · [Discussion](https://news.ycombinator.com/item?id=49070138)

**Background**: Paged Out is a free, community-driven technical magazine that focuses on low-level programming, hacking, and computer science topics. It is designed to be both aesthetically pleasing and intellectually stimulating, appealing to readers who enjoy deep dives into obscure or foundational subjects.

**Discussion**: Readers on Hacker News praised the magazine for its technical depth and design, comparing it favorably to classic zines like Phrack and 2600. One commenter noted that the computable tilings article rediscovered Wang&\#x27;s work without attribution, sparking interest in the link between tilings and the halting problem.

**Tags**: `#hacking`, `#programming`, `#computer science`, `#zine`, `#technical articles`

---

<a id="item-9"></a>
## [Libsm64 turns Super Mario 64 into a reusable library for game engines](https://github.com/libsm64/libsm64) ⭐️ 8.0/10

The open-source project libsm64 decompiles Super Mario 64 into a C++ library that provides Mario&\#x27;s movement and rendering code, allowing developers to embed Mario into any external game engine. This project enables creative crossovers, such as Mario appearing in Half-Life 2, and demonstrates how classic game assets can be repurposed in modern engines without relying on hype-driven concepts like the metaverse. Libsm64 is built on the full SM64 decompilation by n64decomp; users must provide their own ROM for asset extraction. An awesome-list repository tracks projects built with libsm64.

hackernews · klaussilveira · Jul 27, 10:04 · [Discussion](https://news.ycombinator.com/item?id=49067352)

**Background**: Super Mario 64 was originally released in 1996 for the Nintendo 64. The n64decomp project fully decompiled the game&\#x27;s source code from its binary, enabling projects like libsm64 to extract and re-package its functionality as a standalone library for integration into custom game engines.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/libsm64/libsm64">GitHub - libsm 64 / libsm 64 : Mario 64 as a library for use in external...</a></li>
<li><a href="https://asibiont.com/en/blog/libsm64-kak-kultovyy-super-mario-64-prevratili-v-biblioteku-dlya-igrovykh-dvizhkov">Libsm 64 : Super Mario 64 Reborn as a Library for... — ASI Biont Blog</a></li>
<li><a href="https://github.com/n64decomp/sm64">GitHub - n64decomp/ sm 64 : A Super Mario 64 decompilation , brought...</a></li>

</ul>
</details>

**Discussion**: Community members expressed excitement about the library&\#x27;s potential, comparing it to the promise of the metaverse but without the hype. Some asked for demo videos, which were provided, and a curated list of projects using libsm64 was shared.

**Tags**: `#game development`, `#software engineering`, `#decompilation`, `#open source`, `#C++`

---

<a id="item-10"></a>
## [ChangXin Memory Tech surges 471% on STAR Market debut](https://www.stcn.com/article/detail/4042119.html) ⭐️ 8.0/10

ChangXin Memory Technologies \(688825.SH\) opened at 49.5 yuan per share on its STAR Market debut, a 471.59% surge from its IPO price of 8.66 yuan, making it the largest IPO in the board&\#x27;s history with total proceeds of up to 66.6 billion yuan. This milestone underscores China&\#x27;s push for semiconductor self-sufficiency, as ChangXin is a key domestic DRAM producer. The record IPO provides substantial capital to scale production and compete with global memory giants like Samsung and SK Hynix. The IPO raised approximately 57.9 billion yuan, with a greenshoe option potentially increasing it to 66.6 billion yuan. The company expects net profit attributable to parent of 50-57 billion yuan in the first half of 2026, turning around from a previous loss.

telegram · zaihuapd · Jul 27, 01:29

**Background**: ChangXin Memory Technologies \(CXMT\) is China&\#x27;s leading DRAM chipmaker, focusing on memory chips for consumer electronics and data centers. The STAR Market \(科创板\) is Shanghai&\#x27;s Nasdaq-style board for tech companies with relaxed listing rules. DRAM is a critical component in computers and smartphones, and China has long sought to reduce reliance on foreign suppliers.

**Tags**: `#IPO`, `#semiconductor`, `#memory`, `#China tech`, `#stock market`

---

<a id="item-11"></a>
## [Alibaba Launches QwenWork AI Office Platform with Computer Control](https://qwenwork.cn/) ⭐️ 8.0/10

Alibaba has launched the beta version of QwenWork \(千问办公\), a one-stop AI office platform that can generate and edit documents, spreadsheets, presentations, web pages, code, and multimedia content via natural language. The desktop client also includes computer control capabilities, allowing it to perform browser automation and cross-application actions like clicking, typing, and data extraction. This product consolidates Alibaba&\#x27;s AI office tools into a single platform deeply integrated with DingTalk, offering competitive pricing and new computer control features that could significantly boost productivity for professionals. It signals Alibaba&\#x27;s aggressive push in the AI office space, potentially reshaping how office tasks are automated. The platform offers free, standard \(78 CNY/month\), and premium \(158 CNY/month\) tiers, with new users receiving 2000 free integration points. Computer control features may capture screen content and perform irreversible operations, so the platform defaults to asking for user confirmation before executing actions.

telegram · zaihuapd · Jul 27, 05:45

**Background**: Alibaba&\#x27;s Qwen is a large language model family, and QwenWork leverages its capabilities for office automation. The concept of AI agents that can control computers \(Computer Use\) has been gaining traction, with projects like Browser Use and OpenAI&\#x27;s Computer Use agent emerging. QwenWork&\#x27;s integration with DingTalk, a major enterprise collaboration tool in China, gives it a strong distribution advantage.

<details><summary>References</summary>
<ul>
<li><a href="https://36kr.com/p/3909382165419144">AI办公，阿里得靠“千问办公”换个打法-36氪</a></li>
<li><a href="https://www.aihub.cn/tools/qwenwork/">千问办公 - 阿里推出的一站式 AI Agent 办公平台，把任务做完并交付产物 - AIHub</a></li>
<li><a href="https://github.com/browser-use/browser-use">browser- use /browser- use : Make websites accessible for AI agents.</a></li>

</ul>
</details>

**Tags**: `#AI office`, `#Alibaba`, `#Qwen`, `#computer control`, `#productivity`

---

<a id="item-12"></a>
## [China begins mass production of domestic DUV lithography tools](https://www.theinformation.com/articles/china-starts-mass-producing-homegrown-duv-chipmaking-tools-advance-local-chip-industry) ⭐️ 8.0/10

China has started mass production of domestic immersion deep ultraviolet \(DUV\) lithography tools, with a plan to produce about 5 units this year and around 20 units by 2027, according to sources familiar with the matter. The tools will be delivered to domestic chipmakers such as SMIC and Hua Hong Semiconductor. This marks a significant step in China&\#x27;s efforts to reduce reliance on foreign semiconductor equipment, especially Dutch supplier ASML, amid ongoing export restrictions. Although the tools lag behind ASML in performance and reliability, scaling up production could gradually erode ASML&\#x27;s market share in China. The domestic tools use mostly locally sourced components, but some critical parts still come from Japan, and supply chain delays have already affected progress this year. Chipmakers need months or longer to test the precision and compatibility before the tools can be used in mass production lines.

telegram · zaihuapd · Jul 27, 14:10

**Background**: Deep ultraviolet \(DUV\) lithography is a key process in semiconductor manufacturing that uses light with wavelengths of 248 nm or 193 nm to pattern circuits on wafers. Immersion lithography improves resolution by placing a liquid \(usually water\) between the lens and the wafer, enabling features below 45 nm. ASML currently dominates the DUV market, but export restrictions have prompted China to develop its own tools.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Immersion_lithography">Immersion lithography</a></li>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://www.asml.com/en/products/duv-lithography-systems">DUV lithography systems | Products - ASML</a></li>

</ul>
</details>

**Tags**: `#semiconductor`, `#lithography`, `#China`, `#ASML`, `#manufacturing`

---