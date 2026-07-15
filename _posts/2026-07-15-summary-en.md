---
layout: default
title: "Horizon Summary: 2026-07-15 (EN)"
date: 2026-07-15
lang: en
---

> From 45 items, 14 important content pieces were selected

---

1. [RL Post-Training on 14 Macs Across 4 Countries](#item-1) ⭐️ 9.0/10
2. [Inkling: Largest Open-Weight Multimodal Model with Audio](#item-2) ⭐️ 8.0/10
3. [Stripe and Advent Jointly Offer to Acquire PayPal](#item-3) ⭐️ 8.0/10
4. [EU court invalidates OpenAI trademark as descriptive](#item-4) ⭐️ 8.0/10
5. [Claude web_fetch Bypass Exfiltrates Private User Data](#item-5) ⭐️ 8.0/10
6. [Linus Torvalds defends AI use in Linux, warns against hostility](#item-6) ⭐️ 8.0/10
7. [German AI consortium releases open 30B model Soofi S](#item-7) ⭐️ 8.0/10
8. [Inkling Model Becomes Top US Open Weight Model](#item-8) ⭐️ 8.0/10
9. [DeepSeek Prepares IPO, Seeks $71B+ Valuation Funding](#item-9) ⭐️ 8.0/10
10. [Judge questions Epic-Google $800M deal may undermine antitrust stance](#item-10) ⭐️ 8.0/10
11. [DeepSeek raises over 50B yuan in first funding round](#item-11) ⭐️ 8.0/10
12. [Musk: X to Open Source All Code, Submit to Third-Party Review](#item-12) ⭐️ 8.0/10
13. [Sandbox Escape in iOS 27 Beta Lets Filza Read Notes Database](#item-13) ⭐️ 8.0/10
14. [ASML Plans Price Hikes; TSMC Resists, Chinese Firms Accept 10% DUV Increase](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [RL Post-Training on 14 Macs Across 4 Countries](https://www.reddit.com/r/LocalLLaMA/comments/1uxb3zn/rl_posttraining_on_14_macs_across_4_countries/) ⭐️ 9.0/10

Pluralis Research conducted the first RL post-training run where all rollouts were generated on 14 consumer Macs across 4 countries using int8 inference with MLX, while gradient updates were performed on a remote B200 via the open internet. This demonstrates that distributed RL post-training is feasible without datacenter interconnects, potentially lowering the barrier for agentic RL compute by leveraging idle consumer hardware. The off-policy gap was controlled using PULSE to send int8 weight deltas (only ~0.5% change per version, ~82 MB instead of 9 GB) and a DPPO-style probability gate to discard tokens with drifted probabilities. The system achieved a cover pass@1 increase from 29% to 63% on PaperSearchQA.

reddit · r/LocalLLaMA · /u/erfan_mhi · Jul 15, 16:36

**Background**: Reinforcement learning post-training fine-tunes a model using RL after initial pretraining. Rollout generation in agentic RL is compute-intensive, typically requiring expensive datacenter GPUs. MLX is an open-source array framework for machine learning on Apple Silicon. The off-policy gap arises when the model generating rollouts has stale weights compared to the trainer model. PULSE efficiently communicates only the changed parameters between quantized model versions.

<details><summary>References</summary>
<ul>
<li><a href="https://mlx-framework.org/">MLX framework</a></li>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple silicon · GitHub</a></li>

</ul>
</details>

**Tags**: `#RL`, `#post-training`, `#distributed computing`, `#MLX`, `#Mac`

---

<a id="item-2"></a>
## [Inkling: Largest Open-Weight Multimodal Model with Audio](https://thinkingmachines.ai/news/introducing-inkling/) ⭐️ 8.0/10

Thinking Machines released Inkling, an open-weights multimodal model claimed to be the largest of its kind supporting audio, with strong audio capabilities and efficient reasoning. This release fills a gap for open-weights multimodal models with strong audio, enabling enterprise customization and local deployment, and could accelerate AI adoption in audio-focused applications. Inkling is available for fine-tuning on Tinker platform and supports long context. Early community benchmarks suggest it may outperform some competitors in audio tasks, though not the strongest overall.

hackernews · vimarsh6739 · Jul 15, 18:12 · [Discussion](https://news.ycombinator.com/item?id=48924912)

**Background**: Open-weights models release trained parameters publicly, allowing anyone to download and modify them. Multimodal models process multiple data types like text, audio, and images. Inkling combines these, emphasizing audio.

<details><summary>References</summary>
<ul>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>
<li><a href="https://en.wikipedia.org/wiki/Multimodal_model">Multimodal model</a></li>

</ul>
</details>

**Discussion**: Community members expressed excitement about Inkling's audio capabilities and open nature, with some noting it could be a strong base for agentic applications. Others compared it to Chinese open models and speculated on its strategic importance for American AI labs.

**Tags**: `#open-weights`, `#multimodal`, `#AI`, `#audio`, `#fine-tuning`

---

<a id="item-3"></a>
## [Stripe and Advent Jointly Offer to Acquire PayPal](https://www.reuters.com/business/finance/stripe-advent-offer-buy-paypal-more-than-53-billion-sources-say-2026-07-15/) ⭐️ 8.0/10

Stripe, a leading payment processor, and Advent International, a private equity firm, have made a joint offer to acquire PayPal for more than $53 billion, according to sources. This acquisition, if completed, would consolidate major fintech players and could significantly reshape the online payment landscape, raising antitrust concerns and affecting millions of merchants and consumers. The offer values PayPal at over $53 billion, and the deal would bring together Stripe, PayPal, Venmo, Braintree, and Xoom under one umbrella, potentially creating a highly concentrated market for card-not-present transactions.

hackernews · rvz · Jul 15, 03:32 · [Discussion](https://news.ycombinator.com/item?id=48915953)

**Background**: Stripe is a major online payment processor known for its developer-friendly API, while PayPal is a pioneering digital payments platform with brands like Venmo and Braintree. Advent International is a global private equity firm. Antitrust regulators are likely to scrutinize the deal due to the combined market share in online payments.

**Discussion**: Community comments express strong concerns about the acquisition, citing potential antitrust issues, higher fees, and Stripe's restrictive policies on certain industries like cannabis and adult content. Users worry that consolidation reduces competition and puts their businesses at risk.

**Tags**: `#fintech`, `#acquisition`, `#paypal`, `#stripe`, `#antitrust`

---

<a id="item-4"></a>
## [EU court invalidates OpenAI trademark as descriptive](https://dpa-international.com/economics/urn:newsml:dpa.com:20090101:260715-930-389143/) ⭐️ 8.0/10

The EU General Court ruled that OpenAI's trademark 'OPENAI' is invalid for software and IT services because the term is descriptive, combining 'open' meaning freely accessible with 'AI' as artificial intelligence. This ruling highlights the stricter distinctiveness requirements in the EU trademark system compared to the US, affecting major AI companies and potentially impacting brand protection strategies. The court found that 'OPENAI' is purely descriptive for certain software and information technology goods and services, lacking acquired distinctiveness through use in the EU.

hackernews · hermanzegerman · Jul 15, 14:32 · [Discussion](https://news.ycombinator.com/item?id=48921461)

**Background**: In trademark law, a descriptive mark directly describes a characteristic of the goods or services, making it difficult to register unless it acquires distinctiveness through extensive use. The EU system requires a mark to be inherently distinctive from the start, while the US allows registration of descriptive marks that have gained secondary meaning.

<details><summary>References</summary>
<ul>
<li><a href="https://www.justia.com/intellectual-property/trademarks/strength-of-marks/descriptive-marks/">Descriptive Trademarks and Service Marks & Their Potential Legal Protection | Intellectual Property Law Center | Justia</a></li>
<li><a href="https://www.inta.org/wp-content/uploads/public-files/resources/the-trademark-reporter/vol109_no3_a1_porangaba.pdf">Acquired Distinctiveness in the European Union</a></li>

</ul>
</details>

**Discussion**: Commenters noted the contrast between EU and US trademark systems, with some praising the court's sensible questioning of the term 'open' being hijacked. Others pointed out that the ruling aligns with prior cases where descriptive marks were rejected.

**Tags**: `#trademark`, `#AI`, `#OpenAI`, `#EU law`, `#open source`

---

<a id="item-5"></a>
## [Claude web_fetch Bypass Exfiltrates Private User Data](https://simonwillison.net/2026/Jul/15/claude-web-fetch-exfiltration/#atom-everything) ⭐️ 8.0/10

Security researcher Ayush Paul demonstrated a prompt injection attack that bypassed Anthropic's protections for the Claude web_fetch tool, tricking it into exfiltrating private user memories such as name, location, and employer. This vulnerability highlights the ongoing challenge of securing AI agents that combine private data, untrusted content, and external communication—the 'lethal trifecta'—and underscores the risk of data exfiltration in widely used AI chatbots. The attack exploited a loophole where web_fetch could follow URLs embedded in previously fetched pages; by creating a honeypot site that presented a fake authentication prompt, the attacker got Claude to navigate through letters to exfiltrate data.

rss · Simon Willison · Jul 15, 14:21

**Background**: The 'lethal trifecta' refers to a dangerous combination in AI agents: access to private data, ability to process untrusted content, and capability to send external communications. Claude's web_fetch tool was designed with protections to prevent data exfiltration by restricting URL navigation to user-entered or search-result URLs only.

<details><summary>References</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/agents-and-tools/tool-use/web-fetch-tool">Web fetch tool - Claude Platform Docs</a></li>
<li><a href="https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/">The lethal trifecta for AI agents: private data, untrusted content, and external communication</a></li>

</ul>
</details>

**Discussion**: On Hacker News, the discussion likely focused on the severity of the attack and the adequacy of Anthropic's response—paying no bounty because they claimed prior internal discovery. Some may have debated the broader implications for AI agent security.

**Tags**: `#AI security`, `#prompt injection`, `#data exfiltration`, `#Claude`, `#Anthropic`

---

<a id="item-6"></a>
## [Linus Torvalds defends AI use in Linux, warns against hostility](https://www.reddit.com/r/LocalLLaMA/comments/1uxbrw4/linus_torvalds_tells_people_to_stop_attacking/) ⭐️ 8.0/10

Linus Torvalds, the creator of Linux, publicly stated that AI is a useful tool and warned the community against attacking others for using AI, asserting that the Linux kernel project is not anti-AI and will continue to focus on technical merit. Torvalds' endorsement carries significant weight in the open-source community, potentially shaping the culture of Linux and other projects to be more accepting of AI tools, which could accelerate AI adoption in software development. Torvalds emphasized that AI, while imperfect, is no longer questionable in usefulness, and that the kernel community makes decisions based on technical merit, not fear of new tools. He also warned that those who disagree can fork the project or leave.

reddit · r/LocalLLaMA · /u/Illustrious_Car344 · Jul 15, 16:59

**Background**: Linus Torvalds is the original creator and long-time lead maintainer of the Linux kernel, one of the largest open-source projects in the world. AI tools, especially large language models (LLMs), have become increasingly used in code generation, review, and bug detection, sparking debate about their impact on code quality and maintainer workload.

**Tags**: `#AI`, `#Linux`, `#Open Source`, `#Linus Torvalds`, `#Community Debate`

---

<a id="item-7"></a>
## [German AI consortium releases open 30B model Soofi S](https://www.reddit.com/r/LocalLLaMA/comments/1uxao7y/german_ai_consortium_releases_soofi_s_an_open_30b/) ⭐️ 8.0/10

The German AI consortium 'Soofi Project' has released Soofi S, an open-source 30B parameter (30B-A3B) foundation model that achieves state-of-the-art performance on benchmarks in both English and German. This release is significant because it demonstrates the ability to build a sovereign, open-source multilingual model using European infrastructure, reducing reliance on US-based AI providers and promoting AI sovereignty. Soofi S is a 30B parameter model with 3B active parameters, trained entirely on the German Industrial AI Cloud operated by Deutsche Telekom in Munich, and is available on Hugging Face under an open license.

reddit · r/LocalLLaMA · /u/yogthos · Jul 15, 16:21

**Background**: Foundation models like GPT-4 or Llama are typically developed by US companies on massive compute clusters. The Soofi Project aims to create a sovereign European alternative, focusing on German and English languages, using EU-based infrastructure. Soofi S is their first major release.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/Soofi-Project/Soofi-S-Base">Soofi-Project/Soofi-S-Base - Hugging Face</a></li>
<li><a href="https://arxiv.org/abs/2607.09424">[2607.09424] A Sovereign, Open-Source Foundation Model for German and English - arXiv</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#LLM`, `#AI`, `#multilingual`, `#benchmarks`

---

<a id="item-8"></a>
## [Inkling Model Becomes Top US Open Weight Model](https://www.reddit.com/r/LocalLLaMA/comments/1uxhpws/inkling_by_thinking_machines_is_the_1_us_open/) ⭐️ 8.0/10

Thinking Machines Lab released Inkling, a 975B total parameter Mixture-of-Experts model, which now ranks as the top US open weight model and fifth globally among open weight models. This marks a significant step for US open weight models in catching up with leading Chinese models, highlighting the competitiveness of open source AI development. Inkling uses a Mixture-of-Experts architecture with 975B total and 41B active parameters, and it surpasses NVIDIA's Nemotron 3 Ultra (550B total, 55B active) on benchmarks.

reddit · r/LocalLLaMA · /u/davidthesong · Jul 15, 20:40

**Background**: Open weight models are AI models whose trained parameters are publicly released, allowing anyone to download and fine-tune them. They differ from fully open source models as they may come with usage restrictions. This release is part of an ongoing competitive landscape where US and Chinese companies vie for leadership in AI, with Chinese models like DeepSeek previously topping charts.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our open-weights model - Thinking Machines Lab</a></li>
<li><a href="https://thinkingmachines.ai/inkling/">Inkling - Thinking Machines Lab</a></li>
<li><a href="https://techcrunch.com/2026/07/15/thinking-machines-amps-up-its-bet-against-one-size-fits-all-ai-with-its-first-open-model-inkling/">Thinking Machines amps up its bet against one-size-fits-all AI with its first open model, Inkling | TechCrunch</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**Tags**: `#open weight models`, `#LLM`, `#AI competition`, `#NLP`, `#model benchmark`

---

<a id="item-9"></a>
## [DeepSeek Prepares IPO, Seeks $71B+ Valuation Funding](https://t.me/zaihuapd/42577) ⭐️ 8.0/10

DeepSeek has initiated IPO preparations and plans to file by end of 2025 or early 2026, targeting a 2027 listing, while simultaneously seeking a new private funding round at a pre-money valuation of at least ¥480 billion (about $71 billion). This significant valuation jump from $50 billion in June 2025 demonstrates strong market confidence in DeepSeek's AI capabilities, and the IPO would be one of the largest for an AI startup in China, impacting the global AI investment landscape. DeepSeek completed its first external funding round in early June 2025, raising $700 million from investors including Tencent and CATL, and now targets at least ¥10 billion in the new round, with the final amount potentially multiplying based on investor participation.

telegram · zaihuapd · Jul 15, 07:04

**Background**: DeepSeek is a leading Chinese AI startup known for its large language models. The company was valued at around $50 billion in its first external round in June 2025. The new valuation of $71 billion reflects rapid growth expectations in the competitive AI sector. Founder Liang Wenfeng's wealth has reportedly surged.

**Tags**: `#DeepSeek`, `#AI`, `#funding`, `#IPO`, `#valuation`

---

<a id="item-10"></a>
## [Judge questions Epic-Google $800M deal may undermine antitrust stance](https://t.me/zaihuapd/42588) ⭐️ 8.0/10

In a recent hearing, U.S. District Judge James Donato disclosed that Epic Games and Google have entered a new commercial partnership involving joint product development, marketing, and partnerships, with Epic paying Google approximately $800 million over six years. The judge expressed concern that this deal could conflict with Epic's push for antitrust reforms in the Android ecosystem. This development could weaken Epic's credibility in its antitrust battle against Google, potentially reducing the likelihood of meaningful reforms to Android's app distribution and payment systems. It also raises broader questions about the alignment of interests between major platform holders and their critics. The deal covers Unreal Engine, Fortnite, and Android-related businesses, and includes a payment of roughly $800 million from Epic to Google over six years. Epic CEO Tim Sweeney stated that the agreement does not include terms for Epic Games Store on Android, but the judge questioned whether the commercial relationship undermines Epic's antitrust positions.

telegram · zaihuapd · Jul 15, 11:15

**Background**: Epic Games sued Google in 2020, alleging that Google's control over the Android app market through Google Play and its billing system constituted an illegal monopoly. The trial concluded in December 2023 with a jury finding Google liable for antitrust violations, and remedies were being negotiated. The newly disclosed commercial deal emerged during remedy hearings, raising concerns about conflicts of interest.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Unreal_Engine">Unreal Engine</a></li>

</ul>
</details>

**Tags**: `#antitrust`, `#epic games`, `#google`, `#android`, `#mobile ecosystem`

---

<a id="item-11"></a>
## [DeepSeek raises over 50B yuan in first funding round](https://t.me/zaihuapd/42589) ⭐️ 8.0/10

DeepSeek completed its first funding round, raising over 500 billion yuan (approximately 74 billion USD), and reached a valuation exceeding 500 billion yuan. The financing adopted an unconventional limited partnership structure where investors contribute to a fund managed by CEO Liang Wenfeng, subject to a five-year lock-up period and no voting rights. This massive funding round signals strong investor confidence in DeepSeek and the Chinese AI industry, especially given the unique governance structure that preserves founder control. The involvement of major corporates like Tencent and CATL highlights the strategic importance of AI in China. The funding round uses a limited partnership structure that separates capital from control, with founder Liang Wenfeng personally investing 20 billion yuan. Tencent is considering investing 10 billion yuan, while CATL plans to invest 5 billion yuan, making them the largest external investors.

telegram · zaihuapd · Jul 15, 12:56

**Background**: A limited partnership structure splits the role of partners into general partners (GP) and limited partners (LP). In this model, the GP (here, CEO Liang Wenfeng) manages the fund and retains control, while LPs provide capital but have limited decision-making power. This structure is often used by startups to raise capital without diluting founder control.

<details><summary>References</summary>
<ul>
<li><a href="https://cj.sina.com.cn/articles/view/1887344341/707e96d502001rse4">有限合伙、五年 锁 定 期 、 无 投票 权 ？传DeepSeek已完成500亿元 融 资</a></li>
<li><a href="https://www.163.com/dy/article/KOV0N13E0556KOZH.html">163.com/dy/article/KOV0N13E0556KOZH.html</a></li>
<li><a href="https://m.gelonghui.com/p/5264691">DeepSeek 融 资 500亿：量化大佬梁文锋的反 资 本实验</a></li>

</ul>
</details>

**Tags**: `#AI`, `#funding`, `#DeepSeek`, `#corporate governance`, `#startup`

---

<a id="item-12"></a>
## [Musk: X to Open Source All Code, Submit to Third-Party Review](https://x.com/elonmusk/status/2077361679034118271) ⭐️ 8.0/10

Elon Musk announced that after a security audit, X (formerly Twitter) will unconditionally open source its entire codebase and invite third-party reviewers to verify that the running system matches the open source code. This move could significantly enhance transparency and trust in X's software, setting a new precedent for major social platforms. It may pressure other companies to adopt similar openness, benefiting the broader open source community and user privacy advocates. The announcement specified that the open sourcing will occur after a security vulnerability review, and third-party reviewers will check the production system for consistency. Musk emphasized that trust from complete transparency is the only trust worth having.

telegram · zaihuapd · Jul 15, 13:32

**Background**: X (formerly Twitter) is a major social media platform. Open sourcing typically involves releasing source code under an open source license, allowing public inspection and contribution. Third-party review adds a layer of verification that the released code matches what actually runs on servers, addressing concerns about surveillance or manipulation.

**Tags**: `#open source`, `#Twitter`, `#transparency`, `#software engineering`

---

<a id="item-13"></a>
## [Sandbox Escape in iOS 27 Beta Lets Filza Read Notes Database](https://x.com/0xjohnny/status/2077216973256274272) ⭐️ 8.0/10

Developer Johnnys modified the Filza file manager to exploit a sandbox escape vulnerability in iOS 27 beta 3, allowing it to access the Notes database on an iPhone 17 Pro Max. This demonstration highlights a critical security flaw in the latest iOS beta, potentially impacting users' privacy and data security. It also shows ongoing cat-and-mouse game between jailbreak community and Apple's security measures. The exploit specifically bypasses the app container sandbox on iOS 27 beta 3, allowing the modified Filza to browse external data including sensitive system databases. The vulnerability has not been assigned a CVE yet.

telegram · zaihuapd · Jul 15, 14:35

**Background**: iOS sandboxing restricts each app to its own container, preventing access to other apps' data and system files. A sandbox escape vulnerability allows an app to break out of this containment, often through kernel vulnerabilities or misconfigured entitlements. Filza is a popular file manager used in jailbroken environments to access the iOS file system.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tigisoftware.com/default/?page_id=78">Filza – TIGI Software</a></li>
<li><a href="https://redfoxsecurity.medium.com/locked-in-a-box-how-ios-sandboxing-challenges-pentesters-8207476da296">Locked in a Box : How iOS Sandboxing Challenges Pentesters | Medium</a></li>

</ul>
</details>

**Tags**: `#iOS security`, `#sandbox escape`, `#vulnerability`, `#Filza`, `#jailbreak`

---

<a id="item-14"></a>
## [ASML Plans Price Hikes; TSMC Resists, Chinese Firms Accept 10% DUV Increase](https://news.bloomberglaw.com/artificial-intelligence/asml-plans-price-increases-on-chipmaking-equipment-information) ⭐️ 8.0/10

ASML announced plans to raise prices for its EUV and DUV lithography equipment, with EUV capacity booked through 2027. TSMC is resisting the EUV price increase, while some Chinese chipmakers have accepted a 10% hike on DUV tools. ASML's pricing power reflects its near-monopoly in advanced lithography, crucial for semiconductor fabrication. The move could widen the gap between leading-edge and mature-node chipmakers, with geopolitical implications as Chinese firms accept DUV hikes amid export restrictions. ASML CFO Roger Dassen cited strong pricing power; EUV systems are fully booked until end of 2027. The DUV price increase of 10% has been agreed to by some Chinese customers, while negotiations with TSMC over EUV pricing remain contentious.

telegram · zaihuapd · Jul 15, 16:49

**Background**: Lithography equipment is essential for printing circuit patterns on silicon wafers. EUV (extreme ultraviolet) lithography, using 13.5 nm light, enables the smallest features in advanced chips (e.g., 5nm, 3nm nodes) and is exclusively produced by ASML. DUV (deep ultraviolet) lithography, using 193 nm light, is widely used for less critical layers and mature nodes. ASML's dominance in EUV and strong position in DUV give it significant leverage over chipmakers globally.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/EUV_lithography">EUV lithography</a></li>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://www.asml.com/en/products/euv-lithography-systems">EUV lithography systems – Products | ASML</a></li>

</ul>
</details>

**Tags**: `#semiconductor`, `#ASML`, `#chip manufacturing`, `#pricing`, `#geopolitics`

---