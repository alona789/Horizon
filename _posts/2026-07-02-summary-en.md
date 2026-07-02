---
layout: default
title: "Horizon Summary: 2026-07-02 (EN)"
date: 2026-07-02
lang: en
---

> From 38 items, 10 important content pieces were selected

---

1. [Linux 6.9 bug: LUKS suspend fails to wipe encryption keys from memory](#item-1) ⭐️ 8.0/10
2. [Podman v6.0.0 Released with Major Improvements](#item-2) ⭐️ 8.0/10
3. [F-Droid Calls Android Developer Verification a Malware Threat](#item-3) ⭐️ 8.0/10
4. [Japan top court: AI cannot be listed as inventor on patents](#item-4) ⭐️ 8.0/10
5. [ECTC 2026 Highlights: EMIB-T, Custom HBM, and Cooling](#item-5) ⭐️ 8.0/10
6. [Hamiltonian Neural Networks through a Differential Geometry Lens](#item-6) ⭐️ 8.0/10
7. [Cloudflare to block mixed-purpose AI crawlers from September](#item-7) ⭐️ 8.0/10
8. [OpenAI Proposes US Government 5% Stake, Eyes Other AI Giants](#item-8) ⭐️ 8.0/10
9. [Citibank blocks GPT-5.5 as AI costs surge, firms limit usage](#item-9) ⭐️ 8.0/10
10. [Anthropic in talks with Samsung for custom AI chips](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Linux 6.9 bug: LUKS suspend fails to wipe encryption keys from memory](https://mathstodon.xyz/@iblech/116769502749142438) ⭐️ 8.0/10

A bug in Linux kernel 6.9 prevents the `cryptsetup luksSuspend` command from wiping disk-encryption master keys from kernel memory during system suspend, leaving them exposed. This security regression compromises disk encryption protection during sleep, making encrypted data vulnerable to cold boot attacks or memory forensics. The bug specifically affects the `cryptsetup luksSuspend` operation, which is a Debian-specific extension not officially part of the LUKS standard; however, it impacts all systems using this feature.

hackernews · IngoBlechschmid · Jul 2, 15:25 · [Discussion](https://news.ycombinator.com/item?id=48763035)

**Background**: LUKS (Linux Unified Key Setup) is a disk encryption specification that stores master keys in kernel memory to perform real-time encryption and decryption. When a system suspends to RAM, these keys normally remain in memory, but the `luksSuspend` command is designed to wipe them before sleep to enhance security. The kernel 6.9 change inadvertently disabled this wiping mechanism.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Linux_Unified_Key_Setup">Linux Unified Key Setup - Wikipedia</a></li>
<li><a href="https://www.howtogeek.com/what-is-luks-and-how-does-it-secure-your-linux-file-system/">What is LUKS , and How Does It Secure Your Linux File System?</a></li>
<li><a href="https://www.golinuxcloud.com/how-to-encrypt-hard-disk-partition-luks-linux/">How to Encrypt New Hard Disk (Partition) using LUKS in Linux</a></li>

</ul>
</details>

**Discussion**: Community comments note that the bug is easy to miss because security failures are often silent. Some argue that regular sleep (not using `luksSuspend`) already leaves keys in memory, so the extra protection was limited. Others emphasize the value of automated testing, such as NixOS tests, to catch such regressions.

**Tags**: `#Linux kernel`, `#LUKS`, `#disk encryption`, `#security regression`, `#key management`

---

<a id="item-2"></a>
## [Podman v6.0.0 Released with Major Improvements](https://blog.podman.io/2026/07/introducing-podman-v6-0-0/) ⭐️ 8.0/10

Podman 6.0.0 has been released, introducing new network improvements and enhanced Quadlet support for easier container management. This release strengthens Podman as a leading Docker alternative, offering daemonless, rootless execution and seamless docker-compose compatibility, benefiting DevOps workflows and container adoption. Notable technical details include a revamped network stack and improved Quadlet integration with systemd, alongside performance optimizations and bug fixes as highlighted in community discussions.

hackernews · soheilpro · Jul 2, 14:23 · [Discussion](https://news.ycombinator.com/item?id=48762098)

**Background**: Podman is an open-source, daemonless container engine from Red Hat that complies with OCI standards. Unlike Docker, it runs containers without a central daemon and supports rootless operations for enhanced security. Its CLI is designed to be Docker-compatible, easing migration for users.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Podman">Podman - Wikipedia</a></li>
<li><a href="https://www.redhat.com/en/topics/containers/what-is-podman">What is Podman?</a></li>
<li><a href="https://docs.podman.io/">What is Podman? — Podman documentation</a></li>

</ul>
</details>

**Discussion**: Community sentiment is overwhelmingly positive, with users praising easy migration from Docker, new network features, and Quadlet. One user noted memory efficiency and daemonless design, while another commented on low text contrast on the blog. Overall, the release is enthusiastically received.

**Tags**: `#podman`, `#containers`, `#docker alternative`, `#devops`, `#version release`

---

<a id="item-3"></a>
## [F-Droid Calls Android Developer Verification a Malware Threat](https://f-droid.org/2026/07/01/adv-malware.html) ⭐️ 8.0/10

F-Droid published a blog post arguing that Android's Developer Verification is a threat masquerading as protection, comparing it to malware like trojans. This article challenges Google's control over Android app distribution and raises concerns about user autonomy and security, potentially influencing the debate on open mobile ecosystems. The article uses strong language, accusing Google of acting like a 'malware vendor' and drawing parallels between Developer Verification and trojan behavior. It also references the Keep Android Open campaign.

hackernews · drewfax · Jul 2, 03:00 · [Discussion](https://news.ycombinator.com/item?id=48755965)

**Background**: F-Droid is a free and open-source app store for Android that only hosts FOSS apps. Android Developer Verification requires developers to verify their identity and submit apps for review, which F-Droid argues restricts user freedom and undermines the open-source ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/F-Droid">F-Droid</a></li>

</ul>
</details>

**Discussion**: Community comments are mixed: some users agree and advocate switching to alternative OSes like GrapheneOS or SailfishOS, while others criticize the article's tone as childish and counterproductive, suggesting the Keep Android Open site is a better resource.

**Tags**: `#Android`, `#F-Droid`, `#mobile security`, `#open source`, `#Google`

---

<a id="item-4"></a>
## [Japan top court: AI cannot be listed as inventor on patents](https://japannews.yomiuri.co.jp/science-nature/technology/20260306-314930/) ⭐️ 8.0/10

Japan's Supreme Court ruled that artificial intelligence cannot be listed as an inventor on patent applications, upholding the requirement that inventors must be natural persons. This ruling sets a clear legal precedent that AI lacks legal personhood, thereby affecting the patentability of AI-generated inventions and influencing global debates on AI and intellectual property. The case involved a petition to list an AI system as the inventor on a patent application. The court emphasized that only humans can be legally recognized as inventors under current patent law.

hackernews · mushstory · Jul 2, 13:43 · [Discussion](https://news.ycombinator.com/item?id=48761536)

**Background**: Patent laws worldwide generally require inventors to be natural persons. As AI systems become capable of generating inventions independently, questions arise about whether AI can be considered an inventor. This ruling aligns with similar decisions in the US, UK, and Europe, reinforcing the human-centric nature of patent systems.

**Discussion**: Commenters expressed mixed views: some questioned the effectiveness of patents in promoting innovation, while others supported the ruling on accountability grounds. Concerns were raised about inventors simply listing themselves as the inventor of AI-generated work, potentially bypassing the ruling.

**Tags**: `#AI`, `#patents`, `#law`, `#Japan`, `#intellectual property`

---

<a id="item-5"></a>
## [ECTC 2026 Highlights: EMIB-T, Custom HBM, and Cooling](https://newsletter.semianalysis.com/p/ectc2026) ⭐️ 8.0/10

At ECTC 2026, Intel showcased its EMIB-T packaging technology for HBM4 integration, while memory makers discussed custom HBM and packaging challenges. Novel microfluidic cooling and photonic interconnects were also highlighted. These advancements are critical for scaling AI accelerators, as they tackle power delivery, heat dissipation, and memory bandwidth limitations. The progress in packaging and interconnects will directly impact the performance and cost of next-generation AI hardware. Intel's EMIB-T supports HBM4 and future HBM5, scaling to a 120mm x 180mm package with over 38 bridges. HBM4 achieves pin speeds over 11 Gb/s, delivering >2.8 TB/s bandwidth. Microfluidic cooling etches channels directly into silicon for three times better heat removal.

rss · Semianalysis · Jul 2, 17:25

**Background**: EMIB (Embedded Multi-die Interconnect Bridge) is Intel's technology for connecting multiple dies using a small silicon bridge embedded in the substrate, enabling high-density interconnects. EMIB-T enhances it with TSVs for vertical power delivery, supporting higher-power chips like AI accelerators. HBM (High Bandwidth Memory) stacks DRAM dies vertically with a wide interface, essential for GPU and AI workloads. Microfluidic cooling integrates liquid cooling channels directly into the silicon for efficient heat removal, while photonic interconnects use light to replace electrical traces for higher bandwidth and lower power.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/intels-emib-t-heads-for-fab-rollout-this-year">Intel's EMIB-T packaging technology set for fab rollout this year — as TSMC CoWoS capacity remains limited, EMIB-T is preparing for advanced AI accelerator designs | Tom's Hardware</a></li>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://news.microsoft.com/source/features/innovation/microfluidics-liquid-cooling-ai-chips/">AI chips are getting hotter. A microfluidics breakthrough goes straight to the silicon to cool up to three times better. - Source</a></li>

</ul>
</details>

**Tags**: `#semiconductor packaging`, `#HBM`, `#photonics`, `#chiplet`, `#cooling`

---

<a id="item-6"></a>
## [Hamiltonian Neural Networks through a Differential Geometry Lens](https://www.reddit.com/r/MachineLearning/comments/1ukzdnj/hamiltonian_neural_networks_from_a_differential/) ⭐️ 8.0/10

A blog post presents Hamiltonian Neural Networks (HNNs) from a differential geometry perspective, highlighting Noether's theorem and the relationship between symmetries and conservation laws. This perspective offers a deeper understanding of why HNNs work, linking physical principles to machine learning generalization, which could inspire more robust physics-informed models. The author includes interactive visuals and emphasizes Noether's theorem, which states that every continuous symmetry corresponds to a conservation law, a concept often underexplored in physics-informed ML.

reddit · r/MachineLearning · /u/FlameOfIgnis · Jul 1, 21:55

**Background**: Hamiltonian Neural Networks are a class of neural networks that learn Hamiltonian dynamics, conserving energy and respecting physical invariants. They are inspired by Hamiltonian mechanics, which describes systems in terms of position and momentum. Noether's theorem connects symmetries to conserved quantities, offering a theoretical foundation for generalization in ML.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/1906.01563">[1906.01563] Hamiltonian Neural Networks</a></li>
<li><a href="https://greydanus.github.io/2019/05/15/hamiltonian-nns/">Hamiltonian Neural Networks</a></li>

</ul>
</details>

**Tags**: `#Hamiltonian Neural Networks`, `#Differential Geometry`, `#Physics-Informed ML`, `#Noether's Theorem`, `#Machine Learning`

---

<a id="item-7"></a>
## [Cloudflare to block mixed-purpose AI crawlers from September](https://techcrunch.com/2026/07/01/cloudflares-new-policy-pushes-ai-companies-to-pay-for-publishers-content/) ⭐️ 8.0/10

Starting September 15, Cloudflare will automatically block mixed-purpose crawlers (including Google's) that simultaneously use scraped content for search indexing and AI training or serving, effectively forcing AI companies to pay for publisher content. This policy shift addresses a long-standing loophole where publishers block AI crawlers but allow Googlebot, enabling Google to use scraped content for AI without compensation. It could set a precedent for the web scraping ecosystem and data compensation models for AI training. Cloudflare specifically called out Google for exploiting this loophole—servers cannot easily distinguish between search indexing and AI training when the same user agent (Googlebot) is used. The policy only applies to pages with ads, and Cloudflare plans future pricing for actual usage rather than just crawling.

telegram · zaihuapd · Jul 2, 05:37

**Background**: Web crawlers are bots that systematically browse websites, typically used by search engines for indexing. A mixed-purpose crawler refers to one that performs multiple functions like searching, AI query answering, and model training concurrently. Publishers have long struggled to block AI crawlers without blocking search engine bots, and Cloudflare's move provides a technical solution.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Web_crawler">Web crawler - Wikipedia</a></li>
<li><a href="https://www.cloudflare.com/learning/bots/what-is-a-web-crawler/">What Is a Web Crawler ? | How Web Spiders Work</a></li>

</ul>
</details>

**Tags**: `#Cloudflare`, `#AI Crawlers`, `#Google`, `#Web Scraping`, `#Content Policy`

---

<a id="item-8"></a>
## [OpenAI Proposes US Government 5% Stake, Eyes Other AI Giants](https://www.bloomberg.com/news/articles/2026-07-02/openai-proposes-giving-the-us-government-a-5-stake-ft-says) ⭐️ 8.0/10

OpenAI has proposed that the US government hold a 5% stake in the company, and is also considering a broader vehicle that would include stakes in other major AI firms such as Google and Meta, according to a Bloomberg report. This proposal could reshape AI governance by linking public benefit to corporate profits, potentially setting a precedent for government participation in technology companies and influencing the distribution of AI-driven economic gains. The plan is reportedly being discussed internally by OpenAI CEO Sam Altman and other executives, but it remains unclear whether other companies like Google and Meta would accept such an arrangement, which could raise concerns over regulatory control and conflicts of interest.

telegram · zaihuapd · Jul 2, 06:02

**Background**: OpenAI is a leading AI research organization that developed GPT models and ChatGPT. The proposal comes amid growing debate over how the benefits of AI should be shared, with some advocating for public ownership or redistribution mechanisms. Government stakes in private companies are rare in the US tech sector but exist in strategic industries.

**Tags**: `#OpenAI`, `#AI政策`, `#美国政府`, `#公司治理`, `#AI产业`

---

<a id="item-9"></a>
## [Citibank blocks GPT-5.5 as AI costs surge, firms limit usage](https://www.404media.co/companies-are-throttling-employees-ai-use-because-its-too-expensive/) ⭐️ 8.0/10

Citibank disabled access to GPT-5.5, Claude Opus 4.6, and 4.7 on June 24, 2026, citing excessive AI credit consumption. Atlassian's AI spending tripled to over $15 million monthly by May 2026, and Adobe declined to renew its unlimited Claude contract. This trend highlights the real-world cost challenges of adopting frontier AI models in enterprises, potentially slowing internal AI adoption and forcing businesses to develop stricter usage policies or seek more cost-effective alternatives. Atlassian's internal dashboard showed AI spending rising from $5 million in August 2025 to over $15 million in May 2026, leading to the end of unlimited usage and introduction of cost-tracking panels. Amazon had previously shut down an internal ranking that encouraged AI use, and employees later discovered previously unknown token usage caps.

telegram · zaihuapd · Jul 2, 13:59

**Background**: Enterprise AI tools like GPT-5.5 and Claude Opus operate on token-based pricing, where each query consumes a certain number of tokens. Companies often provide employees with a pool of AI credits; expensive frontier models can quickly deplete these credits, leading to unexpected cost overruns. GPT-5.5 is OpenAI's frontier model released in April 2026, known for strong reasoning capabilities but higher per-token cost.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.5">GPT-5.5</a></li>
<li><a href="https://openrouter.ai/openai/gpt-5.5">GPT - 5 . 5 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://www.afternoon.co/blog/token-based-pricing-guide">Token-Based Pricing: How to Account for AI Credits and LLM Usage | Afternoon Blog</a></li>

</ul>
</details>

**Tags**: `#AI`, `#enterprise`, `#cost`, `#productivity`, `#news`

---

<a id="item-10"></a>
## [Anthropic in talks with Samsung for custom AI chips](https://www.theinformation.com/articles/anthropic-talks-samsung-manufacture-custom-ai-chip) ⭐️ 8.0/10

Anthropic has begun developing its own custom AI chips and is in early-stage talks with Samsung Electronics for potential manufacturing. This move aims to increase control over the computing infrastructure for its Claude model. This signals vertical integration in AI hardware by a leading AI company, following similar moves by OpenAI and others. It could reduce reliance on third-party chip suppliers and potentially optimize performance for Anthropic's specific workloads. The project is still in very early stages, and Anthropic is entering later than some competitors who have already advanced their own server chip efforts. Samsung Foundry offers advanced process technologies including 3nm GAA (Gate-All-Around) transistors.

telegram · zaihuapd · Jul 2, 15:57

**Background**: Custom AI chips are specialized semiconductors designed to accelerate machine learning workloads more efficiently than general-purpose chips like GPUs. Samsung Foundry is one of the world's largest semiconductor contract manufacturers, offering fabrication services for companies designing their own chips. Anthropic is the developer of the Claude family of large language models, which are trained using constitutional AI techniques.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Samsung_Foundry">Samsung Foundry</a></li>
<li><a href="https://semiconductor.samsung.com/foundry/">Foundry Overview | Samsung Semiconductor Global</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_(language_model)">Claude (language model)</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#Anthropic`, `#Samsung`, `#custom silicon`, `#AI hardware`

---