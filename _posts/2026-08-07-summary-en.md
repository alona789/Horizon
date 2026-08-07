---
layout: default
title: "Horizon Summary: 2026-08-07 (EN)"
date: 2026-08-07
lang: en
---

> From 36 items, 14 important content pieces were selected

---

1. [DeepSeek V4 Flash 0731 launches with low cost and fast local inference](#item-1) ⭐️ 8.0/10
2. [Tech&\#x27;s Sadness: When Workers Lose Faith in Their Careers](#item-2) ⭐️ 8.0/10
3. [Oracle Bans AI-Generated Code From OpenJDK, Citing Copyright and Review Burden](#item-3) ⭐️ 8.0/10
4. [Making Postgres 300x Faster for Analytics with Batching, Fusion, SIMD](#item-4) ⭐️ 8.0/10
5. [Cloudflare launches Kitesurf: agent-first browser on V8 isolates](#item-5) ⭐️ 8.0/10
6. [2027 Memory Capacity Sold Out as HBM Squeezes DRAM Supply](#item-6) ⭐️ 8.0/10
7. [A Year of Fighting Scrapers on a 1.5-Million-Page Website](#item-7) ⭐️ 8.0/10
8. [New Mexico court orders Meta to pay $567m over children&\#x27;s mental health harms](#item-8) ⭐️ 8.0/10
9. [Codex + GPT-5.6 Sol Ultra Builds Better Raccoon Heist Game Than Claude Fable 5](#item-9) ⭐️ 8.0/10
10. [SemiAnalysis: Gemini Struggles, GCP Gains Short-Term from AI Demand](#item-10) ⭐️ 8.0/10
11. [SEC Approves Nasdaq 23-Hour Trading, Launching December 6](#item-11) ⭐️ 8.0/10
12. [US Probes Chinese AI Firms&\#x27; Offshore Access to Nvidia Chips](#item-12) ⭐️ 8.0/10
13. [Sub2API OAuth Flaw Allows Account Takeover with Just an Email](#item-13) ⭐️ 8.0/10
14. [OpenAI Says Upcoming Astra Model May Reach &\#x27;Critical&\#x27; Cyber Capability Threshold](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek V4 Flash 0731 launches with low cost and fast local inference](https://arcprize.org/results/deepseek-v4-flash-0731) ⭐️ 8.0/10

DeepSeek released the V4 Flash 0731 model on July 31, an update to its efficiency-focused V4 Flash line that succeeds the earlier preview. The model combines strong performance with very low API costs and fast local inference speeds. This release makes near-frontier model quality accessible at a cost low enough that developers can treat token usage as negligible, which could accelerate the shift toward open-weight models over pricey proprietary APIs. Its local speed also expands practical options for privacy-sensitive or offline deployments. DeepSeek V4 Flash is a Mixture-of-Experts model with 284B total parameters and 13B activated, supporting a 1M-token context window. The 0731 designation marks the July 31 release, a distinct update from the earlier &\#x27;preview&\#x27;; local users report roughly 8k tokens/s prefill and around 250 tokens/s generation on a single stream with dual RTX Pro 6000 Blackwell GPUs.

hackernews · tosh · Aug 7, 17:56 · [Discussion](https://news.ycombinator.com/item?id=49214008)

**Background**: DeepSeek V4 Flash is designed as an efficiency-optimized model for reasoning across a 1M-token context, and its size makes it feasible for both API use and local inference. The ARC Prize is a nonprofit initiative that uses benchmarks and prizes to accelerate open-source artificial general intelligence research, and it now hosts results for this model.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek -ai/ DeepSeek - V 4 - Flash · Hugging Face</a></li>
<li><a href="https://ollama.com/library/deepseek-v4-flash">deepseek - v 4 - flash</a></li>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-flash">DeepSeek V 4 Flash - API Pricing &amp; Benchmarks | OpenRouter</a></li>

</ul>
</details>

**Discussion**: Commenters are largely enthusiastic: one says the model is &\#x27;good enough to use it for \(almost\) everything&\#x27; and hard to spend more than $5 per day even with many active sessions, while another reports that the 07/31 update &\#x27;feels like a whole tier up&\#x27; with excellent debugging and analysis abilities. However, another user notes issues with infinite loops and tool calls not being executed, wasting tokens compared with the previous V4 Flash version.

**Tags**: `#AI`, `#LLM`, `#DeepSeek`, `#Model Release`, `#ARC Prize`

---

<a id="item-2"></a>
## [Tech&\#x27;s Sadness: When Workers Lose Faith in Their Careers](https://www.noemamag.com/why-is-everyone-in-tech-so-sad/) ⭐️ 8.0/10

Noema Magazine published an article asking why so many tech workers feel sad, examining career disillusionment across the industry. The piece resonated widely, earning 333 points and 475 comments on aggregator sites. The discussion signals a major cultural shift in tech, where workers once full of optimism now doubt their place. If an entire class loses faith, it could affect innovation, retention, and how society views tech careers. Commenters drew historical parallels, such as the decline of the printing trade, and pointed to online toxicity as a factor. The article itself includes personal accounts and industry-wide analysis rather than specific data.

hackernews · RickJWagner · Aug 7, 12:42 · [Discussion](https://news.ycombinator.com/item?id=49209539)

**Background**: Tech careers have long been seen as stable, high-status, and lucrative. In recent years, factors like layoffs, burnout, and a changing public perception have contributed to a growing sense of disillusionment. This article explores that mood, connecting personal stories to larger industry trends.

**Discussion**: Animats compared tech&\#x27;s decline to the printing trade, noting workers eventually lose everything. marginalia\_nu highlighted the toxic nature of the modern web, while dec0dedab0de said it was the least he has cared about in 20 years. Havoc found the article&\#x27;s tone gleeful but saw societal value in the discussion.

**Tags**: `#tech culture`, `#burnout`, `#software engineering`, `#career`, `#mental health`

---

<a id="item-3"></a>
## [Oracle Bans AI-Generated Code From OpenJDK, Citing Copyright and Review Burden](https://app.dealroom.co/news/feed/oracle-bans-ai-generated-code-from-openjdk-despite-ellison-s-claim-oracle-isn-t-writing-its-own-code) ⭐️ 8.0/10

Oracle has issued an interim policy banning AI-generated code from OpenJDK contributions, according to a post at openjdk.org/legal/ai. The policy is temporary, and Oracle&\#x27;s lawyers are drafting a final version. This decision could set a precedent for how major open-source projects handle AI-assisted contributions, especially given the legal uncertainty around AI-generated code. It also highlights the tension between Oracle&\#x27;s aggressive AI investments and its role as steward of Java&\#x27;s open-source implementation. The interim policy says AI-generated code could create copyright uncertainty and place an undue burden on &\#x27;the already limited time of human reviewers.&\#x27; The final policy is being written by Oracle&\#x27;s legal team, according to the OpenJDK page.

hackernews · delduca · Aug 7, 17:36 · [Discussion](https://news.ycombinator.com/item?id=49213754)

**Background**: OpenJDK is a free and open-source implementation of the Java Platform, Standard Edition \(Java SE\), originating from a Sun Microsystems initiative in 2006. Oracle acquired Sun in 2010 and has since overseen OpenJDK, which serves as the basis for many production Java distributions, including Oracle JDK and Red Hat builds.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenJDK">OpenJDK - Wikipedia</a></li>
<li><a href="https://www.azul.com/blog/what-is-openjdk/">What is OpenJDK &amp; What is it Used For? | Azul</a></li>
<li><a href="https://www.redhat.com/en/topics/application-modernization/openjdk-vs-oracle-jdk">OpenJDK versus Oracle JDK</a></li>

</ul>
</details>

**Discussion**: Commenters linked to the primary sources and generally saw the move as pragmatic, though several noted the irony. One argued Oracle&\#x27;s legal side is protecting its ability to sue over AI-generated proprietary code, while another joked that the release notes have likely been written by AI for a year already.

**Tags**: `#Oracle`, `#OpenJDK`, `#AI-generated code`, `#Open Source Policy`, `#Java`

---

<a id="item-4"></a>
## [Making Postgres 300x Faster for Analytics with Batching, Fusion, SIMD](https://malisper.me/how-we-made-postgres-hundreds-of-times-faster-the-query-engine/) ⭐️ 8.0/10

The author of pgrust details how batching, operator fusion, and SIMD can make Postgres analytics queries hundreds of times faster, while using formal verification and differential fuzz testing to guarantee correctness. If the performance claims hold, Postgres could handle analytics workloads that currently require specialized column-store or vectorized databases. The approach also shows how data-centric query compilation can be applied to mature database systems like Postgres. The project is called pgrust, and the author has reportedly proved more than 1,000 user-facing functions behave identically to Postgres. Operator fusion in query engines can often yield gains of 1.7x to 2.5x alone, so the reported 300x speedup likely combines multiple techniques.

hackernews · poly2it · Aug 7, 11:00 · [Discussion](https://news.ycombinator.com/item?id=49208535)

**Background**: PostgreSQL is a general-purpose relational database that historically favors OLTP workloads, and its row-at-a-time execution model can hinder analytical queries. Operator fusion combines multiple query operators into a loop to reduce per-row overhead, while SIMD \(single instruction, multiple data\) lets a CPU process several data elements in a single instruction. Differential fuzzing runs the same inputs through two implementations and compares outputs to find mismatches without needing a hand-written oracle.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Differential_testing">Differential testing - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Single_instruction,_multiple_data">Single instruction, multiple data - Wikipedia</a></li>
<li><a href="https://db.cs.cmu.edu/papers/2017/p1-menon.pdf">Relaxed Operator Fusion for In-Memory Databases:</a></li>

</ul>
</details>

**Discussion**: Commenters are skeptical that users will adopt pgrust over Postgres, citing trust in the core team and project longevity rather than raw performance. Some praise adaptive planning as a long-awaited feature that could prove its viability outside academic contexts, and others ask for a deeper architecture overview of the IO and thread schedulers.

**Tags**: `#postgres`, `#database`, `#performance`, `#SIMD`, `#query-engine`

---

<a id="item-5"></a>
## [Cloudflare launches Kitesurf: agent-first browser on V8 isolates](https://blog.cloudflare.com/kitesurf/) ⭐️ 8.0/10

Cloudflare announced Kitesurf, an agent-first browser that runs entirely within V8 isolates on Cloudflare Workers. Built on the open-source Blitz engine, it is designed for browser automation and AI agents on Cloudflare&\#x27;s global network. This matters because it brings a full browser runtime to Cloudflare&\#x27;s edge platform, enabling AI agents to perform web automation, scraping, and testing with low latency and high scalability. It also raises questions about Cloudflare&\#x27;s dual role as both a CDN with anti-bot protection and a platform for agent-driven browsing. Kitesurf is stateless, highly scalable, and cost-effective, running entirely on Workers. It is built on Blitz, an open-source modular web engine written in Rust by DioxusLabs, which is currently in alpha and not yet production-ready.

hackernews · m3h · Aug 7, 10:42 · [Discussion](https://news.ycombinator.com/item?id=49208393)

**Background**: V8 isolates are isolated execution contexts for running JavaScript, and Cloudflare Workers uses them to run serverless functions with high density and security. Blitz is a radically modular web engine that provides HTML/CSS rendering and can be embedded or combined with other components. Agent-first browsers are designed to let AI agents interact with web pages programmatically, performing actions and extracting data without human intervention.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.cloudflare.com/kitesurf/">Introducing Kitesurf : The agent - first browser that... | Cloudflare Blog</a></li>
<li><a href="https://github.com/DioxusLabs/blitz">GitHub - DioxusLabs/blitz: A radically modular HTML/CSS rendering engine · GitHub</a></li>
<li><a href="https://medium.com/@adityashete009/v8-isolates-for-serverless-functions-a-game-changer-0e8355cf7ac9">V8 isolates for Serverless Functions? A game changer | by Aditya Shete | Medium</a></li>

</ul>
</details>

**Discussion**: Community comments include nicoburns noting that Kitesurf is built on Blitz, which he has been developing for 2.5 years, and that Cloudflare intends to open source and upstream their patches. minraws expresses concern about Cloudflare&\#x27;s dual role as a CDN and an agent platform, while QuantumNomad\_ asks whether Cloudflare&\#x27;s anti-bot systems will block its own browser instances. cautiouscat questions practical use cases for browser agents, and ako makes a lighthearted comment about kitesurfing being outdated.

**Tags**: `#browser`, `#cloudflare`, `#web-automation`, `#v8`, `#browser-engine`

---

<a id="item-6"></a>
## [2027 Memory Capacity Sold Out as HBM Squeezes DRAM Supply](https://www.ign.com/articles/ramageddon-continues-another-year-as-2027-memory-capacity-is-reportedly-sold-out) ⭐️ 8.0/10

Reports indicate that memory production capacity for 2027 is already fully sold out, driven by high-bandwidth memory \(HBM\) manufacturing consuming an outsized share of semiconductor wafer capacity. This leaves less room for conventional memory types such as DDR5. This signals prolonged memory shortages and rising prices for both AI hardware and consumer PCs. It also highlights how AI-driven demand for HBM is fundamentally reshaping the memory industry&\#x27;s production priorities. According to industry analysis, HBM3E consumes roughly three times the wafer supply as DDR5 to produce a given number of bits at the same technology node. HBM dies must also be larger than ordinary DRAM dies because of the final 3D packaging process.

hackernews · inigyou · Aug 7, 07:58 · [Discussion](https://news.ycombinator.com/item?id=49207236)

**Background**: High Bandwidth Memory \(HBM\) is a 3D-stacked DRAM interface developed by Samsung, AMD, and SK Hynix, designed for high-performance computing applications such as AI accelerators. Wafer capacity refers to the number of silicon wafers a fab can process, and because HBM stacks multiple dies vertically and requires more wafer area per bit, ramping up HBM production constrains the industry&\#x27;s ability to grow output of non-HBM memory like DDR5.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://www.techtimes.com/articles/317859/20260606/sk-hynix-dram-capacity-roadmap-revealed-yongin-alone-adds-360k-wafers-monthly.htm">SK hynix DRAM Capacity Roadmap Revealed: Yongin Alone Adds...</a></li>

</ul>
</details>

**Discussion**: Commenters largely focused on the HBM-versus-DDR5 trade-off, with one noting that one unit of HBM capacity consumes roughly the wafer capacity that could have produced three DDR5 units. Others expressed frustration over rising RAM prices and AI-driven memory demand, while some suggested the industry needs a universal memory standard like USB to reuse older sticks.

**Tags**: `#memory`, `#HBM`, `#semiconductors`, `#supply-chain`, `#AI-hardware`

---

<a id="item-7"></a>
## [A Year of Fighting Scrapers on a 1.5-Million-Page Website](https://patronview.com/news/99-percent-of-my-website-traffic-is-bots/) ⭐️ 8.0/10

The author of a 1.5-million-page website details a year-long battle against bot traffic, revealing that a single bad month spiked hosting costs by roughly 500% above the usual $90 monthly bill. The post also admits the site itself scrapes public documents, adding irony to the complaint. This story underscores the financial and operational toll that AI crawlers and scrapers impose on independent web publishers. It also raises broader questions about relying on centralized services like Cloudflare to decide who can access a site, and whether alternative approaches such as proof-of-work challenges are more sustainable. The cost spike was linked to Cloudflare&\#x27;s D1 database, not just bandwidth. Commenters suggest dropping D1 for a static site, and point to Anubis, a proof-of-work challenge that validates real browser software, as an effective mitigation for sites not behind a CDN. One commenter measured Claude-searchbot fetching ~205,000 pages in 72 hours while sending only one referral.

hackernews · petercooper · Aug 7, 14:51 · [Discussion](https://news.ycombinator.com/item?id=49211386)

**Background**: Scrapers and bots are automated programs that crawl websites, sometimes for indexing, price monitoring, or AI training data, but they can generate huge amounts of traffic and cost. Bot mitigation ranges from static request analysis to behavioral fingerprinting and AI-based detection at the edge, as offered by Akamai and others. Cloudflare&\#x27;s Bot Fight Mode is a popular free option, but it can also block legitimate AI crawlers and raises concerns about centralized control. Residential proxies allow scrapers to evade IP-based blocking, making the arms race more difficult for site owners.

<details><summary>References</summary>
<ul>
<li><a href="https://www.imperva.com/learn/application-security/what-are-bots/">What are Bots | Bot Types &amp; Mitigation Techniques | Imperva</a></li>
<li><a href="https://community.cloudflare.com/t/community-tip-bot-fight-mode/117572">Community Tip - Bot Fight Mode - Tutorial - Cloudflare Community</a></li>
<li><a href="https://brightdata.com/">Bright Data - All in One Platform for Proxies and Web Scraping</a></li>

</ul>
</details>

**Discussion**: The comments mix concern and practical advice. Some worry that outsourcing bot decisions to Cloudflare undermines the open web, while others recommend alternatives like Anubis or moving to static hosting. There is also frustration over AI crawlers receiving content without compensation, as well as acknowledgment that many sites, including this one, are themselves scrapers.

**Tags**: `#web scraping`, `#bot mitigation`, `#cloudflare`, `#devops`, `#cost optimization`

---

<a id="item-8"></a>
## [New Mexico court orders Meta to pay $567m over children&\#x27;s mental health harms](https://www.theguardian.com/technology/2026/aug/06/new-mexico-court-meta) ⭐️ 8.0/10

A New Mexico court ruled against Meta, ordering it to pay $567 million \(some outlets report $942 million total\) for harming children&\#x27;s mental health through its social media platforms. The judgment found Meta violated the state&\#x27;s public-nuisance law and required changes for underage users. This is one of the largest state-level rulings against a major social media company and a significant test of using public-nuisance law to regulate online platforms. It could encourage other jurisdictions to pursue similar litigation against tech companies over child safety and mental health. The exact amount differs across reports: Reuters and The Guardian cite $567 million for a teen mental-health fund, while The Wall Street Journal reports $942 million, likely including additional fees or remedies. The order also requires Meta to make changes for underage users. Commenters noted the ruling cited New Mexico&\#x27;s public-nuisance law \(NMSA 1978 § 30-8-1\).

hackernews · boplicity · Aug 7, 00:06 · [Discussion](https://news.ycombinator.com/item?id=49204352)

**Background**: Public nuisance law traditionally addresses activities that harm public health, safety, morals, or welfare, or interfere with public rights. Using it against social media companies is a novel legal strategy; prior cases generally targeted physical nuisances like pollution or dangerous properties. This ruling could set a precedent for holding platforms accountable for algorithm-driven harms to minors.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Public_nuisance">Public nuisance - Wikipedia</a></li>
<li><a href="https://www.lawandjusticewiki.org/wiki/Public_nuisance">Public nuisance - Justice Definitions Project</a></li>

</ul>
</details>

**Discussion**: Commenters had mixed reactions: some argued the fine is a &\#x27;slap on the wrist&\#x27; relative to Meta&\#x27;s revenue, while others pointed out that for a small state like New Mexico, $942 million is proportionally enormous. One commenter noted the ruling cited the specific public-nuisance statute, and another called Instagram Reels and TikTok &\#x27;online versions of heroin&\#x27; for their addictive design. A common concern was that the penalty might still be treated as just a &\#x27;cost of doing business.&\#x27;

**Tags**: `#Meta`, `#legal`, `#mental-health`, `#regulation`, `#social-media`

---

<a id="item-9"></a>
## [Codex + GPT-5.6 Sol Ultra Builds Better Raccoon Heist Game Than Claude Fable 5](https://simonwillison.net/2026/Aug/7/moonlight-mayhem/#atom-everything) ⭐️ 8.0/10

Simon Willison ran the exact same “Raccoon Heist” prompt on Codex Desktop with GPT-5.6 Sol Ultra, producing a much better game called “Moonlight &amp; Mayhem.” The game features a museum heist where raccoon crewmates stack to steal a golden sardine, unlike Claude Fable 5&\#x27;s simpler back yard coin-collecting version. This head-to-head comparison shows GPT-5.6 Sol Ultra with Codex sub-agents outperforming Claude Fable 5 on one-shot game generation, signaling rapid progress in agentic coding. AI/ML developers can use this as a practical benchmark when choosing models for long-horizon, multi-step creative tasks. Codex spent 52 minutes on the project and generated textures using gpt-image-2; the session would have cost about $23.28 at full API prices. The initial one-shot output had a bug where raccoons had giant sphere-like eyeballs, which Codex failed to catch despite reviewing screenshots; Simon fixed it by asking “Why do the raccoons have huge black spheres on them?” and then “Fix it.”

rss · Simon Willison · Aug 7, 19:18

**Background**: GPT-5.6 Sol is OpenAI&\#x27;s latest coding model; Sol Ultra is the max-reasoning mode that aggressively uses sub-agents, setting new state-of-the-art results on coding benchmarks. Codex is OpenAI&\#x27;s agentic coding tool that can spawn sub-agents for parallel work with individual instructions and tool context. Claude Fable 5 is Anthropic&\#x27;s most powerful generally available model, released in June 2026. Simon previously had Claude Fable 5 build a working game from a premise generated by GPT-3 and DALL-E four years ago, which became the basis for this comparison.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/gpt-5-6/">GPT - 5 . 6 : Frontier intelligence that scales with your ambition | OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Codex`, `#GPT`, `#Claude`, `#game-generation`

---

<a id="item-10"></a>
## [SemiAnalysis: Gemini Struggles, GCP Gains Short-Term from AI Demand](https://newsletter.semianalysis.com/p/gemini-is-cooked-but-gcp-is-cooking) ⭐️ 8.0/10

SemiAnalysis published an analysis arguing that Google&\#x27;s Gemini AI model is strategically failing in the long term, but Google Cloud Platform \(GCP\) is benefiting in the short term from the infrastructure demand generated by this AI race. The article frames this as DeepMind&\#x27;s long-term failure being GCP&\#x27;s short-term gain. This perspective highlights an internal divergence inside Alphabet: DeepMind&\#x27;s struggles with Gemini contrast with GCP&\#x27;s commercial momentum. It matters because it affects how Google competes with cloud and AI rivals like Microsoft/OpenAI and Amazon, and could reshape investor perceptions of Alphabet&\#x27;s AI strategy. The analysis comes from SemiAnalysis, a well-known independent research firm focused on AI, semiconductors, and cloud infrastructure. The article&\#x27;s core claim is that even if Gemini loses the model-quality race, the massive compute demand for training and inference still flows to GCP, providing short-term revenue tailwinds.

rss · Semianalysis · Aug 7, 02:32

**Background**: Google DeepMind is Alphabet&\#x27;s AI research lab, formed in 2023 from a merger of DeepMind and Google Brain, and is responsible for developing the Gemini family of large language models. Google Cloud Platform \(GCP\) is Alphabet&\#x27;s cloud computing arm, which competes with AWS and Microsoft Azure. SemiAnalysis is a subscription-based analytical firm known for deep technical reports on AI hardware and cloud economics, often cited in industry discussions.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepMind">DeepMind</a></li>
<li><a href="https://x.com/SemiAnalysis_">SemiAnalysis (@SemiAnalysis_) on X</a></li>

</ul>
</details>

**Tags**: `#Google`, `#AI`, `#cloud computing`, `#Gemini`, `#GCP`

---

<a id="item-11"></a>
## [SEC Approves Nasdaq 23-Hour Trading, Launching December 6](https://finance.sina.com.cn/stock/bxjj/2026-08-07/doc-inimnkup0012339.shtml) ⭐️ 8.0/10

The SEC has approved Nasdaq&\#x27;s 23-hour-per-day trading schedule \(23/5\), which will go live on December 6, 2026. The market will close for only one hour each day, from 8:00 to 9:00 PM ET, for settlement and data processing. This marks a significant regulatory step toward near-24/7 US equity trading on a major exchange, with broad implications for market infrastructure, algorithmic trading systems, and global investors. It may accelerate moves by other exchanges and reshape how and when participants trade US stocks. The daily one-hour halt \(20:00–21:00 ET\) is reserved for clearing and data processing. NYSE Arca had earlier received accelerated SEC approval for 22-hour trading, while Cboe has submitted a near-24x5 proposal, all targeting December 2026.

telegram · zaihuapd · Aug 7, 10:03

**Background**: US exchanges traditionally operate from 9:30 AM to 4:00 PM Eastern, plus limited pre- and after-hours sessions. Overnight trading has been growing through alternative trading systems \(ATSs\) such as Blue Ocean ATS, which launched in 2021 and lets retail investors trade US stocks during Asian business hours. The SEC is scheduled to hold a roundtable on September 17 to discuss investor-protection issues related to near-24-hour markets.

<details><summary>References</summary>
<ul>
<li><a href="https://www.fastcompany.com/91293088/nasdaq-stock-market-trading-24-hour-new-schedule-challenging?ref=upstract.com">Nasdaq 24/ 5 trading ? New stock market hours could... - Fast Company</a></li>
<li><a href="https://www.blueocean-tech.io/blue-ocean-ats/">Blue Ocean ATS – Blue Ocean Technologies LLC</a></li>
<li><a href="https://www.investor.gov/introduction-investing/investing-basics/glossary/alternative-trading-systems-atss">Alternative Trading Systems (ATSs) | Investor.gov</a></li>

</ul>
</details>

**Tags**: `#finance`, `#trading`, `#SEC`, `#Nasdaq`, `#market infrastructure`

---

<a id="item-12"></a>
## [US Probes Chinese AI Firms&\#x27; Offshore Access to Nvidia Chips](https://www.bloomberg.com/news/articles/2026-08-07/us-reviews-china-s-offshore-access-to-nvidia-chips-after-ai-breakthroughs) ⭐️ 8.0/10

The US Commerce Department&\#x27;s Bureau of Industry and Security \(BIS\) has launched a systematic review of how Chinese AI companies obtain and use Nvidia chips offshore, including via remote cloud access. This follows the release of Moonshot AI&\#x27;s Kimi K3 model, which a White House official accused of illegally using Nvidia chips accessed remotely through Thailand. The review could reshape AI compute supply chains and export controls, potentially granting BIS new authority over cloud computing agreements. It has major implications for the AI industry, international relations, and cloud providers worldwide. The review includes compiling two lists: countries where black markets smuggle restricted chips into China, and countries where Chinese firms remotely rent chips. The US House has passed a bipartisan bill to grant BIS explicit enforcement power, but it faces expected opposition from Nvidia and other tech companies.

telegram · zaihuapd · Aug 7, 11:18

**Background**: The US has restricted advanced Nvidia chip exports to China since October 2022 to slow China&\#x27;s military and surveillance AI capabilities. Remote access to cloud-based chips is not itself illegal, creating a legal gray area that BIS is now investigating. Alibaba is reportedly involved through a Singapore shell company using Nvidia chips in Malaysia via the US-investigated firm Megaspeed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bis.gov/">Homepage | Bureau of Industry and Security</a></li>
<li><a href="https://thepulsegazette.com/article/china-ai-chip-smuggling-indictments">DOJ Indicts 12 for Smuggling AI Chips to China - The Pulse Gazette</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Nvidia`, `#Export Controls`, `#Geopolitics`, `#Semiconductors`

---

<a id="item-13"></a>
## [Sub2API OAuth Flaw Allows Account Takeover with Just an Email](https://github.com/Wei-Shaw/sub2api/issues/5350) ⭐️ 8.0/10

A critical OAuth account-takeover vulnerability \(CVE-2026-27812, CVSS 8.8\) was disclosed in sub2api v0.1.171 and earlier. An attacker who knows only the victim&\#x27;s email address can bind their own OAuth identity to the victim&\#x27;s account without a password, verification code, or any user interaction. This vulnerability gives full control of API keys, billing balance, and subscription quotas, affecting any user of sub2api, a tool that aggregates AI API capabilities. Because exploitation is trivial and silent, immediate upgrades or mitigations are essential for all deployments. The flaw lies in the pending-session flow&\#x27;s existingUser branch, which fails to verify the password or captcha when attaching an OAuth identity. The attacker sets the target user ID to the victim&\#x27;s, completes the OAuth binding once, and thereafter every OAuth login resolves to the victim&\#x27;s account.

telegram · zaihuapd · Aug 7, 14:59

**Background**: OAuth 2.0 is a widely used authentication standard that lets users log in via third-party providers like Google or GitHub. When an application adds OAuth to an existing account, it must confirm that the current user actually owns that account; otherwise, attackers can hijack accounts by taking over the pending-session exchange. This type of &\#x27;account linking&\#x27; vulnerability is a known OAuth pitfall covered in security training like PortSwigger&\#x27;s Web Security Academy.

<details><summary>References</summary>
<ul>
<li><a href="https://linux.do/t/topic/2721334">sub2api 曝 OAuth ... - LINUX DO</a></li>
<li><a href="https://www.sentinelone.com/vulnerability-database/cve-2026-27812/">CVE-2026-27812: Sub2API Auth Bypass Vulnerability</a></li>
<li><a href="https://portswigger.net/web-security/oauth">OAuth 2.0 authentication vulnerabilities | Web Security Academy</a></li>

</ul>
</details>

**Tags**: `#security`, `#oauth`, `#vulnerability`, `#account-takeover`, `#sub2api`

---

<a id="item-14"></a>
## [OpenAI Says Upcoming Astra Model May Reach &\#x27;Critical&\#x27; Cyber Capability Threshold](https://openai.com/index/responding-next-frontier-critical-cyber-capabilities/) ⭐️ 8.0/10

On August 7, 2026, OpenAI disclosed that internal evaluations of its upcoming Astra model showed enough progress in agentic coding and cybersecurity that the company cannot rule out it meeting the &\#x27;critical&\#x27; cyber capability threshold—a level not reached by previous models such as GPT-5.6-Sol. As a result, OpenAI paused non-compliant internal activities and expanded safety testing, which may delay Astra&\#x27;s release. This is significant because &\#x27;critical&\#x27; capability would mean Astra could autonomously discover and exploit zero-day vulnerabilities in hardened systems or execute novel end-to-end cyberattacks without human oversight. The decision could set a precedent for how frontier AI labs handle near-threshold models and balance release timelines against catastrophic risk. OpenAI has suspended internal Astra activities that do not meet strengthened security requirements, and is implementing isolated testing environments, enhanced encryption, and universal monitoring. It will also conduct third-party testing with government agencies and AI safety organizations.

telegram · zaihuapd · Aug 7, 16:44

**Background**: OpenAI&\#x27;s Preparedness Framework categorizes frontier models by risk levels, with &\#x27;critical&\#x27; reserved for capabilities like autonomous zero-day exploitation. Astra is reportedly OpenAI&\#x27;s next major model family, confirmed on August 1, 2026, and has already shown notable results in solving open math problems. The framework&\#x27;s thresholds inform when models require special safeguards or delayed deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://cdn.openai.com/pdf/18a02b5d-6b67-4cec-ab64-68cdfbddebcd/preparedness-framework-v2.pdf">Preparedness Framework</a></li>
<li><a href="https://mykreatool.com/en/news/openai-astra-ii-agenty-reshenie-zadach">OpenAI Astra Model Solves 10 Open Math Problems — MyKreaTool</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#AI safety`, `#cybersecurity`, `#Astra`, `#model evaluation`

---