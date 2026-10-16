---
layout: default
title: "Horizon Summary: 2026-10-16 (EN)"
date: 2026-10-16
lang: en
---

> From 42 items, 6 important content pieces were selected

---

1. [Meta Releases Muse Spark Open, an 816B Open-Weight Model Built for Local Deployment](#item-1) ⭐️ 8.0/10
2. [Goodfire&\#x27;s Nick Cammarata argues neural networks are &\#x27;clean&\#x27;](#item-2) ⭐️ 8.0/10
3. [Citizen Lab: Israeli Firm Discover Tech Turned Targeted Ads Into Zero-Click Spyware Pipeline](#item-3) ⭐️ 8.0/10
4. [Libreboot 26.10 &quot;Ominous Olive&quot; adds UEFI/EDK2 and Chromebook support](#item-4) ⭐️ 8.0/10
5. [Anthropic Tells Investors Quarterly Revenue Up Nearly 50% to $16.8bn Ahead of IPO](#item-5) ⭐️ 8.0/10
6. [MIT/PNAS: Randomly Wired Neurons Self-Assemble Their Own Learning Motifs](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Meta Releases Muse Spark Open, an 816B Open-Weight Model Built for Local Deployment](https://research.meta.ai/blog/muse-spark-open) ⭐️ 8.0/10

Meta released Muse Spark Open under the Hugging Face repository meta-models/Muse-Spark-Open-816B-A42B, a large open-weight model with 816B total parameters and 42B active parameters. The company says the release is optimized for local deployment, with deployment guides covering runners such as Unsloth and MLX, including running on a Mac Studio. It is another major open-weight release from Meta and immediately puts the company in direct comparison with Qwen and GLM in the local-deployment segment. Because the license restricts commercial serving of the model, the release also reignites the industry debate over what &quot;open-weight&quot; actually means and how much freedom such releases really grant. The license permits general use but blocks &quot;Model as a Service&quot; — offering the model to third parties via API or similar interfaces — for any licensee or affiliate whose aggregate gross revenue exceeds 20 million dollars. Early third-party benchmark comparisons place Muse Spark Open below Qwen3.8 Flash Next and GLM 5.3 Flash, both of which can reportedly run on a single B300 GPU.

hackernews · bigwheels · Oct 15, 17:47 · [Discussion](https://news.ycombinator.com/item?id=50107379)

**Background**: Open-weight models publish their trained numerical parameters for download, but unlike open-source software they usually come with custom licenses that can restrict commercial use, so &quot;open-weight&quot; is not the same as OSI-approved open source. Muse Spark Open uses a Mixture-of-Experts \(MoE\) architecture, in which each token is routed through only a few expert sub-networks: the 816B total parameter count determines how much memory is needed to hold the model, while the 42B active parameters determine the compute and speed per token. Local deployment tooling such as MLX, Unsloth and similar runtimes lets users execute these models on their own hardware instead of paying per-token API fees.

<details><summary>References</summary>
<ul>
<li><a href="https://vettedconsumer.com/mixture-of-experts-moe-explained-why-active-parameters-decide-what-runs-on-your-machine/">Mixture - of - Experts (MoE), Explained: Why “ Active Parameters ”...</a></li>
<li><a href="https://github.com/Open-Weights/Definition">GitHub - Open-Weights/Definition: Definition for Open Weights ... Open-Weight AI Model Licenses: Commercial Use Rules Explained Open-Weight License Landscape 2026 - Presenc AI Open Weight License Explorer - a Hugging Face Space by open ... Open Weight Definition (OWD)</a></li>
<li><a href="https://www.layer3labs.io/open-weights/best-open-weights-ai-models">Open-Weight AI Models List: Best for Business (2026)</a></li>

</ul>
</details>

**Discussion**: Commenters were split: some argued the license means this is not truly open-weight, with one user quoting the clause blocking API-style &quot;Model as a Service&quot; above 20 million dollars in revenue, while others praised Meta for making the model runnable on essentially every runner from Unsloth to MLX. Benchmark-focused critics said it underperforms Qwen3.8 Flash Next and GLM 5.3 Flash, and one user ran the model through OpenRouter rather than local hardware. A recurring strategic argument was that Meta is using free distribution to make its model a standard and build an ecosystem moat.

**Tags**: `#AI`, `#open-weight models`, `#Meta`, `#LLM`, `#licensing`

---

<a id="item-2"></a>
## [Goodfire&\#x27;s Nick Cammarata argues neural networks are &\#x27;clean&\#x27;](https://already-clean.goodfire.com/) ⭐️ 8.0/10

Nick Cammarata, an early mechanistic interpretability researcher at OpenAI now at Goodfire, published a new essay \(hosted at already-clean.goodfire.com\) arguing that neural networks are fundamentally &\#x27;clean&\#x27; and interpretable, pushing back on the long-held pessimism that features are hopelessly entangled via superposition. The claim, promoted via his X launch post, triggered a large and largely skeptical Hacker News debate with 489 points and 187 comments. If neural networks are genuinely &\#x27;clean&\#x27; rather than relying on heavy superposition, mechanistic interpretability becomes far more tractable, which matters enormously for AI safety and alignment efforts that depend on understanding what models are actually doing. The essay thus feeds directly into the ongoing strategic debate over whether interpretability is a solvable problem or an intractable one. The argument is built as an evidentiary brief that revisits famously messy neurons, catalogs tool failures and places where &\#x27;polysemanticity&\#x27; still hides, rather than presenting a single new experiment. Notably, Cammarata states he co-authored early mech interp work at OpenAI and came away pessimistic, making this an explicit reversal of his prior position.

hackernews · themgt · Oct 15, 16:04 · [Discussion](https://news.ycombinator.com/item?id=50105647)

**Background**: Mechanistic interpretability is a subfield of explainable AI that tries to reverse-engineer the internal algorithms, circuits and concepts of neural networks into human-understandable form. A central obstacle has been superposition: the idea that networks pack more sparse features into their activations than they have neurons, by arranging features in near-orthogonal directions, which produces &\#x27;polysemantic&\#x27; neurons that respond to seemingly unrelated inputs. Goodfire is a San Francisco interpretability startup focused on mapping and editing the internal geometry of models.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanistic_interpretability">Mechanistic interpretability - Wikipedia</a></li>
<li><a href="https://www.greaterwrong.com/posts/8EyCQKuWo6swZpagS/suphttps-imgur-com-a-ufttll0erposition-is-not-just-neuron">Superposition is not &quot;just&quot; neuron polysemanticity - LessWrong...</a></li>
<li><a href="https://www.goodfire.com/">Goodfire AI</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were largely skeptical, with bluejay2387 calling the claims &\#x27;an overreach of what is actually proven&\#x27; and noting that progressive feature complexity and lottery-ticket-style phenomena are not mutually exclusive with parameter overloading. Others, like dleeftink, asked why we would want to reduce a neuron to an interchangeable feature, arguing that the external context and genesis of a neuron carry irreplaceable information, while antics framed the essay as a &\#x27;massive evidentiary brief&\#x27; arguing that it is easier than expected to &\#x27;sequence the AI genome&\#x27;.

**Tags**: `#mechanistic-interpretability`, `#neural-networks`, `#AI-alignment`, `#AI-research`, `#superposition`

---

<a id="item-3"></a>
## [Citizen Lab: Israeli Firm Discover Tech Turned Targeted Ads Into Zero-Click Spyware Pipeline](https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/) ⭐️ 8.0/10

Citizen Lab published research alleging that the Israeli company Discover Tech abused targeted advertising infrastructure to profile, track and deliver zero-click mercenary spyware to victims&\#x27; mobile devices without any user interaction, with The Guardian and The Verge reporting on the findings on 15 October 2026. The report describes the ad ecosystem being repurposed as both a distribution and command-and-control channel rather than a conventional malvertising lure that requires a click. If confirmed, this represents a novel attack vector in which ordinary ad-auction infrastructure — used by virtually every app and website — becomes a stealthy delivery pipeline for government-grade surveillance, eroding the already fragile trust between users, publishers and ad intermediaries. It also widens the accountability gap, since spyware vendors, ad exchanges, demand-side platforms and data brokers all sit in the chain but none clearly owns the abuse. The research reportedly details the infection and command-and-control stages in some depth but remains vague on the precise technical mechanism that allowed the spyware to install without any user action — a gap that security engineers have already flagged as the report&\#x27;s weakest point. It also implicates an Israeli commercial vendor, continuing a pattern of mercenary-surveillance companies operating behind nominally civilian business fronts.

hackernews · jcomp · Oct 15, 10:43 · [Discussion](https://news.ycombinator.com/item?id=50101813)

**Background**: Zero-click spyware infects a device by exploiting hidden vulnerabilities in software, apps or operating systems, so the target never has to tap a link or open a message, unlike older attacks that relied on social engineering. Mercenary spyware — the best-known example being NSO Group&\#x27;s Pegasus — is commercial surveillance tooling sold to governments and typically aimed at journalists, activists, opposition politicians and diplomats. Real-time bidding, the auction system behind most programmatic advertising, exposes huge amounts of device, location and behavioural signals that let an operator single out a specific handset for attack, a technique MITRE catalogs as malvertising infrastructure acquisition \(T1583.008\).

<details><summary>References</summary>
<ul>
<li><a href="https://me-en.kaspersky.com/about/press-releases/from-targeted-advertising-to-targeted-attacks-how-advertising-data-is-weaponized-by-cyberthreat-actors">From targeted advertising to targeted attacks: How ...</a></li>
<li><a href="https://attack.mitre.org/techniques/T1583/008/">Acquire Infrastructure: Malvertising, Sub-technique T1583.008 ...</a></li>
<li><a href="https://www.foreignaffairs.com/world/autocrat-in-your-iphone-mercenary-spyware-ronald-deibert">The Autocrat in Your iPhone: How Mercenary Spyware Threatens...</a></li>

</ul>
</details>

**Discussion**: Discussion was sharply divided: a 13-year adtech engineer called the report &\#x27;highly sensationalist&\#x27; about the zero-click claim, noting it never explains the activation mechanism, and pushed back on the idea that &\#x27;ad providers&\#x27; can simply be held responsible since the adtech ecosystem has no such single actor. Other commenters debated whether Israeli cyber firms can ever be treated as independent of the state, questioned how Israel became a top-tier cyber power, and linked the industry&\#x27;s roots to the long-documented Download Valley adware cluster.

**Tags**: `#security`, `#spyware`, `#adtech`, `#privacy`, `#cyber-espionage`

---

<a id="item-4"></a>
## [Libreboot 26.10 &quot;Ominous Olive&quot; adds UEFI/EDK2 and Chromebook support](https://libreboot.org/news/libreboot2610.html) ⭐️ 8.0/10

Libreboot 26.10, codenamed &quot;Ominous Olive&quot;, has been released with two major additions: integration of UEFI via the EDK2 framework and support for all 233 currently supported Chromebooks imported from the MrChromebox coreboot distribution. The changelog is relative to the previous Libreboot 26.01 release, and the Chromebook ports are source-only in this release, meaning users must build from source since no pre-built binaries are provided. This release dramatically multiplies the number of devices Libreboot can run on and lowers the barrier for future ports, marking a significant expansion for the niche open-source firmware ecosystem. It also makes Libreboot relevant to a much wider audience, since UEFI/EDK2 support and Chromebook compatibility are far more mainstream than the older, narrowly supported hardware Libreboot historically targeted. The Chromebook support is imported wholesale from MrChromebox&\#x27;s coreboot distro, with Baytrail \(Kip\) tested while other models still require testing, and no binaries are shipped so users must compile from source. The release has also drawn attention for its strict anti-AI-contribution policy, documented in an AGENTS file in the project&\#x27;s lbmk repository, which restricts LLM-assisted contributions.

hackernews · iamnothere · Oct 15, 12:52 · [Discussion](https://news.ycombinator.com/item?id=50102923)

**Background**: Libreboot is a free and open-source distribution of coreboot, a lightweight firmware project that initializes hardware and then loads an operating system, intended to replace proprietary BIOS and UEFI firmware. Because coreboot performs low-level hardware initialization, it must be ported chipset by chipset and motherboard by motherboard, which historically limited Libreboot to a small set of older machines. UEFI/EDK2 is a modern, cross-platform firmware development environment for the UEFI and PI specifications, so integrating it lets Libreboot adopt more contemporary firmware interfaces and hardware.

<details><summary>References</summary>
<ul>
<li><a href="https://libreboot.org/news/libreboot2610.html">Libreboot – Libreboot 26.10 “Ominous Olive” released! With ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Libreboot">Libreboot</a></li>
<li><a href="https://en.wikipedia.org/wiki/Coreboot">Coreboot</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agreed that the AI policy has overshadowed the real news, with one noting that UEFI/EDK2 integration and Chromebook support are &quot;a massive step forward&quot; that multiply available devices. A Heads project contributor shared related ChromeOS porting work using MrChromebox&\#x27;s code as an upstream dependency, while another praised the strict anti-LLM contribution stance as refreshing for a serious open-source project. Others expressed enthusiasm about potentially running Libreboot on devices they had previously flashed with MrChromebox firmware.

**Tags**: `#libreboot`, `#coreboot`, `#UEFI`, `#open-source-firmware`, `#chromebook`

---

<a id="item-5"></a>
## [Anthropic Tells Investors Quarterly Revenue Up Nearly 50% to $16.8bn Ahead of IPO](https://simonwillison.net/2026/Oct/15/anthropic-tells-investors/) ⭐️ 8.0/10

Anthropic told investors on Wednesday that its quarterly revenue grew nearly 50% to $16.8bn, according to an FT report, with Q1 at about $4.8bn, Q2 at $11.5bn and Q3 at $16.8bn. The company also disclosed that model distillation by rival labs accounted for 5% to 7% of revenue and that it had cut that activity back &quot;materially&quot; in Q3. These hard figures from a leading AI lab ahead of a planned IPO give an unusually concrete view of how much revenue frontier model providers can generate, and the disclosed crackdown on distillation signals that labs are willing to sacrifice paying API customers to protect their model weights. The news also matters because Anthropic has apparently stopped leaning on the friendlier &quot;annualized run-rate revenue&quot; metric in investor communications, shifting the industry toward clearer quarterly reporting. In Q3 Anthropic reported $1.70 in revenue for every $1 spent on computing power, with adjusted operating margins \(excluding stock-based compensation\) of 11%. Simon Willison&\#x27;s napkin math suggests that if distillation was 5% of Q2 revenue before the cutback, unnamed rival labs spent over half a billion dollars distilling Anthropic&\#x27;s models in that single quarter.

rss · Simon Willison · Oct 15, 13:04

**Background**: Model distillation \(or knowledge distillation\) is a machine-learning technique in which a smaller &quot;student&quot; model is trained to imitate the outputs of a larger, more capable &quot;teacher&quot; model, typically so the resulting model is cheaper to run. In the commercial LLM era, labs have objected to rivals using this method against their API outputs, since it effectively lets a competitor acquire model capabilities through heavy paid usage rather than original training. Anthropic is a leading AI lab and maker of the Claude model family, and the reported figures come as it prepares for an initial public offering.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_distillation">Model distillation</a></li>
<li><a href="https://www.flozic.ai/blog/ai-model-distillation">AI Model Distillation : Smarter AI with Less Compute</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#AI industry`, `#IPO`, `#business`, `#revenue`

---

<a id="item-6"></a>
## [MIT/PNAS: Randomly Wired Neurons Self-Assemble Their Own Learning Motifs](https://www.reddit.com/r/MachineLearning/comments/1x6hmyg/how_artificial_neural_networks_build_their_own/) ⭐️ 8.0/10

An MIT-covered PNAS paper published on 9 October 2026, &quot;How Biological Synapses Self-Assemble Gradient Learning,&quot; reports that randomly interconnected neuron-like units governed by shared local plasticity rules can self-organize into learning motifs capable of pattern recognition and image classification. The authors report that the resulting networks perform similarly to the backpropagation-trained networks they compared against. The result reframes the problem of learning: instead of directly designing a learning circuit, one specifies local rules from which the learning machinery organizes itself, which is conceptually important for both machine learning and neuroscience. It suggests a biologically plausible route to learning that could inform new architectures beyond backpropagation, though it is not presented as a replacement for backpropagation in large-scale models. The authors explicitly caution that self-organization does not establish that the brain actually uses this mechanism, and the motivating goal is biological plausibility rather than benchmark superiority. Open questions noted in the coverage include whether the discovered motifs remain stable under different initial connectivity and whether they generalize beyond the specific tasks demonstrated.

reddit · r/MachineLearning · /u/Dorian182 · Oct 15, 10:01

**Background**: Backpropagation is the standard algorithm for training artificial neural networks: it computes gradients by propagating error signals backward through the whole network, which requires globally coordinated, non-local information that biological synapses do not obviously have. Local plasticity rules instead update each synapse using only information available at that synapse, such as the activity of the neurons it connects, and are considered far more plausible as models of how real brains learn. This work asks whether such purely local rules, applied to a randomly wired network, can let functional learning structures emerge on their own.

<details><summary>References</summary>
<ul>
<li><a href="https://news.mit.edu/2026/how-artificial-neural-networks-build-their-own-learning-machinery-1013">How artificial neural networks build their own learning machinery</a></li>
<li><a href="https://infoscience.epfl.ch/server/api/core/bitstreams/fccff930-b75c-4944-9ddc-c9f6b24617a2/content">Local plasticity rules can learn deep representations</a></li>
<li><a href="https://www.nature.com/articles/s41467-026-70920-3">Intrinsic stabilization of synaptic plasticity improves ...</a></li>

</ul>
</details>

**Discussion**: Discussion in the Reddit thread was largely engaged but brief, focusing on the framing questions rather than disputing the result: commenters highlighted the stability of the self-assembled motifs across different initial connectivity and whether the approach can extend beyond the demonstrated tasks as the key tests of the finding&\#x27;s significance.

**Tags**: `#neural-networks`, `#self-organization`, `#synaptic-plasticity`, `#computational-neuroscience`, `#machine-learning`

---