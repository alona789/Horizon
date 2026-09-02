---
layout: default
title: "Horizon Summary: 2026-09-02 (EN)"
date: 2026-09-02
lang: en
---

> From 43 items, 8 important content pieces were selected

---

1. [Anthropic launches Claude Fable 5.1 and Mythos 5.1 with cheaper cache reads](#item-1) ⭐️ 9.0/10
2. [Google Play Forces AnkiDroid to Remove Open Collective Donation Link](#item-2) ⭐️ 8.0/10
3. [Small Transformer Trained in 1.5 Hours Outperforms Many LLMs on ARC](#item-3) ⭐️ 8.0/10
4. [Korea&\#x27;s Trillion-Dollar Sovereign AI Investment: Nvidia Wins, Hynix Loses](#item-4) ⭐️ 8.0/10
5. [TontaubeV1: Open-Weight 2.9B TTS Model for Long-Form Speech](#item-5) ⭐️ 8.0/10
6. [EvoUndo Framework Enables Recoverability for Self-Evolving LLM Agents](#item-6) ⭐️ 8.0/10
7. [Virtualizor Update Infrastructure Hit by BGP Hijacking, Root Backdoor Delivered](#item-7) ⭐️ 8.0/10
8. [Google Gemini 3.8 Flash reportedly narrows AI coding gap with rivals](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic launches Claude Fable 5.1 and Mythos 5.1 with cheaper cache reads](https://www.anthropic.com/claude-fable-and-mythos-5-1) ⭐️ 9.0/10

Anthropic announced Claude Fable 5.1 and Claude Mythos 5.1, the latest models in its Claude family. The release brings improved writing style, new reasoning capabilities, and a 75% reduction in cache read pricing \(from $1 per million tokens to $0.25\). This release represents a major update to Anthropic&\#x27;s most capable model line, directly impacting developers and enterprises building long-running agentic applications. The substantial cache-read price cut makes high-volume usage significantly cheaper, and the improvements are likely to intensify competition among LLM providers. Claude Fable 5.1 keeps the same input and output prices as Fable 5, with cache reads priced at a quarter of the previous rate. It is optimized for jobs that span hours and multiple applications, including Cowork, Slack via Claude Tag \(beta\), browser automation, and unattended managed agents; Mythos 5.1 adds cybersecurity and biology gains.

hackernews · denysvitali · Sep 1, 17:53 · [Discussion](https://news.ycombinator.com/item?id=49525378)

**Background**: Claude Fable 5 and Claude Mythos 5 were released in June 2026 as &\#x27;Mythos-class&\#x27; models sharing the same underlying technology, differing mainly in safeguards. Fable is the publicly available version with additional safety filters, while Mythos is a restricted-access version with fewer restrictions in areas like cybersecurity and biology. Earlier, Anthropic kept the original Mythos Preview private due to concerns about software vulnerability discovery. The Fable 5.1 update extends this line with stronger agentic coding and research capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://platform.claude.com/docs/en/models/fable-5-1/whats-new-fable-5-1">What&#x27;s new in Claude Fable 5.1 - Claude Platform Docs</a></li>

</ul>
</details>

**Discussion**: Community reactions are largely positive. An Anthropic employee highlighted a marked improvement in writing style, describing it as less stereotypically &\#x27;Claude&\#x27; and more responsive to style instructions. Users testing reasoning effort levels reported strong outputs, though one developer noted that on complex asynchronous workloads the model sometimes describes actions rather than executing them and needs a nudge to finish; another commenter observed that the cache-read price cut suggests Anthropic saw weak adoption at the original pricing and that benchmark gains appear modest outside terminal-Bench-Science.

**Tags**: `#AI`, `#Anthropic`, `#LLM`, `#Machine Learning`, `#Claude`

---

<a id="item-2"></a>
## [Google Play Forces AnkiDroid to Remove Open Collective Donation Link](https://github.com/ankidroid/Anki-Android/issues/21656) ⭐️ 8.0/10

Google Play has told AnkiDroid to remove its Open Collective donation link from the Android app, citing Play billing policy. The maintainers logged the dispute as issue \#21656, which has drawn nearly 245 comments from developers and users. This is a high-profile example of app-store policy affecting how open-source projects fund themselves, since many FOSS apps rely on donations rather than in-app purchases. It reignites concerns about Google Play&\#x27;s market power and the consistency of its enforcement, affecting Android developers and maintainers broadly. The dispute centers on tax status: Open Collective is a 501\(c\)\(6\) nonprofit, so donations to hosted projects such as AnkiDroid are not tax-deductible for donors, which may not satisfy Google&\#x27;s &\#x27;tax-exempt donations&\#x27; exemption language. Participants also noted that Google previously ejected WireGuard from the Play Store in 2019 over a similar donation-policy issue.

hackernews · hexa555 · Sep 1, 10:11 · [Discussion](https://news.ycombinator.com/item?id=49520022)

**Background**: AnkiDroid is the Android client for Anki, a popular free and open-source flashcard app that uses spaced repetition to help users memorize information. Open Collective is a crowdfunding and financial management platform designed for open-source projects, offering fiscal hosting rather than requiring a separate legal entity. Google Play&\#x27;s developer policies restrict how apps collect payments for digital content, and donations are generally allowed only when they provide no in-app benefit; this framework has become a recurring point of tension for donation-funded open-source apps.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AnkiDroid">AnkiDroid</a></li>
<li><a href="https://en.wikipedia.org/wiki/Open_Collective">Open Collective</a></li>
<li><a href="https://support.google.com/googleplay/android-developer/thread/288305302/how-to-handle-donations?hl=en">How to handle donations? - Google Play Developer Community</a></li>

</ul>
</details>

**Discussion**: Commenters were frustrated by Google&\#x27;s control, with one citing the 2019 WireGuard removal as evidence that app-store monopolies can capriciously deny distribution. Others discussed the legal nuances of 501\(c\)\(6\) status versus tax-deductible donations, while some users thanked the team and said the link reminded them to donate. A few suggested that progressive web apps could circumvent store restrictions if Apple made them more visible.

**Tags**: `#open source`, `#app store policy`, `#donations`, `#google play`, `#android`

---

<a id="item-3"></a>
## [Small Transformer Trained in 1.5 Hours Outperforms Many LLMs on ARC](https://mvakde.github.io/blog/44-on-arc-1/) ⭐️ 8.0/10

The author trained a small autoregressive transformer from scratch in just 1.5 hours and showed it beats many large language models on the ARC benchmark. This result challenges the common assumption that massive scale and training compute are necessary for strong reasoning performance. This demonstrates that efficient, task-specific models can rival or surpass much larger general-purpose LLMs on challenging benchmarks like ARC. It could push the field toward more compute-efficient approaches and prompt rethinking of the scale-centric paradigm in AI research. The model is not an LLM but a small autoregressive transformer, and major score gains came from modern architecture choices like SwiGLU and RMSNorm, better data diversity and shuffling, and scaling up to 8 layers. The author defends training on the evaluation puzzles by clarifying that the labels of test data were never used, and that ARC is a metalearning benchmark where learning from the puzzles is intended.

hackernews · porridgeraisin · Sep 1, 09:52 · [Discussion](https://news.ycombinator.com/item?id=49519939)

**Background**: The Abstraction and Reasoning Corpus \(ARC\) is a benchmark designed to measure general intelligence through visual reasoning puzzles, often used to evaluate large language models. Large language models are typically transformer-based neural networks trained on vast amounts of text, but they often require enormous compute and still struggle on ARC. This work explores an alternative: a small, task-specific transformer trained quickly with a carefully designed recipe.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_benchmarks">AI benchmarks</a></li>
<li><a href="https://arcprize.org/">ARC Prize</a></li>
<li><a href="https://deepgram.com/learn/arc-llm-benchmark-guide">ARC Benchmark Guide for Evaluating LLMs | Deepgram</a></li>

</ul>
</details>

**Discussion**: The author engaged in the discussion, clarifying that the model is not an LLM and that training on eval puzzles is not equivalent to training on test labels. Some commenters acknowledged the impressive results but suggested that architecture tweaks might be a &\#x27;last resort&\#x27; rather than a fundamental breakthrough, while others praised the novelty and efficiency. A few also noted the author&\#x27;s personal story mentioned on their homepage.

**Tags**: `#transformer`, `#ARC`, `#LLM`, `#efficiency`, `#benchmark`

---

<a id="item-4"></a>
## [Korea&\#x27;s Trillion-Dollar Sovereign AI Investment: Nvidia Wins, Hynix Loses](https://newsletter.semianalysis.com/p/koreas-trillion-dollar-sovereign) ⭐️ 8.0/10

Korea has launched a trillion-dollar sovereign AI initiative structured as a national AI tournament, dubbed &\#x27;Squid Games&\#x27;, to develop a Korean-controlled open-source model. According to the analysis, Nvidia emerges as the main winner while SK Hynix is disadvantaged. This investment redefines Korea&\#x27;s AI chip market, strengthening Nvidia&\#x27;s CUDA-based ecosystem and potentially eroding demand for SK Hynix&\#x27;s memory products in AI servers. It also influences the global race for non-Chinese open-source AI models. The project&\#x27;s goal is to produce an open-source model that Korean organizations can train, modify, and operate without relying on foreign AI labs. Nvidia&\#x27;s dependence on open-source models is cited as a reason for its alignment with the tournament, while Hynix and Samsung face uncertain implications in memory supply.

rss · Semianalysis · Sep 1, 20:14

**Background**: Sovereign AI refers to a country&\#x27;s ability to build, run, and govern AI using its own infrastructure, data, and rules, rather than depending on foreign providers. Korea&\#x27;s Ministry of Science and ICT has been promoting nationwide AI adoption and competitions. The national AI tournament is part of a larger trillion-dollar investment to secure AI independence and competitiveness.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/koreas-trillion-dollar-sovereign">Korea’s Trillion-Dollar Sovereign AI Investment: Nvidia Wins, Hynix Loses</a></li>
<li><a href="https://www.mckinsey.com/featured-insights/mckinsey-explainers/what-is-sovereign-ai">What is sovereign AI? | McKinsey</a></li>
<li><a href="https://en.sedaily.com/news/2026/03/26/korea-launches-nationwide-ai-competition-for-all-ages">Korea Launches Nationwide AI Competition for All Ages - Seoul Economic Daily</a></li>

</ul>
</details>

**Tags**: `#sovereign AI`, `#semiconductors`, `#Nvidia`, `#Hynix`, `#AI investment`

---

<a id="item-5"></a>
## [TontaubeV1: Open-Weight 2.9B TTS Model for Long-Form Speech](https://www.reddit.com/r/MachineLearning/comments/1w4afjn/we_released_tontaubev1_a_characterlevel_tts_model/) ⭐️ 8.0/10

A brother duo released TontaubeV1, a 2.9B-parameter open-weight TTS model for expressive, long-form speech synthesis. It builds on the DualCodec audio codec and supports zero-shot voice cloning from up to one minute of reference audio. This release provides the ML community with a large, open-weight TTS model that offers low-latency local inference and zero-shot voice cloning. Its character-level tokenization approach offers a less common but effective alternative to BPE tokenizers in LLM-based TTS, potentially inspiring further research. The model was trained on 7 languages and about 200k hours of audio, with primary focus on English and German. Technically, it uses character-level tokenization, a custom chunking and position scheme, and DualCodec&\#x27;s multi-codebook discrete audio tokens; the authors report that character-level tokenization outperformed Qwen&\#x27;s original BPE tokenizer for TTS tasks.

reddit · r/MachineLearning · /u/EAVDR · Sep 1, 12:23

**Background**: Text-to-speech \(TTS\) models generate spoken audio from written text. Many modern TTS systems are LLM-based and use a tokenizer to convert text into IDs, then predict audio tokens from a codec. Character-level tokenization splits text into individual characters, which can simplify text-to-sound mapping but usually increases sequence length. Audio codecs like DualCodec compress audio into discrete tokens that a language model can predict, with DualCodec using low frame rates \(25Hz and 12.5Hz\) and larger codebooks for efficient speech synthesis. Zero-shot voice cloning allows a model to mimic a new speaker&\#x27;s voice from a short reference sample.

<details><summary>References</summary>
<ul>
<li><a href="https://dualcodec.github.io/">DualCodec Demo Page</a></li>
<li><a href="https://arxiv.org/abs/2505.13000">[2505.13000] DualCodec: A Low-Frame-Rate, Semantically-Enhanced Neural Audio Codec for Speech Generation</a></li>
<li><a href="https://www.geeksforgeeks.org/nlp/nlp-how-tokenizing-text-sentence-words-works/">Tokenization in NLP - GeeksforGeeks</a></li>

</ul>
</details>

**Tags**: `#TTS`, `#speech synthesis`, `#open-source`, `#machine learning`, `#audio`

---

<a id="item-6"></a>
## [EvoUndo Framework Enables Recoverability for Self-Evolving LLM Agents](https://www.reddit.com/r/MachineLearning/comments/1w4m0hq/evoundo_recoverabilityconstrained_selfevolution/) ⭐️ 8.0/10

The paper introduces EvoUndo, a framework for representing, synthesizing, diagnosing, and verifying recoverability of model-generated self-modifications in LLM agents across counterfactual states. The framework improves recovery from 0/197 with conventional repair to 191/197 with an extended recovery calculus on 600 unseen one-shot tasks. This addresses the critical safety problem of persistent, unrecoverable changes in self-evolving LLM agents, which is essential for reliable deployment. The results show that recoverability must be co-designed with verification, grounding, and recovery-language expressivity, not handled by iterative prompting alone. On the gpt-oss-120b backbone, adding exact-address diagnostics to the richer language reduces recovery from 142/143 to 133/143, a negative interaction not reproduced with Qwen3.8-27B, indicating model-dependent effects. The study identifies 197 capability-improving mutations that fail recoverability verification across 600 unseen one-shot tasks.

reddit · r/MachineLearning · /u/AccomplishedLeg1508 · Sep 1, 19:17

**Background**: LLM agents increasingly modify their own prompts, tools, middleware, resources, and execution harnesses at runtime, a process known as self-evolution. A successful mutation may leave persistent effects that cannot be safely reversed in states different from the one in which it was created; counterfactual states are alternative states used to test whether recovery works across varied conditions. EvoUndo builds on formal verification and typed effect systems to synthesize and independently verify recovery procedures.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2608.28363">[2608.28363] EvoUndo: Recoverability-Constrained Self -Evolution for...</a></li>
<li><a href="https://arxiv.org/html/2608.28363v1">EvoUndo: Recoverability-ConstrainedSelf-Evolution for LLM ...</a></li>
<li><a href="https://lilys.ai/en/notes/daily-papers-20260831/evoundo-llm-agent-recoverable-self-evolution">EvoUndo: Self-Evolution with Recoverability Constraints for ...</a></li>

</ul>
</details>

**Tags**: `#LLM agents`, `#self-evolution`, `#recoverability`, `#AI safety`, `#machine learning`

---

<a id="item-7"></a>
## [Virtualizor Update Infrastructure Hit by BGP Hijacking, Root Backdoor Delivered](https://www.virtualizor.com/blog/security-incident-bgp-hijacking/) ⭐️ 8.0/10

Virtualizor&\#x27;s update infrastructure was compromised via a BGP hijacking from August 28 to 30, 2026, allowing attackers to push malicious update packages signed with valid TLS certificates. The company confirmed that only a small number of installations that updated during that window were affected. This is a significant supply chain security incident because it demonstrates how BGP hijacking can bypass trust in update channels, even with valid TLS certificates. It underscores the risk to hosting providers and control-panel users who rely on automatic updates for security. Independent forensics found that the malicious package wrote a root SSH key, installed a Java payload, and set up persistent services. AlbaHost detected indicators on 5 of 34 hypervisors, and Softaculous stated there is currently no evidence that other products were affected.

telegram · zaihuapd · Sep 1, 06:05

**Background**: BGP \(Border Gateway Protocol\) is the routing protocol that directs traffic across the internet; BGP hijacking occurs when an attacker corrupts routing tables to intercept traffic meant for specific IP prefixes. Virtualizor is a popular web-based VPS control panel used by hosting providers to deploy and manage virtual servers. Because update servers are trusted, a hijack can trick clients into accepting malware as a legitimate patch.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/BGP_hijacking">BGP hijacking</a></li>
<li><a href="https://www.cloudflare.com/learning/security/glossary/bgp-hijacking/">What Is BGP Hijacking ?</a></li>
<li><a href="https://www.virtualizor.com/">Virtualizor – Cloud Control Panel</a></li>

</ul>
</details>

**Tags**: `#security`, `#bgp hijacking`, `#supply chain`, `#rootkit`, `#virtualizor`

---

<a id="item-8"></a>
## [Google Gemini 3.8 Flash reportedly narrows AI coding gap with rivals](https://www.wsj.com/tech/ai/new-google-ai-model-said-to-narrow-gap-on-coding-ability-264c6052) ⭐️ 8.0/10

Google DeepMind is reportedly set to release Gemini 3.8 Flash, internal codename Skimaki, as soon as this Wednesday. The model&\#x27;s coding abilities improved significantly, and in internal comparisons using Google&\#x27;s Jetski programming tool, engineers reportedly preferred it over Anthropic&\#x27;s Opus model. If confirmed, this would help Google close a widely perceived gap in coding-focused AI models behind OpenAI and Anthropic. The move could reshape competition in AI-assisted software development, where model coding quality is a key battleground. The report comes from The Wall Street Journal, citing people familiar with the matter, and has not been publicly confirmed by Google. The internal evaluation reportedly took place in Google&\#x27;s Jetski coding tool, where the new Flash model was compared against Anthropic&\#x27;s Opus model.

telegram · zaihuapd · Sep 2, 00:35

**Background**: Gemini Flash is Google&\#x27;s family of fast, cost-efficient AI models, typically used for high-volume, low-latency tasks and agentic workflows. Anthropic&\#x27;s Opus models are positioned as its most powerful AI models, often setting high marks in coding and complex reasoning benchmarks. This reported release continues an industry trend in which major labs rapidly iterate on models specifically tuned for software engineering.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/models/model-cards/gemini-3-7-flash/">Gemini 3.7 Flash - Model Card — Google DeepMind</a></li>
<li><a href="https://ai.google.dev/gemini-api/docs/models">Models - Gemini API | Google AI for Developers</a></li>
<li><a href="https://www.anthropic.com/news/claude-opus-4-8">Introducing Claude Opus 4.8 \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Google`, `#Gemini`, `#coding`, `#model release`

---