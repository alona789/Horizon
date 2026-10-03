---
layout: default
title: "Horizon Summary: 2026-10-03 (EN)"
date: 2026-10-03
lang: en
---

> From 31 items, 5 important content pieces were selected

---

1. [New AI Beats Top Human Stratego Player Using 34x Fewer Games](#item-1) ⭐️ 8.0/10
2. [Redis creator antirez releases ds4, a local LLM inference engine](#item-2) ⭐️ 8.0/10
3. [Greg Kroah-Hartman Debunks Anthropic&\#x27;s LLM Kernel Bug Claims](#item-3) ⭐️ 8.0/10
4. [Zig v0.17.0 released, sparking debate on design and LLM use](#item-4) ⭐️ 8.0/10
5. [Google Research&\#x27;s Cogentic multi-agent system claims new results on five open math problems](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [New AI Beats Top Human Stratego Player Using 34x Fewer Games](https://arstechnica.com/science/2026/10/ai-finally-beat-the-best-stratego-player-in-history-and-did-it-on-a-budget/) ⭐️ 8.0/10

Researchers have built an AI system that became the first to defeat the best human Stratego player in history, according to a paper published in Nature with a companion arXiv preprint \(2511.07312\). The system reportedly reached superhuman strength while playing roughly 34 times fewer games than DeepMind&\#x27;s DeepNash did in 2022. Stratego is an imperfect-information game where players cannot see each other&\#x27;s pieces, making it markedly harder for AI than fully observable games like chess or Go. Demonstrating a 34x improvement in sample efficiency suggests these methods could transfer to other hidden-information settings such as negotiation, security, and real-world strategic planning. The key novelty is learning speed: the algorithm played about 34 times fewer games than DeepNash yet ended up substantially stronger, which matters because hidden information makes forward search — reasoning &\#x27;if I do this, they will do that&\#x27; — fundamentally unreliable. The work was peer-reviewed and published in Nature alongside an arXiv paper, lending it more weight than a typical benchmark announcement.

hackernews · PaulHoule · Oct 2, 14:11 · [Discussion](https://news.ycombinator.com/item?id=49933740)

**Background**: Stratego is a two-player board game in which each side&\#x27;s pieces are hidden from the opponent, and revealing or deducing piece identities is central to winning. DeepMind&\#x27;s DeepNash, announced in July 2022, used model-free multi-agent reinforcement learning to reach expert human level at the game. Imperfect-information games like Stratego and poker have long been a hard class for AI, since standard search and evaluation techniques assume the full state is known.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Google_DeepMind">Google DeepMind - Wikipedia</a></li>
<li><a href="https://www.deeplearning.ai/the-batch/deepnash-the-rl-system-that-plays-stratego-like-a-master">DeepNash, the RL System That Plays Stratego like a Master</a></li>
<li><a href="https://dl.acm.org/doi/10.5555/3060621.3060765">Imperfect - information games and generalized planning | Proceedings...</a></li>

</ul>
</details>

**Discussion**: Commenters largely saw sample efficiency as the real story, with one arguing that because hidden information makes search unreliable, learning fast is what lets the approach work at all. Others put the result in perspective against DeepMind&\#x27;s 2022 &\#x27;mastering Stratego&\#x27; claim, noting that four years later the new method finally appears genuinely superhuman, while a few shared nostalgic childhood anecdotes about the board game \(and one about an opponent&\#x27;s subtly chipped pieces\).

**Tags**: `#AI/ML`, `#game-playing AI`, `#imperfect-information games`, `#reinforcement learning`, `#research papers`

---

<a id="item-2"></a>
## [Redis creator antirez releases ds4, a local LLM inference engine](https://dwarfstar.sh/) ⭐️ 8.0/10

Salvatore Sanfilippo \(antirez\), the creator of Redis, has released ds4, an open-source local inference engine for running large language models such as DeepSeek V4 Flash and PRO on consumer hardware. The project ships backends for Metal, CUDA and ROCm, and has recently added Vision and Qwen model support. It gives individual developers and hobbyists a lightweight alternative to llama.cpp, Ollama and vLLM for running capable models on their own machines instead of paying for cloud APIs. The volume of attention around it — a busy Hacker News thread, FFI forks, and derivative engines — shows how strong demand is for practical local inference on everyday hardware. ds4 targets Metal, CUDA and ROCm backends and supports the DeepSeek V4 Flash/PRO family, with Vision and Qwen support added in recent weeks. Community members report that SSD storage may be able to substitute for very large amounts of RAM, but throughput and tool-calling performance figures remain largely unverified.

hackernews · fibo · Oct 2, 18:01 · [Discussion](https://news.ycombinator.com/item?id=49936575)

**Background**: ds4 is an inference engine — the software layer that loads a model&\#x27;s weights and executes text generation — written by antirez, best known as the creator of the Redis in-memory database. Local inference engines such as llama.cpp, Ollama and vLLM let users run open-weight models on their own GPUs rather than calling a hosted API, trading some speed and convenience for privacy, predictable cost and offline operation.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/antirez/ds4">GitHub - antirez/ds4: DeepSeek 4 Flash and PRO local ...</a></li>
<li><a href="https://developer.amd.com/playbooks/deepseek-v4-flash-ds4/">Running DeepSeek V4 Flash with ds4 | AMD AI Playbooks</a></li>
<li><a href="https://www.local-llm.net/compare/inference-engines-2026/">Local LLM Inference Engines Compared: The Definitive 2026 ...</a></li>

</ul>
</details>

**Discussion**: Hacker News reaction is enthusiastic and hands-on: neomantra maintains a fork that exposes ds4 as shared libraries for FFI and Go bindings \(ds4go\), cuttothechase asks whether tool calling is well supported and whether SSD can replace a big-RAM Mac at around 50 TPS, ttoinou reports great results on an M5 Max 128GB with DeepSeek V4 Flash and Qwen 3.8 Flash, and simoiacos has built a derivative engine called xenolith for Intel Xe-LP laptops. A recurring caveat is that reliability and throughput numbers are still anecdotal, with some blaming odd model behavior on agentic harnesses rather than ds4 itself.

**Tags**: `#local-llm`, `#inference-engine`, `#antirez`, `#ds4`, `#hackernews`

---

<a id="item-3"></a>
## [Greg Kroah-Hartman Debunks Anthropic&\#x27;s LLM Kernel Bug Claims](https://www.youtube.com/watch?v=NnV_cWeoo5Q) ⭐️ 8.0/10

In a talk titled &quot;Security in the LLM Age,&quot; Linux kernel maintainer Greg Kroah-Hartman dissected Anthropic&\#x27;s Mythos claim of finding 79 Linux kernel vulnerabilities, showing that 24 lacked any detail, 14 were not bugs at all, 3 were fabricated data, and 15 were already fixed in the latest release — leaving only about 20 that needed real fixes, most of which amounted to pattern-matching already-known patches. The talk directly challenges the marketing narratives of leading AI labs that frame LLM-driven vulnerability discovery as a breakthrough in security, and it lands amid a broader debate over AI safety hype — especially since Anthropic restricts its most capable model under the same safety framing it uses to promote it. Of the roughly 20 fixes that were actually needed, 7 assumed a malicious filesystem image and 2 assumed an attacker who could insert malicious input, meaning many were theoretical rather than exploitable in realistic threat models; Kroah-Hartman also noted Anthropic failed to credit the kernel developers who originally wrote the patches it was re-deriving.

hackernews · usernomdeguerre · Oct 2, 02:51 · [Discussion](https://news.ycombinator.com/item?id=49929391)

**Background**: CVE \(Common Vulnerabilities and Exposures\) is a standardized ID system for publicly disclosed security flaws, so any claim of finding 79 CVEs sounds impressive and quantifiable. Anthropic&\#x27;s Claude Mythos is described as its most capable model to date, capable of autonomously discovering vulnerabilities, and its preview was released only to vetted partners under safety concerns. Greg Kroah-Hartman is a longtime Linux kernel maintainer, giving his assessment unusually high credibility in the open-source community.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/mythos">Claude Mythos \ Anthropic</a></li>
<li><a href="https://www.cve.org/">CVE : Common Vulnerabilities and Exposures</a></li>
<li><a href="https://labs.cloudsecurityalliance.org/research/ai-vuln-discovery-containment-claude-mythos-v1-0-csa-styled/">Claude Mythos: AI Vulnerability Discovery and Containment ...</a></li>

</ul>
</details>

**Discussion**: Commenters widely praised Kroah-Hartman&\#x27;s candor and slide-by-slide tally, with several arguing this exposes a stark dissonance between AI labs&\#x27; world-ending safety rhetoric and their exaggerated product marketing. Others criticized Anthropic for not crediting the original kernel developers whose patches Mythos re-derived, while a few noted the approach could still become genuinely useful with specialized models trained on kernel specifics.

**Tags**: `#LLM security`, `#Linux kernel`, `#vulnerability research`, `#AI hype critique`, `#Anthropic`

---

<a id="item-4"></a>
## [Zig v0.17.0 released, sparking debate on design and LLM use](https://ziglang.org/download/0.17.0/release-notes.html) ⭐️ 8.0/10

The Zig project published release notes for v0.17.0, the latest tagged release of its systems programming language and toolchain, detailing changes across the compiler, build system, and platform support. The accompanying Hacker News discussion focused on Zig&\#x27;s broad target support, new build/tooling integration, and creator Andrew Kelley&\#x27;s growing openness to using LLMs to discover bugs. Zig is one of the most closely watched modern alternatives to C for systems programming, and its unusually wide target support is seen by some developers as competitive with C itself, so each release influences tooling choices for cross-platform and embedded work. The LLM angle also matters because a project that has historically taken a hard line against AI contributions now appears to be pragmatically adopting LLMs for bug discovery, which could influence other open-source compiler and infrastructure projects. Zig is still pre-1.0, so v0.17.0 is a node in an ongoing, frequently breaking evolution rather than a stable milestone, and commenters note the ecosystem remains small. Several features users say they are waiting for — a stackless coroutine IO implementation and first-class fuzzer tooling — are described as targets for future releases, not deliverables of this one, while one commenter claims to have left the ecosystem over friction with core members.

hackernews · ErenayDev · Oct 2, 20:56 · [Discussion](https://news.ycombinator.com/item?id=49938521)

**Background**: Zig is a general-purpose systems programming language created by Andrew Kelley and first announced in 2016, positioned as a general-purpose improvement over C: it has no macros or preprocessor, supports compile-time generics \(comptime\), requires manual memory management, and offers low-level features such as packed structs, arbitrary-width integers, and multiple pointer types. It is free and open-source under an MIT license, with development funded by the Zig Software Foundation through corporate sponsorships and personal donations, and each tagged version ships a detailed release-notes page on ziglang.org. Because the language has not yet reached 1.0, breaking changes between versions are common, which is why release notes are closely followed by users. The interest in LLM-assisted bug finding is often tied in the discussion to reported results from SQLite, where LLMs were used to help uncover code defects.

<details><summary>References</summary>
<ul>
<li><a href="https://ziglang.org/">Home Zig Programming Language</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_%28programming_language%29">Zig (programming language)</a></li>

</ul>
</details>

**Discussion**: Sentiment on Hacker News was largely positive: one developer with professional experience in JS, C, Pascal, and Go called Zig the best-designed language they have tried, and another praised its target support as possibly the only thing that competes with C, with several welcoming Kelley&\#x27;s pragmatic turn toward LLM-assisted bug discovery. Dissent came from those noting that Zig is still unstable with a small ecosystem, and one commenter said they left Zig for Odin because of what they described as hostile behavior from core members toward contributors.

**Tags**: `#Zig`, `#programming languages`, `#systems programming`, `#release notes`, `#LLM-assisted development`

---

<a id="item-5"></a>
## [Google Research&\#x27;s Cogentic multi-agent system claims new results on five open math problems](https://arxiv.org/abs/2609.40324v1) ⭐️ 8.0/10

Google Research presented Cogentic, a multi-agent harness for automated proof discovery on open research problems, built on Gemini as the base model. Using a &quot;prove-verify&quot; loop in which multiple independent provers explore competing directions while a dedicated component performs adversarial verification, Cogentic reportedly produced new results on five open problems in online learning, auction theory, and mechanism design, all independently checked by domain experts and written up in companion papers. If the claims hold up, this is a notable milestone for LLM-driven mathematics: rather than a single-shot generation that stalls on hard problems, a coordinated multi-agent system is credited with producing expert-verified new theorems on genuinely open questions. That would push automated theorem proving from &quot;assisting with known proofs&quot; toward contributing original research, with implications for how mathematicians and theorists use AI as a collaborator. The architecture&\#x27;s distinctive element is a persistent verification ledger that accumulates confirmed results so intermediate progress is retained across long explorations, paired with adversarial verification rather than self-checking. Caveats remain: the arXiv link in the item appears malformed and future-dated \(2609.40324\), and no independent replication or community discussion is available yet, so the expert-verification claims cannot be confirmed from the submission alone.

telegram · zaihuapd · Oct 2, 12:04

**Background**: Automated theorem proving traditionally relies on formal systems and proof assistants such as Lean, where machines verify each step mechanically, but LLMs have recently been used to generate informal proof ideas that are then checked. Frontier models can produce strong mathematical ideas in a single shot, yet open problems typically require exploring multiple competing conjectures and surviving subtle technical obstructions over long horizons. Multi-agent approaches try to address this by having several agents generate and critique candidates in parallel, and a verification ledger is a known pattern for recording check results persistently so later steps can build on already-validated outputs.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.40324">[2609.40324] Cogentic: Multi-Agent Orchestration for ...</a></li>
<li><a href="https://agentpatterns.ai/verification/verification-ledger/">Verification Ledger for Tracking Agent Output Quality</a></li>
<li><a href="https://research.google/blog/towards-a-science-of-scaling-agent-systems-when-and-why-agent-systems-work/">Towards a science of scaling agent systems: When and why ...</a></li>

</ul>
</details>

**Tags**: `#multi-agent-systems`, `#automated-theorem-proving`, `#llm-reasoning`, `#google-research`, `#formal-verification`

---