---
layout: default
title: "Horizon Summary: 2026-09-11 (EN)"
date: 2026-09-11
lang: en
---

> From 36 items, 7 important content pieces were selected

---

1. [Calif Research unveils WeWorm, AI-built zero-click WeChat worm](#item-1) ⭐️ 9.0/10
2. [Shopify Abandons React Native for Native Swift and Kotlin Apps](#item-2) ⭐️ 8.0/10
3. [Researchers question trusting OpenAI with unpublished math ideas](#item-3) ⭐️ 8.0/10
4. [Microsoft Recognizes Rust as a Tier-1 Language](#item-4) ⭐️ 8.0/10
5. [trynix.dev boots any Nix package from 13 years of history in the browser](#item-5) ⭐️ 8.0/10
6. [SemiAnalysis Deep-Dive: Why Behind-the-Meter Datacenter Power Is So Hard](#item-6) ⭐️ 8.0/10
7. [Fly connectome fails to learn Pong, and the audit is the real story](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Calif Research unveils WeWorm, AI-built zero-click WeChat worm](https://simonwillison.net/2026/Sep/10/calif-research/) ⭐️ 9.0/10

Calif Research has released a demo of WeWorm, which it describes as the first zero-click worm to spread through WeChat calls on both iOS and Android. The team says that working with AI it found the bug and wrote the first remote code execution \(RCE\) exploit in about two days, then spent one more week building the worm itself. If validated, this marks a milestone for both offensive security and AI risk: a self-propagating, zero-click attack against a messaging app used by over a billion people, built in days rather than months. It also suggests AI is collapsing the time and team size needed to turn a vulnerability into a working exploit, lowering the barrier for large-scale attacks. According to Calif Research, the victim does not need to answer the call or interact with the phone at all, and even if they do answer they hear nothing while the exploit still succeeds. Notable caveats are that this is a demo rather than a fully documented advisory, and no independent verification, affected version numbers, or patch status have been provided.

rss · Simon Willison · Sep 10, 00:56

**Background**: A zero-click attack is one that executes automatically when a vulnerable app or service processes malicious input, requiring no user deception such as a phishing link. Remote code execution \(RCE\) means an attacker can run arbitrary code on a target device over a network, which is typically the stepping stone for deploying malware or stealing data, while a worm is malware that copies itself from device to device without user action. AI-assisted vulnerability discovery is an emerging trend in which models help researchers find and even patch flaws that might otherwise go unnoticed, and this incident is an early example of that capability being applied to exploit development as well.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kaspersky.com/resource-center/definitions/what-is-zero-click-malware">Zero-Click Exploits</a></li>
<li><a href="https://en.wikipedia.org/wiki/Remote_code_execution">Remote code execution</a></li>
<li><a href="https://www.vulncheck.com/blog/ai-assisted-vulnerability-discovery">The First CVE Wave: Signs That AI-Assisted Vulnerability Discovery Is Reshaping Disclosure Volumes | Blog | VulnCheck</a></li>

</ul>
</details>

**Tags**: `#security`, `#AI`, `#WeChat`, `#zero-click exploit`, `#RCE`

---

<a id="item-2"></a>
## [Shopify Abandons React Native for Native Swift and Kotlin Apps](https://shopify.engineering/back-to-native) ⭐️ 8.0/10

Shopify announced it is moving its mobile apps off React Native and back to fully native development using Swift for iOS and Kotlin for Android. The engineering blog post, which has drawn nearly 500 comments on Hacker News, frames the shift as a reversal of Shopify&\#x27;s earlier bet on a single shared JavaScript codebase across platforms. Shopify runs one of the highest-traffic commerce apps in the world, so its retreat from React Native is a significant signal for the broader cross-platform versus native debate. It reinforces a growing industry view that companies at Shopify&\#x27;s scale eventually want dedicated native engineers who can optimize each platform individually. The migration reportedly involved rewriting each screen based on the existing React Native code and adding separate Android and iOS directories, with tooling such as Maestro used for app testing. Commenters note that debugging crashes spanning JavaScript, C++ and native threads can cost more than simply maintaining two codebases.

hackernews · fnthawar2 · Sep 10, 14:09 · [Discussion](https://news.ycombinator.com/item?id=49643982)

**Background**: React Native, maintained by Meta, lets developers write mobile apps in JavaScript and React and share most of the code between iOS and Android, which is attractive because web developers can contribute directly to mobile. Swift is Apple&\#x27;s compiled language for iOS and macOS apps, while Kotlin is JetBrains&\#x27; statically typed language and the preferred choice for modern Android development. The tradeoff is that cross-platform frameworks reduce duplicated work but can add layers of abstraction, making performance tuning and native debugging harder.

<details><summary>References</summary>
<ul>
<li><a href="https://reactnative.dev/">React Native</a></li>
<li><a href="https://en.wikipedia.org/wiki/Swift_%28programming_language%29">Swift (programming language) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Kotlin">Kotlin - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion is broadly sympathetic to leaving React Native, with one iOS engineer saying the decision validated years of arguing against a shared codebase. However, several commenters push back on the narrative that LLMs made the migration newly affordable, noting that similar rewrites were completed before LLM code assistance and that models have simply become much better at generating native apps.

**Tags**: `#React Native`, `#Mobile Development`, `#Swift`, `#Kotlin`, `#Cross-Platform`

---

<a id="item-3"></a>
## [Researchers question trusting OpenAI with unpublished math ideas](https://mathstodon.xyz/@andreasthom/117240535270608201) ⭐️ 8.0/10

A Mastodon thread by @andreasthom has sparked debate over whether mathematicians can safely share unpublished ideas with OpenAI, after reports that OpenAI used researchers&\#x27; collaborative chats to produce research results without attributing them. The discussion follows claims that OpenAI stated the model used to generate a result was not trained on those collaborative chats. The episode raises fundamental questions about research ethics and attribution norms when AI labs interact with academics, and could discourage researchers from using or sharing ideas with commercial models. It also touches on the broader debate about whether AI systems are genuinely solving open problems or are being fed the very ideas they later appear to discover. The claims are contested: some argue that pretraining on user chats could subtly improve a model&\#x27;s latent intuition, while others note that reinforcement learning on verifiable math problems with massive compute could independently produce superhuman techniques. Details are further complicated by reports that OpenAI generated roughly 300 billion output tokens from a model still in training shortly after learning a major math proof might be in its training data.

hackernews · pred\_ · Sep 10, 06:49 · [Discussion](https://news.ycombinator.com/item?id=49639408)

**Background**: Large language models like those from OpenAI are trained in stages, including pretraining on vast text corpora and reinforcement learning on tasks that can be automatically verified, such as math problems. In mathematics, attribution matters greatly because priority for a proof or theorem is a core form of credit, so using someone&\#x27;s unpublished idea without acknowledgement is treated as a serious breach of academic norms. The debate centers on whether an AI company that receives a researcher&\#x27;s private ideas effectively becomes a collaborator with duties of attribution, or merely a tool provider.

**Discussion**: Commenters largely agreed the situation is troubling. One drew an analogy to a human collaborator, arguing that if a person behaved this way it would be clearly unethical; another argued both things can be true, since chat data may improve intuition while reinforcement learning could independently discover results. Others worried researchers are being fed fresh problems while their work is absorbed, flagged the 300 billion output tokens as suspiciously timed, and questioned how much people should trust companies with their data.

**Tags**: `#AI ethics`, `#OpenAI`, `#research integrity`, `#mathematics`, `#AI safety`

---

<a id="item-4"></a>
## [Microsoft Recognizes Rust as a Tier-1 Language](https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/) ⭐️ 8.0/10

In a guest post published by the Rust Foundation, Microsoft confirmed that Rust has officially reached tier-1 status inside the company, placing it alongside long-established options such as C++ for new systems-level development. The announcement also coincides with renewed public signals about MSVC toolchain integration for Rust, a topic that had previously only been the subject of rumors. Microsoft is one of the largest owners of C and C++ code in the world, so giving Rust first-class status signals that a memory-safe systems language is now a mainstream enterprise default rather than an experiment. It also strengthens Rust&\#x27;s position in the broader &quot;better C/C++&quot; space, which is especially relevant as all major OS vendors diversify the systems languages they support for greenfield work. Tier-1 status does not mean parity with C++: the post notes that C++ still dominates after decades of investment, and community members point out that tier-1-grade debugging support in Visual Studio is still an open question. Commenters also link to Microsoft&\#x27;s stated goal of converting 1 billion lines of C/C++ to Rust by 2030 through automated tooling described as enabling &quot;1 engineer, 1 month, 1 million lines of code&quot;, plus DARPA-funded work in which six teams are exploring different ways to automate C-to-Rust translation.

hackernews · mmastrac · Sep 10, 13:39 · [Discussion](https://news.ycombinator.com/item?id=49643546)

**Background**: At large software vendors, languages are usually ranked by how much official investment they receive in compilers, build systems, debuggers, libraries and security review workflows; a tier-1 label means engineers can choose the language for production work without special approval. Rust is a systems programming language that reached 1.0 in 2015, and its central selling point is memory safety enforced at compile time, which prevents whole classes of bugs such as buffer overflows and use-after-free errors. That matters to Microsoft because a large majority of the security vulnerabilities \(CVEs\) in its products have historically been memory-safety issues in C and C++ code.

<details><summary>References</summary>
<ul>
<li><a href="https://rustfoundation.org/media/guest-post-rust-is-tier-1-language-at-microsoft/">Guest Post: Rust Is Tier - 1 Language at Microsoft</a></li>
<li><a href="https://news.ycombinator.com/item?id=49643546">Rust Is Tier - 1 Language at Microsoft | Hacker News</a></li>
<li><a href="https://markaicode.com/legacy-code-migration-c-to-rust-tools-2025/">C to Rust Migration in 2025: Tools , Strategies, and... | Markaicode</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread \(592 points, 334 comments\) is broadly positive, with commenters arguing that announcements like this prove Rust is no longer a fast-moving &quot;break things&quot; language but a mature competitor to C++ and C\#, and that rivals in the better-C space such as Zig and Odin are still comparatively rough. A developer with five years of professional Rust experience claims there is no longer a technical reason to pick another language for high-level application work, while others welcome the diversification of systems languages across major OS vendors and ask when Visual Studio will offer genuinely first-class Rust debugging.

**Tags**: `#Rust`, `#Microsoft`, `#programming-languages`, `#systems-programming`, `#software-engineering`

---

<a id="item-5"></a>
## [trynix.dev boots any Nix package from 13 years of history in the browser](https://simonwillison.net/2026/Sep/10/trynix/) ⭐️ 8.0/10

Farid Zakaria launched trynix.dev, which uses qemu-wasm to run an x86\_64 Linux virtual machine entirely inside the browser and boots it with any Nix package built over the past 13 years. Environments are URL-addressable — for example https://trynix.dev/?pkg=python3%403.6.2 loads an interactive shell running Python 3.6.2 from 2017 — and he also released trynix-preview, a GitHub Action that comments a link on a pull request so reviewers can boot the PR&\#x27;s build in the browser. It dramatically lowers the barrier to reproducing historical software environments: instead of reconstructing a decade-old toolchain locally, anyone can open a link and get a working shell. The trynix-preview action also shows practical downstream value for code review and CI verification, since reviewers can boot the exact artifact a pull request produces without provisioning any server. The browser VM runs through ktock&\#x27;s qemu-wasm, which combines QEMU&\#x27;s TCI interpreter with a TCG backend that only compiles frequently executed translation blocks \(for example those run 1,000 times\) into WebAssembly. Everything runs client-side with no servers, but it depends on Nix&\#x27;s cached binary artifacts and does not preserve state between reloads, and emulating a full x86\_64 machine in Wasm is inherently slower than native execution.

rss · Simon Willison · Sep 10, 23:44

**Background**: Nix is a purely functional package manager created by Eelco Dolstra in 2003 that stores build results in an immutable store addressed by a hash of the complete dependency tree, which makes builds reproducible and allows many versions of the same package to coexist. That content-addressed store is why trynix.dev can reliably fetch a package exactly as it was built years ago. qemu-wasm is the QEMU emulator compiled to WebAssembly via Emscripten, letting a full Linux system run inside a browser tab.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ktock/qemu-wasm">GitHub - ktock/ qemu - wasm : QEMU on browser · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nix_%28package_manager%29">Nix (package manager)</a></li>
<li><a href="https://nixos.org/">Nix &amp; NixOS | Declarative builds and deployments</a></li>

</ul>
</details>

**Tags**: `#nix`, `#webassembly`, `#virtualization`, `#qemu`, `#developer-tools`

---

<a id="item-6"></a>
## [SemiAnalysis Deep-Dive: Why Behind-the-Meter Datacenter Power Is So Hard](https://newsletter.semianalysis.com/p/what-is-so-hard-about-behind-the) ⭐️ 8.0/10

SemiAnalysis published Part 1 of a deep-dive newsletter examining the technical and economic challenges of behind-the-meter power solutions for datacenters, subtitled &quot;Dumb Science Experiments vs. Money Printing Machines.&quot; The piece sets up a comparison between speculative, scientifically interesting power approaches and those that actually generate profitable, bankable returns. Power, not land or capital, has become the binding constraint on datacenter growth as AI training and inference demand surges, so how operators secure electricity determines how fast new AI capacity can come online. Behind-the-meter generation is increasingly pitched as a way to bypass crowded grid interconnection queues, making this analysis directly relevant to hyperscalers, utilities, and infrastructure investors. Behind-the-meter systems place generation assets literally behind the utility meter, so the datacenter supplies its own primary power independently of the public grid, in contrast to a standard power purchase agreement or utility contract. Such setups typically rely on microgrids powered by gas turbines, fuel cells, or modular nuclear reactors, and they bring their own financing, regulatory, and technology risks.

rss · Semianalysis · Sep 10, 14:28

**Background**: Behind-the-meter power means a facility generates electricity on its own side of the utility meter rather than buying it from the grid, which separates datacenter demand from community electricity use. This matters because grid interconnection queues in major digital hubs can stretch for years, while power—not space—has become the key constraint of modern datacenters. The tradeoff is that operators take on fuel supply, permitting, emissions, and reliability obligations that a utility would otherwise carry.

<details><summary>References</summary>
<ul>
<li><a href="https://www.williams.com/2026/03/17/powering-data-centers-behind-the-meter-power-explained/">Powering data centers: behind-the-meter power, explained | Williams Companies</a></li>
<li><a href="https://datacenterhawk.com/resources/market-insights/behind-the-meter-power-solutions-the-data-center-industry-s-new-reality">Behind-the-Meter Power Solutions: The Data Center Industry&#x27;s New Reality - datacenterHawk</a></li>
<li><a href="https://www.aoshearman.com/en/insights/data-center-insights/powering-data-centers-the-rise-and-challenges-of-the-behind-the-meter-model">Data centers and the rise of behind-the-meter power</a></li>

</ul>
</details>

**Tags**: `#datacenters`, `#power-infrastructure`, `#AI-infrastructure`, `#energy`, `#behind-the-meter`

---

<a id="item-7"></a>
## [Fly connectome fails to learn Pong, and the audit is the real story](https://www.reddit.com/r/MachineLearning/comments/1wc67ci/i_tried_to_make_a_real_fly_connectome_learn_to/) ⭐️ 8.0/10

A developer tried to train a small real subgraph of the newly released MaleCNS v1.0 fruit fly connectome \(166k neurons, from real electron-microscopy reconstruction\) to play Pong using dopamine-style plasticity, and it failed to learn. Auditing the failure uncovered a neuPrint regex bug that silently zeroed out two whole neuron populations, a neuron selection with no path from photoreceptors to anything else, and motor neurons with literally zero synapses from any sensory pathway that could never have fired. The viral &quot;fly brain plays Doom/Minecraft/Beat Saber&quot; demos have been widely shared this week as evidence that connectome-scale simulation produces emergent behavior, but the author shows those projects&\#x27; own repositories and creator comments admit they failed validation gates, keep motion pathways silent, or hand-inject behaviors. This negative result provides a much-needed methodological check on how connectome-based learning claims are evaluated, and it matters for anyone in computational neuroscience or ML tempted to treat a game-engine demo as proof. Even after fixing the bugs and getting a working pipeline, turning plasticity on versus off produced bit-for-bit identical results across multiple seeds despite weights verifiably changing, because half of the four available motor neurons had zero sensory synapses; a rebuilt circuit based on a courtship-pursuit visual tracking hypothesis was refuted by the data. The final divergence between learning-on and learning-off looked like the learning rule simply quieting the whole system down — punishment dominates when misses outnumber hits, shrinking motor response rather than producing skill.

reddit · r/MachineLearning · /u/oPeraza2007 · Sep 10, 02:28

**Background**: A connectome is a synapse-level map of all neurons and their connections in a nervous system, obtained by tracing electron-microscopy images; MaleCNS v1.0 is Janelia&\#x27;s reconstruction of an entire male Drosophila central nervous system, including the central brain, optic lobes and ventral nerve cord. neuPrint is the query interface used to fetch neurons and their connectivity from such datasets. Pong is used here as a deliberately unforgiving test bed because it gives only a single binary hit-or-miss signal per frame, leaving no room for vague &quot;it moves, so it&\#x27;s alive&quot; claims, and dopamine-style plasticity refers to learning rules that modulate synaptic strengths via reward/punishment-like signals.

<details><summary>References</summary>
<ul>
<li><a href="https://male-cns.janelia.org/">Male CNS Connectome - MaleCNS connectome</a></li>
<li><a href="https://connectome-neuprint.github.io/neuprint-python/docs/changelog.html">Changelog — neuprint-python 0.5.1+10 ... - GitHub Pages</a></li>
<li><a href="https://www.nature.com/articles/s41586-022-05485-4">Dopamine promotes head direction plasticity during orienting movements | Nature</a></li>

</ul>
</details>

**Tags**: `#connectomics`, `#computational neuroscience`, `#reinforcement learning`, `#plasticity`, `#negative results`

---