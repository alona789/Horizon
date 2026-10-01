---
layout: default
title: "Horizon Summary: 2026-10-01 (EN)"
date: 2026-10-01
lang: en
---

> From 34 items, 6 important content pieces were selected

---

1. [Google Announces Gemini 4 Argon Frontier Model](#item-1) ⭐️ 9.0/10
2. [EDG open-sources its long-standing commercial C++ front-end as company winds down](#item-2) ⭐️ 8.0/10
3. [DeepSeek open-sources full foundational software stack for Huawei Ascend](#item-3) ⭐️ 8.0/10
4. [Cloudflare to Become a Public Certificate Authority](#item-4) ⭐️ 8.0/10
5. [Kimi K3 Lands in OpenAI Codex Enterprise Channel via Baseten](#item-5) ⭐️ 8.0/10
6. [Reddit to Kill RSS Feeds and Shut Down Public API](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google Announces Gemini 4 Argon Frontier Model](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/) ⭐️ 9.0/10

Google announced Gemini 4 Argon, its new frontier model positioned above the Gemini 3.8 line, targeting real-world coding, enterprise knowledge work \(such as legal tasks\), and cyber defense, with a rollout planned soon. The announcement landed with 984 points and 666 comments on Hacker News, alongside a companion analysis post on its intelligence, performance, and price. Argon is Google&\#x27;s most advanced model to date and represents another leap in the rapid back-and-forth between frontier labs, which is increasingly being read as evidence that AI capabilities are becoming distributed across hyperscalers, neoclouds, and startups rather than concentrating in a single winner-take-all leader. Its push into agentic coding and cyber defense also signals where large vendors expect enterprise value to accrue next. Google says it will keep gathering feedback from early testers to iterate on guardrails before making Argon available to developers, enterprises, and consumers, which drew criticism that the model is effectively announced before it can be shipped; the blog also highlights Argon agents working on migrating C/C++ codebases to Rust across Google.

hackernews · bradleyg223 · Sep 30, 20:04 · [Discussion](https://news.ycombinator.com/item?id=49913571)

**Background**: Gemini is Google&\#x27;s family of large language models, and each named generation \(here the Gemini 3.8 line and now Gemini 4 Argon\) generally marks a step up in reasoning, coding, and long-horizon task performance. Agentic coding refers to AI systems that work at the project level rather than the file level, reading configuration and test files, tracing dependencies, and carrying out multi-step development tasks with limited human intervention. The &\#x27;concentrating&\#x27; thesis, associated with Anthropic CEO Dario Amodei, holds that AI is a winner-take-all field in which an early lead is never given back.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/">Introducing Gemini 4 Argon - The Keyword</a></li>
<li><a href="https://www.cnbc.com/2026/09/30/google-gemini-4-argon-ai.html">Google rolls out Gemini 4 Argon, its most advanced model - CNBC</a></li>
<li><a href="https://www.datacamp.com/blog/gemini-4-argon">Gemini 4 Argon: Benchmarks, Pricing, and Access | DataCamp</a></li>

</ul>
</details>

**Discussion**: Commenters were largely impressed by the model&\#x27;s agentic capabilities — one recounted Gemini 3.8 Flash attaching GDB to a GPU driver, reverse-engineering the kernel queue ioctl interface, and writing an LD\_PRELOAD shim to get ROCm llama.cpp working on a Strix Halo machine. Several used the release to argue against Amodei&\#x27;s winner-take-all thesis, noting AI now looks more distributed across neoclouds, hyperscalers, GPU and ASIC vendors, and startups, while others criticized Google for announcing before shipping \(&\#x27;can&\#x27;t release a model allegations&\#x27;\) and advised developers to keep models and providers replaceable so intelligence becomes a commodity.

**Tags**: `#AI/ML`, `#Google Gemini`, `#LLM`, `#Model Release`, `#Industry Analysis`

---

<a id="item-2"></a>
## [EDG open-sources its long-standing commercial C++ front-end as company winds down](https://edgcpp.org/#transition) ⭐️ 8.0/10

Edison Design Group \(EDG\), a long-time maker of commercial C++ compiler front-ends, has published its C++ front-end as open source on GitHub \(github.com/edgcpp/compiler\) with the announcement hosted at edgcpp.org. The release appears tied to the company winding down, and the code carries a history reaching back to the earliest commits in 1990. EDG&\#x27;s front-end is widely regarded for its rigorous standards conformance and has been licensed into other commercial compilers and analysis tools, so its open-sourcing gives the broader C++ ecosystem a battle-tested parser and semantic analyzer that was previously only available under commercial license. Because the company is winding down, this could preserve a critical piece of compiler infrastructure that many tools have historically relied on. The repository is licensed under Apache-2.0 WITH LLVM-exception, and the source retains its full version history from 1990 onward, which commenters noted is unusual for an open-sourcing event. The front-end supports ISO C++ standards through C++17 \(with C++20 work in progress\) and can also be configured for ANSI/ISO C and Microsoft language extensions.

hackernews · iandinwoodie · Sep 30, 19:26 · [Discussion](https://news.ycombinator.com/item?id=49913192)

**Background**: A compiler front-end is the language-dependent portion of a compiler that preprocesses, parses, and analyzes source code into an intermediate, machine-independent representation, before back-end stages generate target code. EDG \(Edison Design Group\) built one of the best-known commercial C++ front-ends, widely used inside other compilers and code-analysis tools, notably as the parsing engine behind Visual C++ IntelliSense even though Visual C++ uses the MSVC compiler for actual code generation.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Edison_Design_Group">Edison Design Group - Wikipedia</a></li>
<li><a href="https://www.edg.com/c">The C++ Front End - edg.com</a></li>
<li><a href="https://jszhn.github.io/brain/Compiler-front-end">Compiler front - end</a></li>

</ul>
</details>

**Discussion**: Commenters broadly framed this as a major event for C++, with jabl pointing out that the announcement omits the company&\#x27;s wind-down as the likely motive. Others highlighted practical angles: badsectoracula speculated about using the source-to-source capability to transpile C++ libraries into languages like Free Pascal, vintagedave noted EDG&\#x27;s front-end is the engine behind Visual C++ IntelliSense, and trebligdivad found the 1990-dated commit history refreshingly unusual for an open-source release.

**Tags**: `#C++`, `#compilers`, `#open-source`, `#EDG`, `#tooling`

---

<a id="item-3"></a>
## [DeepSeek open-sources full foundational software stack for Huawei Ascend](https://mp.weixin.qq.com/s/X41mKH4Ds-VXUAnK6M8Eww) ⭐️ 8.0/10

DeepSeek open-sourced a set of foundational components for Huawei&\#x27;s Ascend platform, including the TileLang high-level compiler tooling plus compute and distributed communication libraries, alongside Ascend ports of DeepGEMM, DeepEP, TileKernels, FlashMLA and DeepSelect. DeepSeek said the components reach near-hardware-limit performance in multiple benchmarks and that it is working with Huawei on a 128-card supernode design for the Ascend 950. This effectively replicates DeepSeek&\#x27;s NVIDIA-oriented toolchain on Huawei silicon, which is a meaningful step toward a non-NVIDIA training and inference ecosystem rather than a one-off kernel port. If the near-hardware-limit claims hold up, it lowers the cost of migrating DeepSeek-family models and tooling onto Ascend NPUs and strengthens the case for Chinese AI hardware inside domestic labs and enterprises. The Ascend port of DeepGEMM is described as fully API-compatible with the original DeepGEMM and supports BF16, FP8 and FP4 GEMM as well as MQA logits, with an MIT license; TileLang is a composable tiled programming model that decouples dataflow from scheduling so developers can leave most optimization work to the compiler. Because the API shape is preserved, existing code written against DeepGEMM&\#x27;s interfaces can keep the same development workflow when retargeted to Ascend NPUs.

telegram · zaihuapd · Sep 30, 03:09

**Background**: Huawei&\#x27;s Ascend NPUs are China&\#x27;s leading alternative to NVIDIA GPUs, but their software ecosystem has historically lagged behind CUDA, making it hard to move modern LLM training and inference workloads onto them. DeepSeek&\#x27;s earlier releases — DeepGEMM \(efficient GEMM kernels, notably FP8\), DeepEP \(expert-parallel communication for MoE models\) and FlashMLA \(optimized multi-head latent attention kernels powering DeepSeek-V3\) — were built for NVIDIA hardware, and TileLang is a higher-level tiled DSL for authoring such AI kernels. The Ascend versions mean the same layer of the stack DeepSeek uses to train and serve its models now has a matching implementation on domestic silicon.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/DeepGEMM-Ascend">GitHub - deepseek-ai/ DeepGEMM - Ascend : DeepGEMM - Ascend ...</a></li>
<li><a href="https://arxiv.org/abs/2504.17577">[2504.17577] TileLang: A Composable Tiled Programming Model ...</a></li>
<li><a href="https://github.com/deepseek-ai/FlashMLA">GitHub - deepseek-ai/ FlashMLA : FlashMLA : Efficient Multi-head...</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#Huawei Ascend`, `#open-source`, `#AI infrastructure`, `#distributed training`

---

<a id="item-4"></a>
## [Cloudflare to Become a Public Certificate Authority](https://blog.cloudflare.com/cloudflare-certificate-authority/) ⭐️ 8.0/10

Cloudflare announced plans to become a public certificate authority, having applied to the Chrome, Apple, Microsoft, and Mozilla root programs and signed an agreement with GlobalSign to acquire a widely trusted root certificate. The company has not yet begun issuing certificates, but says it will prioritize ACME-based automated issuance and renewal and aims to issue production-grade Merkle Tree Certificates for the post-quantum internet in Q1 2027. A major CDN and security vendor entering the public CA market could reshape a PKI industry long dominated by a handful of commercial and non-profit issuers, and it gives Cloudflare a chance to push ACME-first automation and post-quantum certificate formats directly into the WebPKI trust stores. Every site behind Cloudflare&\#x27;s network could eventually obtain certificates without leaving the platform, tightening its integration with the broader TLS ecosystem. Cloudflare is not starting from zero on trust: the GlobalSign agreement gives it an already widely trusted root, which can shorten the multi-year audit and browser-vetting process that new CAs normally face. The headline technical commitment is Merkle Tree Certificates, a proposed format designed to keep post-quantum authentication lightweight enough for the web, targeted for production issuance in Q1 2027.

telegram · zaihuapd · Sep 30, 06:26

**Background**: A certificate authority is an entity whose root certificate is embedded in browsers and operating systems, allowing it to vouch for the identity of websites through TLS. To reach that status, a CA must pass audits and be accepted into root programs run by vendors such as Chrome, Apple, Microsoft, and Mozilla. ACME is the industry-standard protocol, originally designed for Let&\#x27;s Encrypt, that automates certificate issuance and renewal; Merkle Tree Certificates are a newer proposal meant to make the much larger post-quantum signature schemes practical for the public web.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automatic_Certificate_Management_Environment">Automatic Certificate Management Environment - Wikipedia</a></li>
<li><a href="https://www.sectigo.com/blog/what-are-merkle-tree-certificates-mtcs">What are Merkle Tree Certificates (MTCs)? | Sectigo® Official</a></li>
<li><a href="https://www.ssl.com/article/what-are-root-certificates-and-why-do-they-matter/">What are Root Certificates , and Why Do They Matter? - SSL.com</a></li>

</ul>
</details>

**Tags**: `#PKI`, `#TLS`, `#Cloudflare`, `#Post-Quantum`, `#ACME`

---

<a id="item-5"></a>
## [Kimi K3 Lands in OpenAI Codex Enterprise Channel via Baseten](https://36kr.com/newsflashes/4005691489112198) ⭐️ 8.0/10

US AI infrastructure company Baseten announced that enterprise customers can now use Kimi K3 inside OpenAI&\#x27;s Codex coding tool, with usage charges billed directly against their existing OpenAI procurement commitments rather than requiring a new vendor onboarding and purchasing process. According to the report, this is the first time a Chinese open-source model has entered OpenAI&\#x27;s enterprise paid settlement channel. If accurate, this signals that enterprise AI procurement is becoming model-agnostic at the point of billing: buyers can route work to a Chinese open-weight model without opening a new vendor relationship, which lowers adoption friction considerably. It also suggests OpenAI&\#x27;s enterprise channel is willing to serve as a settlement layer for third-party models, a notable shift in how competing model ecosystems interoperate commercially. The arrangement reportedly runs through Baseten as the inference infrastructure provider rather than through a direct Kimi/OpenAI integration, and the key convenience is that cost accounting reuses existing OpenAI procurement commitments. Kimi K3 itself is described as a 2.8T-parameter open model with Kimi Delta Attention and Attention Residuals architectures, native vision support, and a 1M-token context window, aimed at long-horizon coding and knowledge work.

telegram · zaihuapd · Sep 30, 11:23

**Background**: Baseten is a US AI inference infrastructure company that helps organizations deploy and serve models in production; it recently raised a $300 million growth round at roughly a $5 billion post-money valuation and has been expanding into agent sandboxing via its acquisition of Blaxel. OpenAI Codex is OpenAI&\#x27;s coding tool for developers, and large enterprises often buy OpenAI capacity through committed-spend agreements, which function like pre-paid credit that must be used within a contract period. Kimi K3 is the latest flagship open model from China&\#x27;s Moonshot AI, whose Kimi series has gained traction internationally for coding and agentic tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.ai/zh-hans/ai-models/kimi-k3">Kimi K3：2.8T 开放模型，适合编程与知识工作</a></li>
<li><a href="https://www.baseten.co/">Inference Platform: Deploy AI models in production | Baseten</a></li>
<li><a href="https://finance.huanqiu.com/article/4TQj8f3mzIJ">中国开源模型首次进入 OpenAI 企 业 客户 采 购 体 系 | 环球网</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Kimi K3`, `#OpenAI Codex`, `#Enterprise AI`, `#China LLM`

---

<a id="item-6"></a>
## [Reddit to Kill RSS Feeds and Shut Down Public API](https://techcrunch.com/2026/09/30/reddit-is-killing-rss-feeds-ending-public-api-access-because-of-ai-bots/) ⭐️ 8.0/10

Reddit announced it will end RSS feed support on November 13, 2026, and shut down public API access in March 2027, citing large-scale scraping and automated abuse, particularly by AI bots. Third-party app and bot developers must register by January 12, 2027 or lose API access, and moderators are being steered toward Discord Relay as a replacement for feed-based workflows. This is a major tightening of public data access on one of the web&\#x27;s largest user-generated content platforms, following Reddit&\#x27;s earlier 2023 API pricing controversy. It directly affects third-party client developers, researchers, archivists, and AI/ML teams that rely on Reddit discussion data, and reinforces a broader trend of platforms restricting open access while monetizing data through licensing deals. RSS support ends on November 13, 2026, while the public API is slated to close in March 2027, giving developers a registration deadline of January 12, 2027. Notably, the API shutdown does not block commercial use outright — organizations wanting Reddit data for commercial purposes are expected to sign separate licensing agreements with the company.

telegram · zaihuapd · Oct 1, 00:27

**Background**: RSS \(Really Simple Syndication\) is a long-standing open format that lets websites publish updates in a machine-readable feed, so readers and tools can automatically follow new content without visiting each site. A public API is a documented interface that lets outside programs read platform data programmatically, which is how most third-party Reddit clients, research datasets and data pipelines have historically worked. Reddit already faced widespread backlash in 2023 when it introduced paid API pricing that forced several popular third-party apps to shut down.

<details><summary>References</summary>
<ul>
<li><a href="https://news.lavx.hu/zh-Hans/article/reddit-guan-bi-rss-ding-yue-yuan-she-ding-2027-nian-wei-gong-gong-api-guan-ting-de-zui-hou-qi-xian">Reddit 关闭 RSS 订阅源，设定 2027 年为公共 API 关停的最后期限 | L...</a></li>
<li><a href="https://www.digitaltoday.co.kr/cn/view/109373/reddit-to-end-rss-support-in-november-public-api-to-stop-in-march-2027">Reddit将于11月13日停止RSS支持 开放API拟于2027年3月关闭</a></li>
<li><a href="https://zh.wikipedia.org/zh-hans/RSS">RSS - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**Tags**: `#Reddit`, `#API deprecation`, `#RSS`, `#AI scraping`, `#platform policy`

---