---
layout: default
title: "Horizon Summary: 2026-10-17 (EN)"
date: 2026-10-17
lang: en
---

> From 37 items, 8 important content pieces were selected

---

1. [Claude Traces NIST ECDSA Curve Seeds to lrand48 Timestamps](#item-1) ⭐️ 9.0/10
2. [llama.cpp runs natively on jailbroken PS5 with any GGUF model](#item-2) ⭐️ 8.0/10
3. [Jake Archibald compares JPEG XL and AVIF for real-world web use](#item-3) ⭐️ 8.0/10
4. [Researchers Exploit 37-Year-Old Kernel Bug in OpenBSD](#item-4) ⭐️ 8.0/10
5. [ORL and dlmrt: 2,788 tokens/s diffusion LLM decoding on one RTX 5090](#item-5) ⭐️ 8.0/10
6. [China&\#x27;s MOFCOM Proposes Temporary Export Registration for AI, Biomedicine, Solar Tech](#item-6) ⭐️ 8.0/10
7. [Court Documents Reveal Telegram Handed US User Data to Law Enforcement](#item-7) ⭐️ 8.0/10
8. [Anthropic IPO Valuation Expectations Reportedly Cut to $1.5 Trillion](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Claude Traces NIST ECDSA Curve Seeds to lrand48 Timestamps](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 9.0/10

Anthropic&\#x27;s Frontier Red Team reported that Claude, in under half an hour, traced the seed values behind the NIST P-192, P-224, P-256, P-384 and P-521 elliptic curves to the C library&\#x27;s lrand48 pseudorandom generator seeded with a Unix timestamp. None of the seeds turned out to be the output of a hash algorithm or the hashing of a memorable phrase, as had long been assumed. This resolves a mystery that fueled roughly two decades of speculation that the NSA deliberately chose the NIST curves to embed a backdoor, and it demonstrates that a frontier LLM can carry out original cryptographic reverse-engineering rather than just summarizing existing work. It could change how the community assesses trust in standardized curve parameters and in the &quot;verifiably random&quot; claims attached to them. The fifth binary seed, B-163, still fits nothing Claude has tried and remains unexplained, and researchers caution that confirming the generation method does not rule out the possibility that candidates were generated and discarded until a curve with some desired property appeared. Only the derivation of the seeds is confirmed, not the selection of the final curves.

hackernews · ahlCVA · Oct 16, 18:55 · [Discussion](https://news.ycombinator.com/item?id=50122800)

**Background**: ECDSA \(Elliptic Curve Digital Signature Algorithm\) is the most widely deployed elliptic curve cryptography standard, and NIST standardized a set of named curves in FIPS 186-2 in 2000. Each parameter set carries a &quot;seed&quot; that was supposed to have been hashed to derive the curve coefficients, giving users a way to check that a curve was not maliciously constructed. Because NIST never explained where those seeds came from — and given episodes such as the Dual\_EC\_DRBG backdoor — cryptographers including Neal Koblitz and Alfred Menezes treated the &quot;verifiably random&quot; claim with suspicion. lrand48 is an old C library pseudo-random generator based on a linear congruential algorithm over 48-bit integers, and it is trivially predictable once its seed is known.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/ecdsa-curve-origins">Claude reveals ECDSA curve origins \ Anthropic</a></li>
<li><a href="https://www.ibm.com/docs/en/zvm/7.5.0?topic=descriptions-lrand48-generate-pseudorandom-number">lrand 48 () — Generate Pseudorandom Number</a></li>
<li><a href="https://www.explainx.ai/blog/claude-ecdsa-nist-curve-seeds-lrand48-anthropic-frontier-red-team-backdoor-question-2026">ECDSA Curve Seeds Solved: Claude Found lrand48 (2026 ...</a></li>

</ul>
</details>

**Discussion**: Commenters reacted with dark amusement — one summed it up as &quot;13 years of tinfoil hats for srand48\(time\(NULL\)\)&quot;, while Thomas Ptacek called it &quot;devastating news... for an entire generation of NIST cryptography conspiracy theories&quot;. Others were more cautious: one noted that confirming the production method says nothing about which candidates were selected or discarded, since the values appear to have been generated over a period of months, so a deliberate search over timestamps cannot be fully excluded. Another suggested the unexplained B-163 seed may simply be a typo introduced somewhere on the way to publication.

**Tags**: `#cryptography`, `#ECDSA`, `#NIST curves`, `#random number generation`, `#AI/LLM`

---

<a id="item-2"></a>
## [llama.cpp runs natively on jailbroken PS5 with any GGUF model](https://github.com/cobanov/PS5LM) ⭐️ 8.0/10

A GitHub project called cobanov/PS5LM demonstrates running native GGUF model inference through llama.cpp directly on a jailbroken PlayStation 5 console, turning Sony&\#x27;s locked-down game machine into a general-purpose local LLM host. The release is a proof of concept that reportedly runs a Qwen 3 27B model at a 2-bit quantization. It shows that a mass-market, heavily locked-down console can be repurposed as a cheap always-on LLM inference box, an appealing alternative to pricey GPUs for long-running, low-intensity workloads. It also reinforces llama.cpp&\#x27;s position as the de facto portable inference core that can be ported to almost any hardware, from phones to servers to game consoles. The reported configuration runs Qwen 3 27B at a 2-bit quantization, which limits output quality but is still usable for tasks that only need a steady, roughly average-quality token stream. Commenters estimate about 70 cents per day in electricity for roughly 2M output tokens per day, and note the approach may also work on BC250 boards built around AMD&\#x27;s cut-down &quot;Cyan Skillfish&quot; APU, which sell on eBay for $150–$200.

hackernews · Anon84 · Oct 16, 18:32 · [Discussion](https://news.ycombinator.com/item?id=50122431)

**Background**: llama.cpp is an open-source C/C++ library started by Georgi Gerganov in March 2023 that performs inference on large language models and is co-developed with the GGML tensor library; it has become the core of most local inference tools, including Ollama and LM Studio. GGUF \(GGML Universal File\) is a binary format that stores model tensors and metadata in a single file so models load and save quickly. Jailbreaking a PlayStation 5 means exploiting software or hardware vulnerabilities to run unsigned code on the console, which normally only runs Sony-approved software. The PS5 uses a custom AMD APU with unified memory, which is why it is attractive as a low-cost inference machine once unlocked.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Llama.cpp">Llama.cpp</a></li>
<li><a href="https://github.com/ggml-org/llama.cpp">GitHub - ggml-org/llama.cpp: LLM inference in C/C++</a></li>
<li><a href="https://grokipedia.com/page/PlayStation_5_jailbreak">PlayStation 5 jailbreak</a></li>

</ul>
</details>

**Discussion**: Commenters are enthusiastic about turning a locked-down appliance into a general-purpose computer, with one framing it as ideal for long-running, low-stakes tasks such as monitoring server error rates, reviewing security footage, or controlling plant watering, and another imagining LLM-powered NPCs becoming standard in games. The main concern is hosting risk: one commenter argues the project should not live primarily on GitHub because Sony could take the page down at any moment and recommends a custom domain instead. Others point to hardware alternatives like the BC250 and its cut-down PS5-derived APU as a cheaper path to the same result.

**Tags**: `#LLM inference`, `#jailbreaking`, `#PS5`, `#llama.cpp`, `#GGUF`

---

<a id="item-3"></a>
## [Jake Archibald compares JPEG XL and AVIF for real-world web use](https://jakearchibald.com/2026/jpeg-xl-vs-avif/) ⭐️ 8.0/10

Web performance expert Jake Archibald published a practical comparison of JPEG XL and AVIF for real-world web use cases, weighing encoding speed, file sizes, and quality trade-offs. The post triggered a 143-comment Hacker News discussion in which implementers shared concrete ffmpeg/AVIF settings and explained why libjxl&\#x27;s high-effort modes are so slow. Image format choice directly affects page weight, load performance, and bandwidth costs for virtually every website, so a credible, hands-on comparison helps developers make a concrete engineering decision rather than relying on vendor benchmarks. It also signals that the JPEG XL versus AVIF debate is still unsettled, which matters for teams deciding which formats to encode and serve today. Commenters noted that libjxl&\#x27;s maximum effort only produces files 2–7% smaller than its default for photos \(~25% for screenshots and illustrations\) yet takes 9–46 seconds, 50–180x as long as the default, largely because of an iterative evaluation-optimization loop over the perceptual metric Butteraugli. One developer shared ffmpeg settings using yuva444p with alpha extraction to produce AVIF files over 10x smaller while preserving PNG transparency, while another argued AVIF&\#x27;s handling of highlights \(e.g. in an F1 photo\) shows visible quality loss.

hackernews · farlight · Oct 16, 16:12 · [Discussion](https://news.ycombinator.com/item?id=50120224)

**Background**: JPEG XL is a next-generation image format supporting both lossy and lossless compression, developed by the JPEG committee together with Google and Cloudinary, and it gained mainstream attention after native support in the iPhone 16 series. AVIF is an image format built on the AV1 video codec by the Alliance for Open Media, designed to shrink images while preserving perceived quality; both are royalty-free and widely pitched as successors to JPEG and WebP for the web.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/JPEG_XL">JPEG XL - Wikipedia</a></li>
<li><a href="https://shortpixel.com/blog/what-is-avif-and-why-is-it-good/">What is AVIF and why is it good? - ShortPixel Blog</a></li>
<li><a href="https://www.keycdn.com/blog/avif">AV1 Image File Format ( AVIF ) - KeyCDN</a></li>

</ul>
</details>

**Discussion**: Overall sentiment was pragmatic and cautious rather than triumphalist: commenters dug into technical specifics like libjxl&\#x27;s Butteraugli optimization loop and shared battle-tested AVIF encoding commands, while a veteran of the MP3/LAME era cautioned against declaring any codec a &quot;winner&quot; before years of maturation, recalling that WebP&\#x27;s superiority claims also failed to fully pan out. Criticism also surfaced that AVIF can replace fine highlight detail with plausible-looking artifacts, which some see as disqualifying for certain photographic use cases.

**Tags**: `#image-compression`, `#web-performance`, `#jpeg-xl`, `#avif`, `#codecs`

---

<a id="item-4"></a>
## [Researchers Exploit 37-Year-Old Kernel Bug in OpenBSD](https://calif.io/research/big-fish) ⭐️ 8.0/10

Security researchers published a detailed write-up titled &quot;Big Fish&quot; describing how they discovered and successfully exploited a kernel vulnerability in OpenBSD that had survived undetected for roughly 37 years, tracing back to shared 4.4BSD-era code. The disclosure triggered discussion about why long-lived bugs can slip past even one of the most heavily audited codebases in the world. OpenBSD is widely regarded as the most security-focused mainstream Unix-like system, so a 37-year-old exploitable kernel bug undermines the assumption that aggressive source auditing alone prevents serious flaws. The case also matters for the broader BSD family and any project reusing decades-old C code, raising questions about how much trust to place in inherited, long-reviewed code. According to community discussion, the same flawed code was accidentally corrected in NetBSD during a rewrite of that section in August 1999, meaning NetBSD incidentally avoided the problem while OpenBSD retained it. Commenters also debated whether automated fuzzing or static analysis could realistically have caught this specific class of bug, or whether exploiting it required human insight into the underlying primitive.

hackernews · rs\_rs\_rs\_rs\_rs · Oct 16, 14:44 · [Discussion](https://news.ycombinator.com/item?id=50118977)

**Background**: OpenBSD is a free, open-source, security-focused Unix-like operating system created by Theo de Raadt in 1995 as a fork of NetBSD 1.0, which itself descends from the Berkeley Software Distribution \(BSD\) code base; it emphasizes portability, correctness, proactive security and integrated cryptography. Fuzzing is an automated testing technique that feeds programs invalid, unexpected or random inputs and watches for crashes or memory errors, while static analysis examines source code without executing it to flag suspicious patterns. Because both techniques are routinely used on mature kernels, the survival of this bug for nearly four decades is what makes the finding notable.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenBSD">OpenBSD - Wikipedia</a></li>
<li><a href="https://www.openbsd.org/faq/faq1.html">OpenBSD FAQ: Introduction to OpenBSD What Is OpenBSD? Everything You Need to Know - MUO What Is OpenBSD? Everything You Need to Know - The Tech Edvocate What Is OpenBSD? - Computer Hope What Is OpenBSD? – ITU Online IT Training</a></li>
<li><a href="https://en.wikipedia.org/wiki/Fuzzing">Fuzzing - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread \(162 points, 46 comments\) was broadly appreciative, with one commenter praising the OpenBSD-release-style graphics and joking about a forthcoming theme song. A key technical observation was that NetBSD accidentally fixed the same bug during an August 1999 rewrite, and a recurring debate centered on whether fuzzing or static analysis could realistically have found this class of bug, or whether it fundamentally required a human reasoning about the exploit primitive.

**Tags**: `#security`, `#openbsd`, `#kernel`, `#vulnerability-research`, `#exploit-development`

---

<a id="item-5"></a>
## [ORL and dlmrt: 2,788 tokens/s diffusion LLM decoding on one RTX 5090](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 8.0/10

A research team released ORL \(On-Policy Residual Learning\), a training method for diffusion language models \(dLLMs\), together with dlmrt, a custom inference engine, reporting up to 2,788 tokens/s single-request decoding on a single RTX 5090 \(LLaDA-2.1-mini + ORL\), 7,708 tokens/s on 8× B200 with DiffusionGemma 26B MoE + ORL in NVFP4, and up to 6.9× higher end-to-end throughput on their QwenDLM-4B model at comparable or better quality. They also report a single-request H100 comparison where QwenDLM-4B + ORL reaches 1,298 tokens/s, which is 1.74× faster than DFlash speculative decoding and well ahead of EAGLE3 \(405 tokens/s\) at matched measured accuracy. Models, training code, evaluation pipeline, and the inference engine are all open sourced. Diffusion LLMs have long promised parallel token generation but have rarely delivered practical speedups over autoregressive models; ORL plus dlmrt claims to change that by beating established speculative-decoding methods while also running fast on a consumer Blackwell GPU. If the results hold up, it could shift inference economics toward diffusion decoding and make high-throughput local deployment on single consumer GPUs far more viable. The team is explicit that all reported figures are single-request decoding \(batch size 1\) peak results on specific benchmarks, not aggregate throughput or averages across arbitrary prompts; the LLaDA-2.1-mini variant needed only 4.2M self-generated training tokens and 36 H100 GPU-hours of post-training, while QwenDLM-4B improved HumanEval pass@1 from 82.9% to 89.6%. dlmrt captures the entire denoising loop in a CUDA graph and executes it on the GPU instead of synchronizing each step from the CPU, supports NVFP4 inference on Blackwell \(including the RTX 5090\), and is reported to run 1.2–1.6× faster than SGLang/vLLM at identical models and settings on a single H100.

reddit · r/MachineLearning · /u/arty\_photography · Oct 16, 20:03

**Background**: Autoregressive LLMs generate text one token at a time, so a forward pass is needed for every output token; diffusion language models instead start from masked or noisy tokens and iteratively denoise many positions in parallel, finalizing several tokens per forward pass. Residual learning means the model carries its own previous predictions forward as context and refines them across denoising steps, and ORL&\#x27;s insight is that this process is inherently &quot;on-policy&quot;: the residual states encountered at inference are produced by the current model itself, so training on stale offline residuals causes a mismatch. Adjacent Entropy Contraction is the auxiliary objective that pushes each denoising step to reduce uncertainty relative to the previous one, while NVFP4 is a 4-bit floating-point format available on Nvidia&\#x27;s Blackwell GPUs, and DFlash and EAGLE3 are speculative-decoding methods that accelerate conventional autoregressive models.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2610.20687v1">On-Policy Residual Learning for Diffusion Language Models</a></li>
<li><a href="https://github.com/Introspective-Diffusion/ORL/blob/main/">ORL: On-Policy Residual Learning for Diffusion Language Models</a></li>

</ul>
</details>

**Tags**: `#diffusion-llm`, `#llm-inference`, `#inference-optimization`, `#open-source`, `#nvfp4-quantization`

---

<a id="item-6"></a>
## [China&\#x27;s MOFCOM Proposes Temporary Export Registration for AI, Biomedicine, Solar Tech](https://aqygzj.mofcom.gov.cn/flzc/gzjgfxwj/art/2026/art_c99f95ca0cd043829ac9991495fc283c.html) ⭐️ 8.0/10

China&\#x27;s Ministry of Commerce has opened a public comment period on a proposed revision to the《China Catalogue of Technologies Prohibited or Restricted from Export》, covering 40 technologies across three fields: AI, biomedicine, and photovoltaics. The AI section lists 23 technologies including large models, intelligent agents, and compute clusters; biomedicine covers 5 technologies such as cell and gene therapy, small nucleic acid drugs, and pathogenic microorganisms; and photovoltaics covers 12 technologies spanning polysilicon, wafer, and cell manufacturing. This is a significant regulatory development that signals China intends to guard its competitive advantages in AI, biotech, and solar supply chains, potentially disrupting global technology collaboration and cross-border licensing deals. It affects multinational firms that license Chinese technology, researchers who collaborate internationally, and global supply chains in semiconductors, renewable energy, and pharmaceuticals. The proposal includes carve-outs: technologies already in the public domain through open-source release or academic publication would not be managed, and outward licensing models that do not involve transfer of ownership would qualify for automatic licensing and other facilitation measures. For photovoltaics, the scope also extends to key and core equipment that embodies the relevant technologies.

telegram · zaihuapd · Oct 16, 09:12

**Background**: Export control catalogues determine which technologies Chinese companies and individuals must obtain government approval before transferring abroad, and revisions are typically opened for public comment before taking effect. The three targeted fields are areas where China has become a global leader — large language models and AI compute clusters, next-generation nucleic acid therapeutics, and the solar manufacturing chain that supplies most of the world&\#x27;s panels. &\#x27;Temporary registration&\#x27; would place these technologies under a lighter, provisional form of control while the catalogue is finalized.

<details><summary>References</summary>
<ul>
<li><a href="https://pubmed.ncbi.nlm.nih.gov/39309508/">Current status and trends in small nucleic acid drug ... - PubMed</a></li>
<li><a href="https://ayarlabs.com/glossary/ai-compute-cluster/">AI Compute Cluster Definition | Understanding AI Clusters</a></li>

</ul>
</details>

**Tags**: `#China regulation`, `#export controls`, `#AI policy`, `#biotechnology`, `#photovoltaics`

---

<a id="item-7"></a>
## [Court Documents Reveal Telegram Handed US User Data to Law Enforcement](https://www.404media.co/heres-what-telegram-giving-data-to-the-u-s-government-looks-like/) ⭐️ 8.0/10

Newly released court documents show that Telegram provided a user&\#x27;s phone number, user ID, and IP address to US law enforcement in response to a US court order, describing the disclosure in a letter as &quot;voluntary&quot; while refusing to acknowledge US jurisdiction. As of January this year, Telegram had supplied data on a total of 2,253 users to US authorities. The disclosure sharply contradicts Telegram&\#x27;s long-cultivated reputation as a privacy-first messenger, and it suggests that US courts can effectively extract data from foreign platforms that publicly deny American jurisdiction. It also signals to other messaging services and their users that the phone number, account ID, and IP metadata held on servers remain reachable by law enforcement regardless of a company&\#x27;s public stance. The request centered on Mahmoud Al-Muhtadi, who has been accused of involvement in the October 7, 2023 attacks on Israel, and the data turned over — phone number, user ID, and IP address — is exactly the type of account metadata a messaging provider stores on its servers. Telegram&\#x27;s phrasing is notable: it framed the handover as voluntary rather than compelled, a legal posture that avoids conceding that a US court order binds the company.

telegram · zaihuapd · Oct 16, 14:57

**Background**: Telegram is a messaging app founded by Pavel Durov that has long marketed itself on privacy and on being outside the reach of most national governments, even though its standard cloud chats are not end-to-end encrypted. US courts can reach foreign companies through so-called long-arm jurisdiction, which extends a court&\#x27;s authority to defendants outside its territory when they have sufficient minimum contacts with the jurisdiction. 404 Media is an independent technology-journalism outlet founded in 2023 by former Motherboard reporters, known for publishing leaked documents and investigative reports.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/%E9%95%BF%E8%87%82%E7%AE%A1%E8%BE%96%E6%9D%83">长臂管辖权 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.kangdalawyers.com/library/834.html">从中兴、华为事件看美国法律的长臂管辖原则</a></li>
<li><a href="https://www.404media.co/">404 Media</a></li>

</ul>
</details>

**Tags**: `#Telegram`, `#隐私`, `#数据披露`, `#政府监控`, `#科技政策`

---

<a id="item-8"></a>
## [Anthropic IPO Valuation Expectations Reportedly Cut to $1.5 Trillion](https://www.reuters.com/business/finance/investors-temper-anthropic-ipo-valuation-expectations-over-revenue-growth-2026-10-15/) ⭐️ 8.0/10

Reuters reports that some investors have lowered their expected valuation for Anthropic&\#x27;s upcoming IPO from roughly $2 trillion to about $1.5 trillion. The downgrade comes despite Anthropic posting Q3 revenue of $16.8 billion, up 45% quarter-over-quarter, along with adjusted profitability and positive quarterly cash flow. Because Anthropic is one of the largest privately held AI model developers, a lower IPO valuation could serve as a reality check for the entire sector and pressure the valuations of other AI companies. The report explicitly frames it as a stress test for Chinese AI firms such as Zhipu, MiniMax, Moonshot AI&\#x27;s Kimi and DeepSeek, shifting investor focus toward revenue durability, gross margins and capital efficiency. The cut is attributed to three pressures: slowing growth rates, intensifying price competition among frontier models, and the heavy capital demands of compute build-out. Notably, the reduction occurred even though the company is reportedly profitable on an adjusted basis and cash-flow positive, suggesting investors are discounting future growth rather than current financial health.

telegram · zaihuapd · Oct 16, 15:46

**Background**: Anthropic is an AI company known for its Claude family of large language models and is one of the leading competitors to OpenAI. An IPO \(initial public offering\) is the process by which a private company lists shares on a public stock exchange; the valuation expectation reflects what investors think the company will be worth at that moment. Valuation in this sector is largely driven by revenue trajectory, model pricing power and the cost of the GPUs and data centers needed to train and serve models. Reuters&\#x27; comparison set includes Chinese model developers such as Zhipu, MiniMax, Kimi \(Moonshot AI\) and DeepSeek, which are candidates for their own listings or funding rounds.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/%E6%99%BA%E8%B0%B1">智谱 - 维基百科，自由的百科全书</a></li>
<li><a href="https://duoke360.com/post/46091">MiniMax 大 模 型 简 介 - 多课网</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#IPO`, `#AI industry`, `#valuation`, `#market analysis`

---