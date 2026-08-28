---
layout: default
title: "Horizon Summary: 2026-08-28 (EN)"
date: 2026-08-28
lang: en
---

> From 32 items, 14 important content pieces were selected

---

1. [Cloudflare Optimizes 1.1.1.1 DNS Cache to Save 100TB Memory](#item-1) ⭐️ 8.0/10
2. [Small Models Have Arrived: Practical AI Beyond Frontier Scale](#item-2) ⭐️ 8.0/10
3. [507 Mechanical Movements: 19th-Century Mechanisms Brought to Life Online](#item-3) ⭐️ 8.0/10
4. [Google unveils Gemini-3.5-Transcribe, a precise speech-to-text model with latency trade-offs](#item-4) ⭐️ 8.0/10
5. [Open-Source Rust LLM Gateway Routes Queries and Trains Custom Models](#item-5) ⭐️ 8.0/10
6. [Analyzing Claude&\#x27;s overused &\#x27;load-bearing&\#x27; vocabulary](#item-6) ⭐️ 8.0/10
7. [Decompiling a Nintendo 64 game in 84 days](#item-7) ⭐️ 8.0/10
8. [Prompt Injection Attack Breaks Claude Code Auto Mode 80% of the Time](#item-8) ⭐️ 8.0/10
9. [New Benchmark HarnessOpt-Bench Measures Recursive Self-Improvement in AI](#item-9) ⭐️ 8.0/10
10. [Nvidia posts $96.2B quarterly revenue; gives first-time 70% FY2028 growth guidance](#item-10) ⭐️ 8.0/10
11. [Anthropic Previews Model Hardware Standard for AI-Controlled Devices](#item-11) ⭐️ 8.0/10
12. [OpenAI Developing Persistent Codex Agent That Keeps Working Until Sleep](#item-12) ⭐️ 8.0/10
13. [US Judge Blocks Pentagon&\#x27;s Ban on Anthropic](#item-13) ⭐️ 8.0/10
14. [Tencent Hunyuan Releases Hy4 Preview, Outperforming Rivals in Blind Test](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Cloudflare Optimizes 1.1.1.1 DNS Cache to Save 100TB Memory](https://blog.cloudflare.com/dns-cache-memory-optimization-1111/) ⭐️ 8.0/10

Cloudflare engineers published a detailed engineering post describing how they reduced the memory footprint of 1.1.1.1&\#x27;s DNS cache by 100 terabytes. The savings came from careful data structure and memory management optimizations rather than hardware changes. Saving 100TB of memory is a massive infrastructural win for a public DNS service that serves billions of queries. It can reduce operating costs, improve cache hit rates by allowing more entries to stay resident, and benefit the wider Internet&\#x27;s resolution performance. The 100TB reduction was achieved by reworking how the DNS cache stores and allocates records, with the blog post providing a detailed technical walkthrough. It exemplifies how low-level memory tuning, often considered &\#x27;trivial&\#x27; by experts, can have an enormous aggregate impact.

hackernews · TangerineDream · Aug 27, 17:17 · [Discussion](https://news.ycombinator.com/item?id=49468083)

**Background**: 1.1.1.1 is Cloudflare&\#x27;s public recursive DNS resolver used to resolve domain names for clients worldwide. To return quick responses and reduce upstream traffic, the resolver caches DNS records in memory. A large, heavily used cache can consume enormous amounts of RAM, so memory layout and allocation strategy directly affect both cost and performance. This post focuses on the memory optimization side of running such a service.

**Discussion**: Commenters generally praised the approach of optimizing only after the product and business were proven, and several noted that similar techniques like struct alignment and reducing allocation overhead are standard in systems programming. One commenter suggested placing record data directly after CacheEntry members instead of separate allocations, while another raised a concern that merging distinct lists into a single structure could weaken Rust&\#x27;s safety guarantees.

**Tags**: `#DNS`, `#memory-optimization`, `#system-programming`, `#Cloudflare`, `#rust`

---

<a id="item-2"></a>
## [Small Models Have Arrived: Practical AI Beyond Frontier Scale](https://calv.info/small-models-have-arrived) ⭐️ 8.0/10

The article &\#x27;Small Models Have Arrived&\#x27; argues that small language models are now practical for many consumer-oriented use cases, signaling a shift away from the industry&\#x27;s focus on frontier-scale AI. It calls for paying attention to the growing demand for &\#x27;fast/cheap/good-enough&\#x27; models. This matters because it challenges the assumption that only the largest, most expensive models are valuable, potentially opening the market to consumer AI and on-device applications. Developers, enterprises, and investors may need to rethink strategies centered on frontier labs and massive compute. Small language models typically have fewer than forty billion parameters, making them feasible to train or host on consumer devices, unlike large models with hundreds of billions of parameters. Efficiency is achieved through techniques such as knowledge distillation, pruning, and quantization.

hackernews · tosh · Aug 27, 15:56 · [Discussion](https://news.ycombinator.com/item?id=49466917)

**Background**: Small language models \(SLMs\) are compact AI models for natural language processing, typically using the same architecture as large language models \(LLMs\) but with far fewer parameters. LLMs contain hundreds of billions to over a trillion parameters, requiring massive computational resources for training and hosting. Local inference, or on-device inference, runs these models on personal computers, smartphones, or local servers instead of cloud data centers. This makes small models attractive for cost-sensitive, privacy-sensitive, or offline applications.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Small_language_model">Small language model</a></li>
<li><a href="https://www.ibm.com/think/topics/small-language-models">What are Small Language Models (SLM)? | IBM</a></li>
<li><a href="https://prajnaaiwisdom.medium.com/what-is-local-llm-inference-a-beginners-guide-b31043768d4f">What Is Local LLM Inference? A Beginner’s Guide | by PrajnaAI | Medium</a></li>

</ul>
</details>

**Discussion**: Commenters are broadly positive, with one describing how a 7B local model combined with the Guidance library automated test-writing and code generation as early as 2024. Some investors question why consumer AI companies are still rare, while another commenter frames the opportunity as &\#x27;room at the bottom&\#x27; strategies where deep world knowledge is unnecessary. A comment also compares &\#x27;IQ 180&\#x27; work with &\#x27;token spewer&\#x27; work, drawing an analogy to Paul Graham&\#x27;s Maker&\#x27;s Schedule and Manager&\#x27;s Schedule.

**Tags**: `#small models`, `#AI`, `#machine learning`, `#local inference`, `#consumer AI`

---

<a id="item-3"></a>
## [507 Mechanical Movements: 19th-Century Mechanisms Brought to Life Online](https://507movements.com/) ⭐️ 8.0/10

The interactive website 507movements.com animates the historical mechanical movements cataloged in Henry T. Brown&\#x27;s 1868 book &quot;507 Mechanical Movements,&quot; turning static line drawings into clickable animations. The site recently drew significant attention on Hacker News, earning 549 points and 70 comments. The site makes a rare 19th-century engineering reference accessible to modern engineers, designers, and hobbyists, helping them understand the origins of common mechanisms. It also sparked a broader community discussion about similar book-to-website projects and related mechanical collections. The animations are based on Henry T. Brown&\#x27;s classic reference, originally published in 1868 and featured in a 1908 edition available on the Internet Archive. Users have noted that individual animations lack titles or names, and that not all 507 movements have been animated yet.

hackernews · helloplanets · Aug 27, 14:08 · [Discussion](https://news.ycombinator.com/item?id=49465169)

**Background**: Henry T. Brown&\#x27;s &quot;507 Mechanical Movements&quot; is a 19th-century technical reference that catalogs mechanisms such as linkages, gears, and escapements with simple line drawings and brief explanations. In the mid-1800s, such books served as idea catalogs for inventors and engineers designing machines. The Internet Archive hosts a scanned copy, and projects like 507movements.com revive these drawings as interactive animations, continuing a tradition of turning classic texts into digital experiences.

<details><summary>References</summary>
<ul>
<li><a href="https://507movements.com/">507 Mechanical Movements</a></li>
<li><a href="https://archive.org/details/fivehundredseven00browiala">Five hundred and seven mechanical movements ... : Brown, Henry T : Free Download, Borrow, and Streaming : Internet Archive</a></li>
<li><a href="https://grokipedia.com/page/507_mechanical_movements_mechanisms_and_devices_%28book%29">507 Mechanical Movements: Mechanisms and Devices (book)</a></li>

</ul>
</details>

**Discussion**: Commenters generally praised the site, calling it a favorite and a great interactive resource. Some wished the animations were complete and that individual movements had names or titles. Others shared related resources, including the Redtenbacher and Reuleaux model collections in Karlsruhe and Cornell, and recommended books on manufacturing processes and materials selection.

**Tags**: `#mechanical-engineering`, `#history-of-technology`, `#interactive-education`, `#animations`, `#reference`

---

<a id="item-4"></a>
## [Google unveils Gemini-3.5-Transcribe, a precise speech-to-text model with latency trade-offs](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5-transcribe/) ⭐️ 8.0/10

Google has introduced Gemini-3.5-Transcribe, a new speech-to-text model that leads in accuracy. Community benchmarks show it lags behind competitors like Soniox and Voxtral in latency. Speech-to-text technology is critical for real-time translation, meeting transcription, and voice interfaces. This release intensifies competition in the STT space, but latency could limit its adoption in real-time applications. The model converts raw audio directly into accurate, polished, formatted text, handling background noise, jargon, and disfluency. It powers Gboard Rambler and will come to Chrome, but some users report it may simplify precise wording and alter meaning.

hackernews · k9294 · Aug 27, 18:03 · [Discussion](https://news.ycombinator.com/item?id=49468818)

**Background**: Speech-to-text \(STT\) models convert audio into text, and traditional models often struggle with noise, jargon, and disfluencies. Gemini-3.5-Transcribe is based on Gemini&\#x27;s audio understanding capabilities. Competitors like Soniox focus on low-latency real-time STT, while Voxtral offers lightweight local models. Recent announcements highlight the trade-off between accuracy and speed in STT.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5-transcribe/">Intelligent transcription with Gemini 3.5 Transcribe</a></li>
<li><a href="https://ai.google.dev/gemini-api/docs/models/gemini-3.5-transcribe">Gemini 3.5 Transcribe | Gemini API | Google AI for Developers</a></li>
<li><a href="https://9to5google.com/2026/08/26/gemini-3-5-transcribe/">Google launches Gemini 3.5 Transcribe, which powers Gboard Rambler &amp; is coming to Chrome</a></li>

</ul>
</details>

**Discussion**: Developers tested the model in real-world scenarios; some praised its accuracy but noted higher latency. One user found it simplifies precise wording, altering meaning, while another was confused by the function-calling description. Overall sentiment is mixed: strong accuracy but latency and precision concerns.

**Tags**: `#speech-to-text`, `#Gemini`, `#Google`, `#AI models`, `#STT`

---

<a id="item-5"></a>
## [Open-Source Rust LLM Gateway Routes Queries and Trains Custom Models](https://github.com/experientiallabs/experiential) ⭐️ 8.0/10

Experientiallabs released Experiential, an open-source LLM gateway written in Rust that unifies self-hosted and commercial models behind a single API. It adds under 1 ms latency for bring-your-own-key requests and can optionally train custom models from user traffic. This tackles the pain of provider fragmentation and opaque markups in model routing. By being open source and taking no markup, it offers a cost-transparent alternative to commercial gateways, while the &\#x27;train from usage&\#x27; feature hints at a new way to improve models from real traffic. The gateway uses standardized OTel traces to mine representative tasks, employs text world models to simulate rollouts, applies an LLM judge for evaluation, and fits a nearest-neighbor classifier on prompt embeddings to select the optimal model. It also suggests cache-hit optimizations and new model suggestions, though commenters note semantic caching is not yet implemented.

hackernews · SilenN · Aug 27, 21:18 · [Discussion](https://news.ycombinator.com/item?id=49471407)

**Background**: An LLM gateway is a middleware layer that routes application requests to different AI models, handling API quirks, rate limits, and observability. Text world models are AI systems that simulate environments for agents, and LLM-as-a-judge is a technique where one language model evaluates another model&\#x27;s outputs; both are used in the gateway&\#x27;s routing and training pipeline. Rust is a systems language chosen for high concurrency.

<details><summary>References</summary>
<ul>
<li><a href="https://coworker.ai/blog/llm-gateway">What Is an LLM Gateway ? 2026 Guide | Coworker AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/LLM-as-a-Judge">LLM-as-a-Judge</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen-AgentWorld-35B-A3B">Qwen/Qwen-AgentWorld-35B-A3B · Hugging Face</a></li>

</ul>
</details>

**Discussion**: Commenters are broadly positive about the open-source, no-markup approach, but several ask about caching: routing across many models could fragment cached input tokens and drive up costs. Others question how simulated rankings are recalibrated against real task success, and whether semantic caching at the router level is planned.

**Tags**: `#LLM`, `#model-gateway`, `#open-source`, `#Rust`, `#AI-infrastructure`

---

<a id="item-6"></a>
## [Analyzing Claude&\#x27;s overused &\#x27;load-bearing&\#x27; vocabulary](https://louisabraham.github.io/load-bearing/) ⭐️ 8.0/10

Developer louisabraham released a live, crowdsourced analysis showing the &\#x27;load-bearing&\#x27; vocabulary Claude overuses in GitHub pull request descriptions, grouping them into eight writing styles. The dataset and analysis are updated daily using GitHub Actions. This analysis exposes how LLMs fall into repetitive verbal patterns, which matters as AI-generated content increasingly shapes online writing. It also fuels discussion about whether model training on AI-generated text creates a feedback loop that worsens these tics. The project clusters GitHub pull request descriptions by the words they use rather than by topic, revealing eight distinct writing styles. The author plans to add a search bar and scale the corpus to 1,000 pull requests per day.

hackernews · Labo333 · Aug 27, 08:59 · [Discussion](https://news.ycombinator.com/item?id=49461817)

**Background**: The phrase &\#x27;load-bearing&\#x27; is often used as a metaphor for something that structurally supports an argument, and it has become a recognized verbal tic in AI-generated text. In natural language processing, collocation extraction automatically identifies multi-word expressions that co-occur more often than chance, which is a technique similar to what this analysis uses. The popularity of this project highlights growing public scrutiny of LLM writing habits.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/louisabraham/load-bearing">GitHub - louisabraham/ load - bearing : The load - bearing vocabulary of...</a></li>
<li><a href="https://mlwiki.org/index.php/Collocation_Extraction">Collocation Extraction - ML Wiki</a></li>
<li><a href="https://www.vocabulary.com/dictionary/load-bearing">Load - bearing - Definition, Meaning &amp; Synonyms | Vocabulary .com</a></li>

</ul>
</details>

**Discussion**: Commenters responded with mixed enthusiasm: ben30 shared that adding an Orwellian rule to his prompt made Claude admit the instruction &\#x27;fights my own system prompt.&\#x27; nater5000 praised the site&\#x27;s concise, single-screen presentation, while author Labo333 announced upcoming features and daily updates. SalariedSlave observed that all current models seem to share the style problem, speculating that newer models may be ingesting too much AI-generated content.

**Tags**: `#LLM`, `#Claude`, `#AI analysis`, `#data visualization`, `#NLP`

---

<a id="item-7"></a>
## [Decompiling a Nintendo 64 game in 84 days](https://blog.chrislewis.au/decompiling-a-nintendo-64-game-in-84-days/) ⭐️ 8.0/10

A developer details the process of decompiling a Nintendo 64 game \(Snowboard Kids\) in 84 days, highlighting modern tooling and community interest in retro game preservation.

hackernews · knackers · Aug 27, 15:01 · [Discussion](https://news.ycombinator.com/item?id=49466006)

**Tags**: `#reverse engineering`, `#decompilation`, `#Nintendo 64`, `#retro gaming`, `#LLM-assisted development`

---

<a id="item-8"></a>
## [Prompt Injection Attack Breaks Claude Code Auto Mode 80% of the Time](https://simonwillison.net/2026/Aug/27/breaking-claude-code-opus-5-auto-mode/) ⭐️ 8.0/10

Security researcher Johann Rehberger demonstrated a prompt injection attack that bypasses Claude Code&\#x27;s auto mode protections roughly 80% of the time. The attack tricks Claude Code into downloading and unzipping a malicious archive, then exploits Python&\#x27;s module resolution to execute a local struct.py file as a dependency of the standard base64 module. This finding challenges Anthropic&\#x27;s claims that auto mode can effectively protect coding agents from prompt injection. Because auto mode is now the default, developers relying on Claude Code for unattended operations are exposed to a practical high-success-rate attack, underscoring the need for sandboxing and network egress controls. In some runs, Claude detected the compromise and tried to terminate the malware process, but auto mode blocked the cleanup command, so the safety mechanism itself became part of the failure. Rehberger recommends running unattended agents in a container, VM, or OS sandbox, restricting network egress, monitoring agents, and not exposing home directories or credentials to the agent runtime.

rss · Simon Willison · Aug 27, 22:50

**Background**: Claude Code is Anthropic&\#x27;s terminal-based AI coding agent. Auto mode, generally available since July 10, 2026, is a permissions mode in which Claude makes permission decisions on the user&\#x27;s behalf, with safeguards monitoring actions before they run. Prompt injection attacks feed malicious instructions to an AI model through hidden content, such as text inside downloaded files. In this case, the agent is tricked into extracting a zip archive containing a crafted struct.py; when the agent later runs Python code that imports base64, that module imports struct, and Python&\#x27;s import resolution executes the local struct.py from the current directory instead of the standard library version.

<details><summary>References</summary>
<ul>
<li><a href="https://claude.com/blog/auto-mode">Auto mode for Claude Code | Claude by Anthropic</a></li>
<li><a href="https://www.datacamp.com/tutorial/claude-code-auto-mode-and-channels">Claude Code Auto Mode and Channels: Build Code ... | DataCamp</a></li>
<li><a href="https://stackoverflow.com/questions/36250353/importing-a-library-from-or-near-a-script-with-the-same-name-raises-attribute">python - Importing a library from (or near) a script... - Stack Overflow</a></li>

</ul>
</details>

**Tags**: `#security`, `#prompt injection`, `#AI agents`, `#Claude Code`, `#vulnerability`

---

<a id="item-9"></a>
## [New Benchmark HarnessOpt-Bench Measures Recursive Self-Improvement in AI](https://www.reddit.com/r/MachineLearning/comments/1w052xg/can_ai_improve_itself_rsi_might_be_the_answer_r/) ⭐️ 8.0/10

Researchers introduced HarnessOpt-Bench, a benchmark that measures how much an LLM improves another agent&\#x27;s harness while keeping evaluation data outside the optimizer&\#x27;s sandbox. Experiments with 5 frontier models across 4 downstream tasks and 111 runs revealed that model choice affects performance gains 1.8× more than harness choice. Recursive self-improvement \(RSI\) is a major AI safety concern, and this benchmark offers a way to study it under controlled, architecture-enforced isolation. It provides evidence that current frontier models can measurably improve other agents&\#x27; harnesses, informing both capability assessment and alignment research. The isolation is guaranteed by construction, not by instruction: the held-out evaluator and permission control sit outside the harness-evolution loop, so API keys, budget enforcement, and held-out data never enter the optimizer&\#x27;s sandbox. On the test split, the optimizer receives no feedback until a trusted server scores the final candidate harness.

reddit · r/MachineLearning · /u/shehio · Aug 27, 20:13

**Background**: Recursive self-improvement refers to an AI system rewriting its own code or improving its successors, potentially leading to an intelligence explosion. Harness optimization is a concrete instance: an &\#x27;optimizer&\#x27; LLM iteratively improves the software harness that wraps a target agent. The benchmark extends this idea by adding strict architectural isolation so the optimizer cannot tamper with the evaluation process or access held-out test data.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2608.06301">HarnessOpt - Bench : Evaluating LLMs at Harness Optimization</a></li>
<li><a href="https://en.wikipedia.org/wiki/Recursive_self-improvement">Recursive self-improvement</a></li>
<li><a href="https://www.anthropic.com/institute/recursive-self-improvement">When AI builds itself \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#AI Safety`, `#Recursive Self-Improvement`, `#Benchmark`, `#Machine Learning`, `#Alignment`

---

<a id="item-10"></a>
## [Nvidia posts $96.2B quarterly revenue; gives first-time 70% FY2028 growth guidance](https://mp.weixin.qq.com/s/JTZ_ZJ_pn5vgrI_1QUyWNw) ⭐️ 8.0/10

Nvidia reported $96.221 billion in revenue for its fiscal 2027 second quarter, up 106% year over year, with data center revenue of $89 billion, up 117%. CFO Colette Kress also provided, for the first time, a fiscal 2028 revenue growth guidance of about 70%, which she said is constrained by supply. Nvidia&\#x27;s results and unprecedented forward guidance signal that demand for AI compute remains extremely strong and that supply, not demand, is the near-term bottleneck. This will shape expectations for AI infrastructure spending and the semiconductor supply chain over the next year. Vera Rubin, Nvidia&\#x27;s next-generation platform combining the Rubin GPU and Vera CPU, has begun volume production and shipping this month, and is expected to contribute about 20% of data center revenue in the third quarter. CFO Kress stressed that the roughly 70% FY2028 growth expectation is supply-limited rather than demand-limited.

telegram · zaihuapd · Aug 27, 08:51

**Background**: Nvidia is the dominant supplier of AI accelerators, and its earnings are widely watched as a barometer for AI infrastructure demand. The Vera Rubin platform, announced by CEO Jensen Huang at Computex in 2024 and named after astrophysicist Vera Rubin, pairs the Rubin GPU with the Vera CPU, is manufactured by TSMC, and is designed for large-scale AI data centers. Forward revenue guidance that far into the future is unusual for Nvidia, making this announcement particularly notable.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Rubin_%28microarchitecture%29">Rubin (microarchitecture) - Wikipedia</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/technologies/rubin/">Infrastructure for Scalable AI Reasoning | NVIDIA Vera Rubin Platform</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#earnings`, `#AI`, `#data center`, `#semiconductor`

---

<a id="item-11"></a>
## [Anthropic Previews Model Hardware Standard for AI-Controlled Devices](https://www.anthropic.com/news/model-hardware-standard-research-preview) ⭐️ 8.0/10

Anthropic has opened a research preview of the Model Hardware Standard \(MHS\), a set of standardized drivers and interfaces that let AI agents operate physical devices such as microscopes, liquid handlers, and robotic arms. The company reports that integration time drops from weeks or months to hours or minutes, with early partners including Genentech, Carnegie Mellon University, and QuEra. This could be a major step toward making AI agents useful beyond software, enabling automated scientific research and manufacturing. The standard may also establish a common protocol similar to the Model Context Protocol \(MCP\), accelerating the adoption of AI-controlled hardware across industries. MHS includes built-in safety checks and human approval gates for high-risk actions. Notably, QuEra&\#x27;s AI controller recovered quantum computer laser locks without human intervention in 99.3% of cases, and Anthropic plans to open-source the standard after completing safety evaluations.

telegram · zaihuapd · Aug 28, 01:38

**Background**: Modern AI agents like Claude often lack a standardized way to interface with physical hardware, making it time-consuming to adapt them for labs or factories. MHS aims to solve that with common drivers, orchestration logic, and safety layers, much like how MCP standardizes software integration. The research preview includes partners in biotech, robotics, and quantum computing, and is being tested for tasks like automated microscopy and quantum laser tuning.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/model-hardware-standard-research-preview">Previewing the Model Hardware Standard \ Anthropic</a></li>
<li><a href="https://arstechnica.com/ai/2026/08/anthropics-new-hardware-standard-lets-ai-agents-control-the-physical-world/">Anthropic &#x27;s new hardware standard lets AI agents... - Ars Technica</a></li>
<li><a href="https://quantumzeitgeist.substack.com/p/queras-ai-now-tunes-quantum-lasers">QuEra’s AI now tunes quantum lasers in seconds, not minutes</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#AI agents`, `#Model Hardware Standard`, `#robotics`, `#AI infrastructure`

---

<a id="item-12"></a>
## [OpenAI Developing Persistent Codex Agent That Keeps Working Until Sleep](https://www.wired.com/story/openai-is-developing-a-persistent-ai-agent/) ⭐️ 8.0/10

OpenAI is reportedly adding a &\#x27;persistent mode&\#x27; to its Codex CLI that lets the coding agent keep working until it is put to sleep, proactively creating its own follow-up tasks across sessions. The company confirmed it is testing the feature but has no near-term launch plans. This signals a shift from reactive AI assistants to proactive, autonomous agents that can work continuously, potentially transforming developer workflows and productivity. It could also push the broader AI agent industry toward longer-running, self-directed systems while raising safety and control concerns. Persistent mode does not expand what the agent is allowed to do; altering anything outside the user&\#x27;s own system still requires prior approval. By March 2026, Codex had grown to over 2 million weekly active users, and OpenAI was positioning it as a broader enterprise agent platform.

telegram · zaihuapd · Aug 28, 02:47

**Background**: Codex is an AI coding agent developed by OpenAI, released in April 2025 as Codex CLI, and available through ChatGPT&\#x27;s web app, a desktop app, and IDE integrations. Traditional Codex sessions stop after minutes or hours, so persistent mode aims to keep the agent working across sessions. The safety safeguards are intended to limit the risks of a continuously operating AI agent.

<details><summary>References</summary>
<ul>
<li><a href="https://www.wired.com/story/openai-is-developing-a-persistent-ai-agent/">OpenAI Is Developing a ‘ Persistent ’ AI Agent | WIRED</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_%28AI_agent%29">OpenAI Codex (AI agent)</a></li>
<li><a href="https://www.thejapantimes.jp/Technology/721802-openai-tests-persistent-mode-for-codex-ai-agent.html">The Japan Times - OpenAI Tests &#x27; Persistent Mode &#x27; for Codex AI Agent</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#Codex`, `#AI agent`, `#autonomous coding`

---

<a id="item-13"></a>
## [US Judge Blocks Pentagon&\#x27;s Ban on Anthropic](https://www.bloomberg.com/news/articles/2026-08-28/anthropic-wins-court-challenge-to-us-supply-chain-risk-label?srnd=phx-technology) ⭐️ 8.0/10

A US district judge in San Francisco ruled that the Trump administration must lift the ban on using Anthropic&\#x27;s AI in federal agencies, finding that the Pentagon&\#x27;s supply chain risk designation lacked sufficient justification and was retribution for Anthropic&\#x27;s criticism of the government. This ruling sets a legal precedent limiting the government&\#x27;s ability to use supply chain risk designations against domestic AI companies, and it directly affects whether federal agencies can use Claude, a leading frontier model authorized for top-secret military networks. It also signals how courts may handle disputes between the government and AI contractors. Anthropic sued after the Pentagon designated it a supply chain risk and banned agency use, following the collapse of military AI negotiations. The judge also indicated that the designation was intended to send a warning to other companies rather than reflecting genuine concerns about model security.

telegram · zaihuapd · Aug 28, 03:15

**Background**: A supply chain risk designation is a government contracting tool used to exclude companies from federal procurement on national security grounds. Anthropic&\#x27;s Claude was reportedly the primary frontier model authorized for top-secret military networks, making the ban especially consequential. Separately, a Presidential Directive ordered agencies to cease all use of Anthropic products, which remains a distinct legal instrument beyond this court ruling. The case is widely seen as a test of how the government handles AI companies that publicly dispute its policies.

<details><summary>References</summary>
<ul>
<li><a href="https://www.lesswrong.com/posts/NwtrG8v9BTq3FyHZh/anthropic-vs-usg-what-will-happen-by-may-1st-long-careful">Anthropic vs USG. What will happen by May 1st? — LessWrong</a></li>
<li><a href="https://www.linkedin.com/posts/eman-taha-12867321a_openai-sweeps-in-to-snag-pentagon-contract-activity-7433633142197886976-6Uc_">US Govt Designates Domestic AI Co as Supply Chain Risk | LinkedIn</a></li>
<li><a href="https://www.taftlaw.com/news-events/law-bulletins/us-government-bans-use-of-anthropic-products-what-this-means-for-government-contractors-and-ai-strategy/?trk=article-ssr-frontend-pulse_little-text-block">U . S . Government Bans Use of Anthropic Products: What... | Taft Law</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Anthropic`, `#Policy`, `#Legal`, `#Government`

---

<a id="item-14"></a>
## [Tencent Hunyuan Releases Hy4 Preview, Outperforming Rivals in Blind Test](https://mp.weixin.qq.com/s/ymr3X878B8oa2XP15CH8TQ) ⭐️ 8.0/10

Tencent Hunyuan released Hy4 preview, an open-source model that scored 2.99/4.00 in a blind test of 203 engineering tasks, slightly beating GLM-5.3 and Kimi K3. With its Hyra agent, it also improved the lower bound for the three-dimensional Blaschke–Lebesgue volume problem to 0.41104. This marks a significant open-source release from a major Chinese tech firm, competitive with leading models. The mathematical advance brings the Blaschke–Lebesgue problem within about 2% of a final proof, showing AI&\#x27;s potential in research. The blind test involved 163 experts evaluating 203 engineering tasks. The volume lower bound of 0.41104 remains below Meissner&\#x27;s tetrahedra volume of about 0.419860, leaving a roughly 2% gap to the conjectured optimum.

telegram · zaihuapd · Aug 28, 06:11

**Background**: The Blaschke–Lebesgue problem asks for the minimum-volume convex body of constant width in three dimensions; the conjectured minimum is the Meissner tetrahedron. Hyra is Hunyuan Research Agent, an agent designed for recursive self-improvement in research and engineering tasks. Tencent confirmed Hy4 is a next-generation multimodal model currently in training, with the preview focusing on engineering and reasoning capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Blaschke%E2%80%93Lebesgue_theorem">Blaschke – Lebesgue theorem - Wikipedia</a></li>
<li><a href="https://arxiv.org/pdf/2606.01754">An Improved Lower Bound for the Three-Dimensional...</a></li>
<li><a href="https://hy.tencent.com/">Tencent Hy</a></li>

</ul>
</details>

**Tags**: `#AI/ML`, `#open-source`, `#model-release`, `#Tencent-Hunyuan`, `#reasoning`

---