---
layout: default
title: "Horizon Summary: 2026-11-19 (EN)"
date: 2026-11-19
lang: en
---

> From 41 items, 8 important content pieces were selected

---

1. [Google Announces Gemini 4 Neon Frontier Model](#item-1) ⭐️ 9.0/10
2. [Critical unauthenticated RCE found in Nginx HTTP/2 implementation](#item-2) ⭐️ 9.0/10
3. [Anthropic Prices IPO at $83 per Share](#item-3) ⭐️ 9.0/10
4. [Ruby Patches Seven Memory-Corruption Flaws in Regexp and String Case Conversion](#item-4) ⭐️ 8.0/10
5. [Microsoft launches seven new MAI models built for price-performance](#item-5) ⭐️ 8.0/10
6. [Google DeepMind releases Genie 4, an interactive world model with audio](#item-6) ⭐️ 8.0/10
7. [Interactive 3D site lets you take Voyager 1 apart, down to a single memory bit](#item-7) ⭐️ 8.0/10
8. [Trump Administration Weighs Public Disclosure of Chinese AI Use](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google Announces Gemini 4 Neon Frontier Model](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/) ⭐️ 9.0/10

Google announced Gemini 4 Neon, a new frontier model in the Gemini 4 family, built for complex coding, analytical reasoning, and production-grade enterprise workflows. The model is positioned as delivering frontier-level reasoning with faster end-to-end task completion for high-frequency complex work. This expands Google&\#x27;s frontier lineup and intensifies competition with Anthropic&\#x27;s Opus and other top models, giving developers another option for high-frequency complex workflows. It also shows how major AI labs are segmenting frontier models by workload rather than releasing a single general-purpose flagship. Google&\#x27;s model card says Neon balances depth and efficiency, while Carbon targets the hardest long-horizon projects and Hydrogen handles fast everyday execution; Neon is intended to deliver frontier-level reasoning faster and more cost efficiently. The model is available through the Gemini API and Google AI Studio documentation.

hackernews · yigitdemirag · Nov 18, 21:34 · [Discussion](https://news.ycombinator.com/item?id=50552424)

**Background**: Frontier models are the most advanced AI systems available at a given moment, trained at massive scale to deliver state-of-the-art performance across many tasks. Gemini 4 is Google&\#x27;s frontier model family, with variants positioned for different workloads: Carbon for long-horizon projects, Hydrogen for fast everyday execution, and Neon between them.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/models/model-cards/gemini-4-neon/">Gemini 4 Neon - Model Card — Google DeepMind</a></li>
<li><a href="https://aistudio.google.com/docs/models/gemini-4-neon">Gemini 4 Neon - Gemini API | Google AI Studio</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work - NVIDIA</a></li>

</ul>
</details>

**Discussion**: Commenters focused on Neon&\#x27;s position in the Gemini 4 lineup, noting that it scores higher overall than Carbon on the AA Index but lower on research-scale evaluations such as CritPt, so Carbon remains the &\#x27;long horizon&\#x27; model. Users also debated benchmark-versus-real-world performance, with one saying Opus 5.5 feels more generally intelligent despite Gemini&\#x27;s benchmark scores, while others highlighted OpenRouter speed of about 127 tokens per second versus Carbon&\#x27;s 46 and expected tougher price competition.

**Tags**: `#AI/ML`, `#LLM`, `#Google Gemini`, `#Model Release`, `#Frontier Models`

---

<a id="item-2"></a>
## [Critical unauthenticated RCE found in Nginx HTTP/2 implementation](https://www.wiz.io/blog/nginx-http2-rce-vulnerabilities) ⭐️ 9.0/10

On November 18, 2026, F5 released security updates for two critical flaws in NGINX&\#x27;s HTTP/2 implementation, CVE-2026-123633 and CVE-2026-123007, both rated CVSS v4.0 9.2, which were independently discovered by Wiz Research, Ikotas Labs, Metnir, Rapid7 and Xint. Xint&\#x27;s broader &quot;NGINX2Root&quot; research chains five NGINX bugs plus a Linux kernel flaw to go from an unauthenticated web visitor to root on the host, and Rapid7 has already published a proof-of-concept exploit. NGINX is one of the most widely deployed web servers and reverse proxies, sitting in front of an estimated 225 million websites, so an unauthenticated, pre-authentication RCE in its HTTP/2 stack is a paradigm-level security event for internet infrastructure. Although HTTP/2 is not enabled by default, roughly 12% of servers reportedly run it, which is still an enormous number of exposed hosts at internet scale. The two CVEs stem from distinct failures in HTTP/2 processing, with CVE-2026-123007 described as a flow-control memory corruption that lets an unauthenticated attacker execute commands inside an NGINX worker process; fixes shipped in nginx 1.30.7 and 1.31.9 alongside patches for 10 CVEs total. The simplest workaround for teams that cannot upgrade immediately is to disable external HTTP/2, and there is currently no evidence of in-the-wild exploitation.

hackernews · speedping · Nov 18, 15:19 · [Discussion](https://news.ycombinator.com/item?id=50547374)

**Background**: HTTP/2 is the binary, multiplexed successor to HTTP/1.1, and its flow-control and stream-management logic runs inside NGINX worker processes that handle untrusted client traffic before any authentication happens. A memory-corruption bug in that code path is especially dangerous because the attacker needs no credentials, only a reachable HTTPS endpoint with HTTP/2 negotiated. Vulnerability disclosure norms normally involve coordinated timing between researchers and vendors, so when a public patch commit precedes an advisory, defenders have less time to react than attackers who monitor repositories.

<details><summary>References</summary>
<ul>
<li><a href="https://www.wiz.io/blog/nginx-http2-rce-vulnerabilities">Unauthenticated Remote Code Execution in NGINX... | Wiz Blog</a></li>
<li><a href="https://safe.security/resources/blog/cve-2026-123007-cve-2026-123633-nginx-http-2-rce-two-critical-flaws-turn-protocol-handling-into-remote-code-execution/">NGINX HTTP/2 RCE: CVE-2026-123007 &amp; CVE-2026-123633 | SAFE</a></li>
<li><a href="https://www.imperva.com/blog/critical-nginx-http-2-vulnerabilities-cve-2026-123633-and-cve-2026-123007-what-imperva-customers-need-to-know/">Critical NGINX HTTP/2 Vulnerabilities (CVE-2026-123633 and ...</a></li>

</ul>
</details>

**Discussion**: Commenters were sharply critical of the disclosure process, noting the fix landed in the open-source repository about a week before the advisory, with a commit message crediting Xint.io, and arguing that a simple PSA was warranted given the trivial &\#x27;disable HTTP/2&\#x27; workaround. Others offered partial reassurance that HTTP/2 is off by default and only about 12% of servers enable it, shared vulnerability-checking and mitigation links, and voiced broader alarm about automated/AI-driven exploitation leaving small operators unable to keep up.

**Tags**: `#security`, `#nginx`, `#vulnerability-disclosure`, `#remote-code-execution`, `#http2`

---

<a id="item-3"></a>
## [Anthropic Prices IPO at $83 per Share](https://www.anthropic.com/news/anthropic-prices-initial-public-offering) ⭐️ 9.0/10

Anthropic priced its initial public offering at $83 per share for 980 million shares of Class A common stock, with about 956 million shares sold by the company and 23.65 million by existing shareholders. The stock is expected to begin trading on the Nasdaq Global Select Market under the ticker ANT on November 19, 2026, and the offering is set to close on November 20, with underwriters granted a 30-day option for up to 147 million additional shares. This is a landmark moment for the AI industry: a leading frontier lab and Claude maker is moving from private to public markets at an extraordinary valuation, giving public investors direct exposure to the AI model race. The listing will be watched as a benchmark for other AI labs, including OpenAI, and could reshape how employees, investors, and competitors value AI businesses. The offering combines a primary sale of roughly 956 million shares by Anthropic with a secondary sale of about 23.65 million shares by existing holders, and Anthropic will not receive proceeds from the shareholder sales. The 30-day underwriter option for up to 147 million additional shares could increase the total deal size if exercised.

hackernews · surprisetalk · Nov 18, 23:30 · [Discussion](https://news.ycombinator.com/item?id=50553843)

**Background**: Anthropic is an American AI safety and research company, structured as a public benefit corporation, whose flagship product is the Claude family of large language models. An IPO is the process by which a private company lists shares on a public stock exchange, raising capital from public investors and allowing existing shareholders to sell; investment banks act as underwriters. In AI, a &\#x27;moat&\#x27; refers to a durable competitive advantage—such as technology, brand, switching costs, or scale—that protects a company from rivals.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>
<li><a href="https://www.investopedia.com/terms/i/ipo.asp">What Is an IPO? How an Initial Public Offering Works</a></li>
<li><a href="https://www.anthropic.com/company">Company \ Anthropic</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters are sharply divided on whether Anthropic has a durable moat: some argue it has no real moat but has nonetheless left Google and OpenAI behind, while others compare it to dot-com-era first movers like AltaVista that were later overtaken. Several commenters focused on the deal mechanics—one noted the IPO expanded from 825 million to 980 million shares and roughly $105 billion in cash, and another called allowing employees to sell immediately a bad sign—while one expressed shock at a reported $1.5 trillion market cap for a company founded in 2021.

**Tags**: `#Anthropic`, `#IPO`, `#AI industry`, `#valuation`, `#Hacker News`

---

<a id="item-4"></a>
## [Ruby Patches Seven Memory-Corruption Flaws in Regexp and String Case Conversion](https://www.ruby-lang.org/en/news/2026/11/18/multiple-vulnerabilities-in-regexp-and-string/) ⭐️ 8.0/10

Ruby released versions 3.3.14, 3.4.13 and 4.0.10 fixing seven memory-corruption vulnerabilities in the Regexp engine and in String case conversion, including a double-free \(GHSA-7x2q-68qv-6p8x\), buffer overflows during pattern compilation \(GHSA-3p8q-wmhx-vm2w\) and a one-byte heap overflow in case conversion tracked as GHSA-34m4-m9fh-gqp5 and nicknamed &quot;ruby2ßhell&quot;. The Ruby team says proof-of-concept code exists showing attacker-controlled memory corruption, and that matching against a crafted regexp may allow remote code execution in applications that accept attacker-supplied patterns. These are remotely triggerable C-level memory-safety bugs in one of the most widely deployed language runtimes, so any Ruby application that passes untrusted input to a regexp or calls downcase/upcase on attacker-controlled strings may be exposed to crashes or code execution. The fact that several flaws were reported with Anthropic&\#x27;s involvement underlines the growing role of AI-assisted bug hunting against established C codebases. Five of the seven flaws affect the regular-expression engine, and Ruby warns that applications using attacker-controlled patterns are at risk; the case-conversion bug allows a single byte to be written out of bounds for encodings such as ISO-8859-1 and Windows-1252 \(CVE-2026-132825, CVSS 7.4\). No CVE identifiers had been assigned at publication time, so the advisory refers to GitHub Security Advisory \(GHSA\) IDs instead, and only the affected version branches 3.3, 3.4 and 4.0 have fixes.

hackernews · runesoerensen · Nov 18, 23:52 · [Discussion](https://news.ycombinator.com/item?id=50554038)

**Background**: Ruby implements its regexp engine and string case conversion in C, which means mistakes in buffer sizing can corrupt memory rather than raise a clean Ruby exception. Multibyte and legacy encodings complicate this: Windows-1252, for instance, can encode the lowercase German ß but not its uppercase form, so upcasing expands &quot;ß&quot; into two characters, &quot;SS&quot;, and the code must reserve extra buffer space for that growth. When code only checks buffer headroom one character at a time, a length-expanding conversion at the end of a buffer can write past its boundary — the root cause tptacek describes in the discussion.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ruby-lang.org/en/news/2026/11/18/multiple-vulnerabilities-in-regexp-and-string/">Security advisories: multiple vulnerabilities in Regexp and ...</a></li>
<li><a href="https://cybersixt.com/originals/ruby-regexp-string-vulnerabilities">Ruby vulnerabilities: seven memory flaws fixed, RCE PoCs exist</a></li>
<li><a href="https://cybersecuritynews.com/ruby2shell-rce/">ruby2ßhell: Critical One-Byte Heap Overflow in Ruby Could ...</a></li>

</ul>
</details>

**Discussion**: Commenters dug into root causes rather than headline severity: tptacek explained how the Windows-1252 ß→&quot;SS&quot; expansion plus per-character headroom checks produces an overflow, and pentestercrab supplied a concrete Shift\_JIS proof-of-concept using a 2\*\*32+4-byte string. nickcw noted operationally that GitHub is now taking roughly four weeks to assign CVEs \(previously 2-3 days\), while rvz argued that AI models finding such bugs in mature software shows memory-unsafe languages are &quot;completely exposed&quot; and warned about abliterated models used offensively without disclosure.

**Tags**: `#security`, `#ruby`, `#memory-corruption`, `#encoding`, `#vulnerability-disclosure`

---

<a id="item-5"></a>
## [Microsoft launches seven new MAI models built for price-performance](https://microsoft.ai/news/microsoft-ignite-2026/) ⭐️ 8.0/10

At Ignite 2026, Microsoft unveiled a family of seven new in-house AI models spanning image, voice, transcription, coding, and reasoning, positioning them as &quot;world-class models at a truly exceptional price-performance.&quot; The company framed the release around the economics of running agents around the clock, arguing that as token spend skyrockets customers also need models cheap enough to do real engineering work 24/7. The launch signals that Microsoft is trying to become self-sufficient in frontier models rather than relying primarily on partner models, which could reshape how it prices and bundles AI across Azure and its developer tools. If the new models really deliver near-parity with leading systems at a lower cost, it intensifies price competition across the LLM market and narrows the moat of premium-priced labs. The models were described as built from scratch by Microsoft&\#x27;s AI team and are aimed at agentic workloads where cost per token dominates total spend; the announcement does not make them open-weight, which drew criticism from commenters who say Microsoft needs open weights to win share. Early user reports of the coding model, MAI Code 2, describe it as roughly comparable to Opus or Sol, though such impressions remain anecdotal rather than benchmark-backed.

hackernews · gmays · Nov 18, 16:08 · [Discussion](https://news.ycombinator.com/item?id=50548021)

**Background**: Microsoft historically depended on OpenAI&\#x27;s models for its flagship AI products, so shipping a full family of homegrown &quot;MAI&quot; models is a strategic shift toward building its own model stack. &quot;Price-performance&quot; in LLM inference refers to capability per unit cost — a measure that matters more than raw quality for agent pipelines that repeatedly call a model and burn through millions of tokens. A related debate concerns open-weight versus open-source: open-weight models let outsiders download and run the trained parameters \(often under restrictive licenses\), while open-source typically implies released code, data, and permissive licensing; Microsoft has previously shipped smaller models like Phi under open licenses.

<details><summary>References</summary>
<ul>
<li><a href="https://microsoft.ai/news/microsoft-ignite-2026/">Seven new world-class models at scalable price-performance ...</a></li>
<li><a href="https://www.geekwire.com/2026/microsoft-unveils-seven-homegrown-ai-models-in-bid-for-long-term-self-sufficiency/">Microsoft unveils seven homegrown AI models in new bid for ...</a></li>
<li><a href="https://www.fierce-network.com/content/open-weight-ai-vs-open-source-ai-whats-difference">Open-weight AI vs. open-source AI: What’s the difference?</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread \(532 points, 345 comments\) is broadly engaged, with one developer reporting that MAI Code 2 has been &quot;quite good&quot; for daily work and roughly on par with Opus or Sol, crediting Microsoft for starting from scratch. Others push back strategically, arguing Microsoft should release models as open-weight or risk a &quot;Windows Phone&quot; repeat, while some commenters are dismissive of the keynote as shallow and describe declining confidence in Microsoft&\#x27;s engineering leadership. A separate thread of discussion questions premium AI pricing more broadly, with one user saying they would skip the Anthropic IPO because competitive pressure from Chinese models, OpenAI, and now Microsoft makes the valuation look overpriced.

**Tags**: `#Microsoft`, `#LLMs`, `#AI models`, `#price-performance`, `#Hacker News`

---

<a id="item-6"></a>
## [Google DeepMind releases Genie 4, an interactive world model with audio](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/genie-4-now-available-project-genie/) ⭐️ 8.0/10

Google DeepMind has released Genie 4, the newest version of its Genie world model, now available through Project Genie to eligible Google AI Ultra subscribers. The model turns text and image prompts into photorealistic, explorable 3D worlds that users can shape and interact with in real time, adding real-time audio and in-world editing over previous generations. World models sit at the intersection of generative AI, game development and robotics simulation, so a stronger Genie points toward a future where interactive environments are generated rather than hand-built in a traditional engine. That could reshape how games and training simulations are authored, and it gives embodied-AI researchers a cheap source of controllable 3D worlds for evaluating agents. Access is heavily gated: the release is limited to &quot;eligible&quot; Google AI Ultra subscribers, and commenters report confusing tier and region restrictions, with some accounts still being shown references to Genie 3 rather than Genie 4. Coverage also describes the launch as a staged research preview for trusted testers, with broader availability planned later, so most developers cannot yet build on it.

hackernews · leumon · Nov 18, 18:49 · [Discussion](https://news.ycombinator.com/item?id=50550415)

**Background**: A &quot;world model&quot; is an AI system that learns the dynamics of an environment — physics, spatial relationships, object interactions and causality — and predicts what happens next, rather than merely classifying or generating outputs; modern versions power robots, autonomous driving and interactive video generation. DeepMind&\#x27;s Genie family, introduced in 2024, was the first generative interactive environment trained unsupervised from unlabeled internet videos, capable of producing action-controllable, playable 3D worlds from text, images or sketches. Genie 2, unveiled in December 2024, was positioned as a foundation world model for training and evaluating embodied agents. Genie 4 extends that line with real-time audio and editing, aiming at worlds that stay consistent as you move through them.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/models/genie/">Genie 4 — Google DeepMind</a></li>
<li><a href="https://deepmind.google/blog/genie-2-a-large-scale-foundation-world-model/">Genie 2: A large-scale foundation world model - deepmind.google</a></li>
<li><a href="https://en.wikipedia.org/wiki/World_model_%28artificial_intelligence%29">World model (artificial intelligence) - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread \(roughly 243 upvotes and 162 comments\) is dominated by frustration over pricing and access: users complain they cannot tell how to pay Google for the product, and that Ultra eligibility varies by workspace account and region. Some commenters push back on the community&\#x27;s focus, arguing there is far more talk about capability and profitability than about potentially devastating consequences, while others praise DeepMind for work that feels driven by craft rather than earnings. Several speculate that this could eventually become a new kind of game engine — &quot;Roblox on crack&quot; — and wonder whether Google would ever allow something like a GTA remake built on it.

**Tags**: `#AI`, `#generative models`, `#Google DeepMind`, `#game development`, `#simulation`

---

<a id="item-7"></a>
## [Interactive 3D site lets you take Voyager 1 apart, down to a single memory bit](https://rshekhar.com/voyager/) ⭐️ 8.0/10

Developer Raj Shekhar launched an interactive 3D website \(rshekhar.com/voyager/\) that lets visitors disassemble Voyager 1 system by system — opening its radioisotope thermoelectric generator to reveal 24 plutonium spheres, descending into the flight data computer to a single memory chip and even one memory bit, reading the Golden Record&\#x27;s cover instructions, and seeing which Deep Space Network dish on Earth is currently listening to each probe. The launch coincides with Voyager 1 passing one light-day from Earth, roughly 25.9 billion kilometers away, and is accompanied by a 4-minute companion film on YouTube. It turns a half-century-old spacecraft into an explorable hardware teardown, making abstract engineering — nuclear power, 1970s memory architecture, radio links across interstellar distances — tangible for students and enthusiasts. Because it includes live spacecraft positions and live dish tracking, it doubles as a teaching tool that connects archival hardware design to the mission&\#x27;s ongoing, still-operating reality. The site is deep-linked at the component level — for example /v1/rtg-1 for the nuclear battery, /v1/bay-4/memories for the data computer&\#x27;s chips, and /v1/bay-3/memory-1/plane-1/bit for a single bit of command computer memory — though the author acknowledged some of these paths are hard to find without the direct links. It focuses on hardware geometry and mission narrative rather than on a verified electrical simulation, and one commenter noted gaps in coverage while still praising the presentation.

hackernews · raj-shekhar · Nov 18, 16:18 · [Discussion](https://news.ycombinator.com/item?id=50548161)

**Background**: Voyager 1 launched on September 5, 1977, and has since left the Sun&\#x27;s heliosphere for interstellar space, so it cannot rely on solar panels; instead it uses a radioisotope thermoelectric generator, a &quot;nuclear battery&quot; that converts heat from decaying plutonium-238 \(half-life about 83 years\) into electricity via thermocouples. Its Flight Data System collects instrument and engineering data and transmits it as binary, and in 2024 a failed memory chip in that subsystem corrupted the downlink until engineers relocated the affected code. Communication is handled by NASA&\#x27;s Deep Space Network, whose three complexes — Goldstone in California, Madrid in Spain, and Canberra in Australia — keep a listening dish pointed at the probes.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Radioisotope_thermoelectric_generator">Radioisotope thermoelectric generator - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Voyager_1">Voyager 1 - Wikipedia</a></li>
<li><a href="https://www.skyatnightmagazine.com/news/voyager-1-transmitting-again">Voyager 1 transmitting again after computer malfunction</a></li>

</ul>
</details>

**Discussion**: The Hacker News reaction was strongly appreciative, with commenters calling it &quot;awesome&quot; and adding related projects such as goldenrecord.voyage and a decoder for the Golden Record&\#x27;s raw audio-to-image data. One commenter asked for the exact physical mechanism behind the 2024 memory-chip failure — whether it was charge-carrier erosion, a fractured interconnect, or something else — and another asked whether the site was AI-generated and whether its claims were checked against authoritative sources, reflecting a broader debate about verification in AI-assisted visualizations.

**Tags**: `#Voyager`, `#interactive visualization`, `#spacecraft engineering`, `#hardware`, `#education`

---

<a id="item-8"></a>
## [Trump Administration Weighs Public Disclosure of Chinese AI Use](https://www.reuters.com/world/china/trump-administration-weighs-forcing-us-firms-disclose-chinese-ai-use-2026-11-18/) ⭐️ 8.0/10

The Trump administration is reportedly considering a plan that would require US companies to publicly disclose their use of Chinese AI models, with the Treasury Department and the White House Office of Science and Technology Policy having discussed the proposal. The aim is to shame firms away from cheap open-weight alternatives like Alibaba&\#x27;s Qwen rather than impose formal restrictions. This would create a novel reputational-pressure lever over enterprise AI procurement, potentially reshaping how US companies choose between cheap Chinese open-weight models and domestic or allied alternatives. It signals that AI model choice is becoming a geopolitical and policy issue, affecting firms already deploying models like Qwen in production. The proposal has reportedly been discussed, but it remains unclear whether it has internal administration support or will advance into formal legislation. Airbnb&\#x27;s use of Alibaba&\#x27;s Qwen to power customer service is cited as an example of the kind of deployment that could be subject to public disclosure.

telegram · zaihuapd · Nov 19, 02:30

**Background**: Open-weight AI models are models whose trained numerical parameters are released under a license, allowing developers to download and self-host them rather than only access them through a paid API. Alibaba&\#x27;s Qwen, also known as Tongyi Qianwen, is a family of predominantly open-weight large and small language models developed by Alibaba Cloud, with many released under the Apache 2.0 license.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://www.alibabacloud.com/en/solutions/generative-ai/qwen?_p_lc=1">Qwen - Alibaba Cloud</a></li>
<li><a href="https://www.cnet.com/tech/services-and-software/openais-new-models-arent-really-open-what-to-know-about-open-weights-ai/">OpenAI&#x27;s New Models Aren&#x27;t Really Open : What to Know... - CNET</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#US-China tech`, `#AI regulation`, `#open-weight models`, `#enterprise AI adoption`

---