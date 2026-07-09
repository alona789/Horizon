---
layout: default
title: "Horizon Summary: 2026-07-09 (EN)"
date: 2026-07-09
lang: en
---

> From 37 items, 14 important content pieces were selected

---

1. [OpenAI Releases GPT-5.6 with SOTA on ARC-AGI-3](#item-1) ⭐️ 9.0/10
2. [Bun Rewritten from Zig to Rust](#item-2) ⭐️ 9.0/10
3. [TypeScript 7.0 Released: Go Rewrite Yields Up to 12x Speed Boost](#item-3) ⭐️ 9.0/10
4. [EU Parliament Approves Chat Control 1.0 Amid Controversy](#item-4) ⭐️ 8.0/10
5. [Tencent's Hy3 Small but Capable AI Model Competes with DeepSeek V4 Flash](#item-5) ⭐️ 8.0/10
6. [No Leap Second in December 2026](#item-6) ⭐️ 8.0/10
7. [Meta Releases Muse Spark 1.1 with Agentic Capabilities](#item-7) ⭐️ 8.0/10
8. [GPT-Live: OpenAI's New Voice Mode with GPT-5.5 Delegation](#item-8) ⭐️ 8.0/10
9. [Meta's Superintelligence Progress: Compute Ramp & RL Startup](#item-9) ⭐️ 8.0/10
10. [IMGNet: Face Verification via Sign Pattern Matching](#item-10) ⭐️ 8.0/10
11. [Ant Group Open-Sources LingBot-Video, First MoE Embodied Video Model](#item-11) ⭐️ 8.0/10
12. [DJI EV50 Drone Sets Altitude Record Flying Over Everest at 8861m](#item-12) ⭐️ 8.0/10
13. [National Supercomputing Internet Core Node Launches in Zhengzhou](#item-13) ⭐️ 8.0/10
14. [OpenAI and US Department of War Agree to Ban AI for Domestic Surveillance](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Releases GPT-5.6 with SOTA on ARC-AGI-3](https://openai.com/index/gpt-5-6/) ⭐️ 9.0/10

OpenAI released GPT-5.6, its latest flagship model, achieving a new state-of-the-art score of 7.8% on the ARC-AGI-3 benchmark. The model comes in three sizes: Luna, Terra, and Sol. Setting a new benchmark on ARC-AGI-3 demonstrates significant progress in agentic intelligence, as the model can now beat an ARC-AGI-3 game for the first time. This release reinforces OpenAI's lead in frontier AI capabilities and offers three tiers to suit different deployment needs. According to the developer guide, GPT-5.6 has improved intent understanding and preserves original image dimensions. Sol is the first verified frontier model to beat an ARC-AGI-3 game, scoring 7.8%.

hackernews · logickkk1 · Jul 9, 17:04 · [Discussion](https://news.ycombinator.com/item?id=48849066)

**Background**: ARC-AGI-3 is an interactive benchmark for agentic intelligence, requiring models to explore, infer goals, and plan actions in novel environments without explicit instructions. GPT-5.6 is OpenAI's latest model, succeeding GPT-5.5, and is available in three sizes named after celestial bodies: Luna (small), Terra (medium), and Sol (large). The model is accessible via the OpenAI API.

<details><summary>References</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">Arc-agi-3</a></li>
<li><a href="https://arxiv.org/abs/2603.24621">ARC-AGI-3: A New Challenge for Frontier Agentic Intelligence</a></li>
<li><a href="https://arcprize.org/leaderboard">ARC-AGI-3 Leaderboard - ARC Prize</a></li>

</ul>
</details>

**Discussion**: Community members noted interesting semantic tips in the developer guide and shared their own tests. One user reported that GPT-5.6 Terra's performance on a toy RTS game was similar to GPT-5.5 and behind Sonnet 5. Another user pointed out that OpenAI excluded Fable 5 from comparisons because it refuses advanced biology questions, which was seen as a 'winner by default' situation.

**Tags**: `#AI`, `#GPT`, `#OpenAI`, `#Large Language Models`, `#Machine Learning`

---

<a id="item-2"></a>
## [Bun Rewritten from Zig to Rust](https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/#atom-everything) ⭐️ 9.0/10

Jarred Sumner, the creator of Bun, has rewritten the entire JavaScript runtime from Zig to Rust using AI coding agents, and the new version is now powering Claude Code. This rewrite challenges the long-held belief that large codebases should never be rewritten, showing that AI-assisted porting can be feasible and cost-effective, while also significantly improving memory safety by leveraging Rust's ownership model. The rewrite cost approximately $165,000 in API tokens, consuming 5.9 billion uncached input tokens and 690 million output tokens. The TypeScript test suite, with over a million assertions, served as a conformance suite to validate the port.

rss · Simon Willison · Jul 8, 23:57

**Background**: Bun is a fast JavaScript runtime, similar to Node.js or Deno, originally written in Zig, a system programming language that requires manual memory management. Rust, in contrast, enforces memory safety at compile time through its ownership system. The rewrite was made possible by advances in AI coding agents, which can autonomously port large codebases under human supervision.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>
<li><a href="https://simonwillison.net/guides/agentic-engineering-patterns/what-is-agentic-engineering/">What is agentic engineering? - Agentic Engineering Patterns - Simon Willison's Weblog</a></li>
<li><a href="https://asdlc.io/patterns/adversarial-code-review/">Adversarial Code Review | ASDLC.io</a></li>

</ul>
</details>

**Tags**: `#Bun`, `#Rust`, `#Zig`, `#JavaScript runtime`, `#software engineering`

---

<a id="item-3"></a>
## [TypeScript 7.0 Released: Go Rewrite Yields Up to 12x Speed Boost](https://devblogs.microsoft.com/typescript/announcing-typescript-7-0/) ⭐️ 9.0/10

Microsoft has released TypeScript 7.0, a native version rewritten in Go that achieves 8-12x faster full builds and supports shared-memory multithreading. Users can install it via npm and editors can use the new language server through LSP. This major update dramatically improves developer productivity by reducing build times, and it paves the way for future performance enhancements in the TypeScript ecosystem. However, toolchains for embedded languages like Vue and Svelte are not yet compatible, which may temporarily fragment the ecosystem. TypeScript 7.0 introduces --checkers and --builders flags to customize parallelism, and provides a compatibility package to coexist with TypeScript 6. The Go rewrite targets the compiler and language server, not the language runtime, so TypeScript code execution speed remains unchanged.

telegram · zaihuapd · Jul 9, 04:01

**Background**: TypeScript is a superset of JavaScript that adds static typing, and its compiler (tsc) has historically been written in TypeScript itself, leading to performance bottlenecks as projects grow. The Go rewrite addresses this by leveraging Go's native compilation and concurrency, resulting in 8-12x faster builds. The Language Server Protocol (LSP) enables editors to provide language features like auto-completion and error checking, and TypeScript 7.0's new LSP support ensures broad editor compatibility.

<details><summary>References</summary>
<ul>
<li><a href="https://www.totaltypescript.com/typescript-announces-go-rewrite">TypeScript Announces Go Rewrite, Achieves 10x Speedup | Total TypeScript</a></li>
<li><a href="https://en.wikipedia.org/wiki/Language_Server_Protocol">Language Server Protocol</a></li>

</ul>
</details>

**Tags**: `#TypeScript`, `#性能优化`, `#微软`, `#Go`

---

<a id="item-4"></a>
## [EU Parliament Approves Chat Control 1.0 Amid Controversy](https://www.patrick-breyer.de/en/eu-parliament-greenlights-chat-control-1-0-breyer-our-children-lose-out/) ⭐️ 8.0/10

On July 9, 2025, the European Parliament approved a temporary derogation from the ePrivacy Directive, allowing US tech companies to voluntarily scan private messages for child sexual abuse material until 2028, despite the fact that a majority of voting MEPs opposed it. This decision effectively legalizes mass surveillance of private communications for millions of users across platforms like Instagram, Gmail, and Skype, setting a concerning precedent for digital privacy and encryption in the EU. The measure was adopted because the motion to reject it required an absolute majority of all 705 MEPs (361 votes), not just those present. Only 276 voted in favor, while 314 voted against and 17 abstained, but 113 were absent, leaving the rejection short.

hackernews · rapnie · Jul 9, 11:03 · [Discussion](https://news.ycombinator.com/item?id=48843923)

**Background**: The so-called 'Chat Control 1.0' is a temporary extension of earlier voluntary scanning measures, grounded in client-side scanning technology that analyzes message content on the device before encryption. This follows the EU's broader 'Chat Control' proposal from 2022, which aims to combat child sexual abuse material online but has sparked major privacy and encryption debates.

<details><summary>References</summary>
<ul>
<li><a href="https://www.internetsociety.org/resources/doc/2020/fact-sheet-client-side-scanning/">Fact Sheet: Client-Side Scanning - Internet Society</a></li>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control">Chat Control - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters expressed outrage at the procedural manipulation, noting that the vote was held just before summer break and required an absolute majority to reject. Many criticized the framing as 'think of the children' and warned of totalitarian implications, while one pointed out that the EU is used to launder unpopular domestic laws.

**Tags**: `#surveillance`, `#privacy`, `#EU legislation`, `#encryption`, `#civil liberties`

---

<a id="item-5"></a>
## [Tencent's Hy3 Small but Capable AI Model Competes with DeepSeek V4 Flash](https://hy.tencent.com/research/hy3) ⭐️ 8.0/10

Tencent released Hy3, a 295B-parameter Mixture-of-Experts model with 21B active parameters, which rivals the performance of DeepSeek V4 Flash and even V4 Pro on some benchmarks. Hy3 demonstrates that very capable AI models can run with relatively low computational cost, potentially making advanced AI more accessible for local deployment and lowering inference expenses. Hy3 has 295B total parameters but only 21B active per token, plus a 3.8B MTP layer; it supports agent tasks and is already integrated into Tencent's Marvis OS assistant and WeChat/Weixin scenarios.

hackernews · andai · Jul 9, 15:27 · [Discussion](https://news.ycombinator.com/item?id=48847552)

**Background**: Mixture-of-Experts (MoE) models divide the network into specialized 'experts' and only activate a subset for each input, allowing large total parameter counts with high efficiency. Active parameters determine the computational cost per token. Hy3's active parameter count (21B) places it between DeepSeek V4 Flash (13B active) and V4 Pro (49B active), offering a balance of capability and efficiency.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Tencent-Hunyuan/Hy3">GitHub - Tencent-Hunyuan/Hy3: Hy3 (295B A21B), a leading ...</a></li>
<li><a href="https://www.tencent.com/en-us/articles/2202386.html">Tencent Hunyuan Officially Releases Hy3, Advancing Agent ...</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/DeepSeek-V4-Flash · Hugging Face</a></li>

</ul>
</details>

**Discussion**: Community members are intrigued by Hy3's capability given its small active parameters, with some noting it rivals larger models on benchmarks. However, pricing confusion and the availability of a free tier on OpenRouter until July 21st have spurred discussion. Some question whether Hy3 offers enough advantage over DeepSeek V4 Flash to warrant adoption, especially for local deployment.

**Tags**: `#AI model`, `#LLM`, `#performance`, `#Tencent`, `#comparison`

---

<a id="item-6"></a>
## [No Leap Second in December 2026](https://datacenter.iers.org/data/latestVersion/bulletinC.txt) ⭐️ 8.0/10

The International Earth Rotation and Reference Systems Service (IERS) announced that no leap second will be introduced at the end of December 2026, maintaining the current UTC offset. This decision prevents potential disruptions to computer systems and networks that rely on precise timekeeping, and reflects ongoing discussions about the future of leap seconds in global time standards. The difference between UTC and International Atomic Time (TAI) remains at -37 seconds, and the UTC-GPS offset stays at -18 seconds, as per the IERS Bulletin C.

hackernews · ChrisArchitect · Jul 9, 14:16 · [Discussion](https://news.ycombinator.com/item?id=48846281)

**Background**: Leap seconds are occasionally added to Coordinated Universal Time (UTC) to keep it within 0.9 seconds of astronomical time (UT1), which is based on Earth's rotation. Earth's rotation is unpredictable due to geological activity, weather, and other factors, leading to irregular leap seconds. The IERS monitors Earth rotation and announces leap seconds when needed.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Leap_second">Leap second - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/International_Earth_Rotation_and_Reference_Systems_Service">International Earth Rotation and Reference Systems Service</a></li>

</ul>
</details>

**Discussion**: Commenters questioned the unpredictability of Earth's rotation and the impact on UNIX timestamps and minimally maintained systems. Others noted the specific offsets between UTC, TAI, and GPS time scales, indicating technical engagement with timekeeping details.

**Tags**: `#leap second`, `#timekeeping`, `#UTC`, `#IERS`, `#earth rotation`

---

<a id="item-7"></a>
## [Meta Releases Muse Spark 1.1 with Agentic Capabilities](https://ai.meta.com/blog/introducing-muse-spark-meta-model-api/) ⭐️ 8.0/10

Meta has released Muse Spark 1.1, an AI model with enhanced agentic capabilities that can autonomously plan and execute tasks using tools. The model is available via API and comes with a new evaluation report and pricing. This release marks Meta's entry into the competitive frontier of agentic AI, offering a cheaper alternative to models from OpenAI and Anthropic while potentially disrupting their revenue. It also reignites debate on open-source strategy and evaluation standards. The evaluation report for Muse Spark 1.1 has been criticized for overriding resource caps in Terminal-Bench 2.1 tests, potentially invalidating results. Pricing is notably low at $1.25/$4.5 per million tokens for input/output, with cached input at $0.15.

hackernews · ot · Jul 9, 14:10 · [Discussion](https://news.ycombinator.com/item?id=48846184)

**Background**: Agentic AI refers to systems that can autonomously plan, use tools, and adapt to accomplish goals with limited supervision. Muse Spark is Meta's first natively multimodal reasoning model supporting text, image, and speech input, with a 262k token context window. It represents Meta's push toward personal superintelligence.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.meta.com/blog/introducing-muse-spark-msl/">Introducing Muse Spark: Scaling Towards Personal Superintelligence</a></li>
<li><a href="https://artificialanalysis.ai/models/muse-spark">Muse Spark - Intelligence, Performance & Price Analysis</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained - MIT Sloan</a></li>

</ul>
</details>

**Discussion**: Community reactions are mixed: some criticize the evaluation methodology for violating benchmark rules, while others praise the low pricing and competitive performance. There is discussion about Meta's role as a 'spoiler' by commoditizing coding models through open weights.

**Tags**: `#Meta`, `#Muse Spark`, `#AI model`, `#open-source`, `#evaluation`

---

<a id="item-8"></a>
## [GPT-Live: OpenAI's New Voice Mode with GPT-5.5 Delegation](https://simonwillison.net/2026/Jul/8/introducing-gptlive/#atom-everything) ⭐️ 8.0/10

OpenAI has introduced GPT-Live, a new generation of voice models for ChatGPT that can delegate complex tasks to GPT-5.5 while maintaining conversation flow. This upgrade significantly improves the voice mode's capabilities and latency, making ChatGPT a much more useful assistant for real-time brainstorming and natural interaction. GPT-Live automatically delegates tasks requiring web search, deep reasoning, or complex work to GPT-5.5 behind the scenes, and seamlessly brings results back into the conversation. OpenAI plans to continuously update the backend model as new frontier models are released.

rss · Simon Willison · Jul 8, 23:20

**Background**: ChatGPT's voice mode allows users to speak with the AI conversationally. Previously, the voice mode was based on an older GPT-4o model with a knowledge cutoff in 2024, which limited its usefulness. GPT-Live uses a newer, more capable voice model that can offload heavy tasks to OpenAI's most advanced models, improving both responsiveness and accuracy.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-live/">Introducing GPT-Live | OpenAI</a></li>
<li><a href="https://openai.com/index/introducing-gpt-5-5/">Introducing GPT‑5.5 - OpenAI</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#GPT-Live`, `#ChatGPT`, `#Voice Mode`, `#AI Models`

---

<a id="item-9"></a>
## [Meta's Superintelligence Progress: Compute Ramp & RL Startup](https://newsletter.semianalysis.com/p/the-future-of-meta-superintelligence) ⭐️ 8.0/10

Meta released a progress update on its superintelligence efforts, detailing an aggressive compute ramp and the emergence of a new reinforcement learning environment startup. This update highlights Meta's intensified investment in AI infrastructure and reinforcement learning, potentially accelerating progress toward superintelligence and reshaping the competitive dynamics among tech giants. The compute ramp is described as the most aggressive ever seen, and the RL startup appeared suddenly; the update also includes advice directed at Google DeepMind.

rss · Semianalysis · Jul 9, 19:16

**Background**: Superintelligence refers to artificial intelligence that surpasses human cognitive abilities. Compute infrastructure is critical for training large-scale AI models, while reinforcement learning environments provide simulated spaces for training RL agents. Meta is competing with other major tech companies in the race toward advanced AI.

**Tags**: `#AI`, `#reinforcement learning`, `#compute infrastructure`, `#Meta`, `#deep learning`

---

<a id="item-10"></a>
## [IMGNet: Face Verification via Sign Pattern Matching](https://www.reddit.com/r/MachineLearning/comments/1urxvxh/i_built_imgnet_a_face_verification_model_that/) ⭐️ 8.0/10

IMGNet introduces a face verification model that replaces cosine similarity with sliding window sign pattern matching, achieving 96.27% on LFW with a 10.58 MB model trained on CASIA-WebFace. This work challenges the default use of cosine similarity in face verification, demonstrating that alternative similarity metrics co-designed with training objectives can achieve competitive performance while reducing model size and improving stability. The model uses three complementary metrics (IMG Sign Score, AMP IMG Score, Chain Score) that all share a single threshold, plus a voting system for decision making; when applied to ArcFace embeddings without retraining, IMG Sign Score reaches 99.58% on LFW.

reddit · r/MachineLearning · /u/img-_- · Jul 9, 18:00

**Background**: Traditional face verification models compare embedding vectors using cosine similarity, which measures the angle between vectors. IMGNet instead examines local sign patterns across overlapping windows of the embedding, looking for relational consistency rather than absolute direction.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/imghost11/imgnetV1">imghost11/imgnetV1 · Hugging Face</a></li>
<li><a href="https://github.com/imamgh11/imgnet/blob/main/README.md">imgnet/README.md at main · imamgh11/imgnet · GitHub</a></li>

</ul>
</details>

**Tags**: `#face verification`, `#deep learning`, `#computer vision`, `#representation learning`

---

<a id="item-11"></a>
## [Ant Group Open-Sources LingBot-Video, First MoE Embodied Video Model](https://www.qbitai.com/2026/07/446458.html) ⭐️ 8.0/10

Ant Group has open-sourced LingBot-Video, the world's first embodied video generation foundation model based on a Mixture-of-Experts (MoE) architecture. The model has 30 billion total parameters but activates only about 3 billion per inference, achieving state-of-the-art results on the RBench benchmark with a score of 0.620. This release significantly reduces the computational cost of embodied video generation while maintaining high quality, promising to accelerate robotics research and applications. As an open-source Apache 2.0 licensed model, it enables wider access for researchers and developers working on robot learning and world models. LingBot-Video uses a DiT+MoE design to balance capacity and cost, and was trained on 70,000 hours of embodied data covering dexterous manipulation, robot mobility, and first-person interaction. A multi-dimensional reinforcement learning reward system emphasizes physical plausibility and task completion, beyond aesthetics and motion consistency.

telegram · zaihuapd · Jul 9, 04:30

**Background**: Mixture-of-Experts (MoE) is a machine learning technique that activates only a subset of model parameters per input, enabling larger models with lower inference cost. Diffusion Transformers (DiT) replace traditional U-Net architectures in video generation, offering better scalability. RBench is a robotics-oriented benchmark that evaluates video generation across five task domains and four robot embodiments. The combination of MoE and DiT in LingBot-Video achieves roughly 3x inference efficiency compared to dense models of similar size.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://dagroup-pku.github.io/ReVidgen.github.io/">Rethinking Video Generation Model for the Embodied World</a></li>
<li><a href="https://arxiv.org/abs/2507.13343">[2507.13343] Taming Diffusion Transformer for Efficient ... Video Diffusion Transformer (DiT) Overview - emergentmind.com VideoDiT: Bridging Image Diffusion Transformers for ... [2407.21705] Tora: Trajectory-oriented Diffusion Transformer ... Diffusion Transformers Explained: Why DiT Is Replacing U-Net ... Diffusion Transformers Explained: Why DiT Is Replacing U-Net ... The Diffusion Transformer Shift: Inside the Technical Re ... Images</a></li>

</ul>
</details>

**Tags**: `#embodied AI`, `#video generation`, `#MoE`, `#open-source`, `#robotics`

---

<a id="item-12"></a>
## [DJI EV50 Drone Sets Altitude Record Flying Over Everest at 8861m](https://www.163.com/dy/article/L1CUCV940514R9OJ.html) ⭐️ 8.0/10

During the 'Peak Mission' scientific expedition on Mount Everest, DJI's unreleased EV50 vertical takeoff and landing (VTOL) transport drone flew over the north slope at an altitude of 8861 meters, setting a world record for the highest flight altitude among similar publicly tested UAVs. This achievement demonstrates the capability of commercial drones to operate at extreme altitudes, opening new possibilities for high-altitude logistics, scientific research, and environmental monitoring in previously inaccessible regions. The EV50 is a composite-wing UAV that can perform vertical takeoff and landing, then switch to fixed-wing cruise for efficient flight. During the 12-day mission, it completed 32 takeoffs and landings, climbed 3730 meters continuously, and still had 30% battery remaining on return.

telegram · zaihuapd · Jul 9, 06:00

**Background**: Composite-wing UAVs combine the vertical takeoff and landing capability of multirotors with the endurance and speed of fixed-wing aircraft, making them suitable for missions requiring both flexibility and range. Atmospheric profile data refers to vertical measurements of temperature, pressure, humidity, and other atmospheric variables at different altitudes, which are critical for weather modeling and climate research. Traditional methods like weather balloons have limited duration and coverage, making drones a promising alternative for collecting such data in challenging environments.

<details><summary>References</summary>
<ul>
<li><a href="https://baike.baidu.com/item/复合翼无人机/67152229">复合翼无人机 - 百度百科</a></li>
<li><a href="https://jandan.net/p/116703">不懂物理也没关系，AI预测天 气 现在很厉害 - 煎蛋</a></li>

</ul>
</details>

**Tags**: `#drone`, `#DJI`, `#high-altitude`, `#UAV`, `#technology`

---

<a id="item-13"></a>
## [National Supercomputing Internet Core Node Launches in Zhengzhou](https://36kr.com/newsflashes/3887797387344387) ⭐️ 8.0/10

On July 9, 2026, the National Supercomputing Internet core node officially went online in Zhengzhou, providing over 100,000 domestic AI computing cards as a single resource pool. This milestone significantly boosts China's domestic AI computing capacity and demonstrates progress in building a unified national computing resource scheduling system. It could reduce reliance on foreign AI chips and support large-scale AI model training and inference across industries. The core node is the largest single domestic AI computing resource pool ever connected to the National Supercomputing Internet platform. It handles operations management, resource scheduling, and integrates services like supply-demand matching and industry incubation.

telegram · zaihuapd · Jul 9, 07:00

**Background**: The National Supercomputing Internet is a national platform that aggregates high-performance computing and AI computing resources across China into a unified network for efficient scheduling. It aims to meet the computing demands of major scientific projects, key engineering efforts, and socio-economic development. A computing resource pool (or 'computing power pool') uses virtualization and software-defined technologies to aggregate dispersed and heterogeneous computing resources, improving utilization and reducing costs.

<details><summary>References</summary>
<ul>
<li><a href="http://paper.people.com.cn/rmrb/images/2024-05/06/19/rmrb2024050619.pdf">KJZKRMRB19B20240506C</a></li>
<li><a href="https://baike.baidu.com/item/算力池化/65662046">算力池化_百度百科</a></li>

</ul>
</details>

**Tags**: `#supercomputing`, `#AI computing`, `#national infrastructure`, `#China tech`

---

<a id="item-14"></a>
## [OpenAI and US Department of War Agree to Ban AI for Domestic Surveillance](https://t.me/zaihuapd/42459) ⭐️ 8.0/10

OpenAI and the US Department of War (formerly the Department of Defense) have agreed to revise their AI contract to explicitly prohibit using the AI system for domestic surveillance of American citizens. This revision was proactively proposed by OpenAI CEO Sam Altman to address public concerns about AI-enabled mass surveillance. This agreement sets a significant precedent for AI ethics and military contracting, potentially establishing a standard for how AI companies engage with defense agencies. It addresses critical public trust issues and could influence future AI governance policies globally. The revised clause explicitly forbids using AI for deliberate surveillance of US citizens and prohibits tracking or monitoring using commercially obtained personally identifiable information. The agreement has not yet been formally signed, and similar controversy previously led Anthropic to halt its contract with the same department.

telegram · zaihuapd · Jul 9, 13:22

**Background**: The US Department of War is the rebranded name of the Department of Defense, emphasizing its military role. The original War Department existed from 1789 to 1947 before being renamed. This context is important because defense contracts with AI companies have raised ethical concerns about using AI for surveillance and autonomous weapons.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cgr9r4qr0ppo">Trump rebrands Department of Defense as Department of War</a></li>
<li><a href="https://www.war.gov/">Home | U . S . Department of War</a></li>

</ul>
</details>

**Tags**: `#AI ethics`, `#OpenAI`, `#government policy`, `#surveillance`, `#AI regulation`

---