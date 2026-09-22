---
layout: default
title: "Horizon Summary: 2026-09-22 (EN)"
date: 2026-09-22
lang: en
---

> From 38 items, 5 important content pieces were selected

---

1. [Xiaomi open-sources MiMo-V2.6 Pro and Flash MoE models](#item-1) ⭐️ 8.0/10
2. [NASA&\#x27;s Mars Sample Return mission has been cancelled](#item-2) ⭐️ 8.0/10
3. [Bryan Cantrill on What Sun Microsystems Got Wrong](#item-3) ⭐️ 8.0/10
4. [Cloudflare Python Workers reach general availability with PEP 783 package support](#item-4) ⭐️ 8.0/10
5. [Mapping Mixture-of-Experts Models onto Inference Hardware](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Xiaomi open-sources MiMo-V2.6 Pro and Flash MoE models](https://mimo.xiaomi.com/mimo-v2-6) ⭐️ 8.0/10

Xiaomi&\#x27;s MiMo team released and open-sourced the MiMo-V2.6 family on September 22, comprising a flagship MiMo-V2.6-Pro \(1.02T total / 42B activated parameters\) and an efficiency-focused MiMo-V2.6-Flash \(309B total / 15B activated\), both native omnimodal models targeting coding, computer-use, 3D and audio-visual agent tasks. A high-throughput Pro-UltraSpeed variant is also rolling out, and the team has opened web demos, an API, Hugging Face checkpoints, 7,000 diverse environments and its full reinforcement-learning framework. A Chinese hardware-and-devices company shipping frontier-class open weights with unusually complete training disclosure raises the bar for what &quot;open&quot; releases look like, and it intensifies competition with US labs on both capability and cost. If MiMo-V2.6-Pro really performs on par with Claude Opus 5 and GPT-5.6 Sol on agent benchmarks, it gives developers a far cheaper self-hostable alternative for agentic workloads. The two variants are mixture-of-experts architectures, so only the activated parameters \(42B and 15B\) are used per token despite the trillion- and 309-billion-parameter totals, keeping inference costs far below dense models of comparable size. Xiaomi claims Pro-UltraSpeed can deliver up to roughly 20x higher output speed at equivalent quality, and the release includes the realtime training dashboard, a detailed tech report, plus Qwen models distilled from MiMo training trajectories.

hackernews · volf\_ · Sep 21, 20:12 · [Discussion](https://news.ycombinator.com/item?id=49792730)

**Background**: Mixture-of-experts \(MoE\) is a neural network design in which many specialized sub-networks \(&quot;experts&quot;\) exist alongside a gating mechanism that routes each input to only a few of them, giving very large total capacity at a fraction of the compute. Xiaomi&\#x27;s MiMo is the company&\#x27;s in-house large-model line led by Luo Fuli, and this release emphasizes &quot;building in public&quot; through scaled reinforcement learning with a live training dashboard. Open-weight releases typically publish only the final model weights, which is why the additional disclosure of data, methodology and RL environments is notable.

<details><summary>References</summary>
<ul>
<li><a href="https://mimo.mi.com/">Xiaomi MiMo-V2.6 Series: 3 New Models Officially Released</a></li>
<li><a href="https://openrouter.ai/xiaomi/mimo-v2.6-pro-ultraspeed">MiMo-V2.6-Pro-UltraSpeed - API Pricing &amp; Providers | OpenRouter</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly positive but split on definitions: one praised the realtime training dashboard and tech report as an excellent learning tool while noting the debate over what counts as a truly open model. Others said they are now more excited about Chinese models than American ones, mainly because of affordability, and several dug into specifics such as the exact parameter counts and links to the Hugging Face RL checkpoints, with one wry observation that these models all seem to love the &quot;01 - UPPERCASE TEXT&quot; web-design motif.

**Tags**: `#llm`, `#open-source`, `#xiaomi`, `#mixture-of-experts`, `#model-release`

---

<a id="item-2"></a>
## [NASA&\#x27;s Mars Sample Return mission has been cancelled](https://www.science.org/content/article/nasa-s-mars-sample-return-mission-dead) ⭐️ 8.0/10

NASA has reportedly abandoned its flagship Mars Sample Return \(MSR\) mission, the NASA-ESA campaign approved in 2022 to retrieve rock and dust samples cached on Mars by the Perseverance rover. The cancellation ends, at least for now, the multi-mission architecture of a NASA Sample Retrieval Lander, a NASA-built Mars Ascent Vehicle, and an ESA Earth Return Orbiter. This is a major setback for planetary science: after the Apollo-era Moon rocks, MSR was meant to be the first mission to bring pristine Martian material to terrestrial laboratories for life-detection and geochronology work that rovers cannot perform on-site. The vacuum is likely to be filled by China&\#x27;s Tianwen-3, which is targeting a 2028 launch and a sample return around 2030-2031, raising concerns about US leadership in deep-space science. The mission&\#x27;s projected cost had ballooned to roughly $8-11 billion with samples not returning until around 2040, and critics note the architecture was designed around legacy launch vehicles such as Ariane 64 rather than newer, cheaper heavy-lift options like Starship or New Glenn. By comparison, the Apollo missions returned 842 pounds \(about 382 kg\) of lunar rock, while MSR was designed to bring back only about 1.1 pounds \(roughly 0.5 kg\) of Martian material.

hackernews · Muhammad523 · Sep 21, 19:14 · [Discussion](https://news.ycombinator.com/item?id=49791939)

**Background**: A Mars sample-return mission aims to collect Martian rock and dust and bring it to Earth, where far more sensitive instruments than any rover can carry can analyze it for signs that Mars once hosted life. NASA&\#x27;s Perseverance rover has been drilling and sealing such samples in titanium tubes on the surface since it landed in 2021, and the NASA-ESA Mars Sample Return campaign was formally approved in 2022 to go and fetch them. ESA&\#x27;s contribution was the Earth Return Orbiter, while NASA was to supply the lander and ascent vehicle that would launch the sample container off Mars. China&\#x27;s parallel Tianwen-3 mission plans a dual-launch architecture during the December 2028-January 2029 Mars launch window, building on landing technology from Tianwen-1 and the Chang&\#x27;e-5 and Chang&\#x27;e-6 lunar sample returns.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mars_sample-return_mission">Mars sample-return mission</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tianwen-3">Tianwen-3 - Wikipedia</a></li>
<li><a href="https://www.space.com/astronomy/mars/china-on-track-to-launch-mars-sample-return-mission-in-2028-if-accurate-this-represents-a-sputnik-moment">China on track to launch Mars sample-return mission in 2028: &#x27;If accurate, this represents a Sputnik moment&#x27; | Space</a></li>

</ul>
</details>

**Discussion**: Commenters largely accepted that the bloated $8-11B, 2040-era architecture had to go, with several blaming JPL leadership for designing around legacy rockets instead of Starship or New Glenn, and one arguing the article reads like &quot;self-pity propaganda&quot; from institutions tied to the old funding model. Others highlighted China&\#x27;s Tianwen-3 as the real competitive context, and a former ExoMars contributor noted how repeatedly delayed European missions like the Rosalind Franklin rover \(now targeting 2028\) show how fragile planetary exploration schedules have become.

**Tags**: `#space exploration`, `#NASA`, `#science-policy`, `#aerospace-engineering`, `#research-funding`

---

<a id="item-3"></a>
## [Bryan Cantrill on What Sun Microsystems Got Wrong](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) ⭐️ 8.0/10

Bryan Cantrill published a retrospective blog post titled &quot;What Sun got wrong,&quot; examining the strategic and technical missteps that led to Sun Microsystems&\#x27; decline. The post quickly drew a dense Hacker News discussion in which former customers and engineers traded anecdotes about Solaris, SPARC, and Sun&\#x27;s sales culture. Sun&\#x27;s collapse and absorption by Oracle in 2010 remains one of the canonical case studies of how a once-dominant vertically integrated systems vendor can lose its market, and Cantrill writes as a former insider rather than a detached historian. The discussion matters today because the same tensions — proprietary versus commodity hardware, open source strategy, and cloud-era economics — still shape vendors like Oracle and the wider server industry. Cantrill is a former Sun engineer closely associated with the company&\#x27;s systems innovations, giving the piece an insider&\#x27;s perspective on decisions that outsiders usually only see the aftermath of. The specific claims in the post itself could not be verified from the available source material, since only the headline and community reaction were provided.

hackernews · chmaynard · Sep 21, 14:03 · [Discussion](https://news.ycombinator.com/item?id=49787436)

**Background**: Sun Microsystems was the company behind Solaris, a proprietary Unix operating system known for scalability and for originating innovations such as DTrace and ZFS, as well as SPARC, a RISC instruction set architecture it developed starting in the mid-1980s. Solaris was largely open-sourced in 2005 as OpenSolaris, but after Oracle acquired Sun in 2010 the project was discontinued, the kernel source became closed again, and the code was forked into Illumos; Oracle ended SPARC development in 2017. Cantrill&\#x27;s own career and reputation were built in that ecosystem, which is part of why his post-mortems carry weight in the systems community.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Solaris_operating_system">Solaris operating system</a></li>
<li><a href="https://en.wikipedia.org/wiki/SPARC_processor_architecture">SPARC processor architecture</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agree that Sun&\#x27;s engineering was first-rate but its business execution was not: one describes the miserable, quote-revision-heavy purchasing process for Sun and DEC hardware versus buying a Dell server next-day, another lists concrete 2000s blunders such as briefly cancelling Solaris on x86 in 2002 and failing to reach a deal with Google. Others share nostalgia for Sun thin clients and Pine/vi workflows, and one quips that Sun &quot;was never interested in running a business,&quot; caring more about building amazing technology than selling it.

**Tags**: `#Sun Microsystems`, `#systems`, `#Solaris`, `#SPARC`, `#tech history`

---

<a id="item-4"></a>
## [Cloudflare Python Workers reach general availability with PEP 783 package support](https://blog.cloudflare.com/python-workers-ga/) ⭐️ 8.0/10

Cloudflare announced the general availability of Python Workers, which run CPython compiled to WebAssembly \(via Pyodide\) directly on the Workers edge runtime rather than in a container. The release also brings first-class package support standardized through PEP 783, which introduces the &quot;pyemscripten&quot; platform tag for wheels built for Pyodide, along with upstream contributions that let HTTP clients like Requests route through the JavaScript fetch API. Python is one of the most widely used languages in the world, so supporting it natively on a serverless edge platform removes a major adoption barrier for developers who would otherwise need containers or a second language. Standardizing WASM package distribution via PEP 783 could also benefit the broader Pyodide/Emscripten ecosystem beyond Cloudflare, since it gives package maintainers a shared target for shipping prebuilt wheels. A key enabler was JSPI \(JavaScript Promise Integration\) support contributed upstream to urllib3, which made synchronous Python HTTP clients like Requests usable under WebAssembly. PEP 783 defines the &quot;pyemscripten&quot; platform tag for wheels built to run under Pyodide, and the relevant CPython version is compiled to WebAssembly rather than being a native runtime; some architectural constraints of the Workers model reportedly remain.

hackernews · torutofu · Sep 21, 13:38 · [Discussion](https://news.ycombinator.com/item?id=49787142)

**Background**: Cloudflare Workers is a serverless platform that runs code at the network edge using the V8 engine and isolates rather than containerized language runtimes, which is what makes it fast to start but historically JavaScript/WASM-centric. Pyodide is a distribution of CPython compiled to WebAssembly that lets Python run in the browser and Node.js. PEP stands for Python Enhancement Proposal, the numbered design documents through which the Python community standardizes changes such as the new pyemscripten wheel tag described in PEP 783.

<details><summary>References</summary>
<ul>
<li><a href="https://peps.python.org/pep-0783/">PEP 783 – Emscripten Packaging - Python Enhancement Proposals</a></li>
<li><a href="https://github.com/pyodide/pyodide">GitHub - pyodide/pyodide: Pyodide is a Python distribution for the browser and Node.js based on WebAssembly · GitHub</a></li>
<li><a href="https://developers.cloudflare.com/workers/reference/how-workers-works/">How Workers works · Cloudflare Workers docs</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion was broadly positive but nuanced: an urllib3 maintainer clarified that funding for the upstream Pyodide/JSPI work went to the external contributor who implemented it rather than to the maintainers, highlighting underappreciated maintenance dynamics. Wasmer&\#x27;s founder praised Cloudflare&\#x27;s progress on package support while noting remaining architectural constraints from the original launch, and other commenters drew sharp historical parallels to Google App Engine&\#x27;s 2008 Python launch, with some joking about the phrase &quot;Python Workers&quot; implying Python developers being replaced.

**Tags**: `#cloudflare-workers`, `#python`, `#webassembly`, `#serverless`, `#pyodide`

---

<a id="item-5"></a>
## [Mapping Mixture-of-Experts Models onto Inference Hardware](https://newsletter.semianalysis.com/p/computation-and-data-movement-for) ⭐️ 8.0/10

SemiAnalysis published a technical deep-dive analyzing how Mixture-of-Experts \(MoE\) models are mapped onto inference hardware, covering model structure, data movement, and efficient serving. Rather than announcing a new model or product, the piece explains the systems-level mechanics of running MoE inference in production. MoE architectures underpin many of today&\#x27;s most capable large models, including GPT-4, Gemini, and Mixtral, so understanding how they map onto hardware directly affects inference latency, throughput, and cost. As inference becomes a real-time, revenue-generating workload, data movement rather than raw compute is emerging as the primary system bottleneck, making this analysis valuable for ML systems and infrastructure engineers. The core trade-off of MoE is that it splits weights into many experts and activates only a few per token, offering the speed of a small model with the knowledge of a large one — but at the cost of much higher memory requirements. This means serving efficiency depends heavily on how experts are placed and shuttled across memory and compute, and many capacity calculators get the memory math wrong.

rss · Semianalysis · Sep 21, 18:14

**Background**: Mixture-of-Experts \(MoE\) is a neural network design that replaces a single dense feed-forward layer with many parallel &\#x27;expert&\#x27; sub-networks plus a routing mechanism that selects only a few experts for each input token. LLM serving is the practice of deploying such trained models in production to handle user prompts and generate responses, where latency, throughput, and cost are the key operational metrics. Because MoE models keep all experts in memory but use only a fraction per token, inference becomes as much a memory-and-interconnect problem as a compute problem.

<details><summary>References</summary>
<ul>
<li><a href="https://localmodel.run/guides/mixture-of-experts">Mixture of experts (MoE) explained for local LLMs · localmodel.run</a></li>
<li><a href="https://davision.ca/memory-bottleneck-ai-inference/">Why AI inference is turning memory into the bottleneck</a></li>
<li><a href="https://docs.anyscale.com/llm/serving/intro">What is LLM serving? | Anyscale Docs</a></li>

</ul>
</details>

**Tags**: `#MoE`, `#Inference`, `#AI Hardware`, `#Systems`, `#LLM Serving`

---